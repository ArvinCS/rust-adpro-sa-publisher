## Reflection

> How many data your publlsher program will send to the message broker in one run?

The publisher program sends five messages to the message broker in one run. Each call to publish_event sends one UserCreatedEventMessage to the "user_created" queue on the message broker. Therefore, a total of five messages will be sent to the broker during the execution of the program.

> The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

The string in both the publisher and subscriber programs indicates that they are connecting to the same instance of the AMQP broker. It means they are communicating with the same broker instance. This ensures that messages published by the publisher are sent to the same broker where the subscriber is listening, enabling communication between the two programs.

## Sending and processing event

![Home](assets/home.png)

![Connection](assets/connection.png)

![Sent and received event](assets/console.png)

What happened is that our publisher sent five events into the broker. When our subscriber subscribe to the broker, we also received the 5 events.

