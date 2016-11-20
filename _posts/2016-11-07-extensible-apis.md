---
published: true
title: Extensible APIs
---
APIs are awesome. We need more of them.

## Every API is about something specific
Flickr is all about pictures. OpenTable is all about reservations, Twitter is all about short posts.
Generally, these are singleton APIs: only one of each type exists.
Some APIs have many hosts with a compatible API. Any host running the WordPress API can be used by any tools that speak that API. The MetaWeblog API is a good long-running example of a cross-platform common API in a common space.

What if we want an API that is about pictures, reservations, AND short posts? We need a new class of API.

### Extensible APIs are Composable Collections of APIs

A single API host can host many different types of APIs, while sharing common infrastructure.

Each API host can host the types of APIs needed for the entity it represents. The particular extensions chosen will depend on the type of entity and should be commonly shared with other APIs representing entities of the same type.

A BusinessHours API could be used by all types of businesses and could respond with information about... yep, business hours. A store might use that in addition to a ProductInventory API, while a restaurant might use it alongside a Menu API and a Reservation API.

The mix and match of API types allow easily interfacing with many different types of businesses with common code, and also allows multiple API definitions to be used simultaneously as new ones emerge and old ones are deprecated.

### Technical Thoughts

Extensible APIs allow the combination of many different APIs on the same host. 
Each API extension lives within a different namespace to avoid path conflicts.

A well-known discovery URL can return a list of extensions supported by the host.

Each namespaced API needs to conform to a spec, likely something like swagger.

Conventions can allow multiple APIs to share API keys on the same host.

Extensible APIs will enable many different systems to build to common API standards, without having to agree on absolutely everything.

### Critical Missing Infrastructure
I believe that Extensible APIs are required for distributed and independent systems. It is critical for healthy IOT ecosystems, and the growth of independent and distributed entities. Personal APIs are one type of Extensible API.

### Open Questions
- Is Extensible APIs the right name for this?
- How should namespaces be organized? Having a predictable namespace for a given API spec will make it easier to hit the specific extension you want.
- Linking namespace to an interface specification?
- What are the minimum behaviors that extensible APIs must support?