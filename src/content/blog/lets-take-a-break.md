---
title: "Let's taking a break"
description: ""
pubDate: 'Mar 20 2023'
heroImage: '/blog/hero/taking-break.png'
---

Since I am creating the [first version of Rūrusetto](https://github.com/Rurusetto/rurusetto/tree/main) I have an idea to create the osu!lazer that fully support on customization of the 'custom ruleset' function. That's why the first idea of Freedom Dive has been created. And that idea is inside my bucket list for a long time.

On just a normal day in my Discord I see the message in Tau ruleset development server.

> It's a good idea if we can have some multiplayer of Tau...

That's why I recover the idea of *Freedom Dive* from the list and try to make this idea work and it's work!

I try to working on the project on every free time that I have. Add some functionality from requested on the site and the custom client. Until during February something has happened.

Let's talk about the infrastructure of the Freedom Dive first, the Freedom Dive have 5 main modules include :

- Freedom Dive main site (Django)
- Freedom Dive Database for storing the user and the score (PostgreSQL)
- osu-web to make the client work include a lot of microservice there (Docker)
- osu! database connect with osu-web (MySQL)
- osu! server spectator to make multiplayer and spectator work (.NET)

These are the main component to make the Freedom Dive work. All component when running on the local machine it use 7-8 GB of memory but if these all component are running on the cloud so how much it cost?

At first I run everything on the one DigitalOcean virtual machine (a.k.a droplet) using 8 GB RAM and it cost 48 Dollar per month (not include VAT 7% on my country)

But when running on one machine and it make the server not smoothly, that's why I seperate these into main 4 droplets and 1 object storage (in Digital Ocean call 'Space') for storing all beatmap metadata, file and replay in there.

![Current infrastructure of Freedom Dive](/blog/content/freedom-dive-infra.png)

All of these cose around 53 dollar include VAT (4 GB RAM Droplet + 1 GB RAM Droplet * 3 + 1 Space). I pay these from my personal money since this project is still in beta phase and I don't want to add some donation to the project (If you registered to the server you can see that I added you the osu!supporter on every account on the server too).

After that the server fee are getting expensive and the uptime of the service still not much improve since some service are not working properly due to the server size that I cannot make it bigger due to the budget.

![Example of an APM alert from the agent in the droplet that I get it a lot of time](/blog/content/freedom-dive-infra-2.png)
But the Freedom Dive still need a lot of component and work to make the server fully working like score processor, leaderboard etc. but I cannot afford any more of the server fee that's I expect it a lot more when all component is online so I decided to stop it here.

# Another reason : time and health
When I think to create the new side project I will try to maintain it as much as but as I have the college (I studying year 3 in Software Engineering) and my part-time as Software Engineer in a tech company I try to maintain this but since this year I have more work in college to be done and cannot much spend time here, that's why I think it's better to close the project that I think I cannot take care of it.

My health since I start in college is getting worse (sleep time, paranoid from professor in the college etc.) so I need the time to maybe take care of myself more.

# Some cool statistics
- 579,491 beatmaps has been imported in the database
- 404 score (include failed attempt) has been submitted

# Final thanks
This project is not much progress without someone playing on this server and some custom ruleset developer. It's 4 months that I gain a lot of knowledge, experience and fun from this project!

Goodbye Freedom Dive, hope this project will be running again (if my salary can maintain this project without donation) in the future and thank you to all who support this project!

PS. Don't be sad, I backed up all server component so let's hope that I can put this into production soon!
