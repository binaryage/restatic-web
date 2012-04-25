---
layout: product
title: Restatic pumps Google spreadsheet content to static sites
product: restatic
product_title: Restatic
product_subtitle: Pumps spreadsheet data to your static web!
download: https://github.com/binaryage/restatic
downloadtitle: Download v0.2
downloadsubtitle: Requires a POSIX system with NodeJS
repo: https://github.com/binaryage/restatic
buttons: <a href="http://restatic-example.herokuapp.com" class="button product-button-thumbup"><div><div>Visit Demo Page<div class="product-specs">And get some inspiration...</div></div></div></a>
advert: After installation and Firefox restart you can visit the <a href="/test/index.html">FireQuery test page</a>
meta_title: Restatic pumps Google spreadsheet content to static sites
meta_keywords: restatic,static-site,osx,google-docs,google,binaryage,software,tool
meta_description: Restatic is a command-line utitlity for parsing google spreadsheet content to your static sites
meta_image: http://www.binaryage.com/shared/img/icons/restatic-256.png
facebook: 1
#retweet: 0
buzz: 1
fbsdk: 1
#flattr: http://restatic.binaryage.com
ogmeta: {
    site_name: "BinaryAge website",
    description: "Restatic pumps Google spreadsheet content to static sites",
    email: "honza@binaryage.com",
    type: "product",
    title: "Restatic",
    url: "http://restatic.binaryage.com",
    image: "http://www.binaryage.com/shared/img/icons/restatic-256.png"
}
shots: [{
    title: "Restatic - a new way how to get Google spreadsheet data to your static site",
    thumb: "/shared/img/restatic-mainshot.png",
    full: "/shared/img/restatic-mainshot-full.png"
}]
---
  
## Usage

### Use Google spreadsheet as a simple CMS

Do you build static web sites for your clients? Do they call you back when they need some changes?

With Restatic you may leave them editing their data in Google Spreadsheet and regenerate the site when needed. You will provide them with environment which they know and love - we hope your clients are smart enough to love Google Docs :-)

### Add markup to your static site

Just put to your html markup pointing to your data, for example `/-Posts-B2-/`

  * '/-' and '-/' are separators (delimiters)
  * 'Posts' is a sheet name (gdocs spreadsheet page name)
  * 'B2' is the cell address
  * '-' is a separator between sheet name and the cell specification

Here is small visualization
<img src="/images/restatic_visualisation.png" alt="visualization" width="900px">

### Publish your Google spreadsheet

Turn on "Publish to the web" (In File->Publish to the web) and you get the spreadsheet key.

### Configure restatic with restatic.json

  * `apiKey: 0AtkoCAIRJ7BPdGM2Y2tYdV9XRXNsNVVrVnFPeFIwb0E`
  * `delimiter: /-, -/`

### Call restatic to regenerate your site

    restatic /path/to/source/dir /path/to/target/dir' 
	
Your freshly built site will be generated into target dir. 
Or alternatively go to the source directory and run `restatic -d` and your site will be generate to `_site` directory in source dir.

## Installation

`npm install restatic -g`

## FAQ
### How user can update site after spreadsheet change?
We have this feature in roadmap - <a href="mailto:jan@binaryage.com">tell us</a> that you need it!

### Do we plan a hosting solution?
We're thinking about it. Want you have hosting service for your restatic powered sites? <a href="mailto:jan@binaryage.com">Let us know!</a>

### Do we plan windows version?
Restatic is not tested on windows, but it doesn't use any linux specific scripts - so try it.

### How to integrate Restatic with Jekyll?
Easilly - You could run restatic on jekyll generated site.

### How to use multiple spreadsheets?
You can run `restatic /source /target fetch` more times with another input data.

### Can I use another data sources?
You could write your own extractor. Just create your Extractor (anywhere you want) and specify it in config using "extractor" : "/path/to/FooExtractor.js" - it should contain function extract which will return the associative array with markup in key and data in value - eg. {"/-Posts-2B-/" : "Hello world"}

## Links
#### Packages used it restatic
  * rimraf (~2.0.1) - [Github](https://github.com/isaacs/rimraf)
  * wrench (~1.3.8) - [Github](https://github.com/ryanmcgrath/wrench-js)
  * mocha (~1.0.1) - [Github](https://github.com/visionmedia/mocha)
  * should (~0.6.1) - [Github](https://github.com/visionmedia/should.js)
  * ansi (~0.1.0) - [Github](https://github.com/TooTallNate/ansi.js)

#### Source code
  * [Sources are hosted on GitHub](https://github.com/binaryage/restatic)

#### Example
  * [Example](http://restatic-example.herokuapp.com)