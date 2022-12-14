# Safe Policies for Factored Partially Observable Stochastic Games
## Steven Carr, Nils Jansen, Alex Nettekoven, Sriram Bommantanki, Ufuk Topcu
Multimedia appendices for Safe Policies for Factored Partially Observable Stochastic Games

### Tethered UAV delivery

In this tethered UAV delivery example, two tello drones are operating in a 6x6 gridworld. The high-level planner gives commands every 5 seconds, resulting in a UAV moving either one or two spaces per decision-cycle.
In the presented example, the red Agent 1 is tasked with collecting information above the green square and then delivering it to the purple square on the opposite corner of the grid. Simultaneously, Agent 1 must remain inside a communication/observable window of the blue Agent 2, which is flying above it.
In the video, we present 3 conditions where Agent 1 attempts to perform this task. The first is with a window of size 3, where Agent 1 must wait for Agent 2 to move within observable distance of the green target.  The second involves the condition of window size 4, where the Agent 1 moves more freely and only slightly has to modify their trajectory to satisfy the objective. Finally, we show the condition where Agent 1 ignores the safety constraint and violates the safety objective in an attempt to minimize the obtained reward.

{% include youtube_tello.html%}


### Mars Rover with Adversarial Charging

When the active charging location is at A<sub>1</sub> and Agent 1 has moved from location s<sub>4</sub> to location s<sub>2</sub> (energy level low at e=1), the permissive policy only allows for one transition - back to s<sub>0</sub> with the active A<sub>1</sub>.
Similarly in the first instance (active charge A<sub>1</sub>), Agent 1 needs three actions to reach T<sub>1</sub> at s<sub>6</sub> and then three to return to charge. 
Therefore the permissive policy rules out the transition from s<sub>3</sub> to s<sub>6</sub>. 
The POMDP solver takes that into account and therefore sees no utility gained by going from s<sub>2</sub> to s<sub>3</sub>.

{% include youtube_mars.html%}


### Autonomous Car with Sensor Array

In the autonomous driving simulator, the permissive policy often just constrains the Agent 1's ability to go straight through an intersection forcing Agent~1 into more uncertain routes. See the video below for how the permissive policy changes the nominal path of the autonomous vehicle.


