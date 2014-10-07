# TiUUID Module

## Description

TODO: Enter your module description here

## Accessing the TiUUID Module

To access this module from JavaScript, you would do the following:

    var tiuuid = require("it.scsoft.tiuuid");

The tiuuid variable is a reference to the Module object.

## Reference

TODO: If your module has an API, you should document
the reference here.

### tiuuid.function

TODO: This is an example of a module function.

### tiuuid.property

TODO: This is an example of a module property.

## Usage

var tiuuid = require('it.scsoft.tiuuid');

//changes each time (no persistent)
tiuuid.uuid();

//changes each time the app gets launched (persistent to session)
tiuuid.uuidForSession();

//changes each time the app gets installed (persistent to installation)
tiuuid.uuidForInstallation();

//changes each time all the apps of the same vendor are uninstalled (this works exactly as identifierForVendor)
tiuuid.uuidForVendor();

//changes only on system reset, this is the best replacement to the good old udid (persistent to device)
tiuuid.uuidForDevice();

//returns the list of all uuidForDevice of the same user
//in this way it's possible manage guest accounts across multiple devices easily.
tiuuid.uuidsOfUserDevices();

## Author

TODO: Enter your author name, email and other contact
details you want to share here.

## License

TODO: Enter your license/legal information here.
