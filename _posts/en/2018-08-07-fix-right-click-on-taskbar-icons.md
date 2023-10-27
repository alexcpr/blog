---
layout: post_en
title: Fix right click on taskbar icons
lang: en_US
toc: true
image: /assets/meta/en/fix-right-click-on-taskbar-icons.png
---

When I’m using Windows 10 I am sometimes facing the problem that I can’t right click on my taskbar icons, but I found a few solutions on how to fix it.

_PS: This works on Windows 7 and 8 as well._

## Solution 1: Using Shift + right-click

All you have to do is to hold the **Shift key** while right-clicking any icon on your taskbar, and after that, you will be able to right-click normally on your taskbar icons. But keep in mind that even if this method works, it should be considered a workaround rather than a fix.

## Solution 2: Restart the Windows Explorer

1. Press **Ctrl + Shift + Esc** to open up the **Task Manager**.
2. In the **Task Manager**, locate the **Windows Explorer** process, **right-click** on it, and choose **Restart**.

![Image](/assets/images/fix-right-click-on-taskbar-icons-1.png)

Now see whether the fix was effective by right-clicking an icon on your taskbar.

## Solution 3: Restarting the Tile Data Model Server

1\. Press **Windows Key + R** to open up a Run command. Then, type “**services.msc**” and hit **Enter** to open the Services window.

![Image](/assets/images/fix-right-click-on-taskbar-icons-2.png)

2\. In the **Services** window, scroll through the **Local Services** list and locate **Tile Data Model Server**.

3\. Right-click on **Tile Data Model Server** and choose **Restart**, then wait for the service to be restarted.

![Image](/assets/images/fix-right-click-on-taskbar-icons-3.png)

4\. Right-click anything in your taskbar to see if the fix has been effective.
