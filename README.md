# DataScience

********************************************************** Python Assingment1 *****************************************************************************
**Solution_On_Conditional_Statement**

#Take three numbers 'x', 'y' and 'z' as input from the user and check which number is greater
x=int(input("Enter First number:"))
y=int(input("Enter Second number:"))
z=int(input("Enter Third number:"))
if y<x>z:
  print("x is greater than y and z.")
elif x<y>z:
  print("y is greater than x and z.")
elif x<z>y:
  print("z is greater than x and y.")
elif x>z<y:
  print("x and y are greater than z.")
elif z>x<y:
  print("y and z are greater than x.")
elif x>y<z:
  print("x and z are greater than y.")
else:
  print("x, y and z are equal.")
            
Output- Enter First number:12
Enter Second number:13
Enter Third number:4
y is greater than x and z.
            
#Take an alphabet as input from the user and check if the alphabet is a vowel, consonant or an exception
#Vowel - 'a','e','i','o','u'
#Exception - 'h', 'y'
#Consonant - rest other alphabets
alphabet=input("Enter a alphabet:") 
vowel=['a','e','i','o','u']

Exception=['h', 'y']
if alphabet in vowel:
  print('Alphabet is a Vowel.')
elif alphabet in Exception:
  print('Alphabet is a Exception.')
else: 
  print('Alphabet is a Consonant.')
            
 Output- Enter a alphabet:h
Alphabet is a Exception.
            
#Write a program to check whether a number given by a user is divisible by 2 and 3 both 
x=int(input("Enter a number:"))
if x%2==0 and x%3==0:
    print("Number is divisible by 2 and 3 both.")
else:
  print("Number is not divisible by 2 and 3.")
Output-Enter a number:18
Number is divisible by 2 and 3 both.
            
#Write a program to accept the cost price  of a bike as input and display the road tax to be paid according to the following crieteria :-
#Cost price - 100000 Tax - 15%
#Cost price - between 50000 to 100000 Tax - 10%
#Cost price - less than 50000 Tax - 5%
cp=int(input("Enter the cost price of bike:"))
if cp==100000:
  print('Tax is 15%')
  tax=0.15*cp
  print('Tax is'+str(tax))
elif 5000<cp<100000:
  print('Tax is 10%')
  tax=0.10*cp
  print('Tax is'+str(tax))
else:
  print('Tax is 5%')
  tax=0.05*cp
  print('Tax is'+str(tax))
 Output- Enter the cost price of bike:500000
Tax is 5%
Tax is25000.0
       
##Write a program to calculate the electricity bill by accepting the number of units consumed by the user as input. Use the following price chart for reference :-
#Price of first 100 units - no charge
#Price of next 100 units - Rs 5/- per unit
#After 200 units - Rs 10/- per unit
units=int(input('Enter number of units:'))
if units<100:
  print('No charge.')
elif 200>units>100:
  extra_units=units-100
  price=extra_units*5
  print('Price is'+str(price))
else:
  price1=100*5
  extra_units=units-200
  price2=extra_units*10
  price3=price1+price2
  print('Price is'+str(price3))
Output- Enter number of units:210
Price is600

********************************************************** Python Assingment2 *****************************************************************************
**Solution_On_Assignment_on_Loops**
# Write a program which accepts month's name as input and display the number of days in the month as output
month_name=input('Enter Month name:')
month1=['January','March','May','July','August','October','December']
month2=['February']
month3=['April','June','September','November']
year=int(input('Enter number of days:'))
if month_name in month1:
  print("Number of days present in "+str(month_name)+'is :31')
elif month_name in month3:
   print("Number of days present in "+str(month_name)+' is :30')
elif month_name in month2:
  if year<366:
    print("Number of days present in "+str(month_name)+' is :28')
  else:
    print("Number of days present in "+str(month_name)+' is :29')
 Output- Enter Month name:April
Enter number of days:365
Number of days present in April is : 30
             
