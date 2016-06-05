---
status: published
published: true
title: Distributed contact management using HTTP
author:
  display_name: Sven Pfleiderer
  login: pfleidi
  email: sven@roothausen.de
author_login: pfleidi
author_email: sven@roothausen.de
date: 2010-10-25 08:17:19 UTC
permalink: "/2010/10/25/distributed-contact-management-using-http/"
categories:
- web
- computer
tags:
- code
- computer
- documentation
- http
- programming
- rest
- scala
- software
- web
comments:
- id: 1039
  author: Finkregh
  author_email: finkregh@mafia-server.net
  author_url: ''
  date: '1288009892'
  content: "i have been searching [i]ages[/i] for that; so much win!\r\n\r\nany plans on releasing your frontend somewhere?"
- id: 1040
  author: pfleidi
  author_email: sven@roothausen.de
  author_url: http://blog.roothausen.de
  date: '1288010771'
  content: "It is planned to release the software when it is ready to use ...\r\n\r\nThe
    reasons I postponed the release of the sources are:\r\n\r\n  * The protocol specification
    needs a rework\r\n  * The software itself has some bugs that need to be fixed\r\n
    \ * I'm currently working on my bachelor thesis and other projects\r\n\r\nI'm
    definitely releasing the software under some opensource license, but it may take
    some time. Stay tuned."
- id: 1041
  author: moritz
  author_email: m.haarmann@gmail.com
  author_url: http://momo.brauchtman.net
  date: '1288878560'
  content: hey there. i'm currently also working one ( part-time, which means like
    5 minutes a week ) on a) releasing the thesis, and b) creating a 2-page document
    explaining the protocol. Sven and I should get together soon to manage some of
    the details, but us being busy prevents this quite successfully so far..
---
## The Idea

A few months ago, [Momo](http://momo.brauchtman.net "Momo's blog") came up with an idea to manage contact data in a decentralized and distributed way. The plan was to provide a simple interface to manage and distribute contact data using HTTP. Some weeks ago he finished his bachelor thesis on this topic.

## The Project

After some discussions with Momo, I decided to implement his protocol specification. Fortunately, I had the possibility to do this as a software project at [my university](http://www.hdm-stuttgart.de "HdM Stuttgart"). The project was mentored by [Prof. Kriha](http://www.kriha.org "Kriha.org").

The implementation itself was done using [Scala](http://scala-lang.org "Scala Website"), [Lift](http://liftweb.net "Lift Website") and [MongoDB](http://mongodb.org "MongoDB Website").

## Abstract

For those of you who don't want to download the whole documentation, here's an abstract:

> We all live in times of digital communication: Almost everybody is reachable via cellphone, instant messaging or email. Not only the communication itself evolved but also the communication channels increased dramatically. Some people have multiple email addresses, instant messaging accounts and profiles on several social networks. It is virtually impossible to keep track of all the information available.<br />
 To address these problems, Moritz Haarmann came up with an idea of a system which is able to manage contact data in a distributed and convenient way. The result of this idea was a protocol proposal which enables users to manage their address data so they can just stop worrying about it.

> This documentation describes the implementation details and design decisions made to create an usable software which uses the protocol defined by Moritz.

## Documentation

I've also written [a documentation which describes the protocol specification, some implementation details and the technology used](/uploads/documents/documentation-rddrssr.pdf "documentation-rddrssr.pdf"). Have fun with it.
