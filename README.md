
This repository was born out of the need to create OpenCV numpy 2-D array representing
an RGB image out of a sequence of color gradient values stored as an 1-D array.

There are following questions with answers on stackoverlog related to this topic:


Algorithm for transformation of an 1-D-gradient into a special form of a 2-D-gradient :
	https://stackoverflow.com/questions/78502481/algorithm-for-transformation-of-an-1-d-gradient-into-a-special-form-of-a-2-d-gra


Reverse (flip) order of values in anti-diagonals of an non-square array without using Python loops
	https://stackoverflow.com/questions/78518903/reverse-flip-order-of-values-in-anti-diagonals-of-an-non-square-array-without


How to put a Python numpy array back together from diagonals obtained from splitting the array into right to left diagonals in first place?
	https://stackoverflow.com/questions/78501763/how-to-put-a-python-numpy-array-back-together-from-diagonals-obtained-from-split


Below an excerpt of one of these questions explaining the required arrangement of 
color entries from the 1-D color gradient array in a 2D-image: 

Assuming there is a 1-D array/list which defines a color gradient I would like to use it in 
order to create a 2-D color gradient as follows:

Let's for simplicity replace color information with a single numerical value for an example
 of an RGB color gradient 1-D array/list :

``` python
[ 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 ]
```
To keep the gradient progressing diagonally with progress of the largest next value 
diagonally over the entire array I would like to transform the 1-D sequence into a 
2D-array with deliberately chosen shape (i.e. width/height, i.e. number of rows x number
of columns where row * columns == length of the 1-D gradient array) as follows:

``` python
[[  1  2  4 ]
 [  3  6  7 ]
 [  5  9 10 ]
 [  8 12 13 ]
 [ 11 14 15 ]]
 ```
 
This special diagonal oriented mapping of the flat 1-D data to a 2-D array  is not covered 
by the in Python and numpy ready-to-use out-of-the-box methods along with building 
a 2-D array out of a list with array right-to-left diagonals. 

 