# Parallax Effect Tutorial
This example code will create a parallax effect using only HTML and CSS.

## Code
In order for this to work correctly, please make sure you create a section as follow:
``` html
<section class="slide1 slide">
  <div class="title">
    <h2>5G Speed</h2>
    <p>5G on iPhone is superfast. So you can download movies on the fly. Stream higher-quality video. Or FaceTime in HD over cellular. With lots less lag. And you can do it in more places, because iPhone 12 has the broadest 5G coverage worldwide.</p>
  </div>
</section>
```

The `<section>` has two classes, `slide1` says that it's the first slide and the number should change for each section if you would like to have a different background. The class `slide` **needs** to be added to all of the section tags.

### Background images
If you are only going to have text and a background image, your CSS should look like this:
``` css
.slide1:before {
  background-image: url("../images/iphone-case.jpg");
  transform: translateZ(-1px) scale(2);
}
```

If you are going to have an image inside of the `<section>`, your CSS should look like this:
``` css
.slide1 {
  background-image: url("../images/iphone-case.jpg");
  z-index: 2;
}
```

### Troubleshooting
If the parallax effect is not working as intended, make sure that you have the CSS for the html selector:
``` css
html {
  height: 100%;
  overflow: hidden;
}
```

## Resources
[How to do a Parallax Effect](https://www.w3schools.com/howto/howto_css_parallax.asp)
