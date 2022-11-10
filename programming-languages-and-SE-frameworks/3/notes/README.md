# Architecture - Part 1

## Web applications
* Every request contains distinct components
  * Address - (www.Google.com)
  * Method - (GET, PUT, DELETE and POST)
  * All methods may include data except GET.
* Enables components in our system to communicate with each other in a
  structured way.
* Every HTTP response contains status code
  * 200-299 indicate success
  * 400-499 problems with the request
  * 500-600 problems with the server
* A response receives a response code and also may contain a payload.
* Original web apps were designed to return documents.
* Browser was used to retrieve the responded document.
* JavaScript allows for dynamic web. Can also make additional data
  async.

## REST API
* REST: Representational State Transfer
* Defines a set of constraints for web services
* Should be scalable allowing support for large number of components.
* Allow for components to change will application is running (continuous
  integration)
* REST API can work together
* The most widely used standard is OpenAPI

## Architecture
* Organisational structure of software.
* How we are arranging components and how they interact.
* How we can create a single cohearant application.
* A general, reusable solution to a commonly occurring problem in
  software architecture within a given context.
* We are not concerned with the implementation stages yet.
* More about being able to respond to a common set of problems with a
  shape or form that we can apply over and over.
* We can then make specific implementations that follow those rules to
  start solving those problems.
* Patterns are not mutually exclusive.
  * We can combine several patterns if required.
  * We may have one part that suits one pattern ect.
* Patterns should be chosen based on requirements.
* Should be able to understand problem domain and understand how to
  apply different patterns to balance performance and  security ect.

## Client-server
* Client sends requests and servers return a response to the client
* Examples include: Email clients, web browser and mobile app.
* This does not always have to happen over a network. The server and
  client can be on the same computer.
* Same with a graphics card. The CPU is the server and gpu is the
  client.
* Convenient way to split up responsibility in our system and make sure
  that  our application is less fragile. We can update the client
  without needing to update the server.

##Peer to peer
* Communication is done together.
* All nodes are the same.
* Example is a file sharing server.
  * Requires dependability
  * Redundancy - can retrieve files from another node if one node is
    down.
* Highly critical systems make use of peer to peer such as space flight.
* No one centralised point will stop the system from working.
* Typically slower.
  * Requires to negotiate a transaction to identify where we are
    sending.
  * To ensure we access the right node or calculate the closest node.
  * Need to communicate which node has the data on the network.
* More complicated because there is no centralised point.
  * No clear defined roles and responsibilities.
* Every part of the application is carrying out the same roles.
* Temporal effects: One node may flicker between online and off line.
* Requires data to be shared. One node may be dependant if only that one
  node has the required data.

##Master - slave
* Useful for carrying out large processing activity that cannot be
  achieved on a single machine.
* All slave machines will do the same operation but on different set of
  operations.
* The master will coordinate and administrate the jobs on the slave
  nodes.
* Master combines results
* Database replication is one example. Master holds the authority of the
  node and the slaves hold localised replicas.
  * The master can restore from the appropriate slave.
* `SETI@Home` - project allows for people to volunteer idle computer
  time to SETI's massive data processing.
    * The master node decides which data to send to the slaves
    * The slaves will process it.
    * The salves then will send the result back to the master
    * The master combines the results to its main database
* Another example will be boinc from berkely to donate computing power
  to help computer research.

## Layered architecture
* Common for business applications to use layered architecture.
  * Business applications consist of layers that start with the user
    data, apply processing and present the data to the clients
* User events filter from top to bottom.
* Presentation tier- implements user interface
* Application tier- communication over a network. Handles information
  over the network to ensure that the downstream data is being passed up
  stream.
* Logic tier - Main rules of the business. How to interpret the data in
  a way that is useful. Data processing / transforming. Logic lay passes
  data to application tier
* Data tier - Data base communication.
* Can manage security effective. Because out logic tier is communicating
  with our data tier. We can ensure that we can apply permissions based
  on the tier before it is exposed to the network.
* Emphasises a separation of concerns.
* Changes will involve changing a tier without affecting other tiers.
* Rely on discipline to maintain structure.
* Down to our professional judgement because there is nothing in the
  language itself that prevents us from skipping layers.
* It is common to have pass through methods to layers. If there is no
  logic to be performed, it is a method that just calls the lower layer.
* To many methods like this can be difficult to maintain.
* Could get dependency issues if we communicate across components.

##Vertical slice
* Each layer has a set of responsibilities.
  * The responsibilities define different roles within the layer.
* We can align the roles vertically to see how they communicate.
* We have to consider if we require communication between slices if they
  are related to each other like Job and application.
