Title: Celery Internals
Date: 2016-11-10 15:34
Status: draft

## Background
I have a few projects which use Celery a distributed task queue. Once in a while celery workers stopped executing tasks submitted to them. I witnessed such behaviour with Redis and MongoDB backends. When it started to annoy me I decided to learn how Celery communicates with its backends.

## Celery app components

### Attributes
* `configured`
* `finalized`
* `_tasks` TaskRegistry

### Classes
* celery.app.amqp:AMQP
* celery.events:Events
* celery.loaders.app:AppLoader
* celery.app.log:Logging
* celery.app.control:Control
* celery.app.task:Task
* celery.app.registry:TaskRegistry

### Hooks
#### on_init()
Allows to insert hook in Celery subclass which is executed at instantiation.


## Celery app configuration

### Defaults
Search for default configuration values in celery.app.defaults module.
