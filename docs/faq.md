---
title: "Frequently asked questions"
date: 2021-08-03T20:30:00+02:00
---

# FAQ

This is a collection of frequently asked questions and their answers. Some of the answers are not yet written. In these cases please ask in the matrix room `#envs:envs.net`.

## I'm confused about Matrix terminology

It's a complex beast. Here is a short list of what is what:

  * **Matrix** - Protocol and ecosystem around it. You cannot "run Matrix" or have an "account on Matrix". Often mixed with matrix.org.
  * **Homeserver** - A Matrix server. There are lot of public ones or you can set up your own. You create user account on a homeserver you choose.
  * **matrix.org** - One of many public Matrix homeservers where you can make an account. Often mixed with Matrix.
  * **Element** - One of many Matrix client applications. Has different Web/Desktop/Android/iOS versions, so always specify which you use when asking for help.
  * **Synapse** - One of many Matrix server implementations. You can run Synapse on your server if you want your own Matrix homeserver.
  * **Space** - Group of rooms and other spaces. Can be used to organize rooms. A bit like Discord guilds or Slack workspaces, but more flexible.
  * **Community** - old way of grouping rooms that was never fully implemented. Replaced by spaces.

***

## I'm running Element Android but notifications are unreliable. I installed it from F-Droid.

Unfortunatly F-Droid version doesn't have the google push notification support and there is no open alternative. Better install from Google Play until a solution is found.

***

## I'm running Element Android and a message is stuck in the bottom of the screen. I can't get rid of it.

Open Element `Settings` / `General` and press `Clear Cache`. This is a long standing bug, I hope it gets fixed one day.

***

## Matrix is slow or not working properly. I'm on matrix.org homeserver

