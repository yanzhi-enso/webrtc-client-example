# WebRTC means Web Real Time Communication. Free WebRTC Demos and Examples.
From Jimmy: use the react-native one

Setups:
Server (singling server):
```
cd react-native-webrtc-app/server
npm install
npm run start
```

Client:
1. Install js dependencies
```
npm install
```
2. Install ios native dependencies
```
cd ios
pod install
```
Note, don't use react native terminal to start the ios app. It might stuck without any error.
3. Compile the client app
```
open WebRTCExample.xcworkspace
```
select the signauture, then install the app
4. Start metro
in `client`, do `npx react-native start` and the app should be setup


Note, 
- make sure the client is running while the server is running.
- You need to set the signaling server ip `  const socket = SocketIOClient('http://127.0.0.1:3500', {` so that the client can find the node js signaling server. For local testing, just keep it as it is, if it's local network use your laptop's ip address. Both side need to be able to access the server using that ip address.
