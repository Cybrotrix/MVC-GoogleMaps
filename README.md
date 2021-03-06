MVC-GoogleMaps
==============

HtmlHelper for using JQuery.GoogleMaps plugin on ASP.NET MVC pages

###What can I do with it
This is HtmlHelper for rendering out GoogleMaps either for editiong or viewing using [JQuery.GoogleMaps plugin](https://github.com/dejanstojanovic/JQuery-GoogleMaps).

The library provides:
* HtmlHelper for rendering out GoogleMap editor of viewer
* Model POCO classes
* Extension methods for serializing and deserializing map model
 
![ScreenShot](http://dejanstojanovic.net/media/31659/googlemap-editor.png)

###How to add to a page
HtmlHelper for GoogleMap can be easily added as any other HtmlHelper in ASP.NET MVC. 
```razor
@Html.GoogleMapEditor("HiddenTreasureMap", new Mvc.GoogleMaps.Models.Map() { editMode=true})
```
However, you will have to add reference to a javascript, jquery and css files manualy in your page. You can referenci them from CDN or from local file system.
```html
<link rel="stylesheet" type="text/css" href="//cdn.jsdelivr.net/jquery.googlemaps/2.2.4/css/mapstyle.min.css" />
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.11.0/jquery.min.js"></script>
<script type="text/javascript" src="//cdn.jsdelivr.net/jquery.googlemaps/2.2.4/jquery.googlemaps.min.js"></script>
```
This library is available as a NuGet package as well, so you van add it to your project through NuGet package manager or console.

[![ScreenShot](http://dejanstojanovic.net/media/23565/nuget-small.png)](https://www.nuget.org/packages/MVC.GoogleMaps/)

Since jQuery.GoogleMaps plugin is available from CDN you can even instantiate it on your page with resources from jsdelivr CDN
```razor
@Html.GoogleMapEditor("test", new Mvc.GoogleMaps.Models.Map()
           {
               editMode = true,
               stylesPath = "//cdn.jsdelivr.net/jquery.googlemaps/2.2.4/styles.json",
               markerPinsPath = "//cdn.jsdelivr.net/jquery.googlemaps/2.2.4/img",
               editTemplatesPath = "//cdn.jsdelivr.net/jquery.googlemaps/2.2.4/html"
           })
```
