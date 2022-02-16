# rabbitMQ
Hello world , Work queues, Publish/Subscribe

[rabbitMq.sh](https://github.com/deesirouss/rabbitMQ/blob/main/rabbitmq.sh)
is script to install rabbitMq-server in ubuntu bionic(18)

## [Hello World](https://github.com/deesirouss/rabbitMQ/tree/main/first-hello-world)
consist two small programs in Python;
- a producer (sender) that sends a single message
- and a consumer (receiver) that receives messages and prints them out. It's a "Hello World" of messaging

## [Work Queue](https://github.com/deesirouss/rabbitMQ/tree/main/second-Work-Queues)
used to distribute time-consuming tasks among multiple workers

## [Publisher/Subscribe](https://github.com/deesirouss/rabbitMQ/tree/main/third-publish-or-subscribe)
build a simple logging system.
It will consist of two programs
- the first will emit log messages
- and the second will receive and print them.

### Some Useful commands
#### Start rabbitmq-server
-> sudo service rabbitmq-server start
-> sudo service rabbitmq-server on

#### Status  of rabbitmq-server
-> sudo rabbitmqctl status

#### Installing pika
-> python3 -m pip install pika --upgrade

#### After sending messege, list queues
-> sudo rabbitmqctl list_queues
-> sudo rabbitmqctl list_queues name messages_ready messages_unacknowledged

#### To list the exchanges on the server you can run the ever useful rabbitmqctl:
-> sudo rabbitmqctl list_exchanges

#### You can list existing bindings using, you guessed it,
-> sudo rabbitmqctl list_bindings

#### If you want to save logs to a file, just open a console and type:
-> python receive_logs.py > logs_from_rabbit.log
