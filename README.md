RobotMovement
=============

Move your own Robot (comes with Demo code)
==

Moving Robot
===
This is a library for the basic functions to move a robot. It can go forward, backwards, turn right, and turn left. The amount can be determined by how long the delay is after the action function.


Functions
===
initMotors() - initializes the motors;

MoveForward() - moves forward;

MoveBack() - moves backward;

TurnLeft() - turns left;

TurnRight() - turns right;

StopBot() - stops the robot;

Delay() - does an action for 1000000 cycles;

ShortDelay() - half of Delay();


Demo Code
===

int main(void) {

	WDTCTL = WDTPW|WDTHOLD;                 // stop the watchdog timer

	initMotors();
	
	
	while(1)
	{
		MoveForward();
		Delay();
		TurnLeft();
		ShortDelay();
		MoveForward();
		Delay();
		Delay();
		StopBot();
		ShortDelay();
		TurnRight();
		ShortDelay();
		MoveBack();
		Delay();
		TurnLeft();
		ShortDelay();
		MoveForward();
		Delay();
		Delay();

	}

}




