# 🔮 Express 

 - [CLIENT-SERVER](#CLIENT-SERVER)
 - [RESOURCE](#resource-----gives-you-the-data-img-test-html-temperary-serves)

# RESTful API

# REST CONSTRAINTS 
- Once a developer becomes familiar with one of your API, he should be able to follow the similar approach for other APIs.

# 1. UNIFORM INTERFACE  

The uniform interface that any REST services must provide is fundamental to its
design. Its constraint defines the interface between clients and servers.
The four guiding principles of the uniform interface are:
1. Resource-Based
2. Actions on Resources Through Representations
3. Self-descriptive Messages
4. Hypermedia as the Engine of Application State

# 2. CLIENT-SERVER

Servers and clients may also be replaced and developed independently, as long
as the interface between them is not altered.

# 3. STATELESS 

No client context shall be stored on the server between requests. 
The client is responsible for managing the state of the application.


# 4. CACHEABLE 

Well-managed caching partially or completely eliminates some client-server
interactions, further improving scalability and performance.

- on seccess response from the server, we can store User info for 24 hours,   (or 400/500 can be too )
- in heder we can set time (..)  in Express
- with Redis, or Nginx/Express 

# 5. LAYERED SYSTEM  (Routers)

Custom Domain in API Gateway api.exapmle.com -> Amazon API -> /auth -> Authentication Service  


# 6. CODE ON DEMAND (OPTIONAL)  - truly RESTful API
All above constraints help you build a truly RESTful API and you should follow
them. Still, at times you may find yourself violating one or two constraints. Do not
worry, you are still making a RESTful API – but not “truly RESTful”.


#  RESOURCE  -  gives you the data (img. test, html, temperary serves)

The key abstraction of information in REST is a resource. Any information that
can be named can be a resource: a document or image, a temporal service (e.g.
“today’s weather in Los Angeles”), a collection of other resources, a non-virtual
object (e.g. a person), and so on. In other words, any concept that might be the
target of an author’s hypertext reference must fit within the definition of a
resource. A resource is a conceptual mapping to a set of entities, not the entity
that corresponds to the mapping at any particular point in time.

Roy Fielding’s


 1) COLLECTION   /customers   
-   * customers will return data  Array / or empty Array 
- 

 2) SINGLETON      /manager
- 1. go get 1 user by id 
- 2. only 1 json data should be


3) SINGLETON      /customers/{customerId} ✅

 4) SUB-COLLECTION /customers/{customerId}/accounts
- shoud return Array

 5) SUB-COLLECTION /customers/{customerId}/accounts/{accountId}

# ENTITIES 
    � Document
    � Collection
    � Store
    � Controller


mock- http://api.example.com/user-management/users/{id}

# DOCUMENT

" Это список из нескольких ресурсов
# Может содержать ресурсы
� Может содержать список эндпоинтов
