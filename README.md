# CustomCssThemes

## How to apply a css theme
### TamperMonkey
Example: __Change the @includes and ss.href link according to your implementation.__
```javascript
// ==UserScript==
// @name         Facebook Messenger Dark
// @version      0.2
// @description  Messenger dark theme
// @author       Zjefke Vanelslande && Steven Impens
// @include      http://messenger.com/*
// @include      https://messenger.com/*
// @include      http://*.messenger.com/*
// @include      https://*.messenger.com/*
// @run-at       document-end
// @grant        none
// ==/UserScript==

(function() {
    'use strict';

    var ss = document.createElement("link");
    ss.rel = "stylesheet";
    ss.type = "text/css";
    ss.href = "https://cdn.rawgit.com/Cosmicus/CustomCssThemes/master/Messenger.com/dark_zdroidv.css";

    var heads = document.getElementsByTagName("head");
    if(heads.length > 0){
        heads[0].appendChild(ss);
    }else{
        document.documentElement.appendChild(ss);
    }
})();
```
