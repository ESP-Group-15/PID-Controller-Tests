# PD Controllers
```
u = Kp * e + Kd * e'
```
Where:
- `u` is the control signal (output of the controller)
- `Kp` is the proportional gain constant
- `e` is the error (desired value - current value)
- `Kd` is the derivative gain constant
- `e'` is the derivative of the error (change in error / change in time)

## Sliding Block Demo
In this example, we have a sliding block that we want to move to a certain position. We can control the position of the block by applying a force to it. The output of the controller is the force that is applied to the block. The force depends on the error between the current position and the desired position as well as the derivative of the error (which is -1 * the derivative of the current position). The derivative term helps to prevent overshoot and oscillation.

### [View Demo](./Sliding-Block.html)

## Sliding Block with Moving Target Demo
In this example, we have a sliding block that we want to move to a certain position that changes over time. We can control the position of the block by applying a force to it. The output of the controller is the force that is applied to the block. The force depends on the error between the current position and the desired position as well as the derivative of the error (which is -1 * the velocity of the block). 

The derivative term helps to prevent overshoot and oscillation. A problem is introduced when the target position changes over time. The block will lag behind the target position. To fix this, an integral term needs to be introduced, forming a PID controller. The integral term will add up all the error over time and this will prevent the block from lagging behind the target position for too long.

### [View Demo](./Sliding-Block-Moving-Target.html)
