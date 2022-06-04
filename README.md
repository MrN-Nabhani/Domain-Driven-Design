# Domain-Driven-Design
Learning about DDD using courses, notes and code!


# Software Architecture: Domain-Driven Design
resource: https://www.linkedin.com/learning/software-architecture-domain-driven-design

* DDD works best with Micro-services, it can work with a monolith system, but although there is no physical seperation for domain, the seperation would be logical.
* Terminologies:
  * Context: each context holds a number of entites. It has a single responsibility and should be decoupled from other contexts.
  * Entity: entities must live in a single context, in DDD entities are represented by their roles (what they do) in the system, not by actors (who they are) e.g. the system doesn't care if a employee is taking the admin permission of a manager to issue a report. It cares that it is an authorised entity that can issue reports.
  * Portal entities: usually a single entity in a context that gives access to the aggregate of its context.
  * Aggregate: a set of entities that perform an action. A context might have more than one. 
  * Communication: in DDD communication happens inside a context, using its own ubiquitous language.
  * Ubiquitous language: the naming used inside a context, in terms of both nouns and verbs used. The language creates boundaries for the context. e.g. a book has a price inside a store and can be sold, but inside a warehouse a book has a shelf-number and can be boxed.


* Reactive vs Orchestrated/Declarative:
  *  Orchestrated means an entity tells another entity what to do.
  *  Reactive means entites react to an event happening in another system. Advantage: changes in downstream systems shouldn’t affect the upstead systems
