## Networking Prototype
2018 Unity Networking Stack

## Contributing
Take a look at the [current issues](https://github.com/valkyrienyanko/Networking-Unity-Prototype/issues).

## Building the Server
#### Terminal
If you prefer to use the terminal for the server build, make sure when building the server inside Unity to check off "Server Build" to get descriptive output and allow input such as Ctrl + C to stop the server.
```batch
"Server.exe" -batchmode -nographics
```

#### Standalone
Commands
`exit` `stop` `start` `restart` `say` `kick`

## Building the Client
Nothing much to say about this right now.

## Warnings
#### Client
Note that the connectionId is NOT from the receiving client but instead from the current client.
```cs
NetworkEventType type = NetworkTransport.Receive(out int recHostId, out int connectionId, out int channelId, recBuffer, recBuffer.Length, out int dataSize, out error);
```
