# Autonomous-Self-Driving-Car
An Autonomous Self driving car using Deep Q network (Reinforcement Learning)


A Reinforcement Learning algorithm that drives a self driving car.


This algorithm utilizes Deep Q-Learning with 5 inputs. The first 3 inputs come from 3 sensors on the front, left, and right of the car which returns the number of sand blocks around them. The last 2 inputs return the orientation of the car, a value from -1 to 1 which represents a value between -180 to 180 degrees corresponding to objective.The algorithm gets a small reward for heading towards the object and a small negative reward for heading away. These values are set to 0.1 and -0.1. These values were left small so that the car would have the freedom to drive in the opposite direction a bit in order to avoid sand without being heavily penalized. In contrast, the car receives a -5 reward if it drives over sand. Furthermore, the car receives a -1 reward if it goes to close to the sides of the map. Finally, a variable/scaled reward is received each time the algorithm reaches it's objective which is defined by previous_steps - current_steps. This additional reward will ensure that the algorithm gets penalized for taking a longer route than the previous run and that it will be rewarded if it takes a shorter route. This reward scales corresponding to high much longer/shorter the current route is compared to the previous route.
