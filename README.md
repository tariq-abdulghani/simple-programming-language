# ex.script lang
is a proposal of some grammar that i don't fully know

## Expressivness
the expressivness of a language ?
..how to measure such thing?
..since there is no clear way to measure it with a quantity
..we can produce a way to describe the ability of a language
..what it can say and what it cant say and
..how many symbols are required to represent a concept in such language

..to make such comparisons we need some thing common to be the base of comparison
..i will choose the purpose of a language what purpose it has?
..what is the thing that is abstracts.

## Self Refering Ideas And Expressions:
### Recursion:
..methods|functions can use it self to produce some computation
..rule can use it self ot define it self? strange isnt it!
..in order to use recursion by some how you need to eliminate 
..ambiguity
..recursion is amazing in describing many things.

### Reflection
`The ability of a programming language to be its own metalanguage is called reflection`
..when objects can see their descriptions and their properties
..and access their meta data is abery strong feature and reduced
..lines of code that describe and use the concept so we can define
..meta data and some meta behaviors also and use it without 
..the need to write it again.

### Meta Language
..in Mathematics lessons we can see that
..Mathematics has its own language that is used
..to define some structures it relies on small
..set of symbols and small set of english expressions
..these aspects make us write less and say more 
so our approach is not very precise neither abstract
it really raises the flag of a need of formal way to describe
languages in a way that answers the question:
How its powerful andm what set of concepts its really good at?


```xscript
$Statement class:
    $template := """
        <ID>:
        [TAB<A> <TYPE>]
        [<F>([<a> <TYPE>])-> <TYPE>:
            [TAB STMT]
        ]
    ""

    $parse($env):
    ....


referencing variables
assigning types to variables
must express how to access environmental variables (varibales in some scope)

declarative language that can  express things in formal way
providing lower level (explaining layer to the text provided)
```
