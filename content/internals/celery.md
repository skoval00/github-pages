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

#### on_configure()
Hook on configuration, i.e. on access to app.conf.


## Celery app configuration

### Defaults
Search for default configuration values in celery.app.defaults module.


## Celery commands

### Parsing options

*celery.bin.base.Command.setup_app_from_commandline*

Celery parses options with the help of optparse. But manages actual parsing of sys.argv by itself. 

Command base class has preload_options attribute. It is populated in Command.prepare_options. These options are used in Command.setup_app_from_commandline. Values from environment variables may also affect app configuration:
- CELERY_APP
- CELERY_LOADER
- CELERY_BROKER_URL
- CELERY_CONFIG_MODULE

If user configures additional preload options in they are configured here also.

Finally Celery application is configured and stored in command object app attribute.

### celery.bin.celery.CeleryCommand

Remaining command line options are handled in CeleryCommand.handle_argv.

This method calls CeleryCommand.execute which dispatches command to the concrete command class and calls its run_from_argv and handle_argv methods and finally command object __call__method.

### celery.bin.celery._RemoteControl

### celery.bin.celery.inspect


