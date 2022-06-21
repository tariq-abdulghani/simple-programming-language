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
 and refer to its member like the way we refer things what is the hell is "." .
 
 this is just my thoughts of what a programming language may be
 its not a omplete work no compilers or even grammar but its my thoughts that i wish
 to be completed one day.
 
 
 ```
// expression
// unified model every thing is a concept
// concept has a name and restrictions based on primitives or 
// other concepts we alias cocepts to use same restrictions but
// with different semantics
// it can abstract objects, operations , and procedures

-- concept Vector: v where
	v = (v1, .., vn), n > 0, vi is real

	let x,y: Vector then

	x+y = x1+y1, .., xn+yn;

	x * y = x1*y1, .., xn * yn;
--

-- concept Person: p where
	p ={
		name, 
		age, 
		birthDate, 
		email, 
		password, 
		..etc
	}

	let p1, p2 : Person then

		p1 = p2 :=  p1[ email and name ] = p2 [email and name]
		repr(p1) := "{name: ${p1'name}"
--

-- concept Webserver: web where 
	web = {
		port,
		staticFilesDir,
		....
	}

	web run (port) ->
		web'port = port
		// do some logic ...


	web on () ->
		// do some logic ...


	web stop () ->
		// clean up logic
--

let App : Application where 
	entryPoint(*Words) ->
		let port = 8888;
		if 'port=\nums\' match any word in Words then
			wordIncludesPort = find word in Words where port=\nums\' match word;
			port = someRegex getFirstMatch (wordIncludesPort);

		let server: WebServer with {port:port}
		server on()
		onError e ->
			sout printLine(e stackTrace)
			server stop();
 ```
 
 -----------------------------------------------------------------------------------------
 
 ```
let Grade = g : 0 <= g<= 100;
let Fragile = f: f < 40;

let n5(x)= x -(x%5) +5;

let grade(x)= {
    n5(x) if ( n5(x)-x )< 3,
    x if x < 38
}

procedure StudentGrades () None :

    studentGrades = [12, 34 ....];
    finalGrades = [];

    for studentGrade in studentGrades do
        finalGrades push(grade(studentGrade))
    end for

    sout printLine(finalGrades)
end grade
 ```
 -----------------------------------------------------------------------------------------
```
	
class Timer:

	#static method 
	every(int period, String perioSpecifier, Callable callBack) None:
		---


class Tank:
	int level
	int minLevel
	int maxLevel

	#method
	startDrain() None:
		---
	#method
	stopDrain() None:
		---

	
class Pump:

	function start(self) None:
		---

	function stop(self) None:
		---


function observeLevelAndAct (Tank tank, Pump pump) f() None :
	return function () None:
		if tank's level <= tank's minLevel:
			tank stopDrain()
			pump start()
		else if tank's level >= tank's maxLevel:
			tank startDrain()
			pump stop()


program(String... args) int:
	
	let Lisa := Student with {
				name:"Lisa",
				password: "passLisa",
				contactInfo: {
					address: { steet: "strr", city: "cit", country: "Cou" },
					phones: { home: "xx-xxxx-xxxx", "office": "xxx-xxx-xxx" }
				},
			}

	Lisa's wallet := Wallet with { 
					student: Lisa, 
					amount: Money(1000, 's')
				}.
	
	let Arabic := Course with {
			name: "Arabic",
			price: Money(20, '$'),
			duration: (4, 'week'),
			capacity: 10,
			enrolledCount: 0
		},

		English := Course with {
			name: "English",
			price: Money(20, '$'),
			duration: (4, 'week'),
			capacity: 10,
			enrolledCount: 0
		},

		History := Course with {
			name: "History",
			price: Money(20, '$'),
			duration: (4, 'week'),
			capacity: 10,
			enrolledCount: 0
		}

	Arabic's duration := Duration ( 5, 'week')
	
	Tom takeCourse (Arabic)
	Tom takeCourse (English)
	Tom takeCourse (History)
	Tom pay (20)
	Tom pay (15)
	Tom cancelCourse (History)

	-- if single argument we can ommit praces --

	Lisa takeCourse Arabic
	Lisa takeCourse English
	Lisa takeCourse History
	Lisa pay 20
	Lisa pay 15
	Lisa cancelCourse History

	let tank1 := Tank with { level: 10, minLevel: 1, maxLevel: 10 }
	let fillPump := Pump instance

	Timer every ( 20, 'second', observeLevelAndAct (tank1, fillPump) )
	--
	Timer every ( 20, 'second', ...-> 
		if tank1's level <= tank1's minLevel:
			tank1 stopDrain()
			fillPump start()
		else if tank1's level >= tank1's maxLevel:
			tank1 startDrain()
			fillPump stop()
		)
	--

	Console write ("Hello Simple " + " ").

	let currentSpeed := car's motoSpeed * car's gearRatio.

	Console write (street of address of Tom's contactInfo + " ") 

	let adj := "tall" if Tom's hieght > Length( 170, 'cm') else "short"

	let succeeded := true if Jane's grade >= 50 else false

	Console write (f"Tom is ${adj}")

	let sb := StringBuilder instance
	
	sb append ("Hello ")
	   append ("World ")
	   append ("Simple ")
	   append ("programming language!. ")
	   append (NEW_LINE)
	   build().


	let pdfWriter := PdfWriter with { font :'', fontSize: '', ...}.

	pdfWriter addHeader ("header")
			  addLine("simple" and "Wow.")
			  addTable (data)
			  save ("data-summery").

	let mult := x,y -> x*y .
	Console write ( mult (10, 2)) .

```


```
goals be 
-readable
-easy to use and write large scale apps easy
- dynamic typed or static typed?
	dynamic types typ checking is made at run time
	static is the opposite

	how to get best of both worlds?

	let x = 0 
	let x: int

	'let x = 0' <==> 'let x: int'
	'const x = 0'

	fn add(x: int, y: int)-> int :
		ret x + y


	class Person  implements User:

		-static id: int
		-name: string
		-email: string
		-password: string

		init(self, name:string, email:string, password:string):
			this.name = name
			this.email = email
			this.password = password

		--override
		fn toString()-> String:
			ret `${name}`

		static fn generateId()->int:
			ret ++id

```
	
	

