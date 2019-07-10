#Ifc converter for Node.js
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FbleungAtGTI%2Fifc-convert.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2FbleungAtGTI%2Fifc-convert?ref=badge_shield)


A simple promised based wrapper for the IfcConvert program for node.

#Requirements

- IfcConvert, Installation instructions and binaries can be found at the [ifcOpenShell](http://ifcopenshell.org/ifcconvert.html) page.

#Usage

```javascript
var ifcConvert = require('ifc-convert');

ifcConvert('source.ifc', 'dest.dae')
    .then(function() {
        //Now you have a Collada file;)
    });

ifcConvert('source.ifc', 'dest.obj')
    .then(function() {
        //Now you have a Wavefront OBJ file with an .mtl file
    });

ifcConvert('source.ifc', 'dest.stp')
    .then(function() {
        //Now you have a STEP file
    });

ifcConvert('source.ifc', 'dest.igs')
    .then(function() {
        //Now you have a IGES file
    });

```

#Options

If you do not have IfcConvert in your path you can give it in options.

```javascript
ifcConvert('source.ifc', 'dest.dae', {path: 'path/to/bin'})
    .then(function() {
        //Done
    });
```


## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FbleungAtGTI%2Fifc-convert.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2FbleungAtGTI%2Fifc-convert?ref=badge_large)