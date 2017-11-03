# AI-Taylor
A.I. Taylor Intelligent LINE Bot service Document and Issue Tracker

-----
## Document

### Webhook API
Support sending message to your group with API request. To send messages, send followed JSON data to your webhook url using POST request.
The total number of messages that can be sent at one time is 5.

```javascript
Method : POST
Content-Type : application/json

{
    "messages": [
        {
            "type": "text",
            "text": "Hello, World!"
        },
        {
            "type": "text",
            "text": "Unfortunately, The Server #137 is dead."
        }
    ]
}
```

#### Return Codes
```javascript
{
    "message": "SUCCESS"
}
```
#### SUCCESS
Success to process the request.

#### NOT_AUTHORIZED
Your Webhook url is wrong. Just copy the Webhook url in Webhook function page and paste it to your application(Don't modify it). If the same problem persists, Please delete that Webhook and re-issue the Webhook.

#### NO_ARGUMENT_ERROR
Your Webhook url is wrong. Just copy the Webhook url in Webhook function page and paste it to your application(Don't modify it). If the same problem persists, Please delete that Webhook and re-issue the Webhook.

#### BAD_ARGUMENT
Make sure your program has sent all necessary datas to server.

#### TOO_MANY_MESSAGES
Please check that there are more than 5 messages in message object. The total number of messages that can be sent at one time is 5.

#### NO_MESSAGE
Message object is empty or total number of messages is 0.
