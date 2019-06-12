
# Seaborn 

*  Seaborn is a statical plotting library 
*  It has default beautiful styles 
*  It aso is designed to work very well with pandas datafram objects 

# Distribution Plots

The distplot shows the distribution of a univariate set of observations.


```python
import seaborn as sns
```


```python
%matplotlib inline
```


```python
tips=sns.load_dataset('tips')
```


```python
tips = sns.load_dataset('tips')
```


```python
print(sns.utils.get_data_home())   # To check The Path of your Data 
```

    C:\Users\sujitd\seaborn-data
    


```python
tips.head()
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
      <th>total_bill</th>
      <th>tip</th>
      <th>sex</th>
      <th>smoker</th>
      <th>day</th>
      <th>time</th>
      <th>size</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>16.99</td>
      <td>1.01</td>
      <td>Female</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>10.34</td>
      <td>1.66</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>3</td>
    </tr>
    <tr>
      <th>2</th>
      <td>21.01</td>
      <td>3.50</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>23.68</td>
      <td>3.31</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>24.59</td>
      <td>3.61</td>
      <td>Female</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>4</td>
    </tr>
  </tbody>
</table>
</div>




```python
sns.distplot(tips['total_bill'])
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1f40e057278>




![png](https://github.com/sujitdhamale/Seaborn/blob/master/images/distplot01.png)



```python
sns.distplot(tips['total_bill'],kde=False)
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1f40ddc3be0>




![png](https://github.com/sujitdhamale/Seaborn/blob/master/images/distplot02.png)



```python
sns.distplot(tips['total_bill'],kde=False,bins=40)
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1f40dfdebe0>




![png](https://github.com/sujitdhamale/Seaborn/blob/master/images/distplot03.png)



```python
sns.distplot(tips['total_bill'],kde=False,bins=100)
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1f40e23fd68>




![png](https://github.com/sujitdhamale/Seaborn/blob/master/images/distplot04.png)


## Joints Plots
jointplot() allows you to basically match up two distplots for bivariate data. With your choice of what **kind** parameter to compare with: 
* “scatter” 
* “reg” 
* “resid” 
* “kde” 
* “hex”


```python
sns.jointplot(x='total_bill',y='tip',data=tips)
```




    <seaborn.axisgrid.JointGrid at 0x1f40e218f60>




![png](01%20Distribution%20Plots_files/01%20Distribution%20Plots_13_1.png)



```python
sns.jointplot(x='total_bill',y='tip',data=tips,kind='hex') 
```




    <seaborn.axisgrid.JointGrid at 0x1f40ded8400>




![png](01%20Distribution%20Plots_files/01%20Distribution%20Plots_14_1.png)



```python
sns.jointplot(x='total_bill',y='tip',data=tips,kind='reg') # Regression
```




    <seaborn.axisgrid.JointGrid at 0x1f40defd208>




![png](01%20Distribution%20Plots_files/01%20Distribution%20Plots_15_1.png)



```python
sns.jointplot(x='total_bill',y='tip',data=tips,kind='kde') # KDE = 2D 
```




    <seaborn.axisgrid.JointGrid at 0x1f40dd5b710>




![png](01%20Distribution%20Plots_files/01%20Distribution%20Plots_16_1.png)


## Pairplot

* plot pairwise relationship across entire datframe on NUmerical columns
* to Print categorical column in pairplot use HUE
* pairplot will plot pairwise relationships across an entire dataframe (for the numerical columns) and supports a color hue argument (for categorical columns). 


```python
sns.pairplot(tips)
```




    <seaborn.axisgrid.PairGrid at 0x1f40dcb9588>




![png](01%20Distribution%20Plots_files/01%20Distribution%20Plots_18_1.png)



```python
tips.head()
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
      <th>total_bill</th>
      <th>tip</th>
      <th>sex</th>
      <th>smoker</th>
      <th>day</th>
      <th>time</th>
      <th>size</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>16.99</td>
      <td>1.01</td>
      <td>Female</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>10.34</td>
      <td>1.66</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>3</td>
    </tr>
    <tr>
      <th>2</th>
      <td>21.01</td>
      <td>3.50</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>23.68</td>
      <td>3.31</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>24.59</td>
      <td>3.61</td>
      <td>Female</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>4</td>
    </tr>
  </tbody>
</table>
</div>




```python
sns.pairplot(tips,hue='sex')
```




    <seaborn.axisgrid.PairGrid at 0x1f40f9a1470>




![png](01%20Distribution%20Plots_files/01%20Distribution%20Plots_20_1.png)



```python
sns.pairplot(tips,hue='sex',palette='coolwarm')
```




    <seaborn.axisgrid.PairGrid at 0x1f40fe6bfd0>




![png](01%20Distribution%20Plots_files/01%20Distribution%20Plots_21_1.png)


## Rugplot
* it draw the DASH mark for every points on Univarint data 
* rugplots are actually a very simple concept, they just draw a dash mark for every point on a univariate distribution. They are the building block of a KDE plot:


```python
sns.rugplot(tips['total_bill'])
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1f4104610f0>




![png](01%20Distribution%20Plots_files/01%20Distribution%20Plots_23_1.png)



```python
sns.distplot(tips['total_bill'],kde=False)   # KDE =Kernel Density Estimates
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1f410ac0ac8>




![png](01%20Distribution%20Plots_files/01%20Distribution%20Plots_24_1.png)


## KDE plot

##### Draw KDE(Kernel Density Estimates) grapth on rugplot

kdeplots are [Kernel Density Estimation plots](http://en.wikipedia.org/wiki/Kernel_density_estimation#Practical_estimation_of_the_bandwidth). These KDE plots replace every single observation with a Gaussian (Normal) distribution centered around that value. For example:


```python
sns.kdeplot(tips['total_bill'])
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1f41073ff28>




![png](01%20Distribution%20Plots_files/01%20Distribution%20Plots_26_1.png)



```python
# Don't worry about understanding this code!
# It's just for the diagram below
import numpy as np
import matplotlib.pyplot as plt
from scipy import stats

#Create dataset
dataset = np.random.randn(25)

# Create another rugplot
sns.rugplot(dataset);

# Set up the x-axis for the plot
x_min = dataset.min() - 2
x_max = dataset.max() + 2

# 100 equally spaced points from x_min to x_max
x_axis = np.linspace(x_min,x_max,100)

# Set up the bandwidth, for info on this:
url = 'http://en.wikipedia.org/wiki/Kernel_density_estimation#Practical_estimation_of_the_bandwidth'

bandwidth = ((4*dataset.std()**5)/(3*len(dataset)))**.2


# Create an empty kernel list
kernel_list = []

# Plot each basis function
for data_point in dataset:
    
    # Create a kernel for each point and append to list
    kernel = stats.norm(data_point,bandwidth).pdf(x_axis)
    kernel_list.append(kernel)
    
    #Scale for plotting
    kernel = kernel / kernel.max()
    kernel = kernel * .4
    plt.plot(x_axis,kernel,color = 'grey',alpha=0.5)

plt.ylim(0,1)
```




    (0, 1)




![png](01%20Distribution%20Plots_files/01%20Distribution%20Plots_27_1.png)



```python
# To get the kde plot we can sum these basis functions.

# Plot the sum of the basis function
sum_of_kde = np.sum(kernel_list,axis=0)

# Plot figure
fig = plt.plot(x_axis,sum_of_kde,color='indianred')

# Add the initial rugplot
sns.rugplot(dataset,c = 'indianred')

# Get rid of y-tick marks
plt.yticks([])

# Set title
plt.suptitle("Sum of the Basis Functions")
```




    Text(0.5, 0.98, 'Sum of the Basis Functions')




![png](01%20Distribution%20Plots_files/01%20Distribution%20Plots_28_1.png)



```python

```


```python

```


```python

```
