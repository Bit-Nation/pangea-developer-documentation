The VM provides some utilities needed for DApp development.

## ethereumAddress
This is a constant representing the ethereum address of the user

## renderModal
`renderModal(uiID <string>, layout <string>, callback <string>)` the uiID must be created with the `newModalUIID` method.
The callback will be called once the modal got rendered.

## sendETHTransaction
`sendETHTransaction(transactionParams <object>, callback <function>)` will send an ethereum transaction.
The transaction params should look like this:

- `value` the value in wei
- `to` should be an address
- `data` can be the data to execute

The callback will be called with an transaction object.

## sendMessage
`sendMessage(chat <string>, payload <object>, callback <function>)` will send a message with the given parameters.
The message payload must have the following properties:
- `shouldSend <bool>` a message can be send or not. If you don't send it it will only be persisted and displayed for you.
- `params <object>` a set of parameters.
- `type <string>` a type of the message e.g. `SEND_MONEY` can be used for filtering later.

## setOpenHandler
`setOpenHandler(handler <function>)` will set a handler that is called when the user open the DApp.

## setMessageRenderer
`setMessageRenderer(renderer <function>)` will set a handler for rendering messages. The handler will be called with object (payload) and a callback.
The callback must be called with an error AND the JSX.

## newModalUIID
`newModalUIID(closer <function>, callback <function>)` will create a new modal id which you can use to render a modal.
The closer will be called once the modal get closed. The callback will be called with an error and the modal ID.
The modal ID can then be used to display a modal.

## db
The database provides four methods:

- `put(key <string>, value <string>, callback <function>)`
- `get(key <string>, callback <function>)`
- `has(key <string>, callback <function>)`
- `delete(key <string>, callback <function>)`
