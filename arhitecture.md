---
marp: true
size: 4:3
theme: default
paginate: true
---

# Node Architecture

---

## *The code is the truth … but it’s not the entire truth.*

---

## *All models are wrong ...*

## *But some of them are useful.*

---

## What is architecture ? 

*The art of separation, grouping, abstraction, and hiding.*

Uncle Bob Martin

---

## What drives architecture ? 

The fulcrum of design decisions is change.

Separate those things that change for different reasons.

Group together those things that change for the same reason.

---

# There are a few questions we can ask and which will help us eliminate a lot of patterns that will not suit our needs.

---

## United or Separate ?

### Monolith vs Micro-services

---

## What is a Monolith approach ?

A single code-base which represents your entire project, it is deployed all at once (front and back) regardless if only one small part of it has been changed recently.

This is the traditional approach to how to architecture your project in terms of how split it should be, and is the default stance for most projects.

---

## Advantages

- easier re-use of code (no inter-application boundaries)

- less overhead 

- coding standards, DoD, procedures are easier to reuse

- higher cohesion in the projects code

---

## Disadvantages

- less freedom for the individual developer

- larger ramp-up needed

- higher coupling of the project's code

---

## What is the Micro-services approach ?

Micro-services are an architectural pattern in which the project is split up into smaller self standing project with each of them being responsible for a *single well defined* part of the overall project.

These micro services are treated as separate code-bases in and of themselves in regards to implementation, coding standards and deployment.

---

## Advantages

- immense flexibility for the developer to tackle problems in their own way

- project as a whole is safe guarded from one module failing

- greater feeling of ownership of the code thereby higher morale

---

## Disadvantages

- more overhead

- latency

- harder to communicate/coordinate with teams who own other micros-services

- requires more experienced than average developers to be effective

---

## Final Answer ?

# Monolith

---

## Why ?

Due to the most probable size and make-up of the teams that will work on node projects.

It’s wide use in the community will make consumption of already existing solutions easier.

Easier to communicate, learn and develop good lessons from the first projects.

Monolith vs Micro-Services is a range, not a binary choice.

---

## Communication

There a few well developed architecture patterns which can be used to describe how our modules will communicate within the project:

- pipes and filters

- event driven

- pub/sub

--- 

## Pipes and Filters

An architectural style in which modules where the output of an module is piped into another module as it’s input and that module’s output is piped into another etc.

Modules thus make up flows of data from one end of the application to the other with each module having one well defined function and well defined inputs and outputs.

Advantages: less overhead, explicit flows, linear debugging

Disadvantages: higher coupling, more setup


