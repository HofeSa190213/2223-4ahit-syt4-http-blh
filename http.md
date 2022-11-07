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

URLS identify the specific host the client wants to communicate with

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

- Request line: says what’s being requested. Consist of a verb, a path, and the Http version
- Headers: additional information about requester, message, communication format
- Body: it is optional. The content of the request. Separated from the header by a blank line

---

## HTTP Request Methods

- GET: fetch a resource from the server
- POST: create a new resource
- PUT: update an existing resource
- DELETE: delete an existing resource

---

## HTTP Headers

give the server information about the sender

- Chache-Control: directive, that controls the caching
- Connection: decides, if the network connection should be open or closed
- Trailer: tells the server, that it can append metadata
- Transfer-encoding: determs the encoding of the data from the server

---

Here's a typical HTTP request:
![image](https://user-images.githubusercontent.com/71715472/200413459-d7b69a3b-bad5-44b0-9496-a684d1739744.png)

---

# Response

- Status Line: tells us, if the request succeeded or not 
- Headers: additional information about the response
- Body: the content of the response

---

## Response Headers

- Age: time, when the message was generated on the server
- ETag: the MD5 hash to check for modification
- Location: used when sending a redirection and contains the new URL
- Server: identifies the server generating the message

-----

## Status Code

client can interpret the server response, every response will have an status code

---

## Type of status code

- 1xx: Informational Messages
  - Can send an Except
- 2xx: Successful
  - Tells the client that it was successfully 
- 3xx: Redirection
  - 301 Moved Permanently: the resource is now located at a new URL   
  - 303 See Other: the resource is temporarily located at a new URL
  - 304 Not Modified: the server has determined that the resource has not changed and the client should use its cached copy 
- 4xx: Client Error
  - When server thinks it’s the fault of the client
- 5xx: Server Error
  - Used to indicate a server failure while processing the request

-----

## Image Examples

### Link

![Github](https://pngimg.com/uploads/github/small/github_PNG67.png)

### Local

![LiTec-Logo](./img/LiTec-Logo.jpg)
