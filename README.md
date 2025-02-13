
     oo                                                oo dP
                                                          88
     dP .d8888b. 88d888b. .d8888b. 88d8b.d8b. .d8888b. dP 88
     88 88'  `88 88'  `88 88'  `88 88'`88'`88 88'  `88 88 88
     88 88.  .88 88       88.  .88 88  88  88 88.  .88 88 88
     88 `88888P8 dP       `88888P' dP  dP  dP `88888P8 dP dP
     88~ooooooooooooooooooooooooooooooooooooooooooooooooooooo
    odP    your humble and faithful electronic postman 

*A commandline tool to easily and privately handle your e-mail*

Version: **2.0**

Updates on: http://dyne.org/software/jaro-mail

# INTRODUCTION

JaroMail is an integrated suite of interoperable tools for GNU/Linux
and Apple/OSX to manage e-mail communication in a private and efficient
way, without relying too much on on-line services, in fact encouraging
users to store e-mail locally.

Rather than reinventing the wheel, JaroMail reuses existing free and
open source tools working since more than 10 years: 

 executable | function
 ---------- | --------------------
  ZShell    | scripting language
  Mutt      | Mail User Agent
  Fetchmail | Mail Transport Agent
  Procmail  | Filtering Agent
  MSmtp     | the mini SMTP
  Mairix    | search engine
  ABook     | addressbook
  Elinks    | HTML rendering

A round-up on JaroMail features follows:

