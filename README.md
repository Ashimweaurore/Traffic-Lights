# Traffic-Lights
#Gishushu Traffic Lights System Specification
1. Objective
The Gishushu Traffic Lights system is designed to manage vehicle and pedestrian traffic at an intersection by cycling through states (Red, Green, and Yellow) to regulate safe and orderly movement. The system operates autonomously, with set timers for each light, and cycles continuously.

2. System States and Actions
The system operates in three main states: Red, Green, and Yellow. Each state serves specific purposes for managing traffic flow and safety.

Red State:

Description: This is the stop signal for vehicles. When the light is Red, all vehicles must stop and wait.
Duration: Typically lasts 60 seconds, allowing pedestrians to cross the road if a crosswalk is present.
Action: The Red light is illuminated, signaling vehicles to stop.
Transition Condition: After the timer expires, the light transitions to Green.
Green State:

Description: This state allows vehicles to proceed through the intersection.
Duration: Lasts around 45 seconds, during which vehicles can pass, and pedestrians must wait.
Action: The Green light is illuminated, signaling vehicles to proceed.
Transition Condition: When the timer expires, the light transitions to Yellow.
Yellow State:

Description: The Yellow light is a warning signal indicating the Green light will soon change to Red, giving vehicles time to prepare to stop.
Duration: Lasts approximately 5 seconds, providing a short interval for vehicles to clear the intersection.
Action: The Yellow light is illuminated, signaling vehicles to slow down and prepare to stop.
Transition Condition: Once the timer expires, the light transitions back to Red.
3. State Transitions
Red to Green: When the Red state timer expires, the light changes to Green, allowing vehicles to proceed.
Green to Yellow: After the Green timer expires, the light transitions to Yellow, signaling caution and the need to prepare to stop.
Yellow to Red: After the Yellow timer expires, the light changes to Red, requiring vehicles to stop.
4. Additional Conditions and Safety Measures
Power Off: In case of a power outage, the traffic light system shuts down. Upon restoration of power, the system reverts to the Red state as a safety measure.
Emergency Mode (optional extension): In case of emergency or congestion, an operator or sensor system could override the cycle, prioritizing one direction to manage traffic flow dynamically.
5. Assumptions
The system operates in a continuous loop unless manually overridden or power is interrupted.
Each state has a fixed duration, which can be adjusted based on traffic density if sensors are implemented.
Pedestrian crosswalk signals are synchronized with the Red state, allowing safe crossing.
6. Diagram Interpretation
The state diagram shows the progression from Red to Green to Yellow and back to Red.
Arrows represent transitions based on timer expirations for each state, and each state displays its associated traffic action.
