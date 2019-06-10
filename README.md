
# matplotlib

* matplotlib is the most popular library for python
* It give you control  over every aspect of figure
* it was designed to have a similar feel to  MatLab's graphical plotting

### Official website https://matplotlib.org/ 


```python
import matplotlib.pyplot as plt
%matplotlib inline
```


```python
import numpy as np
x=np.linspace(0,5,11)
y=x **2
```


```python
x
```




    array([ 0. ,  0.5,  1. ,  1.5,  2. ,  2.5,  3. ,  3.5,  4. ,  4.5,  5. ])




```python
y
```




    array([  0.  ,   0.25,   1.  ,   2.25,   4.  ,   6.25,   9.  ,  12.25,
            16.  ,  20.25,  25.  ])



### Using two way we can create matplotlib graph
* Functional method 
* object oriented method


## Functional method 


```python
plt.plot(x,y)
plt.show()
```


![png](README_files/README_8_0.png)


### Adding lable to graph


```python
plt.plot(x,y)
plt.xlabel("X lable")
plt.ylabel("Y Lable")
plt.title("First grap from Matplot lib")
```




    Text(0.5, 1.0, 'First grap from Matplot lib')




![png](README_files/README_10_1.png)


### Multiplot on same canvas 


```python
plt.subplot(1,2,1) # 1=Number of row  , 2= NUmer of column and #1 Number of plot you are refering to 
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1976fc31898>




![png](README_files/README_12_1.png)



```python
plt.subplot(1,2,1) # 1=Number of row  , 2= NUmer of column and #1 Number of plot you are refering to 
plt.plot(x,y,'r-')
```




    [<matplotlib.lines.Line2D at 0x19773201c18>]




![png](README_files/README_13_1.png)



```python
plt.subplot(1,2,1) # 1=Number of row  , 2= NUmer of column and #1 Number of plot you are refering to 
plt.plot(x,y,'r-')

plt.subplot(1,2,2)
plt.plot(y,x)
```




    [<matplotlib.lines.Line2D at 0x197736c5da0>]




![png](README_files/README_14_1.png)


# object oriented method

*   figure object and call the method 


```python
fig =plt.figure()
```


    <Figure size 432x288 with 0 Axes>



```python
fig =plt.figure()
axes=fig.add_axes([0.1,1,0.8,0.8])  # List tabking four argument LEFT BOttom width and height 
```


![png](README_files/README_17_0.png)



```python
fig =plt.figure()
axes=fig.add_axes([0.1,1,0.8,0.8])  # List tabking four argument LEFT BOttom width and height 
axes.plot(x,y)
```




    [<matplotlib.lines.Line2D at 0x19774ab3e48>]




![png](README_files/README_18_1.png)


### Setting lable


```python
fig =plt.figure()
axes=fig.add_axes([0.1,1,0.8,0.8])  # List tabking four argument LEFT BOttom width and height 
axes.plot(x,y)
axes.set_xlabel("X lable ")
axes.set_ylabel("Y Lable ")
axes.set_title("Title of graph")
```




    Text(0.5, 1.0, 'Title of graph')




![png](README_files/README_20_1.png)



```python
fig =plt.figure()
axes1=fig.add_axes([0.1,0.1,0.8,0.8])  #LEFT BOttom width and height 
axes2=fig.add_axes([0.1,0.6,0.4,0.3])  #LEFT BOttom width and height 


```


![png](README_files/README_21_0.png)



```python
fig =plt.figure()
axes1=fig.add_axes([0.1,0.1,0.8,0.8])  #LEFT BOttom width and height 
axes2=fig.add_axes([0.7,0.1,0.2,0.2])  #LEFT BOttom width and height 

```


![png](README_files/README_22_0.png)



```python
fig =plt.figure()
axes1=fig.add_axes([0.1,0.1,0.8,0.8])  #LEFT BOttom width and height 
axes2=fig.add_axes([0.2,0.5,0.4,0.3])  #LEFT BOttom width and height 

axes1.plot(x,y)
axes2.plot(y,x)

axes1.set_title("Larger Plot")
axes2.set_title("Smaller Plot")

```




    Text(0.5, 1.0, 'Smaller Plot')




![png](README_files/README_23_1.png)



```python

