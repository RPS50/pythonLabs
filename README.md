# pythonLabs



00:08:11 How Python Code Gets Executed 
print("RPS")
print("o----")
print(" ||||")
print("*" * 10) #  <--an expression creates a value.  In this case 10 asterics


00:11:24 How Long It Takes To Learn Python 
3 months for basics and 6 for specialized.  Call it a year.

00:13:03 Variables 
price = 10  # <--- price is a variable and you are setting it to 10
print(price)

when you run this you get:
"D:\my'stuff\Training\Free Code Camp\LearnPythonWithMosh\PyCharmFiles\venv\Scripts\python.exe" "D:\my'stuff\Training\Free Code Camp\LearnPythonWithMosh\PyCharmFiles\app.py" 
10

Process finished with exit code 0  ← this means the code ran and you have no errors.

price = int(10)  # <--- price is a variable and you are setting it to 10
print(price)
rating = 4.9
name = "scott"
is_published = True
price = 20
print(price)


"D:\my'stuff\Training\Free Code Camp\LearnPythonWithMosh\PyCharmFiles\venv\Scripts\python.exe" "D:\my'stuff\Training\Free Code Camp\LearnPythonWithMosh\PyCharmFiles\app.py" 
10
20

Process finished with exit code 0

first_name = "John"
last_name = "Smith"
age = 20
is_new = True
print(f"Is {first_name} {last_name}, {age} years of age a new patient? {is_new}.")

Is John Smith, 20 years of age a new patient? True.

Process finished with exit code 0

00:18:21 Receiving Input 

name = input("What is your name? ")
print("Hi " + name)  #<--this expression concatenates 2 strings.
What is your name? Scott
Hi Scott

Process finished with exit code 0

name = input("What is your name? ")
color = input ("What is your favorite color? ")
print(name + " likes the color " + color + ".")  #<--this expression concatenates 2 strings.

What is your name? Scott
What is your favorite color? blue
Scott likes the color blue

Process finished with exit code 0

00:22:16 Python Cheat Sheet 
	Python cheat sheet: http://bit.ly/2Gp80s6 

00:22:46 Type Conversion 
birth_year = input("Birth year:  ")
age = 2023 - birth_year
print(age)

Birth year:  1959
Traceback (most recent call last):
  File "D:\my'stuff\Training\Free Code Camp\LearnPythonWithMosh\PyCharmFiles\app.py", line 2, in <module>
    age = 2023 - birth_year
          ~~~~~^~~~~~~~~~~~
TypeError: unsupported operand type(s) for -: 'int' and 'str'

Process finished with exit code 1
this is because we are trying to subtract a string from and integer.

birth_year = input("Birth year:  ")
print(type(birth_year))
age = 2023 - int(birth_year)
int()
float()
bool()
print(age)
print(type(age))

Birth year:  1959
<class 'str'>
64
<class 'int'>

Process finished with exit code 0

weight = input("Please enter your weight in pounds: ")
weight_in_Kilos = float(weight) * 0.45359237
print("Your weight in Kilos is:  " + str(weight_in_Kilos))

Please enter your weight in pounds: 128
Your weight in Kilos is:  58.05982336


00:29:31 Strings 
course = "Python"
print(course)

Python

Process finished with exit code 0

course = 'Python'
print(course)

Python

Process finished with exit code 0

course = '''
Hi John,

Here is our first email to you

thank you, 
the Support team


'''
print(course)
Hi John,

Here is our first email to you

thank you, 
the Support team
course = 'Python for Beginers'
print(course[-2])
r

course = 'Python for Beginers'
#         0123
print(course[0:3])

Pyt

Process finished with exit code 0

course = 'Python for Beginers'
#         0123
print(course[0:])
Python for Beginers

course = 'Python for Beginers'
#         0123
another = course[:]
print(course[:5])
print(another)
Pytho
Python for Beginers

course = 'Python'
#         0123
another = course[:]
print(course[:5])
print(another)
print(course[-1])
print(course[-2])
print(course[0:3])
print(course[0:])
print(course[:5])
print(another)
name = "Jennifer"
print(name[1:-1])



00:37:36 Formatted Strings 

first_name = "John"
last_name = "Smith"

#John Smith is a coder

message = first_name + " [" + last_name + "] is a coder."
print(message)
John [Smith] is a coder.

Process finished with exit code 0

first_name = "John"
last_name = "Smith"

#John Smith is a coder

message = first_name + " [" + last_name + "] is a coder."
msg = f"{first_name} [{last_name}] is a coder"
print(message)
print(msg)
"D:\my'stuff\Training\Free Code Camp\LearnPythonWithMosh\PyCharmFiles\venv\Scripts\python.exe" "D:\my'stuff\Training\Free Code Camp\LearnPythonWithMosh\PyCharmFiles\app.py" 
John [Smith] is a coder.
John [Smith] is a coder

Process finished with exit code 0

00:40:50 String Methods 
course = "Python for Pros"
print(len(course))
20  ←--this is the result

course = "Python for Pros"
print(len(course))
course.upper()  #<--method
print(course.upper()) #<-- prints it all in upper case
print(course) #<-- but doesn't alter the original
PYTHON FOR Pros
Python for Pros

course = "Python for Pros"
print(len(course))
course.upper()  #<--method
print(course.upper()) #<-- prints it all in upper case
print(course.lower()) #<-- prints it all in lower case
print(course) #<-- but doesn't alter the original
print(course.find("o"))  #<---o is the 5th letter
print(course.replace("P","J"))
print("Python" in course)
print("python" in course)  #<--- this produces sa boolean value.  Do we have it or not?  Remember case sensitiviety
len()
course.upper()
course.lower()
course.title()
course.find()
course.replace()
"..." in course

