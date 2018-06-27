# Donation Envelope

[![Build status](https://ci.appveyor.com/api/projects/status/8gpxn0fx2qmyqb6p?svg=true)](https://ci.appveyor.com/project/lcamichigan/donation-envelope)

This is an InDesign file of a No.&nbsp;9 envelope for mailing donations to Sigma
Alumni Association.

## Contents

* [Getting Started](#getting-started)
* [Creating an InDesign File](#creating-an-indesign-file)

## Getting Started

To create the envelope, you need:

* [Adobe InDesign](https://www.adobe.com/products/indesign.html). Visit
  https://www.adobe.com/creativecloud/plans.html for more information.

* Envelope.idml. The easiest way to get this file is to download it from
  https://ci.appveyor.com/project/lcamichigan/donation-envelope/build/artifacts,
  but you can also [create your own](#creating-an-indesign-file).

* These fonts:

  | Font                                                   | Download URL                                                             |
  |--------------------------------------------------------|--------------------------------------------------------------------------|
  | [Damion](https://fonts.google.com/specimen/Damion)     | https://github.com/google/fonts/raw/master/ofl/damion/Damion-Regular.ttf |
  | [Gillius](http://arkandis.tuxfamily.org/adffonts.html) | http://arkandis.tuxfamily.org/fonts/Gillius-Collection-20110312.zip      |

## Creating an InDesign File

Creating an InDesign IDML file from the files in this repository requires the
free [Zip](http://www.info-zip.org/Zip.html) utility. To install Zip on Windows:

1. Download zip300xn-x64.zip from
   ftp://ftp.info-zip.org/pub/infozip/win32/zip300xn-x64.zip.

2. Right-click zip300xn-x64.zip, choose Extract All, and then click Extract to
   extract a folder named zip300xn-x64.

3. Right-click zip300xn-x64.zip in the zip300xn-x64 folder you just extracted,
   choose Extract All, and then click Extract to extract another folder named
   zip300xn-x64.

4. Move this second zip300xn-x64 folder to C:\Program Files.

Zip is included with macOS.

To create an InDesign file, first download this repository as a ZIP archive. To
do this, click
[here](https://github.com/lcamichigan/donation-envelope/archive/master.zip).
Unzip the archive wherever you wish. Then, `cd` to the
[Envelope IDML](Envelope%20IDML) folder and enter in PowerShell

```powershell
& "$env:ProgramFiles\zip300xn-x64\zip" -X0 ..\Envelope.idml mimetype
& "$env:ProgramFiles\zip300xn-x64\zip" --recurse-paths --no-dir-entries -X9 ..\Envelope.idml * --exclude mimetype
```

or in Command Prompt

```batch
"%ProgramFiles%\zip300xn-x64\zip" -X0 ..\Envelope.idml mimetype
"%ProgramFiles%\zip300xn-x64\zip" --recurse-paths --no-dir-entries -X9 ..\Envelope.idml * --exclude mimetype
```

or in Terminal

```sh
zip -X0 ../Envelope.idml mimetype
zip --recurse-paths --no-dir-entries -X9 ../Envelope.idml * --exclude *.DS_Store mimetype
```
