# voicecommandjs
A simple javascript tool to run JavaScript code when a command is said.

Test it out on [CodePen](https://codepen.io/Vanceagher/pen/NWrYGGJ)!


## How to use VCJS

All you have to do to use VCJS is add in a script tag to your HTML file.

`<script src="https://vanceagher.github.io/voicecommandjs/vcjs.min.js"></script>`

Run code on a voice command with something like this.
The variable `vc` is what the person says, so if you say "chocolate cake" then `vc` will be "chocolate cake".
If you don't want the command variable to be `vc` then change it to whatever you want, just make sure to change it in your code, and in `onCommand(vc)`.

```
function onCommand(vc) {
  if (vc == "chocolate cake") {
    alert("you said chocolate cake");
  }
}
```

If you are one of those people that doesn't like to depend on other sites for your code to work, no problem! Instead of linking VCJS, just paste this at the top of your script file.

```
b();function b(){var c=c||webkitSpeechRecognition,a=new c;a.onstart=function(){};a.onspeechend=function(){a.stop();b()};a.onresult=function(d){console.log(d.results[0][0].transcript);onCommand(d.results[0][0].transcript)};a.start()};
```

## More examples

```
function onCommand(vc) {
  if (vc == "chocolate cake") {
    alert("you said chocolate cake");
  }
  
  if (vc == "vanilla cake") {
    alert("you said vanilla cake");
  }
}
```

```
function onCommand(vc) {
  alert("you said " + vc);
}
```
