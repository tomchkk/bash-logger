Bash Logger
===========

A logger for bash
-----------------

Bash Logger gives you powerful logging for your bash scripts including:

- [x] Log levels
- [x] Logging channels
- [x] Logging context

## Usage

Just `source` the `src/index` file with `max-level`, `channel` and optional `prefix` positional arguments in a suitable place for your project, and then call the relevant log level function with a message and optional context.

```shell
source [path/2/bash-logger/]src/index "INFO" path/2/file.log

log::debug "This is a debug message"
# no output as the log-level 'DEBUG' was not reached

log::info "This is an info message"
# output: [TIMESTAMP] INFO - This is an info message
```

## Arguments

### Max Level

The first argument to bash-logger is a string representing the maximum _level_ that logging should reach. This allows different levels of logging to be set in different environments. Available levels in ascending order are:

 - EMERGENCY
 - ALERT
 - CRITICAL
 - ERROR
 - WARNING
 - NOTICE
 - INFO
 - DEBUG

### Channel

The `channel` can be used to direct logging output, which can be any writeable file or terminal – using, for instance,  `$(tty)`.

### Prefix

A prefix on all log messages can also be set by optionally passing in a string as the third argument to the `source` file call. Setting a prefix can improve readability of log messages.