# Take any word as input from the user and count the number of vowels in the word
name=input("Enter any name:")
count=0
vowel=['A','E','I','O','U','a','e','i','o','u']
for i in name:
  if i in vowel:
    count=count+1
print("vowel count in name"+str(name)+" is :"+str(count))
Output- Enter any name:Ashu
vowel count in nameAshu is :2
               
# Write a program to separate even and odd numbers in two distinct lists from a list of numbers of your choice
def odd_even(list1):
  evenlist=[]
  oddlist=[]
  for i in list1:
    if i%2==0:
      evenlist.append(i)
    else:
      oddlist.append(i)
  print("Evenlist:"+str(evenlist))
  print("Oddlist:"+str(oddlist))
odd_even([2,3,5,7,8,9])
Output-Evenlist:[2, 8]
Oddlist:[3, 5, 7, 9]
               
# Write a program that appends datatype of elements from a list to a separate list

def datatypeOflist(list1):
  new_list=[]
  for i in my_list:
    new_list.append(type(i))
  print(new_list)

my_list=['India','numpy',3.12,5,88]
datatypeOflist(my_list)
O/p- [<class 'str'>, <class 'str'>, <class 'float'>, <class 'int'>, <class 'int'>]
  
## Write a program to display only those numbers from a list that satisfies the following conditions:

# The number must be divisible by 7

# If the number is 140 then skip it and move to the next number in the list

# If the number in the list is greater than 630 then stop the loop

def displayList(list1):
  for i in list1:
    if i%7==0:
      if i==140:
        continue
      elif i>630:
        break
      else:
        print(i)

displayList([2,7,8,14,28,9,111,140,147])
O/p - 
 7
14
28
147

********************************************************** Python Assingment3 *****************************************************************************
**Solution_On_Functions**
#Define a function that accepts a number and returns whether the number is even or odd.
def even_odd(num):
  if num%2==0:
    print("Number "+str(num)+' is even.')
  else:
    print("Number "+str(num)+' is odd.')
num=int(input("Enter Number:"))
even_odd(num)

Output-
Enter Number:25
Number 25 is odd.

#Define a function to create and print a list where the values are square of numbers between 1 and 30 (both included).
def square_num():
  my_list=[]
  for i in range(1,31):
    i=i**2
    my_list.append(i)
  print(my_list)
square_num()
Output-
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100, 121, 144, 169, 196, 225, 256, 289, 324, 361, 400, 441, 484, 529, 576, 625, 676, 729, 784, 841, 900]

#Define a function, shut_down, that takes one parameter. Then, if the shut_down function receives a value equal to "yes", it should print "Shutting down". 
#Alternatively, if vallue is equal to "no", then the function should print "Shutdown aborted". Finally, if shut_down gets anything other than those inputs, 
#the function should print "Sorry".
def shut_down(value):
  if value=="yes":
    print("Shutting down...")
  elif value=="no":
    print("Shutdown aborted...")
  else:
    print("Sorry")
value=input("Enter your input:")
shut_down(value)
Output-
Enter your input:yes
Shutting down...

#Define a function called "by_three" that takes a parameter called number. If that number is divisible by 3, "by_three" should print the cube of the number. 
#Otherwise, by_three should print False.
def by_three(number):
  if number%3==0:
    num=number**3
    print(num)
  else:
    print("false")
number=int(input("Enter a number:"))
by_three(number)
Output-
Enter a number:90
729000

#Define a function that takes a list and prints a new list with no duplicate elements given in the first list.
def no_duplicates(l1):
  newl1=[]
  for i in l1:
    if ',' not in i:
      mycount=l1.count(i)
      print("count of "+str(i)+" is "+str(mycount))
      if mycount==1:
        newl1.append(i)
  print(newl1)
l1=list(input("Enter numbers of elements : "))
no_duplicates(l1)
Output-
Enter numbers of elements : 1,2,2,3,5,6,7,7,8,9,0
count of 1 is 1
count of 2 is 2
count of 2 is 2
count of 3 is 1
count of 5 is 1
count of 6 is 1
count of 7 is 2
count of 7 is 2
count of 8 is 1
count of 9 is 1
count of 0 is 1
['1', '3', '5', '6', '8', '9', '0']

