# ClassicUO World Map Markers for Ultima Legacy: Reborn

Based on the excellent UO:Renaissance markers available at https://github.com/markdwags/uor-markers

A simple repository to store the map marker points to be used with the World Map in the [ClassicUO](https://github.com/andreakarasho/ClassicUO) client.

![example](https://imgur.com/jvjntAD.gif)

## Installation

- [Download](https://github.com/dallenwilson/ulr-markers/archive/master.zip) this repository.
- Extract all the files into `Data\Client` located at the root of the ClassicUO folder - Do not include the ulr-markers-master folder.
- Eg, you want to see 'Data\Client\Common.csv', not 'Data\Client\ulr-markers-master\Common.csv'.
- Open the World Map or right-click and select `Reload markers`.

If you just want to download the map icons, [click here](https://raw.githubusercontent.com/dallenwilson/ulr-markers/master/MapIcons.zip).

## Format

Creating your own marker file is simple. Create an empty file and enter it using this format:

`x,y,mapindex,name of marker,iconname,color,zoom level`

`x` and `y` are the coordinates for the marker.

The `mapindex` defines what map the client must be on for the marker to display. `0` for `map0.mul`, `1` for `map1.mul`, etc.

The `name of marker` is just that, the name you want to see in the map or when you hover over the marker.

The `iconname` must match the name of the image in the `Data\Client\MapIcons` folder. If no icon exists, it will display a simple dot using the color defined. Icons can be created as `.cur, .png, .jpg, .ico` files.

For `color`, the supported values are `red, green, blue, purple, black, yellow, white, none`.

`zoom level` defines when the icon will show/hide when zooming.  `0 = furthest` and `9 = closest` so if you had a marker zoom level set to 1 (for example dungeon entrances), it will show at any zoom level except if you're all the way out (at 0). Default level is 3.
