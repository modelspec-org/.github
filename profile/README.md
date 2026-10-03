# ModelSpec

**Define your application data model once.**

ModelSpec is an open specification language for application data models. It
describes entities, their fields, types, keys and links in one place,
independently of the database, programming language, API layer or hosting
that will use them. You write a model in HCL; tools read its JSON form.

## Why a shared model helps

- **Start from a published model.** A new project can reuse a model someone
  has already written and checked, instead of designing its tables again.
- **Recognise the same data in different places.** When several hosters serve
  databases built on the same model, tools can tell they share one shape and
  treat them alike.
- **Run many databases of one model.** A service that gives every customer
  an isolated database can declare one model for all of them.

## Where ModelSpec sits

One database can be described by three layers, each answering one question:

| Layer | Question |
|---|---|
| [OVDB Directory](https://directory.openvaultdb.com) | Where is the data, who publishes it and how do I reach it? |
| **ModelSpec** | What shape is the data: entities, fields, types and links? |
| [MeaningGraph](https://meaninggraph.io) | What does the data mean? |

Meanings are attached to ModelSpec fields, and directory entries name the
model they implement, so one model connects every copy of the same data.
The worked example is the [Chinook sample database](https://github.com/datatug/chinookdb).

## Repositories

- [specscore/modelspec](https://github.com/specscore/modelspec): the
  specification, JSON schema and website ([modelspec.org](https://modelspec.org)).
- [registry](https://github.com/modelspec-org/registry): the public registry
  of published models, an inGitDB database on GitHub. Being built; its pages
  will be at [modelspec.org/registry](https://modelspec.org/registry/).

## Status

Preview. The language is usable and still changing; the registry is new.
