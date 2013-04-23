![Image Framer](Image-Framer.jpg)

## Image Framer jquery plugin

Image Framer is very simple jQuery plugin that wraps your images inside a frame. _Actually, despite the name, you can frame any element._


_Website is coming soon._ Currently you can find demo html files in the package.

## Freatures

* All of the frames are flexible to pretty much any image size
* Contains 24 frames
* All frames come in 4 different sizes
* 4 different optional inner shadows
* HTML 5 data-attributes can be used to overwrite the plugin options

## Tested browsers

* _Coming soon..._

## Usage instructions

###1.

* [Download the .zip][1].
* Move `imageframer` folder to you website root.

###2.

Add the following to your web page `<head>`.

```HTML
<!-- Make sure that jquery is linked as well -->
<script type="text/javascript" src="jquery.min.js"></script>
<link rel="stylesheet" type="text/css" href="imageframer/if.css" />
<script type="text/javascript" src="imageframer/if.js" ></script>
<script type="text/javascript">
    $(function() {

      $('.frame').imageframer();

    });
</script>
```

###3.

Add the `.frame` class to all elements you wish to frame

## Options

* **frameType:** 'wood' `List of frames below`
* **frameSize:** 4 `Numbers from 1 to 4. 1 is the smallest and 4 is the largest`
* **innerShadow:** null `Numbers from 1 to 4. 1 is the smallest / lightest and 4 is the biggest / darkest `
* **disable:** false `Boolean value`
* **callback:** function() {} `Triggered after everything is generated`

Options example

```html
<script type="text/javascript">
    $(function() {

      $('.frame').imageframer({
          frameType: 'wood3',
          callback: function() {
              $(this).addClass('aClass');
          },
          innerShadow: 1
      });

    });
</script>
```

## List of available frames:

* wood-dark
* wood-dark2
* wood-darkgrey
* wood-darkgreen
* wood-darkorange
* wood-darkred
* wood-light
* wood-light2
* wood-light3
* wood-old
* wood-oldlight
* wood-purple
* wood3
* wood4
* wood5
* wood6
* rock
* metallic
* black
* red
* gold
* gold2
* silver
* silver2


## Data-attributes

Example of all data attributes applied to one image ( minus 'disable' and 'callback' ):

```html
<img 
    class="frame" 
    data-frame-type="black" 
    data-frame-size="3" 
    data-inner-shadow="1" 
    data-custom-class="myClass" 
    src="myImg.jpg" alt="" 
/>

```

Example of the disable option:


```html
<img class="frame" data-disable="true" src="myImg.jpg" alt="" />
<img class="frame" src="myImg.jpg" alt="" />
<img class="frame" src="myImg.jpg" alt="" />
<img class="frame" src="myImg.jpg" alt="" />

```

Callback can only be used as a data-attribute to disable `callback` for certain elements:

```html
<img class="frame" data-callback="false" src="myImg.jpg" alt="" />
<img class="frame" src="myImg.jpg" alt="" />
<img class="frame" src="myImg.jpg" alt="" />
<img class="frame" src="myImg.jpg" alt="" />

```

## What's to come (maybe)?

* Moar frames!!!
* a psd file and script, to enable anyone ( who has photoshop ) to make frames in a snap.
 * Currently I do have a file much like that, to streamline my workflow to create the frames, but it's much too messy to be released to the wild ...and I use it with Slicy.
* I do also have a script that enables you to very easily re-color frames with very little effort. I just need to clean that up as well.
* I need to refine some of the frame files.
 * Quality
 * top-bottom and right-left images are unnecessary wide for some frame types.
 * I pretty much half-assed the way I named the frames. Need to work on that.


[1]: https://github.com/joonaspaakko/Image-Framer-jquery-plugin/archive/master.zip
