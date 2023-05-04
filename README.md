# CX-Infinity

CX Infinity
https://cxi.novelvox.net/
Agent App Flow:
1. Load the URL https://cxi.novelvox.net/cxinfinity and login with credentials provided
2. Make Agent Ready (Top Right - Click on Message Icon and select Ready)
Client App Flow:
1. Load the URL https://cxi.novelvox.net/customers/sample_webrtc/index.html
2. Websocket establish the connection with server (Can be seen in Network/WS - Signalling)
3. User clicks on Start Chat
4. client sents registration request to server (messageType: "REGISTER_TO_BROKER")
5. server responds with registration successfull/failed (messageType: "REGISTERATION_DONE")
6. Agent will be assigned to that request on the server and a Popup with Accept/Reject will show on Agent Side
7. Click on Accept on Agent Side
8. Event will be received on client side - (messageType: "OFFER_RECEIVED"))
9. Now chat is connected. You can exchange messages between agent and customer using the text box provided on both sides. (messageType: "MESSAGE_SEND" and messageType: "MESSAGE_RECEIVED")
10. You can disconnect the chat using the End Chat button on client side or End Chat button on the agent side.
here is the workflow
I have mentioned some of the events only.. but there are other events as well which are used for features like Read Receipts/Sneak Peak etc
all events are there in SDK.. on production you would need to implement all the methods/features/events

Android version has already been finished wonderfully, you have to convert it to iOS SDK.
