# How many data your publlsher program will send to the message broker in one run?

The publisher program will send 5 messages to the message broker in one run. Each call to p.publish_event sends one message, and there are 5 such calls in our `main.rs`.

# The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

It means that both programs are connecting to the same RabbitMQ server instance. This allows the publisher to send messages to the same exchange and queue that the subscriber is listening to, enabling communication between the two programs.

![alt text](image.png)