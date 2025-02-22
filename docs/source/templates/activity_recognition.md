---
title: Activity Recognition
type: templates
category: Time Series Analysis
cat: time-series-analysis
order: 703
meta_title: Activity Recognition Data Labeling Template
meta_description: Template for labeling human activity recognition in a time series using Label Studio for your machine learning and data science projects.
---

If you want to perform time series classification for human activity recognition, use this template to classify different activities across several time series channels.

## Labeling Configuration

```html
<View>
    <!-- Control tag for region labels -->
    <TimeSeriesLabels name="label" toName="ts">
        <Label value="Run" background="red"/>
        <Label value="Walk" background="green"/>
        <Label value="Fly" background="blue"/>
        <Label value="Swim" background="#f6a"/>
        <Label value="Ride" background="#351"/>
    </TimeSeriesLabels>

    <!-- Object tag for time series data source -->
    <TimeSeries name="ts" valueType="url" value="$timeseriesUrl"
                sep=","
                timeColumn="time"
                timeFormat="%Y-%m-%d %H:%M:%S.%f"
                timeDisplayFormat="%Y-%m-%d"
                overviewChannels="velocity">

        <Channel column="velocity"
                 units="miles/h"
                 displayFormat=",.1f"
                 strokeColor="#1f77b4"
                 legend="Velocity"/>

        <Channel column="acceleration"
                 units="miles/h^2"
                 displayFormat=",.1f"
                 strokeColor="#ff7f0e"
                 legend="Acceleration"/>
    </TimeSeries>
</View>
```

## Related tags

- [TimeSeriesLabels](/tags/timeserieslabels.html)
- [TimeSeries](/tags/timeseries.html)
