# A Look at Pokemon by Generation

Pokemon became a sensation in the 1990's and continues to be a popular franchise to this date. 
Pokemon the video game has evolved (pun intended) over the decades into a complex game that takes 
a lot of statistics and analyze to create teams that can win the meta at tournaments. The point 
of this kernal is to look at the Pokemon by generation and see if we can find any insight into 
the numbers behind the design.

# A Look at Every Generation

Looking at all the generations at once we can create a control that we can compare to the 
other datasets. Here we make a Pearson correlation chart to see the correlations and create 
a histogram for each variable to see distribution and other useful information.

To start looking at the data first you need to upload libraries.

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
#import libraries
```

Then import the data.

```python
pokemon = pd.read_csv('Pokemon.csv')
#import data
```

Now we can graph the data.

```python
colormap = plt.cm.plasma
plt.figure(figsize=(16,12))
plt.title('Pearson correlation of data', y = 1.05, size = 15)
sns.heatmap(pokemon.corr(), linewidths=0.1, vmax=1.0, square=True, cmap=colormap, linecolor='black', annot=True)
sns.plt.show()
#color map looking at Pearson correlations
```

![alt text](https://github.com/justinminsk/Pokemon-Stats/blob/master/heat1.png)

As we can see sp. def and defense as well as sp. attack and sp. def have some of 
the strongest correlations.

```python
pokemon.hist()
fig=plt.gcf()
fig.set_size_inches(20,15)
plt.show()
#histograms of the different stats to show if they have normal distribution
```
