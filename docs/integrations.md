---
title: "Integrations"
date: 2021-08-03T20:30:00+02:00
---

# Use integrations, bridges, bots (e.g. Jitsi)

Integrations/Widgets can be managed via the room information in the upper right corner.

![Add integration button](/images/01_Widgets_en.png "Add integration button")

Here, for example, an etherpad, a jitsi video conference, an RSS bot, etc. can be integrated, i.e. services that are located and run on other servers. Therefore, when using integrations, the JavaScript activity of vector.im (for the integration manager) and other servers (e.g. in the Firefox addon NoScript) must be allowed. Since the widgets are often too small to use the services in their full functionality, widgets can often be opened large in new browser tabs.

## Jitsi Videoconference

A 1:1 phone call or video within Matrix uses the direct WebRTC connection between both parties. From the 3rd person on, [Jitsi](https://de.wikipedia.org/wiki/Jitsi) is used, a free video conferencing tool (Apache license).

If the video conference call is started via the camera icon in the lower right corner. In order for Jitsi to be used for the video conference, at least three people must participate in the conference. If only two people participate in the conference, a direct connection will be established.

Also with Jitsi, opening the widget as a separate tab is useful to use the full functionality (e.g. screen sharing). 

The use of a headset (headphone + microphone) is highly recommended to avoid feedback between sound recording and sound playback. Ideally a headset with a microphone close to the head and not just a headphone and use of the microphone hole on the laptop, which causes noise through it.

The `m` key mutes your microphone - with this setting you should always start a conference. The space bar switches the microphone on when muting is active (push-to-talk). Since the microphone input levels are all set differently, all hearing participants can adjust the volume of all conference participants individually. Furthermore, the individual video quality can be adjusted. 

For sharing the screen contents (or specific program windows), it may be necessary to adjust the security settings of the operating system (e.g. in MacOS under System Preferences > Security > Privacy > Screen Capture).

## Etherpad

The Etherpad widget can be used for collaborative writing or attaching important information to a room.

Etherpads have no user rights management, everyone can write and overwrite other texts (caution!). If user management is needed, better use [Hedgedoc](https://hedgedoc.envs.net/)

## Custom widget

Any Internet pages can be integrated. For example [Hedgedoc](https://hedgedoc.envs.net/) to display LaTeX formulas.
