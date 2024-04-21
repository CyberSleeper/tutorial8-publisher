# How many data your publlsher program will send to the message broker in one run?

The publisher program will send 5 messages to the message broker in one run. Each call to p.publish_event sends one message, and there are 5 such calls in our `main.rs`.

# The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

It means that both programs are connecting to the same RabbitMQ server instance. This allows the publisher to send messages to the same exchange and queue that the subscriber is listening to, enabling communication between the two programs.

![alt text](image.png)
Initial display of RabbitMQ server


![alt text](image-1.png)
Display of RabbitMQ server after running the Subscriber and publisher programs.
The spike in the graph shows the messages sent by the publisher program to the message broker. The subscriber program is listening to the same queue and receives the messages sent by the publisher program. The subscriber program then prints the messages to the console.