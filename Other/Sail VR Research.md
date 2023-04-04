Research subjects: **Normcore, Photon Fusion, and Mirror**
Purpose: Compare and contrast these three frameworks to find the one that works best for us.

### Notes
- Because Red Team 19 is a small and growing team, it would be best to have a flexible platform with lower prices and a fast development process to get us off the ground.
- **We don’t have server equipment to host our own servers.**
- **Multiplayer Requirements**
	- **Host / Join a Room or a Server browser**
	-  **2 - 5 people per session**  
	- Also needs to Support players moving with the Ship
	- Support a large open world with lots of networked objects juggling
	- Networked AI (includes animations, health, movement, etc.)
	- Networked Quest Systems (track progress on quest etc.)  
	- There is more to it than this but those are the basics. . .

### Comparison:
I'll be comparing the following traits: number of CCUs, pricing, and whether or not the service provides hosting. I'll also be calculating a few hypothetical and *very estimated* benchmarks. Assuming that the typical CCU uses around 75 MB per hour ([got that from internet](https://forum.photonengine.com/discussion/14223/ccu-and-data-1player-3gb-processing-speed-or-data-usage-bandwidth-im-lost)), and the avg user spends 8 hours a month.
1. 1000 CCUs in a month with 8000 Room hours, and 600 TB of data 
2. 5000 CCUs in a month with 40000 Room hours, and 15,000 TB of data
3. 10000 CCUs in a moth with 80000 room hours, and 60,000 TB of data.

## [Normcore](https://normcore.io/documentation/)   

*Probably the easiest to get started with in the VR space and most flexible as far as pricing goes. I also have contacts at the company so we could potentially get their support if we have issues. Also it's super tailored to VR so that's a huge plus.* 

My Observations:
- Appears to be very, very intuitive and not very difficult to setup on the frontend and seems to have little to no maintanence on the backend.
- Has all of the needed support required for Sail VR!
- Lots of tutorials
- The official documentation seems to be sufficient too.
- This is my fav blend of simplicity, ability, and adaptablility.
- Normcore is definitely my pick. Here's why:
	- During the development phase of the game, I think that it would be best to start with the simplest solution.
	- In addition, normcore has the potential to remain the best solution for years to come.
	- It's catered towards VR.
	- This seems to me to be the solution that will get us off of the ground and into mutliplayer the fastest.
	- With a hosting service, we don't have to worry as much about very technical and *super* frustrating things such as jitter, client prediction, etc.

Comparison traits:
- Free version
	- Num CCU's: 30
	- Free
	- Free hosting
- Pro -> Unlimited
	- Num CCU's: unlimited
	- $49/mo + 0.01/room hour after 1000 room hours + 0.1/GB after 3TB
	- Hosting

### Pricing Benchmarks
1. 100 CCUs in a month with 800 Room hours, and 60 TB of data: $51.10
2. 500 CCUs in a month with 4000 Room hours, and 1500 TB of data: $93.70
3. 1000 CCUs in a moth with 8000 room hours, and 6000 TB of data: $178.70

## [Photon Fusion](https://doc.photonengine.com/fusion/current/getting-started/fusion-intro)

*Most commonly used for unity multiplayer, super well documented and there's tons of examples on the internet of how to do things, the down side of this is that it could potentially be super expensive once we scale to a larger audience*

My Observations:
* This is a good solution.
* The API is good and it provides a hosting service just like Normcore.
* LOTS of tutorials online
* Seems like a VERY good option. 
* Only beat by Normcore on price and VR integration.
* Easy console crossplay
* More expensive than Normcore

Comparison traits:
- Free version:
	- 20 CCUs
	- Free
	- Hosting - yes
- Paid:
	- Up to 50,000 with *Photon PREMIUM CLOUD* - CCU's are twice as expensive with this.
		- WIth PREMIUM CLOUD: $0.29 per CCU
		- With Photon PUBLIC CLOUD: around $0.185 per CCU
	- Price is based on CCUs ⬆️
	- Hosting - yes

### Pricing Benchmarks
1. 100 CCUs in a month with 800 Room hours, and 60 TB of data: $7.9 ($95 for a year)
2. 500 CCUs in a month with 4000 Room hours, and 1500 TB of data: $95
3. 1000 CCUs in a moth with 8000 room hours, and 6000 TB of data: $185

## [Mirror](https://mirror-networking.gitbook.io/docs/)   

*This is the one recommended by the Senior dev, it's open source but we'd have to figure out the server hosting, match making etc. Which might be a fun challenge for you? ¯\_(ツ)_/¯*

My observations:
- Totally free EXCEPT they don't host your game.
- Apparently the API is difficult.
- If we had a hosting solution this would be a lot more viable (maybe 3rd party? AWS? Some other service?). However, depairing the hosting solution and the API could cause more problems.
- On the other hand, being able to code everything all around would give us more transparency and ability to fix bugs without relying on another team.
- Seems like it would be a good solution for a team with more experience, more money, and more experience. I would probably pull my hair out figuring this out.

Comparison
- Free
	- Unlimited CCUs - as much as *your* servers can handle
	- Free
	- Hosting - NO

### Pricing Benchmarks
Depends entirely on hosting. AWS seems to vary greatly. Anywhere from $9 a month to $400 depending on the instance you get.

# Conclusion
## Pricing
![[desmos-graph.png]]
This graph is viable after the 1000 CCU mark, imo.

This is the price (per month) scaling of Photon (black) and Normcore:
- red: 25 MB/CCU-hour
- blue 50 MB/CCU-hour
- green 75 MB/CCU-hour (this is the one in the price comparison)
- orange: 100 MB/CCU-hour
You can see the Photon pricing jumping from Public Cloud to Premium Cloud at the 2000 CCU mark.

You can check out the graph here: https://www.desmos.com/calculator/psw6qhpdnf

## My Verdict
My verdict is to go ahead with either Photon or Normcore. I MAYBE will be able to figure out Mirror and host it on AWS this summer (don't count on it) which seems to be the cheapest option (I'd really have to look into more to be sure). However, Photon and Normcore both look very doable. It surprised me to see that Photon was just as cheap as Normcore as prices increased. Normcore seems like the simplest of the two but scales massively once you've got a lot of CCUs and a lot of data. I don't know how much data is used per CCU per hour but I figured that I'd give some options. In any case, they are both good options that have good infrastructures and are both very viable for Sail VR. In my estimation, Normcore will be easiest to set up for Sail VR.

Thanks, Garett! I hope that this is helpful!