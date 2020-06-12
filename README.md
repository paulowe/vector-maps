# diningPhilosopher

Configuration Settings

## map 'world_en'
Map you want to load. Must include the javascript file with the name of the map you want. Available maps with this library are world_en, usa_en, europe_en and germany_en

## backgroundColor '#a5bfdd'
Background color of map container in any CSS compatible format.


## borderColor '#818181'
Border Color to use to outline map objects


## borderOpacity 0.5
Border Opacity to use to outline map objects ( use anything from 0-1, e.g. 0.5, defaults to 0.25 )


## borderWidth 3
Border Width to use to outline map objects ( defaults to 1 )


## color '#f4f3f0'
Color of map regions.

## colors
Colors of individual map regions. Keys of the colors objects are country codes according to ISO 3166-1 alpha-2 standard. Keys of colors must be in lower case.

## hoverColor '#c9dfaf'
Color of the region when mouse pointer is over it.

## hoverColors
Colors of individual map regions when mouse pointer is over it. Keys of the colors objects are country codes according to ISO 3166-1 alpha-2 standard. Keys of colors must be in lower case.

## hoverOpacity 0.5
Opacity of the region when mouse pointer is over it.

## scaleColors ['#b6d6ff', '#005ace']
This option defines colors, with which regions will be painted when you set option values. Array scaleColors can have more then two elements. Elements should be strings representing colors in RGB hex format.

## selectedColor '#333333'
Color for a region when you select it

## enableZoom boolean
Whether to Enable Map Zoom ( true or false, defaults to true)

## normalizeFunction 'linear'
This function can be used to improve results of visualizations for data with non-linear nature. Function gets raw value as the first parameter and should return value which will be used in calculations of color, with which particular region will be painted.

# selectedRegions ['MO', 'FL', 'OR']
This is the Region that you are looking to have preselected (two letter ISO code, defaults to null ). See REGIONS.md

# multiSelectRegion boolean
Whether to enable more than one region to be selected at a time.

# onLoad function(event, map)
Callback function which will be called when map is loading, returning the map event and map details.

# showTooltip boolean
Whether to show Tooltips on Mouseover ( true or false, defaults to true )

# onLabelShow function(event, label, code)
Callback function which will be called before label is shown. Label DOM object and country code will be passed to the callback as arguments.

# onRegionOver function(event, code, region)
Callback function which will be called when the mouse cursor enters the region path. Country code will be passed to the callback as argument.

# onRegionOut function(event, code, region)
Callback function which will be called when the mouse cursor leaves the region path. Country code will be passed to the callback as argument.

# onRegionClick function(event, code, region)
Callback function which will be called when the user clicks the region path. Country code will be passed to the callback as argument. This callback may be called while the user is moving the map. If you need to distinguish between a "real" click and a click resulting from moving the map, you can inspect $(event.currentTarget).data('mapObject').isMoving.

# onRegionSelect function(event, code, region)
Callback function which will be called when the selects a region. Country code will be passed to the callback as argument.

# onRegionDeselect function(event, code, region)
Callback function which will be called when the deselects a region. Country code will be passed to the callback as argument.

# onResize function(event, width, height)
Callback function which will be called when the map is resized. Return event, width & height.

# pins { "pk" : "pk_pin_metadata", "ru" : "ru_pin_metadata", ... }
This option defines pins, which will be placed on the regions. The JSON can have only one element against one country code. Elements should be strings containing the HTML or id of the pin (depends on the 'pinMode' option explained next).

# pinMode content
This option defines if the "pins" JSON contains the HTML strings of the pins or the ids of HTML DOM elements which are to be placed as pins.

If the pin mode is "content" (or not specified) then the parameter "pins" contains the stringified html content to be placed as the pins.
