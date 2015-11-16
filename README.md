# Erik



[![Join the chat at https://gitter.im/phimage/Erik](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/phimage/Erik?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat
            )](http://mit-license.org) [![Platform](http://img.shields.io/badge/platform-ios_osx-lightgrey.svg?style=flat
             )](https://developer.apple.com/resources/) [![Language](http://img.shields.io/badge/language-swift-orange.svg?style=flat
             )](https://developer.apple.com/swift) [![Issues](https://img.shields.io/github/issues/phimage/Erik.svg?style=flat
           )](https://github.com/phimage/Erik/issues) [![Cocoapod](http://img.shields.io/cocoapods/v/Erik.svg?style=flat)](http://cocoadocs.org/docsets/Erik/) [![Build Status](https://travis-ci.org/phimage/Erik.svg)](https://travis-ci.org/phimage/Prephirences)


[<img align="left" src="http://www.halloweenmart.com/t_FO60823_PHANTOM_MASK.png" hspace="20">](#logo) Erik (The Phantom of Opera) is an headless browser based on WebKit and HTML parser [Kanna](https://github.com/tid-kijyun/Kanna).

An headless browser allow to run functional tests, to access and manipulate webpages.

```swift
let browser = WebKitBrowser.sharedInstance
browser.visitURL(url]) { htmlDocument, error in
    // browse HTML element, click, form submit
}

```

## Navigation
```swift
let browser = WebKitBrowser.sharedInstance
browser.visitURL(url]) { object, error in
   if let e = error {
   
   } else if let doc = object as? HTMLDocument {
     // HTML Inspection
   }
}
```

## HTML Inspection
Using HTML Parser  [Kanna](https://github.com/tid-kijyun/Kanna) functions you can find element

```swift
// Search for nodes by CSS
for link in doc.css("a, link") {
    println(link.text)
    println(link["href"])
 }

// Search for nodes by XPath
for link in doc.xpath("//a | //link") {
    println(link.text)
    println(link["href"])
}
```

## Links
- [A list of (almost) all headless web browsers in existence](https://github.com/dhamaniasad/HeadlessBrowsers)
- [Wikipédia](https://en.wikipedia.org/wiki/Headless_browser)

## Roadmap
- [x] Basic protocol concepts
- [ ] Submit: Form post
- [ ] Click: follow link

## Lisense
The MIT License. See the LICENSE file for more infomation.

