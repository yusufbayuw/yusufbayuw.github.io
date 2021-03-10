
---
title: "Portfolio bokeh md"
excerpt: "Short description of portfolio item number 2 <br/><img src='/images/500x300.png'>"
collection: portfolio
---
```python
import numpy as np # we will use this later, so import it now

from bokeh.io import output_notebook, show
from bokeh.plotting import figure
```


```python

```


```python

```


```python
output_notebook()
```



<div class="bk-root">
    <a href="https://bokeh.org" target="_blank" class="bk-logo bk-logo-small bk-logo-notebook"></a>
    <span id="1001">Loading BokehJS ...</span>
</div>





```python
import bokeh.sampledata
bokeh.sampledata.download()
```

    Using data directory: C:\Users\lenovo\.bokeh\data
    Skipping 'CGM.csv' (checksum match)
    Skipping 'US_Counties.zip' (checksum match)
    Skipping 'us_cities.json' (checksum match)
    Skipping 'unemployment09.csv' (checksum match)
    Skipping 'AAPL.csv' (checksum match)
    Skipping 'FB.csv' (checksum match)
    Skipping 'GOOG.csv' (checksum match)
    Skipping 'IBM.csv' (checksum match)
    Skipping 'MSFT.csv' (checksum match)
    Skipping 'WPP2012_SA_DB03_POPULATION_QUINQUENNIAL.zip' (checksum match)
    Skipping 'gapminder_fertility.csv' (checksum match)
    Skipping 'gapminder_population.csv' (checksum match)
    Skipping 'gapminder_life_expectancy.csv' (checksum match)
    Skipping 'gapminder_regions.csv' (checksum match)
    Skipping 'world_cities.zip' (checksum match)
    Skipping 'airports.json' (checksum match)
    Skipping 'movies.db.zip' (checksum match)
    Skipping 'airports.csv' (checksum match)
    Skipping 'routes.csv' (checksum match)
    Skipping 'haarcascade_frontalface_default.xml' (checksum match)
    

# Scatter Plot


```python
# create a new plot with default tools, using figure
p = figure(plot_width=400, plot_height=400)

# add a circle renderer with x and y coordinates, size, color, and alpha
p.circle([1, 2, 3, 4, 5], [6, 7, 2, 4, 5], 
         radius=0.1, 
         line_color="navy", 
         fill_color="orange", 
         fill_alpha=0.5)

show(p) # show the results
```








<div class="bk-root" id="39ce6c3c-9a56-4bbc-9f35-13f69b081a09" data-root-id="1002"></div>






```python
# create a new plot using figure
p = figure(plot_width=400, plot_height=400)

# add a square renderer with a size, color, alpha, and sizes
p.square([1, 2, 3, 4, 5], [6, 7, 2, 4, 5], size=[10, 15, 20, 25, 30], color="firebrick", alpha=0.6)

show(p) # show the results
```








<div class="bk-root" id="e35f1d78-8362-4dca-88a4-65fc26b0c233" data-root-id="1092"></div>





* asterisk()
* circle()
* circle_cross()
* circle_x()
* cross()
* diamond()
* diamond_cross()
* hex()
* inverted_triangle()
* square()
* square_cross()
* square_x()
* triangle()
* x()


```python
# create a new plot using figure
p = figure(plot_width=400, plot_height=400)

# add a square renderer with a size, color, alpha, and sizes
p.diamond_cross([1, 2, 3, 4, 5], [6, 7, 2, 4, 5], size=[10, 15, 20, 25, 30], color="firebrick", alpha=0.6)

show(p) # show the results
```








<div class="bk-root" id="ce49b05f-1c63-4f1d-a56f-1a860f03d417" data-root-id="1191"></div>






```python
# EXERCISE: Make a scatter plot using the "autompg" dataset

from bokeh.sampledata.autompg import autompg as df # run df.head() to inspect 
```


```python
df.head()
```




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
      <th>mpg</th>
      <th>cyl</th>
      <th>displ</th>
      <th>hp</th>
      <th>weight</th>
      <th>accel</th>
      <th>yr</th>
      <th>origin</th>
      <th>name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>18.0</td>
      <td>8</td>
      <td>307.0</td>
      <td>130</td>
      <td>3504</td>
      <td>12.0</td>
      <td>70</td>
      <td>1</td>
      <td>chevrolet chevelle malibu</td>
    </tr>
    <tr>
      <th>1</th>
      <td>15.0</td>
      <td>8</td>
      <td>350.0</td>
      <td>165</td>
      <td>3693</td>
      <td>11.5</td>
      <td>70</td>
      <td>1</td>
      <td>buick skylark 320</td>
    </tr>
    <tr>
      <th>2</th>
      <td>18.0</td>
      <td>8</td>
      <td>318.0</td>
      <td>150</td>
      <td>3436</td>
      <td>11.0</td>
      <td>70</td>
      <td>1</td>
      <td>plymouth satellite</td>
    </tr>
    <tr>
      <th>3</th>
      <td>16.0</td>
      <td>8</td>
      <td>304.0</td>
      <td>150</td>
      <td>3433</td>
      <td>12.0</td>
      <td>70</td>
      <td>1</td>
      <td>amc rebel sst</td>
    </tr>
    <tr>
      <th>4</th>
      <td>17.0</td>
      <td>8</td>
      <td>302.0</td>
      <td>140</td>
      <td>3449</td>
      <td>10.5</td>
      <td>70</td>
      <td>1</td>
      <td>ford torino</td>
    </tr>
  </tbody>