********************************************************** Python Assingment4 *****************************************************************************
**#Solution_On_Functions**
#Define a function that accepts a number and returns whether the number is even or odd.
def num(n):

  if n%2==0:
    print("number is even")

  else:
    print("number is odd") 
 Output-
  num(7) -> number is odd
  num(2) -> number is even
  
 #Define a function to create and print a list where the values are square of numbers between 1 and 30 (both included).
 def square():
  l=list()

  for i in range(1,31):
    l.append(i**2)
  print(l)
  o/p-
  square()
  [1, 4, 9, 16, 25, 36, 49, 64, 81, 100, 121, 144, 169, 196, 225, 256, 289, 324, 361, 400, 441, 484, 529, 576, 625, 676, 729, 784, 841, 900]
  
 #Define a function, shut_down, that takes one parameter. Then, if the shut_down function receives a value equal to "yes", it should print "Shutting down". Alternatively, if vallue is equal to "no", then the function should print "Shutdown aborted". Finally, if shut_down gets anything other than those inputs, the function should print "Sorry".
 def shut_down(s):

  if s=='yes':
    print("shutting down")
  
  elif s=='no':
    print("shutdown aborted")

  else:
    print("sorry")
  
  shut_down("yes")
  o/p- shutting down
  
 #Define a function called "by_three" that takes a parameter called number. If that number is divisible by 3, "by_three" should print the cube of the number. Otherwise, by_three should print False.
 def by_three(n):

  if n%3==0:
    print(n*n*n)

  else:
    pass
  by_three(9)
  o/p- 729
  by_three(5) -125
  
  #Define a function that takes a list and prints a new list with no duplicate elements given in the first list.
  def unique_list(l):
  x = []
  for a in l:
    if a not in x:
      x.append(a)
  print(x)
  o/p-
  unique_list([3,4,5,3,4,5,7,9])
  [3, 4, 5, 7, 9]

********************************************************** Python Assingment5 *****************************************************************************
**Solution_On_Final_assignment**
  
 #Write code to print characters from a string that are present at an even index number. For example, if your input string is "python", 
#the output characters will be (p,t,o).

word=input("Enter any string:")
print(word[::2])
 
O/P- Enter any string:python
pto
  
#Write a function that calculates the average of the elements of the list:
#elements = [5, 7, 4, 9, 2]

def avg(list1):
  sum=0
  for i in list1:
    sum=sum+i
  avg=sum/5
  print(avg)

list1=[5,7,4,9,2]
avg(list1)
  
o/p- 5.4
  
##Write a code that takes a year as input and determines whether it is a leap year or not.

def leapYear(year):
  
  if year%4==0 and year % 100 != 0:
    print("Year: " + str(year) +" is a Leap Year")
  elif year%400==0:
    print("Year: " + str(year) +" is a Leap Year")
  else:
    print("Year: " + str(year) +" is not a Leap Year")

year=int(input("Enter Year:"))
leapYear(year)
  
O/P - Enter Year:2004
Year: 2004 is a Leap Year

##Create a 1 dimensional numpy array of the first 50 even numbers. Convert this to a 10x5 numpy array and print its transpose.

import numpy as np
arr_1d=np.arange(0,100,2)
print(arr_1d)
print(arr_1d.shape)
arr_2d=arr_1d.reshape(10,5)
print(arr_2d)
print(arr_2d.T)
  
O/P - [ 0  2  4  6  8 10 12 14 16 18 20 22 24 26 28 30 32 34 36 38 40 42 44 46
 48 50 52 54 56 58 60 62 64 66 68 70 72 74 76 78 80 82 84 86 88 90 92 94
 96 98]
(50,)
[[ 0  2  4  6  8]
 [10 12 14 16 18]
 [20 22 24 26 28]
 [30 32 34 36 38]
 [40 42 44 46 48]
 [50 52 54 56 58]
 [60 62 64 66 68]
 [70 72 74 76 78]
 [80 82 84 86 88]
 [90 92 94 96 98]]
