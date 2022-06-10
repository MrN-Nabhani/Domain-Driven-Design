# Domain-Driven-Design
Learning about DDD using courses, notes and code!


# Software Architecture: Domain-Driven Design
resource: https://www.linkedin.com/learning/software-architecture-domain-driven-design

* DDD works best with Micro-services, it can work with a monolith system, but although there is no physical seperation for domain, the seperation would be logical. Usually, choice microservices when you want independent deployability.
* Terminologies:
  * Context: each context holds a number of entites. It has a single responsibility and should be decoupled from other contexts.
  * Entity: entities must live in a single context, in DDD entities are represented by their roles (what they do) in the system, not by actors (who they are) e.g. the system doesn't care if a employee is taking the admin permission of a manager to issue a report. It cares that it is an authorised entity that can issue reports.
  * Portal entities: usually a single entity in a context that gives access to the aggregate of its context.
  * Aggregate: a set of entities that perform an action. A context might have more than one. 
  * Communication: in DDD communication happens inside a context, using its own ubiquitous language.
  * Ubiquitous language: the naming used inside a context, in terms of both nouns and verbs used. The language creates boundaries for the context. e.g. a book has a price inside a store and can be sold, but inside a warehouse a book has a shelf-number and can be boxed.


* Reactive vs Declarative:
  *  Declarative/Orchestrated means an entity tells another entity what to do.
  *  Reactive means entites react to an event happening in another system. Advantage: changes in downstream systems shouldn’t affect upstream systems

* Event Storming:
brain storming the timeline of the domains that are of interest to the business. Notes are used to represent the timeline:
  *  Event: of interest to the business.
  *  Action: what do we want to have happen.
  *  Questions: missing information that requires additional work.
  *  Policy: controls how the action plays out.
  *  Human activity: this might replace the event or action, basically a human was the cause.
  *  External System: outside the contexts or scope.

> Kullar Kert : the best way to understand events is the Special Theory of Relativity. In physics, and in particular relativity, an event is the instantaneous physical situation or occurrence associated with a point in spacetime (that is, a specific place and time). For example, a glass breaking on the floor is an event; it occurs at a unique place and a unique time. Strictly speaking, the notion of an event is an idealization, in the sense that it specifies a definite time and place, whereas any actual event is bound to have a finite extent, both in time and in space. In the information system Events are modeled as Messages so as to let interested parties know that an Event has indeed occurred with Space and Time information. Since Space and Time are relativistic this information transmission is complicated. For example GPS receivers need to correct for relativistic adjustment for the event messages they receive.

