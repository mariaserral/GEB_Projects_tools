# **DELIVERY**
Lucía Fantino, Maria Serral i Lucía Trellu

## 1. Description of the laboratory session
In this laboratory session we used an ESP32-based PCB board with an IMU sensor to obtain 3D orientation in space. 

To proceed with the session, we first set up the hardware; which included the ESP32, the IMU sensor and the PC. 
In Visual Studio Code, we uploaded the `Endowrist_IMU` program to the Endo-module using PlatformIO. First, in the `Endowrist_IMU` program, we verified whether the Wi-Fi credentials (`Robotics_UB`) were correct. As they were already correct, no modifications were needed. However, during the initial evaluation of the system, we observed that it was not functioning correctly, and we later found out the source of the problem was the WiFi connection, which needed to be re-started.

In the same program, we replaced the PC IP address and the device ID that were already defined in the code (`receiverComputerIP` and `deviceId`) with those corresponding to our group.

Then, we ran the `3D_Orientation.rdk` file in the RoboDK to visualize the `Endowrist tool`. 
The following step was to run the `Receive_data_RPY_IMU_world.py` script, but before doing so, we  updated the `TARGET_DEVICE` variable to match our assigned device. After running it, we reviewed the orientation obtained in the 3D representation in RoboDK, and answered the questions in the following section.  

## 2. How you have proceed with the questions we suggest in last section
**2.1. Is the plane 3D object in roboDK moving properly?**

Initially, the plane’s movement was not synchronized with the sensor. Although the sensor was transmitting data, there was a misalignment between the sensor's local axes and the virtual environment's axes.

**2.2. What you have made to properly verify the orientation angles Roll, Pitch and Yaw?**

We placed the sensor on a flat, stable surface, and then made sure that the axes of the virtual object matched the axes of the sensor, which are already defined.

**2.3. Change the 3D object orientation to "surgical_needle". What you have to change in the python code?.**
When visualizing the surgical needle, we modified the Python code by replacing `plane` with `surgical_needle` in the `object_name` variable.


## 3. Final conclusions including a discussion on how you can use these tools in your avant-projecte or also in your TFG or future engineering projects

This seminar was a practical look at connecting hardware sensors to software simulations for robotics. We set up an ESP32 and an IMU through PlatformIO to obtain real-time spatial data. By sending that data over a local Wi-Fi network, we were able to control a 3D plane and a virtual needle in RoboDK using Python. Dealing with the initial connection issues and axis alignment showed why we need a stable network and precise calibration for robotics to work properly.