[[ 0 10 20 30 40 50 60 70 80 90]
 [ 2 12 22 32 42 52 62 72 82 92]
 [ 4 14 24 34 44 54 64 74 84 94]
 [ 6 16 26 36 46 56 66 76 86 96]
 [ 8 18 28 38 48 58 68 78 88 98]]
  
##Consider the 10x5 array created in the previous question. Find the mean of each row and column. You may use in built functions in order to 
#have a more optimal solution

#Mean of Column
mean_of_column=arr_2d.mean(axis=0)
print("Mean Of Column",mean_of_column)

#Mean of row
mean_of_row = arr_2d.mean(axis=1)
print ("Mean of Row",mean_of_row)
  
O/P - Mean Of Column [45. 47. 49. 51. 53.]
Mean of Row [ 4. 14. 24. 34. 44. 54. 64. 74. 84. 94.]

********************************************************** Data Visualization Assingment1 *****************************************************************************
**Solution_On_Data_Visualization_Assingment1**

#1.Using pandas, create a dummy dataset (of at least 6 columns and 5 rows)
import pandas as pd
import numpy  as np
dummy_data = pd.DataFrame(np.arange(0,30).reshape(5,6),index=['Student1','Student2','Student3','Student4','Student5',],columns=['Maths','English','Hindi','Physics','Computer','Science'])
print(dummy_data)
o/p-
            Maths  English  Hindi  Physics  Computer  Science
Student1      0        1      2        3         4        5
Student2      6        7      8        9        10       11
Student3     12       13     14       15        16       17
Student4     18       19     20       21        22       23
Student5     24       25     26       27        28       29

#2. Save the dataset created as a .csv file and use it in step 3
dummy_data.to_csv('Assingment1.csv')

#3. The dataset created, needs to be uploaded and visualization on such data needs to be performed
import matplotlib.pyplot as plt
import seaborn as snr
dummy_data=pd.read_csv("Assingment1.csv")

#4. Since this is the first assessment, you can keep yourselves constrained to ‘Bar Chart’, ‘Pie Chart’, ‘Histograms’ etc
#5. Make sure each of your visualization is followed with at least one line of self explanatory 
#statement which tells about some basic statistical inference which has been made by you.

#Bar Graph
dummy_data.plot(kind='bar')
# Below Bar Graph represents Students at x-axis and Marks on y-axis Of all 5 Students marks in 6 Subjects.
# Blue line represents Maths.
# Orange line represents English.
# Green line represents Hindi.
# Red line represents Physics.
# Purple line represents Computer.
# Brown line represents Science.
O/P- 
<matplotlib.axes._subplots.AxesSubplot at 0x7fbd05dc09d0>
Graph will be drawn

#Bar Graph
dummy_data['Physics'].plot(kind='hist')
# Below Bar Graph represents Students Marks at x-axis and frequency on y-axis Of all 5 Students marks in 6 Subjects.
# Blue line represents Physics Subject marks of 5 students in class.
O/P- <AxesSubplot:ylabel='Frequency'>
Graph will be drawn

#Pie Graph
dummy_data = pd.DataFrame(np.arange(0,30).reshape(5,6),index=['0','1','2','3','4'],columns=['Maths','English','Hindi','Physics','Computer','Science'])
dummy_data.iloc[0:3].plot.pie(subplots=True,figsize=(10,10),fontsize=20,autopct='%.2f')
# Below Bar Graph represents marks obtained by 2nd Student in 6 Subjects.
O/P-array([<matplotlib.axes._subplots.AxesSubplot object at 0x7fbd039d90a0>,
       <matplotlib.axes._subplots.AxesSubplot object at 0x7fbd039a4ca0>,
       <matplotlib.axes._subplots.AxesSubplot object at 0x7fbd039d0eb0>,
       <matplotlib.axes._subplots.AxesSubplot object at 0x7fbd0398b040>,
       <matplotlib.axes._subplots.AxesSubplot object at 0x7fbd03931d00>,
       <matplotlib.axes._subplots.AxesSubplot object at 0x7fbd038e9280>],
      dtype=object)
  Graph will be drawn.

