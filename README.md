# Hypermedia Notes

## Overview

This contains my notes about designing hypermedia APIs.

Currently the notes are very brief and mostly this is a list of pre-defined formats and specs that
can make up an API design.

## Design Process

See [RESTful Web APIs](http://restfulwebapis.com) for a thorough description of the design process.

* [A Web API Design Methodology](https://www.infoq.com/articles/web-api-design-methodology) (article)
* [API Design Methodology](https://www.infoq.com/presentations/api-design-methodology) (presentation video)

## Design Goals

* Linking and forms to advertise possible next states (requests)
* Reference data resources where helpful in making next-requests
* Clearly define link relations
* Clearly identify and describe profiles/message-types

## Design Elements

### Hypermedia types

Provide hypermedia factors and leave room to layer on application-specific semantics.

* [UBER](http://rawgit.com/uber-hypermedia/specification/master/uber-hypermedia.html)
* [HAL](https://tools.ietf.org/html/draft-kelly-json-hal-07)
* [Siren](https://github.com/kevinswiber/siren)
* [Mason](https://github.com/JornWildt/Mason)
* [JSON-LD](http://json-ld.org): JSON for Linking Data
* [Hydra](http://www.markus-lanthaler.com/hydra): Hypermedia-Driven Web APIs
* [JSON API](http://jsonapi.org)
* [Home Documents for HTTP APIs](http://tools.ietf.org/html/draft-nottingham-json-home-03)
* XLink
* XForms
* [HAL Forms](http://mamund.site44.com/misc/hal-forms/)
* RDF

### Application-specific media types

Types that fully define specific applications. They may still make good base types for other
applications that further specialize what they define.

* [The Atom Publishing Protocol](https://tools.ietf.org/html/rfc5023)
* [The Atom Syndication Format](https://tools.ietf.org/html/rfc4287)
* [Collection+JSON](http://amundsen.com/media-types/collection)
* [JSON Patch](http://tools.ietf.org/html/rfc6902)
* [OData](http://www.odata.org)
* [OpenSearch](http://www.opensearch.org)
* [Problem Details for HTTP APIs](https://tools.ietf.org/html/draft-ietf-appsawg-http-problem-00)
* [Status Documents for HTTP Resources](https://github.com/tavis-software/Tavis.Status)
  * Operational Status
  * Health checks?

### Machine-readable message-type descriptions / profiles

* [ALPS](http://alps.io/spec/index.html)
* [Hyperdescribe](https://github.com/smizell/hyperdescribe)
* [JSON Schema](http://json-schema.org)
* RDF Schema
* [Open API Initiative](https://openapis.org)

#### Modeling

These usually generate some combination of documentation, server, and client. This is not the same
thing as message-type descriptions and profiles, as these are meant to describe those things on
specific trees of URLs. This usually (always) means a specific server or implementation.

* [Swagger](http://swagger.io)
* [RAML](http://raml.org)
* [Blueprint](https://apiary.io/blueprint)
* [I/O Docs](https://github.com/mashery/iodocs)

### Supporting specs

* [Web Linking](https://tools.ietf.org/html/rfc5988)
* [URI Template](https://tools.ietf.org/html/rfc6570)
* [CURIES](http://www.w3.org/TR/curie)
* [JSON Reference](http://tools.ietf.org/html/draft-pbryan-zyp-json-ref-03)
* [HTTP API Specs](https://pmhsfelix.github.io/http-api-specs/)

## Implementation Support

### Frameworks

* [NARWHL](http://www.narwhl.com)
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
* [APIMAN](http://www.apiman.io/latest/)
* [Amazon API Gateway](https://aws.amazon.com/api-gateway/)

## Resources

### Concepts

* [Web Concepts](http://webconcepts.info)
* [Microservice architecture](http://microservices.io)
  * Including patterns and other resources
* [H-Factors](http://amundsen.com/hypermedia/hfactor)

### Design advice

* [HTTP API Design Guide](https://github.com/interagent/http-api-design/blob/master/README.md)

### Type registries

* [IANA Media Types](http://www.iana.org/assignments/media-types/media-types.xhtml)
* [IANA Link Relations](http://www.iana.org/assignments/link-relations/link-relations.xhtml)
* [Additional Link Relations](https://tools.ietf.org/html/rfc6903)
* [ALPS registry](http://alps.io)
* [schema.org](http://schema.org)
* [Microformats Wiki](http://microformats.org/wiki/Main_Page)

### Service registries

* [API Commons](http://apicommons.org)
* [API Search](http://apis.io)
