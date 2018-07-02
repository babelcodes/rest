# REST - REpresentational State Transfer

- modèle de maturité de Richardson
  - 0 : un seul point d'entrée pour communiquer avec l'API (ex `api`) et un seule verbe HTTP `POST`
  - 1 : une URI pour chaque ressource et un verbe pour chaque action (CRUD => POST, GET, PUT et DELETE) plus un code retour

## REST Architectural Constraints

1. ___Client–server___ – separating user interface & data storage => improve user interface portability (across multiple platforms) and scalability (by simplifying the server components).
1. ___Stateless___ – Each request (from client to server) must contain all of the information (necessary to understand the request), and cannot take advantage of any stored context on the server. Session state is therefore kept entirely on the client.
1. ___Cacheable___ – Cache constraints require that the data within a response to a request be implicitly or explicitly labeled as cacheable or non-cacheable (If a response is cacheable, then a client cache is given the right to reuse that response data for later, equivalent requests).
1. ___Uniform interface___ – By applying the software engineering principle of generality to the component interface, the overall system architecture is simplified and the visibility of interactions is improved. In order to obtain a uniform interface, multiple architectural constraints are needed to guide the behavior of components. REST is defined by four interface constraints: 
   1. identification of resources
   1. manipulation of resources through representations
   1. self-descriptive messages
   1. hypermedia as the engine of application state
1. ___Layered system____ – The layered system style allows an architecture to be composed of hierarchical layers by constraining component behavior such that each component cannot “see” beyond the immediate layer with which they are interacting.
1. ___Code on demand___ (optional) – REST allows client functionality to be extended by downloading and executing code in the form of applets or scripts. This simplifies clients by reducing the number of features required to be pre-implemented.


## Resource

- Any information that can be named can be a ___resource___
- REST uses a ___resource identifier___ to identify the particular resource involved in an interaction between components.
- The state of resource at any particular timestamp is known as ___resource representation___ (data, metadata and hypermedia links)
- The data format of a representation is known as a ___media type___