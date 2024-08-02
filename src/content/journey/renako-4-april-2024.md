---
title: 'Renako development blog - 4 April 2024'
description: "The real gameplay screen is playable with the real beatmap IO"
pubDate: 'April 4 2024'
heroImage: '/journey/hero/renako-4-april-2024.png'
tags: ['renako']
---

## The beatmap IO storage
Now the game can read the beatmap from the game folder (the beatmap folder is <game_storage>/beatmaps). The beatmap file is .rkb file. But since the beatmap serializer still using the same Beatmap class that's using in the game database and it store the entire BeatmapSet object inside it and serialize it into the file. This will fix!

## Dropping of test collection
The test collection is the 5 beatmapset that we use when we just not done the beatmap IO with the game storage by completely inject these 5 beatmapset (with beatmap inside it) into the game's database on launch. But since the game can now read the beatmap from the game storage that's why from now I will start dropping the usage of the test collection from here. Now the game will try to "write" the 5 beatmapset into the game's storage only on first launch and no longer injected it everytime you launch the game. So now if you don't want to use the test beatmap just delete it in the game storage.

## The real gameplay screen is available
From the IO part and the last post that we implemented the gameplay POC code. So now the game's gameplay screen that use the real beatmap is available! Note that only the beatmap background now interact with the value from the user's config. The scroll speed will implemented later. This part also come with the easy loading screen that will be use later when the playfield loading time has getting long (but now it's really short that you don't need to have it) The key is D F J K

> The test collection will embed with the test 5 beatmapset that have a random note (1 note per minutes) through the whole song.

![Current gameplay screen](/journey/content/4-april-1.png)
