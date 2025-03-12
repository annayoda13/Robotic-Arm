The Robotic Arm Control System is a simple command-line program designed to simulate the control and operation of a robotic arm with three segments: base, upper arm, and lower arm. The system allows users to interactively control the angles and torques of these segments, reset the arm to its initial position, and adjust the torques independently.

This simulation can be helpful for understanding how a robotic arm works in terms of movement and torque application. The system mimics real-world control of robotic arms, where precise angles and torque adjustments are essential for performing tasks in various applications, such as manufacturing, robotics research, or even entertainment.

Features:
Move the Arm: Users can move the robotic arm by specifying the angles of each arm segment (base, upper, and lower) as well as the torque for each segment. The angles define the arm's position, while the torque determines the force applied to each segment.

Adjust Torque: The system provides a way to adjust the torque applied to each arm segment independently, allowing for precise control over the arm's movements without changing the angles.

Reset the Arm: Users can reset the arm back to its initial position, where all the angles and torques are set to zero. This feature is useful for starting over or bringing the arm to its home position after performing a series of movements.

Interactive Command Interface: The system uses a simple text-based command interface that guides users in issuing commands to move, reset, and adjust the arm. The user interacts with the system by typing commands in a terminal.

State Display: After each command, the system prints the current state of the robotic arm, showing the angles and torque values for the base, upper arm, and lower arm segments.

Command Reference
The system accepts the following commands:

1. Move the Arm
To move the robotic arm, use the move command followed by the desired angles for the base, upper arm, and lower arm, as well as the torques for each segment. This command will update the arm's position and torque values.

php-template
Copy
move <base angle> <upper arm angle> <lower arm angle> <base torque> <upper torque> <lower torque>
Example:

arduino
Copy
move 30 45 90 5.0 3.5 2.0
This sets:

Base angle: 30 degrees
Upper arm angle: 45 degrees
Lower arm angle: 90 degrees
Base torque: 5.0 Nm
Upper arm torque: 3.5 Nm
Lower arm torque: 2.0 Nm
2. Adjust Torque
You can independently adjust the torque for the base, upper arm, and lower arm segments using the adjust_torque command. The format is as follows:

php-template
Copy
adjust_torque <base torque> <upper torque> <lower torque>
Example:

nginx
Copy
adjust_torque 6.0 4.0 3.5
This sets:

Base torque: 6.0 Nm
Upper arm torque: 4.0 Nm
Lower arm torque: 3.5 Nm
3. Reset the Arm
To reset the robotic arm to its initial position (all angles and torques set to zero), use the reset command:

perl
Copy
reset
4. Exit the Program
To exit the program, use the exit command:

bash
Copy
exit
Program Flow
Startup: When the program begins, the system prints a welcome message, explains the available commands, and enters a loop where it waits for user input.
Command Processing: The user can input commands to move the arm, adjust its torque, reset its position, or quit the program. After each command, the current state of the arm is displayed.
State Update: Each time a command is executed, the program updates the arm's angles and torques as per the user's input, ensuring the state is visible to the user in real-time.
Exit: The program will continue running in a loop until the user inputs the exit command.
Example Session
yaml
Copy
Welcome to the Robotic Arm Control System!
Commands:
  'move <base angle> <upper arm angle> <lower arm angle> <base torque> <upper torque> <lower torque>'
  'adjust_torque <base torque> <upper torque> <lower torque>'
  'reset' to reset the arm to its initial position
  'exit' to quit the program

Enter command: move 30 45 90 5.0 3.5 2.0
Current Arm Angles and Torque:
  Base Angle: 30 degrees, Torque: 5 Nm
  Upper Arm Angle: 45 degrees, Torque: 3.5 Nm
  Lower Arm Angle: 90 degrees, Torque: 2 Nm

Enter command: adjust_torque 6.0 4.0 3.5
Current Arm Angles and Torque:
  Base Angle: 30 degrees, Torque: 6 Nm
  Upper Arm Angle: 45 degrees, Torque: 4 Nm
  Lower Arm Angle: 90 degrees, Torque: 3.5 Nm

Enter command: reset
Current Arm Angles and Torque:
  Base Angle: 0 degrees, Torque: 0 Nm
  Upper Arm Angle: 0 degrees, Torque: 0 Nm
  Lower Arm Angle: 0 degrees, Torque: 0 Nm

Enter command: exit
How to Run
Compile the Code: To compile the C++ code, use the following command:

bash
Copy
g++ robotic_arm.cpp -o robotic_arm
Run the Program: After compilation, run the program with:

bash
Copy
./robotic_arm
Interact: Follow the instructions displayed on the terminal to control the robotic arm, issue commands, and see the state of the arm after each action.

Requirements
A C++ compiler (e.g., g++) for compiling the program.
A terminal or command prompt to run the program.
Basic understanding of C++ and how to execute programs from the command line.# Robotic-Arm
