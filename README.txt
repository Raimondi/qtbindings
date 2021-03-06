qtbindings
----------
This project provides bindings that allow the QT Gui toolkit to be used from the
Ruby Programming language. Overall it is a repackaging of a subset of the KDE 
bindings ruby and smoke systems into a format that lends itself well to 
packaging into a Ruby gem.

Goals
-----
1. To make it easy to install a Qt binding for Ruby on all platforms using 
   RubyGems
2. To maintain an up-to-date binary gem for Windows that is bundled with 
   the latest version of Qt from http://qt.nokia.com
3. To reduce the scope and maintenance of the bindings to only bind to the 
   libraries provided by the Qt SDK.
4. To increase compatibility with non-linux platforms

Tested Environments
--------------------
Mac OSX 10.6.4 (Snow Leopard)
XCode 3.2.3
Macports 1.9.1
qt4-mac 4.6.3
Cmake 2.8.2

Windows XP SP3
QT SDK 4.6.3
Cmake 2.8.2
Ruby 1.8.7p299 installed from rubyinstaller.org

Ubuntu Linux 10.4
QT SDK 4.6.3
Cmake 2.8.2

Compiling
---------
Compiling qtbindings requires the following prerequisites:
1. cmake 2.6.3+ installed and in your path
2. QT 4.6.x installed and in your path
3. Ruby installed and in your path
4. gcc 4.x

Additionally: all of the operating system prequisites for compiling, 
window system development, opengl, etc must be installed.

Operating Systems Notes:

Debian Linux
------------
1. The following should get you the packages you need:
sudo aptitude install build-essential bison openssl libreadline5 
  libreadline-dev curl git-core zlib1g zlib1g-dev libssl-dev vim 
  libsqlite3-0 libsqlite3-dev sqlite3 libreadline5-dev libreadline6-dev 
  libxml2-dev git-core subversion autoconf xorg-dev libgl1-mesa-dev 
  libglu1-mesa-dev

Mac OSX Snow Leopard
-----------------------
1. XCode
2. qt4-mac installed from macports - NOTE: For some reason smokegen does 
   not work with the SDK or Cocoa libraries directly from qt.nokia.com - 
   Uninstall these if necessary using: 
   sudo python /Developer/Tools/uninstall_qt.py

Windows - Note: Only necessary for debugging (binary gem available)
--------
1. mingw from the Qt SDK in your path: ie C:\Qt\2010.04\mingw\bin

Install
------
On linux/MacOSX you must make sure you have all the necessary prerequisites 
installed or the compile will fail. 

gem install qtbindings

This should always work flawlessly on Windows because everything is nicely 
packaged into a binary gem. However, the gem is very large ~49MB, so please
be patient while gem downloads the file. 

To get help:
Sign up to the kdebindings mailing list at:
https://mail.kde.org/mailman/listinfo/kde-bindings
You can also file tickets here at github for issues specific to the 
qtbindings gem.

License:
This library is released under the LGPL Version 2.1.
See COPYING.LIB.txt

Disclaimer:
Almost all of this code was written by the great guys who work on the KDE 
bindings project, particurly Arno Rehn and Richard Dale. I hope to increase 
the adoption and use of the code that they have written. 
