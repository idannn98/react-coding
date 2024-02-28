# Gankster coding challenge

Welcome to our coding challenge! Please read this file carefuly, as it contains all of the information you need.

![screenshot-desktop](https://puu.sh/Hp0C2/cb14e843de.png)

Mobile view:

<img alt="screenshot-mobile" width=400 src="https://puu.sh/HoYEw/9b760f91f7.png" />

## Starting conditions

The project starts with an error. Let's fix the error and get things rolling.

![starting error](https://iili.io/JMH2saI.png)

## Todo 📖

- Show the initial Botty message by default (can be found in `common/constants`)
- Submit a message and render it to the list.
- Use **sockets** to:
  - Send the user's message to Botty
  - Show a typing message when Botty is typing
  - Handle incoming Botty messages and display them
- Scroll to the bottom of the messages list when sending/receiving a message

Most of the work needs to be done in the `Messages` components.

### What's Already Been Done 🏁

- Socket setup/configuration with the [Botty server](https://github.com/alexgurr/botty) ([botty.alexgurr.com](https://botty.alexgurr.com))
- All UX and UI, including for messages
- All components, including a message and typing message component
- A context for setting the latest message, which will change the preview in the left user list
- Hooks for playing send/receive sounds

## Reference:

### Botty Socket Events

See the [Botty server](https://github.com/alexgurr/botty) documentation for more information.

- `bot-typing`: Received from Botty when they are typing in response to a user message.
- `bot-message`: Received from Botty with a message payload in response to a user message.
- `user-message`: Emitted by you/the client with a messsage payload

### Message Classes

We've provided `Message` components and classes. Here's some information about the classes.
- `.message--last`: The last message in a group
- `.message--typing`: The message the user sees when the recipient is typing
- `.message--me`: Denotes a user message