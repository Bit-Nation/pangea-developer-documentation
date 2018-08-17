The VM provides some utilits needed for DApp development.

## ethereumAddress
This is a constant representing the ethereum address of the user

## renderMessage

## renderModal

## sendETHTransaction

## sendMessage
`sendMessage(chat <string>, payload <object>, callback <function>)` will send a message with the given parameters.
The message payload must have the following properties:
- `shouldSend <bool>` a message can be send or not. If you don't send it it will only be persisted and displayed for you.
- `params <object>` a set of parameters.
- `type <string>` a type of the message e.g. `SEND_MONEY` can be used for filtering later.

## setOpenHandler
`setOpenHandler(handler <function>)` will set a handler that is called when the user opens the DApp.

## setMessageRenderer
`setMessageRenderer(renderer <function>)` will set a handler for rendering messages. The handler will be called with object (payload) and a callback.
The callback must be called with an error AND the JSX.

## newModalUIID
`newModalUIID(closer <function>, callback <function>)` will create a new modal id which you can use to render a modal.
The closer will be called once the modal get closed. The callback will be called with an error and the modal id.
The modal ID can then be used to display a modal.

## db
The database provides four methods:
- `put(key <string>, value <string>, callback <function>)`
- `get(key <string>, callback <function>)`
- `has(key <string>, callback <function>)`
- `delete(key <string>, callback <function>)`