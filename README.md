# 1.Write a blog on Difference between HTTP1.1 vs HTTP2

## HTTP :
			Http is (HyperText Transfer Protocol) used for transferring the data Client to Server and Server to Client via the internet. It basically works for Request and Response manners. And the Client sends the Request(Google.com) to the Server, the Server sends the Response(Google.com) to the Client.If we want the Html file, Css or any other image file, everything will be transferred to the Request and Response manner only.

## HTTP2 Vs. HTTP1 or HTTP1 Vs. HTTP2 – Let’s Understand The Two Protocols

HTTP/1.1 has been around for more than a decade. With Google’s SPDY leading the way in 2015, the IETF (Internet Engineering Task Force) gave us HTTP/2, which introduces several features to reduce page load times. Let’s compare HTTP2 Vs. HTTP1.1 in detail.


HTTP/2 achieves faster webpage loading without performance optimizations that require extensive human efforts in terms of development. It significantly reduces the complexities that had crept into HTTP/1.1 and gives us a robust protocol which, though not without its flaws, will perhaps stand the test of time. Before making this leap forward, let’s trace our steps back to when the internet was in its infancy to understand how the different versions evolved into the current form.

## The Beginnings of HTTP & The Internet

Our story begins in 1969, with a program called Advanced Research Projects Agency Network (ARPANET). ARPANET used packet switching and allowed multiple computers to communicate with each other on a single network. However, this was just a by-product. The original intention behind ARPANET was to design a time-sharing system that allowed research institutes to share their computer resources for effective utilization of processing power.

Before then, sometime during the 19th century, the seeds for the existence of the internet as we know it today had already been sown with the invention of electricity and the telegraph. With Morse sending the first telegraphic message in 1844 and the first cable being laid across Atlantic, the telegraph network infrastructure had spread its roots through continents and across oceans. In years to come, this would become the very foundation on which the internet was built. In 1973, Kahn and Cerf designed the TCP/IP protocol suite which was adopted by ARPANET a decade later, and from this point on, we witness the development of an interconnected network. The internet took a more recognizable form with the invention of the World Wide Web (that used HTTP as its underlying protocol) by Tim Berners-Lee and the Commercial Internet eXchange (CIX) that allowed a free exchange of TCP/IP traffic between ISPs.

## Evolution of HTTP

HTTP (Hypertext Transfer Protocol) is a set of rules that runs on top of the TCP/IP suite of protocols and defines how files are to be transferred between clients and servers on the world wide web.

