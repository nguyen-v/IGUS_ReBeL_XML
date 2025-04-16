## Introduction
This repository is a collection of XML files used in a pick-and-place coin sorter project, developed at l'Espace des Inventions (EDI) in the context of their robotics exhibition.

## Requirements
- IGUS Robot Control software from [the official website](https://www.igus.eu/automation/robot-control-system/robot-software).
- An IGUS ReBeL 4-DoF arm
- Custom PCBs: PLC interface and Arduino Nano Every interface. The code related to the arduino is found [here](https://github.com/nguyen-v/IGUS_RebeL_Interface)

## Installation
1. Clone or download this project, and place the xml files in a subfolder of `C:\iRC-igusRobotControl-V14\Data\Programs`, for example `C:\iRC-igusRobotControl-V14\Data\Programs\EDI`

2. In your network settings, make sure to set IP assignment to manual. Then set the IPv4 address as `192.168.3.1` and the IPv4 mask as `255.255.255.0`

3. Connect an ethernet cable between your computer and the robot and open IGUS Robot Control.

4. Press on connect

5. Load the `main.xml` file with the Load button

6. Press Play

## Troubleshooting
If the robot stops at an awkward position (different from any of the normal states), you must manually bring it back to its resting pose.

1. Manually jog it close to the rest position, then load the `straight_to_rest.xml` file. This will move the robot back to its resting position. Make sure it can move to the rest position without encountering any obstacles.

2. Load the `main.xml` file again.

3. Press Play
