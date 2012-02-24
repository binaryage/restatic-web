---
layout: product2
title: Restatic is lightweight tool for parsing google spreadsheet content to static sites
product: restatic
product_title: Restatic
product_subtitle: parsing google spreadsheet content to static sites
note: 
download: https://github.com/JPalounek/restatic/zipball/master
downloadtitle: Download v0.2
downloadsubtitle: Requires OS X 10.6 or higher
repo: https://JPalounek@github.com/JPalounek/restatic.git
meta_title: Restatic is lightweight tool for parsing google spreadsheet content to static sites
meta_keywords: restatic,static-site,osx,google-docs,google, binaryage,software,tool
meta_description: Restatic is lightweight tool for parsing google spreadsheet content to static siteskeyboard shortcut
meta_image: http://www.binaryage.com/shared/img/icons/totalterminal-256.png
facebook: 1
retweet: 1
buzz: 1
fbsdk: 1
#flattr: http://restatic.binaryage.com
ogmeta: {
    site_name: "BinaryAge website",
    description: "Restatic is lightweight tool for parsing google spreadsheet content to static sites",
    email: "support@binaryage.com",
    type: "product",
    title: "Restatic",
    url: "http://restatic.binaryage.com",
    image: "/images/restatic64.png"
}
shots: [{
    title: "Restatic - new way to parse google docs spreadsheet to your static site.",
    thumb: "/shared/img/totalterminal-mainshot.png",
    full: "/shared/img/totalterminal-mainshot-full.png"
}]
---



## Installation

You can install whole tool with just a row of code to execute in your terminal.
> sudo bash < <(curl -s https://raw.github.com/JPalounek/restatic/master/install.sh)

And you can also update it with executing
> sudo bash < <(curl -s https://raw.github.com/JPalounek/restatic/master/update.sh)
  
---
  
## FAQ

#### How I can parse a content to my static site?

It's quite simple. First you should do is configure it - in directory in which you decided to put your content create file 

> restatic.yml

and put there these lines

> googleSpreadSheetKey: 0AtkoCAIRJ7BPdGM2Y2tYdV9XRXNsNVVrVnFPeFIwb0E <br>
> sheetsIds: 1, 2 <br>
> delimiter: /-, -/ <br>

#### What it means? 
Google spreadsheet key is key which gave you google when you turned on "Publish to the web" (In File->Publish to the web).
Sheet ids - means numbers of sheets which you are going to use - don't put there sheet names use just numbers. - it's optional variable
Delimiter - means separator of cell specification in html - it's optional variable

#### How to write page content?
Just put to html something like

> /-Posts-B2-/

Where '/-' and '-/' are separators (delimiters), 'Posts' is page name (gdocs spreadsheet page name), '-' is separator between page name and cell specification, 'B2' is cell name (cell from gdocs spreadsheet on previously specified sheet).

#### How to parse data to site?
Just call 'restatic /path/to/source/dir /path/to/target/dir' and you freshly built site is prepared in target dir.

#### Inspire in our Restatic bootstrap
> https://JPalounek@github.com/JPalounek/restatic-bootstrap.git

## Changelog
This project is too young to have a changelog. And in too progressive development - so wait while we will stabilize it.

<!--
<div class="changelogx"></div>

<script type="text/javascript" charset="utf-8">
    $(function() {
        $('.changelogx').load('changelog-beta.html?x='+((Math.random()+"").substring(2))+' #page');
    });
    
    function showBetaHint() {
        $('.betahint').toggle();
    }
</script>
-->

## Links

#### Source code
  * [sources are hosted on GitHub](https://JPalounek@github.com/JPalounek/restatic.git)