# Bike Sharing Rides Prediction

## Introduction

For bike sharing companies, it is important to predict how many bikes they need. If there are too few bikes, they will lose money from potential riders. If there are too many bikes, it is a waste of money for them. Thus, it is useful to predict from historical data how many bikes they need in the future.

In this project, a neural network has been built and then trained on historical data to predict bike sharing rides.

### Files

	- Readme.txt: details of the datasets (including licence) written by the data provider
	- hour.csv : bike sharing counts aggregated on hourly basis. Records: 17379 hours


### Data <sup>[1]</sup>

	- instant: record index
	- dteday : date
	- season : season (1:springer, 2:summer, 3:fall, 4:winter)
	- yr : year (0: 2011, 1:2012)
	- mnth : month ( 1 to 12)
	- hr : hour (0 to 23)
	- holiday : weather day is holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
	- weekday : day of the week
	- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
	+ weathersit :
		- 1: Clear, Few clouds, Partly cloudy, Partly cloudy
		- 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
		- 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
		- 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
	- temp : Normalized temperature in Celsius. The values are divided to 41 (max)
	- atemp: Normalized feeling temperature in Celsius. The values are divided to 50 (max)
	- hum: Normalized humidity. The values are divided to 100 (max)
	- windspeed: Normalized wind speed. The values are divided to 67 (max)
	- casual: count of casual users
	- registered: count of registered users
	- cnt: count of total rental bikes including both casual and registered


<sup>[1]</sup>
License: Fanaee-T, Hadi, and Gama, Joao, "Event labeling combining ensemble detectors and background knowledge", Progress in Artificial Intelligence (2013): pp. 1-15, Springer Berlin Heidelberg, doi:10.1007/s13748-013-0040-3.

## Installation
- Google Colab
- Python 3
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

import unittest
import sys
```

## Hyperparameters

```
iterations      = 3000
learning_rate   = 0.6
hidden_nodes    = 20
output_nodes    = 1
```

## Results

### Loss
Training loss: 0.069
Validation loss: 0.144

![Loss]()

### Prediction
![prediction]()