```

# Subplot using Object oriented method


```python
fig,axes=plt.subplots(nrows=1,ncols=2)
```


![png](README_files/README_26_0.png)



```python
fig,axes=plt.subplots(nrows=3,ncols=3)
```


![png](README_files/README_27_0.png)


### Tight layout 


```python
fig,axes=plt.subplots(nrows=3,ncols=3)
plt.tight_layout()
```


![png](README_files/README_29_0.png)



```python
axes
```




    array([[<matplotlib.axes._subplots.AxesSubplot object at 0x00000197783E9358>,
            <matplotlib.axes._subplots.AxesSubplot object at 0x000001977841D6A0>,
            <matplotlib.axes._subplots.AxesSubplot object at 0x00000197783F8908>],
           [<matplotlib.axes._subplots.AxesSubplot object at 0x00000197783D5AC8>,
            <matplotlib.axes._subplots.AxesSubplot object at 0x000001977846A390>,
            <matplotlib.axes._subplots.AxesSubplot object at 0x00000197784915C0>],
           [<matplotlib.axes._subplots.AxesSubplot object at 0x00000197784B97F0>,
            <matplotlib.axes._subplots.AxesSubplot object at 0x00000197784E29E8>,
            <matplotlib.axes._subplots.AxesSubplot object at 0x000001977850AC50>]], dtype=object)




```python
type(axes)
```




    numpy.ndarray




```python
fig,axes=plt.subplots(nrows=1,ncols=3)
for curr_axes in  axes:
    curr_axes.plot(x,y)
```


![png](README_files/README_32_0.png)



```python
fig,axes=plt.subplots(nrows=1,ncols=3)
axes[0].plot(x,y)
```




    [<matplotlib.lines.Line2D at 0x1977524e208>]




![png](README_files/README_33_1.png)



```python
fig,axes=plt.subplots(nrows=1,ncols=3)
axes[1].plot(x,y)
axes[1].set_title("Axxess 1")

axes[0].set_title("Empty")
```




    Text(0.5, 1.0, 'Empty')




![png](README_files/README_34_1.png)



```python

```

# figure Size , aspect ratio and DPI (Dots Per Inch)


```python
fig=plt.figure(figsize=(8,2))  
ax=fig.add_axes([0,0,1,1])
ax.plot(x,y)
```




    [<matplotlib.lines.Line2D at 0x19774f6ebe0>]




![png](README_files/README_37_1.png)



```python
fig,axes=plt.subplots(nrows=2,ncols=1,figsize=(8,2))  
axes[0].plot(x,y)
axes[1].plot(y,x)  
```




    [<matplotlib.lines.Line2D at 0x19778f1e400>]




![png](README_files/README_38_1.png)



```python
fig,axes=plt.subplots(nrows=2,ncols=1,figsize=(8,2))  
axes[0].plot(x,y)
axes[1].plot(y,x)
plt.tight_layout()    # it is optionl but it is recommend to use for fixing layout and overlapping
```


![png](README_files/README_39_0.png)


# Save figure


```python
fig
```




![png](README_files/README_41_0.png)




```python
fig.savefig('My_picture.png')
```


```python
fig.savefig('My_picture1.png',dpi=200)
```

# Legned

The legend is often located on the right-hand side of the chart or graph and is sometimes surrounded by a border. <br>
The legend is linked to the data being graphically displayed in the plot area of the chart


```python
fig =plt.figure()
axes=fig.add_axes([0.1,1,0.8,0.8])  # List tabking four argument LEFT BOttom width and height 
axes.plot(x,y)
axes.set_xlabel("X lable ")
axes.set_ylabel("Y Lable ")
axes.set_title("Title of graph")
```


```python
fig=plt.figure()
axes=fig.add_axes([0.1,0.1,0.8,0.8])
axes.plot(x,x**2,label="X Square")  # Label is mandatory  for legend
axes.plot(x,x**3,label="X Cube")

axes.legend()
```




    <matplotlib.legend.Legend at 0x19777f788d0>




![png](README_files/README_46_1.png)


### Legend location https://matplotlib.org/3.1.0/api/_as_gen/matplotlib.pyplot.legend.html


Location String	Location Code<br>
'best'	0 <br>
'upper right'	1<br>
'upper left'	2<br>
'lower left'	3<br>
'lower right'	4<br>
'right'	5<br>
'center left'	6<br>
'center right'	7<br>
'lower center'	8<br>
'upper center'	9<br>
'center'	10<br>


```python
fig=plt.figure()
axes=fig.add_axes([0.1,0.1,0.8,0.8])
axes.plot(x,x**2,label="X Square")  # Label is mandatory  for legend
axes.plot(x,x**3,label="X Cube")

