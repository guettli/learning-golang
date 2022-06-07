# Learning Golang

I develop software with the programming language Python since more than 20 years.

I like Python.

Nevertheless I want to try something new.

# Motivation

Why Golang? Because I am interested in Kubernetes, and in this context almost
all code is written in go.

I do web development since 2001. I am super happy that the browser wars are over.

Most things work flawlessly on all browsers.

I don't like the new JavaScript based applications. They are like old (and slow) native applications.

I like [htmx.org](//htmx.org), but up to now this is only a spare time thing, because we don't use it at work.

I am curious and want to try something new.

# Learning Ressources

https://gobyexample.com/

Podcast: https://changelog.com/gotime


# Things I like in Golang

Declared, but not used variables are an error, not just a warning.

IDE (vscode) shows a warning you can't overlook if you don't use the value of variable.

Golang does not burn the planet. Just duckduckgo for [energy consumption programming languages](https://duckduckgo.com/?q=energy+consumption+programming+languages). C, C++ andRust are better, but having a language with garbage collector makes
the life of a developer much easier.

Strict Typing. During the last weeks I worked on a large and old code base which was new to me. It was Python code without type annotations. Before I never missed type annotations because I worked on a code base which was well known to me during the last years. But being new to a large code base
changed my mind. I want to be able to use ctrl+click to get to the type definition.

# Things I don't like in Golang

Getting all keys of a map is too complicated. See [Getting a slice of keys from a map](https://stackoverflow.com/questions/21362950/getting-a-slice-of-keys-from-a-map)

I am missing exceptions. But maybe I just need to get used to explicit error handling.

# About OOP

Golang does not support OOP.

When I was young I was facianted by OOP (object oriented programming). The thing
which facianted me the most, was that I did not understand it immediately, but I heard
great things about it over and over again. In the year 1996 I only had experience with
BASIC and Pascal.

Inheritance is great, but in most cases not needed.

I mostly write methods which handle http requests. These methods run for some milliseconds and then
return the result. I don't create complex and long living objects. I work with SQL databases and APIs. 
For both things I don't need inheritance.

I can live without OOP.



# Unicode Strings

```
package main

import (
	"fmt"
	"unicode/utf8"
)

func main() {
	my_string := "abc-äöü"
	fmt.Println("len", len(my_string))
	fmt.Println("RuneCount", utf8.RuneCountInString(my_string))
	for index, character := range my_string {
		fmt.Println("index:", index, 
			" character: ", character,
			" string(character): ", string(character))
	}
}
```
