__Important notice__
*As for today and for as long as the version 1.4 of 3L is in beta, many information in the README (this file) and [3L website](http://mateuszkocz.github.io/3l/) are not up to date and mostly refers to the previous 3L's version. Especially this holds true for the usage instructions and [Bootstrap](http://twitter.github.io/bootstrap/) integration.*
*The previous version is still downloadable [on the site](http://mateuszkocz.github.io/3l/) and if you feel uncofortable with the lack of infromation, please use the version 1.3 of 3L. However I strongly recomend you to use the version 1.4, since 1.3 is not updated for a long time and is obsolete.*

# 3L was made for YOU to help you create awesome websites and fill the Internet with excessive amount of Love! ♥

Keep up your good work!

* Author: [Mateusz Kocz](http://radiatingstar.com)
* [Watch 3L on Github](https://github.com/mateuszkocz/3l)
* [Submit a bug issue](https://github.com/mateuszkocz/3l/issues?state=open)
* [Download .zip](https://github.com/mateuszkocz/3l/archive/master.zip)

3L is MIT licensed.

[LESS](http://lesscss.org/) is made by Alexis Sellier and licensed under [Apache License v2.0](http://www.apache.org/licenses/LICENSE-2.0)

[reset.css](http://meyerweb.com/eric/tools/css/reset/) is made by Eric Meyer and is in public domain.

[normalize.css](http://necolas.github.com/normalize.css/) is made by Nicolas Gallagher and Jonathan Neal and licensed under MIT License.

[HTML5 Boiler Plate's default CSS](http://html5boilerplate.com/) is made by Nicolas Gallagher, Jonathan Neal, Kroc Camen, the H5BP dev community and other people and is licensed under MIT License.

3L version: 1.4.3-beta (2013.04.10)
LESS version: 1.3.1
Reset.css version: 2.0
Normalize.css version: 2.0.1
HTML5BP's CSS version: 4.0.1

[Get your own LESS.js](http://lesscss.org/)

==========================================

HOW TO USE

Inside the .zip file you have:

* my-style.less – here you'll be writing you code,
* 3L-mini.less – the basic file with mixins,
* 3L-maxi.less – mixins with documentation and examples,
* less.js – the newest, compatible with 3L version of LESS.js,
* animations.less – mixins required for declaring @keyframes,
* bootstrap – files to be replaced in Bootstrap's less directory in order to use 3L together with Bootstrap.

Copy my-style.less, 3L-mini.less and less.js into the folder with your project. Place the code below in the <head> section of your .html file.

	<link rel="stylesheet/less" type="text/css" href="my-style.less" />
	<script src="less.js" type="text/javascript"></script>

You can now start writing your own style in my-style.less. Check out the documentation for class names available to use and make your code awesome!

==========================================

ANIMATIONS

Using animations with 3L is pretty easy. Copy the animations less files (animationX.less) to the folder where you have your style sheet. In your code just type @import "animation1" (or any other number), create a class .animation1 (or any other) and declare your animation. 3L will make @keyframes for you. Now just use this animation in any element you want with .animation() class.

	@import "animation1";
	.animation1 () {
		/* your @keyframes rules */
		}
	.someClassName {
		.animation(.animation1 1s);
		}
	
==========================================

How to make 3L compatible with Bootstrap?

It's easy! First you need to download pre-compiled Bootstrap (tested on v.2.0.2) with LESS files. Get it here -> https://github.com/twitter/bootstrap/ and unzip it. Then, in your downloaded 3L folder, you have a bootstrap folder with 2 files: bootstrap.less and mixins.less. Replace Bootstrap's original files in less folder with those two. After that just copy and paste 3l-mini.less (and all animations if you wish to use them) to the Bootstrap's less folder and create some awesome website!

---

Where are my grids?

3L doesn't have a grid system implemented. It is not meant to have any style included. Of course grids are cool so create yours with Gridpak —> http://gridpak.com/ . Gridpak gives you a responsive grid in LESS file so you can use it together with 3L.

---

Compiler I use fail to compile 3L!

Unfortunately not all compilers can deal with some of the 3L classes. The hardest to compile are opacity in percentages (it uses a small piece of JavaSript), keyframes and guarded mixins. I strongly encourage you to use WinLess (also the online version) as it works very well with all 3L classes.

If you're on a Mac and compiler you use was able to deal with all the issues stated above, please, let me know (mateusz@radiatingstar.com)!

Other solution would be to delete the option to declare opacity in percentages (it's the biggest class in opacity block in 3L.less file and uses JavaScript). If it still doesn't help, you seriously need to consider getting a better compiler compatible with all LESS functionality!

---

I've found a bug (in your English)

That's great! Please, submit an issue via GitHub, so I'll get it fixed ASAP. -> https://github.com/mateuszkocz/3l/issues?state=open

If you find an error in language — be it on this website or in 3L's documentation — do not hesitate to also point that out! 3L is learning English very hard!

---

After compilation I have many comments in my style sheet

The reason is that you're using 3L-maxi.less that has documentation included. Your compiler leaves the comments intact. Solution is pretty easy — use either 3L-mini.less (if you use my-style.less 3L-mini is the default) or minify your CSS. Actually you should always minify CSS files so even if you were using 3L-maxi.less, those comments will be deleted eventually.
