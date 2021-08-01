# appworks_assignment

2.	Here are a few git and GitHub commands we usually use in software development, please explain the meanings and use cases of them.

●	git status: Show the working tree status.
It lets you see which changes have been staged, which haven’t, and which files aren’t being tracked by Git.
	
●	git add: Add file contents to the index.
This command updates the index using the current content found in the working tree, to prepare the content staged for the next commit.

●	git commit: Record changes to the repository
Create a new commit containing the current contents of the index and the given log message describing the changes.

●	git log: Show commit logs.
List commits that are reachable by following the parent links from the given commit(s), but exclude commits that are reachable from the one(s) given with a ^ in front of them. The output is given in reverse chronological order by default.

git push [ Repo_name ] [ Branch_name ]: to upload local repository content to a remote repository.

●	git remote -v
●	git branch
●	fork

3.	Please describe how to establish a GitHub repo and how to upload the local projects to GitHub. Try to explain your answers with as much detail as possible.
Basic
1.	In Swift, we usually define a variable through the syntax as below:
.var x: Int = 10.
We use the formula: 2 * radius * Pi to calculate the area of a circle. Now, please define a variable Pi and assign a value to it. You can refer to the syntax above while thinking about using var or let and which data type it should be.
let Pi: Double = 3.14

2.	Create two constants x and y of type Int then assign any value to them. After that, please calculate the average of x and y and store the result in a constant named average.
let az: Int = 9
let otherVaccine: Int = 2
let average: Int = (az + otherVaccine) / 2


3.	Following Q2, now we want to save the average in a record system, but the system doesn’t accept 65 but 65.0.
●	Please solve this problem so that we can put the average in the record system.
let doubleAverage = Double(average)

●	Please explain the difference between ( 10 / 3 ) and ( 10.0 / 3.0 ).
(10 /3) number type Int operation return the Int value, the quotient: 3, without the left over.

( 10.0 / 3.0 ) Floating-point type or Double type return the same type, the quotient and remainder: 3.3333
4.	Swift is a very powerful language that can infer the data type for you ( Type inference ) while we still need to know the basics well. Please change the following codes into the one with the data type.
Ex: .var x = 10. => .var x: Int = 10.
var flag = true
var inputString = "Hello world."
let bitsInBite = 8
let averageScore = 86.8

var flag: Bool = true
var inputString: String = "Hello world."
let bitsInBite: Int = 8
let averageScore: Double = 86.8


5.	Compound assignment operators are very useful when programming. Please create a salary as 22000, and use unary plus operator adding 28000 to salary, and it will be 50000 after this process.

Var salary = 22000
salary += 28000


6.	You should notice that ‘=’ has a different meaning in programming. In the real world, .‘=’ means equal while In programming, ‘=’ means assign . You simply put the right hand side data into the left hand side variable or constant.
Now please write down the Equality operator in swift.

Equality operator in swift:  (a == b)

7.	Declare two constants that values are 10 and 3 each, then please calculate the remainder and save the result in a constant named remainder .

8.	let constant1 = 10
9.	let constant2 = 3
10.	let remainder = constant1 % constant2


11.	Please explain the difference between let and var .

let is used to declare a constant value.
It creates immutable variables, value cannot be changed after it is created.

var defines an ordinary variable.
It creates mutable variables, the value can be changed to a different value in the future.

12.	Please write down naming conventions and rules you learned in this session.

Constant and variable names can contain almost any character, including Unicode characters.

Constant and variable names can’t contain whitespace characters, mathematical symbols, arrows, nor can they begin with a number

One popular convention is CamelCasing.
One important tip to naming is to make it effectively communicates the semantic meaning of its value.



13.	What is Type Inference in swift?

Swift is a type-safe language, which means the language helps us to be clear about the types of values our code can work with. 
If part of our code requires a String, type safety prevents us from passing it an Int by mistake. 

If you don't specify the type of value you need, Swift uses type inference to work out the appropriate type. Type inference enables a compiler to deduce the type of a particular expression automatically when it compiles our code, simply by examining the values we provide.


14.	What is the problem about this piece of code?
var phoneNumber = 0987654321
phoneNumber = "Hello world."

Once the type of a variable is declared (or inferred) the type cannot change. Trying to change the type of it will result in an error.


Collection
append
You should know how to declare an array in Swift, and also how to add, remove, insert, read an object in an array. You should be familiar with the following syntax:,
.insert ,	remove
.
Arrays are dangerous in swift. If you access the array with an index which is out of range, your app will crash with fatal error. Please interact with the array very carefully.

