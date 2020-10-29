# voicecommandjs
A simple javascript tool to run JavaScript code when a command is said.

## How to use VCJS

All you have to do to use VCJS is add in a script tag to your HTML file.

`<script src="https://vanceagher.github.io/voicecommandjs/vcjs.min.js"></script>`

Run code on a voice command with something like this.
The variable `vc` is what the person says, so if you say "chocolate cake" then `vc` will be "chocolate cake".

```
function onCommand(vc) {
  if (vc == "test") {
    alert("tested");
  }
}
```
