# angular2-qrscanner
QrScanner will scan for a QRCode from your Web-cam and return its
string representation by drawing the captured image onto a 2D Canvas
and use [@LazarSoft/jsqrcode](https://github.com/LazarSoft/jsqrcode) to check for a valid QRCode every *Xms*

```html
<!--
Component attributes
[debug]         debug flag for console.log spam              (default: false)
[canvasWidth]   canvas width                                 (default: 640)
[canvasHeight]  canvas height                                (default: 480)
[mirror]        should the image be a mirror?                (default: false)
[stopAfterScan] should the scanner stop after first success? (default: true)
[updateTime]    miliseconds between new capture              (default: 500)
(onRead)        callback when qr code is detected
-->
<qr-scanner
   [debug]="false"        
   [canvasWidth]="640"    
   [canvasHeight]="480"   
   [mirror]="false"       
   [stopAfterScan]="true" 
   [updateTime]="500"     
   (onRead)="decodedOutput($event)"></qr-scanner>
```