20
PYTHON FOR Pros
python for Pros
Python for Pros
4
Jython for Pros
True
False

00:48:33 Arithmetic Operations 

print(10+3)
print(10 / 3)
print(10 // 3)
print(10 % 3)
print(10 ** 3)
13
3.3333333333333335
3
1
1000
x = 10
print(x)
x = x+ 3
print(x)
x += 3
print(x)
x -= 3
print(x)
10
13
16
13

00:51:33 Operator Precedence 
x = 10 + 3 * 2 #←--remember multiplication comes bef
print(x)
16
x = 10 + 3 * 2 ** 2
print(x)
# 1) exponentiation 2 ** 3
# 2) multiplication or division
# 3) addition or subtraction
22
 = (10 + 3) * 2 ** 2
print(x)
# 0) Parenthesis
# 1) exponentiation 2 ** 3
# 2) multiplication or division
# 3) addition or subtraction
52
x = (2+3) * 10 - 3
print(x)
47


00:55:04 Math Functions 
import math

print(math.ceil(2.9))

x = 2.9
print(round(x))
print(abs(-2.9))

3
3
2.9
the math functions page is here:  https://docs.python.org/3/library/math.html


00:58:17 If Statements 

is_hot = False
is_cold = True

if is_hot:
    print("It's a hot day")
    print("Drink plenty of water")
elif is_cold:
    print("It's a cold day")
    print("Wear warm clothes")
else:
    print("It's a lovely day")
print("Enjoy your day")


It's a cold day
Wear warm clothes
Enjoy your day
house_price = 1000000
good_credit = True


if good_credit:
    print("You need to put down 10%")
    good_down_payment = house_price * .10
    print("$" + str(good_down_payment))
else:
    if good_credit != True:
        print("You need to put down 20%")
        high_down_payment = house_price * .20
        print("$" + str(high_down_payment))
print("Enjoy your day")
You need to put down 10%
$100000.0
Enjoy your day
house_price = 1000000
good_credit = False

if good_credit:
    print("You need to put down 10%")
    down_payment = house_price * .10
    print("$" + str(down_payment))
else:
        print("You need to put down 20%")
        down_payment = house_price * .20
        print(F"Down payment: ${down_payment}")
print("Enjoy your day")
You need to put down 20%
Down payment: $200000.0
Enjoy your day
house_price = 1000000
good_credit = True

if good_credit:
    print("You need to put down 10%")
    down_payment = house_price * .10
    print("$" + str(down_payment))
else:
        print("You need to put down 20%")
        down_payment = house_price * .20
        print(F"Down payment: ${down_payment}")
print("Enjoy your day")
You need to put down 10%
$100000.0
Enjoy your day


01:06:32 Logical Operators 
has_high_income = True
has_good_credit = True

#AND:  both
#OR:  at least one
#NOT

if has_high_income and has_good_credit: #<-- both must be true
    print("and says: Eligible for loan")

if has_high_income or has_good_credit:  #<-- one or the other must be true
    print("or says: Eligible for loan")
and says: Eligible for loan
or says: Eligible for loan
has_good_credit = True
has_criminal_record = True

if has_good_credit and not has_criminal_record:
    print("and says: Eligible for loan")

#AND:  both
#OR:  at least one
#NOT  <-- in the case above it takes a positive and flips it negative, he had a crim record so was not eligible
<this one gives you nothing as he has a criminal record

01:11:25 Comparison Operators  (oh, by the way in Pycharm Ctrl + / will comment a line and shift F10 will run your code)

temperature = 30
# <
# >
# =
# <=
# >=
# !=  is not equal
# ==


if temperature == 35:
    print("it's a hot day")
else:
    print("It's not a hot day")

It's not a hot day

#assignment
name = input("write your name:  ")
name_length = len(name)
if(name_length) < 3:
    print("use a longer version of your name")
elif(name_length) > 50:
    print("use a shorter version of your name")
else:
    print("name looks good!")

# 	print("name must be at least 3 characters long. ")
# elif it's more than 50 character long
#  	name can be a maximum of 50 characters
# otherwise
#    name looks good!

#solution
name = "Scott"

print(len(name))
if len(name)< 3:
    print("Name must be at least 3 characters:  ")
elif len(name) > 50:
    print("Name must be a max. of 50 characters.  Write something shorter.  ")
else:
    print("Name looks good!")
so I took a slightly different approach

01:16:17 Weight Converter Program 



01:20:43 While Loops 

01:24:07 Building a Guessing Game 

01:30:51 Building the Car Game 

01:41:48 For Loops 

01:47:46 Nested Loops 

01:55:50 Lists 

02:01:45 2D Lists 

02:05:11 My Complete Python Course 

02:06:00 List Methods 

02:13:25 Tuples 

02:15:34 Unpacking 

02:18:21 Dictionaries 

02:26:21 Emoji Converter 

02:30:31 Functions 

02:35:21 Parameters 

02:39:24 Keyword Arguments 

02:44:45 Return Statement 

02:48:55 Creating a Reusable Function 

02:53:42 Exceptions 

02:59:14 Comments 

03:01:46 Classes 

03:07:46 Constructors 

03:14:41 Inheritance 

03:19:33 Modules 

03:30:12 Packages 

03:36:22 Generating Random Values 

03:44:37 Working with Directories 

03:50:47 Pypi and Pip 

03:55:34 Project 1: Automation with Python
 
04:10:22 Project 2: Machine Learning with Python 

04:58:37 Project 3: Building a Website with Django




