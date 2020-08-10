# Reading 07 - REST

## A conversation about REST
HTTP tells the browser what protocol to use.

REST provides a definition of a “resource”, which is what those things point to.

A web page is a “representation” of a resource.

REST - REpresentational State Transfer.
It is an architectural style for providing standards between computer systems on th web, making it easier for systems to communicate with each other.

HTTP—this protocol Fielding and his friends created—is all about applying verbs to nouns. For instance, when you go to a web page, the browser does an HTTP GET on the URL you type in and back comes a web page.

Each of the systems would retrieve information from each other using a simple HTTP GET. If one system needs to add something to another system, it would use an HTTP POST. If a system wants to replace something in another system, it uses an HTTP PUT, or, to do a partial update, it'll hopefully use PATCH.

## What Google learned from its Quest to Build the Perfect Team
Amazing article.  Will reread it over and over in the years to come. 

## SuperAgent
SuperAgent is light-weight progressive ajax API crafted for flexibility, readability, and a low learning curve after being frustrated with many of the existing request APIs.

Request Basics
A request can be initiated by invoking the appropriate method on the request object, then calling .then() (or .end() or await) to send the request.

Setting header fields
Setting header fields is simple, invoke .set() with a field name and value.

GET requests
The .query() method accepts objects, which when used with the GET method will form a query-string.

HEAD requests
You can also use the .query() method for HEAD requests.

POST / PUT requests
Setting the Content-Type
Serializing request body
SuperAgent will automatically serialize JSON and forms. You can setup automatic serialization for other types as well.
Retrying requests - When given the .retry() method.
Setting Accept - the .type() method it is also possible to set the Accept header via the short hand method .accept().
Query strings - req.query(obj) is a method which may be used to build up a query-string.
TLS options - In Node.js SuperAgent supports methods to configure HTTPS
Aborting requests - To abort requests simply invoke the req.abort() method.

Timeouts - You should use both deadline and response timeouts. This way you can use a short response timeout to detect unresponsive networks quickly, and a long deadline to give time for downloads on slow, but reliable, networks. Note that both of these timers limit how long uploads of attached files are allowed to take. Use long timeouts if you're uploading files.

Authentication - In both Node and browsers auth available via the .auth() method.

Saving cookies - In Node SuperAgent does not save cookies by default, but you can use the .agent() method to create a copy of SuperAgent that saves cookies.

Piping Data - The Node client allows you to pipe data to and from the request. Please note that .pipe() is used instead of .end()/.then() methods.
Note that when you pipe to a request, superagent sends the piped data with chunked transfer encoding, which isn't supported by all servers (for instance, Python WSGI servers).

Multipart requests
SuperAgent is also great for building multipart requests for which it provides methods .attach() and .field().
When you use .field() or .attach() you can't use .send() and you must not set Content-Type (the correct type will be set for you).

Promise and Generator support
SuperAgent's request is a "thenable" object that's compatible with JavaScript promises and the async/await syntax.

Browser and node versions
SuperAgent has two implementations: one for web browsers (using XHR) and one for Node.JS (using core http module). By default Browserify and WebPack will pick the browser version.

If want to use WebPack to compile code for Node.JS, you must specify node target in its configuration.
