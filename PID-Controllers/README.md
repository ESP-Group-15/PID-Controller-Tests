# PID Controllers
```
u = Kp * e + Kd * e' + Ki * E
```
Where:
- `u` is the control signal (output of the controller)
- `Kp` is the proportional gain constant
- `e` is the error (desired value - current value)
- `Kd` is the derivative gain constant
- `e'` is the derivative of the error (change in error / change in time)
- `Ki` is the integral gain constant
- `E` is the integral of the error (sum of all the error over time)

## Sliding Block with Moving Target Demo
In this example, we have a sliding block that we want to move to a certain position that changes over time. We can control the position of the block by applying a force to it. The output of the controller is the force that is applied to the block. The force depends on the error between the current position and the desired position, the derivative of the error (which is -1 * the velocity of the block) as well as the integral of the error (sum of all the error over time). 

The derivative term helps to prevent overshoot and oscillation. The integral term adds up all the error over time and prevents the block from lagging behind the target position for too long.

### [View Demo](./Sliding-Block-Moving-Target.html)
