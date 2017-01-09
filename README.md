ZipKit
======

[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage)

ZipKit is an Objective-C framework for reading and writing Zip archives in OS X and iOS apps. It supports:

* the standard [PKZip format](http://www.pkware.com/documents/casestudies/APPNOTE.TXT);
* files larger than 4GB in size using PKZip's zip64 extensions (ZKFileArchive only);
* optionally, resource forks in a manner compatible with OS X's Archive Utility (in the OS X targets only);
* clean interruption, so archiving can be cancelled by the invoking object (e.g., a NSOperation or NSThread).

It was developed by Karl Moskowski (aka [@kolpanic](https://twitter.com/kolpanic)) and released under the BSD license. iOS framework and Carthage support were added by [Stuart Malone](https://github.com/samalone).

If you find ZipKit to be useful, please [let me know](http://about.me/kolpanic).

###Requirements

ZipKit requires Xcode 8.2.1. It works on OS X 10.8 Mountain Lion, and iOS 8.0 or greater. The Xcode project contains two targets:

* an OS X framework
* an iOS framework

###Using ZipKit

This fork of ZipKit supports [Carthage](https://github.com/Carthage/Carthage). To use it:

1. Add `github "samalone/ZipKit" ~> 1.0` to your [Cartfile](https://github.com/Carthage/Carthage/blob/master/Documentation/Artifacts.md#cartfile).
2. In a terminal window, go to your Xcode project directory and type `carthage bootstrap`.
3. Drag the file `Carthage\Build\iOS\ZipKit.framework` or `Carthage\Build\macOS\ZipKit.framework` to the Embedded Binaries section of the General settings for your application target.
 
See the accompanying demo projects for guidance.

###License

ZipKit is released under the BSD license. It's in COPYING.TXT in the project. Acknowledge ZipKit (and other FOSS projects you use) in your app's About or Settings view or window. (If your iOS app doesn't have either, you can add a Settings Bundle; see the ZipKit Touch demo.)

###Demo Projects
* [ZipKit Utility](https://github.com/kolpanic/ZipKit-Utility) - an OS X Cocoa application
* [zku](https://github.com/kolpanic/zku) - an OS X command line tool
* [ZipKit Touch](https://github.com/kolpanic/ZipKit-Touch) - an iOS application

####Note
This project was originally a Mercurial repository hosted at Bitbucket. It was converted to git using [fast-export](https://github.com/frej/fast-export), and all open issues were manually copied here.