axes.legend(loc=10)
```




    <matplotlib.legend.Legend at 0x197781f6ba8>




![png](README_files/README_48_1.png)



```python
fig=plt.figure()
axes=fig.add_axes([0.1,0.1,0.8,0.8])
axes.plot(x,x**2,label="X Square")  # Label is mandatory  for legend
axes.plot(x,x**3,label="X Cube")

axes.legend(loc=(0.1,0.1))   # one more method for setting legend 
```




    <matplotlib.legend.Legend at 0x19778081be0>




![png](README_files/README_49_1.png)


# Setting colour, line size , line size and cutomization 

## Color


```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
#axes.plot(x,y,color='green')
axes.plot(x,y,color='#FF8C00')  #RGB HEX code 
```




    [<matplotlib.lines.Line2D at 0x19776a3a630>]




![png](README_files/README_52_1.png)


# Linewidth


```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,color='purple', linewidth=10)
```




    [<matplotlib.lines.Line2D at 0x1977863e0f0>]




![png](README_files/README_54_1.png)



```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,color='purple', lw=10) # alternative to linewidth is "lw"
```




    [<matplotlib.lines.Line2D at 0x197786b22e8>]




![png](README_files/README_55_1.png)


## Alfha argumnet to control transparnat line


```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])

axes.plot(x,y,color='green', linewidth=5)
```




    [<matplotlib.lines.Line2D at 0x19776659160>]




![png](README_files/README_57_1.png)



```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])

axes.plot(x,y,color='green', linewidth=5,alpha=0.5)
```




    [<matplotlib.lines.Line2D at 0x197787717b8>]




![png](README_files/README_58_1.png)


## Line Style


```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,color='red',lw=5,linestyle='--')
```




    [<matplotlib.lines.Line2D at 0x1977b4fa6d8>]




![png](README_files/README_60_1.png)



```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,color='purple',lw=5,ls=':')   # Shortcut is ls for line size
```




    [<matplotlib.lines.Line2D at 0x1977cb1db70>]




![png](README_files/README_61_1.png)



```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,color="Green",lw=5,linestyle='steps')
```




    [<matplotlib.lines.Line2D at 0x1977cb7da58>]




![png](README_files/README_62_1.png)


# Markers 
* tom mark  the point in graph


```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,color='red',lw='3',marker='o')
```




    [<matplotlib.lines.Line2D at 0x1977cd8d9e8>]




![png](README_files/README_64_1.png)



```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
#axes.plot(x,y,color='purple',lw='3',marker='+')
axes.plot(x,y,color='purple',lw='1',marker='*')
```




    [<matplotlib.lines.Line2D at 0x1977d0d9fd0>]




![png](README_files/README_65_1.png)



```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,lw=2,marker='+',markersize=20)
```




    [<matplotlib.lines.Line2D at 0x1977e1c4390>]




![png](README_files/README_66_1.png)



```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,lw=2,marker='o',markersize=20,markerfacecolor="yellow")
```




    [<matplotlib.lines.Line2D at 0x1977e20f518>]




![png](README_files/README_67_1.png)



```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,lw=2,marker='o',markersize=20,markerfacecolor="yellow",markeredgewidth=3)
```




    [<matplotlib.lines.Line2D at 0x1977d0c4208>]




![png](README_files/README_68_1.png)



```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,lw=2,marker='o',markersize=20,markerfacecolor="yellow",markeredgewidth=3,markeredgecolor='black')
```




    [<matplotlib.lines.Line2D at 0x1977e32b390>]




![png](README_files/README_69_1.png)


# Control  over axis appearance 


```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,lw=2,ls='--')
```




    [<matplotlib.lines.Line2D at 0x197769de400>]




![png](README_files/README_71_1.png)



```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,lw=2,ls='--')
axes.set_xlim([0,1])   # Disply x till 1 
axes.set_ylim([0,2])   # Disply y till 2
```




    (0, 2)




![png](README_files/README_72_1.png)


# Special Plot Type

 #  http://dana.loria.fr/doc/tutorial.html


```python

```
