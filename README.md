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
  @include apple-Iphone6Plus(portrait){
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
  +apple-IpadRetina(landscape)
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
| LG Optimus LTE| lg-OptimusLTE($orientation)      | 
| LG Optimus Optimus One| lg-OptimusONE($orientation)      |
| Motorola Defy | motorola-Defy($orientation)      | 
| Motorola Droid| motorola-Droid($orientation)      | 
| Motorola Milestone | motorola-Milestone($orientation)      | 
| Motorola Droid 3| motorola-Droid3($orientation)      | 
| Motorola Droid 4 | motorola-Droid4($orientation)      | 
| Motorola Razr| motorola-Razr($orientation)      | 
| Motorola Atrix| motorola-Atrix($orientation)      | 
| Motorola Droid Razr HD | motorola-DroidRazrHD($orientation)      | 
| Motorola Xoom| motorola-Xoom($orientation)      | 
| Motorola Xyboard| motorola-Xyboard($orientation)      | 
| Nokia C5| nokia-C5($orientation)      | 
| Nokia C6 | nokia-C6($orientation)      | 
| Nokia C7| nokia-C7($orientation)      | 
| Nokia N97| nokia-N97($orientation)      | 
| Nokia N8 | nokia-N8($orientation)      | 
| Nokia X8| nokia-X8($orientation)      | 
| Nokia Lumia7X0| nokia-Lumia7X0($orientation)      | 
| Nokia Lumia 8XX | nokia-Lumia8XX($orientation)      | 
| Nokia Lumia 900| nokia-Lumia900($orientation)      | 
| Nokia Lumia N800| nokia-LumiaN800($orientation)      | 
| Nokia Lumia N810 | nokia-LumiaN810($orientation)      | 
| Nokia N900| nokia-LumiaN900($orientation)      | 
| Samsung Galaxy Note| samsung-GalaxyNote($orientation)      | 
| Samsung Galaxy Note 3| samsung-GalaxyNote3($orientation)      | 
| Samsung Galaxy Note 2| samsung-GalaxyNote2($orientation)      | 
| Samsung Galaxy S III| samsung-GalaxyS3($orientation)      | 
| Samsung Galaxy Nexus | samsung-GalaxyNexus($orientation)      | 
| Samsung Galaxy S| samsung-GalaxyS($orientation)      | 
| Samsung Galaxy S II | samsung-GalaxyS2($orientation)      | 
| Samsung Galaxy W| samsung-GalaxyW($orientation)      | 
| Samsung Galaxy S IV| samsung-GalaxyS4($orientation)      | 
| Samsung Galaxy Tab | samsung-GalaxyTab($orientation)      | 
| Samsung Galaxy Tab 7.7"| samsung-GalaxyTab77($orientation)      |
| Samsung Galaxy Tab 8.9"| samsung-GalaxyTab89($orientation)      | 
| Samsung Galaxy Tab 10.1" | samsung-GalaxyTab101($orientation)      | 
| Sony Xperia S| sony-XperiaS($orientation)      |
| Samsung Ion | sony-Ion($orientation)      |
| Sony Xperia Sola| sony-XperiaSola($orientation)      |
| Sony Xperia U| sony-XperiaU($orientation)      |
| Sony Xperia Z| sony-XperiaZ($orientation)      |
| Sony Xperia Z1| sony-XperiaZ1($orientation)      |
| Apple iPhone 3| apple-Iphone3($orientation)      |
| Apple iPhone 4| apple-Iphone4($orientation)      |
| Apple iPhone 5| apple-Iphone5($orientation)      |
| Apple iPhone 6| apple-Iphone6($orientation)      |
| Apple iPhone 6 Plus| apple-Iphone6Plus($orientation)      |
| Apple iPad| apple-Ipad($orientation)      |
| Apple iPad Retia| apple-IpadRetina($orientation)      |

...more supported devices soon. Open for pull requests.