</table>
</div>



# Line Plots


```python
# create a new plot (with a title) using figure
p = figure(plot_width=400, plot_height=400, title="My Line Plot")

# add a line renderer
p.line([1, 2, 3, 4, 5], [6, 7, 2, 4, 5], 
       line_width=2,
       line_color='red', 
       line_dash=[])

show(p) # show the results
```








<div class="bk-root" id="32aa1793-833b-46d8-bf8b-dd20a65a95a3" data-root-id="1299"></div>






```python
from bokeh.sampledata.glucose import data
data.head()
```




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
      <th>isig</th>
      <th>glucose</th>
    </tr>
    <tr>
      <th>datetime</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2010-03-24 09:51:00</th>
      <td>22.59</td>
      <td>258</td>
    </tr>
    <tr>
      <th>2010-03-24 09:56:00</th>
      <td>22.52</td>
      <td>260</td>
    </tr>
    <tr>
      <th>2010-03-24 10:01:00</th>
      <td>22.23</td>
      <td>258</td>
    </tr>
    <tr>
      <th>2010-03-24 10:06:00</th>
      <td>21.56</td>
      <td>254</td>
    </tr>
    <tr>
      <th>2010-03-24 10:11:00</th>
      <td>20.79</td>
      <td>246</td>
    </tr>
  </tbody>
</table>
</div>




```python
# reduce data size to one week
week = data.loc['2010-10-01':'2010-10-08']

p = figure(x_axis_type="datetime", title="Glocose Range", plot_height=350, plot_width=800)
p.xgrid.grid_line_color=None
p.ygrid.grid_line_alpha=0.5
p.xaxis.axis_label = 'Time'
p.yaxis.axis_label = 'Value'

p.line(week.index, week.glucose)

show(p)
```








<div class="bk-root" id="3aa37e01-f0df-443a-997d-c9cb826830a6" data-root-id="1412"></div>






```python
# EXERCISE: Look at the AAPL data from bokeh.sampledata.stocks and create a line plot using it
from bokeh.sampledata.stocks import AAPL

# AAPL.keys()
# dict_keys(['date', 'open', 'high', 'low', 'close', 'volume', 'adj_close'])

dates = np.array(AAPL['date'], dtype=np.datetime64) # convert date strings to real datetimes
```

# Hex Tiling


```python
from bokeh.palettes import Viridis256
from bokeh.util.hex import hexbin

n = 50000
x = np.random.standard_normal(n)
y = np.random.standard_normal(n)

bins = hexbin(x, y, 0.1)

# color map the bins by hand, will see how to use linear_cmap later
color = [Viridis256[int(i)] for i in bins.counts/max(bins.counts)*255]

# match_aspect ensures neither dimension is squished, regardless of the plot size
p = figure(tools="wheel_zoom,reset", match_aspect=True, background_fill_color='#440154')
p.grid.visible = False

p.hex_tile(bins.q, bins.r, size=0.1, line_color=None, fill_color=color)

show(p)
```








<div class="bk-root" id="51524834-8706-4f5e-a788-8c950bc002b1" data-root-id="1605"></div>






```python
# Exercise: Experiment with the size parameter to hexbin, and using different data as input
```

# Images


```python
N = 500
x = np.linspace(0, 10, N)
y = np.linspace(0, 10, N)
xx, yy = np.meshgrid(x, y)

img = np.sin(xx)*np.cos(yy)

p = figure(x_range=(0, 10), y_range=(0, 10))

# must give a vector of image data for image parameter
p.image(image=[img], x=0, y=0, dw=10, dh=10, palette="Spectral11")

show(p)  
```








<div class="bk-root" id="6ee413c3-ae16-4ab0-8950-dc39efdd83b1" data-root-id="1735"></div>






```python
from __future__ import division
import numpy as np
 
N = 20
img = np.empty((N,N), dtype=np.uint32) 

# use an array view to set each RGBA channel individiually
view = img.view(dtype=np.uint8).reshape((N, N, 4))
for i in range(N):
    for j in range(N):
        view[i, j, 0] = int(i/N*255) # red
        view[i, j, 1] = 158          # green
        view[i, j, 2] = int(j/N*255) # blue
        view[i, j, 3] = 255          # alpha
        
# create a new plot (with a fixed range) using figure
p = figure(x_range=[0,10], y_range=[0,10])

# add an RGBA image renderer
p.image_rgba(image=[img], x=[0], y=[0], dw=[10], dh=[10])

show(p) 
```








<div class="bk-root" id="38dd30c8-6eb3-446f-a49c-df39a88d5566" data-root-id="1890"></div>





https://docs.bokeh.org/en/latest/docs/user_guide/plotting.html#ovals-and-ellipses


```python

```
