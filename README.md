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
// I WANNA DESCRIBE MY PRO LANG BY ANOTHER LANG:
// --------------------------------------------

$ statment FUNC_DECL[$scope]
        `
        func <ID> (<a_i> <T_i> )<R>{
            // stmts is reference to zero or moew stmt but not part of the syntax
           --stms-- [STMT ;]
        }
    `
    where
        0 < i < 20, a matches($names_regex), T  is a TYPE, R  is a TYPE

    exec_stmt
        create sc Sope
        $scope.append(sc)
        let args: (text, struct)[] := []
        for j in i do
            args.append(($a_j , $T_j))
        end
        sc.append('args', args)
        sc.appendStatmens($smts)
end
```
```xscript
$ expression FUNC_CALL [$scope, $line]
    `<ID>(<v_i> )`
    where
        0 < i < 20,

    exec_stmt
        node := $scope.rerieve($ID)
        if node then
            args := node.retrieve('args')
            for j in i do
                // name binding
               node.append(args_j, $v_j)
               try
                   result:= node.eval()
                   return result
                catch e
                    error e.message
            end
        else
            error '$ID is not defined line $line'

end
```
```xscript
$ modifier ASYNC_MOD
    `async <STMT:FUNC_DECL>`
end
```
```typescript
// each scope is associated to set of  statements
// each scope represents a node in AST by some how
//

// x script has 3 levels lang
// higher level is the meta lang its the lang that u can use to describe
// and extend the lang

// lvl 2 is the api level or developer level which is used
// lvl 3 is the low level which is byte code


// referencing variables
// assigning types to variables
// must express how to access environmental variables (varibales in some scope)

// declarative language that can  express things in formal way
// providing lower level (explaining layer to the text provided)
```
