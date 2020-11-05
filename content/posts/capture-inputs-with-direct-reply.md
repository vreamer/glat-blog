---
title: "Capture Input with Direct Reply Notification in Android with Flutter"
date: 2020-08-24T12:43:42+08:00
draft: true
---

### What is Direct Reply Notification?

[Direct reply](https://developer.android.com/training/notify-user/build-notification#reply-action) is a notification action. It enables users to directly enter text into the notification. Meanwhile, the app stays in the background. Usually, you would encounter direct reply when using messaging apps like Whatsapp.

TODO: add gif of direct reply here

### Why did I want it?
I was not building a messaging app, but the idea of capturing input from notification without opening the app appeals to me. I was building an app to capture ideas quickly with minimum interruption to my workflow. 

Think of this scenario, when you form an interesting idea while reading. You want to capture that idea quickly without breaking the current reading flow. Normally, you would write it down on a paper nearby or open another app to take notes. 

I used to take notes like that. But after the thousandth time of losing that piece of paper or getting distracted while opening another app. I decide to build an app that will capture my idea from the notification. So I can simply swipe down, type my idea, swipe up and move on.

### Flutter Notification Alternatives
* Local Notifcation
* Firebase Messaging

### Tools
* Flutter (version)

### Let's Build It Together

create app
`flutter create direct_reply_notification`

#### Android Land
Now we enter the Android Land to show our direct reply notifications.

1. Create a notification channel

A channel is required for all notification after Android 8.0 (Oreo, API level 26). For more details, click [here](https://developer.android.com/training/notify-user/channels)

Create a `NotificationHelper.kt` next to `MainActivity.kt`. We will use `NotificationHelper.kt` to create channel and show notifications.

TODO: add create channel gist

2. Show  notification

3. Handle user input

4. Refresh notification


### Minor changes
* notification title

References:
[Notifications Tutorial Part 5 - MESSAGING STYLE + DIRECT REPLY - Android Studio Tutorial](https://youtu.be/DsFYPTnCbs8)