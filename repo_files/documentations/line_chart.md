# LineChart

<img src="https://github.com/imaNNeoFighT/fl_chart/raw/master/repo_files/images/line_chart/line_chart.jpg" width="300" >

### How to use
```
FlChartWidget(
      flChart: LineChart(
        LineChartData(
        	// read about it in the below section
        ),
      ),
    );
```

### LineChartData
|PropName		|Description	|default value|
|:---------------|:---------------|:-------|
|lineBarsData| list of [LineChartBarData ](#LineChartBarData ) to showing the lines chart, they will stack and draw on top of each other|[]|
|titlesData| check the [FlTitlesData](base_chart.md#FlTitlesData)| FlTitlesData()|
|gridData| check the [FlGridData](base_chart.md#FlGridData)|FlGridData()|
|borderData| check the [FlBorderData](base_chart.md#FlBorderData)|FlBorderData()|
|minX| minimum x of showing x axis, if null, value will read from input lineBars |null|
|maxX| maximum x of showing x axis, if null, value will read from input lineBars | null|
|minY| minimum y of showing y axis, if null, value will read from input lineBars | null|
|maxY| maximum y of showing y axis, if null, value will read from input lineBars | null|


### LineChartBarData
|PropName		|Description	|default value|
|:---------------|:---------------|:-------|
|show| determines show and hide the bar line|true|
|spots| list of [FlSpot](base_chart.md#FlSpot) x and y coordinates that the line go through it| []
|colors| color of the line, if multiple colors provided gradient will apply|[Colors.redAccent]|
|colorStops| stop positions of the gradient color, [Read More](https://api.flutter.dev/flutter/dart-ui/Gradient/Gradient.linear.html)|null|
|barWidth| stroke width of the line bar|2.0|
|isCurved| curve the line corners on the spots position| false|
|curveSmoothness| smoothness radius of the curve corners (works if isCurved is true) | 0.35|
|isStrokeCapRound| determines if start and end of the bar line is Qubic or Round | false|
|belowBarData| check the [BelowBarData](#BelowBarData) |BelowBarData()|
|dotData| check the [FlDotData](#FlDotData) | FlDotData()|


### BelowBarData
|PropName|Description|default value|
|:-------|:----------|:------------|
|show|determines show or hide the below bar|true|
|colors|color of the belo bar area, if multiple colors provided gradient will apply|[Colors.blueGrey]|
|gradientFrom|determines start of the gradient, each number should be between 0 and 1, [Read More](https://api.flutter.dev/flutter/dart-ui/Gradient/Gradient.linear.html)|Offset(0, 0)|
|gradientTo|determines end of the gradient, each number should be between 0 and 1, [Read More](https://api.flutter.dev/flutter/dart-ui/Gradient/Gradient.linear.html)|Offset(1, 0)|
|gradientColorStops|stop positions of the gradient color, [Read More](https://api.flutter.dev/flutter/dart-ui/Gradient/Gradient.linear.html)|null|


### FlDotData
|PropName|Description|default value|
|:-------|:----------|:------------|
|show|determines show or hide the dots|true|
|dotColor|color of showing dot|Colors.blue|
|dotSize|size of showing dot|4.0|
|checkToShowDot|a function to check show or not show the dot on the given spot|showAllDots|

### some samples
----
##### Sample 1 ([Source Code](/example/lib/line_chart/samples/line_chart_sample1.dart))
<img src="https://github.com/imaNNeoFighT/fl_chart/raw/master/repo_files/images/line_chart/line_chart_sample_1.png" width="300" >


##### Sample 2 ([Source Code](/example/lib/line_chart/samples/line_chart_sample2.dart))
<img src="https://github.com/imaNNeoFighT/fl_chart/raw/master/repo_files/images/line_chart/line_chart_sample_2.png" width="300" >


##### Sample 3 ([Source Code](/example/lib/line_chart/samples/line_chart_sample3.dart))
<img src="https://github.com/imaNNeoFighT/fl_chart/raw/master/repo_files/images/line_chart/line_chart_sample_3.png" width="300" >


##### Sample 4 ([Source Code](/example/lib/line_chart/samples/line_chart_sample4.dart))
<img src="https://github.com/imaNNeoFighT/fl_chart/raw/master/repo_files/images/line_chart/line_chart_sample_4.png" width="300" >


##### Sample 5 ([Source Code](/example/lib/line_chart/samples/line_chart_sample5.dart))
<img src="https://github.com/imaNNeoFighT/fl_chart/raw/master/repo_files/images/line_chart/line_chart_sample_5.png" width="300" >