![111](https://user-images.githubusercontent.com/105142903/173268982-af2dc647-1dff-4f22-82a4-2a46fccce87a.png)

## The Beginning of HTTP: Version 0.9 & 1.0

In the earliest phase (HTTP/0.9), the HTTP protocol did not use headers and only transmitted plain HTML files. It was a one-line protocol only supporting the GET method.

![2](https://user-images.githubusercontent.com/105142903/173269042-9d58597c-ac39-4584-bb44-45d1d28fce9e.png)

As the need to exchange more than just plain HTML emerged along with the client and server applications becoming more mature, HTTP/1.0 (between 1991-1996) introduced several new features.

## Key Features of HTTP/1.0:

The concept of headers both for requests (from the client machine) as well as responses (from servers) was introduced. The use of headers such as GET, POST, HEAD added extended flexibility, none of which was possible with the earlier version.
Version information was now included.
It allowed a single request/response for every TCP connection.
Status codes were used to indicate successful requests and to indicate transmission errors.
The content-type header made it possible to send files other than plain HTML, including scripts and media.

## Created for Added Security: HTTPS


In 1994, Netscape Communications created HTTPS (Hypertext Transfer Protocol Secure) to be used with SSL for its web browser, Netscape Navigator. The need for encrypted transmission channels emerged as the applications being designed shifted towards a more commercial market where advertisers, unknown individuals, and cybercriminals could have easy access to personal data. SSL evolved into TLS with TLS version 1.2 and 1.3 being used currently.

## The Protocol Serving Netizens for Over 15 Years: HTTP/1.1

HTTP/1.1, the first standardized version of HTTP, was introduced in 1997. It presented significant performance optimizations (over HTTP/0.9 and HTTP/1.0) and transformed the way requests and responses were exchanged between clients and servers.

![3](https://user-images.githubusercontent.com/105142903/173269078-045fb5f2-50b5-40da-9628-a41ca83e15d8.png)

## Key Features of HTTP/1.1:

It was no longer required for each connection to be terminated immediately after every request was served with a response; instead, with the keep-alive header, it was possible to have persistent connections. It allowed multiple requests/responses per TCP connection.
The Upgrade header was used to indicate a preference from the client that made it possible to switch to a more preferred protocol if found appropriate by the server.
HTTP/1.1 provided support for chunk transfers that allowed streaming of content dynamically as chunks and for additional headers to be sent after the message body. This enhancement was particularly useful in cases where values of a field remained unknown until the content had been produced. For example, when the content had to be digitally signed, it was not possible to do so before the entire content gets generated.
Other features that reinforced its stability were introduced such as:
pipelining (the second request is sent before the response to the first is adequately served)
content negotiation (an exchange between client and server to determine the media type, it also provides the provision to serve different versions of a resource at the same URI)
cache control (used to specify caching policies in both requests and responses)
The Protocol Designed to Speed Up Today’s Complex Web pages: HTTP/2
At the beginning of 2010, Google introduced an experimental protocol, SPDY, which supported multiplexing (multiple requests/responses sent and received asynchronously over a single TCP connection) but as it gained traction IETF’s HTTP Working Group came up with HTTP/2 in 2015, which is based on the SPDY protocol.

## Key Features of HTTP/2:

It introduces the concept of a server push where the server anticipates the resources that will be required by the client and pushes them prior to the client making requests. The client retains the authority to deny the server push; however, in most cases, this feature adds a lot of efficiency to the process.

![4](https://user-images.githubusercontent.com/105142903/173269124-a47ee1ad-bc74-45b5-b198-29471141fc9e.png)

Introduces the concept of multiplexing that interleaves the requests and responses without head-of-line blocking and does so over a single TCP connection.

![5](https://user-images.githubusercontent.com/105142903/173269168-c18ac822-933e-4a0f-acce-9f0d30286591.png)

It is a binary protocol i.e. only binary commands in the form of 0s and 1s are transmitted over the wire. The binary framing layer divides the message into frames that are segregated based on their type – Data or Header. This feature greatly increases efficiency in terms of security, compression and multiplexing.

![binary-framing-layer-500x258](https://user-images.githubusercontent.com/105142903/173269200-89a29f27-6bb8-4291-a696-b65fc0fc98ee.png)

![http-2-binary-traffic-768x384 (1)](https://user-images.githubusercontent.com/105142903/173269245-b13299c4-d17f-42f9-8c48-604a4b1e3901.png)

HTTP/2 uses HPACK header compression algorithm that is resilient to attacks like CRIME and utilizes static Huffman encoding.
HTTP/3, the next version in the series, is based on Google’s QUIC which, unlike its precursors is a drastic shift to UDP. Given the gradual adoption rate of HTTP/2, HTTP/3 with its security challenges (that comes into play the moment we switch from TCP to UDP) is expected to face some difficulties.

![evolution-of-http](https://user-images.githubusercontent.com/105142903/173269288-bafe662b-2d40-45ab-8302-fb66ec491c0f.png)

## HTTP/1.x vs HTTP/2: A Comparative Study

HTTP2 Vs. HTTP1 is not a debate at all. HTTP2 is much faster and more reliable than HTTP1. HTTP1 loads a single request for every TCP connection, while HTTP2 avoids network delay by using multiplexing.

HTTP is a network delay sensitive protocol in the sense that if there is less network delay, then the page loads faster. However, an impressive increase in network bandwidth only slightly improves page load time. This is key to understanding the differences in performance efficiencies between the different versions of HTTP. Back in the day when people used dial up modems web pages were simple and it was the actual data transfer between the server and the client that contributed towards the largest chunk of the page load time. Today the actual downloading of resources from server takes a negligible portion of the total page load time due to the tremendous increase in bandwidth availability. It is the time taken to establish the TCP connection and making requests that impacts performance. It was initially recommended to use only two connections per hostname but today most browsers use six connections per hostname. When we talk about http vs http2 in terms of performance it is important to note that a lot of performance optimizations adopted by HTTP/1.1 introduced complexities in terms of developmental efforts as well as network congestion that HTTP/2 attempts to address.

## The table below points out the differentiating factors between http2 vs http1:

Header CompressionHeaders are sent on every request leading to a lot of duplicate data being sent uncompressed across the wire.Header compression is included by default in HTTP/2 using HPACK.Performance OptimizationProvides support for caching to deliver pages faster.Spriting, concatenating, inlining, domain sharding are some of the optimizations used as a workaround to the ‘six connections per host’ rule.Removes the need for unnecessary optimization hacks.Protocol TypeText based protocol that is in the readable form.It is a binary protocol (HTTP requests are sent in the form of 0s and 1s). Needs to be converted back from binary in order to read it.SecuritySSL is not required but recommended. Digest authentication used in HTTP1.1 is an improvement over HTTP1.0. HTTPS uses SSL/TLS for secure encrypted communication.Though security is still not mandatory, it is mostly encrypted (though it is not enforced) since almost all clients require traffic to be encrypted. It also has some minimum standards, such as minimum key size for encryption. TLS 1.2 etc.

Header CompressionHeaders are sent on every request leading to a lot of duplicate data being sent uncompressed across the wire.Header compression is included by default in HTTP/2 using HPACK.Performance OptimizationProvides support for caching to deliver pages faster.Spriting, concatenating, inlining, domain sharding are some of the optimizations used as a workaround to the ‘six connections per host’ rule.Removes the need for unnecessary optimization hacks.Protocol TypeText based protocol that is in the readable form.It is a binary protocol (HTTP requests are sent in the form of 0s and 1s). Needs to be converted back from binary in order to read it.SecuritySSL is not required but recommended. Digest authentication used in HTTP1.1 is an improvement over HTTP1.0. HTTPS uses SSL/TLS for secure encrypted communication.Though security is still not mandatory, it is mostly encrypted (though it is not enforced) since almost all clients require traffic to be encrypted. It also has some minimum standards, such as minimum key size for encryption. TLS 1.2 etc.

![Untitled](https://user-images.githubusercontent.com/105142903/173269997-dc62ec3d-aeff-4e54-8ba2-d799c93f6e06.png)


Header CompressionHeaders are sent on every request leading to a lot of duplicate data being sent uncompressed across the wire.Header compression is included by default in HTTP/2 using HPACK.Performance Optimization Provides support for caching to deliver pages faster. Spriting, concatenating, inlining, domain sharding are some of the optimizations used as a workaround to the ‘six connections per host’ rule.Removes the need for unnecessary optimization hacks. Protocol Type Text based protocol that is in the readable form.It is a binary protocol (HTTP requests are sent in the form of 0s and 1s). Needs to be converted back from binary in order to read it. SecuritySSL is not required but recommended. Digest authentication used in HTTP1.1 is an improvement over HTTP1.0. HTTPS uses SSL/TLS for secure encrypted communication.Though security is still not mandatory, it is mostly encrypted (though it is not enforced) since almost all clients require traffic to be encrypted. It also has some minimum standards, such as minimum key size for encryption. TLS 1.2 etc.

## How to Implement HTTP/2 on Your Website

Since using HTTP/2 is an invisible process when correctly implemented, your website may already be using it without your realization. There is an easy way to check this:

Open the web developer tool on the web browser (like Firefox).
Under the network tab, select any of the resources and check the version number under the headers tab.
While HTTP/2 does not mandate the use of SSL, it is crucial to install an SSL certificate because the leading browsers, including Firefox and Chrome, have decided to implement HTTP/2 only over TLS (HTTPS). In order to enable HTTP/2 it is essential to get an SSL/TLS certificate and make every page on the website https.

At the web server level, it could be as simple as a software update, for example, Apache began support for HTTP/2 in version 2.4.17.


# 2.Write a blog about objects and its internal representation in Javascript

## Internal Representation Of Objects In Java Script

Objects, in JavaScript, is it’s most important data-type and forms the building blocks for modern JavaScript. These objects are quite different from JavaScript’s primitive data-types(Number, String, Boolean, null, undefined and symbol) in the sense that while these primitive data-types all store a single value each (depending on their types).

Objects are more complex and each object may contain any combination of these primitive data-types as well as reference data-types.
An object, is a reference data type. Variables that are assigned a reference value are given a reference or a pointer to that value. That reference or pointer points to the location in memory where the object is stored. The variables don’t actually store the value.

Loosely speaking, objects in JavaScript may be defined as an unordered collection of related data, of primitive or reference types, in the form of “key: value” pairs. These keys can be variables or functions and are called properties and methods, respectively, in the context of an object.
An object can be created with figure brackets {…} with an optional list of properties. A property is a “key: value” pair, where a key is a string (also called a “property name”), and value can be anything.

To understand this rather abstract definition, let us look at an example of a JavaScript Object :

**let school = {
name : “Vivekananda School”,
location : “Delhi”,
established : “1971”
}**

In the above example “name”, “location”, “established” are all “keys” and “Vivekananda School”, “Delhi” and 1971 are values of these keys respectively.

Each of these keys is referred to as properties of the object. An object in JavaScript may also have a function as a member, in which case it will be known as a method of that object.

Let us see such an example :
// javascript code demonstrating a simple object
**let school = {
name: ‘Vivekananda School’,
location : ‘Delhi’,
established : ‘1971’,
displayInfo : function(){
console.log(${school.name} was established
in ${school.established} at ${school.location});
}
}
school.displayInfo();**

Output:
In the above example, “displayinfo” is a method of the school object that is being used to work with the object’s data, stored in its properties.

## Properties of JavaScript Object

The property names can be strings or numbers. In case the property names are numbers, they must be accessed using the “bracket notation” like this :
**let school = {
name: ‘Vivekananda School’,
location : ‘Delhi’,
established : ‘1971’,
20 : 1000,
displayInfo : function(){
console.log(The value of the key 20 is ${school[‘20’]});
}
}
school.displayInfo();**

Output:
But more on the bracket notation later.
Property names can also be strings with more than one space separated words. In which case, these property names must be enclosed in quotes :
**let school = {
“school name” : “Vivekananda School”,
}**

Like property names which are numbers, they must also be accessed using the bracket notation.

Like if we want to access the ‘Vivekananda’ from ‘Vivekananda School’ we can do something like this:
// bracket notation
**let school = {
name: ‘Vivekananda School’,
displayInfo : function(){
console.log(${school.name.split(‘ ‘)[0]});
}
}
school.displayInfo(); // Vivekananda**

Output:
In the above code, we made use of bracket notation and also split method provided by javascript which you will learn about in strings article.

## Creating Objects

There are several ways or syntax’s to create objects. One of which, known as the Object literal syntax, we have already used. Besides the object literal syntax, objects in JavaScript may also be created using the constructors, Object Constructor or the prototype pattern.
Using the Object literal syntax : Object literal syntax uses the {…} notation to initialize an object an its methods/properties directly.

Let us look at an example of creating objects using this method :
**var obj = {
member1 : value1,
member2 : value2,
};**
These members can be anything — strings, numbers, functions, arrays or even other objects. An object like this is referred to as an object literal. This is different from other methods of object creation which involve using constructors and classes or prototypes, which have been discussed below.

Object Constructor : Another way to create objects in JavaScript involves using the “Object” constructor. The Object constructor creates an object wrapper for the given value. This, used in conjunction with the “new” keyword allows us to initialize new objects.
Example :
**const school = new Object();
school.name = ‘Vivekanada school’;
school.location = ‘Delhi’;
school.established = 1971;
school.displayInfo = function(){
console.log(${school.name} was established
in ${school.established} at ${school.location});
}
school.displayInfo();**

Output:
The two methods mentioned above are not well suited to programs that require the creation of multiple objects of the same kind, as it would involve repeatedly writing the above lines of code for each such object. To deal with this problem, we can make use of two other methods of object creation in JavaScript that reduces this burden significantly, as mentioned below:

### Constructors: 

Constructors in JavaScript, like in most other OOP languages, provides a template for creation of objects. In other words, it defines a set of properties and methods that would be common to all objects initialized using the constructor.

Let us see an example :
**function Vehicle(name, maker) {
this.name = name;
this.maker = maker;
}
let car1 = new Vehicle(‘Fiesta’, ‘Ford’);
let car2 = new Vehicle(‘Santa Fe’, ‘Hyundai’)
console.log(car1.name); // Output: Fiesta
console.log(car2.name); // Output: Santa Fe**

Output:
Notice the usage of the “new” keyword before the function Vehicle. Using the “new” keyword in this manner before any function turns it into a constructor. What the “new Vehicle()” actually does is :
It creates a new object and sets the constructor property of the object to schools (It is important to note that this property is a special default property that is not enumerable and cannot be changed by setting a “constructor: someFunction” property manually).

Then, it sets up the object to work with the Vehicle function’s prototype object ( Each function in JavaScript gets a prototype object, which is initially just an empty object but can be modified.The object, when instantiated inherits all properties from its constructor’s prototype object).

Then calls Vehicle() in the context of the new object, which means that when the “this” keyword is encountered in the constructor(vehicle()), it refers to the new object that was created in the first step.
Once this is finished, the newly created object is returned to car1 and car2(in the above example).

Inside classes, there can be special methods named constructor().
**class people {
constructor()
{
this.name = “Adam”;
}
}
let person1 = new people();
// Output : Adam
console.log(person1.name);**

Output:
Having more than one function in a class with the name of constructor() results in an error.

### Prototypes : 

Another way to create objects involves using prototypes. Every JavaScript function has a prototype object property by default(it is empty by default). Methods or properties may be attached to this property. A detailed description of prototypes is beyond the scope of this introduction to objects.

However you may familiarize yourself with the basic syntax used as below:
let obj = Object.create(prototype_object, propertiesObject)
// the second propertiesObject argument is optional
An example of making use of the Object.create() method is:
**let footballers = {
position: “Striker”
}
let footballer1 = Object.create(footballers);
// Output : Striker
console.log(footballer1.position);**

Output:
In the above example footballers served as a prototype for creating the object “footballer1”.

All objects created in this way inherits all properties and methods from its prototype objects. Prototypes can have prototypes and those can have prototypes and so on. This is referred to as prototype chaining in JavaScript. This chain terminates with the Object.prototype which is the default prototype fallback for all objects. Javascript objects, by default, inherit properties and methods from Object.prototype but these may easily be overridden. It is also interesting to note that the default prototype is not always Object.prototype.For example Strings and Arrays have their own default prototypes — String.prototype and Array.prototype respectively.

## Accessing Object Members

Object members(properties or methods) can be accessed using the
dot notation :
**(objectName.memberName)
let school = {
name : “Vivekanada”,
location : “Delhi”,
established : 1971,
20 : 1000,
displayinfo : function() {
console.log(${school.name} was established
in ${school.established} at ${school.location});
}
}
console.log(school.name);
console.log(school.established);**

Output:
Bracket Notation :
**objectName[“memberName”]
let school = {
name : “Vivekanada School”,
location : “Delhi”,
established : 1995,
20 : 1000,
displayinfo : function() {
document.write(${school.name} was established
in ${school.established} at ${school.location});
}
}
// Output : Vivekanada School
console.log(school[‘name’]);
// Output: 1000
console.log(school[‘20’]);**

Output:
Unlike the dot notation, the bracket keyword works with any string combination, including, but not limited to multi-word strings.

For example:
somePerson.first name // invalid
somePerson[“first name”] // valid
Unlike the dot notation, the bracket notation can also contain names which are results of any expressions variables whose values are computed at run-time.
For instance :
let key = “first name” somePerson[key] = “Name Surname”
Similar operations are not possible while using the dot notation.










