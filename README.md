# css-loading.css

css-loading.css is an all CSS loading icon, like one might typically use while waiting for server response on an AJAX request. It leverages CSS animations and transforms to draw out the shape.

Written in SASS to provide the ability to compile different versions for different sizing, coloring, speed, etc.

Inspired by (http://codepen.io/hakimel/full/CxliK)

## Issues

There is one issue I'd like to find a solution for. Particularly, when the spokes are big enough to overlap one another, the desired rendering would be like Penrose Stairs (http://en.wikipedia.org/wiki/Penrose_stairs) where each spoke overlaps the next spoke and is overlapped by the previous. However in CSS as far as know each element has its own static z-index and so you eventually get to the cross over from last to first spoke where the z-index sequence resets to the lowest value. That leaves the last spoke in the sequence to overlap both the penultimate spoke and the first spoke.

## Browser support

<table width="100%" style="text-align: center;">
  <thead>
    <tr>
      <td>Safari</td>
      <td>Firefox</td>
      <td>Chrome</td>
      <td>&lt;=IE9</td>
      <td>IE10+</td>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>&#x2713;</td>
      <td>&#x2713;</td>
      <td>&#x2713;</td>
      <td>&#x2717;</td>
      <td>&#x2713;</td>
    </tr>
  </tbody>
</table>


## Build instructions

css-loading is built using [grunt](http://gruntjs.com) & RubySASS.

You'll need:

* Ruby (and sass - `gem install sass`)
* Run `npm install` from the root directory.
* To run a build, you'll simply need to run `grunt`.
