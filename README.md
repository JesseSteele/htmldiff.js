# htmldiff.js
*A drop-in, working, JavaScript derivative of htmldiff.js*

This is from an inline "editor" view using a tool like `diff`, originally written in CoffeeScript, but now in pure JavaScript.

## How to use

You only need `htmldiff.min.js`!

| **HTML .js src** :

```html
<script src="htmldiff.min.js"></script>
```

| **HTML DOM** :

```html
<div class="outercard">
  <div class="row">
    <div class="col">
      <h4>Old</h4>
      <div class="card" id="outputOld"></div>
    </div>
    <div class="col">
      <h4>Diff</h4>
      <div class="card" id="outputDif"></div>
    </div>
    <div class="col">
      <h4>Current</h4>
      <div class="card" id="outputCur"></div>
    </div>
  </div>
</div>
```

| **HTML script** :

```html
<script>
let oldHTML = `Original_HTML_or_PHP_etc_$Variable_here`;
let curHTML = `Current_HTML_or_PHP_etc_$Variable_here`;
let difHTML = htmldiff(oldHTML, curHTML);
document.getElementById("outputOld").innerHTML = oldHTML;
document.getElementById("outputCur").innerHTML = curHTML;
document.getElementById("outputDif").innerHTML = difHTML;
</script>
```

| **CSS** :

```css
ins {
  text-decoration: none;
  background-color: #d4fcbc;
}

del {
  text-decoration: line-through;
  background-color: #fbb6c2;
  color: #555;
}

.outercard {
  border: none;
  margin: 1rem;
  padding: 1rem;
}

.card {
  background: #fff;
  border: 1px solid #ccc;
  border-radius: 3px;
  margin: 0;
  padding: 1rem;
  flex: 1 0 0;
}

.row {
  display: flex;
  justify-content: space-between;
  margin-right: -8px;
}

.col {
  display: flex;
  flex: 1 0 0;
  flex-direction: column;
  margin-right: 8px;
}
````

## Deployment

The .html and .css files are part of a working example, but may require a live webserver to work.

For reference, htmldiff.js is also available. Remember, htmldiff.min.js contains no license and is not distributable by itself.

## Brief derivative history
According to a [recent port](https://github.com/tnwinc/htmldiff.js/blob/master/README.md)...

This started about 2012 in CoffeeScript at:

[https://github.com/myobie/htmldiff]

Then, it moved to:

[https://github.com/tnwinc/htmldiff.js]

While called "htmldiff.js", it did not work with as a standalone, sourced script.

Then, at some point it was derived and rearranged in 2018 at:

[https://codepen.io/benbowes/pen/pVaMpv]

And now, after some simplifying and correcting the broken `id="output"` taxonomy, it is here.

Previously it was licensed under MIT; here it is GPL.
