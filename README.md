a. How many data your publlsher program will send to the message broker in one run?

My publisher program will send five data messages (five events of type `UserCreatedEventMessage`) to the message broker in one run using the `CrosstownBus` publisher, each representing the creation of a user with a unique user ID and user name.

b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

It means they are both connecting to the same AMQP message broker running on the local machine (localhost) on the default port 5672.

- Running RabbitMQ
![](static/Screenshot%202024-04-24%20130838.png)

- Sending and processing event
![](static/Screenshot%202024-04-24%20132205.png)
![](static/Screenshot%202024-04-24%20132644.png)
The subscriber received all five messages published by the publisher. Each message contains a user ID and a user name, and the subscriber program prints out each message it receives.

- Monitoring chart
![](static/Screenshot%202024-04-24%20134322.png)
The spikes show the message rates when each event batch (in this case 5 events simultaneously) is published.