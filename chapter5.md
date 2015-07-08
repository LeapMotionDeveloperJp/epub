# サンプルアプリをつくる
## DOM操作
### index.htmlを用意
表示するためのHTMLファイルを作成し、LeapMotionのJavaScriptライブラリを読み込みます。
```
<html>
    <head></head>
    <body>
        <h1>Hello, LeapJS (V2)!</h1>
        <div id="output"></div>
        <script src="//js.leapmotion.com/leap-0.6.3.min.js"></script>
    </body>
</html>
```
### インラインにJavaScriptを用意
index.htmlの```</body>```にスクリプトを書いてきます。
```
<script src="//js.leapmotion.com/leap-0.6.3.min.js"></script>
<script type="text/javascript">
function concatData(id, data) {
    return id + ": " + data + "<br>";
}
// DOM
var output = document.getElementById("output");
// Frame, Hand, Finger Variable
var frameString = "", handString = "", fingerString = "";
var hand, finger;

// Main Leap Loop
Leap.loop(options, function (frame) {
    frameString = concatData("frame_id", frame.id);
    frameString += concatData("num_hands", frame.hands.length);
    frameString += concatData("num_fingers", frame.fingers.length);
    frameString += "<br>";

// Output HTML
    output.innerHTML = frameString;
});
</script>
```
### インラインにJavaScriptを用意
index.htmlの```</body>```にスクリプトを書いてきます。
```
function concatData(id, data) {
    return id + ": " + data + "<br>";
}
// FingerName
function getFingerName(fingerType) {
    switch (fingerType) {
        case 0:
            return 'Thumb';
            break;
        case 1:
            return 'Index';
            break;
        case 2:
            return 'Middle';
            break;
        case 3:
            return 'Ring';
            break;
        case 4:
            return 'Pinky';
            break;
    }
}
// Concat Joint Position
function concatJointPosition(id, position) {
    return id + ": " + position[0] + ", " + position[1] + ", " + position[2] + "<br>";
}
```


￼
```
 ...
var hand, finger;
// Leap.loop uses browser's requestAnimationFrame var options = { enableGestures: true };
// Main Leap Loop Leap.loop(options, function(frame) {
frameString = concatData("frame_id", frame.id);
frameString += concatData("num_hands", frame.hands.length); frameString += concatData("num_fing```


￼
```
// Helpers for thumb, pinky, etc.
fingerString = concatJointPosition("finger_thumb_dip", hand.thumb.dipPosition);
for (var j = 0, len2 = hand.fingers.length; j < len2; j++) {
finger = hand.fingers[j];
fingerString += concatData("finger_type", finger.type) + " (" +
getFingerName(finger.type) + ") <br>";
fingerString += concatJointPosition("finger_dip",
finger.dipPosition);
fingerString += concatJointPosition("finger_pip",
finger.pipPosition);
fingerString += concatJointPosition("finger_mcp",
finger.mcpPosition); fingerString += "<br>";
}
frameString += handString;
frameString += fingerString; }
output.innerHTML = frameString; });
</script> </body>
</html>```

## Three.js
## じゃんけん
## ブラウザプレゼンテーション（の操作）
