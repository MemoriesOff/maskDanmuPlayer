# MaskDanmuPlayer

A smart DanmuPlayer with a function to prevent people from being blocked.

[Try the demo here!](http://acgtrip.com/demo/maskDanmuPlayer/index.html)


## Installation

You can use this as standalone es5 bundle like this:

```html
        <link rel="stylesheet" href="src/maskDanmuPlayer.css"/>
	<script src="src/jquery-2.1.4.min.js"></script>
        <script src="src/CommentCoreLibrary.js"></script>
	<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@1.0.0"></script>
	<script src="src/util.js"></script>
	<script src="src/ModelWeights.js"></script>
	<script src="src/mobileNet.js"></script>
	<script src="src/SemanticSegmentation.js"></script>
        <script src="src/maskDanmuPlayer.js"></script>
```

For the convenience of debugging, we haven't packaged or compressed the code.

## Usage

```html
  <div id="player" style="margin:50px auto;position:relative"></div>
```

```javascript
  $('#player').H5Player(
        {
          width: "800" ,
          height: "450", 
          src:"video.mp4",
          comments:"danmu.xml",
          modelAddress:"model.json",
          testcanva:canva
        });
```

#### Inputs

- **width** the player's width

- **height** the player's height. Note:only the video's height, all the player's height will be this add 37px;

- **src** the video file route

- **comments** the Danmu file route. More information can be find [here](https://github.com/jabbany/CommentCoreLibrary/tree/master/docs/data-formats)

- **modelAddress** the address of the cheakpoint. you can find one cheakpoint at [here](https://github.com/MemoriesOff/github_blog/tree/gh-pages/static/semanticDemo/web_model).All files in the folder is necessary and the modelAddress means the route of the "model.json". For example, if you want to use our model weight, the modelAddress can be given as "http://www.acgtrip.com/static/semanticDemoweb_model/model.json".

- **testcanva** if you want to show the mask layer for test, give the canve object here. 

## About the Semantic-Segmentation network.

This program use the artificial neural network to get the mask layer, if you want to learn more about the network ,please move on to [browser-semantic-segmentation](https://github.com/MemoriesOff/browser-semantic-segmentation), our sister project.

## Acknowledgement

This work use the danmaku comments [CommentCoreLibrary](https://github.com/jabbany/CommentCoreLibrary)

## Todo list

- [ ] Mobile Adaptation

## License

The program is licensed licensed [MIT](http://opensource.org/licenses/mit-license.php).
