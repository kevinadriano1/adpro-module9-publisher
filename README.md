## How much data your publisher program will send to the message broker in one run?
The publisher program sends 5 messages to the message broker in one run. Each message contains a user_id and a user_name, both as strings. The user_id is a short string like "1" or "5", and the user_name is around 20 characters long. Using Borsh serialization, each message will be about 30–40 bytes. So the total data sent is around 150–200 bytes for all 5 messages combined. This is a small amount of data and is sent quickly to the message broker.

## The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
The URL amqp://guest:guest@localhost:5672 is used to connect to the RabbitMQ server. Both the publisher and subscriber use this same URL. This means they are connecting to the same message broker. The first guest is the username, and the second guest is the password. localhost means the broker is running on your own computer, and 5672 is the default port for AMQP. Because they use the same URL, the messages sent by the publisher can be received by the subscriber.

## Running RabbitMQ as message broker.
<img src="img/ss1.png">