********************************************************** Data Visualization Assingment2 *****************************************************************************
****Solution_On_Data_Visualization_Assingment2****

#1. Use the FITBIT Dataset shared for Data Visualization
#2. You are free to make as many visualization as you wish, right from scatter plot to Box plot, 
Violin plot, Swarm plot and whatever comes to your mind
#3. Make sure each of your visualization is followed with at least one line of self explanatory 
statement which tells about some basic statistical inference which has been made by you.

import pandas as pd
import numpy  as np
import matplotlib.pyplot as plt
import seaborn as snr

FitBit_data=pd.read_csv("/content/FitBit data.csv")

#line graph
ax=FitBit_data.plot(figsize=(10,10),title='FitBit_data')
ax.set_xlabel('x axis') #total number of rows in the iris dataset
ax.set_ylabel('y axis') #highest magnitude of numerical variables 
O/P- Graph will be drawn

#Bar Graph
FitBit_data.plot(kind="bar")
O/P- Graph will be drawn

#Histograph
FitBit_data.plot(kind="hist",bins=200)
O/P- Graph will be drawn

#Scatter Plot
FitBit_data.plot.scatter(x='TotalSteps',y='Calories',color='g')
O/P- Graph will be drawn

#Relational Plot
snr.relplot(x='TotalDistance', y='Calories',data=FitBit_data)
O/P- Graph will be drawn

#Cat Plot
snr.catplot(x='TotalSteps', y='Calories',data=FitBit_data)
O/P- Graph will be drawn

#Box Plot
snr.boxplot(x='TotalSteps', y='Calories',data=FitBit_data)
O/P - Graph will be drawn

********************************************************** Data Visualization Assingment3 *****************************************************************************
****Solution_On_Data_Visualization_Assingment3****

1. Use the Titanic Dataset which is already available in Seaborn library for Data Visualization
2. You are free to make as many visualization as you wish, right from scatter plot to Box plot, 
Violin plot, Swarm plot and whatever comes to your mind
3. Make sure each of your visualization is followed with at least one line of self explanatory 
statement which tells about some basic statistical inference which has been made by you.
Step 3 is optional and if you wish to share and get verified your output (with insights collected)
you can mail me the same at assimilate.ai03@gmail.com

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as snr

titanic=snr.load_dataset('titanic')

#Line Graph
ax=titanic.plot(figsize=(10,10),title='Titanic')
ax.set_xlabel('x axis')
ax.set_ylabel('y axis')
#Here, In line Graph drawn below represents titanic data.
# Blue line represents Survived Peoples.
# Orange line represents pclass.
# Green line represents age.
# Red line represents sibsp.
# Purple line represents parch.
# Brown line represents fare.
O/P - Graph willbe drawn.

#Bar Graph
titanic.plot(kind='bar')
# Below Bar Graph represents titanic ship details.
O/P - Graph will be drawn.

#Histogram
titanic.plot(kind="hist",bins=200)
# Below HistoGram represents titanic ship details.

#Scatter Plot
titanic.plot.scatter(x='age',y='fare',color='g')
# Below Scatter Plot Graph represents age vs fare titanic ship details.
O/P - Graph will be drawn

#Relational Plot
snr.relplot(x='age',y='fare',data=titanic)
O/P - Graph will be drawn.

#Cat Plot
snr.catplot(x='age',y='fare',data=titanic)
O/P - Graph will be drawn

#Box Plot
snr.boxplot(x='age',y='fare',data=titanic)
O/P - Graph will be drawn

#Violin Plot
snr.violinplot(x='age',y='fare',data=titanic)
O/P - Graph will be drawn

#Swarm Plot
snr.swarmplot(x='age',y='fare',data=titanic)
O/P - Graph will be drawn
