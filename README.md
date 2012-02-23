Netosphere: An Atmosphere Framework WebSocket and Comet Server build on top of Netty!


Meteor, AtmosphereHandler, WebSocketProtocol and Jersey resource are supported.

The Server can be started using java

    java -cp atmosphere-netty.jar:atmosphere-runtime.jar
          org.atmosphere.plugin.netty.NettyAtmosphereServer
                [/path/to/an/exploded/war/file] [host] [port]

or embedded using

    NettyAtmosphereServer server = new NettyAtmosphereServer.Builder().config(
                 new Config.Builder()
                    .path("/apps")
                    .host("127.0.0.1")
                    .port(8080).build())
                    .build();
    server.start();

or

    NettyAtmosphereServer server = new NettyAtmosphereServer.Builder().config(
                 new Config.Builder()
                    .host("127.0.0.1")
                    .port(8080).build())
                    .broadcaster(DefaultBroadcaster.class)
                    .handler("/*", MyAtmosphereHandler.class)
                    .build();
    server.start();

If you are interested, subscribe to our mailing list (http://groups.google.com/group/atmosphere-framework) for more info!  We are on irc.freenode.net under #atmosphere-comet
