---
title: Adjusting Map Range
---

# #14. Adjusting Map Range

<div class="ui segment note">
<span class="ui ribbon label">Note</span>
This is a web-version of a tutorial chapter embedded right into the XOD IDE.
To get a better learning experience we recommend to install the
<a href="/downloads/">desktop IDE</a> or start the
<a href="/ide/">browser-based IDE</a>, and you’ll see the same tutorial there.
</div>

After the previous lesson, the `map` node linearly maps the 20–50°C range to the
0–90° servo rotation. Let’s raise the sensitivity. Say, we want to map 15–30°C
to 0–90° rotation.

However, what will happen if the `X` pin of the `map` receives data that is
outside the input range (10 or 42, for example)? The output value which is a
servo angle will fall outside the desired range too.

For such cases there is a sibling node called `map-clip`. It works the same way,
but any input that is out of range will be rounded to `Smin` or `Smax`. Thus, if
`X` receives a value of 10, the `map-clip` node will accept it as 15, and 42
will be accepted as 30.

![Patch](./patch.png)

## Test circuit

<div class="ui segment note">
<span class="ui ribbon label">Note</span>
The circuit is the same as for the previous lesson.
</div>

![Circuit](./circuit.fz.png)

[↓ Download as a Fritzing project](./circuit.fzz)

## How-to

Just use the `map-clip` instead of the `map` if you want the output range to be
guaranteed.

If you prefer °F, you can easily translate the data from the thermometer with
the `c-to-f` node from `xod/units`. The range will be 59–95°F.

![Screencast](./screencast.gif)

[Next lesson →](../15-buttons/)
