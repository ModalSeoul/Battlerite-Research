# Battlerite reverse engineering progress
Battlerite's a MOBA-style game. Not in the traditional sense, though. While it is massively online, and also has a battle arena, it lacks things that other MOBA games have in spades. For instance, Battlerite has no concept of minions or lanes. The only goal is to skull-fuck your opponents.


Battlerite is written in C# using the Unity engine. The PlayerRefs they store are located in

`HKEY_CURRENT_USER\SOFTWARE\StunlockStudios\Battlerite`

The data you'll find in that path will look something like this (so long as you've ran the game)

![](http://i.imgur.com/apocxh0.png)

Nothing special.

Taking a peak inside the game's directory shows they use the following libs

* [Protobuf.NET](https://code.google.com/archive/p/protobuf-net/)
* [Json.NET](http://www.newtonsoft.com/json)
* [CaronteFX](https://www.nextlimit.com/products/name/carontefx/)
* [StunLock.TestUnity](http://i.imgur.com/1mFx0zs.png)
* [AG-Software Matrix XMPP SDK](http://www.ag-software.net/matrix-xmpp-sdk/)

They also use the following standard Mono libs<br>
* Mono.Data.Sqlite
* Mono.Data.Tds
* Mono.Messaging
* Mono.Posix
* Mono.Security
* Mono.Web
* Mono.WebBrowser (?)

They track metadata with something called "AssetMetadataProto".
Pushing
