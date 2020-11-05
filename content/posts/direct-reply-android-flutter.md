---
title: "Direct Reply Notification for Android in 4 Steps"
date: 2020-08-25T10:30:31+08:00
draft: true
---

### What is Direct Reply Notification?

[Direct reply](https://developer.android.com/training/notify-user/build-notification#reply-action) is a notification action. It enables users to directly enter text into the notification. Meanwhile, the app stays in the background. Usually, you would encounter direct reply when using messaging apps like Whatsapp.

TODO: add gif of direct reply here

### Preparation


### Tools
* Flutter (version)
* Android (version)

### Let's Build It Together

TODO: add image

1. Create a notification channel
2. Show direct reply notification
3. Handle user input
4. Refresh notification

#### Details
Now we enter the Android Land to show our direct reply notifications.

1. Create a notification channel

A channel is required for all notification after Android 8.0 (Oreo, API level 26). For more details, click [here](https://developer.android.com/training/notify-user/channels)

Create a `NotificationHelper.kt` next to `MainActivity.kt`. We will use `NotificationHelper.kt` to create channel and show notifications.

TODO: add create channel gist

2. Show  notification

3. Handle user input
    register notification receiver
    implement notification receiver


4. Refresh notification


### Minor changes
* notification title

References:
[Notifications Tutorial Part 5 - MESSAGING STYLE + DIRECT REPLY - Android Studio Tutorial](https://youtu.be/DsFYPTnCbs8)

TODO: 
initial project
final project