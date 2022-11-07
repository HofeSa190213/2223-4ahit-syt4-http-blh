# HTTP

## Hypertext Transfer Protocol

Laher Benedikt - Breuer Mario - Hofer Samuel

-----

# About HTTP

---

- Stateless application-layer protocol
- Request are sent, response are received over TCP/IP layer
- Foundation oft he modern web
- simultaneously requests 

---

## since version http/2.0

- simultaneously requests 
- less latency 
- Cuts down time required to load a page

-----

# URL

URLs identify the specific host the client wants to communicate with

---

## Example

![image](https://user-images.githubusercontent.com/71715472/200410363-735d3771-d314-4603-9dbe-3e1517941011.png)

- https specifies the protocol. It can be http or https, which makes the communication secure
- www.domain.com is the host
- 1234 is the port. In many cases, the browser hides the port. The default is 80
- path/to/resource is the resource path. It helps the server identify a specific resource and generate the right response
- ?a=b&x=y are query string parameters. Query string parameters are used by the server to spot the right resource

-----

# Requests & Response

---

# Requests

Requests are made up of the following parts

- **Request line**: says what’s being requested. Consist of a verb, a path, and the Http version
- **Headers**: additional information about requester, message, communication format
- **Body**: it is optional. The content of the request. Separated from the header by a blank line

---

## HTTP Request Methods

- **GET**: fetch a resource from the server
- **POST**: create a new resource
- **PUT**: update an existing resource
- **DELETE**: delete an existing resource

---

## HTTP Headers

give the server information about the sender

- **Chache-Control**: directive, that controls the caching
- **Connection**: decides, if the network connection should be open or closed
- **Trailer**: tells the server, that it can append metadata
- **Transfer-encoding**: determs the encoding of the data from the server

---

Here's a typical HTTP request: 
<br>
![image](https://user-images.githubusercontent.com/71715472/200413459-d7b69a3b-bad5-44b0-9496-a684d1739744.png)

---

# Response

- **Status Line**: tells us, if the request succeeded or not 
- **Headers**: additional information about the response
- **Body**: the content of the response

---

## Response Headers

- **Age**: time, when the message was generated on the server
- **ETag**: the MD5 hash to check for modification
- **Location**: used when sending a redirection and contains the new URL
- **Server**: identifies the server generating the message

-----

# Status Code

client can interpret the server response, every response will have an status code

---

## Type of status code

- **1xx**: Informational Messages
  - Can send an Except
- **2xx**: Successful
  - Tells the client that it was successfully 
- **3xx**: Redirection
  - 301 Moved Permanently: the resource is now located at a new URL   
  - 303 See Other: the resource is temporarily located at a new URL
  - 304 Not Modified: the server has determined that the resource has not changed and the client should use its cached copy 
- **4xx**: Client Error
  - When server thinks it’s the fault of the client
- **5xx**: Server Error
  - Used to indicate a server failure while processing the request

-----

# Tools to view HTTP Traffic

---

- Chrome Webkit inspector: 
  - Lot of information about HTTP response and request
- web debugging proxies (Fiddler, Charles Proxy, OSX)
- Command Line (curl, tcpdump, tshark)
  - Used for monitoring the HTTP traffic

---

## Chrome Webkit inspector

![image](https://user-images.githubusercontent.com/71715472/200420405-4b142fee-517d-4d72-aea4-50867b1c61b9.png)

---

## Fiddler

![image](https://user-images.githubusercontent.com/71715472/200420488-51076a64-de22-4ae4-afe9-4fe7f2a4c1cb.png)

-----

# Using HTTP in Web Frameworks and Libraries

---

- Express(Node.js)
  - Provides simple API for writing web servers 

![image](https://user-images.githubusercontent.com/71715472/200420682-c58f5e4b-203f-471b-a610-ea427c9bbd07.png)

-----

# Sending an HTTP Request With the Fetch API

---

- two methods: 
  - jQuery
  - modern browsers have built-in Fetch API

---

## GET Requests With Fetch

**fetch(**"https://example.com/something.html"**)** --> returns a promise, which you can **await** to get a response

![image](https://user-images.githubusercontent.com/71715472/200421153-a9b5d8c3-89c2-4f49-98ca-5b6fb1b8678e.png)

---

## POST Requests With Fetch
**fetch(**'https://example.com/profile', {  method: 'POST'}**)** --> post data with an optional payload and returns a promise, which you can **await** to get a response

![image](https://user-images.githubusercontent.com/71715472/200421581-44352c39-b5be-44ef-826d-8685fb31a8d6.png)

-----

# SOURCES

https://code.tutsplus.com/tutorials/http-the-protocol-every-web-developer-must-know-part-1--net-31177
https://developer.mozilla.org/en-US/docs/Web/HTTP
