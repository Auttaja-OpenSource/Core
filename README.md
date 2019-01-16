# Core
Meta repo for the Auttaja Core.  The distribute core that power's Auttaja.

## What is this?
This is an effort to create a distrubted, scalable framework for building Discord bots.

## Why?
All bot libraries are currently very monolithic, and even with sharding, growing to a large size can still lead to some serious challenges, such as one resource intensive command starving the rest of the bot, even in an asyncronous environment.

## OK, yep, I agree, so what?
So, we are created a distributed framework, where each component is handled by a unique container, and then all of it is run in Kubernetes to handle scheduling, and enforce some sensible resource limits.

## That's neat... but, I run a small bot
That's alright!  The focus of this project might be very large bots serving > 100,000 servers, this project can still be run all on one VM or dedicated server for smaller bots who expect to grow, and don't want to rework everything just to scale.

## I work in X language, do I need to learn a specific language to use this?
No! We wrote the core completely in Python, but the actual meat of your bot: the event and command handlers, can be written in any langugae you choose! We offer a nice common API for accessing the other components.
