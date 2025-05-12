Monolith - Put everything into a single application
Microservice - Distributed by nature

Typical Application has:
- User interface
- Business Logic
- Database Access

For monolith, it is packaged and delivered as a single unit.

**Monolith**
For user interface, business logic, and database access, all have: transaction, payment, and logistic

Monolith Pros:
- easy source code navication )source code in one place)
- Easy debugging
- EAsy deployment
- Single node access is faster than distributed communication so it is performant

Monolith Cons:
- tightly coupled
- Limited knowledge
- Undesireable change
- Limited tech stack
- Since it's all one big module/codebase, it can be hard to change out any parts of the tech stack
- hard to scale

Microservice Pros:
- loos coupling
- knowledge maintenance (documentation)
- less udesirable changes
- change in tech stack is easier
- easy to scale

Microservice cons
- complexity increases a lot