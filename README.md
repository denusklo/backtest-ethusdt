---
jupyter:
  kernelspec:
    display_name: Python 3.10.7 64-bit
    language: python
    name: python3
  language_info:
    codemirror_mode:
      name: ipython
      version: 3
    file_extension: .py
    mimetype: text/x-python
    name: python
    nbconvert_exporter: python
    pygments_lexer: ipython3
    version: 3.10.7
  nbformat: 4
  nbformat_minor: 2
  orig_nbformat: 4
  vscode:
    interpreter:
      hash: 26de051ba29f2982a8de78e945f0abaf191376122a1563185a90213a26c5da77
---

::: {.cell .markdown}
Using Historic_Crypto API
([David-Woroniuk/Historic_Crypto](https://github.com/David-Woroniuk/Historic_Crypto))
:::

::: {.cell .code execution_count="1"}
``` {.python}
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```
:::

::: {.cell .code execution_count="2"}
``` {.python}
from Historic_Crypto import HistoricalData
import datetime 

tod = datetime.datetime.now()
d = datetime.timedelta(days = 100)
a = tod - d
# print(a.strftime("%Y-%m-%d-00-00"))
new = HistoricalData('ETH-USD',300, a.strftime("%Y-%m-%d-00-00")).retrieve_data()

print(new)

new.to_csv('eth_since_' + a.strftime("%Y%m%d") + '.csv', sep=',')
```

::: {.output .stream .stdout}
    Checking input parameters are in the correct format.
    Formatting Dates.
    Checking if user supplied is available on the CoinBase Pro API.
    Connected to the CoinBase Pro API.
    Ticker 'ETH-USD' found at the CoinBase Pro API, continuing to extraction.
    Provisional Start: 2022-09-08T00:00:00
    Provisional End: 2022-09-09T01:00:00
    Data for chunk 1 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-09-09T01:00:00
    Provisional End: 2022-09-10T02:00:00
    Data for chunk 2 of 97 extracted
    Provisional Start: 2022-09-10T02:00:00
    Provisional End: 2022-09-11T03:00:00
    Data for chunk 3 of 97 extracted
    Provisional Start: 2022-09-11T03:00:00
    Provisional End: 2022-09-12T04:00:00
    Data for chunk 4 of 97 extracted
    Provisional Start: 2022-09-12T04:00:00
    Provisional End: 2022-09-13T05:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 5 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-09-13T05:00:00
    Provisional End: 2022-09-14T06:00:00
    Data for chunk 6 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-09-14T06:00:00
    Provisional End: 2022-09-15T07:00:00
    Data for chunk 7 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-09-15T07:00:00
    Provisional End: 2022-09-16T08:00:00
    Data for chunk 8 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-09-16T08:00:00
    Provisional End: 2022-09-17T09:00:00
    Data for chunk 9 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-09-17T09:00:00
    Provisional End: 2022-09-18T10:00:00
    Data for chunk 10 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-09-18T10:00:00
    Provisional End: 2022-09-19T11:00:00
    Data for chunk 11 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-09-19T11:00:00
    Provisional End: 2022-09-20T12:00:00
    Data for chunk 12 of 97 extracted
    Provisional Start: 2022-09-20T12:00:00
    Provisional End: 2022-09-21T13:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 13 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-09-21T13:00:00
    Provisional End: 2022-09-22T14:00:00
    Data for chunk 14 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-09-22T14:00:00
    Provisional End: 2022-09-23T15:00:00
    Data for chunk 15 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-09-23T15:00:00
    Provisional End: 2022-09-24T16:00:00
    Data for chunk 16 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-09-24T16:00:00
    Provisional End: 2022-09-25T17:00:00
    Data for chunk 17 of 97 extracted
    Provisional Start: 2022-09-25T17:00:00
    Provisional End: 2022-09-26T18:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 18 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-09-26T18:00:00
    Provisional End: 2022-09-27T19:00:00
    Data for chunk 19 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-09-27T19:00:00
    Provisional End: 2022-09-28T20:00:00
    Data for chunk 20 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-09-28T20:00:00
    Provisional End: 2022-09-29T21:00:00
    Data for chunk 21 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-09-29T21:00:00
    Provisional End: 2022-09-30T22:00:00
    Data for chunk 22 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-09-30T22:00:00
    Provisional End: 2022-10-01T23:00:00
    Data for chunk 23 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-01T23:00:00
    Provisional End: 2022-10-03T00:00:00
    Data for chunk 24 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-03T00:00:00
    Provisional End: 2022-10-04T01:00:00
    Data for chunk 25 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-04T01:00:00
    Provisional End: 2022-10-05T02:00:00
    Data for chunk 26 of 97 extracted
    Provisional Start: 2022-10-05T02:00:00
    Provisional End: 2022-10-06T03:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 27 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-06T03:00:00
    Provisional End: 2022-10-07T04:00:00
    Data for chunk 28 of 97 extracted
    Provisional Start: 2022-10-07T04:00:00
    Provisional End: 2022-10-08T05:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 29 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-08T05:00:00
    Provisional End: 2022-10-09T06:00:00
    Data for chunk 30 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-09T06:00:00
    Provisional End: 2022-10-10T07:00:00
    Data for chunk 31 of 97 extracted
    Provisional Start: 2022-10-10T07:00:00
    Provisional End: 2022-10-11T08:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 32 of 97 extracted
    Provisional Start: 2022-10-11T08:00:00
    Provisional End: 2022-10-12T09:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 33 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-12T09:00:00
    Provisional End: 2022-10-13T10:00:00
    Data for chunk 34 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-13T10:00:00
    Provisional End: 2022-10-14T11:00:00
    Data for chunk 35 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-14T11:00:00
    Provisional End: 2022-10-15T12:00:00
    Data for chunk 36 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-15T12:00:00
    Provisional End: 2022-10-16T13:00:00
    Data for chunk 37 of 97 extracted
    Provisional Start: 2022-10-16T13:00:00
    Provisional End: 2022-10-17T14:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 38 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-17T14:00:00
    Provisional End: 2022-10-18T15:00:00
    Data for chunk 39 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-18T15:00:00
    Provisional End: 2022-10-19T16:00:00
    Data for chunk 40 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-19T16:00:00
    Provisional End: 2022-10-20T17:00:00
    Data for chunk 41 of 97 extracted
    Provisional Start: 2022-10-20T17:00:00
    Provisional End: 2022-10-21T18:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 42 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-21T18:00:00
    Provisional End: 2022-10-22T19:00:00
    Data for chunk 43 of 97 extracted
    Provisional Start: 2022-10-22T19:00:00
    Provisional End: 2022-10-23T20:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 44 of 97 extracted
    Provisional Start: 2022-10-23T20:00:00
    Provisional End: 2022-10-24T21:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 45 of 97 extracted
    Provisional Start: 2022-10-24T21:00:00
    Provisional End: 2022-10-25T22:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 46 of 97 extracted
    Provisional Start: 2022-10-25T22:00:00
    Provisional End: 2022-10-26T23:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 47 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-26T23:00:00
    Provisional End: 2022-10-28T00:00:00
    Data for chunk 48 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-28T00:00:00
    Provisional End: 2022-10-29T01:00:00
    Data for chunk 49 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-29T01:00:00
    Provisional End: 2022-10-30T02:00:00
    Data for chunk 50 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-10-30T02:00:00
    Provisional End: 2022-10-31T03:00:00
    Data for chunk 51 of 97 extracted
    Provisional Start: 2022-10-31T03:00:00
    Provisional End: 2022-11-01T04:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 52 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-01T04:00:00
    Provisional End: 2022-11-02T05:00:00
    Data for chunk 53 of 97 extracted
    Provisional Start: 2022-11-02T05:00:00
    Provisional End: 2022-11-03T06:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 54 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-03T06:00:00
    Provisional End: 2022-11-04T07:00:00
    Data for chunk 55 of 97 extracted
    Provisional Start: 2022-11-04T07:00:00
    Provisional End: 2022-11-05T08:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 56 of 97 extracted
    Provisional Start: 2022-11-05T08:00:00
    Provisional End: 2022-11-06T09:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 57 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-06T09:00:00
    Provisional End: 2022-11-07T10:00:00
    Data for chunk 58 of 97 extracted
    Provisional Start: 2022-11-07T10:00:00
    Provisional End: 2022-11-08T11:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 59 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-08T11:00:00
    Provisional End: 2022-11-09T12:00:00
    Data for chunk 60 of 97 extracted
    Provisional Start: 2022-11-09T12:00:00
    Provisional End: 2022-11-10T13:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 61 of 97 extracted
    Provisional Start: 2022-11-10T13:00:00
    Provisional End: 2022-11-11T14:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 62 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-11T14:00:00
    Provisional End: 2022-11-12T15:00:00
    Data for chunk 63 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-12T15:00:00
    Provisional End: 2022-11-13T16:00:00
    Data for chunk 64 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-13T16:00:00
    Provisional End: 2022-11-14T17:00:00
    Data for chunk 65 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-14T17:00:00
    Provisional End: 2022-11-15T18:00:00
    Data for chunk 66 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-15T18:00:00
    Provisional End: 2022-11-16T19:00:00
    Data for chunk 67 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-16T19:00:00
    Provisional End: 2022-11-17T20:00:00
    Data for chunk 68 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-17T20:00:00
    Provisional End: 2022-11-18T21:00:00
    Data for chunk 69 of 97 extracted
    Provisional Start: 2022-11-18T21:00:00
    Provisional End: 2022-11-19T22:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 70 of 97 extracted
    Provisional Start: 2022-11-19T22:00:00
    Provisional End: 2022-11-20T23:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 71 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-20T23:00:00
    Provisional End: 2022-11-22T00:00:00
    Data for chunk 72 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-22T00:00:00
    Provisional End: 2022-11-23T01:00:00
    Data for chunk 73 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-23T01:00:00
    Provisional End: 2022-11-24T02:00:00
    Data for chunk 74 of 97 extracted
    Provisional Start: 2022-11-24T02:00:00
    Provisional End: 2022-11-25T03:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 75 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-25T03:00:00
    Provisional End: 2022-11-26T04:00:00
    Data for chunk 76 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-26T04:00:00
    Provisional End: 2022-11-27T05:00:00
    Data for chunk 77 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-27T05:00:00
    Provisional End: 2022-11-28T06:00:00
    Data for chunk 78 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-28T06:00:00
    Provisional End: 2022-11-29T07:00:00
    Data for chunk 79 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-11-29T07:00:00
    Provisional End: 2022-11-30T08:00:00
    Data for chunk 80 of 97 extracted
    Provisional Start: 2022-11-30T08:00:00
    Provisional End: 2022-12-01T09:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 81 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-12-01T09:00:00
    Provisional End: 2022-12-02T10:00:00
    Data for chunk 82 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-12-02T10:00:00
    Provisional End: 2022-12-03T11:00:00
    Data for chunk 83 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-12-03T11:00:00
    Provisional End: 2022-12-04T12:00:00
    Data for chunk 84 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-12-04T12:00:00
    Provisional End: 2022-12-05T13:00:00
    Data for chunk 85 of 97 extracted
    Provisional Start: 2022-12-05T13:00:00
    Provisional End: 2022-12-06T14:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 86 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-12-06T14:00:00
    Provisional End: 2022-12-07T15:00:00
    Data for chunk 87 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-12-07T15:00:00
    Provisional End: 2022-12-08T16:00:00
    Data for chunk 88 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-12-08T16:00:00
    Provisional End: 2022-12-09T17:00:00
    Data for chunk 89 of 97 extracted
    Provisional Start: 2022-12-09T17:00:00
    Provisional End: 2022-12-10T18:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 90 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-12-10T18:00:00
    Provisional End: 2022-12-11T19:00:00
    Data for chunk 91 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-12-11T19:00:00
    Provisional End: 2022-12-12T20:00:00
    Data for chunk 92 of 97 extracted
    Provisional Start: 2022-12-12T20:00:00
    Provisional End: 2022-12-13T21:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 93 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-12-13T21:00:00
    Provisional End: 2022-12-14T22:00:00
    Data for chunk 94 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-12-14T22:00:00
    Provisional End: 2022-12-15T23:00:00
    Data for chunk 95 of 97 extracted
    Provisional Start: 2022-12-15T23:00:00
    Provisional End: 2022-12-17T00:00:00
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Data for chunk 96 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
    Provisional Start: 2022-12-17T00:00:00
    Provisional End: 2022-12-18T01:00:00
    Data for chunk 97 of 97 extracted
:::

::: {.output .stream .stderr}
    C:\Users\sean1\AppData\Local\Programs\Python\Python310\lib\site-packages\Historic_Crypto\HistoricalData.py:176: FutureWarning: The frame.append method is deprecated and will be removed from pandas in a future version. Use pandas.concat instead.
      data = data.append(dataset)
:::

::: {.output .stream .stdout}
                             low     high     open    close       volume
    time                                                                
    2022-09-08 00:05:00  1632.08  1636.66  1633.88  1633.86   906.641223
    2022-09-08 00:10:00  1633.22  1635.24  1633.78  1633.66   571.596657
    2022-09-08 00:15:00  1631.94  1637.30  1633.65  1634.31   737.752473
    2022-09-08 00:20:00  1632.84  1636.19  1634.47  1633.34   331.129292
    2022-09-08 00:25:00  1629.60  1633.39  1633.39  1630.01   455.804051
    ...                      ...      ...      ...      ...          ...
    2022-12-17 07:40:00  1181.55  1184.11  1182.44  1183.02  1459.669410
    2022-12-17 07:45:00  1180.56  1183.95  1183.25  1181.70   909.092594
    2022-12-17 07:50:00  1181.48  1183.38  1181.76  1183.05   601.106949
    2022-12-17 07:55:00  1182.71  1184.10  1182.91  1183.95   419.138022
    2022-12-17 08:00:00  1183.32  1184.45  1183.95  1183.63   228.393765

    [28896 rows x 5 columns]
:::
:::

::: {.cell .markdown}
The first arguments for `HistoricalData` class is symbol/ticker
information which you want to return (`str` type), second argument is
granularity in seconds (60, 300, 900, 3600, 21600, 86400, `int` type),
third argument is start date of the trade history in the format
YYYY-MM-DD-HH-MM (`str` type), fourth argument is optional which is end
date of the desired trade history in the format of YYYY-MM-DD-HH-MM
(`str` type), its default value is now. `<br>`{=html} After that, the
record will save the data into a csv file.
:::

::: {.cell .markdown}
Data since July 29, 2022
:::

::: {.cell .code execution_count="2"}
``` {.python}
# This is needed if you're using Jupyter to visualize charts:
%matplotlib inline
last100days = 'eth_since_20220729.csv'
data = pd.read_csv(last100days, index_col = 'time')
# Converting the dates from string to datetime format:
data.index = pd.to_datetime(data.index)
data
```

::: {.output .execute_result execution_count="2"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>low</th>
      <th>high</th>
      <th>open</th>
      <th>close</th>
      <th>volume</th>
    </tr>
    <tr>
      <th>time</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2022-07-29 00:05:00</th>
      <td>1724.54</td>
      <td>1726.83</td>
      <td>1726.13</td>
      <td>1725.69</td>
      <td>427.256878</td>
    </tr>
    <tr>
      <th>2022-07-29 00:10:00</th>
      <td>1717.75</td>
      <td>1726.12</td>
      <td>1725.58</td>
      <td>1720.65</td>
      <td>626.614850</td>
    </tr>
    <tr>
      <th>2022-07-29 00:15:00</th>
      <td>1689.45</td>
      <td>1720.89</td>
      <td>1720.67</td>
      <td>1699.02</td>
      <td>5657.571089</td>
    </tr>
    <tr>
      <th>2022-07-29 00:20:00</th>
      <td>1696.42</td>
      <td>1706.89</td>
      <td>1698.96</td>
      <td>1703.48</td>
      <td>1965.359876</td>
    </tr>
    <tr>
      <th>2022-07-29 00:25:00</th>
      <td>1699.33</td>
      <td>1705.85</td>
      <td>1703.82</td>
      <td>1699.94</td>
      <td>1266.102777</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2022-11-06 06:40:00</th>
      <td>1615.29</td>
      <td>1616.98</td>
      <td>1616.85</td>
      <td>1615.46</td>
      <td>209.340523</td>
    </tr>
    <tr>
      <th>2022-11-06 06:45:00</th>
      <td>1614.46</td>
      <td>1616.37</td>
      <td>1615.54</td>
      <td>1616.25</td>
      <td>407.810987</td>
    </tr>
    <tr>
      <th>2022-11-06 06:50:00</th>
      <td>1616.28</td>
      <td>1616.92</td>
      <td>1616.35</td>
      <td>1616.76</td>
      <td>132.739697</td>
    </tr>
    <tr>
      <th>2022-11-06 06:55:00</th>
      <td>1616.04</td>
      <td>1617.31</td>
      <td>1616.76</td>
      <td>1617.09</td>
      <td>183.119694</td>
    </tr>
    <tr>
      <th>2022-11-06 07:00:00</th>
      <td>1616.63</td>
      <td>1617.83</td>
      <td>1617.10</td>
      <td>1617.20</td>
      <td>128.437408</td>
    </tr>
  </tbody>
</table>
<p>28883 rows × 5 columns</p>
</div>
```
:::
:::

::: {.cell .markdown}
Data since Jan 1, 2022
:::

::: {.cell .code execution_count="3"}
``` {.python}
# This is needed if you're using Jupyter to visualize charts:
%matplotlib inline
since2022 = 'eth_since_20220101.csv'
data = pd.read_csv(since2022, index_col = 'time')
# Converting the dates from string to datetime format:
data.index = pd.to_datetime(data.index)
data
```

::: {.output .execute_result execution_count="3"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>low</th>
      <th>high</th>
      <th>open</th>
      <th>close</th>
      <th>volume</th>
    </tr>
    <tr>
      <th>time</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2022-01-01 00:05:00</th>
      <td>3684.96</td>
      <td>3705.64</td>
      <td>3688.78</td>
      <td>3696.76</td>
      <td>951.396208</td>
    </tr>
    <tr>
      <th>2022-01-01 00:10:00</th>
      <td>3686.40</td>
      <td>3698.33</td>
      <td>3696.72</td>
      <td>3691.29</td>
      <td>1012.726630</td>
    </tr>
    <tr>
      <th>2022-01-01 00:15:00</th>
      <td>3683.96</td>
      <td>3691.90</td>
      <td>3691.25</td>
      <td>3687.27</td>
      <td>771.031043</td>
    </tr>
    <tr>
      <th>2022-01-01 00:20:00</th>
      <td>3686.88</td>
      <td>3698.89</td>
      <td>3687.27</td>
      <td>3698.35</td>
      <td>588.404706</td>
    </tr>
    <tr>
      <th>2022-01-01 00:25:00</th>
      <td>3694.00</td>
      <td>3698.82</td>
      <td>3698.82</td>
      <td>3696.76</td>
      <td>303.219324</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2022-10-11 14:40:00</th>
      <td>1283.92</td>
      <td>1287.40</td>
      <td>1284.26</td>
      <td>1284.88</td>
      <td>2188.453125</td>
    </tr>
    <tr>
      <th>2022-10-11 14:45:00</th>
      <td>1283.35</td>
      <td>1286.24</td>
      <td>1284.98</td>
      <td>1284.60</td>
      <td>2131.085450</td>
    </tr>
    <tr>
      <th>2022-10-11 14:50:00</th>
      <td>1283.25</td>
      <td>1285.48</td>
      <td>1284.44</td>
      <td>1283.72</td>
      <td>1778.952546</td>
    </tr>
    <tr>
      <th>2022-10-11 14:55:00</th>
      <td>1281.93</td>
      <td>1286.18</td>
      <td>1283.72</td>
      <td>1281.99</td>
      <td>1945.641490</td>
    </tr>
    <tr>
      <th>2022-10-11 15:00:00</th>
      <td>1281.99</td>
      <td>1282.56</td>
      <td>1282.21</td>
      <td>1282.56</td>
      <td>64.150849</td>
    </tr>
  </tbody>
</table>
<p>81683 rows × 5 columns</p>
</div>
```
:::
:::

::: {.cell .code execution_count="4"}
``` {.python}
df = data.copy()
sma_span = 200
ema_span = 20
df['sma200'] = df['close'].rolling(sma_span).mean()
df['ema20'] = df['close'].ewm(span=ema_span).mean()
df.round(3)
```

::: {.output .execute_result execution_count="4"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>low</th>
      <th>high</th>
      <th>open</th>
      <th>close</th>
      <th>volume</th>
      <th>sma200</th>
      <th>ema20</th>
    </tr>
    <tr>
      <th>time</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2022-01-01 00:05:00</th>
      <td>3684.96</td>
      <td>3705.64</td>
      <td>3688.78</td>
      <td>3696.76</td>
      <td>951.396</td>
      <td>NaN</td>
      <td>3696.760</td>
    </tr>
    <tr>
      <th>2022-01-01 00:10:00</th>
      <td>3686.40</td>
      <td>3698.33</td>
      <td>3696.72</td>
      <td>3691.29</td>
      <td>1012.727</td>
      <td>NaN</td>
      <td>3693.888</td>
    </tr>
    <tr>
      <th>2022-01-01 00:15:00</th>
      <td>3683.96</td>
      <td>3691.90</td>
      <td>3691.25</td>
      <td>3687.27</td>
      <td>771.031</td>
      <td>NaN</td>
      <td>3691.458</td>
    </tr>
    <tr>
      <th>2022-01-01 00:20:00</th>
      <td>3686.88</td>
      <td>3698.89</td>
      <td>3687.27</td>
      <td>3698.35</td>
      <td>588.405</td>
      <td>NaN</td>
      <td>3693.448</td>
    </tr>
    <tr>
      <th>2022-01-01 00:25:00</th>
      <td>3694.00</td>
      <td>3698.82</td>
      <td>3698.82</td>
      <td>3696.76</td>
      <td>303.219</td>
      <td>NaN</td>
      <td>3694.249</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2022-10-11 14:40:00</th>
      <td>1283.92</td>
      <td>1287.40</td>
      <td>1284.26</td>
      <td>1284.88</td>
      <td>2188.453</td>
      <td>1282.024</td>
      <td>1281.600</td>
    </tr>
    <tr>
      <th>2022-10-11 14:45:00</th>
      <td>1283.35</td>
      <td>1286.24</td>
      <td>1284.98</td>
      <td>1284.60</td>
      <td>2131.085</td>
      <td>1281.974</td>
      <td>1281.886</td>
    </tr>
    <tr>
      <th>2022-10-11 14:50:00</th>
      <td>1283.25</td>
      <td>1285.48</td>
      <td>1284.44</td>
      <td>1283.72</td>
      <td>1778.953</td>
      <td>1281.938</td>
      <td>1282.061</td>
    </tr>
    <tr>
      <th>2022-10-11 14:55:00</th>
      <td>1281.93</td>
      <td>1286.18</td>
      <td>1283.72</td>
      <td>1281.99</td>
      <td>1945.641</td>
      <td>1281.877</td>
      <td>1282.054</td>
    </tr>
    <tr>
      <th>2022-10-11 15:00:00</th>
      <td>1281.99</td>
      <td>1282.56</td>
      <td>1282.21</td>
      <td>1282.56</td>
      <td>64.151</td>
      <td>1281.808</td>
      <td>1282.102</td>
    </tr>
  </tbody>
</table>
<p>81683 rows × 7 columns</p>
</div>
```
:::
:::

::: {.cell .code execution_count="5"}
``` {.python}
df.dropna(inplace=True)
df.round(3)
```

::: {.output .execute_result execution_count="5"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>low</th>
      <th>high</th>
      <th>open</th>
      <th>close</th>
      <th>volume</th>
      <th>sma200</th>
      <th>ema20</th>
    </tr>
    <tr>
      <th>time</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2022-01-01 16:40:00</th>
      <td>3738.32</td>
      <td>3744.09</td>
      <td>3740.25</td>
      <td>3741.59</td>
      <td>172.434</td>
      <td>3718.176</td>
      <td>3730.749</td>
    </tr>
    <tr>
      <th>2022-01-01 16:45:00</th>
      <td>3732.41</td>
      <td>3746.25</td>
      <td>3741.74</td>
      <td>3733.97</td>
      <td>420.403</td>
      <td>3718.362</td>
      <td>3731.056</td>
    </tr>
    <tr>
      <th>2022-01-01 16:50:00</th>
      <td>3730.57</td>
      <td>3738.97</td>
      <td>3733.92</td>
      <td>3731.71</td>
      <td>397.460</td>
      <td>3718.564</td>
      <td>3731.118</td>
    </tr>
    <tr>
      <th>2022-01-01 16:55:00</th>
      <td>3725.81</td>
      <td>3732.96</td>
      <td>3730.79</td>
      <td>3728.81</td>
      <td>532.698</td>
      <td>3718.772</td>
      <td>3730.898</td>
    </tr>
    <tr>
      <th>2022-01-01 17:00:00</th>
      <td>3728.81</td>
      <td>3736.47</td>
      <td>3728.81</td>
      <td>3734.38</td>
      <td>228.033</td>
      <td>3718.952</td>
      <td>3731.230</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2022-10-11 14:40:00</th>
      <td>1283.92</td>
      <td>1287.40</td>
      <td>1284.26</td>
      <td>1284.88</td>
      <td>2188.453</td>
      <td>1282.024</td>
      <td>1281.600</td>
    </tr>
    <tr>
      <th>2022-10-11 14:45:00</th>
      <td>1283.35</td>
      <td>1286.24</td>
      <td>1284.98</td>
      <td>1284.60</td>
      <td>2131.085</td>
      <td>1281.974</td>
      <td>1281.886</td>
    </tr>
    <tr>
      <th>2022-10-11 14:50:00</th>
      <td>1283.25</td>
      <td>1285.48</td>
      <td>1284.44</td>
      <td>1283.72</td>
      <td>1778.953</td>
      <td>1281.938</td>
      <td>1282.061</td>
    </tr>
    <tr>
      <th>2022-10-11 14:55:00</th>
      <td>1281.93</td>
      <td>1286.18</td>
      <td>1283.72</td>
      <td>1281.99</td>
      <td>1945.641</td>
      <td>1281.877</td>
      <td>1282.054</td>
    </tr>
    <tr>
      <th>2022-10-11 15:00:00</th>
      <td>1281.99</td>
      <td>1282.56</td>
      <td>1282.21</td>
      <td>1282.56</td>
      <td>64.151</td>
      <td>1281.808</td>
      <td>1282.102</td>
    </tr>
  </tbody>
</table>
<p>81484 rows × 7 columns</p>
</div>
```
:::
:::

::: {.cell .code execution_count="6"}
``` {.python}
def plot_system1(data):
    df = data.copy()
    dates = df.index
    price = df['close']
    sma200 = df['sma200']
    ema20 = df['ema20']
    
    with plt.style.context('fivethirtyeight'):
        fig = plt.figure(figsize=(14,7))
        plt.plot(dates, price, linewidth=1.5, label='ETH price - Daily Close')
        plt.plot(dates, sma200, linewidth=2, label='200 SMA')
        plt.plot(dates, ema20, linewidth=2, label='20 EMA')
        plt.title("ETH-USD, EMA, SMA")
        plt.ylabel('Price($)')
        plt.legend()
    
    plt.show() # This is needed only if not in Jupyter
```
:::

::: {.cell .code execution_count="7"}
``` {.python}
plot_system1(df)
```

::: {.output .display_data}
![](vertopal_479213917d514cc9aed9cac00e52806e/6bfc031c797d2bd63df735ce6e09578afff7b35c.png)
:::
:::

::: {.cell .code execution_count="8"}
``` {.python}
# Our trading condition:
long_positions = np.where(df['ema20'] > df['sma200'], 1, 0)
df['Position'] = long_positions
df.round(3)
```

::: {.output .execute_result execution_count="8"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>low</th>
      <th>high</th>
      <th>open</th>
      <th>close</th>
      <th>volume</th>
      <th>sma200</th>
      <th>ema20</th>
      <th>Position</th>
    </tr>
    <tr>
      <th>time</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2022-01-01 16:40:00</th>
      <td>3738.32</td>
      <td>3744.09</td>
      <td>3740.25</td>
      <td>3741.59</td>
      <td>172.434</td>
      <td>3718.176</td>
      <td>3730.749</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-01-01 16:45:00</th>
      <td>3732.41</td>
      <td>3746.25</td>
      <td>3741.74</td>
      <td>3733.97</td>
      <td>420.403</td>
      <td>3718.362</td>
      <td>3731.056</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-01-01 16:50:00</th>
      <td>3730.57</td>
      <td>3738.97</td>
      <td>3733.92</td>
      <td>3731.71</td>
      <td>397.460</td>
      <td>3718.564</td>
      <td>3731.118</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-01-01 16:55:00</th>
      <td>3725.81</td>
      <td>3732.96</td>
      <td>3730.79</td>
      <td>3728.81</td>
      <td>532.698</td>
      <td>3718.772</td>
      <td>3730.898</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-01-01 17:00:00</th>
      <td>3728.81</td>
      <td>3736.47</td>
      <td>3728.81</td>
      <td>3734.38</td>
      <td>228.033</td>
      <td>3718.952</td>
      <td>3731.230</td>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2022-10-11 14:40:00</th>
      <td>1283.92</td>
      <td>1287.40</td>
      <td>1284.26</td>
      <td>1284.88</td>
      <td>2188.453</td>
      <td>1282.024</td>
      <td>1281.600</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2022-10-11 14:45:00</th>
      <td>1283.35</td>
      <td>1286.24</td>
      <td>1284.98</td>
      <td>1284.60</td>
      <td>2131.085</td>
      <td>1281.974</td>
      <td>1281.886</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2022-10-11 14:50:00</th>
      <td>1283.25</td>
      <td>1285.48</td>
      <td>1284.44</td>
      <td>1283.72</td>
      <td>1778.953</td>
      <td>1281.938</td>
      <td>1282.061</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-10-11 14:55:00</th>
      <td>1281.93</td>
      <td>1286.18</td>
      <td>1283.72</td>
      <td>1281.99</td>
      <td>1945.641</td>
      <td>1281.877</td>
      <td>1282.054</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-10-11 15:00:00</th>
      <td>1281.99</td>
      <td>1282.56</td>
      <td>1282.21</td>
      <td>1282.56</td>
      <td>64.151</td>
      <td>1281.808</td>
      <td>1282.102</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>81484 rows × 8 columns</p>
</div>
```
:::
:::

::: {.cell .code execution_count="9"}
``` {.python}
buy_signals = (df['Position'] == 1) & (df['Position'].shift(1) == 0)
df.loc[buy_signals].round(3)
```

::: {.output .execute_result execution_count="9"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>low</th>
      <th>high</th>
      <th>open</th>
      <th>close</th>
      <th>volume</th>
      <th>sma200</th>
      <th>ema20</th>
      <th>Position</th>
    </tr>
    <tr>
      <th>time</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2022-01-02 09:50:00</th>
      <td>3752.94</td>
      <td>3760.55</td>
      <td>3756.58</td>
      <td>3753.34</td>
      <td>103.169</td>
      <td>3750.664</td>
      <td>3750.687</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-01-02 14:15:00</th>
      <td>3752.15</td>
      <td>3756.96</td>
      <td>3753.14</td>
      <td>3756.68</td>
      <td>139.460</td>
      <td>3749.455</td>
      <td>3749.575</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-01-02 14:35:00</th>
      <td>3747.51</td>
      <td>3757.05</td>
      <td>3751.09</td>
      <td>3755.18</td>
      <td>173.270</td>
      <td>3749.371</td>
      <td>3749.858</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-01-03 05:30:00</th>
      <td>3806.79</td>
      <td>3822.95</td>
      <td>3806.91</td>
      <td>3820.48</td>
      <td>593.472</td>
      <td>3798.256</td>
      <td>3798.415</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-01-03 08:05:00</th>
      <td>3811.11</td>
      <td>3818.14</td>
      <td>3814.73</td>
      <td>3811.56</td>
      <td>105.225</td>
      <td>3806.791</td>
      <td>3806.925</td>
      <td>1</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2022-10-09 10:00:00</th>
      <td>1316.46</td>
      <td>1317.91</td>
      <td>1317.45</td>
      <td>1316.46</td>
      <td>204.177</td>
      <td>1316.403</td>
      <td>1316.416</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-10-10 00:40:00</th>
      <td>1322.68</td>
      <td>1328.02</td>
      <td>1322.68</td>
      <td>1326.65</td>
      <td>1051.044</td>
      <td>1321.932</td>
      <td>1322.096</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-10-10 04:45:00</th>
      <td>1324.08</td>
      <td>1325.20</td>
      <td>1324.37</td>
      <td>1324.81</td>
      <td>425.603</td>
      <td>1323.829</td>
      <td>1323.867</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-10-11 12:25:00</th>
      <td>1289.76</td>
      <td>1292.70</td>
      <td>1289.87</td>
      <td>1292.10</td>
      <td>1280.261</td>
      <td>1285.323</td>
      <td>1286.031</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-10-11 14:50:00</th>
      <td>1283.25</td>
      <td>1285.48</td>
      <td>1284.44</td>
      <td>1283.72</td>
      <td>1778.953</td>
      <td>1281.938</td>
      <td>1282.061</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>383 rows × 8 columns</p>
</div>
```
:::
:::

::: {.cell .code execution_count="10"}
``` {.python}
buy_signals_prev = (df['Position'].shift(-1) == 1) & (df['Position'] == 0)
df.loc[buy_signals | buy_signals_prev].round(3)
```

::: {.output .execute_result execution_count="10"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>low</th>
      <th>high</th>
      <th>open</th>
      <th>close</th>
      <th>volume</th>
      <th>sma200</th>
      <th>ema20</th>
      <th>Position</th>
    </tr>
    <tr>
      <th>time</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2022-01-02 09:45:00</th>
      <td>3756.23</td>
      <td>3761.78</td>
      <td>3761.69</td>
      <td>3756.58</td>
      <td>118.031</td>
      <td>3750.547</td>
      <td>3750.407</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2022-01-02 09:50:00</th>
      <td>3752.94</td>
      <td>3760.55</td>
      <td>3756.58</td>
      <td>3753.34</td>
      <td>103.169</td>
      <td>3750.664</td>
      <td>3750.687</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-01-02 14:10:00</th>
      <td>3748.81</td>
      <td>3754.24</td>
      <td>3751.43</td>
      <td>3753.14</td>
      <td>259.738</td>
      <td>3749.496</td>
      <td>3748.827</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2022-01-02 14:15:00</th>
      <td>3752.15</td>
      <td>3756.96</td>
      <td>3753.14</td>
      <td>3756.68</td>
      <td>139.460</td>
      <td>3749.455</td>
      <td>3749.575</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-01-02 14:30:00</th>
      <td>3746.65</td>
      <td>3752.07</td>
      <td>3746.66</td>
      <td>3751.02</td>
      <td>117.841</td>
      <td>3749.343</td>
      <td>3749.298</td>
      <td>0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2022-10-10 04:45:00</th>
      <td>1324.08</td>
      <td>1325.20</td>
      <td>1324.37</td>
      <td>1324.81</td>
      <td>425.603</td>
      <td>1323.829</td>
      <td>1323.867</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-10-11 12:20:00</th>
      <td>1288.87</td>
      <td>1291.03</td>
      <td>1290.91</td>
      <td>1289.87</td>
      <td>1427.036</td>
      <td>1285.410</td>
      <td>1285.392</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2022-10-11 12:25:00</th>
      <td>1289.76</td>
      <td>1292.70</td>
      <td>1289.87</td>
      <td>1292.10</td>
      <td>1280.261</td>
      <td>1285.323</td>
      <td>1286.031</td>
      <td>1</td>
    </tr>
    <tr>
      <th>2022-10-11 14:45:00</th>
      <td>1283.35</td>
      <td>1286.24</td>
      <td>1284.98</td>
      <td>1284.60</td>
      <td>2131.085</td>
      <td>1281.974</td>
      <td>1281.886</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2022-10-11 14:50:00</th>
      <td>1283.25</td>
      <td>1285.48</td>
      <td>1284.44</td>
      <td>1283.72</td>
      <td>1778.953</td>
      <td>1281.938</td>
      <td>1282.061</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
<p>766 rows × 8 columns</p>
</div>
```
:::
:::

::: {.cell .code execution_count="11"}
``` {.python}
def plot_system1_sig(data):
    df = data.copy()
    dates = df.index
    price = df['close']
    sma200 = df['sma200']
    ema20 = df['ema20']
    
    buy_signals = (df['Position'] == 1) & (df['Position'].shift(1) == 0)
    buy_marker = sma200 * buy_signals - (sma200.max()*.05)
    buy_marker = buy_marker[buy_signals]
    buy_dates = df.index[buy_signals]
    sell_signals = (df['Position'] == 0) & (df['Position'].shift(1) == 1)
    sell_marker = sma200 * sell_signals + (sma200.max()*.05)
    sell_marker = sell_marker[sell_signals]
    sell_dates = df.index[sell_signals]
    
    with plt.style.context('fivethirtyeight'):
        fig = plt.figure(figsize=(14,7))
        plt.plot(dates, price, linewidth=1.5, label='CPB price - Daily Adj Close')
        plt.plot(dates, sma200, linewidth=2, label='200 SMA')
        plt.plot(dates, ema20, linewidth=2, label='20 EMA')
        plt.scatter(buy_dates, buy_marker, marker='^', color='green', s=160, label='Buy')
        plt.scatter(sell_dates, sell_marker, marker='v', color='red', s=160, label='Sell')
        plt.title("A Simple Crossover System with Signals")
        plt.ylabel('Price($)')
        plt.legend()
    
    plt.show() # This is needed only if not in Jupyter
```
:::

::: {.cell .code execution_count="12"}
``` {.python}
plot_system1_sig(df['2022-8-15':'2022-10-11'])
```

::: {.output .display_data}
![](vertopal_479213917d514cc9aed9cac00e52806e/d8b0e92ed10348159cfb06dd6169e7ccd40cbebb.png)
:::
:::

::: {.cell .code execution_count="13"}
``` {.python}
# The returns of the Buy and Hold strategy:
df['Hold'] = np.log(df['close'] / df['close'].shift(1))
# The returns of the Moving Average strategy:
df['Strategy'] = df['Position'].shift(1) * df['Hold']
# We need to get rid of the NaN generated in the first row:
df.dropna(inplace=True)
df
```

::: {.output .execute_result execution_count="13"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>low</th>
      <th>high</th>
      <th>open</th>
      <th>close</th>
      <th>volume</th>
      <th>sma200</th>
      <th>ema20</th>
      <th>Position</th>
      <th>Hold</th>
      <th>Strategy</th>
    </tr>
    <tr>
      <th>time</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2022-01-01 16:45:00</th>
      <td>3732.41</td>
      <td>3746.25</td>
      <td>3741.74</td>
      <td>3733.97</td>
      <td>420.403322</td>
      <td>3718.36210</td>
      <td>3731.055634</td>
      <td>1</td>
      <td>-0.002039</td>
      <td>-0.002039</td>
    </tr>
    <tr>
      <th>2022-01-01 16:50:00</th>
      <td>3730.57</td>
      <td>3738.97</td>
      <td>3733.92</td>
      <td>3731.71</td>
      <td>397.459772</td>
      <td>3718.56420</td>
      <td>3731.117955</td>
      <td>1</td>
      <td>-0.000605</td>
      <td>-0.000605</td>
    </tr>
    <tr>
      <th>2022-01-01 16:55:00</th>
      <td>3725.81</td>
      <td>3732.96</td>
      <td>3730.79</td>
      <td>3728.81</td>
      <td>532.697871</td>
      <td>3718.77190</td>
      <td>3730.898150</td>
      <td>1</td>
      <td>-0.000777</td>
      <td>-0.000777</td>
    </tr>
    <tr>
      <th>2022-01-01 17:00:00</th>
      <td>3728.81</td>
      <td>3736.47</td>
      <td>3728.81</td>
      <td>3734.38</td>
      <td>228.033022</td>
      <td>3718.95205</td>
      <td>3731.229754</td>
      <td>1</td>
      <td>0.001493</td>
      <td>0.001493</td>
    </tr>
    <tr>
      <th>2022-01-01 17:05:00</th>
      <td>3730.00</td>
      <td>3737.29</td>
      <td>3734.25</td>
      <td>3732.68</td>
      <td>206.905942</td>
      <td>3719.13165</td>
      <td>3731.367873</td>
      <td>1</td>
      <td>-0.000455</td>
      <td>-0.000455</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2022-10-11 14:40:00</th>
      <td>1283.92</td>
      <td>1287.40</td>
      <td>1284.26</td>
      <td>1284.88</td>
      <td>2188.453125</td>
      <td>1282.02425</td>
      <td>1281.600153</td>
      <td>0</td>
      <td>0.000576</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2022-10-11 14:45:00</th>
      <td>1283.35</td>
      <td>1286.24</td>
      <td>1284.98</td>
      <td>1284.60</td>
      <td>2131.085450</td>
      <td>1281.97450</td>
      <td>1281.885853</td>
      <td>0</td>
      <td>-0.000218</td>
      <td>-0.000000</td>
    </tr>
    <tr>
      <th>2022-10-11 14:50:00</th>
      <td>1283.25</td>
      <td>1285.48</td>
      <td>1284.44</td>
      <td>1283.72</td>
      <td>1778.952546</td>
      <td>1281.93795</td>
      <td>1282.060533</td>
      <td>1</td>
      <td>-0.000685</td>
      <td>-0.000000</td>
    </tr>
    <tr>
      <th>2022-10-11 14:55:00</th>
      <td>1281.93</td>
      <td>1286.18</td>
      <td>1283.72</td>
      <td>1281.99</td>
      <td>1945.641490</td>
      <td>1281.87670</td>
      <td>1282.053816</td>
      <td>1</td>
      <td>-0.001349</td>
      <td>-0.001349</td>
    </tr>
    <tr>
      <th>2022-10-11 15:00:00</th>
      <td>1281.99</td>
      <td>1282.56</td>
      <td>1282.21</td>
      <td>1282.56</td>
      <td>64.150849</td>
      <td>1281.80800</td>
      <td>1282.102024</td>
      <td>1</td>
      <td>0.000445</td>
      <td>0.000445</td>
    </tr>
  </tbody>
</table>
<p>81483 rows × 10 columns</p>
</div>
```
:::
:::

::: {.cell .code execution_count="14"}
``` {.python}
returns = np.exp(df[['Hold', 'Strategy']].sum()) - 1
print(f"Buy and hold return: {round(returns['Hold']*100,2)}%")
print(f"Strategy return: {round(returns['Strategy']*100,2)}%")
```

::: {.output .stream .stdout}
    Buy and hold return: -65.72%
    Strategy return: -11.55%
:::
:::

::: {.cell .code execution_count="15"}
``` {.python}
n_days = len(df)
# Assuming 252 trading days in a year:
ann_returns = 252 / n_days * returns
print(f"Buy and hold annualized return: {round(ann_returns['Hold']*100,2)}%")
print(f"Strategy annualized return:{round(ann_returns['Strategy']*100,2)}%")
```

::: {.output .stream .stdout}
    Buy and hold annualized return: -0.2%
    Strategy annualized return:-0.04%
:::
:::

::: {.cell .markdown}

------------------------------------------------------------------------
:::

::: {.cell .markdown}
Binance API
:::

::: {.cell .code execution_count="198"}
``` {.python}
from binance import Client, ThreadedWebsocketManager, ThreadedDepthCacheManager
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
pd.plotting.register_matplotlib_converters()

import config
client = Client(config.apiKey, config.apiSecurity)

print('Logged in')

# info = client.get_recent_trades(symbol='BNBBTC')


```

::: {.output .stream .stdout}
    Logged in
:::
:::

::: {.cell .code execution_count="17"}
``` {.python}
import datetime 
tod = datetime.datetime.now()
d = datetime.timedelta(days = 100)
a = tod - d
print(a.strftime("%Y%m%d"))
print(a.strftime("%d %b %Y"))
```

::: {.output .stream .stdout}
    20220929
    29 Sep 2022
:::
:::

::: {.cell .code execution_count="18"}
``` {.python}
def plot_systemETH(data, title):
    df = data.copy()
    dates = df.index
    price = df['Close']
    sma200 = df['sma200']
    ema20 = df['ema20']
    
    with plt.style.context('fivethirtyeight'):
        fig = plt.figure(figsize=(14,7))
        plt.plot(dates, price, linewidth=1.5, label='ETH price')
        plt.plot(dates, sma200, linewidth=2, label='200 SMA')
        plt.plot(dates, ema20, linewidth=2, label='20 EMA')
        plt.title(title)
        plt.ylabel('Price($)')
        plt.legend()
    
    plt.show() # This is needed only if not in Jupyter

```
:::

::: {.cell .code execution_count="19"}
``` {.python}
def plot_system1_sig(data, title):
    df = data.copy()
    dates = df.index
    price = df['Close']
    sma200 = df['sma200']
    ema20 = df['ema20']
    
    buy_signals = (df['Position'] == 1) & (df['Position'].shift(1) == 0)
    buy_marker = sma200 * buy_signals - (sma200.max()*.05)
    buy_marker = buy_marker[buy_signals]
    buy_dates = df.index[buy_signals]
    sell_signals = (df['Position'] == 0) & (df['Position'].shift(1) == 1)
    sell_marker = sma200 * sell_signals + (sma200.max()*.05)
    sell_marker = sell_marker[sell_signals]
    sell_dates = df.index[sell_signals]
    
    with plt.style.context('fivethirtyeight'):
        fig = plt.figure(figsize=(14,7))
        plt.plot(dates, price, linewidth=1.5, label='ETH price - Daily Adj Close')
        plt.plot(dates, sma200, linewidth=2, label='200 SMA')
        plt.plot(dates, ema20, linewidth=2, label='20 EMA')
        plt.scatter(buy_dates, buy_marker, marker='^', color='green', s=160, label='Buy')
        plt.scatter(sell_dates, sell_marker, marker='v', color='red', s=160, label='Sell')
        plt.title(title)
        plt.ylabel('Price($)')
        plt.legend()
    
    plt.show() # This is needed only if not in Jupyter
```
:::

::: {.cell .code execution_count="259"}
``` {.python}
candles = client.get_historical_klines('ETHUSDT', Client.KLINE_INTERVAL_5MINUTE, a.strftime("%d %b %Y"))
candles_df = pd.DataFrame(candles)
candles_df.columns = ['Open Time','Open', 'High', 'Low', 'Close', 'Volume', 'Close Time', 'Quote Asset Volume', 'Number of Trades', 'TB Base Volume', 'TB Quote Volume', 'Ignore']

candles_df.index = pd.to_datetime(candles_df['Open Time'], unit='ms')

numeric_column = ['Open', 'High', 'Low', 'Close', 'Volume']
candles_df[numeric_column] = candles_df[numeric_column].apply(pd.to_numeric, axis=1)

sma_span = 200
ema_span = 20
candles_df['sma200'] = candles_df['Close'].rolling(sma_span).mean()
candles_df['ema20'] = candles_df['Close'].ewm(span=ema_span).mean()
candles_df.round(3)
candles_df.dropna(inplace=True)
candles_df.round(3)
candles_df = candles_df.drop(['Open Time', 'Close Time', 'Quote Asset Volume', 'TB Base Volume', 'TB Quote Volume', 'Ignore', 'Number of Trades'], axis=1)

# plot_systemETH(candles_df, 'ETH-USDT (5 minute timeframe)')

# Our trading condition:
long_positions = np.where(candles_df['ema20'] > candles_df['sma200'], 1, 0)
candles_df['Position'] = long_positions
candles_df.round(3)

buy_signals = (candles_df['Position'] == 1) & (candles_df['Position'].shift(1) == 0)
candles_df.loc[buy_signals].round(3)

buy_signals_prev = (candles_df['Position'].shift(-1) == 1) & (candles_df['Position'] == 0)
candles_df.loc[buy_signals | buy_signals_prev].round(3)

plot_system1_sig(candles_df, 'ETH-USDT (5 minute timeframe)')
```

::: {.output .display_data}
![](vertopal_479213917d514cc9aed9cac00e52806e/c7d692c2be0c980b51723400d9a634526d62da0c.png)
:::
:::

::: {.cell .code execution_count="244"}
``` {.python}
candles = client.get_historical_klines('ETHUSDT', Client.KLINE_INTERVAL_30MINUTE, a.strftime("%d %b %Y"))
candles_df = pd.DataFrame(candles)
candles_df.columns = ['Open Time','Open', 'High', 'Low', 'Close', 'Volume', 'Close Time', 'Quote Asset Volume', 'Number of Trades', 'TB Base Volume', 'TB Quote Volume', 'Ignore']

candles_df.index = pd.to_datetime(candles_df['Open Time'], unit='ms')

numeric_column = ['Open', 'High', 'Low', 'Close', 'Volume']
candles_df[numeric_column] = candles_df[numeric_column].apply(pd.to_numeric, axis=1)

sma_span = 200
ema_span = 20
candles_df['sma200'] = candles_df['Close'].rolling(sma_span).mean()
candles_df['ema20'] = candles_df['Close'].ewm(span=ema_span).mean()
candles_df.round(3)
candles_df.dropna(inplace=True)
candles_df.round(3)
candles_df = candles_df.drop(['Open Time', 'Close Time', 'Quote Asset Volume', 'TB Base Volume', 'TB Quote Volume', 'Ignore', 'Number of Trades'], axis=1)

# plot_systemETH(candles_df, 'ETH-USDT (30 minute timeframe)')

# Our trading condition:
long_positions = np.where(candles_df['ema20'] > candles_df['sma200'], 1, 0)
candles_df['Position'] = long_positions
candles_df.round(3)

buy_signals = (candles_df['Position'] == 1) & (candles_df['Position'].shift(1) == 0)
candles_df.loc[buy_signals].round(3)

buy_signals_prev = (candles_df['Position'].shift(-1) == 1) & (candles_df['Position'] == 0)
candles_df.loc[buy_signals | buy_signals_prev].round(3)

plot_system1_sig(candles_df, 'ETH-USDT (30 minute timeframe)')
```

::: {.output .display_data}
![](vertopal_479213917d514cc9aed9cac00e52806e/669ce7be11ed2dd438acabed4290897b18eb2a08.png)
:::
:::

::: {.cell .code}
``` {.python}
candles = client.get_historical_klines('ETHUSDT', Client.KLINE_INTERVAL_1HOUR, a.strftime("%d %b %Y"))
candles_df = pd.DataFrame(candles)
candles_df.columns = ['Open Time','Open', 'High', 'Low', 'Close', 'Volume', 'Close Time', 'Quote Asset Volume', 'Number of Trades', 'TB Base Volume', 'TB Quote Volume', 'Ignore']

candles_df.index = pd.to_datetime(candles_df['Open Time'], unit='ms')

numeric_column = ['Open', 'High', 'Low', 'Close', 'Volume']
candles_df[numeric_column] = candles_df[numeric_column].apply(pd.to_numeric, axis=1)

sma_span = 200
ema_span = 20
candles_df['sma200'] = candles_df['Close'].rolling(sma_span).mean()
candles_df['ema20'] = candles_df['Close'].ewm(span=ema_span).mean()
candles_df.round(3)
candles_df.dropna(inplace=True)
candles_df.round(3)
candles_df = candles_df.drop(['Open Time', 'Close Time', 'Quote Asset Volume', 'TB Base Volume', 'TB Quote Volume', 'Ignore', 'Number of Trades'], axis=1)

# plot_systemETH(candles_df, 'ETH-USDT (1 hour timeframe)')

# Our trading condition:
long_positions = np.where(candles_df['ema20'] > candles_df['sma200'], 1, 0)
candles_df['Position'] = long_positions
candles_df.round(3)

buy_signals = (candles_df['Position'] == 1) & (candles_df['Position'].shift(1) == 0)
candles_df.loc[buy_signals].round(3)

buy_signals_prev = (candles_df['Position'].shift(-1) == 1) & (candles_df['Position'] == 0)
candles_df.loc[buy_signals | buy_signals_prev].round(3)

plot_system1_sig(candles_df, 'ETH-USDT (1 hour timeframe)')
```

::: {.output .display_data}
![](vertopal_479213917d514cc9aed9cac00e52806e/aedb8af69ca61cdbda49698339f56957725c37bd.png)
:::
:::

::: {.cell .code}
``` {.python}
candles = client.get_historical_klines('ETHUSDT', Client.KLINE_INTERVAL_2HOUR, a.strftime("%d %b %Y"))
candles_df = pd.DataFrame(candles)
candles_df.columns = ['Open Time','Open', 'High', 'Low', 'Close', 'Volume', 'Close Time', 'Quote Asset Volume', 'Number of Trades', 'TB Base Volume', 'TB Quote Volume', 'Ignore']

candles_df.index = pd.to_datetime(candles_df['Open Time'], unit='ms')

numeric_column = ['Open', 'High', 'Low', 'Close', 'Volume']
candles_df[numeric_column] = candles_df[numeric_column].apply(pd.to_numeric, axis=1)

sma_span = 200
ema_span = 20
candles_df['sma200'] = candles_df['Close'].rolling(sma_span).mean()
candles_df['ema20'] = candles_df['Close'].ewm(span=ema_span).mean()
candles_df.round(3)
candles_df.dropna(inplace=True)
candles_df.round(3)
candles_df = candles_df.drop(['Open Time', 'Close Time', 'Quote Asset Volume', 'TB Base Volume', 'TB Quote Volume', 'Ignore', 'Number of Trades'], axis=1)

# plot_systemETH(candles_df, 'ETH-USDT (2 hour timeframe)')

# Our trading condition:
long_positions = np.where(candles_df['ema20'] > candles_df['sma200'], 1, 0)
candles_df['Position'] = long_positions
candles_df.round(3)

buy_signals = (candles_df['Position'] == 1) & (candles_df['Position'].shift(1) == 0)
candles_df.loc[buy_signals].round(3)

buy_signals_prev = (candles_df['Position'].shift(-1) == 1) & (candles_df['Position'] == 0)
candles_df.loc[buy_signals | buy_signals_prev].round(3)

plot_system1_sig(candles_df, 'ETH-USDT (2 hour timeframe)')
```

::: {.output .display_data}
![](vertopal_479213917d514cc9aed9cac00e52806e/e1c5677dd1118298827eceecb8f466a5a823be66.png)
:::
:::

::: {.cell .code execution_count="24"}
``` {.python}
candles = client.get_historical_klines('ETHUSDT', Client.KLINE_INTERVAL_12HOUR, a.strftime("%d %b %Y"))
candles_df = pd.DataFrame(candles)
candles_df.columns = ['Open Time','Open', 'High', 'Low', 'Close', 'Volume', 'Close Time', 'QUote Asset Volume', 'Number of Trades', 'TB Base Volume', 'TB Quote Volume', 'Ignore']
candles_df_copy = candles_df.copy()
candles_df_copy.index = pd.to_datetime(candles_df_copy['Open Time'], unit='ms')

numeric_column = ['Open', 'High', 'Low', 'Close', 'Volume']
candles_df_copy[numeric_column] = candles_df_copy[numeric_column].apply(pd.to_numeric, axis=1)

sma_span = 200
ema_span = 20
candles_df_copy['sma200'] = candles_df_copy['Close'].rolling(sma_span).mean()
candles_df_copy['ema20'] = candles_df_copy['Close'].ewm(span=ema_span).mean()
# candles_df_copy.round(3)
# candles_df_copy.dropna(inplace=True)
candles_df_copy.round(3)
candles_df_copy = candles_df_copy.drop(['Open Time', 'Close Time', 'QUote Asset Volume', 'TB Base Volume', 'TB Quote Volume', 'Ignore', 'Number of Trades'], axis=1)

candles_df_copy
# plot_systemETH(candles_df_copy)
```

::: {.output .execute_result execution_count="24"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Open</th>
      <th>High</th>
      <th>Low</th>
      <th>Close</th>
      <th>Volume</th>
      <th>sma200</th>
      <th>ema20</th>
    </tr>
    <tr>
      <th>Open Time</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2022-09-29 00:00:00</th>
      <td>1337.20</td>
      <td>1352.02</td>
      <td>1313.55</td>
      <td>1336.56</td>
      <td>325248.1636</td>
      <td>NaN</td>
      <td>1336.560000</td>
    </tr>
    <tr>
      <th>2022-09-29 12:00:00</th>
      <td>1336.57</td>
      <td>1348.25</td>
      <td>1288.52</td>
      <td>1335.70</td>
      <td>445343.5259</td>
      <td>NaN</td>
      <td>1336.108500</td>
    </tr>
    <tr>
      <th>2022-09-30 00:00:00</th>
      <td>1335.69</td>
      <td>1352.30</td>
      <td>1320.12</td>
      <td>1330.80</td>
      <td>267665.6467</td>
      <td>NaN</td>
      <td>1334.159251</td>
    </tr>
    <tr>
      <th>2022-09-30 12:00:00</th>
      <td>1330.79</td>
      <td>1373.19</td>
      <td>1313.35</td>
      <td>1328.72</td>
      <td>473087.9643</td>
      <td>NaN</td>
      <td>1332.589023</td>
    </tr>
    <tr>
      <th>2022-10-01 00:00:00</th>
      <td>1328.71</td>
      <td>1333.69</td>
      <td>1317.24</td>
      <td>1325.42</td>
      <td>110889.3418</td>
      <td>NaN</td>
      <td>1330.854897</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2023-01-05 00:00:00</th>
      <td>1256.91</td>
      <td>1259.95</td>
      <td>1245.30</td>
      <td>1255.91</td>
      <td>135184.8079</td>
      <td>NaN</td>
      <td>1220.634457</td>
    </tr>
    <tr>
      <th>2023-01-05 12:00:00</th>
      <td>1255.90</td>
      <td>1256.01</td>
      <td>1242.81</td>
      <td>1251.24</td>
      <td>137620.5221</td>
      <td>NaN</td>
      <td>1223.549271</td>
    </tr>
    <tr>
      <th>2023-01-06 00:00:00</th>
      <td>1251.25</td>
      <td>1257.98</td>
      <td>1237.98</td>
      <td>1243.40</td>
      <td>115681.4428</td>
      <td>NaN</td>
      <td>1225.439817</td>
    </tr>
    <tr>
      <th>2023-01-06 12:00:00</th>
      <td>1243.40</td>
      <td>1276.70</td>
      <td>1236.00</td>
      <td>1269.14</td>
      <td>226662.7595</td>
      <td>1298.00840</td>
      <td>1229.601739</td>
    </tr>
    <tr>
      <th>2023-01-07 00:00:00</th>
      <td>1269.13</td>
      <td>1271.09</td>
      <td>1262.24</td>
      <td>1265.31</td>
      <td>37776.2767</td>
      <td>1297.65215</td>
      <td>1233.002526</td>
    </tr>
  </tbody>
</table>
<p>201 rows × 7 columns</p>
</div>
```
:::
:::

::: {.cell .markdown}
:::

::: {.cell .code execution_count="258"}
``` {.python}
def plot_system1_sig(data, title):
    df = data.copy()
    dates = df.index
    price = df['Close']
    sma200 = df['sma200']
    ema20 = df['ema20']
    
    buy_signals = (df['Position'] == 1) & (df['Position'].shift(1) == 0)
    buy_marker = sma200 * buy_signals - (sma200.max()*.05)
    buy_marker = buy_marker[buy_signals]
    buy_dates = df.index[buy_signals]
    sell_signals = (df['Position'] == 0) & (df['Position'].shift(1) == 1)
    sell_marker = sma200 * sell_signals + (sma200.max()*.05)
    sell_marker = sell_marker[sell_signals]
    sell_dates = df.index[sell_signals]
    
    df['OpenTime'] = df.index
    df.loc[(df['Position'] == 1) & (df['Position'].shift(1) == 0), 'ep'] = df['Open']
    df.loc[(df['Position'] == 1) & (df['Position'].shift(1) == 0), 'date_time'] = df['OpenTime']
    df = df.fillna(method='ffill')


    df.loc[sell_signals, 'tp'] = df['Open'] - 10.00
    df.loc[sell_signals, 'sl'] = df['Open'] + 10.00
    df.loc[buy_signals, 'tp'] = df['Open'] + 10.00
    df.loc[buy_signals, 'sl'] = df['Open'] - 10.00
    df = df.fillna(method='ffill')

    df['outcome'] = ' '
    df.loc[(df['Position'] == 1) & (df['Close'] > df['tp']), 'outcome'] = 'WIN'
    df.loc[(df['Position'] == 1) & (df['Close'] < df['sl']), 'outcome'] = 'LOSS'
    df.loc[(df['Position'] == 0) & (df['Close'] < df['tp']), 'outcome'] = 'WIN'
    df.loc[(df['Position'] == 0) & (df['Close'] > df['sl']), 'outcome'] = 'LOSS'

    df.rename(columns= {'ot': 'Open Time'}, inplace=True)

    df2=df.reset_index()
    df2['ts'] = df2['Open Time'].astype('int64') // 10**9
    df2['outcome'] = df2['outcome'].replace(' ', np.nan)
    df2 = df2.dropna(subset=['outcome'])

    df3 = df2.groupby(['tp', 'outcome'], as_index=False)
    df3 = df3.first()
    df3['Open Time'] = pd.to_datetime(df3['ts'], unit='s')
    df3.set_index("Open Time", inplace = True)
    df3 = df2.groupby(['tp'], as_index=False)
    df3 = df3.first()
    df3.set_index("Open Time", inplace = True)
    df3 = df3.sort_index()

    df4 = df3.set_index('date_time')
    df4 = df4.drop(['Open', 'High', 'Low', 'Close', 'Volume', 'sma200', 'ema20', 'OpenTime', 'ts'], axis=1)
    df4 = df4[['Position', 'ep', 'tp', 'sl', 'outcome']]
    df4.loc[df4['Position'] == 1, ['Position']] = 'Long'
    df4.loc[df4['Position'] == 0, ['Position']] = 'Short'


    df4.to_csv(title + datetime.datetime.now().strftime("%Y%m%d") + '.csv', sep=',')

    with plt.style.context('fivethirtyeight'):
        fig = plt.figure(figsize=(14,7))
        plt.plot(dates, price, linewidth=1.5, label='ETH price - Daily Adj Close')
        plt.plot(dates, sma200, linewidth=2, label='200 SMA')
        plt.plot(dates, ema20, linewidth=2, label='20 EMA')
        plt.scatter(buy_dates, buy_marker, marker='^', color='green', s=160, label='Buy')
        plt.scatter(sell_dates, sell_marker, marker='v', color='red', s=160, label='Sell')
        plt.scatter(df3.index, df3['tp'], marker='*', color="black", s=160)
        plt.title(title)
        plt.ylabel('Price($)')
        plt.legend()
    
    plt.show() # This is needed only if not in Jupyter
```
:::

::: {.cell .markdown}
2 hour timeframe is chose.
:::

::: {.cell .code execution_count="253"}
``` {.python}
hourlycandles = client.get_historical_klines('ETHUSDT', Client.KLINE_INTERVAL_15MINUTE, a.strftime("%d %b %Y"))
hourlycandles_df = pd.DataFrame(hourlycandles)
hourlycandles_df.columns = ['Open Time','Open', 'High', 'Low', 'Close', 'Volume', 'Close Time', 'Quote Asset Volume', 'Number of Trades', 'TB Base Volume', 'TB Quote Volume', 'Ignore']

hourlycandles_df.index = pd.to_datetime(hourlycandles_df['Open Time'], unit='ms')

numeric_column = ['Open', 'High', 'Low', 'Close', 'Volume']
hourlycandles_df[numeric_column] = hourlycandles_df[numeric_column].apply(pd.to_numeric, axis=1)

sma_span = 200
ema_span = 20
hourlycandles_df['sma200'] = hourlycandles_df['Close'].rolling(sma_span).mean()
hourlycandles_df['ema20'] = hourlycandles_df['Close'].ewm(span=ema_span).mean()
hourlycandles_df.round(3)
hourlycandles_df.dropna(inplace=True)
hourlycandles_df.round(3)
hourlycandles_df = hourlycandles_df.drop(['Open Time', 'Close Time', 'Quote Asset Volume', 'TB Base Volume', 'TB Quote Volume', 'Ignore', 'Number of Trades'], axis=1)

plot_systemETH(hourlycandles_df, 'ETH-USDT (2 hour timeframe)')
```

::: {.output .display_data}
![](vertopal_479213917d514cc9aed9cac00e52806e/2361209184310b77bcd79d4fe074a098500b46c1.png)
:::
:::

::: {.cell .code execution_count="216"}
``` {.python}
hourlycandles_df
```

::: {.output .execute_result execution_count="216"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Open</th>
      <th>High</th>
      <th>Low</th>
      <th>Close</th>
      <th>Volume</th>
      <th>sma200</th>
      <th>ema20</th>
    </tr>
    <tr>
      <th>Open Time</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2022-10-01 01:45:00</th>
      <td>1329.35</td>
      <td>1332.42</td>
      <td>1328.73</td>
      <td>1331.49</td>
      <td>1741.5333</td>
      <td>1334.12455</td>
      <td>1330.127831</td>
    </tr>
    <tr>
      <th>2022-10-01 02:00:00</th>
      <td>1331.48</td>
      <td>1332.05</td>
      <td>1330.00</td>
      <td>1330.00</td>
      <td>1445.9259</td>
      <td>1334.08450</td>
      <td>1330.115657</td>
    </tr>
    <tr>
      <th>2022-10-01 02:15:00</th>
      <td>1330.00</td>
      <td>1331.87</td>
      <td>1329.39</td>
      <td>1330.86</td>
      <td>2047.4808</td>
      <td>1334.03470</td>
      <td>1330.186547</td>
    </tr>
    <tr>
      <th>2022-10-01 02:30:00</th>
      <td>1330.85</td>
      <td>1332.49</td>
      <td>1329.70</td>
      <td>1329.74</td>
      <td>2911.4267</td>
      <td>1333.99795</td>
      <td>1330.144018</td>
    </tr>
    <tr>
      <th>2022-10-01 02:45:00</th>
      <td>1329.73</td>
      <td>1331.89</td>
      <td>1329.30</td>
      <td>1330.16</td>
      <td>2689.4357</td>
      <td>1333.97770</td>
      <td>1330.145540</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>2023-01-08 05:30:00</th>
      <td>1262.74</td>
      <td>1262.99</td>
      <td>1262.47</td>
      <td>1262.98</td>
      <td>377.4708</td>
      <td>1260.68875</td>
      <td>1262.279700</td>
    </tr>
    <tr>
      <th>2023-01-08 05:45:00</th>
      <td>1262.98</td>
      <td>1263.71</td>
      <td>1262.98</td>
      <td>1263.70</td>
      <td>492.4481</td>
      <td>1260.75215</td>
      <td>1262.414966</td>
    </tr>
    <tr>
      <th>2023-01-08 06:00:00</th>
      <td>1263.70</td>
      <td>1263.77</td>
      <td>1262.70</td>
      <td>1263.20</td>
      <td>769.2098</td>
      <td>1260.81170</td>
      <td>1262.489731</td>
    </tr>
    <tr>
      <th>2023-01-08 06:15:00</th>
      <td>1263.21</td>
      <td>1263.44</td>
      <td>1262.80</td>
      <td>1263.05</td>
      <td>794.5682</td>
      <td>1260.87885</td>
      <td>1262.543090</td>
    </tr>
    <tr>
      <th>2023-01-08 06:30:00</th>
      <td>1263.05</td>
      <td>1263.57</td>
      <td>1262.90</td>
      <td>1263.56</td>
      <td>780.0611</td>
      <td>1260.94515</td>
      <td>1262.639939</td>
    </tr>
  </tbody>
</table>
<p>9524 rows × 7 columns</p>
</div>
```
:::
:::

::: {.cell .code execution_count="182"}
``` {.python}
long_positions = np.where(hourlycandles_df['ema20'] > hourlycandles_df['sma200'], 1, 0)
hourlycandles_df['Position'] = long_positions
hourlycandles_df.round(3)

hourlycandles_df['ot'] = hourlycandles_df.index


hourlycandles_df.loc[(hourlycandles_df['Position'] == 1) & (hourlycandles_df['Position'].shift(1) == 0), 'ep'] = hourlycandles_df['Open']
hourlycandles_df.loc[(hourlycandles_df['Position'] == 1) & (hourlycandles_df['Position'].shift(1) == 0), 'ep_time'] = hourlycandles_df['ot']
hourlycandles_df = hourlycandles_df.fillna(method='ffill')

# hourlycandles_df.to_csv('eth_test.csv', sep=',')


# buy_signals = (hourlycandles_df['Position'] == 1) & (hourlycandles_df['Position'].shift(1) == 0)
# hourlycandles_df['tp'] = hourlycandles_df.loc[buy_signals]['Open'] + 10.00
# hourlycandles_df['sl'] = hourlycandles_df.loc[buy_signals]['Open'] - 10.00
hourlycandles_df.loc[buy_signals].round(3)
```

::: {.output .execute_result execution_count="182"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Open</th>
      <th>High</th>
      <th>Low</th>
      <th>Close</th>
      <th>Volume</th>
      <th>sma200</th>
      <th>ema20</th>
      <th>Position</th>
      <th>ot</th>
      <th>ep</th>
      <th>ep_time</th>
    </tr>
    <tr>
      <th>Open Time</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2022-11-27 18:00:00</th>
      <td>1215.65</td>
      <td>1218.54</td>
      <td>1211.11</td>
      <td>1213.19</td>
      <td>16270.967</td>
      <td>1206.753</td>
      <td>1211.725</td>
      <td>1</td>
      <td>2022-11-27 18:00:00</td>
      <td>1216.87</td>
      <td>2022-11-27 06:00:00</td>
    </tr>
    <tr>
      <th>2022-12-19 10:00:00</th>
      <td>1184.30</td>
      <td>1188.38</td>
      <td>1182.29</td>
      <td>1183.28</td>
      <td>16080.020</td>
      <td>1255.187</td>
      <td>1184.375</td>
      <td>0</td>
      <td>2022-12-19 10:00:00</td>
      <td>1209.04</td>
      <td>2022-11-29 18:00:00</td>
    </tr>
    <tr>
      <th>2022-12-22 08:00:00</th>
      <td>1213.86</td>
      <td>1221.63</td>
      <td>1212.11</td>
      <td>1218.68</td>
      <td>28430.008</td>
      <td>1243.142</td>
      <td>1211.468</td>
      <td>0</td>
      <td>2022-12-22 08:00:00</td>
      <td>1209.04</td>
      <td>2022-11-29 18:00:00</td>
    </tr>
    <tr>
      <th>2023-01-04 22:00:00</th>
      <td>1252.66</td>
      <td>1257.70</td>
      <td>1252.25</td>
      <td>1256.90</td>
      <td>13289.368</td>
      <td>1210.071</td>
      <td>1240.498</td>
      <td>1</td>
      <td>2023-01-04 22:00:00</td>
      <td>1217.18</td>
      <td>2023-01-02 10:00:00</td>
    </tr>
  </tbody>
</table>
</div>
```
:::
:::

::: {.cell .code execution_count="280"}
``` {.python}
hourlycandles = client.get_historical_klines('ETHUSDT', Client.KLINE_INTERVAL_1HOUR, a.strftime("%d %b %Y"))
hourlycandles_df = pd.DataFrame(hourlycandles)
hourlycandles_df.columns = ['Open Time','Open', 'High', 'Low', 'Close', 'Volume', 'Close Time', 'Quote Asset Volume', 'Number of Trades', 'TB Base Volume', 'TB Quote Volume', 'Ignore']

hourlycandles_df.index = pd.to_datetime(hourlycandles_df['Open Time'], unit='ms')

numeric_column = ['Open', 'High', 'Low', 'Close', 'Volume']
hourlycandles_df[numeric_column] = hourlycandles_df[numeric_column].apply(pd.to_numeric, axis=1)

sma_span = 200
ema_span = 20
hourlycandles_df['sma200'] = hourlycandles_df['Close'].rolling(sma_span).mean()
hourlycandles_df['ema20'] = hourlycandles_df['Close'].ewm(span=ema_span).mean()
hourlycandles_df.round(3)
hourlycandles_df.dropna(inplace=True)
hourlycandles_df.round(3)
hourlycandles_df = hourlycandles_df.drop(['Open Time', 'Close Time', 'Quote Asset Volume', 'TB Base Volume', 'TB Quote Volume', 'Ignore', 'Number of Trades'], axis=1)

# plot_systemETH(hourlycandles_df, 'ETH-USDT (2 hour timeframe)')

# identify long and short position
long_positions = np.where(hourlycandles_df['ema20'] > hourlycandles_df['sma200'], 1, 0)
hourlycandles_df['Position'] = long_positions
hourlycandles_df.round(3)

# set the entry point and entry time ('ep', 'date_time') for buy and sell
hourlycandles_df['OpenTime'] = hourlycandles_df.index
buy_signals = (hourlycandles_df['Position'] == 1) & (hourlycandles_df['Position'].shift(1) == 0) # when position is 0 and the next row (-ve means after) is postion 1
sell_signals = (hourlycandles_df['Position'] == 0) & (hourlycandles_df['Position'].shift(1) == 1)
hourlycandles_df.loc[(buy_signals | sell_signals), 'ep'] = hourlycandles_df['Open']
hourlycandles_df.loc[(buy_signals | sell_signals), 'date_time'] = hourlycandles_df['OpenTime']

# fill the empty cell with value from previous row
hourlycandles_df = hourlycandles_df.fillna(method='ffill')

# set tp and sl of sell to 1000 pips below and above 
hourlycandles_df.loc[sell_signals, 'tp'] = hourlycandles_df['Open'] - 10.00
hourlycandles_df.loc[sell_signals, 'sl'] = hourlycandles_df['Open'] + 10.00
# set tp and sl of buy to 1000 pips above and below 
hourlycandles_df.loc[buy_signals, 'tp'] = hourlycandles_df['Open'] + 10.00
hourlycandles_df.loc[buy_signals, 'sl'] = hourlycandles_df['Open'] - 10.00

# fill the empty cell with value from previous row
hourlycandles_df = hourlycandles_df.fillna(method='ffill')

# identify the winning and lossing trade
hourlycandles_df['outcome'] = ' '
hourlycandles_df.loc[(hourlycandles_df['Position'] == 1) & (hourlycandles_df['Close'] > hourlycandles_df['tp']), 'outcome'] = 'WIN'
hourlycandles_df.loc[(hourlycandles_df['Position'] == 1) & (hourlycandles_df['Close'] < hourlycandles_df['sl']), 'outcome'] = 'LOSS'
hourlycandles_df.loc[(hourlycandles_df['Position'] == 0) & (hourlycandles_df['Close'] < hourlycandles_df['tp']), 'outcome'] = 'WIN'
hourlycandles_df.loc[(hourlycandles_df['Position'] == 0) & (hourlycandles_df['Close'] > hourlycandles_df['sl']), 'outcome'] = 'LOSS'

# get a new empty column to store index value 'Open Time'
# hourlycandles_df.rename(columns= {'ot': 'Open Time'}, inplace=True)

# reset index 
df2=hourlycandles_df.reset_index()

# create a new column 'ts' (stand for timestamp) to store the time. Neede to convert to timestamp format because the year, month, date type format will be excluded after we regroup in the future step
df2['ts'] = df2['Open Time'].astype('int64') // 10**9

# # drop the empty cell, by replace the empty with NaN then using dropna function
df2['outcome'] = df2['outcome'].replace(' ', np.nan)
df2 = df2.dropna(subset=['outcome'])

# # group by 'tp' and get first outcome of the buy/sell 
df3 = df2.groupby(['tp'], as_index=False)
df3 = df3.first()

# when grouped, 'Open Time' column will disolve. So I create a new column 'Open Time', the reference to column 'ts' and convert to year, month, date format
df3['Open Time'] = pd.to_datetime(df3['ts'], unit='s')
df3.set_index("date_time", inplace = True)
df3 = df3.sort_index()

# rename column, drop unuse column and sort the column according to given order
df3.rename(columns= {'Open Time': 'Exit Time'}, inplace=True)
df3 = df3[['Position', 'ep', 'tp', 'sl', 'outcome', 'Exit Time', 'Close']]

# at column 'position' change the value of 1 to long and 0 to short
df3.loc[df3['Position'] == 1, ['Position']] = 'Long'
df3.loc[df3['Position'] == 0, ['Position']] = 'Short'
df3
```

::: {.output .execute_result execution_count="280"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Position</th>
      <th>ep</th>
      <th>tp</th>
      <th>sl</th>
      <th>outcome</th>
      <th>Exit Time</th>
      <th>Close</th>
    </tr>
    <tr>
      <th>date_time</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2022-10-08 10:00:00</th>
      <td>Short</td>
      <td>1327.25</td>
      <td>1317.25</td>
      <td>1337.25</td>
      <td>WIN</td>
      <td>2022-10-08 21:00:00</td>
      <td>1307.34</td>
    </tr>
    <tr>
      <th>2022-10-14 13:00:00</th>
      <td>Long</td>
      <td>1338.74</td>
      <td>1348.74</td>
      <td>1328.74</td>
      <td>LOSS</td>
      <td>2022-10-14 14:00:00</td>
      <td>1320.30</td>
    </tr>
    <tr>
      <th>2022-10-14 19:00:00</th>
      <td>Short</td>
      <td>1300.21</td>
      <td>1290.21</td>
      <td>1310.21</td>
      <td>WIN</td>
      <td>2022-10-15 08:00:00</td>
      <td>1280.47</td>
    </tr>
    <tr>
      <th>2022-10-17 05:00:00</th>
      <td>Long</td>
      <td>1305.05</td>
      <td>1315.05</td>
      <td>1295.05</td>
      <td>WIN</td>
      <td>2022-10-17 09:00:00</td>
      <td>1317.98</td>
    </tr>
    <tr>
      <th>2022-10-19 22:00:00</th>
      <td>Short</td>
      <td>1294.33</td>
      <td>1284.33</td>
      <td>1304.33</td>
      <td>WIN</td>
      <td>2022-10-20 00:00:00</td>
      <td>1276.85</td>
    </tr>
    <tr>
      <th>2022-10-22 14:00:00</th>
      <td>Long</td>
      <td>1310.29</td>
      <td>1320.29</td>
      <td>1300.29</td>
      <td>WIN</td>
      <td>2022-10-23 17:00:00</td>
      <td>1328.69</td>
    </tr>
    <tr>
      <th>2022-11-02 20:00:00</th>
      <td>Short</td>
      <td>1535.93</td>
      <td>1525.93</td>
      <td>1545.93</td>
      <td>WIN</td>
      <td>2022-11-02 20:00:00</td>
      <td>1511.27</td>
    </tr>
    <tr>
      <th>2022-11-04 13:00:00</th>
      <td>Long</td>
      <td>1609.72</td>
      <td>1619.72</td>
      <td>1599.72</td>
      <td>WIN</td>
      <td>2022-11-04 14:00:00</td>
      <td>1660.45</td>
    </tr>
    <tr>
      <th>2022-11-07 09:00:00</th>
      <td>Short</td>
      <td>1568.08</td>
      <td>1558.08</td>
      <td>1578.08</td>
      <td>LOSS</td>
      <td>2022-11-07 10:00:00</td>
      <td>1578.54</td>
    </tr>
    <tr>
      <th>2022-11-24 06:00:00</th>
      <td>Long</td>
      <td>1200.88</td>
      <td>1210.88</td>
      <td>1190.88</td>
      <td>WIN</td>
      <td>2022-11-24 06:00:00</td>
      <td>1214.01</td>
    </tr>
    <tr>
      <th>2022-12-06 18:00:00</th>
      <td>Short</td>
      <td>1251.70</td>
      <td>1241.70</td>
      <td>1261.70</td>
      <td>LOSS</td>
      <td>2022-12-06 23:00:00</td>
      <td>1271.32</td>
    </tr>
    <tr>
      <th>2022-12-09 03:00:00</th>
      <td>Long</td>
      <td>1281.07</td>
      <td>1291.07</td>
      <td>1271.07</td>
      <td>LOSS</td>
      <td>2022-12-09 18:00:00</td>
      <td>1268.85</td>
    </tr>
    <tr>
      <th>2022-12-12 04:00:00</th>
      <td>Short</td>
      <td>1243.83</td>
      <td>1233.83</td>
      <td>1253.83</td>
      <td>LOSS</td>
      <td>2022-12-12 10:00:00</td>
      <td>1255.30</td>
    </tr>
    <tr>
      <th>2022-12-13 02:00:00</th>
      <td>Long</td>
      <td>1267.53</td>
      <td>1277.53</td>
      <td>1257.53</td>
      <td>WIN</td>
      <td>2022-12-13 09:00:00</td>
      <td>1278.04</td>
    </tr>
    <tr>
      <th>2022-12-16 03:00:00</th>
      <td>Short</td>
      <td>1269.86</td>
      <td>1259.86</td>
      <td>1279.86</td>
      <td>WIN</td>
      <td>2022-12-16 08:00:00</td>
      <td>1244.62</td>
    </tr>
    <tr>
      <th>2022-12-23 03:00:00</th>
      <td>Long</td>
      <td>1224.63</td>
      <td>1234.63</td>
      <td>1214.63</td>
      <td>LOSS</td>
      <td>2022-12-25 14:00:00</td>
      <td>1214.24</td>
    </tr>
    <tr>
      <th>2022-12-28 00:00:00</th>
      <td>Short</td>
      <td>1211.55</td>
      <td>1201.55</td>
      <td>1221.55</td>
      <td>WIN</td>
      <td>2022-12-28 03:00:00</td>
      <td>1197.72</td>
    </tr>
    <tr>
      <th>2023-01-02 10:00:00</th>
      <td>Long</td>
      <td>1217.18</td>
      <td>1227.18</td>
      <td>1207.18</td>
      <td>WIN</td>
      <td>2023-01-04 02:00:00</td>
      <td>1231.60</td>
    </tr>
  </tbody>
</table>
</div>
```
:::
:::

::: {.cell .markdown}
Strategy returns
:::

::: {.cell .code execution_count="18"}
``` {.python}
# The returns of the Buy and Hold strategy:
hourlycandles_df['Hold'] = np.log(hourlycandles_df['Close'] / hourlycandles_df['Close'].shift(1))
# The returns of the Moving Average strategy:
hourlycandles_df['Strategy'] = hourlycandles_df['Position'].shift(1) * hourlycandles_df['Hold']
# We need to get rid of the NaN generated in the first row:
hourlycandles_df.dropna(inplace=True)
hourlycandles_df
```

::: {.output .execute_result execution_count="18"}
```{=html}
<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Open</th>
      <th>High</th>
      <th>Low</th>
      <th>Close</th>
      <th>Volume</th>
      <th>sma200</th>
      <th>ema20</th>
      <th>Position</th>
      <th>tp</th>
      <th>sl</th>
      <th>Hold</th>
      <th>Strategy</th>
    </tr>
    <tr>
      <th>Open Time</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2022-09-05 22:00:00</th>
      <td>1596.99</td>
      <td>1631.99</td>
      <td>1592.64</td>
      <td>1617.80</td>
      <td>50095.1706</td>
      <td>1578.10730</td>
      <td>1579.202366</td>
      <td>1</td>
      <td>1597.99</td>
      <td>1595.99</td>
      <td>0.012947</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2022-09-07 22:00:00</th>
      <td>1645.74</td>
      <td>1657.50</td>
      <td>1620.24</td>
      <td>1630.00</td>
      <td>55816.3941</td>
      <td>1576.13955</td>
      <td>1576.570726</td>
      <td>1</td>
      <td>1646.74</td>
      <td>1644.74</td>
      <td>-0.009610</td>
      <td>-0.0</td>
    </tr>
    <tr>
      <th>2022-10-04 16:00:00</th>
      <td>1353.93</td>
      <td>1354.89</td>
      <td>1338.12</td>
      <td>1347.35</td>
      <td>40269.4914</td>
      <td>1327.72460</td>
      <td>1329.850835</td>
      <td>1</td>
      <td>1354.93</td>
      <td>1352.93</td>
      <td>-0.004872</td>
      <td>-0.0</td>
    </tr>
    <tr>
      <th>2022-10-18 00:00:00</th>
      <td>1331.39</td>
      <td>1341.73</td>
      <td>1329.33</td>
      <td>1332.83</td>
      <td>41627.2583</td>
      <td>1314.25290</td>
      <td>1314.515344</td>
      <td>1</td>
      <td>1332.39</td>
      <td>1330.39</td>
      <td>0.001073</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2022-10-23 04:00:00</th>
      <td>1313.22</td>
      <td>1314.72</td>
      <td>1308.02</td>
      <td>1308.72</td>
      <td>10580.9798</td>
      <td>1305.68890</td>
      <td>1305.753614</td>
      <td>1</td>
      <td>1314.22</td>
      <td>1312.22</td>
      <td>-0.003433</td>
      <td>-0.0</td>
    </tr>
  </tbody>
</table>
</div>
```
:::
:::

::: {.cell .code execution_count="19"}
``` {.python}
returns = np.exp(hourlycandles_df[['Hold', 'Strategy']].sum()) - 1
print(f"Buy and hold return: {round(returns['Hold']*100,2)}%")
print(f"Strategy return: {round(returns['Strategy']*100,2)}%")
```

::: {.output .stream .stdout}
    Buy and hold return: -0.39%
    Strategy return: 0.0%
:::
:::

::: {.cell .code execution_count="20"}
``` {.python}
n_days = len(hourlycandles_df)
# Assuming 252 trading days in a year:
ann_returns = 252 / n_days * returns
print(f"Buy and hold annualized return: {round(ann_returns['Hold']*100,2)}%")
print(f"Strategy annualized return:{round(ann_returns['Strategy']*100,2)}%")
```

::: {.output .stream .stdout}
    Buy and hold annualized return: -19.59%
    Strategy annualized return:0.0%
:::
:::
