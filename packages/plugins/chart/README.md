# vuepress-plugin-chart

A plugin for adding JavaScript charting library [Chart.js](https://www.chartjs.org) to [VuePress](https://vuepress.vuejs.org/) to create interactive charts in Markdown.

[Demo](https://vuepress-theme-gungnir.vercel.app/zh/docs/plugins/chart.html)


&nbsp;

## Installation

Install this plugin with:

```bash
yarn add vuepress-plugin-chart
# or
npm install vuepress-plugin-chart
```

Then add it to your `.vuepress/config.js`:

```js
module.exports = {
  plugins: [
    [
      'vuepress-plugin-chart'
    ]
  ]
}
```


&nbsp;

## Usage

The token info of the code block should be `chart`, for example:

~~~json
```chart
{
  "type": "bar",
  "data": {
    "labels": ["Red", "Blue", "Yellow", "Green", "Purple", "Orange"],
    "datasets": [{
      "label": "Salary",
      "data": [12, 19, 3, 5, 2, 3],
      "backgroundColor": [
        "rgba(255, 99, 132, 1)",
        "rgba(54, 162, 235, 1)",
        "rgba(255, 206, 86, 1)",
        "rgba(75, 192, 192, 1)",
        "rgba(153, 102, 255, 1)",
        "rgba(255, 159, 64, 1)"
      ]
    }]
  },
  "options": {
    "scales": {
      "y": {
        "ticks": {
          "beginAtZero": true,
          "callback": "function(value){ return '￥' + value + 'k'; }"  // functions should be stringified before being passed through `callback`
        }
      }
    }
  }
}
```
~~~

Refer to the [documentation of Chart.js](https://www.chartjs.org/docs/latest/) for more information.


&nbsp;

## License

[MIT](LICENSE)
