# Request Header Parser

---

This microservice will be able to take in parameters related to a requested timestamp, and return a JSON formatted response with that timestamp
in UNIX and UTC formats.

The functionality will look something similar to [this](https://request-header-parser-microservice.freecodecamp.rocks/).

---

I will need an HTML landing page, and on that page a description of the service.
The user will then be able to browse to a URL _(i.e. http://<webpage>/api/whoami)_, then receive a JSON formatted response containing the request
header data.

---

### User Stories

| Story                                                         | Completed? |
| ------------------------------------------------------------- | ---------- |
| I can access a landing page with a description of the service | **YES**     |
| The service provides a JSON-formatted response                | **YES**    |
| The service provides the requester's IP address               | **YES**    |
| The service provides the requester's language                 | **YES**    |
| The service provides the requester's browser information      | **YES**    |

---

### Implementation

This project was easier than my previous ([Timestamp Service](https://github.com/sulfuroussquares/Timestamp-Service)), mostly because this is a simple matter of returning request header
information.

To display header request information, users must navigate to the `/api/whoami` extension from wherever the project is deployed to. I used a static express route to achieve this.

To return the header information in JSON format, I utilized express' `response.json()` method. The request information I pulled straight out of the GET request using a callback method as part of the `.get()` functionality in express.

---

---

#### Credit

The idea for this project (and base fork boilerplate with no functionality) comes from [FreeCodeCamp](https://www.freecodecamp.org/).  
I used [Glitch](https://glitch.com/) as a quick way to build/test a Node-based webapp without having to set up a local repository on my machine.

##### [Request Header Parser Microservice](https://www.freecodecamp.org/learn/apis-and-microservices/apis-and-microservices-projects/request-header-parser-microservice)
