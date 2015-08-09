# Hypermedia Notes

## Overview

This contains my notes about designing hypermedia APIs.

Currently the notes are very brief and mostly this is a list of pre-defined formats and specs that
can make up an API design.

## Design Process

See [RESTful Web APIs](http://restfulwebapis.com) for a thorough description of the design process.

## Design Goals

* Linking and forms to advertise possible next states (requests)
* Reference data resources where helpful in making next-requests
* Clearly define link relations
* Clearly identify and describe profiles/message-types

## Design Elements

### Base media types

Provide hypermedia factors and leave room to layer on application-specific semantics.

* [UBER](http://rawgit.com/uber-hypermedia/specification/master/uber-hypermedia.html)
* [HAL](https://tools.ietf.org/html/draft-kelly-json-hal-07)
* [Siren](https://github.com/kevinswiber/siren)
* [Mason](https://github.com/JornWildt/Mason)
* [JSON-LD](http://json-ld.org): JSON for Linking Data
* [Hydra](http://www.markus-lanthaler.com/hydra): Hypermedia-Driven Web APIs
* [JSON API](http://jsonapi.org)
* [Collection+JSON](http://amundsen.com/media-types/collection)
* [OData](http://www.odata.org)

### Application-specific media types

Types that fully define specific applications.

* [The Atom Syndication Format](https://tools.ietf.org/html/rfc4287)

### Machine-readable message-type descriptions / profiles

* [ALPS](http://alps.io/spec/index.html)
* [Hyperdescribe](https://github.com/smizell/hyperdescribe)

### Supporting types

* [Problem Details for HTTP APIs](https://tools.ietf.org/html/draft-ietf-appsawg-http-problem-00)
* [Home Documents for HTTP APIs](http://tools.ietf.org/html/draft-nottingham-json-home-03)
* [APIS.json](http://apisjson.org)
* [Status Documents for HTTP Resources](https://github.com/tavis-software/Tavis.Status)
  * Operational Status
  * Health checks?
* [JSON Patch](http://tools.ietf.org/html/rfc6902)
* [JSON Schema](http://json-schema.org)

### Other supporting specs

* [Web Linking](https://tools.ietf.org/html/rfc5988)
* [URI Template](https://tools.ietf.org/html/rfc6570)
* [CURIES](http://www.w3.org/TR/curie)
* [JSON Reference](http://tools.ietf.org/html/draft-pbryan-zyp-json-ref-03)

## Implementation Support

### Modeling

These usually generate some combination of documentation, server, and client. This is not the same
thing as message-type descriptions and profiles, as these are meant to describe those things on
specific trees of URLs. This usually (always) means a specific server or implementation.

* [RAML](http://raml.org)
* [Blueprint](https://apiary.io/blueprint)
* [I/O Docs](https://github.com/mashery/iodocs)

### Frameworks

* [NARWHL](http://www.narwhl.com)
* [Swagger](http://swagger.io)
* [Core API](http://www.coreapi.org)

I find opinionated API frameworks to be detrimental. They never or rarely make clients and servers
equals in the resulting services. It probably takes modelling (see above) to do this and from there
a server framework could/should be minimal (e.g., [sinatra](http://www.sinatrarb.com),
[morepath](http://morepath.readthedocs.org), [spark](http://sparkjava.com)).

### Service gateways and management layers

* [Kong](https://getkong.org)
* [Tyk](https://tyk.io)
* [Consul](https://consul.io)
* [API Umbrella](http://apiumbrella.io)

## Resources

### Concepts

* [H-Factors](http://amundsen.com/hypermedia/hfactor)

### Design advice

* [HTTP API Design Guide](https://github.com/interagent/http-api-design/blob/master/README.md)

### Type registries

* [IANA Media Types](http://www.iana.org/assignments/media-types/media-types.xhtml)
* [IANA Link Relations](http://www.iana.org/assignments/link-relations/link-relations.xhtml)
* [Additional Link Relations](https://tools.ietf.org/html/rfc6903)
* [ALPS registry](http://alps.io)
* [schema.org](http://schema.org)

### Service registries

* [API Commons](http://apicommons.org)
* [API Search](http://apis.io)