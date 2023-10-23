# Request/Response: Client-Side: <br> How a Browser Handles Requests/Responses

In the context of web communication, 'client-side' refers to the part of an app/website that is displayed or run on the client, i.e., end-user’s device

On the client-side, the browser acts as the agent handling the communication between the user and web servers, termed 'requests and responses'

A series of events take place before the web content requested by the user is made accessible to them

## Step-by-Step Overview

### 1. _User Input_

- The user interacts with the browser, by entering a URL (Uniform Resource Locator) in the browser's address bar, clicking a link, submitting a form, etc.

### 2. _URL Parsing_

- The browser parses the user input to extract the URL, which specifies the address of the resource requested by the user
- The browser checks to see if the URL is already stored in its cache (temporary storage) from previous visits to the same website
  - If yes, it retrieves the resource from the cache and renders it to the screen directly
  - If not, it proceeds to the next step

### 3. _DNS Resolution_

- The browser initiates a DNS (Domain Name System) lookup to translate the domain name in the URL into an IP (Internet Protocol) address, which enables the server hosting the resource requested to be located

### 4. _Initiating a Connection_

- Once the browser has the IP address, it establishes a TCP (Transmission Control Protocol) connection with the server at the IP address and the default HTTP (Hypertext Transfer Protocol) or HTTPS (Hypertext Transfer Protocol Secure) port
  - TCP ensures that the data that is transmitted between the client and server remains error-free

### 5. _Sending an HTTP Request_

- Once the connection is established, the browser sends an HTTP request to the server
  - The request includes info such as the HTTP method (`GET`, `POST`, `PUT`, `DELETE`, etc.), the resource requested (e.g., the path of the URL), headers containing info about the browser type and supported content types, as well as other info such as the user's language preferences

### 6. _Receiving an HTTP Response_

- The server processes the request and sends back an HTTP response
  - The response includes the requested resource, as well as other info including the status code of the request and the server's date and time
- HTTP responses are classified into 5 categories called 'status codes':
  - `1XX`: Informational
  - `2XX`: Success
  - `3XX`: Redirection
  - `4XX`: Client error
  - `5XX`: Server error

### 7. _Resource Retrieval & Page Rendering_

- The browser receives the response, parses it and starts rendering the web page
- To display the content properly, the browser may be required to parse the following:
  - HTML (Hypertext Markup Language), which defines the structure and actual content
  - CSS (Cascading Style Sheets), which defines the presentation and styling of the content
  - JS (JavaScript), which adds interactivity to the page
- In the case where there is an issue with the request/response, depending on the nature of the error (as indicated by the status code), the browser may display error messages or attempt to handle the error
