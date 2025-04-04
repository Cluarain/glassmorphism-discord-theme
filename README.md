# Glassmorphism

## Preface  

The Glassmorphism theme was created purely out of boredom and will (or won't) be supported by the author as time permits.  
During the writing process, an idea emerged to split the theme into two types: **Glassmorphism Static** and **Glassmorphism Animated**, respectively.  

### Glassmorphism Static  

A theme with a static background. You can set any image, GIF, SVG, video, etc. All you need to do is... open the theme file and replace `--bg-image: url(link);`.  
There is also the ability to use [CSS filters](https://cssgenerator.org/filter-css-generator.html) via the variable `--bg-filter: saturate(150%);`.

### Glassmorphism Animated  

A theme with a dynamically changing background. You can set any image, GIF, SVG, video, etc., and any number of them.  
To replace the current ones, you just need to... open the theme file and replace the link in `--bg-image-X: url(link);`.  
To add new images to the carousel, you need to add a new variable `--bg-image-X: url(link);` in the `:root {...}` block  
and rewrite the `@keyframes changeBg {...}` block.

If there are 5 images, then accordingly 100% / 5 = 20% of the time for each image:

```css
  0%,
  19.99% {
    background: var(--bg-image-1);
  }
  20%,
  39.99% {
    background: var(--bg-image-2);
  }
  /* and so on */
```

There is the ability to use [CSS filters](https://cssgenerator.org/filter-css-generator.html), but in that case, you'll need to set the filters for each frame or reset the previous ones using the variable `--bg-filter: none;`.
