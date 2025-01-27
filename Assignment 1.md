# NAME: Konstantinos Kalogerogiannis
## EMAIL: kk05192n@pace.edu
## GROUP:
    

# Assignment 1

You may work in groups, but you must submit your own work. If you worked with others, please be sure to include their names in your submitted work. 

Be sure to **DOCUMENT your work** (points will be deducted without documentation). Always import any packages that you use at the top of your assignment. 

Be sure to includes you name and email address in the jupyter notebook that you turn in.  

Each question is worth 10 points.

Use the power of the internet when you're stuck or need to find a function to execute it. **CITE YOU WORK**

## Question 1
Please tell me what the function `np.histogram()` does in your own words. What are the required arguments and optional arguments? In your answer, tell me how you looked up the function (include links to any websites or internal function in python that you used).


### Write your answer here:

I use np.histogram() to compute the histogram of a dataset. 
Two arguments are Required --> a: array_like data and bins: integer,sequence or a string. 
The optional arguments--> *Range: I compute by "(a.(min),a.(max))" and it is the difference between the max and min values of the dataset.
                           *Weights: each value within the data contributes it's associated weight towards the bin count.
                             *Density: if FALSE, the results will contain the number of samples within each bin. If TRUE, the result will contain the value of probability density function at the bin.
I imported "numpy" package that I installed in my environment. Then I used help(np.histogram) to obtain information about the function.

## Question 2
Identify the lists below. If they are a list, explain how you know this (syntax or function that you used). If it is not a list, tell me what it is and explain how you know this.

1. np.std()
2. print(['hello', 67, 85, '25'])
3. ['fall','spring','summer','winter']
4. {'a':1, 'b':2, 'c': 3, 'd':4, 'e':5, 'g':6}
5. [[1,45],[56,89],[88,45]]
6. ('August','September', 'October','November','December')

### Write your answer here:

From numpy package that I imported:
1.) It is not a list. np.std(a) is a function located within the numpy library and calculates the standard deviation of an array of numbers from the mean. So, the output is expected as an integer or float.
2.) it is not a list, it is a function that gives as an output the list of strings and integers: ['hello',67,85,'25']. I used the type function for each of the characters.
3.) it is a list of strings
4.)it is not a list, it is a dictionary because i use {} and also it could be an unordered collection of pairs, while a list is an ordered collection of elements.
5.)it is a list of lists. Specifically, it a represents a 3x2 matrix. 3: number of rows, 2:number of columns.
6.)it is a tuple. An ordered, immutable collection of elements.





## Question 3
Write a python script using a for loop and range function that prints numbers 30 through 100 by every 10 except 70.

### Write your code here:


```python
for i in range(30,101,10):
    if i !=70:
        print(i)
    
```

    30
    40
    50
    60
    80
    90
    100


## Question 4
1. Write a python script that contains a for loop that prints 'even' and the number for every even number
2. and (in the same script) create a new list of even numbers in the series:
[1,2,3,7,9,34,56,70,90,123,136,148,156] 

    

### Write your code here:


```python
list=[1,2,3,7,9,34,56,70,90,123,136,148,156]
for i in list:
        if i%2==0:
            print("even")
            print(i)

evenlist=[num for num in list if num%2==0]
print(evenlist)
```

    even
    2
    even
    34
    even
    56
    even
    70
    even
    90
    even
    136
    even
    148
    even
    156
    [2, 34, 56, 70, 90, 136, 148, 156]


## Question 5

1. Write a while loop that calculates celsius to farenheit up to and including 38 celsius (hint: (32°F − 32) × 5/9 = 0°C)
2. How long does it take to run the script you wrote? Use python to show this.

### Write your code here:


```python
import time
starttime=time.time()
celsius=0
while celsius<=38:
    fahreneit=(9/5*celsius)+32
    print(f"{celsius} C is equal to {fahreneit} F")
    celsius+=1

endtime=time.time()
elapsedtime=endtime-starttime
print(f"time taken to write the code: {elapsedtime} seconds")
```

    0 C is equal to 32.0 F
    1 C is equal to 33.8 F
    2 C is equal to 35.6 F
    3 C is equal to 37.4 F
    4 C is equal to 39.2 F
    5 C is equal to 41.0 F
    6 C is equal to 42.8 F
    7 C is equal to 44.6 F
    8 C is equal to 46.4 F
    9 C is equal to 48.2 F
    10 C is equal to 50.0 F
    11 C is equal to 51.8 F
    12 C is equal to 53.6 F
    13 C is equal to 55.400000000000006 F
    14 C is equal to 57.2 F
    15 C is equal to 59.0 F
    16 C is equal to 60.8 F
    17 C is equal to 62.6 F
    18 C is equal to 64.4 F
    19 C is equal to 66.2 F
    20 C is equal to 68.0 F
    21 C is equal to 69.80000000000001 F
    22 C is equal to 71.6 F
    23 C is equal to 73.4 F
    24 C is equal to 75.2 F
    25 C is equal to 77.0 F
    26 C is equal to 78.80000000000001 F
    27 C is equal to 80.6 F
    28 C is equal to 82.4 F
    29 C is equal to 84.2 F
    30 C is equal to 86.0 F
    31 C is equal to 87.80000000000001 F
    32 C is equal to 89.6 F
    33 C is equal to 91.4 F
    34 C is equal to 93.2 F
    35 C is equal to 95.0 F
    36 C is equal to 96.8 F
    37 C is equal to 98.60000000000001 F
    38 C is equal to 100.4 F
    time taken to write the code: 0.0008530616760253906 seconds