![JaroMail functions diagram](http://files.dyne.org/jaromail/diagram.png)

* Minimalistic interface with automatic threading
* Targets intensive usage of mailinglists
* Does whitelisting and integrates addressbooks
* Can do search and backup using easy expressions
* Automatically generates filter rules for procmail and sieve
* Computes and shows statistics on mail traffic
* Secure password storage (GPG native, OSX and Gnome keyrings)
* Stores e-mails locally in a reliable format (Maildir)
* Defers connections, all operations run off-line
* Checks SSL server certificates (imap, smtp)
* Supports strong encryption messaging (GnuPG)
* Is multi platform: GNU/Linux/BSD, Apple/OSX
* Old school, used by its author for the past 15 years

# INSTALL

**Apple/OSX** users can simply drag JaroMail into /Applications When
  started JaroMail opens a Terminal window preconfigured with its
  environment, to activate it for any terminal add this to
  `~/.profile`:
```
export PATH=/Applications/JaroMail.app/Contents/Resources/jaro/bin:$PATH
```

**GNU/Linux** users can run `make` to install all needed components
  (done automatically, requires root) and compile auxiliary
  tools. Once compiled then `make install` will put JaroMail in
  `/usr/local`.

The dependencies to be installed on the system for JaroMail are
* build: `bison flex make autoconf automake sqlite3 libgnome-keyring-dev`
* run: `procmail fetchmail msmtp mutt mairix pinentry abook wipe`

Bare in mind **you need to read the Manual**: this software is not
graphical, it is not meant to be intuitive, does not contains
eyecandies (except for stats on mail traffic). JaroMail is operated
via Terminal, configured in plain text and overall made by geeks for
geeks.

# Manual and usage instructions

For a brief overview see the commandline help:
```
 jaro -h
```
When in doubt, make sure you read the User's Manual, it is important.

Download the PDF: https://files.dyne.org/jaromail/jaromail-manual.pdf

Or browse online the latest version:
https://github.com/dyne/JaroMail/blob/master/doc/jaromail-manual.org

# DEVELOPERS

All revisioned in Git, see: https://github.com/dyne/JaroMail

Pull requests and patches welcome, for an overview of current plans
see [TODO](TODO.md)

Our chat channel is **#dyne** on https://irc.dyne.org

Make sure to idle in that channel, answers take some time to come.

We are all idling artists.

# DONATE

Donations are very welcome and well needed.

By donating you will encourage further development.

 https://www.dyne.org/donate

# ACKNOWLEDGEMENTS

The JaroMail software and user's manual is conceived, designed and put
together with a substantial amount of ZShell scripts and some C code
by Denis Roio aka [Jaromil](http://jaromil.dyne.org).

The email envelop NyanCat graphics is kindly contributed by the
Société ECOGEX.

JaroMail makes use of many external components to work and here below
there is a non-inclusive list of those, with authors and contributors.

## Mutt

The Mutt sourcecode included is maintained by Antonio Radici
<antonio@dyne.org> who is also the original maintainer of the Debian
package. Here below the list of Mutt authors:

```
 Copyright (C) 1996-2007 Michael R. Elkins <me@cs.hmc.edu>
 Copyright (C) 1996-2002 Brandon Long <blong@fiction.net>
 Copyright (C) 1997-2008 Thomas Roessler <roessler@does-not-exist.org>
 Copyright (C) 1998-2005 Werner Koch <wk@isil.d.shuttle.de>
 Copyright (C) 1999-2009 Brendan Cully <brendan@kublai.com>
 Copyright (C) 1999-2002 Tommi Komulainen <Tommi.Komulainen@iki.fi>
 Copyright (C) 2000-2004 Edmund Grimley Evans <edmundo@rano.org>
 Copyright (C) 2006-2008 Rocco Rutte <pdmef@gmx.net>
```

## Mairix

The Mairix search engine is licensed GNU GPL v2, made by:

```
 Copyright (C) Richard P. Curnow  2002,2003,2004,2005,2006,2007,2008
 Copyright (C) Sanjoy Mahajan 2005
 Copyright (C) James Cameron 2005
 Copyright (C) Paul Fox 2006
```

With contributions by: Anand Kumria, André Costa, Andreas Amann, Andre
Costa, Aredridel, Balázs Szabó, Bardur Arantsson, Benj. Mako Hill,
Chris Mason, Christoph Dworzak, Christopher Rosado, Chung-chieh Shan,
Claus Alboege, Corrin Lakeland, Dan Egnor, Daniel Jacobowitz, Dirk
Huebner, Ed Blackman, Emil Sit, Felipe Gustavo de Almeida, Ico
Doornekamp, Jaime Velasco Juan, James Leifer, Jerry Jorgenson, Joerg
Desch, Johannes Schindelin, Johannes Weißl, John Arthur Kane, John
Keener, Jonathan Kamens, Josh Purinton, Karsten Petersen, Kevin
Rosenberg, Mark Hills, Martin Danielsson, Matthias Teege, Mikael
Ylikoski, Mika Fischer, Oliver Braun, Paramjit Oberoi, Paul Fox, Peter
Chines, Peter Jeremy, Robert Hofer, Roberto Boati, Samuel Tardieu,
Sanjoy Mahajan, Satyaki Das, Steven Lumos, Tim Harder, Tom Doherty,
Vincent Lefevre, Vladimir V. Kisil, Will Yardley, Wolfgang
Weisselberg.

## MSmtp

MSmtp is developed and maintained by Martin Lambers.

The RFC 822 address parser (fetchaddr) is originally written by
Michael Elkins for the Mutt MUA.

## ABQuery

The gateway to Apple/OSX addressbook (ABQuery) was written by Brendan
Cully and just slightly updated for our distribution.

## Stats modules
We are also including some (experimental, still) modules for statistical
visualization using JQuery libraries:

```
Timecloud is Copyright (C) 2008-2009 by Stefan Marsiske
TagCloud version 1.1.2 (c) 2006 Lyo Kato <lyo.kato@gmail.com>
ExCanvas is Copyright 2006 Google Inc.
jQuery project is distributed by the JQuery Foundation under the
 terms of either the GNU General Public License (GPL) Version 2.
The Sizzle selector engine is held by the Dojo Foundation and is
 licensed under the MIT, GPL, and BSD licenses.
JQuery.sparkline 2.0 is licensed under the New BSD License
Visualize.JQuery by Scott Jehl Copyright (c) 2009 Filament Group 
```

# Disclaimer

JaroMail is Copyright (C) 2010-2014 Denis Roio <jaromil@dyne.org>

This source code is free software; you can redistribute it and/or
modify it under the terms of the GNU Public License as published by
the Free Software Foundation; either version 3 of the License, or (at
your option) any later version.

This source code is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  Please refer to
the GNU Public License for more details.

You should have received a copy of the GNU Public License along with
this source code; if not, write to: Free Software Foundation, Inc.,
675 Mass Ave, Cambridge, MA 02139, USA.
