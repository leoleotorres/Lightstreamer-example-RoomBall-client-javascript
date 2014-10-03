# Lightstreamer Room-Ball Demo for JavaScript Client #

This project includes a web client front-end example for the [Lightstreamer Room-Ball Demo Adapter]().

## Room-Ball Demo ##

<table>
  <tr>
    <td style="text-align: left">
      &nbsp;<a href="http://demos.lightstreamer.com/RoomBallDemo" target="_blank"><img src="screen.png"></a>&nbsp;
      
    </td>
    <td>
      &nbsp;An online demonstration is hosted on our servers at:<br>
      &nbsp;<a href="http://demos.lightstreamer.com/RoomBallDemo" target="_blank">http://demos.lightstreamer.com/RoomBallDemo</a>
    </td>
  </tr>
</table>

This <b>Room-Ball Demo</b> implements a simple gaming/collaborative application fed in real-time via a Lightstreamer server.<br>
Once logged in, the user can start moving his or her avatar in the room and exchange messages with every other users present in the demo. For each user, an avatar of a specific background color is created, on top of which the nickname chosen by the user is displayed and the balloon with the last typed message appears to the right.<br>
User messages are broadcasted as you type, character by character, to all other users.<br>
The red ball is a passive object that you can push in different directions with your avatar.<br>

The demo includes the following client-side technologies:
* A [Subscription](http://www.lightstreamer.com/docs/client_javascript_uni_api/Subscription.html) containing 1 item, subscribed to in <b>COMMAND</b> mode.
* The user messages are sent to the Lightstreamer Server using the [LightstreamerClient.sendMessage](http://www.lightstreamer.com/docs/client_javascript_uni_api/LightstreamerClient.html#sendMessage) utility.

# Deploy #

Before you can run the demo, some dependencies need to be solved:

-  Get the lightstreamer.js file from the [latest Lightstreamer distribution](http://www.lightstreamer.com/download) 
   and put it in the src/js folder of the demo. Alternatively, you can build a lightstreamer.js file from the 
   [online generator](http://www.lightstreamer.com/distros/Lightstreamer_Allegro-Presto-Vivace_5_1_1_Colosseo_20130305/Lightstreamer/DOCS-SDKs/sdk_client_javascript/tools/generator.html).
   In that case, be sure to include the LightstreamerClient, Subscription, DynaGrid, and StatusWidget modules and to use the "Use AMD" version.
-  Get the require.js file form [requirejs.org](http://requirejs.org/docs/download.html) and put it in the src/[demo_name]/js folder of the demo.
-  Please note that the demo uses a jQuery customized theme, included in this project.

You can deploy this demo to use the Lightstreamer server as Web server or in any external Web Server you are running. 
If you choose the former case, please note that, in the <LS_HOME>/pages/demos/ folder, there is a copy of the /src directory of this project, if this is not your case, please create the folders <LS_HOME>/pages/demos/ChatTileDemo then copy here the contents of the /src folder of this project.<br>
The client demo configuration assumes that Lightstreamer Server, Lightstreamer Adapters, and this client are launched on the same machine. If you need to target a different Lightstreamer server, please search this line:
```js
var lsClient = new LightstreamerClient(null,"DEMO");
```
in js/lsClient.js file and change it accordingly (replace null with your server URI).<br>
Anyway the [ROOM]() Adapters have to be deployed in your local Lightstreamer server instance.
The demo is now ready to be launched.

# See Also #

## Lightstreamer Adapters Needed by This Demo Client ##

* [Lightstreamer Room-Ball Demo Adapter]()
* [Lightstreamer Reusable Metadata Adapter in Java](https://github.com/Weswit/Lightstreamer-example-ReusableMetadata-adapter-java)

## Similar demo clients that may interest you ##

* [Lightstreamer Chat-Tile Demo for JavaScript Client](https://github.com/Weswit/Lightstreamer-example-ChatTile-client-javascript)
* [Lightstreamer Chat Demo for JavaScript Client](https://github.com/Weswit/Lightstreamer-example-Chat-client-javascript)
* [Lightstreamer Round-Trip Demo for JavaScript Client](https://github.com/Weswit/Lightstreamer-example-RoundTrip-client-javascript)
* [Lightstreamer Messenger Demo for JavaScript Client](https://github.com/Weswit/Lightstreamer-example-Messenger-client-javascript)
* [Lightstreamer 3D World Demo Client for JavaScript](https://github.com/Weswit/Lightstreamer-example-3DWorld-client-javascript)

# Lightstreamer Compatibility Notes #

- Compatible with Lightstreamer JavaScript Client library version 6.0 or newer.# Lightstreamer - Basic Chat Demo - Java Adapter 
