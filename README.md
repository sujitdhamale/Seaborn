# matplotlib

* matplotlib is the most popular library for python
* It give you control  over
every aspect of figure
* it was designed to have a similar feel to  MatLab's
graphical plotting

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

```python
y
```

### Using two way we can create matplotlib graph
* Functional method 
* object
oriented method

## Functional method

```python
plt.plot(x,y)
plt.show()
```

### Adding lable to graph

```python
plt.plot(x,y)
plt.xlabel("X lable")
plt.ylabel("Y Lable")
plt.title("First grap from Matplot lib")
```

### Multiplot on same canvas

```python
plt.subplot(1,2,1) # 1=Number of row  , 2= NUmer of column and #1 Number of plot you are refering to 
```

```python
plt.subplot(1,2,1) # 1=Number of row  , 2= NUmer of column and #1 Number of plot you are refering to 
plt.plot(x,y,'r-')
```

```python
plt.subplot(1,2,1) # 1=Number of row  , 2= NUmer of column and #1 Number of plot you are refering to 
plt.plot(x,y,'r-')

plt.subplot(1,2,2)
plt.plot(y,x)
```

# object oriented method

*   figure object and call the method

```python
fig =plt.figure()
```

```python
fig =plt.figure()
axes=fig.add_axes([0.1,1,0.8,0.8])  # List tabking four argument LEFT BOttom width and height 
```

```python
fig =plt.figure()
axes=fig.add_axes([0.1,1,0.8,0.8])  # List tabking four argument LEFT BOttom width and height 
axes.plot(x,y)
```

### Setting lable

```python
fig =plt.figure()
axes=fig.add_axes([0.1,1,0.8,0.8])  # List tabking four argument LEFT BOttom width and height 
axes.plot(x,y)
axes.set_xlabel("X lable ")
axes.set_ylabel("Y Lable ")
axes.set_title("Title of graph")
```

```python
fig =plt.figure()
axes1=fig.add_axes([0.1,0.1,0.8,0.8])  #LEFT BOttom width and height 
axes2=fig.add_axes([0.1,0.6,0.4,0.3])  #LEFT BOttom width and height 


```

```python
fig =plt.figure()
axes1=fig.add_axes([0.1,0.1,0.8,0.8])  #LEFT BOttom width and height 
axes2=fig.add_axes([0.7,0.1,0.2,0.2])  #LEFT BOttom width and height 

```

```python
fig =plt.figure()
axes1=fig.add_axes([0.1,0.1,0.8,0.8])  #LEFT BOttom width and height 
axes2=fig.add_axes([0.2,0.5,0.4,0.3])  #LEFT BOttom width and height 

axes1.plot(x,y)
axes2.plot(y,x)

axes1.set_title("Larger Plot")
axes2.set_title("Smaller Plot")

```

```python

```

# Subplot using Object oriented method

```python
fig,axes=plt.subplots(nrows=1,ncols=2)
```

```python
fig,axes=plt.subplots(nrows=3,ncols=3)
```

### Tight layout

```python
fig,axes=plt.subplots(nrows=3,ncols=3)
plt.tight_layout()
```

```python
axes
```

```python
type(axes)
```

```python
fig,axes=plt.subplots(nrows=1,ncols=3)
for curr_axes in  axes:
    curr_axes.plot(x,y)
```

```python
fig,axes=plt.subplots(nrows=1,ncols=3)
axes[0].plot(x,y)
```

```python
fig,axes=plt.subplots(nrows=1,ncols=3)
axes[1].plot(x,y)
axes[1].set_title("Axxess 1")

axes[0].set_title("Empty")
```

```python

```

# figure Size , aspect ratio and DPI (Dots Per Inch)

```python
fig=plt.figure(figsize=(8,2))  
ax=fig.add_axes([0,0,1,1])
ax.plot(x,y)
```

```python
fig,axes=plt.subplots(nrows=2,ncols=1,figsize=(8,2))  
axes[0].plot(x,y)
axes[1].plot(y,x)  
```

```python
fig,axes=plt.subplots(nrows=2,ncols=1,figsize=(8,2))  
axes[0].plot(x,y)
axes[1].plot(y,x)
plt.tight_layout()    # it is optionl but it is recommend to use for fixing layout and overlapping
```

# Save figure

```python
fig
```

```python
fig.savefig('My_picture.png')
```

```python
fig.savefig('My_picture1.png',dpi=200)
```

# Legned

The legend is often located on the right-hand side of the chart or
graph and is sometimes surrounded by a border. <br>
The legend is linked to the
data being graphically displayed in the plot area of the chart

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

### Legend location
https://matplotlib.org/3.1.0/api/_as_gen/matplotlib.pyplot.legend.html
Location String	Location Code<br>
'best'	0 <br>
'upper right'	1<br>
'upper left'
2<br>
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

```python
fig=plt.figure()
axes=fig.add_axes([0.1,0.1,0.8,0.8])
axes.plot(x,x**2,label="X Square")  # Label is mandatory  for legend
axes.plot(x,x**3,label="X Cube")

axes.legend(loc=(0.1,0.1))   # one more method for setting legend 
```

# Setting colour, line size , line size and cutomization

## Color

```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
#axes.plot(x,y,color='green')
axes.plot(x,y,color='#FF8C00')  #RGB HEX code 
```

# Linewidth

```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,color='purple', linewidth=10)
```

```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,color='purple', lw=10) # alternative to linewidth is "lw"
```

## Alfha argumnet to control transparnat line

```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])

axes.plot(x,y,color='green', linewidth=5)
```

```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])

axes.plot(x,y,color='green', linewidth=5,alpha=0.5)
```

## Line Style

```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,color='red',lw=5,linestyle='--')
```

```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,color='purple',lw=5,ls=':')   # Shortcut is ls for line size
```

```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,color="Green",lw=5,linestyle='steps')
```

# Markers 
* tom mark  the point in graph

```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,color='red',lw='3',marker='o')
```

```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
#axes.plot(x,y,color='purple',lw='3',marker='+')
axes.plot(x,y,color='purple',lw='1',marker='*')
```

```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,lw=2,marker='+',markersize=20)
```

```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,lw=2,marker='o',markersize=20,markerfacecolor="yellow")
```

```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,lw=2,marker='o',markersize=20,markerfacecolor="yellow",markeredgewidth=3)
```

```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,lw=2,marker='o',markersize=20,markerfacecolor="yellow",markeredgewidth=3,markeredgecolor='black')
```

# Control  over axis appearance

```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,lw=2,ls='--')
```

```python
fig=plt.figure()
axes=fig.add_axes([0,0,1,1])
axes.plot(x,y,lw=2,ls='--')
axes.set_xlim([0,1])   # Disply x till 1 
axes.set_ylim([0,2])   # Disply y till 2
```

# Special Plot Type

 #  http://dana.loria.fr/doc/tutorial.html

```python

```
