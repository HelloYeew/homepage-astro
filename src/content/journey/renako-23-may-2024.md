---
title: 'Renako development blog - 23 May 2024'
description: "First update since a long time ago"
pubDate: 'May 24 2024'
heroImage: '/journey/hero/renako-23-may-2024.png'
tags: ['renako']
---

> Now since I spend almost all of my free time on this project and I want somewhere to update this project's progress properly that's why I start this daily development blog, you can follow my blog for this project's progress!

## Song selection screen final settings
Now all the main flow has already completed in song selection screen with some WIP final settings screen. Something still a bit strange here but will be fixed soon

![WIP final settings screen](/journey/content/23-may-1.png)

## More interaction on the component
At first I didn't implemented the component to interact with the player's action but I implemented some of these and want to see the interaction

- Now the button (back button and go button) will move on hover and flash with the current beatmapset's BPM
- If player gone "idle" (no interaction for sometime), the screen will set to idle mode (can disable this in settings)

![Song selection screen when go idle](/journey/content/23-may-2.png)

## First real gameplay implemented on code

I already [created a pull request](https://github.com/HelloYeew/renako/pull/15) a first version of gameplay in test scene but you can still watch the first version of it on the video attached in pull request. It's just a PoC but full design also available on [Figma](https://www.figma.com/file/slfKBAdlVhJXxCgGKEmNfa/Renako-Design?type=design&node-id=358-3&mode=design). Feedback is appreciated!

![Current gameplay design (more in Figma!)](/journey/content/23-may-3.png)
