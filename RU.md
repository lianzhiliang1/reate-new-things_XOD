---
title: Документация XOD
version: 1.0.0
---

# Документация XOD

Этот репозитарий содержит исходный код документации [XOD](https://github.com/xodio/xod/) которая распологается по адресу https://xod.io/docs/

## Структура документов

Весь исходный контент находится в каталоге `./docs`. Каждый подкаталог (как и основной `./docs`) соответствует отдельной странице на https://xod.io/docs/. Если пользователь открывает страницу `https://xod.io/docs/foo/bar/`, то система ищет файл в `./docs/foo/bar/README.md`.

Файл `README.md` является точкой входа каждой страницы. Это файл оформляется синтаксисом [`Markdown`](https://www.markdownguide.org/), так что каждый автор может сосредоточиться на содержании документа, а не вдаваться в тонкости компоновки. Тем не менее, `README.md` может содержать чистый HTML и шаблоны Handlebars для тех случаев, когда страницу тяжело описывать на Markdown. Как и следовало ожидать, `README.md` может ссылаться на изображения и файлы, которые располагаются рядом с ним.

### Переводы

Страницы могут быть написаны на разных языках. `README.md` всегда содержит английскую версию, перевод на другие языки должен располагаться в этом же каталоге в соответствующих файлах: `DE.md`, `IT.md`, `UA.md` и т.д. Система открывает нужный файл в зависимости от выбранного языка на сайте. Если перевод не найден, то открывается английская версия страницы.

### Форматирование YAML

Некоторые страницы, например как [Поддерживаемое оборудование](./docs/reference/supported-hardware) содержат сложно структурированные данные ([так это выглядит в живую на сайте xod.io](https://xod.io/docs/reference/supported-hardware/)), которые тяжело описывать на обычном Markdown/HTML.

В этих случаях приходит на выручку [YAML](https://en.wikipedia.org/wiki/YAML). Структура объекта, описанная на нём, превращается в Markdown с использованием небольшой шаблонной магии:

```html
{{#each index}}
<h2>{{ section }}</h2>
{{#each parts}}
<div>
  {{ part }} {{ kind }} {{#if vendor}}от {{ vendor }}{{/if}}.
</div>
{{/each}} {{/each}}
```

Обратите внимание на теги `{{ xxx }}`. Это инструкции для [Handlebars](https://handlebarsjs.com/). Любой `.yaml` файл, расположенный рядом с `README.md`, доступен из шаблонов по имени (`index` для [`index.yaml`](./docs/reference/supported-hardware/index.yaml), как указано в примере выше).

## Форматирование Markdown

Есть несколько простых правил для поддержания всех исходных файлов в согласованности и лёгкости обслуживания. Особенно важно, чтоб все Markdown файлы содержали строки не длиннее 80 символов.

Вместо описания всех правил и проверки их на ревью, примените их автоматически через [Prettier](https://prettier.io/). После завершения существенной части работы запустите `yarn prettier` для правильного форматирования вашего Markdown.

### Вводная часть

Первое, что вы увидите в исходных файлах Markdown, будет блок, начинающийся с `---`. Это метаданные для движка сайта:

```Markdown
---
title: Hello World
version: 1.2.3
---
```

Поле `title` передаётся в браузер для отображения заголовока страницы (`<title/>`).

Поле `version` - это [семантическая версия](https://semver.org/) текущей страницы для понимания того, что изменилось и как сильно текущий перевод отстаёт от мастер версии. Увеличение цифры в части (`3`) указывает на орфографические и стилистические правки, которые не требуют корректировки перевода. Изменение в минорной части (`2`) говорит о том, что в тексте были добавления и улучшения, которые нужно применить в переведённой версии документа. Смена мажорной части версии (`1`) указывает на полное изменение документа. Если поле `version` не указано, то по умолчанию принимается версия `1.0.0`.

## Обслуживание

```bash
$ yarn prettier:all
# Форматирует *все* Markdown в репозитарии

$ yarn prettier README.md CONTRIBUTING.md
# Форматирует только указанные файлы

$ yarn prettier-check:all
# Проверяет все Markdown в репозитарии
```

## Лицензия

Весь контент доступен под лицензией Creative Commons license.

## Как внести свой вклад

Любая помощь в исправлении грамматики, перевода, разрешении двусмысленностей, добавлении ссылок и общих улучшений очень ценится. Как это правильно сделать читайте в [CONTRIBUTING_RU.md](./CONTRIBUTING_RU.md).