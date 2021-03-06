# opening_hours_html_formatter.js

This library can be used to HTML format opening hours.
The opening hours must conform to the [OpenStreetMap opening hours format specification][osm-openinghours].


## Usage

Please take a look at the [demo](demo/index.html) to understand how to integrate the library.

A typical processing chain looks something like this:

```
"Mo-Tu, Th-Su 08:00-20:00"

           ||
           \/
      ______________
     /              \
     | OpeningTimes |
     \______________/

           ||
           \/
     _______________
    /               \
    | WeekGenerator |
    \_______________/

           ||
           \/
 ________________________
/                        \
| WeekTableHtmlGenerator |
\________________________/

           ||
           \/

       HTML table
```

Please note, that all elements of the library can be found under the following namespace:

``` js
window.ohhf.*
```

## Deployment

A shell script is used to concatenate all JavaScript files into one.
Run the following command to generate the library:

``` bash
$ deploy/deploy.sh
```

Afterwards, the generated one-file-library can be found in the [dist](dist/) folder.


## Dependencies

The following libraries are used by this library and must be provided in the application project.

* [opening_hours.js][opening-hours-js]
* [moment.js][moment-js]


## License

This library is freely distributable under the terms of the [MIT license](LICENSE).



[moment-js]: http://momentjs.com
[opening-hours-js]: https://github.com/opening-hours/opening_hours.js/tree/master
[osm-openinghours]: https://wiki.openstreetmap.org/wiki/Key:opening_hours/specification
