## CSV FORMAT

| datetime            | src                     | dst                     | channel | mean_rssi | pdr   |
|---------------------|-------------------------|-------------------------|---------|-----------|-------|
|  iso8601 string     | string                  | string                  | string  | float     | float |

### Standard example:

| datetime            | src                     | dst                     | channel | mean_rssi | pdr |
|---------------------|-------------------------|-------------------------|---------|-----------|-----|
| 2017-12-19 21:35:41 | 05-43-32-ff-03-d7-94-75 | 05-43-32-ff-03-da-c3-76 | 11      | -74.5     | 1.0 |

### The source or destination can be empty (i.e when measured on all the neighbors of the src):

| datetime            | src                     | dst                     | channel | mean_rssi | pdr |
|---------------------|-------------------------|-------------------------|---------|-----------|-----|
| 2017-12-19 21:35:41 | 05-43-32-ff-03-d7-94-75 |                         | 11      | -74.5     | 1.0 |

### The channel can be a range:
| datetime            | src                     | dst                     | channel | mean_rssi | pdr |
|---------------------|-------------------------|-------------------------|---------|-----------|-----|
| 2017-12-19 21:35:41 | 05-43-32-ff-03-d7-94-75 | 05-43-32-ff-03-da-c3-76 | 11-25   | -74.5     | 1.0 |
