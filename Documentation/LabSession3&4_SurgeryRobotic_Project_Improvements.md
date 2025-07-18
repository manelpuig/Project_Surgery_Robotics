![University of Barcelona Logo](././Images/Session1/figure1.png)

## Degree in Biomedical Engineering
## ROBOTICS AND CONTROL OF BIOMEDICAL SYSTEMS
# **Surgery Robotics Project**
### Laboratory sessions 3 & 4: Biorobotics Laboratory Surgery Robotic system Project improvements

---

In the previous session you have seen the main performances of your first prototype of a DaVinci surgery system.

You have seen the complexity to perform a simple surgery process in roboDK simulation environment.

### The objective of this laboratory session will be:
- Identify the main limitation performances of your first prototype
- Propose and design useful solutions to improve the system
- Implement your own improved surgical robotic system
- Verify the improvements in the system performances for the same surgical process in roboDK simulation environment

### Proposed improvements for Surgery Robotic system prototype in Biorobotcs Lab

The main improvements are based on:
- Servomotors module:
    - apply the RPY angles to the four servomotors to obtain the desired Gripper orientation.
    read the torques on the four servomotors to detect the gripper contact with the tissue.
    - send these torques to the Gripper module and PC.
    ![ServomotorsModule](././Images/Session1/Servos1.png)
    ![ServomotorsModule](././Images/Session1/Servos2.png)
    ![ServomotorsModule](././Images/Session1/Servos3.png)

- Endowrist module:
    - send RPY angles to Gripper module
- Gripper module:
    - receives the RPY angles from Endowrist module and correct the gripper orientation
    - receives the torques from the Servomotors module.
    - Apply a vibration with actuator to feel the contact with the tissue.

- PC module:
    - receives the RPY corrected angles from the Gripper module and perform the simulated gripper orientation
    - receives the RPY angles from the Endowrist module and apply them to the UR5e robot arm with a proper python based sockets program
    - receives the torques from the Servomotors module and apply a color code and write the numeric values
    
![Proposed Project Improvements](././Images/Session1/ProjectImprovements2.png)

### Laboratory sessions: Tasks

The proposed tasks for this first session are:
- Connect properly the Hardware setup
- Save the ESP32 InitialPrograms for the 3 ESP32 modules using th VScode Arduino Community Edition. Take care about the proper IP address of each module and PC.
- Run the InitSurgeryRobotic_students.rdk file in the roboDK program to visualize the UR5e robot arm and the Endowrist tool.
- Test the system performances described above 
- Try to perform a suture process in simulation according to the following video:
[![suture process in simulation](Images/Session1/training.png)](https://youtu.be/1t3-Ggcp_Hg?feature=shared)

Show and explain the system performances to your teacher.