Day 1: Baseline Quiz
====

## Intro

Some of the questions below are short-answer questions, others require some coding. Some of the short-answer questions may require you to write some code to explain yourself.

Please take your time with this quiz, there is no rush. While we generally strongly encourage you to use Google to answers questions on a very regular basis, please do your best to complete this quiz without any external assistance from Google or from the CodingNomads online platform.

When you have finished, or gotten as far as you can, please email your quiz to yurigorokhov@gmail.com and ryan@codingnomads.co. After everyone has completed the quiz and emailed their results to Yuri and Ryan we will discuss the quiz as a class.

## Git & GitHub

- What is Git?  ### Git is a version control system.
- What is GitHub? ### Github is an online collaborative workplace where everyone can upoload their code/projects and collaborate.
- Please list all the Git commands you can think of, and explain what each of the commands does.
    ### git init -- creates a git repository
    ### git status --  gets to know the status
    ### git commit -- creates s git commit
    ### git push -- pushes the files in the commit
- What is the general git workflow for a developer on a day-to-day basis?
    ### write code -->  check code -->  commit to git --> push to github or other repository
- Is it important to push your work to GitHub every day?
    ### I think it depends.  But may be safe to do so.

## Python Basics

- Name 5 python keywords.
   ### AND
   ### IF
   ### OR
   ### FALSE
   ### TRUE
- Describe the difference between a `statement` and an `expression`. Provide an example of each.
    ###(I LOOKED UP) expressions -- an expression evaluates to a value : print(1 + 2)
    ###(I LOOKED UP)  statement -- a statement performs an action:  if a > b
- Name the primitive python datatypes (as many as you can think of), and provide a declaration of each.
    ### Integers --> 1
    ### Floats --> 1.0
    ### Strings --> Hello
- Convert a floating point to an integer
```a = 1.0
b = int(a)
print(type(b))```

- Name some complex python data structures. Specify why and when you would use these.
    ### List --> mutable
    ### Tuple --> unmutable
    ### Dictionary --> have keys and are mutable
    ### Set --> if you want unique values
- Write a `for` loop and a `while` loop
``` for i in range(0, 10):
        print(i)

a = 1.0
while a > 10:
    a =+ 1
print(a)```

    - When would you prefer one over the other?
        ### For loops are good for a range; while loops are good to do "while" a check is happening.

## Functions
- What is a function? Define a simple function. (One that adds two numbers for example)
    ### A function is pre-defined code that executes automatically.
``` def addme(a, b):
        return a + b
print(addme(1, 10))```

- When a variable is declared inside a function, what scope does it have?\
    ### The scope is limited within the function itself.
- Describe variable shadowing and how it applies to functions (use code to explain yourself if appropriate)
    ### (I LOOKED UP) when a variable within a function is also defined outside of the said function.
- What are first class functions? Provide a code example of first class functions being used.
    ### (I LOOKED UP)  I do not know.
- What does the return keyword do
    ### It closes the argument
- [Optional] - What is pass by reference vs pass by value? When would you use one over the other?
    ### Pass by value means that a value is actually used in the calculation.  Vs. Pass by by reference means that you are referencing a value via a variable, etc...


## OOP
- What is object oriented programing. Why use it?
    ### (I LOOKED UP) -- programming where programmers define not only data type but also types of operations
- What is the difference between a function and a method?
    ### they are the same.  But a method is a function within a class
- Write and use a simple class that contains: a constructor, an instance variable, an instance method.
### (I LOOKED UP)```
class Human:
    hair = "brown"

new_human = Human()
print(new_human.hair)```

- Describe inheritance. Why use it?
    ### Inheritance allows you to create a new "child" class that inherits from another already established class.
- What does is to mean to "override" a function?
    ### (I LOOKED UP) -- i forgot this one...
- What is `self`
    ### Self is the way to define attributes to a class.  For example, self.name = name
- What is polymorphism?
    ### (I LOOKED UP) -- i forgot this one...

## Error handling
- Unfortunately programs do not always run perfectly. What type of errors might occur in a program?
    ### ValueError, IndexError, etc...
- How does python handle reporting and handling of these errors?
    ### Python will return which type of error is flagged.  Then based on this you can adjust your code.
- [Optional] what are other ways to handle errors?
    ### You can also create an exception, where either the error is bypassed or a specific text is returned when an error happens.
- Give an example of when you would throw an exception. (write code)
     ### (I LOOKED UP) --
```while True:
...     try:
...         x = int(input("Please enter a number: "))
...         break
...     except ValueError:
...         print("Oops!  That was no valid number.  Try again...")```
- Give a code example of how you would handle the exception above.
    ### See above, which I got from the internet
- What is "Pbd"? How do we use it?
    ### Python debugger.  In Pycharm there is a little green bug that you can click on.

## List comprehensions/generators

- Generate the following array with list comprehensions:
    - `[2, 4, 6, 8, 10, 12, 14, 16, 18]`
```x = []
for num in range(1, 10):
    x.append(num * 2)
print(x)```

    - `[2, 4, 8, 16, 32, 64, 128, 256, 512]`
- What is the difference between:
    - `[x for x in range(10)]`
    - `(x for x in range(1, 10))`
    ### In the second example you exclude 0.

## Databases

- What is a primary key?
    ### Primary key is a unique identifier within a a table.
- What is a foreign key?
    ### A foreign key is a unique varible within a table that links to another table
- How do we avoid releating and redundant data in relational databases?
    ### I do not know sir.
- What is a relational database?
    ### A relational database is a database made of tables that can link together?
- What makes a database relational?
    ### I believe it is the linkages between tables.
- Write a simple database schema (make up your own). Write a simple `SELECT`, `INSERT` and `DELETE` query against your schema. Make sure they actually work.
    ### Select * from Sakila.actor
    ### (I FORGOT) -- Insert Into sakila.actor first_name VALUES ("jesus")
    ### (I FORGOT) --  Delete from sakila.actor WHERE first_name = "jesus"
- Given the following schema:

```sql
CREATE TABLE IF NOT EXISTS employees (
    employee_id decimal(6,0) NOT NULL PRIMARY KEY,
    first_name varchar(20) DEFAULT NULL,
    last_name varchar(25) NOT NULL,
    salary decimal(8,2) DEFAULT NULL,
    manager_id decimal(6,0) DEFAULT NULL
);
```

write the following queries:
- A result set of employees that have a salary above $50,000K
    ### Select employee_id WHERE salary_decimal > "50,000"
- A result set of all the employees and their corresponding managers.
    ### Select employee_id, salary_decimal FROM employees
- A result set of all the managers and the average salary of the employees that report to them.
    ### Select manager_id, AVG(salary) FROM employees

## Challenges (do as many as you can)
- Write a function to reverse a string
    ### ```x = "hello"
for letter in range(1, len(x)+1):
    print(x[-1 * letter])```

- Write a function that determines if a number is odd or even
    ### ```def iseven(a):
    return a % 2 == 0
print(iseven(11))```

- Write a function to check if a number is prime
- Write a function that generates the first n prime numbers
- Write a function that takes a list as input and returns a list with all duplicates removed. eg: `[1,1,2,2,3]` -> `[1,2,3]`
    ###```my_list = []
def de_doop():
    for num in range(3):
        list = input("please enter a number")
        my_list.append(int(list))
    print(set(my_list))
de_doop()```

- Write a generator function that creates the [Fibonacci numbers](https://en.wikipedia.org/wiki/Fibonacci_number)
- Write a python implementation of the `wc` command. See `man wc` for a description of how it is supposed to work.
