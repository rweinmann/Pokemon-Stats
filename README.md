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

![alt text](https://github.com/justinminsk/Pokemon-Stats/blob/master/hist1.png)

Attack, Defense, HP, Sp. Atk, Sp. Def, and Speed have decent distributions.

# Generation 1

```python
df1 = pokemon[pokemon.Generation == 1]
#look at just first generation pokemon

colormap = plt.cm.plasma
plt.figure(figsize=(16,12))
plt.title('Pearson correlation of data', y = 1.05, size = 15)
sns.heatmap(df1.corr(), linewidths=0.1, vmax=1.0, square=True, cmap=colormap, linecolor='black', annot=True)
plt.savefig('heat2.png', bbox_inches='tight')
sns.plt.show()
#color map looking at Pearson correlations
```

![alt text](https://github.com/justinminsk/Pokemon-Stats/blob/master/heat2.png)

Here we can see that sp. attack and sp. def have the highest correlation, even higher then our control. This means in gen one sp. attack and sp. def tended to go hand in hand.

```python
df1.hist()
fig=plt.gcf()
fig.set_size_inches(20,15)
plt.savefig('hist2.png', bbox_inches='tight')
plt.show()
#histograms of the different stats to show if they have normal distribution
```

![alt text](https://github.com/justinminsk/Pokemon-Stats/blob/master/hist2.png)

Attack, Defense, HP, Sp. Atk, and Speed have decent distributions.

# Generation 2

```python
df1 = pokemon[pokemon.Generation == 2]
#look at gen 2 pokemon

colormap = plt.cm.plasma
plt.figure(figsize=(16,12))
plt.title('Pearson correlation of data', y = 1.05, size = 15)
sns.heatmap(df1.corr(), linewidths=0.1, vmax=1.0, square=True, cmap=colormap, linecolor='black', annot=True)
plt.savefig('heat3.png', bbox_inches='tight')
sns.plt.show()
#color map looking at Pearson correlations
```

![alt text](https://github.com/justinminsk/Pokemon-Stats/blob/master/heat3.png)


In gen two it seems that the two def stats (sp. def and defense) correlate best, but we see that sp. def and sp. attack correlation almost completely drops off compared to our control and gen one. 
The other new trend is between attack and defense which have a strong correlation compared to the rest of the stats.

```python
df1.hist()
fig=plt.gcf()
fig.set_size_inches(20,15)
plt.savefig('hist3.png', bbox_inches='tight')
plt.show()
#histograms of the different stats to show if they have normal distribution
```

![alt text](https://github.com/justinminsk/Pokemon-Stats/blob/master/hist3.png)

This generation does not have normal distributions.

# Generation 3

```python
df1 = pokemon[pokemon.Generation == 3]
#look at gen 3 pokemon

colormap = plt.cm.plasma
plt.figure(figsize=(16,12))
plt.title('Pearson correlation of data', y = 1.05, size = 15)
sns.heatmap(df1.corr(), linewidths=0.1, vmax=1.0, square=True, cmap=colormap, linecolor='black', annot=True)
plt.savefig('heat4.png', bbox_inches='tight')
sns.plt.show()
#color map looking at Pearson correlations
```

![alt text](https://github.com/justinminsk/Pokemon-Stats/blob/master/heat4.png)

This gen (gen three) has a crazy high correlation between sp. atk and attack. Speed and sp atk also have high correlation which is a new correlation. This could be a generation that you would leave out for trying to predict type off of stats. The trend with the defenses (sp. def and defense) contiue also.

```python
df1.hist()
fig=plt.gcf()
fig.set_size_inches(20,15)
plt.savefig('hist4.png', bbox_inches='tight')
plt.show()
#histograms of the different stats to show if they have normal distribution
```

![alt text](https://github.com/justinminsk/Pokemon-Stats/blob/master/hist4.png)

# Generation 4

```python
df1 = pokemon[pokemon.Generation == 4]
#look at gen 4 pokemon

colormap = plt.cm.plasma
plt.figure(figsize=(16,12))
plt.title('Pearson correlation of data', y = 1.05, size = 15)
sns.heatmap(df1.corr(), linewidths=0.1, vmax=1.0, square=True, cmap=colormap, linecolor='black', annot=True)
plt.savefig('heat5.png', bbox_inches='tight')
sns.plt.show()
#color map looking at Pearson correlations
```

![alt text](https://github.com/justinminsk/Pokemon-Stats/blob/master/heat5.png)


Here we have the correlation out of all the gens. At a 71% correlation defense and sp. def in this generation should be the same or close to the same number. Here we also see a correlation between hp and attack which is a different trend compared to other gens.

```python
df1.hist()
fig=plt.gcf()
fig.set_size_inches(20,15)
plt.savefig('hist5.png', bbox_inches='tight')
plt.show()
#histograms of the different stats to show if they have normal distribution
```

![alt text](https://github.com/justinminsk/Pokemon-Stats/blob/master/hist5.png)

Attack has decent distribution.

# Generation 5

```python
df1 = pokemon[pokemon.Generation == 5]
#look at gen 5 pokemon

colormap = plt.cm.plasma
plt.figure(figsize=(16,12))
plt.title('Pearson correlation of data', y = 1.05, size = 15)
sns.heatmap(df1.corr(), linewidths=0.1, vmax=1.0, square=True, cmap=colormap, linecolor='black', annot=True)
plt.savefig('heat6.png', bbox_inches='tight')
sns.plt.show()
#color map looking at Pearson correlations
```

![alt text](https://github.com/justinminsk/Pokemon-Stats/blob/master/heat6.png)

This generation we see a come back of sp. atk and sp. def correlation, we also still have an unsually high correlation of sp. def and defense. The trend form last gen (gen 4) of attack and hp contiues as well. 

```python
df1.hist()
fig=plt.gcf()
fig.set_size_inches(20,15)
plt.savefig('hist6.png', bbox_inches='tight')
plt.show()
#histograms of the different stats to show if they have normal distribution
```

![alt text](https://github.com/justinminsk/Pokemon-Stats/blob/master/hist6.png)

Attack and HP have decent distributions.

# Generation 6

```python
df1 = pokemon[pokemon.Generation == 6]
#look at gen 6 pokemon

colormap = plt.cm.plasma
plt.figure(figsize=(16,12))
plt.title('Pearson correlation of data', y = 1.05, size = 15)
sns.heatmap(df1.corr(), linewidths=0.1, vmax=1.0, square=True, cmap=colormap, linecolor='black', annot=True)
plt.savefig('heat7.png', bbox_inches='tight')
sns.plt.show()
#color map looking at Pearson correlations
```

![alt text](https://github.com/justinminsk/Pokemon-Stats/blob/master/heat7.png)

The trends in gen 6 are speed and sp atk, sp. def, and sp. atk, attack and sp atk, and attack and hp. 

```python
df1.hist()
fig=plt.gcf()
fig.set_size_inches(20,15)
plt.savefig('hist7.png', bbox_inches='tight')
plt.show()
#histograms of the different stats to show if they have normal distribution
```

![alt text](https://github.com/justinminsk/Pokemon-Stats/blob/master/hist7.png)

Attack, Defense, and HP have decent distributions.

# Conclusion

Each gen has its' own unique correlations and trends. This means that if you want to find a strong tank Pokemon (high hp, sp. def, defence) you might look at gen 4 with a 71% correlation between sp. def and defence. The next varible to look at would be legendary which might skew the data. 

# Looking at Pokemon without Legendaries

```python
df1 = pokemon['Legendary'].map(lambda x: x == 0)
df1 = pokemon[df1]
#get the data without legendaries

colormap = plt.cm.plasma
plt.figure(figsize=(16,12))
plt.title('Pearson correlation of data without legendaries', y = 1.05, size = 15)
sns.heatmap(df1.corr(), linewidths=0.1, vmax=1.0, square=True, cmap=colormap, linecolor='black', annot=True)
plt.savefig('heat8.png', bbox_inches='tight')
sns.plt.show()
#color map looking at Pearson correlations
colormap = plt.cm.plasma
plt.figure(figsize=(16,12))
plt.title('Pearson correlation of data with legendaries', y = 1.05, size = 15)
sns.heatmap(pokemon.corr(), linewidths=0.1, vmax=1.0, square=True, cmap=colormap, linecolor='black', annot=True)
sns.plt.show()
#color map looking at Pearson correlations
```

![alt text](https://github.com/justinminsk/Pokemon-Stats/blob/master/heat8.png)

## Histograms of data without legendaries

```python
df1.hist()
fig=plt.gcf()
fig.set_size_inches(20,15)
plt.savefig('hist8.png', bbox_inches='tight')
plt.show()
#histograms of the different stats to show if they have normal distribution
```

![alt text](https://github.com/justinminsk/Pokemon-Stats/blob/master/hist8.png)