Matrix.org is used as default server in many clients. It is known to be slow occasionally. You should pick a server you like from [joinmatrix.org](https://joinmatrix.org/servers/) or the asra.gr list of [public servers](https://wiki.asra.gr/en:public_servers) and register there. If you already have joined many rooms, you can use [migration tool](https://ems.element.io/tools/account-migration) to "copy" your old account to the new account.
 
After finished, remember to leave all rooms with your matrix.org account so it won't use any resources on the already overloaded server. You can login to both accounts simultaneously with private browser windows.

This also helps decentralize Matrix which is important for the whole ecosystem. 

***

## Messages not readable
  * At least one verified session must be open at all times, the easiest way to do this is to set up the Desktop Client or Element on a smartphone. These programs can be closed and restarted without having to log in again. Otherwise, a verified Matrix session can be created in a private web browser window by logging into Matrix there and verifying this session from an existing one. This window can be closed after about five minutes. The keys are transferred to the other Matrix clients by the verification process. This creates a ghost session which is then always open. Then all other clients can be logged out. Otherwise messages which are received in the period without open matrix session cannot be read later. This is to be solved in the future by means of the function dehydrated devices.
  * Has the [Secure Backup](/settings/#secure_backup) been set up properly?
  * Messages remain unreadable when matrix sessions are created and then the web browser window is simply closed without logging out. Solution: only possible for new messages: read this documentation.

***

## What is the difference between passphrase and recovery key?
The password that can access the key backup is called the recovery key and is very long, starts with a capital E and should be saved or printed after setup. Since this password is hard to remember in everyday life (e.g. when you are on the road, want to have a look at Matrix, but only have access to other computers) you can think of a (easy to remember) passphrase from which the recovery key can be calculated (in the browser/client) before trying to "open" the key backup.

***

## Why is there no status bar at the bottom of the screen when hovering over hyperlinks in the Desktop-Client element? How can you trust them then?
In fact, the status bar is a popular test of the seriousness of hyperlinks you are trying to click on. In the Desktop Client element this is not possible, similar to the mobile clients. Here you can only right-click on the link and check the presented target page for seriousness.

***

## How to tell people a room address with Element Desktop Client?
With the matrix.to link, which you can see under the i for the room properties and another click on "Share room".

***

## How do you tell people a room address with Element Web-Client?
With the matrix.to link, which you can see under the i for the room properties and a further click on "Part room" and an exchange of the front matrix.to with matrix.envs.net

***

## Can I write LaTeX?
Yes, but it is an experimental feature right now. It will be available for everybody in a few weeks: [https://github.com/vector-im/element-web/issues/1945](https://github.com/vector-im/element-web/issues/1945)

***

## Are there something like Threads (like in Mattermost/Slack) in Matrix?
Threads like in Mattermost or Slack are currently available as lab feature in Matrix and will be stable within the next weeks. To get more information, follow their roadmap: [https://github.com/vector-im/roadmap/projects/1](https://github.com/vector-im/roadmap/projects/1)

***

## I do not have a security key (recovery key)
To do this, please check whether this has been set up at all. See [Secure backup](/settings/#secure_backup)

***

## How do I change the passphrase for my key backup?
  * export the room keys for all matrix sessions except for one, which is still accessible, `Settings` -> `Security & Privacy` -> `Encryption`/`Cryptography`, here it is best to provide the matrix login password. Finally, log out by clicking on the user name in the upper left corner and log out. If you are asked whether you want the encrypted messages, click on 'I don't want my encrypted messages', because these keys have already been exported.
  * Under `Settings`-> `Security & Privacy` -> `Secure Backup` press first `Delete Backup`, afterwards the button `Reset` and may a clearing of the cache under `Settings`-> `Help & About` is necessary, as well a logging off and logging on again. If all this does not work, continue in the next point. The action was successful, if only the green 'Setup' button is displayed.
  * For all previously exported key backups, perform the manual import path
  * Set up a new security backup. See [Secure backup](/settings/#secure_backup)

***

## How do I reset the secure backup if I have lost my security phrase AND my (saved and printed) security key?
Please execute the following:

  * export the room keys for all matrix sessions except for one, which is still accessible, `Settings` -> `Security & Privacy` -> `Encryption`/`Cryptography`, here it is best to provide the matrix login password. Finally, log out by clicking on the user name in the upper left corner and log out. If you are asked whether you want the encrypted messages, click on 'I don't want my encrypted messages', because these keys have already been exported.
  * [Delete](/settings/#security_privacy) all sessions that are no longer accessible. the top one in bold is the current session, do not tick this one
  * Log off the last session
  * Write a message to the ServiceDesk with a request to delete the security keys from the database.
  * Wait for the answer
  * Log in again at Matrix and skip verification at windows and messages
  * Log out from Matrix
  * Log in again at Matrix and skip verification at windows and messages again
  * Under `Settings`-> `Security & Privacy` -> `Secure Backup` look if there is a green button `Setup` and no red buttons. If there are still red buttons, press first `Delete Backup`, afterwards the button `Reset` and may a clearing of the cache under `Settings`-> `Help & About` is necessary, as well a logging off and logging on again. Also it may be necessary to press the red button `Reset` under `Settings`-> `Security & Privacy` -> `Cross-Signing`. The action was successful, if for 'Secure Backup' and 'Cross-Signing' only the green 'Setup' button is displayed.
  * If all this does not work reply to the ticket with a request for a jitsi meeting
  * For all previously exported key backups, perform the manual import path
  * Set up a new security backup. See [Secure backup](/settings/#secure_backup)

***

## Sometimes I see a room marked in bold and click on it, but I don't have the time to edit the content and any consequences for me immediately. How can I mark the room as "unread" again?
Unfortunately this is not possible in Element. As a workaround, you can mark the room as a favorite and notice yourself that your own favorites should be looked at again.

***

## What should I do if video or audio in a video conference does not work on a MacOS?
Often Element does not have the rights to access the webcam and microphone. These can be assigned in the system settings under Security and Privacy.

***

## How many people can be invited at ones into a room? Can I invite people by their E-Mail address?
Mass invite by E-Mail is currently not supported in Element.

***

## Can I modify access permissions for all rooms in my community, that only members of the community can enter?
No, this is not possible. Rooms can be part of multiple communities. Therefore the access permission will be set on room based level.

***

## I do not see any message of a specific person in a room
A common reason for this is that you blocked that person by accident. You do not see any message of the person even if you hear that this person posted them. Open your Security settings in Element and scroll down. Please check in the category "Blocked user" if you find the person that does not belong there… Remove it!

***

## Can I manage multiple Matrix-Account on my Element Desktop Client?
With the Element Desktop client, you can only manage one Matrix-Account right now. But it is possible to start several Element-windows with different Matrix-Accounts, also within your Autostart-settings of your computer. Therefore, you need to change (or create additional) execution commands to open a specific profile:

```
element-desktop --profile PROFILE_NAME
```
So you can place several Element-Starters in your Autorstart, with different profile names, e.g. `--profile work` or `--profile private`. Unfortunately, both opened windows will appear with the same Icon in the Indicator-Applet. But therefore, a solution will upcome soon, for sure...

Furthermore, there are other Matrix-Clients, that can handle more Matrix-Accounts per se, e.g. [weechat](https://matrix.org/docs/projects/client/weechat-matrix), [Spectral](https://matrix.org/docs/projects/client/spectral), [Quaternion](https://matrix.org/docs/projects/client/quaternion), or [Mirage](https://matrix.org/docs/projects/client/mirage).

***

## User-specified Element Desktop config.json

You can configure the app in `config.json` and customising it. All config options with description can you find in the [element docs](https://github.com/vector-im/element-web/blob/develop/docs/config.md).

For a good example, see [https://develop.element.io/config.json](https://develop.element.io/config.json).

- `%APPDATA%\$NAME\config.json` on Windows
- `$XDG_CONFIG_HOME\$NAME\config.json` or `~/.config/$NAME/config.json` on Linux
- `~/Library/Application Support/$NAME/config.json` on macOS

In the paths above, `$NAME` is typically `Element`, unless you use `--profile
$PROFILE` in which case it becomes `Element-$PROFILE`, or it is using one of
the above created by a pre-1.7 install, in which case it will be `Riot` or
`Riot-$PROFILE`.

***

## Create a tombstone event

This will move all Matrix users in the old room to the new room.

!!! note
    Do NOT use `/upgraderoom` instead, as IRC bridge will follow it and FOOBAR the new room.

1) Create an new Room an copy the room_ID.
 
2) Go back to the old room.

* Type `/devtools`.
* Select "Explore room state" -> "Send custom timeline event"
* Set "event type" to `m.room.tombstone` ("state key" can remain empty)
* In event content enter (you'll need the target room_ID now):

```json
{
    "body": "This room has been replaced by new one",
    "replacement_room": "!target_room_id:server.tld"
}
``` 

Press `Send`

Hooray! Users in the old room should now come to the new room. Your new room is also the latest version. If the IRC bridge automatically follows, you can kick it. Give admins and  mods to people you trust when they join.

***

!!! info "Annotations"
    * Losing the room keys will result in the loss of your messages, as they can only be read by you and your communication participants. No admin can help with that.
    * Because of the new session, a red warning sign is subsequently displayed for all your previous messages. This is not an error, but just a little too dramatic information setting (further information can be found here: [https://github.com/vector-im/element-web/issues/13701](https://github.com/vector-im/element-web/issues/13701))
    * If you only use Matrix on one device and you do not have access to your security phrase or security key you have to follow route c) to not loose your encrypted messages.
