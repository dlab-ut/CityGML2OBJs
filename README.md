# :cityscape: CityGML2OBJ 2.0 :cityscape:
Command line converter of **CityGML (.gml)** to **OBJ (.obj)** files, while maintaining the semantics 
This is a fork of the following project
https://github.com/tum-gis/CityGML2OBJv2

![Before-After](https://user-images.githubusercontent.com/44395224/235768949-747bd3c7-e347-45ab-9ae0-713065da90f3.png)

## :arrow_forward: How to run?
Open your command line and type in:
  
  `-i  your-input-citygml-path-here` 
  
  `-o  your-output-obj-path-here` 

Please make sure to use the absolute paths to the respective directories.

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
|epsgの番号を指定します。デフォルトは6677|`--epsg [コード番号]`|
|平面直角座標系におけるxy座標を入れ替え、東がx軸、北がy軸になります。|`-yx`|

### コマンドラインオプション：-yx
- **X座標とY座標の入れ替え**： `-yx` コマンドラインオプションは、生成されたOBJモデル内のx座標とy座標を入れ替えることを可能にします。これによって平面直角座標系で東方向がx軸、北方向がy軸となるように座標系が変更されます。

### EPSGコードのカスタマイズ
`--epsg`オプションを使用してEPSGコードをカスタマイズできます。このオプションにより、ユーザーは変換プロセスにおいて使用するEPSGコードを指定できます。各地域におけるEPSGコードの番号は[平面直角座標系 WEBマップ](https://lemulus.me/column/jpc-map)をご確認下さい。

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

## :sparkles: このフォークで追加された機能

このCityGML2OBJのバージョンでは、オリジナルの[CityGML2OBJ 2.0](https://github.com/tum-gis/citygml2obj-2.0)に対して、以下の追加機能があります：

### 座標系の変換
- **地理座標から面直角座標への変換**：このバージョンでは、地理座標系（緯度と経度）を平面直角座標系に変換する機能などが導入されています。




## :handshake: Credits
This project is based on [CityGML2OBJ 2.0](https://github.com/tum-gis/citygml2obj-2.0) by Thomas Froech, Benedikt Schwab, and Olaf Wysocki. The original project is distributed under the MIT License. See `LICENSE` for more information.


