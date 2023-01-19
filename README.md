## Usage

### Setup

This repository requires a version of go-libp2p with WebRTC transport.
Clone the go-libp2p repository locally and add a replace directive to the 
go.mod file.

```
replace github.com/libp2p/go-libp2p => <path to go-libp2p>

```

### Listener

Run `./webrtc-test -l <port>` to listen on WebRTC.
For other transports use:
`./webrtc-test -l <port> -t <transport>`
Supported values for transport are:
1. tcp
2. quic
3. websocket
4. webtransport
5. webrtc

This should output a multiaddr which can be used by the client to connect.

### Client

Run `webrtc -d <multiaddr> -c <number of connections> -s <number of streams>`

