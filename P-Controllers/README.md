# P Controllers
```
u = Kp * e
```
Where:
- `u` is the control signal (output of the controller)
- `Kp` is the proportional gain constant
- `e` is the error (desired value - current value)

## Sliding Block Demo
In this example, we have a sliding block that we want to move to a certain position. We can control the position of the block by applying a force to it. The force is proportional to the error between the current position and the desired position. The force is also proportional to the gain, which is a constant that we can adjust to make the block move faster or slower. The force is calculated by multiplying the error by the gain. The force is then applied to the block, which causes the block to move. However, this will cause an infinite oscillation if 
there is no friction. This is something that the derivative term that is introduced in the PD controller can help with. 

### [View Demo](./Sliding-Block.html)
