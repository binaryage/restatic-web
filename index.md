---
layout: product2
title: Restatic is lightweight tool for parsing google spreadsheet content to static sites
product: restatic
product_title: Restatic
product_subtitle: Pump spreadsheet data to your static web!
note: 
download: https://github.com/JPalounek/restatic
downloadtitle: Download v0.2
downloadsubtitle: Requires OS X 10.6 or higher
repo: https://github.com/JPalounek/restatic
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
    email: "honza@binaryage.com",
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
  
## How and Why

#### Why I should use Restatic
Because it's fast way to fill your page with data from the Google documents spreadsheet and its right way how to organize your page content. <br>

Are you creating webs for clients? So use Google Documents as CMS and provide them envronment which they know and are used to work with.

#### How I can parse a content to my static site?

It's quite simple. First you should do is configure it - in directory in which you decided to put your content create file 

`restatic.yml`

and put there these lines

`googleSpreadSheetKey: 0AtkoCAIRJ7BPdGM2Y2tYdV9XRXNsNVVrVnFPeFIwb0E`
`delimiter: /-, -/`

#### What it means? 
Google spreadsheet key is key which gave you google when you turned on "Publish to the web" (In File->Publish to the web).
Delimiter - means separator of cell specification in html - it's optional variable - you shouldnt specify it.

#### How to write page content?
Just put to html something like

`/-Posts-B2-/`

Where '/-' and '-/' are a separators (delimiters), 'Posts' is a sheet name (gdocs spreadsheet page name), '-' is a separator between sheet name and the cell specification, 'B2' is the cell name (cell from gdocs spreadsheet on previously specified sheet).

#### How to parse data to site?
Just call 'restatic /path/to/source/dir /path/to/target/dir' and you freshly built site is prepared in target dir. Or go to source directory and run 'restatic -d' and your site will be generate to '_site' directory in source dir.

#### Inspire in our Restatic bootstrap
`https://JPalounek@github.com/JPalounek/restatic-example.git`

---

## Installation

You can install the whole tool with just executing in your terminal this:
`sudo bash < <(curl -s https://raw.github.com/JPalounek/restatic/master/install.sh)`

And you can also update it with executing
`sudo bash < <(curl -s https://raw.github.com/JPalounek/restatic/master/update.sh)`
  
---

## FAQ

We don't have any questions - ask me on email jan@binaryage.com :) and your question may be here...

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

#### These foreign libraries are used in restatic
  * [Spyc] (http://code.google.com/p/spyc/)
  * [NFinder] (http://phpfashion.com/pohodlne-prochazeni-filesystemem)

#### Source code
  * [sources are hosted on GitHub](https://github.com/JPalounek/restatic)