# Mecanum Drive Base Starter Code

This Vex V5 code is a starter template for a robot utilizing Mecanum wheels. The code is based on the Competition Template, so it can have both autonomous and driver control code.

This drivetrain uses an arcade style of control: the left joystick controls both forward/backward and side-to-side driving, and the right stick controls turns.

There is a 15% deadzone built into the code to account for stick drift. This can be changed in the lines declaring the three input variables:

```
float forwardVal = abs(Controller1.Axis3.position(percent)) > 15 ? Controller1.Axis3.position(percent) : 0;
float sidewaysVal = abs(Controller1.Axis4.position(percent)) > 15 ? Controller1.Axis4.position(percent) : 0;
float turnVal = abs(Controller1.Axis1.position(percent)) > 15 ? Controller1.Axis1.position(percent) : 0;

```

Simply change the "15" in each line to a value that corresponds to the amount of drift in your controllers. Start with smaller numbers and slowly increase them until the drift is gone or minimized.
