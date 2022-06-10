# Stock Market App Architecture Proposal

This is a Systems Design solution for a Chat app. We present a High Level and Low Level overview and discuss some of the main critical parts of a chat application.

- [Systems Design - High Level](#systems-design---high-level)
  - [Gathering System Requirements](#gathering-system-requirements)
  - [Coming Up With A Plan](#coming-up-with-a-plan)
  - [Persistent Storage Solution and App Load](#persistent-storage-solution-and-app-load)
  - [Load Balancing](#load-balancing)
  - [Sharding](#sharding)
  - [Pub-Sub System for Real-Time Behavior](#pub-sub-system-for-real-time-behavior)

The Low Level section contains various parts of the systems and we do a quick deep dive inside the internal components.

- [Systems Design - Low Level](#systems-design---low-level)
  - [Gathering System Requirements](#gathering-system-requirements)
  - [Actions](#actions)
  - [Coming Up With A Plan](#coming-up-with-a-plan)
  - [C4](#c4)
    - [System Context](#system-context)
    - [Container Diagram](#container-diagram)
    - [Component Diagram](#component-diagram)
    - [Code](#code)
  - [Elixir APIs](#elixir-apis)
    - [Project Structure](#project-structure)
      - [Databases](#databases)
      - [Asynchronous jobs](#asynchronous-jobs)
      - [Error Handling](#error-handling)
      - [Documentation of API](#documentation-of-api)
      - [Rollbar](#rollbar)
      - [Circle CI](#circle-ci)
      - [Elixir Scanners](#elixir-scanners)
    - [Tests and Delivery Automation](#tests-and-delivery-automation)
    - [Docker](#docker)

# Systems Design - High Level

## Gathering System Requirements

## Coming Up With A Plan

## Persistent Storage Solution and App Load

## Load Balancing

## Sharding

## Pub-Sub System for Real-Time Behavior

# Systems Design - Low Level

## Gathering System Requirements

### Actions

## Coming Up With A Plan

## C4

### System Context

### Container Diagram

### Component Diagram

### Code

## Elixir APIs

### Project Structure

#### Databases

#### Asynchronous jobs

#### Error Handling

#### Documentation of API

#### Rollbar

Rollbar is the option regarding error tracking and monitoring. It offers a good query search & filter tool and lots of useful information on error debugging and replay.

#### Circle CI

Automated testing and deployment will run with the help of Circle CI.

#### Elixir Scanners

### Tests and Delivery Automation

### Docker

Docker should be our default tool in any project that we build. `Dockerfile`, `docker-compose.yml` and a `Makefile` are required to work with containers locally and be able to deploy applications via Docker. Some suggestion for the projects’ Makefile:

| Command                   | Description                            |
|---------------------------|----------------------------------------|
| make start                | Start the application                  |
| make specs                | Run all the specs                      |
| make bash                 | access the bash inside the container   |
| make console              | access console                         |
| make routes               | display routes                         |
