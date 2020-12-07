# Plasma Slider
An image slider plugin

# Uses
## Method 1 : Define options on markup
### JS
```
var slider = new PlasmaSlider({
  containerID: "plasma-slider"
});

slider.init();
```

### HTML
```
<div id="plasma-slider" class="plasmaSlider" 
    data-width="16" 
    data-height="9" 
    data-show-thumbnails="1"
    data-blur-background="1" 
    data-rtl="0" 
    data-background-color="#000"
    >
    <!-- Optional : Placeholder Image, stays until javascript file loads -->
    <div class="plasmaSliderTempImage" style="padding-top: 52.25%;">
        <img class="plasmaSliderTempImgBlur" src="https://images.unsplash.com/photo-1566640241039-2443899336c2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=750&q=80" alt="">
        <img class="plasmaSliderTempImg" src="https://images.unsplash.com/photo-1566640241039-2443899336c2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=750&q=80" alt="">
    </div>

    <div class="plasmaSliderImages">
        <span class="plasmaSliderImageItem" data-src="https://images.unsplash.com/photo-1566640241039-2443899336c2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=750&q=80" data-alt=""></span>
        <span class="plasmaSliderImageItem" data-src="https://images.unsplash.com/photo-1570121962635-3552954619a6?ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80" data-alt=""></span>
        <span class="plasmaSliderImageItem" data-src="https://images.unsplash.com/photo-1569834381156-7b735e41e57d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=889&q=80" data-alt=""></span>
        <span class="plasmaSliderImageItem" data-src="https://images.unsplash.com/photo-1547738765-ee82a7f07da8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=334&q=80" data-alt=""></span>
        <span class="plasmaSliderImageItem" data-src="https://images.unsplash.com/photo-1567845531350-79f5c0464b96?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=334&q=80" data-alt=""></span>
        <span class="plasmaSliderImageItem" data-src="https://images.unsplash.com/photo-1566640241039-2443899336c2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=750&q=80" data-alt=""></span>
        <span class="plasmaSliderImageItem" data-src="https://images.unsplash.com/photo-1570121962635-3552954619a6?ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80" data-alt=""></span>
        <span class="plasmaSliderImageItem" data-src="https://images.unsplash.com/photo-1569834381156-7b735e41e57d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=889&q=80" data-alt=""></span>
        <span class="plasmaSliderImageItem" data-src="https://images.unsplash.com/photo-1547738765-ee82a7f07da8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=334&q=80" data-alt=""></span>
        <span class="plasmaSliderImageItem" data-src="https://images.unsplash.com/photo-1567845531350-79f5c0464b96?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=334&q=80" data-alt=""></span>
        <span class="plasmaSliderImageItem" data-src="https://images.unsplash.com/photo-1566640241039-2443899336c2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=750&q=80" data-alt=""></span>
        <span class="plasmaSliderImageItem" data-src="https://images.unsplash.com/photo-1570121962635-3552954619a6?ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80" data-alt=""></span>
        <span class="plasmaSliderImageItem" data-src="https://images.unsplash.com/photo-1569834381156-7b735e41e57d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=889&q=80" data-alt=""></span>
        <span class="plasmaSliderImageItem" data-src="https://images.unsplash.com/photo-1547738765-ee82a7f07da8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=334&q=80" data-alt=""></span>
        <span class="plasmaSliderImageItem" data-src="https://images.unsplash.com/photo-1567845531350-79f5c0464b96?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=334&q=80" data-alt=""></span>
    </div>
</div>
```


## Method 2 : Define options on script
### JS
```
var slider = new PlasmaSlider({
  containerID: "plasma-slider",
  width: 16,
  height: 9,
  showThumbnails: true,
  rtl: false
  blurBackground: false,
  backgroundColor: '#000'
  images: [
    {
      src: "https://images.unsplash.com/photo-1566640241039-2443899336c2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=750&q=80",
      alt: ""
    },
    {
      src: "https://images.unsplash.com/photo-1570121962635-3552954619a6?ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80",
      alt: ""
    },
    {
      src: "https://images.unsplash.com/photo-1569834381156-7b735e41e57d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=889&q=80",
      alt: ""
    },
    {
      src: "https://images.unsplash.com/photo-1547738765-ee82a7f07da8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=334&q=80",
      alt: ""
    },
    {
      src: "https://images.unsplash.com/photo-1567845531350-79f5c0464b96?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=334&q=80",
      alt: ""
    }
  ]
});
slider.init();
```

### HTML
```
<div id="plasma-slider" class="plasmaSlider">
    <!-- Optional : Placeholder Image, stays until javascript file loads -->
    <div class="plasmaSliderTempImage" style="padding-top: 52.25%;">
        <img class="plasmaSliderTempImgBlur" src="https://images.unsplash.com/photo-1566640241039-2443899336c2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=750&q=80" alt="">
        <img class="plasmaSliderTempImg" src="https://images.unsplash.com/photo-1566640241039-2443899336c2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=750&q=80" alt="">
    </div>
</div>
```
