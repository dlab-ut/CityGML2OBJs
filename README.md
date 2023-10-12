# :cityscape: CityGML2OBJ 2.0 :cityscape:
Command line converter of **CityGML (.gml)** to **OBJ (.obj)** files, while maintaining the semantics 

![Before-After](https://user-images.githubusercontent.com/44395224/235768949-747bd3c7-e347-45ab-9ae0-713065da90f3.png)

## :arrow_forward: How to run?
Open your command line and type in:
  
  `-i  your-input-citygml-path-here` 
  
  `-o  your-output-obj-path-here` 

and Bob's your uncle! :construction_worker:

### :wrench: Optional features

| Optional feature | specification |
| -------- | -------- |
| Semanitcs Option|`-s 1`|
| Geometry Validation | `-v 1`|
| Object Preservation | `-g 1`|
| Skip the triangulation | `-p 1`|
| Conversion of the resulting dataset into a local coordinate system | `-t 1`|
| Translation of the CityGML dataset into a local coordinate system before further processing, without saving the translation parameters|`-tC 1`|
| Translation of the CityGML dataset into a local coordinate system before further processing, with saving the translation parameters to a designated .txt file|`-tCw 1`|
|xy座標を入れ替えます。|`-xyz`|


## :page_with_curl: Requirements

### Python packages:

+ [Numpy](http://docs.scipy.org/doc/numpy/user/install.html) 
+ [Triangle](http://dzhelil.info/triangle/)
+ [lxml](http://lxml.de)
+ [Shapely](https://github.com/Toblerity/Shapely)
+ [Decimal](https://docs.python.org/3/library/decimal.html)
+ [pyproj](https://pyproj4.github.io/pyproj/stable/)
  
#### Optional:

+ [Matplotlib](http://matplotlib.org/users/installing.html)

### Tested:

Using Python 3.10 and Windows 10 OS

### CityGML Requirements:

#### Mandatory:

+ CityGML 1.0 or 2.0
+ Files must end with `.gml`, `.GML`, `.xml`, or `.XML`
+ Vertices in either `<gml:posList>` or `<gml:pos>`
+ Your files must be valid (e.g., free check with [CityDoctor](https://www.citydoctor.eu/de/startseite.html))

#### Optional, but recommended:

+ `<gml:id>` for each `<bldg:Building>` and other types of city objects
+ `<gml:id>` for each `<gml:Polygon>`

 
## Limitations

Information on the limitations can be found in this [Wiki Page](https://github.com/tum-gis/citygml2obj-2.0/wiki/Limitations) 

## :handshake: Credits
This project is based on [CityGML2OBJ 2.0](https://github.com/tum-gis/citygml2obj-2.0) by Thomas Froech, Benedikt Schwab, and Olaf Wysocki. The original project is distributed under the MIT License. See `LICENSE` for more information.

## :mailbox: Contact & Feedback

Feel free to open a discussion under Issues or write us an email

- [Thomas Froech](thomas.froech@tum.de)
- [Benedikt Schwab](benedikt.schwab@tum.de) 
- [Olaf Wysocki](olaf.wysocki@tum.de)
