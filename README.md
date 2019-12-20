# Vue Map Chart

A Vue JS Component for displaying dynamic data on a world map.

![preview](https://raw.githubusercontent.com/maguayo/vue-map-chart/master/preview/preview-world.png)


## Credits

- Most of this code is copied from [https://github.com/Ghrehh/vue-world-map](https://github.com/Ghrehh/vue-world-map)
- Map SVG [amCharts](https://www.amcharts.com/svg-maps/?map=world)


## Installation

Install via npm using `npm install vue-map-chart`
``` javascript
import MapChart from 'vue-map-chart'
```

## Usage

This component is most useful in creating a heat map for various countries. And
will color countries differently based on a props passed.

The component requires a prop of `countryData` to be passed to it, which is a JS
object formatted like so.

``` javascript
{
  "US": 100,
  "CA": 120,
  "GB": 400,
}
```

Where the key is a country's
[ISO 3166 Code](https://en.wikipedia.org/wiki/ISO_3166) and the value is a
numerical value associated with it.

Example:
``` javascript
import MapChart from 'vue-map-chart'

<MapChart
  :countryData="{'US': 4, 'CA': 7, 'GB': 8, 'IE': 14, 'ES': 21}"
  highColor="#ff0000"
  lowColor="#aaaaaa"
  countryStrokeColor="#909090"
  defaultCountryFillColor="#dadada"
  />
```

## API

| Props | Description | Optional |
| --- | --- | --- |
| countryData | See Usage Section above for details  | no |
| lowColor | Countries with lower values will be colored more strongly with this color | yes |
| highColor | Countries with higher values will be colored more strongly with this color | yes |
| defaultCountryFillColor | Countries with no data will default to this color | yes |
| countryStrokeColor | The color of the border around countries | yes |
| legendBorderColor | (WIP) The color of the legend's border | WIP |
| legendHeaderBackgroundColor | (WIP) The background color of the legend's header | WIP |
| legendContentBackgroundColor | (WIP) The background color of the legend's content | WIP |
| showLegend | (WIP) If true, when you select a country a legend will appear on the screen | WIP |


## Roadmap
- Change Map type (World, Europe, single country, etc...) (WIP)
- Click events
- More customization
- Export PDF/CSV