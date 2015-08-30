# Rest

What is REST?

    Representational State Transfer (REST) is a software architecture style for building scalable web services.
    
    REST is web standards based architecture and uses HTTP Protocol for data communication. It revolves around resource where
    
    every component is a resource and a resource is accessed by a common interface using HTTP standard methods. 
    
    In REST architecture, a REST Server simply provides access to resources and REST client accesses and presents the
    
    resources. Here each resource is identified by URIs/ global IDs. REST uses various representations to represent a resource
    
    like text, JSON and XML. Now a days JSON is the most popular format being used in web services.
    
    HTTP Methods:
    
        Following well known HTTP methods are commonly used in REST based architecture.

        GET - Provides a read only access to a resource.

        PUT - Used to create a new resource.

        DELETE - Used to remove a resource.

        POST - Used to update a existing resource or create a new resource.

        OPTIONS - Used to get the supported operations on a resource.
    
a REST service is:

    Platform-independent (you don't care if the server is Unix, the client is a Mac, or anything else),
    
    Language-independent (C# can talk to Java, etc.),
    
    Standards-based (runs on top of HTTP), and Can easily be used in the presence of firewalls.

Architectural constraints

    Client–server:

      A uniform interface separates clients from servers. This separation of concerns means that, for example, clients are not concerned with data storage, which remains internal to each server, so that the portability of client code is improved. 
      
      Servers are not concerned with the user interface or user state, so that servers can be simpler and more scalable. Servers and clients may also be replaced and developed independently, as long as the interface between them is not altered.
      
    Stateless:
    
      By stateless it means that the web server does not store any state about the client application/session state. The session is stored on the client. 
      
      The server is stateless means that every server can service any client at any time, there is no session affinity or sticky sessions. The relevant session information is stored on the client and passed to the server as needed.
      
      The client's application state should never be stored on the server, but passed around from the client to every place that needs it.
      
      That is where the ST in REST comes from, State Transfer. You transfer the state around instead of having the server store it. This is the only way to scale to millions of concurrent users.

      The load of session management is amortized across all the clients, the clients store their session state and the servers can service many orders of magnitude or more clients in a stateless fashion.
      
    Advantages of Statelessness:
    
        Following are the benefits of statelessness in RESTful web services

            Web services can treat each method request independently.

            Web services need not to maintain client's previous interactions. It simplifies application design.

            As HTTP is itself a statelessness protocol, RESTful Web services work seamlessly with HTTP protocol.
            
    Disadvantages of Statelessness:
    
            Following are the disadvantages of statelessness in RESTful web services

            Web services need to get extra information in each request and then interpret to get the client's state in case
            
            client interactions are to be taken care of.
      
    Cacheable
    
      As on the World Wide Web, clients and intermediaries can cache responses.
      
      Responses must therefore, implicitly or explicitly, define themselves as cacheable, or not, to prevent clients from reusing stale or inappropriate data in response to further requests. 
      
      Well-managed caching partially or completely eliminates some client–server interactions, further improving scalability and performance.
      
What is a Resource?

    REST architecture treats every content as a resource. These resources can be text files, html pages, images, videos or
    
    dynamic business data. REST Server simply provides access to resources and REST client accesses and modifies the
    
    resources. Here each resource is identified by URIs/ global IDs. REST uses various representations to represent a resource
    
    where text, JSON, XML. XML and JSON are the most popular representations of resources.
    
URL format: 
    
    Each resource in REST architecture is identified by its URI, Uniform Resource Identifier. A URI is of following format:

    <protocol>://<service-name>/<ResourceType>/<ResourceID>
    
HTTP Request:

    A HTTP Request has five major parts:

        Verb- Indicate HTTP methods such as GET, POST, DELETE, PUT etc.

        URI- Uniform Resource Identifier (URI) to identify the resource on server

        HTTP Version- Indicate HTTP version, for example HTTP v1.1 .

        Request Header- Contains metadata for the HTTP Request message as key-value pairs. For example, client ( or browser)         type, format supported by client, format of message body, cache settings etc.

        Request Body- Message content or Resource representation.
        
HTTP Response:
    A HTTP Response has four major parts:

        Status/Response Code- Indicate Server status for the requested resource. For example 404 means resource not found and         200 means response is ok.

        HTTP Version- Indicate HTTP version, for example HTTP v1.1 .

        Response Header- Contains metadata for the HTTP Response message as key-value pairs. For example, content length,            content type, response date, server type etc.
        
             Header & Description: 
             
                Date  
                
                Date and Time of the resource when it was created.
                
                Last Modified
                	
                Date and Time of the resource when it was last modified.
                
                Cache-Control: 
                	
                Primary header to control caching.
                
                    Public: Indicates that resource is cachable by any component.
                    
                    Private: Indicates that resource is cachable by only client and server, no intermediary can cache the
                    resource.
                    
                    no-cache/no-store: Indicates that resource is not cachable
                    
                    max-age: Indicates the caching is valid up to max-age in seconds. After this, client has to make another                     request.
                
                Expires
                	
                Expiration date and time of caching
                
                Age
                	
                Duration in seconds from when resource was fetched from the server.

        Response Body- Response message content or Resource representation.
        
   
    

    

      

      

      
    
