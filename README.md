# Java EE7: WebSockets

Java EE7 added support for WebSockets.

The [WebSockets standard](#more-on-websockets) defines a full-duplex communication protocol to simplify and streamline long-running communications between a client and a server. The protocol has a well-defined wire format that allows for text or binary messages to be interleaved at will: either side of the connection can send messages at any time, in any order (which is a significant difference from the requirements of Comet or other long-polling mechanisms which require management of several connections to emulate bidirectional communication). The wire format is compact and efficient, making it ideal for small messages.

A WebSocket is established by upgrading an existing HTTP connection via an Upgrade handshake. The connection continues to use the original HTTP connection after upgrade, which allows it to work with firewalls and other infrastructure optimized for HTTP traffic; however, HTTP [proxy servers may need to be upgraded to understand the WebSocket protocol][WebSockets: Proxy Traversal], especially those that do SSL termination.

This sample contains a few variations to illustrate how to use WebSockets in EE7 applications. Once the server has been started, go to [http://localhost:9082/websocket/](http://localhost:9082/websocket/) to interact with the sample. Cross-reference the source to understand what the client side (Java or JavaScript) and server side (Java) are doing.

* [Building with Gradle](/docs/Building-the-sample.md#building-with-gradle)
* [Building with maven](/docs/Building-the-sample.md#building-with-maven)
* [Downloading WAS Liberty](/docs/Downloading-WAS-Liberty.md)
* [Start the server using the command line, or maven/gradle plugins](/docs/Starting-the-server.md)
* [Using Eclipse and WebSphere Development Tools (WDT)](/docs/Using-WDT.md)

## More on WebSockets
* [Wikipedia summary](https://en.wikipedia.org/wiki/WebSocket)
* [WebSockets: Proxy Traversal](https://en.wikipedia.org/wiki/WebSocket#Proxy_traversal)
* [w3 JavaScript WebSockets API](http://www.w3.org/TR/websockets/)
* [WebSocket protocol: RFC 6455](http://tools.ietf.org/html/rfc6455)

## Notice

© Copyright IBM Corporation 2015.

## License

```text
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
````
