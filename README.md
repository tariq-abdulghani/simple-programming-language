# simple-programming-language

is a proposal of some grammar that i don't fully know,
but promises with readability and being more natural
since many problems comes from 
"the language we speak is not the language that expresses problem solving."
in our daily life we use verbs and nouns and adverbs and conjunction
that actually refers to structures and impiels
  logic
  repeatition 
  conditionals
 so why not to think in that way why not to be clear and write in a formal\
 way what we want
 why not to map object methods to verbs ?
 and refer to its member like the way we refer things what is the hill is "." .
 
 this is just my thoughts of what a programming language may be
 its not a omplete work no compilers or even grammar but its my thoughts that i wish
 to be completed one day.
 
 
 My-programming-language
---------------------------------------------------------------------------
# Mini Math proposal
Let
Let  x = 10

#Constant
Let PI = 3.14

—---------------------

Function <name > (arg list) -> type:
	// body

—-----------------------

Structure <name>:
	init():
	// init body

—-----------------------

Protocol <name>:
	// collection of procedures

For i in range(10):
	// do something


English like,  math like,
high readability, simple,
 more natural and close to natural languages
consistent, logic,
concurrent 


2 if <bool expression>:
	//
   Else if <bool expression>:
	//
   Else:
	//

4 for  … in … :
	//

5 while …. :
	//

6 prototype inheritance

7 operators:
	Logical : and  or  not  xor
	Relational: > ,< ,== ,!= ,>= ,<=,   , a >= x<= b
	Math: + - * % ^ 
	Slice: [a,]
	Evaluate: ()


Structure Person :
	Name  String
	birthDate Date
	Age Integer
	
	Represent  f(this):
		Return “”

Protocol Callable:
	Call: this -> Any

Structure Function Supports Callable, Representable:
	[x: String]: Any
	 Call: f(this):
	//
	
	
Protocol Representable:
	Represent: this -> String;

Protocol Iterable<T>:
	Next: this -> T
	hasNext:  this -> Bool


Bool = {0,1} 

Let p, q  ∊ Person

->set
Let People = {x : ∊ Person}

-> list // list protocol has multiple impl
Let Books  = [ b  : ∊ Book]

-> tuple
Let Point = (x, y, z) : x,y,z  ∊ Integer


Multiply: Int * Int -> Int  // declare function

Multiply(a Int , b Int):
	Return a *b

Prototype Printer:

	Local String model

	Function print(this) -> None:
		Console print “Hello”

Function main():
	
	Let printer = Printer()
	Printer print
	
--------------------------------------------------------------------------------------------------------------------------------------------
# Simple programming  language

```
abstract type WebServer:
	
	run: int #port -> None;
	
type MyServer is WebServer:

	runOnPort(int port):
		super run port
  

abstract type Iterator<T>:
	hasNext: None -> bool
	next: None -> T

type Range is Iterator<int> and Callable:
	
	instance (local int value, local int limit).
	
	call (int value, int limit):
		return MyRange instance value, limit
	
	hasNext :
		return value < limit
	
	next :
		return value := value + 1


abstract type Engine :
	
	model String
	speedUp: int  speed| None -> None
	speedDown: int  speed| None -> None

type HondeV8 is Engine:
	// pla pla pla
	
type Car :
	
	instance(local Engine engine)
	
	withEngine (Engine engine):
		return Car instance engine
	
	speedUp(int speed):
		engine speedUp speed
	.
	
	speedDown(int speed):
	engine speedDown speed
	.


program(String... args):
	
	let file <- FileSystem open "c://filedirectory"
	
	// FileSystem open "c://filedirectory" -> file

	if file::( not directory and readable ) then
		while line := file readLine :
			Console write line
	else
		Console write "is directory"
	.

	Console write "Hello Simple" if true
	
	for i in [1:10]
		Console write i
	.
	
	let server <- MyServer instance
	server runOnPort 9000
	
	if money > 1000:
		Console write " "
		
	else if money > 600:
		Console write " "
		
	else if money > 200:
		Console write " "
		
	else:
		Console write " "
	.
	
	for num in Range (1, 10):
		Console write num
	.
	
	let hondaCar <- Car withEngine (HondeV8 model '12e-cde').
	hondaCar speedUp 10
	hondaCar speedDown 10
	
	return 11 if a >= b else 10
	X <- 11 if a >= b  else 10
```
—---------------------------------------------------------------------------------------------------------

```
let Student:
	wallet Wallet
	name String
	password String
	courses Collection<Course>
	contactInfo ContactInfo
	
	takeCourse (Course c) None:
		// pla pla

	cancelCourse (Course c) None:
		// pla pla

	pay(int amount) None:
		// pla pla
	
	
let Wallet:
	id String
	student Student
	amount Money
	
	withdraw (Money money) None:
		// pla pla

	deposit(Money money) None:
		// pla pla


let Course:
	name String
	price Money
	duration int
	capacity int
	enrolledCount int
	students Collection<Student>
	
	full() None:
		// pla pla


let Money is Scalar:
	quantity int
	currency String
	
	# add, multip, subt, div 

let Address:
	street String
	city String
	country String
	
let ContactInfo:
	address Address
	phones:
		home TelephoneNumber
		office MobileNumber
	.

program(String... args):
	
	let Tom := Student (
				"Tom", 
				"password",
				ContactInfo (
					Address("street", "city", "country"),
					Phones("xxx-xxx-xxx", "yyy-yyy-yyy")
					)
				)
	.
	
	Tom's wallet := Wallet ( Tom, Money ( 1000, '$') ).
	
	let Arabic, English, History := 
		Course( "Arabic", Money (20, '$'), 4 weeks , 10 , 0),
		Course( "English", Money (20, '$'), 4 weeks , 10 , 0),
		Course( "History", Money (20, '$'), 4 weeks , 10 , 0)
	.
	
	// Tom takeCourse Arabic and English and History.
	// method invocation as verbs or operator
	Tom takeCourse Arabic, 
		and English, 
		and History if price of History <= 15 '$', 
	then
		pay 20,
		and 20,
	then 
		cancelCourse History

	// member expression # "of", "'s"
	Console write street of address of Tom's contactInfo.
	Console write "remaining := " + amount of Tom's wallet.

	let courses := Collection (Arabic, English, History).
	// iteration expression
	for course in courses:
		Console write course

	let claculator := Calculator ()
	let sum := claulator add 1, 2

```

	

