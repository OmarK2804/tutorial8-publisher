a. How many data your publlsher program will send to the message broker in one run?

My publisher program will send five data messages (five events of type `UserCreatedEventMessage`) to the message broker in one run using the `CrosstownBus` publisher, each representing the creation of a user with a unique user ID and user name.

b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

It means they are both connecting to the same AMQP message broker running on the local machine (localhost) on the default port 5672.

- Running RabbitMQ
![](static/Screenshot%202024-04-24%20130838.png)