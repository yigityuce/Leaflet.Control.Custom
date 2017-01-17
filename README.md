# Leaflet.Control.Custom

A Customizable Leaflet Control Panel.
You can insert any HTML element to map corners with

  - Custom **id**
  - Custom **title**
  - Custom **classes**
  - Custom **styles**
  - Custom **data attributes**
  - Custom **events**


## Requirements
Leaflet v0.6.0+


## Installation

Include script inside the head tag after Leaflet:

```
<script src="Leaflet.Control.Custom.js"></script>
```



## Examples
[Basic Demo](https://yigityuce.github.io/Leaflet.Control.Custom/examples/index.html)



## Usage

```

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
        cursor: 'pointer',
    },
    datas   :
    {
        'foo': 'bar',
    },
    events:
    {
        click: function(data)
        {
            console.log('wrapper div element clicked');
            console.log(data);
        },
        dblclick: function(data)
        {
            console.log('wrapper div element dblclicked');
            console.log(data);
        },
        contextmenu: function(data)
        {
            console.log('wrapper div element contextmenu');
            console.log(data);
        },
    }
})
.addTo(map);
```


## Options

Option | Values | Default | Description
:--- | :--- | :--- | :---
position | "topleft", "topright", "bottomleft", "bottomright" | "topright" | map position of element
| id | String | - | wrapper div element's id
| title | String | - | wrapper div element's title
| classes | String | - | wrapper div element's class(es) [*Seperate multiple class with space character*] [MDN Element.className](https://developer.mozilla.org/en-US/docs/Web/API/Element/className)
| content | String | - | html content
| style | Object | - | wrapper div element's class(es) [MDN HTMLElement.style](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/style)
| datas | Object | - | wrapper div element's data(s) [MDN HTMLElement.dataset](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/dataset)
| events | Object | - | wrapper div element's event(s) and its callbacks




## License

MIT


## Version History

Version | Date | Description
:--- | :--- | :--- | :---
| v1.0.1 | Jan 17, 2017 | Stopped scroll propagation over control wrapper
| v1.0.0 | Jan 10, 2017 | -
