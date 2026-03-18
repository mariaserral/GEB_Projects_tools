# **DELIVERY**
Lucía Fantino, Maria Serral i Lucía Trellu

## **1. First operating performances diagnostic** 

During the initial evaluation of the system, we observed that it was not functioning correctly, and we later found out the source of the problem was the WiFi connection, which needed to be re-started. Moreover, we had to ensure both the computer and the ESP32 device were connected to the same WiFi net.
On the other hand, we needed to make sure the orientation of the axes that were represented in the simulation program of the computer matched those of the sensor, which were already established.

## **2. Corrections we have made in the code** 
First, in the `Endowrist_IMU` program, we checked whether the Wi-Fi credentials (`Robotics_UB`) were correct. As they were already correct, no modifications were needed.
In the same program, we replaced the PC IP address and the device ID (`receiverComputerIP` and `deviceId`) that were already defined in the code with those corresponding to our group.

Before running the `Receive_data_RPY_IMU_world.py` script, we also updated the `TARGET_DEVICE` variable to match our assigned device.

Finally, when visualizing the surgical needle, we modified the Python code by replacing `plane` with `surgical_needle` in the `object_name` variable.

## **3. Final conclusions** 

