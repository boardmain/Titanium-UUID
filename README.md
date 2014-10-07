# Titanium UUID

## Description

TiUUID  library as alternative to the old good UDID and identifierForVendor.

This library provides the simplest API to obtain universally unique identifiers with different persistency levels.
All methods can be called as static methods or via the shared instance.

It's possible to retrieve the UUIDs created for all devices of the same user, in this way with a little bit of server-side help it's possible manage guest accounts across multiple devices easily.

## Quick Start

### Get it [![gitTio](http://gitt.io/badge.png)](http://gitt.io/component/it.scsoft.tiuuid)
Download the latest distribution ZIP-file and consult the [Titanium Documentation](http://docs.appcelerator.com/titanium/latest/#!/guide/Using_a_Module) on how install it, or simply use the [gitTio CLI](http://gitt.io/cli):

`$ gittio install it.scsoft.tiuuid`


## Community Driven

I encourage everyone to send Pull Requests - keeping this module flying with new features.


## Author

**Samuele Coppede'**  
web: http://www.scsoft.it  
email: samuele@scsoft.it
twitter: @samuele81



# Example 

```javascript


var tiuuid = require('it.scsoft.tiuuid');

Ti.API.info('UUID:'+tiuuid.uuid());
Ti.API.info('UUID for Session:'+tiuuid.uuidForSession());
Ti.API.info('UUID for Vendot:'+tiuuid.uuidForVendor());
Ti.API.info('UUID for Device:'+tiuuid.uuidForDevice());
Ti.API.info(JSON.stringify(tiuuid.uuidsOfUserDevices()));

```


##API
All the following methods (excluding the last one) return a different Universally Unique Identifier, each one with its own persistency level.

```objective-c
//changes each time (no persistent)
tiuuid.uuid();

//changes each time the app gets launched (persistent to session)
tiuuid.uuidForSession();

//changes each time the app gets installed (persistent to installation)
tiuuid.uuidForInstallation();

//changes each time all the apps of the same vendor are uninstalled (this works exactly as identifierForVendor)
tiuuid.uuidForVendo()r;

//changes only on system reset, this is the best replacement to the good old udid (persistent to device)
tiuuid.uuidForDevice();

//returns the list of all uuidForDevice of the same user
//in this way it's possible manage guest accounts across multiple devices easily.
tiuuid.uuidsOfUserDevices();
```


## License

	Titanium Port for the Library [FCUUID](https://github.com/fabiocaccamo/FCUUID) by Fabio Caccamo
	
    Copyright (c) 2010-2014 Samuele Coppede

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in
    all copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
    THE SOFTWARE.
    


------------------------------
