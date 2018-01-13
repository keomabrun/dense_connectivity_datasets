## CSV FORMAT

| datetime            | src                     | dst                     | channel | mean_rssi | pdr           | transaction_id |
|---------------------|-------------------------|-------------------------|---------|-----------|---------------|----------------|
|  iso8601 string     | string                  | string                  | string  | float     | float (0-100) | int            |

Each CSV is prepended by a one-line header. The header is the json dump of a dict. The header contains the dataset meta data.
Ex:
```
{"site": "grenoble", "tx_length": 100, "start_date": "2017-06-20 16:22:15", "end_date": "2017-06-21 10:29:29", "tx_count": 100, "node_count": 50, "channel_count": 16, "transaction_count": 10, "tx_ifdur": 10}
```

### Standard example:

| datetime            | src                     | dst                     | channel | mean_rssi | pdr | transaction_id |
|---------------------|-------------------------|-------------------------|---------|-----------|-----|----------------|
| 2017-12-19 21:35:41 | 05-43-32-ff-03-d7-94-75 | 05-43-32-ff-03-da-c3-76 | 11      | -74.5     | 1.0 | 1              |

### The source or destination can be empty (i.e when measured on all the neighbors of the src):

| datetime            | src                     | dst                     | channel | mean_rssi | pdr | transaction_id |
|---------------------|-------------------------|-------------------------|---------|-----------|-----|----------------|
| 2017-12-19 21:35:41 | 05-43-32-ff-03-d7-94-75 |                         | 11      | -74.5     | 1.0 | 1              |

### The channel can be a range:
| datetime            | src                     | dst                     | channel | mean_rssi | pdr | transaction_id |
|---------------------|-------------------------|-------------------------|---------|-----------|-----|----------------|
| 2017-12-19 21:35:41 | 05-43-32-ff-03-d7-94-75 | 05-43-32-ff-03-da-c3-76 | 11-25   | -74.5     | 1.0 | 1              |
