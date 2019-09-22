Update: This project does not work any more; I no longer have time to maintain it as Chrome and Netflix make changes which break functionality. --Jared

flixplus
=======

About
-----
Flix Plus by Lifehacker is a Chrome extension built by Jared Sohn that helps you customize Netflix.  Read more [here](http://lifehacker.com/preview/flixc-plus-customizes-netflix-to-your-hearts-desire-1640968001).

The source code uses a couple of frameworks:

* It uses [OpenForge](https://github.com/trigger-corp/browser-extensions) to make it easier to build cross-browser extensions.  However, at this time it only works for Chrome and more work would be necessary to support other browsers.

* It uses [openforge-greasemonkey-multi-script-compiler](https://www.github.com/jaredsohn/openforge-greasemonkey-multi-script-compiler), which is a new framework built for this extension to make it easier to build browser extensions from userscripts.  (Since this framework has only been used once, more work would be needed to adapt it to other extensions.)


Setup
-----

1. Clone [OpenForge](https://github.com/trigger-corp/browser-extensions) as your flix_plus folder and follow OpenForge's setup instructions.

2. Clone the openforge-greasemonkey-multi-script-compiler folder as your openforge-greasemonkey-multi-script-compiler folder and follow the instructions for setting it up.

3. Clone this project as openforge-greasemonkey-multi-script-compiler/_inputs/flix_plus and continue following the compiler instructions.


Contributing
------------
   Feel free to submit a pull request.  Most code should follow [Google's Javascript coding standards](https://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml) (with the exceptions of fade_rated.js, fade_watched.js, netflixnotes.js, queue_sorter.js, ratings.js, links.js, keyboard_shortcuts_info.js, expiring.js, and shortcuts_editor.js; some already conform to slightly-different styles while other files have barely been changed for this extension).  The code is linted with [Closure Linter](https://developers.google.com/closure/utilities/) with rules {131,110,220} excluded.


Building
--------
   See the openforge-greasemonkey-multi-script compiler documentation for build instructions.

Debugging
---------
To get debugging information in the JavaScript console, enter the following commands:

```javascript
localStorage["flix_plus debug_level"] = 4;
localStorage["fplib debug"] = true;
localStorage["extlib debug"] = true;
```

Licensing
--------
   The configuration files in this repository (except for some images) are licensed GPL.  Each userscript has its own license (the ones produced by Lifehacker are cross-licensed GPL and MIT).
