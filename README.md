`amqp-read` is a cli tool for reading from AMQP/RabbitMQ broker queue into a file.

## Installation

    $ npm install amqp-read -g

## Usage overview

```
Usage: node ./bin/amqp-read [options]

Options:
  --uri           uri                                                                          [required]
  --queue, -q     queue's name to work with                                                    [required]
  --export, -e    the file to output messages to                                               [required]
  --count, -c     limit the number of message to read
```

### Read the first 5000 messages of a queue
into a file
```
  amqp-read --host amqp://guest:guest@localhost/test -q queuetest --count 5000 --export dump.json
```