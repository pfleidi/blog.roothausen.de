---
status: published
published: true
title: Verkleinern von Bildern mit Ruby und Imagemagick
author:
  display_name: Sven Pfleiderer
  login: pfleidi
  email: sven@roothausen.de
author_login: pfleidi
author_email: sven@roothausen.de
date: 2009-08-09 14:38:53 UTC
permalink: "/2009/08/09/verkleinern-von-bildern-mit-ruby-und-imagemagick/"
categories:
- computer
tags:
- code
- computer
- linux
- programming
- ruby
- shortys
- software
- windows
comments:
- id: 997
  author: Claudio
  author_email: geistwc@gmail.com
  author_url: ''
  date: '1250204731'
  content: "\"Unter Windows reicht es Imagamagick und Ruby mit dem Paketmanager seiner
    Wahl...\"\r\n\r\nSeit wann hat Windows einen Paketmanager? ;)\r\n\r\nGrüße"
- id: 998
  author: pfleidi
  author_email: blog2@the-pf.e4ward.com
  author_url: http://blog.roothausen.de
  date: '1250243013'
  content: Ich meinte natuerlich Linux ;)
---
Vor kurzem hatte ich das Bedürfnis Bilder automatisiert, mit Hilfe eines Ruby-Scripts, zu verkleinern. Dieses Script sollte zudem ohne Änderungen sowohl auf Linux als auch auf Windows lauffähig sein.

Fuer diese Aufgabe ist [Imagemagick](http://www.imagemagick.org/) natürlich ein super Werkzeug, da man es auch als Bibliothek von Ruby aus nutzen kann und auch für Windows verfuegbar ist. Unter Windows ist hierfür eine [Installation von Ruby](http://rubyinstaller.rubyforge.org), sowie die [Installation von Imagemagick und dem passenden RMagick Ruby-Gem](http://rmagick.rubyforge.org/install-faq.html#win) notwendig. Unter Linux reicht es Imagamagick und Ruby mit dem Paketmanager seiner Wahl zu installieren und mittels "gem install rmagick" das Gem zu installieren.

Der eigentliche Code gestaltet sich relativ simpel. Prinzipiell lässt sich ein Bild mit wenigen Anweisungen verkleinern:

```ruby
#!/usr/bin/env ruby</p>

require 'rubygems'
require 'RMagick'

@debug = true

def resize\_image(file)
 puts "let's resize #{file} ..." if @debug
 img = Magick::Image::read(file).first
 img.resize\_to\_fit(1024, 1024)
 img.write(file)
 puts "resizing of #{file} successful" if @debug
end
```

Die Methode [resize\_to\_fit()](http://www.imagemagick.org/RMagick/doc/image3.html#resize_to_fit) sorgt hier für das Verkleinern auf bestimmte Maximalwerte in Länge und Breite. Weiteres erfährt man aus der [Doku](http://www.imagemagick.org/RMagick/doc/image3.html).
