---
layout: product2
title: Restatic pumps Google spreadsheet content to static sites
product: restatic
product_title: Restatic
product_subtitle: Pumps spreadsheet data to your static web!
download: https://github.com/binaryage/restatic
downloadtitle: Download v0.2
downloadsubtitle: Requires a POSIX system with PHP
repo: https://github.com/binaryage/restatic
buttons: <a href="http://restatic-example.herokuapp.com" class="button product-button-thumbup"><div><div>Visit Demo Page<div class="product-specs">And get some inspiration...</div></div></div></a>
advert: After installation and Firefox restart you can visit the <a href="/test/index.html">FireQuery test page</a>
meta_title: Restatic pumps Google spreadsheet content to static sites
meta_keywords: restatic,static-site,osx,google-docs,google,binaryage,software,tool
meta_description: Restatic is a command-line utitlity for parsing google spreadsheet content and using it for generating a static site
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
<img src="/images/restatic_visualisation.png" alt="visualization">

### Publish your Google spreadsheet

Turn on "Publish to the web" (In File->Publish to the web) and you get the spreadsheet key.

### Configure restatic with restatic.yml

  * `googleSpreadSheetKey: 0AtkoCAIRJ7BPdGM2Y2tYdV9XRXNsNVVrVnFPeFIwb0E`
  * `delimiter: /-, -/` (optional)

### Call restatic to regenerate your site

    restatic /path/to/source/dir /path/to/target/dir' 
	
Your freshly built site will be generated into target dir. 
Or alternatively go to the source directory and run `restatic -d` and your site will be generate to `_site` directory in source dir.

## Installation

`sudo bash < <(curl -s https://raw.github.com/binaryage/restatic/master/install.sh)`

## FAQ
### How user can update site after spreadsheet change?
It is definitely possible - see the tool Remote https://github.com/JPalounek/restatic-tools and this blogpost - http://jpalounek.github.com/posts/2012/03/19/serverside-restatic-sites-actualization/

### Do we plan a hosting solution?
We're thinking about it. Want you have hosting service for your restatic powered sites? <a href="mailto:jan@binaryage.com">Let us know!</a>

### Do we plan windows version?
No, we don't.

### How to integrate Restatic with Jekyll?
Easilly - You could run restatic on jekyll generated site.

### How to use multiple spreadsheets?
We dont have now support for multiple spreadsheets.

### Can I use another data sources?
You could write your own extractor. Extend the class Extractor and create function extract which will return the associative array with markup in key and data in value - eg. array('/-Posts-2B-/' => 'Hello world')

## Links
#### 3rd-party libraries used in restatic:
  * [Spyc](http://code.google.com/p/spyc)
  * [NFinder](http://phpfashion.com/pohodlne-prochazeni-filesystemem)

#### Source code
  * [Sources are hosted on GitHub](https://github.com/binaryage/restatic)

#### Example
  * [Example](http://restatic-example.herokuapp.com)