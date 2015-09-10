# YAPL SPECIFICATION

There are some features i think in this language.

## currying in everything

```
; use fn to create function

fn (impl:int) foo:(a:int,b:int)=>(x:int,y:int) throw error{
   defer{ }
   require{ }
   ensure{ }
   guard{ }
   doc{ }
   test{ }
   
   return a+b,a
}

; use _ 

f1 = foo(a,_) # fn f1(x)=>(a,b) { return foo(a,x) }
f1(2) # call function

```

or you can use "_1 or _2 ..." to create anything function you want

```
fn foo(x,y,z)->(x int){
   return x
}

f12 = foo(_,_,3)
f13 = foo(_,2,_)
f23 = foo(1,_,_)

ffo = foo(1,_2,_1)
ffo(1,2) # => foo(1,2,1)
```
## piple for everything

you can use symbol `|>` to create data flow.

```
; array
f = [1,2,3] 
f |> map(_1,{_ + 1}) |> filter(_1,{_ >2}) # => [3,4]

; function

f = {_ +1 } |> {_ + 2} |> {_ + 4} # => { { { _ + 1} + 2} + 4 }
f(2) # =>  9

```

## lambda function
lambda express will return last express value.

```
{|x,y| x+y}
{_1 + _2 }
```
## string 
i think like ruby

## int 
like ruby

## float 
like ruby

## block
like ruby yield

## generate
like python yield

## meta funciton 
like ruby

## control flow
like ruby

## value and variable
like scala

## class and member
like ruby
like c++ member function point






```
