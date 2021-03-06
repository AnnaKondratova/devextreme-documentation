---
id: dxChartSeriesTypes.BubbleSeries.aggregation.method
acceptValues: 'avg' | 'custom'
type: String
default: 'avg'
---
---
##### shortDescription
Specifies how to aggregate series points.

---
Series points get aggregated by individual [aggregation intervals](/api-reference/20%20Data%20Visualization%20Widgets/dxChart/1%20Configuration/argumentAxis/aggregationInterval '/Documentation/ApiReference/UI_Components/dxChart/Configuration/argumentAxis/aggregationInterval/'). The following list describes aggregation methods available for series of the **Bubble** type:

- *"avg"*       
Calculates the average of all point values in an interval.

- *"custom"*        
Applies a custom aggregate function specified in the [calculate](/api-reference/20%20Data%20Visualization%20Widgets/dxChart/5%20Series%20Types/CommonSeries/aggregation/calculate.md '/Documentation/ApiReference/UI_Components/dxChart/Configuration/series/aggregation/#calculate') property. 

#include common-ref-enum with {
    enum: "`ChartSeriesSelectionrMode`",
    values: "`Avg` and `Custom`"
} Note that although this enum accepts more values, only these can be applied to a **Bubble** series.

#####See Also#####
- [Data Aggregation](/concepts/05%20Widgets/Chart/88%20Data%20Aggregation '/Documentation/Guide/UI_Components/Chart/Data_Aggregation/')