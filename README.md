# DEVICCSES

SASS/SCSS mixins to generate CSS for the most popular devices. 

For example the following SCSS for Sony Xperia Z1, Iphone6-Plus and Samsung-GalaxyS4 
```scss
.myclass{
  width: 100px;
  height: 100px;
  @include sony-XperiaZ1(portrait){
    width: 50px;
    height: 50px;
  }
  @include iphone6-plus(portrait){
    width: 60px;
    height: 60px;
  }
  @include samsung-GalaxyS4(portrait){
    width: 30px;
    height: 30px;
  }
}
```
Will generate the appropriate CSS for these devices
```css
.myclass {
  width: 100px;
  height: 100px;
}
@media only screen and (min-device-width: 360px) and (max-device-width: 640px) and (orientation: portrait) {
  .myclass {
    width: 50px;
    height: 50px;
  }
}
@media only screen and (min-device-width: 414px) and (max-device-width: 736px) and (-webkit-device-pixel-ratio: 3) and (orientation: portrait) {
  .myclass {
    width: 60px;
    height: 60px;
  }
}
@media only screen and (min-device-width: 360px) and (max-device-width: 640px) and (orientation: portrait) {
  .myclass {
    width: 30px;
    height: 30px;
  }
}
```

Another example using SASS for Ipad, Samsung Tab
```sass
.myclass
  margin-left: 0em
  margin-right: 0em
  +ipad-retina(landscape)
    margin-left: 1.1em
    margin-right: 1.1em

  +amazon-KindleFireHDX7(landscape)
    margin-left: 1.2em
    margin-right: 1.2em
```
Will generate
```css
.myclass {
  margin-left: 0em;
  margin-right: 0em;
}
@media only screen and (min-device-width: 768px) and (max-device-width: 1024px) and (-webkit-device-pixel-ratio: 2) and (orientation: landscape) {
  .myclass {
    margin-left: 1.1em;
    margin-right: 1.1em;
  }
}
@media only screen and (min-device-width: 1200px) and (max-device-width: 1920px) and (orientation: landscape) {
  .myclass {
    margin-left: 1.2em;
    margin-right: 1.2em;
  }
}
```

| Device        | Query      | 
| :-------------: |:-------------:| 
| Amazon Kindle Fire (First)      | amazon-KindleFire1($orientation)| 
| Amazon Kindle Fire HDX 7"      | amazon-KindleFireHDX7      |  
| Amazon Kindle Fire HDX 8.9" | amazon-KindleFireHDX89      |   