1.	Please create an empty array with String data type and save it in a variable named .myFriends .
var myFriends: [String] = []

2.	According to Q1, now I have three friends, ‘Ian’, ‘Bomi’, and ‘Kevin’. Please help me to add their name into myFriends array.
myFriends += ["Ian", "Bomi", "Kevin"]

3.	Oops,I forgot to add ‘Michael’ who is one of my best friends, please help me to add Michael to the end of myFriends array.

myFriends.append("Michael")

4.	Because I usually hang out with Kevin, please move Kevin to the beginning of the .myFriends array.
Before append:
MyFriends.insert("Michael", at: 0)

After append:

myFriends.swapAt(0,3)

myFriends
5.	Use for…in to print all the friends in array.

var allMyFriends = myFriends[0...3]
print (allMyFriends)


6.	Now I want to know who is at index 5 in the myFriends array, try to find the answer for me. Please explain how you get the answer and why the answer is it.

There will be an error.
Because the index is out of range of the array, which only have 4 items, that the index 5 doesn’t exist.

7.	How to get the first element in an array?

arrayName[0],
arrayName.first

8.	How to get the last element in an array?
arrayName.last

9.	Please create a dictionary with keys of type String, value of type Int, and save it in a variable named myCountryNumber .

10.	Please add three keys ‘US’, ‘GB’, ‘JP’ with values 1, 44 , 81.
11.	Change the ‘GB’ value from 44 to 0.
12.	How to declare an empty dictionary?
13.	How to remove a key-value pair in a dictionary?

Control Flow 1. Here is an array:
let lottoNumbers = [10, 9, 8, 7, 6, 5]
Please use For-Loop and Range to print the last three members in the .lottoNumbers. array.

		For-Loop:
		let lottoNumbers = [10, 9, 8, 7, 6, 5]

for i in 3..<lottoNumbers.count {
    		print(lottoNumbers[i])
    			}



		Range:
let lottoNumbers = [10, 9, 8, 7, 6, 5]
var lastThreeNumbers = lottoNumbers [3...5]
print(lastThreeNumbers)



2.	Please use swift syntax to get the result as images list below :
.5
.6
.7
.8
.9
.10


.10
.8
.6



Please find a method which can help us complete these requirements.

3.	Please use a while loop to solve the above question.

4.	var x = 5
5.	while x < 11{
6.	    print(x)
7.	    x += 1
8.	}



9.	Please use a repeat-while loop to solve question 2.

10.	What are the differences between while and repeat-while? 

The repeat-while loop, performs a single pass through the loop block first, before considering the loop’s condition. It then continues to repeat the loop until the condition is false.


11.	Here is the variable isRaining to record the weather. Please write a statement that if the weather is raining, print “It’s raining, I don’t want to work today.”, otherwise print
“Although it’s sunny, I still don’t want to work today.”
if isRaining = true {
    print("It’s raining, I don’t want to work today.”)
} else {
    print(“Although it’s sunny, I still don’t want to work today.”)
}

7. In a company, we usually use numbers to represent job levels. Let’s make an example. 
There are four job levels: Member, Team Leader, Manager, and Director.
We use 1 for the Member, 2 for Team Leader, 3 for Manager, and 4 for Director. 
Now, create a variable name jobLevel and assign a number to it. 
If the jobLevel number is in our list, print the relative job title name; if not, just print “We don't have this job”. Please use a switch statement to complete this requirement.


var jobLevel = 4

switch jobLevel {
case 1:
  print("Member")
case 2:
  print("Team Leader")
case 3:
  print("Manager")
case 4:
  print("Director")
default:
  print("We don't have this job.")
}


Function
1.	Please declare a function named greet with person as argument label and .name. as a parameter name. This greet function will return a String. For example, if you call the function greet like this:
greet(person: "Luke")
It will return the string: “Hello, Luke”.


2.	Please declare a function named multiply with two arguments a and b . This
function won’t return any value and will only print out  the result of a * b . Be noticed that we want to give argument b a default value of 10.


3.	What’s the difference between argument label and parameter name in function ?


4.	What are the return types in the following statements?
func birthday( ) -> String {

}

func payment( ) -> Double {

}
![image](https://user-images.githubusercontent.com/15847990/127777868-ec65ebf8-9403-496d-aeda-158bf4bf2596.png)
