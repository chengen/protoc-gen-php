PHP Protocol Buffer Generator
=============================

This is a plugin for Google's Protocol Buffer Generator, protoc. It generates PHP code from a .proto file.
by Andrew Brampton ([bramp.net](http://bramp.net)) (c) 2010,2013

It's not finished, but supports most common features, and I'm currently using it in a production system.

Install
-------

I've only tested the code on Debian Linux. You may need the following libraries which can be installed from apt:

```
sudo apt-get install libprotobuf-dev libprotobuf-lite7 libprotobuf7 libprotoc-dev libprotoc7
```

To build just type "make".

Use
---

Once compiled you can use it via protoc like so:

```
 protoc -I. -I/usr/include --php_out . --plugin=protoc-gen-php=./protoc-gen-php your.proto
```

This should generate the file "your.proto.php", which should be able to encode and decode protocol buffer messages. When using the generated PHP code you must include the "protocolbuffers.inc.php" file.

There are many TODOs to finish, for example writing better documentation :)

Licence (Simplified BSD License)
--------------------------------
Copyright (c) 2010-2013, Andrew Brampton
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met: 

1. Redistributions of source code must retain the above copyright notice, this
   list of conditions and the following disclaimer. 
2. Redistributions in binary form must reproduce the above copyright notice,
   this list of conditions and the following disclaimer in the documentation
   and/or other materials provided with the distribution. 

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR
ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND
ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

