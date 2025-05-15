# Tutorial Pemrograman Lanjut
## Nayla Farah Nida - 2306213426

### Module 9

**Understanding publisher and message broker**

a. How much data your publisher program will send to the message broker in one run?  

The publisher send 5 messages to the message broker in one run.

b. The url of: ```amqp://guest:guest@localhost:5672``` is the same as in the subscriber program, what does it mean? 

it means both are connecting to the same server, which is expected and necessary for the publisher and subscriber to communicate.

**Running RabbitMQ as message broker**

![Running RabbitMQ](image_1.png)

**Sending and processing event**

Publisher successfully sent 5 messages to the RabbitMQ broker at ```amqp://guest:guest@localhost:5672```. The subscriber, already connected to the same broker and listening for ```user_created``` events, received those messages. Each ```UserCreatedEventMessage``` was deserialized and handled by the ```UserCreatedHandler```, which printed then printed on the console.

![Sending event](image_2.png)

**Monitoring chart based on publisher**

The spike represents a sudden increase in the rate of messages being published to the broker (by the publisher) and delivered to subscribers.

![Monitoring chart](image_3.png)
