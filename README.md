JSEmbed
=======

A quick tool for embedding HTML5 (and other JS) applications onto pages with a single line.

Usage
=======

JSEmbed lets you dynamically add JS applications to a page with a single line, include libs, and 

JSEmbed is best used for embedding HTML5 canvas applications. It has special exceptions to support many popular
libraries, such as Construct2, Tresensa and Haxe/Flambe.

It includes helper methods such as the ability to set and get the scale of the canvas, enforcing maximum dimensions, and
remotely communicating with your embeded application through "inform" events, external pause/unpause requests, etc.

Sample Embed
========
```
<html><body>
	<head>
		<title>JSEmbed Example Embed</title>
	  <script type="text/javascript" src="jsembed.js"></script>
		<script type="text/javascript">
			// Parameters to configure jsembed.
			var params = {
				base: "", // Set a base url of all app content. Defaults "".
			 	api: "none", // supported custom apis are defined in jsembed. Defaults "none".
			 	scaletype: "fit", // update window.canvasScale on window resize? Defaults "fit". Also supports "fill", "fillto" and "none."
			 	indexroot: "true", // use the current index url as the path root? If false uses domain root instead. Defaults false (use domain root).			 	
			 	//allowtouchmove: "false", // allow the page to scroll when user drags or swipes? Defaults to false.
			 	//maxwidth: 1024, //The maximum width to scale the canvas to. Only works with fillto.
			 	//maxheight: 640, //The maximum height to scale the canvas to. Only works with fillto.  		
			 	//libs: ["flambe.js"] // array of libs to embed before trying to launch app. Defaults []. Libs will load from base url unless you set libsIgnoreBase: "true" param.
			}			
			// Attributes will be set on the embed target for use by the app. "base" will be set as well.
			var attr = {				
				
			};
			
			jsembed.embed("helloworld.js", "embedtarget", "960", "560", params, attr);
		</script>	   	
	</head>
	<body style="padding: 0; margin: 0; background-color:#000000">
		<div id="embedtarget"></div>	
</body></html>
```

COMING SOON
========
More details examples coming soon!
