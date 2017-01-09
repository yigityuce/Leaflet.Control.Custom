# Leaflet.Control.Custom

A Customizable Leaflet Control Panel

  - Put any HTML element to map corners
  - Bind events
  - Manipulate content at any time

### Requirements
Minimum Leaflet v0.6.0

### Installation

Include script inside the head tag after Leaflet:

```
<script src="Leaflet.Control.Custom.js"></script>
```

### Examples

* [Basic Demo] [PlOd]

### Usage

```sh

var map = L.map('map').setView([41.044663,29.033775], 12);

L.tileLayer('http://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',{
            maxZoom: 19,
            attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>'
}).addTo(map);

L.control.custom({
    position: 'topright',
    content : '<button type="button" class="btn btn-default">'+
              '    <i class="fa fa-crosshairs"></i>'+
              '</button>'+
              '<button type="button" class="btn btn-info">'+
              '    <i class="fa fa-compass"></i>'+
              '</button>'+
              '<button type="button" class="btn btn-primary">'+
              '    <i class="fa fa-spinner fa-pulse fa-fw"></i>'+
              '</button>'+
              '<button type="button" class="btn btn-danger">'+
              '    <i class="fa fa-times"></i>'+
              '</button>'+
              '<button type="button" class="btn btn-success">'+
              '    <i class="fa fa-check"></i>'+
              '</button>'+
              '<button type="button" class="btn btn-warning">'+
              '    <i class="fa fa-exclamation-triangle"></i>'+
              '</button>',
    classes : 'btn-group-vertical btn-group-sm',
    style   :
    {
        margin: '10px',
        padding: '0px 0 0 0',
        cursor: 'pointer'
    },
})
.addTo(map);
```

### Options

 - Write Tests
 - Rethink Github Save
 - Add Code Comments
 - Add Night Mode

License
----

MIT


**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>


