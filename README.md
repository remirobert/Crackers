<p align="center">
  <img src ="https://raw.githubusercontent.com/remirobert/Crackers/master/ressources/logo.gif"/>
  <h1 align="center">Crackers</h1>
</p>

Stop to get worked up, use crackers for all networking call !

Crackers is an **HTTP networking** library written in Swift, for **OSX** and **iOS**.

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
