---

title: "Starkit"

author: "Miguel"

description: "A thrust vector controlled electric model rocket designed for propulsive landings"

created_at: "2025-05-20"

---
## May 22: Initial ideas and goal of the project

I always like to begin engineering projects by setting a goal. For this project, my goal is the following:
> To learn, have fun and to make something that I'm proud of by building an electric model rocket capable of lifting off, hovering and landing propulsively.

I want to build a fully reusable vehicle capable of landing propulsively through thrust vector control. If the rocket is capable of performing a 1 meter hop and hover for 30 seconds, I will consider it a success.

Based on my vision for this project, I've set some design requirements. This way, I will try to find the most efficient and cost-effective way possible of creating something that I'll be happy with:

## Design requirements
These are the absolute musts that a design should have:

- The rocket is powered by electric propulsion for cheap and safe flights and fast turnarounds
- The rocket uses thrust vectoring to lift off, hover and land propulsively
- The rocket can perform a 1 meter hop and hover for 30 seconds
- The rocket is modular
	- Components are easily accessible and replaceable
	- The rocket is designed for a future launchpad integration
	  > If I achieve reliable landings, I might try to build a launchpad to launch and catch the rocket from. The rocket should be modular and be designed with this in mind.

		- The rocket has got detachable landing legs and attachable catch pins
		- The pad should be able to hold the rocket until full throttle is reached

## Dream goals
These are not essential but they'd be cool to have:

- The rocket can perform a 10 meter hop
- The rocket can hover for a minute
- The rocket looks as cool as possible


![](Images/Sketches.png)

*Initial ideas and concepts of possible designs*

**Total time spent: 1h 15min**

## May 24: Research on propulsion systems
I've decided to choose a propulsion system first and then work around that. Some options I think would fit this project are:
- Single EDF (Electric Ducted Fan)
- Single propeller
- Counter-rotating propellers
- Ducting a propeller(s) myself

The main things I've learnt today are:
- Ducting a propeller can increase efficiency and thrust.
- EDFs take advantage of this. An added benefit is that they often have stator vanes that minimize the torque produced by spinning the propeller.
- A larger propeller is usually more efficient and provides more thrust. A larger propeller could match the thrust of a smaller EDF while being less expensive, however the torque and gyroscopic effects become greater the more you scale the propeller.
- If I use a single propeller I probably wouldn't want to duct it myself as it could actually decrease the performance (EDFs are propeller and duct combinations specifically made to work together).

I've discarded ducting a propeller myself. However, I still have to make more research to figure out what the best option is. If I manage to overcome the gyroscopic effects, a single propeller would be a nice option over an EDF, as it would be less expensive. Counter-rotating propellers would also be a good option as they cancel their torque, but I still have to research if the thrust of two propellers in series is just the sum of their individual thrust.

**Total time spent: 2h 30min**

## May 24: Research on counter-rotating propellers
I've seen that placing two propellers in series decreases thrust and efficiency. However, if I keep the propellers spaced and use airflow straighteners for feeding the second propeller cleaner air, this could be mitigated.


![](Images/Efficiency.png)
*Test on the efficiency of normal, overlapping and coaxial propellers. Coaxial propellers are about 80% of the efficiency at a low spacing. Source: https://www.youtube.com/watch?v=tFJyE3Uns3o

The reasons I would choose counter-rotating propellers over a single propeller are:
1. They cancel their torque, which means that they don't apply any rotational force to the vehicle and you don't have to worry about gyroscopic effects.
2. You have some control authority in the roll axis. If the rocket gains angular speed, you can correct it by adjusting the throttle of each individual motor. This also allows me to only use 2 servos for TVC, as you only need to correct 2 axis.

![](Images/Ikarus.png)
*The Ikarus model rocket had an issue where whenever it wanted to apply a torque through TVC, it had to apply a perpendicular torque as well due to the gyroscopic effects of a single propeller. In the Ikarus II rocket this problem was solved by using counter-rotating EDFs.*

If I want to get as much thrust as possible, I should use a higher pitch in the rear propeller. However, that would cause the propellers to rotate at different speeds, potentially needing TVC roll control to counteract the torque. I think investing in a higher thrust motor and propeller would be cheaper than increasing the rear propeller pitch and adding another TVC axis. I'll have to do more research to figure this out, but I think counter-rotating propellers are a really good option.

![](Images/CoaxialTest.png)
*Test showing the thrust of different propeller spacings and rear propeller pitch difference. Source: https://www.icas.org/icas_archive/ICAS2014/data/papers/2014_0072_paper.pdf According to https://drones.stackexchange.com/questions/1209/do-propellers-layered-on-top-of-each-other-have-twice-the-thrust-of-one-propelle, you can get almost the full thrust if you increase the pitch of the rear propeller.

**Time spent: 1h 30min**

