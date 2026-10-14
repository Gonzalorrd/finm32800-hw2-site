# Dataframe: `hw2:fed_funds_futures` - 30-Day Fed Funds Futures

Daily open, high, low, close, and volume bars (ohlcv-1d schema) for 30-Day Fed Funds futures, pulled from the CME Globex dataset (GLBX.MDP3) on Databento with the parent symbol ZQ.FUT, which returns every listed contract. One row per contract per trading day, over the trailing window set by START_DATE and END_DATE (about 180 days by default). Columns: date (tz-naive trading date), symbol, open, high, low, close, volume. The symbol column holds outright monthly contracts such as ZQU6 and calendar spreads such as ZQU6-ZQZ6; drop the spreads with fedwatch.filter_outright_contracts. A contract settles at 100 minus the average daily effective fed funds rate over its month, so 100 - close is the market's expected average rate for that month. Thinly traded far-dated months may have no bar on some days.


## DataFrame Glimpse

```
Rows: 11764
Columns: 7
$ date   <datetime[ns]> 2026-10-13 00:00:00
$ symbol          <str> 'ZQF7'
$ open            <f64> 95.85
$ high            <f64> 95.86
$ low             <f64> 95.83
$ close           <f64> 95.835
$ volume          <u64> 55707


```

## Dataframe Manifest

| Dataframe Name                 | 30-Day Fed Funds Futures                                                          |
|--------------------------------|--------------------------------------------------------------------------------------|
| Dataframe ID                   | [fed_funds_futures](../dataframes/hw2/fed_funds_futures.md)                                       |
| Sources                        | CME Group                                          |
| Providers                      | Databento                                        |
| Provider Links                 | https://databento.com/                                   |
| Tags                           | Monetary Policy, Futures, Fed Funds, Fedwatch                                             |
| Access Types                   |                                       |
| How is data pulled?            | Databento API via Python                                                   |
| Data available up to (min)     | 2026-10-13 00:00:00                                                             |
| Data available up to (max)     | 2026-10-13 00:00:00                                                             |
| Dataframe Path                 | C:\Users\gonza\Documents\UChicago\Quarters\Fall II\FINM 32800 - Data Pipelines\Homeworks\hw2-Gonzalorrd\_data\fed_funds_futures.parquet                                             |


**Linked Charts:**


- [hw2:fedwatch_latest_forecast](../../charts/hw2.fedwatch_latest_forecast.md)



## Pipeline Manifest

| Pipeline Name                   | HW 2: The Yield Curve and the Policy Path                       |
|---------------------------------|--------------------------------------------------------|
| Pipeline ID                     | [hw2](../../../index.md)              |
| Maintainer                      | Jeremiah Bejarano               |
| Contributors                    | Jeremiah Bejarano |
| Repository                     | https://github.com/hw-finm-32800/hw2                  |
| Pipeline Web Page               | <a href="file://C:/Users/gonza/Documents/UChicago/Quarters/Fall II/FINM 32800 - Data Pipelines/Homeworks/hw2-Gonzalorrd/docs/index.html">Pipeline Web Page      |
| Date of Last Code Update        | 2026-10-14 14:30:26           |
| OS Compatibility                | Windows, Linux, macOS |
| Linked Dataframes               |  [hw2:crsp_treasury_consolidated](../../dataframes/hw2/crsp_treasury_consolidated.md)<br>  [hw2:fed_yield_curve](../../dataframes/hw2/fed_yield_curve.md)<br>  [hw2:fed_funds_futures](../../dataframes/hw2/fed_funds_futures.md)<br>  |


**Build Commands:**
```
doit

```

