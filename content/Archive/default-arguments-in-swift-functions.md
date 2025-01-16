---
title: "Default Arguments in Swift Functions"
date: "2016-01-25"
categories: 
  - "words"
---

Default Parameters in Swift

Its the little things that make my life as programmer easier. Like default parameters in Swift. From the The Swift Programming Language (Swift 2.1):

> You can define a default value for any parameter in a function by assigning a value to the parameter after that parameter’s type. If a default value is defined, you can omit that parameter when calling the function.

I was working on a swifty implementation of the DigitalOcean API and I came up with a monster function definition, like this:

```
func createDropletNamed(name: String,
    region: String = "nyc3",
    size:String = "512mb",
    image:String = "ubuntu-14-04-x64",
    keys:[String] = [],
    backups:Bool = false,
    ipv6:Bool = true,
    userData:String = "",
    privateNetworking:Bool = false,
    callback:(NSDictionary?, ErrorType?) -> Void = {_,_ in }) {
```

In the days of Objecective-C, if I wanted simpler convenience versions of this call, I’d define additional functions which take fewer arguments,[\[1\]](#fn:1 "see footnote") and then call the monser function by suppliying some defaults. You see that pattern all the time in Objective-C initializers.

Thanks to the magic of default parameters, that’s not nececcary. Any of the following calls are valid based on the original definition with default arguments:

```
createDroplenNamed("devserver1")

createDropletNamed("devserver2", size: "1gb")

createDropletNamed("devserver3") { result, error in
    //handle callback
}
```

The swift manual advises lising arameters with default arguments after paramters that always require arguments. Elsewhere, it recommneds that closures always come in the last position to support the trailing closure syntax. Those two rules together imply that if you have a funciton with default arguments and a closure, the closure must take a default argument. Luckily it’s pretty easy to define an empty closure like `{_,_ in }`.

* * *

2. Actually, I’d probably define a function that takes an NSDictionary, but then I’d lose auto-completion and type checking.  [↩](#fnref:1 "return to article")
