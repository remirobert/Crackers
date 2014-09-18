<p align="center">
  <img src ="https://raw.githubusercontent.com/remirobert/Crackers/master/ressources/logo.gif"/>
  <h1 align="center">Crackers</h1>
</p>

Stop to get worked up, use crackers for all networking call !

Crackers is an **HTTP networking** library written in Swift, for **OSX** and **iOS**.

<h1 align="center">Feature</h1>

 - HTTP methods : **GET**, **POST**, **PUT**, **DELETE**
 - Asynchronous request
 - Management of large packets
 - HTTP Basic Authentication

<h1 align="center">Usage</h1>
<h3 align="center">GET Request</h3>

```Swift
let requestGet = Crackers(url: "http://httpbin.org/get")

requestGet.requestGET { (data, response, error) -> () in
  if (error == nil) {
    println("request success ! \(response), \(data)")
  }
  else {
    println("\(error)")
  }
}
```

<h3 align="center">POST Request with parameters</h3>

```Swift
let requestPost = Crackers(url: "http://httpbin.org/post")

var parameters = Dictionary<String, String>()
parameters["username"] = "remi"
parameters["password"] = "github"
        
requestPost.setHeader("application/json", headerField: "Content-Type")
        
requestPost.requestPOST { (data, response, error) -> () in
  if (error == nil) {
    println("request success ! \(response), \(data)")
  }
  else {
    println("\(error)")
  }
}
```

<h3 align="center">HTTP Basic Authentication</h3>

```Swift
let requestGet = Crackers(url: "http://httpbin.org/get")
        
requestGet.setAutorizationHeader("remi", password: "github")
        
requestGet.requestGET { (data, response, error) -> () in
  if (error == nil) {
    println("request success ! \(response), \(data)")
  }
  else {
    println("\(error)")
  }
}
```

Currently used in a personnal work.

<h1 align="center">Author</h1>
Rémi ROBERT, remirobert33530@gmail.com

<h1 align="center">Licence</h1>
Crackers is available under the MIT license. See the LICENSE file for more info.
