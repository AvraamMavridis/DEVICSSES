# DEVICSSES

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
@media only screen and (min-device-width: 360px) and (max-device-width: 640px) and (-webkit-device-pixel-ratio: 3) and (orientation: portrait) {
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
@media only screen and (min-device-width: 360px) and (max-device-width: 640px) and (-webkit-device-pixel-ratio: 3) and (orientation: portrait) {
  .myclass {
    width: 30px;
    height: 30px;
  }
}
```

Another example using SASS for Ipad, Amazon Kindle Fire HDXX7
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
@media only screen and (min-device-width: 1200px) and (max-device-width: 1920px) and (-webkit-device-pixel-ratio: 2) and (orientation: landscape) {
  .myclass {
    margin-left: 1.2em;
    margin-right: 1.2em;
  }
}
```
## Supported Devices

| Device        | Query      | 
| :------------- |-------------:| 
| Amazon Kindle Fire (First)      | amazon-KindleFire1($orientation)| 
| Amazon Kindle Fire HDX 7"      | amazon-KindleFireHDX7($orientation)     |  
| Amazon Kindle Fire HDX 8.9" | amazon-KindleFireHDX89($orientation)      |   
| Blackberry Playbook | blackberyy-Playbook($orientation)      | 
| Blackberry Z10 | blackberyy-Z10($orientation)      | 
| Blackberry Z30 | blackberyy-Z30($orientation)      | 
| Google Nexus | google-Nexus10($orientation)      | 
| Google Nexus 4 | google-Nexus4($orientation)      | 
| Google Nexus 7 | google-Nexus7($orientation)      | 
| Google Nexus 5 | google-Nexus5($orientation)      | 
| Google Nexus 7 2 | google-Nexus72($orientation)      | 
| Google Nexus S | google-NexusS($orientation)      | 
| HTC Desire | htc-Desire($orientation)      | 
| HTC Evo | htc-Evo($orientation)      | 
| HTC Touch | htc-Touch($orientation)      | 
| HTC OneX | htc-OneX($orientation)      | 
| HTC Evo LTE | htc-Evo-Lte($orientation)      | 
| HTC Sensation | htc-Sensation($orientation)      | 
| HTC EVO 3D | htc-Evo3d($orientation)      | 
| LG Optimus | lg-Optimus($orientation)      | 
| LG Optimus G| lg-OptimusG($orientation)      | 

...list to be updated

