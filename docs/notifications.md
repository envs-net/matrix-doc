---
title: "Notifications"
date: 2021-08-03T20:30:00+02:00
---

## Fine-tune notifications

You have to be able to do your work and not be disturbed by Matrix. In times of digital distraction, we all need to learn how notifications should be adapted step by step in a meaningful way. 

### Scenario 1

If you are writing a proposal for a research project and the deadline is approaching, you may want to be notified when your colleagues want to start a discussion with you.  Notifications in this room are intended to draw attention and will be set accordingly...

### Scenario 2

If you are in a room whose main purpose is to inform yourself about new scientific papers and other interesting things from time to time, you may want to turn off the notifications and remind yourself to enter the room from time to time, or you may want to be notified aloud only when your name is mentioned in the discussion.

### Global settings

**Settings > Notifications**

Here experiences must be made if necessary, which help with the estimate, which notifications one really needs promptly and when a back-and-forth-looking is sufficient.

See [recommendations for first steps after first login](/settings/#other_important_settings)

![Screenshot of the menu to select when to send notifications](/images/notifications2.png "Screenshot of the menu to select when to send notifications")

### Roomwise settings

When the mouse is moved over individual rooms in the room list, 3 grey dots appear on the right-hand edge for each room. After clicking on them, you can set up the notifications for each room individually.

![Screenshot of the notification options in the room settings](/images/notification-rooms.png "Screenshot of the notification options in the room settings")

## using an alternative push gateway (ntfy)

ntfy (pronounce: notify) is a simple HTTP-based pub-sub notification service.

To make use of envs ntfy service, on Android for example, you need two things:

* the `ntfy` app
* a UnifiedPush-compatible matrix app

You need to install the `ntfy` app on each device on which you want to receive push notifications through your ntfy server. The `ntfy` app will provide UnifiedPush notifications to any number of UnifiedPush-compatible messaging apps installed on the same device.

### Setting up the `ntfy` Android app

1. Install the [ntfy Android app](https://ntfy.sh/docs/subscribe/phone/) from F-droid or Google Play.
2. In its Settings -> `General: Default server`, enter your ntfy server URL, such as `https://ntfy.envs.net`.
3. In its Settings -> `Advanced: Connection protocol`, choose `WebSockets`.

That is all you need to do in the ntfy app. It has many other features, but for our purposes you can ignore them. In particular you do not need to follow any instructions about subscribing to a notification topic as UnifiedPush will do that automatically.

### Setting up a UnifiedPush-compatible matrix app

Install any UnifiedPush-enabled matrix app on that same device. The matrix app will learn from the `ntfy` app that you have configured UnifiedPush on this device, and then it will tell your matrix server to use it.

Steps needed for specific matrix apps:

* FluffyChat-android:
  - Should auto-detect and use it. No manual settings.

* SchildiChat-android:
  1. enable `Settings` -> `Notifications` -> `UnifiedPush: Force custom push gateway`.
  2. choose `Settings` -> `Notifications` -> `UnifiedPush: Re-register push distributor`. *(For info, a more complex alternative to achieve the same is: delete the relevant unifiedpush registration in `ntfy` app, force-close SchildiChat, re-open it.)*
  3. verify `Settings` -> `Notifications` -> `UnifiedPush: Notification targets` as described below in the "Troubleshooting" section.

* Element-android v1.4.26+:
  1. choose `Settings` -> `Notifications` -> `Notification method` -> `ntfy`
  2. verify `Settings` -> `Troubleshoot` -> `Troubleshoot notification settings`

If the matrix app asks, "Choose a distributor: FCM Fallback or ntfy", then choose "ntfy".

If the matrix app doesn't seem to pick it up, try restarting it and try the Troubleshooting section below.
