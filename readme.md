# Brusher

<b>Demo: <a href="https://brusher.netlify.app/">brusher.netlify.app</a></b>

<b>See brusher.js for code. </b> <i>Little vanilla JS library to add interactive backgrounds to your webpages.</i>

![demo](https://github.com/MasonWang025/brusher/blob/master/assets/demo.JPG?raw=true)
([View Demo](https://brusher.netlify.app/))

<i>This is an improved version of [kamranahmedse's brusher](https://github.com/kamranahmedse/brusher).</i> This version can <b>target any DOM node</b> and allows you to <b>create multiple instances</b> of Brusher. It also includes <b>added configuration setttings</b>.

## Usage

Download the brusher.js file.
For the basic usage, all you need to do is create an instance of `Brusher` and provide an image.

```javascript
const brusher = new Brusher({
  image: "abstract.png",
});

brusher.init();
```

This is the image that will be shown when brusher hovers over. To provide the original image, <b>set a CSS background.</b> <i>For example, use a blurred background or a black and white one (like the demo).</i>

## Available Options

Here is the list of options that you may use:

```javascript
const brusher = new Brusher({
  image: "abstract.png", // Path of the image to be used as a brush
  keepCleared: true, // Put the blur back after user has cleared it
  stroke: 80, // Stroke size for the brush
  lineStyle: "round", // Brush style (round, square, butt)
  removeStepsTime: 120, // how long old steps should last (does not matter for keepCleared: true)
});

brusher.init();
```

A note on blurry background: [blur the image yourself](http://pinetools.com/blur-image) and apply it to the body for improved performance. Here is the sample CSS that you may use for the background

```css
body {
  background-size: cover;
  background-position: 0 0;
  background-attachment: fixed;
  background-image: url(path/to/blurred/image.jpg);
}
```

## License

This was modified from Kamran Ahmed's original source code:
MIT &copy; [Kamran Ahmed](https://twitter.com/kamranahmedse)