## Question 6

Write a script that skips vowels from the following string: "Python is for everyone!"

Be sure that this outputs in one string or list in one line.

### Write your code here:


```python
string="Python is for everyone!"
vowels="aoeyiAOEYI"
result=''.join([char for char in string if char not in vowels])
print (result)

```

    Pthn s fr vrn!


## Question 7

Write a script with for loops that prints out every month and then prints out the total number of days in that month. 
(ie January, 31, February, 28, etc) Use for loops to do this. 


### Write your code here:


```python
import calendar
month=[('January',31),('February',28),('March',31),('April',30),('May',31),('June',30),('July',31),('August',31),('September',30),('October',31),('November',30),('December',31)]
for month,days in month:
    print(f"{month},{days}")
    
```

    January,31
    February,28
    March,31
    April,30
    May,31
    June,30
    July,31
    August,31
    September,30
    October,31
    November,30
    December,31


## Question 8
matrix_1 = np.matrix([[34,567,32,40],[95,20,32,55],[94,51,24,593],[35,526,97,393],[94,822,362,263]])

1. Slice matrix_1 to show column 2 and rows 2 through 5
2. Filter matrix_1 to show values that are between 54 through 90 (not including 54 or 90)
3. Transpose matrix_1

### Write your code here:


```python
import numpy as np
matrix_1=np.matrix([[34,567,32,40],[95,20,32,55],[94,51,24,593],[35,526,97,393],[94,822,362,263]])
print(matrix_1)
result=matrix_1[1:5,1] # index starts from 0, so 1:5-> rows 2 through -but not including- 6th row and 1 is for 2nd column
print(result)
filtered=matrix_1[(matrix_1>54) & (matrix_1<90)]
print(filtered)
newmatrix=np.transpose(matrix_1) # rows become columns
print(newmatrix)


```

    [[ 34 567  32  40]
     [ 95  20  32  55]
     [ 94  51  24 593]
     [ 35 526  97 393]
     [ 94 822 362 263]]
    [[ 20]
     [ 51]
     [526]
     [822]]
    [[55]]
    [[ 34  95  94  35  94]
     [567  20  51 526 822]
     [ 32  32  24  97 362]
     [ 40  55 593 393 263]]


## Question 9
Using the following arrays:
a = np.array([45,86,78,300,586,686,486,794,486,58,77,93,55,83,136])
b = np.array([45,67,239,555,597,264,908,562,44,58,39,57,62,58,224])

Write a python code using **numpy** that:
    1. calculates the difference between the minimum and maximum number for each earray
    2. calculates the 75th percentile for each array
    3. calculates the mean and standard deviation for each array
    4. calculates the correlation coefficient between the two arrays
    
Please document what those numbers are in your answer. 

Hint: the functions for these statistics can easily be found in the lecture slides and any reference guide to python

### Write your code here:


```python
import numpy as np
a=np.array([45,86,78,300,586,686,486,794,486,58,77,93,55,83,136])
b=np.array([45,67,239,555,597,264,908,562,44,58,39,57,62,58,224])
maxa=max(a)
mina=min(a)
print(maxa)
print(mina)
diffa=maxa-mina #range of array a
print(diffa)
maxb=max(b)
minb=min(b)
print(maxb)
print(minb)
diffb=maxb-minb #range of array b
print(diffb)
stda=np.std(a) #distance of values from the mean of array A
stdb=np.std(b) # " " of array B
print(stda)
print(stdb)
meana=np.mean(a)
meanb=np.mean(b)
print(meana)
print(meanb)
percentilea=np.percentile(a,75) #75th percentile for the distribution of values within array A.
percentileb=np.percentile(b,75) # " " array B
print(percentilea)
print(percentileb)
corrab=np.corrcoef(a,b) # the two arrays are highly correlated
print(corrab)
```

    794
    45
    749
    908
    39
    869
    255.04469325111543
    265.0120668112219
    269.93333333333334
    251.93333333333334
    486.0
    409.5
    [[1.         0.65399586]
     [0.65399586 1.        ]]


## Question 10

Use a numpy function that randomly generates numbers in an array that has the shape(8,8)

### Write your code here:


```python
import numpy as np
```


```python
array=np.random.rand(8,8)
array1=np.array(array)
```


```python
print(array1)
```

    [[0.64873266 0.19147882 0.2735474  0.78577678 0.55825675 0.36025114
      0.20187379 0.4176446 ]
     [0.57380346 0.36679997 0.29749272 0.30467419 0.49442827 0.4859062
      0.68191685 0.09282455]
     [0.50536117 0.80657968 0.94820388 0.12446771 0.41557036 0.46567101
      0.78111672 0.47742245]
     [0.64448304 0.78291658 0.41628953 0.65077535 0.854118   0.2734515
      0.75824284 0.40839481]
     [0.62145962 0.17537538 0.27638989 0.63351785 0.60051984 0.37581826
      0.44170572 0.86539699]
     [0.22593979 0.43141981 0.80248819 0.26750379 0.28950652 0.60949056
      0.78827974 0.99699447]
     [0.35145397 0.45210254 0.70676092 0.15776801 0.04131749 0.33357008
      0.58110302 0.54207943]
     [0.1804588  0.34923828 0.65681876 0.86081306 0.97749662 0.21516949
      0.4353142  0.38196606]]

