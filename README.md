# Rest

What is REST?

    Representational State Transfer (REST) is a software architecture style for building scalable web services.
    
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
      
    Cacheable
    
      As on the World Wide Web, clients and intermediaries can cache responses.
      
      Responses must therefore, implicitly or explicitly, define themselves as cacheable, or not, to prevent clients from reusing stale or inappropriate data in response to further requests. 
      
      Well-managed caching partially or completely eliminates some client–server interactions, further improving scalability and performance.
      
    
