---
title: XOD Documentation
version: 1.2.0
---

<style>
/* Force linked headers to be black, not blue */
h2 a {
  color: black;
  text-decoration: underline;
}

h2.icon.header {
  padding: 1.5em 0 0.5em 0;
}

/* Style for tutorial/guide/reference icons */
.ui.icon.header img {
  width: 64px;
  opacity: 0.4;
}

#showcase-cards .card {
  width: 340px;
}

/* No space below a card image */
#showcase-cards .image {
  font-size: 0;
}

/* Keep all images the same size */
#showcase-cards .card img {
  width: 100%;
  height: 191px; /* Aspect ratio 16/9 for 340px width */
  object-fit: cover;
}
</style>

# XOD Documentation

<div class="ui three column doubling stackable horizontally padded grid">

<!------------------------ Tutorial ------------------------->
<div class="column">
<h2 class="ui icon header">
  <a href="./tutorial/">
    <img src="./__img__/tutorial.svg" />
  </a>
  <div class="content">
    <a href="./tutorial/">Tutorials</a>
  </div>
</h2>

<h3 class="ui header">Official</h3>

- [Get started](./tutorial/install/)
- [Full index](./tutorial/) (42 chapters)

<style>
  .banner-colony-kit {
    position: relative;
    display: block;

    width: 100%;
    height: auto;
    background: rgb(55,55,55);
    background: linear-gradient(0deg, rgba(36,36,36,1) 0%, rgba(55,55,55,1) 50%, rgba(59,59,59,1) 100%);

    border-radius: 4px;
    padding: .5em .5em 1em 5em;
    cursor: pointer;
  }
  .banner-colony-kit:before {
    position: absolute;
    content: '';
    display: block;
    z-index: 0;
    width: 90px;
    height: 90px;
    left: .5em;
    top: .5em;

    background-image: url(./__img__/colony-kit.png);
    background-repeat: no-repeat;
    background-size: contain;
  }
  .banner-colony-kit * {
    color: #fff;
    font-size: .8em;
  }
  .banner-colony-kit p {
    font-size: .66em;
  }

</style>
<a href="https://my.amperka.com/kits/colony-kit?utm_source=site&utm_medium=docs&utm_campaign=tutorial" class="banner-colony-kit">
  <h3>Amperka Colony Kit</h3>
  <p>
    Alternative XOD tutorial with a microcontroller, sensors, actuators, and a colorful guide with an exciting story inside.
  </p>
</a>

<h3>For video lovers</h3>

<div class="ui relaxed list">
  {{#each tutvideos}}
    <div class="item">
      <img class="ui avatar image" src="{{ avatar }}">
      <div class="content">
        <a href="{{ url }}" target="_blank">{{ title }}</a>
        <!-- counter _blank underscore ??? -->
        <div class="description">{{ description }}</div>
      </div>
    </div>
  {{/each}}
</div>

</div><!-- column -->

<!-------------------------- Guide -------------------------->
<div class="column">
<h2 class="ui icon header">
  <a href="./guide/">
    <img src="./__img__/guide.svg" />
  </a>
  <div class="content">
    <a href="./guide/">User Guide</a>
  </div>
</h2>

[Concepts](./guide/#concepts) ??? XOD language objects and processes described in detail.

[Making your own nodes](./guide/#making-your-own-nodes) ??? the most straightforward way to extend XOD and add support for new hardware.

[XOD Cloud](./guide/#xod-cloud) ??? cloud services for IoT development.

[Case studies](./guide/#case-studies) ??? how-to???s for common scenarios.

[Development](./guide/#development) ??? creating, managing, and sharing programs in XOD.

</div><!-- column -->

<!------------------------ Reference ------------------------>
<div class="column">
<h2 class="ui icon header">
  <a href="./reference">
    <img src="./__img__/reference.svg" />
  </a>
  <div class="content">
    <a href="./reference/">Reference</a>
  </div>
</h2>
<div><!-- A div to force the following list to be the first-child and suppress margins -->

- [Supported hardware](./reference/supported-hardware/) <i class="ui large green microchip icon"></i>
- [Mouse and keyboard shortcuts](./reference/shortcuts/)
- [Data types reference](./reference/data-types/)
- [C++ node API reference](./reference/node-cpp-api/)
- [Tabtest reference](./reference/tabtests/)
- [Global literals reference](./reference/globals/)

</div>
<h3 class="ui header">Standard library nodes</h3>

- [`xod/bits`](https://xod.io/libs/xod/bits/)
- [`xod/common-hardware`](https://xod.io/libs/xod/common-hardware/)
- [`xod/core`](https://xod.io/libs/xod/core/) <i class="ui small yellow star outline icon"></i>
- [`xod/gpio`](https://xod.io/libs/xod/gpio/)
- [`xod/i2c`](https://xod.io/libs/xod/i2c/)
- [`xod/math`](https://xod.io/libs/xod/math/)
- [`xod/net`](https://xod.io/libs/xod/net/)
- [`xod/stream`](https://xod.io/libs/xod/stream/)
- [`xod/uart`](https://xod.io/libs/xod/uart/)
- [`xod/units`](https://xod.io/libs/xod/units/)

</div><!-- column -->

</div><!-- grid -->

---

<h2 id="showcase" class="ui header">
  <div class="content">
    Showcase
    <div class="sub header">Complete devices done with XOD</div>
  </div>
</h2>

<div id="showcase-cards" class="ui cards">
  {{#each showcase}}
    <div class="card">
      <div class="image">
        <a href="{{ url }}" target="_blank"><img src="{{ image }}" /></a>
        <!-- counter _blank underscore ??? -->
      </div>
      <div class="content">
        <a class="header" href="{{ url }}" target="_blank">{{ title }}</a>
        <!-- counter _blank underscore ??? -->
        <div class="meta">{{{ description }}} by {{ author }}</div>
      </div>
    </div>
  {{/each}}
</div>

<h2 id="contributing" class="ui header"><a href="./contributing/">Contributing</a></h2>

Looking for the ways to improve the documentation, XOD language, or the ecosystem? There are many opportunities and we???re happy to accept any help. Read the summary in the [Contributor???s??guide](./contributing/).
