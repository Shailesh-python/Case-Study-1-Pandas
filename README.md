# Case Study #1 Danny's Diner

<img src='https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white)'/>
<img src='https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)'/>

The following are my solutions to the Case Study 1 Danny's Diner questions using pandas in
[Danny Ma's Serious SQL course](https://www.datawithdanny.com/ "Data With Danny")
<br/>
<br/>
Danny has shared with you 3 key datasets for this case study :
[Data Set](https://github.com/Shailesh-python/Case_Study_1_Dannys_Diner/blob/main/Data%20And%20Tables)
<br/>
- `sales`

- `menu`

- `members`


```python
import pandas as pd
import pyodbc
from pandas.tseries.offsets import DateOffset
from datetime import timedelta
import numpy as np

import warnings
warnings.filterwarnings('ignore')
```


```python
import pyodbc as py
import pandas as pd

conn = py.connect(
    "DRIVER={SQL Server};SERVER=SHAILESH-PC\SQLEXPRESS;DATABASE=DannyMa;"
)

df_sales = pd.read_sql_query('select * from dannys_diner.sales',conn)
df_members = pd.read_sql_query('select * from dannys_diner.members',conn)
df_menu = pd.read_sql_query('select * from dannys_diner.menu',conn)

conn.close()
```


[Check my solution](https://github.com/Shailesh-python/Case-Study-1-Pandas/blob/main/Case%20Study%201%20Solutions.ipynb)
