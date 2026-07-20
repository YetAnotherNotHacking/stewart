<p align="center">
  <img src="https://github.com/user-attachments/assets/bdb685d1-d0d9-41c2-94ef-2c487b0834eb" alt="Project Banner" width="100%"/>
</p>

<h1 align="center">Stewart Platform Controller</h1>

<p align="center">
  ESP32 • PCA9685 • 6 DoF
</p>

<p align="center">
  A simple, open implementation of a Stewart's platform with kinematics for all 6 DoF.
</p>

# About
This is a simple implementation of a Stewart's platform, something commonly used in settings like simulators or other applications of high strength high dof platforms. This uses an ESP32 and PCA9685 Servo Controller driving MG996r servos to allow for high quality control of the platform.

This reposity also includes a robust desktop control app, currently featuring jog movement and jump to position control for the platform using the ESP's wireless networking. It's planned for later integration for heavier automation (possibly Lua based) to make it easier to automate the platform.

## Resources:
Things to help you around this project

### Assembly
An assembly guide for how to build the project is here: [link](https://docs.google.com/presentation/d/1fX6R6pKFSlhVpZevY7VcBayyEp1o772PA0JAKRDqIYo/edit?usp=sharing)

### Wiring
An image showing the wiring nessecary for the project is below.:
<img width="960" height="540" alt="stewartwiring" src="https://github.com/user-attachments/assets/0c013d9f-8c55-40f4-9c44-78a244a8197b" />

### Programming
See the `code/` folder of this repo!

The desktop code can be run be downloading all of the python files and running main.py. You may need to create an `__init__.py`. Once I have the hardware and confirm it's functionality, I will ship the app more properly as a cross compliled bundled application. For now, however, you are going to need to download and run all scripts.

The ESP32's code can be flashed like any other code. See more information at the end of the assembly guide.

### Bill of Materials:
You can see the bill of materials [here]([url](https://docs.google.com/spreadsheets/d/1tSShUhzgmsK12tPjXI03KWSomIxZK9p5Zw8UYwgLAco/edit?usp=sharing)). It should be noted that a 12v supply could be substituted for a generic high amperage 5v supply. However, for the amerage needed to run this reliably, I chose 12v. It also allows me to complete another hackclub project with a failed supply.

### Adaptation:
Currently, this platform is more of a kinematics demo then something that solves any real problem. The step files and fusion export for the main assembly are included in the `cad/` folder to allow you to modify this for whatever needs you have. Feel free to use this, its open source and I put no requirements on it.

### Support:
If you ever need any support, feel free to create an issue on this repository and I will try to get back to you as fast as I can!

## Render:
<img width="2280" height="1384" alt="0b346e73-0dd3-4ae0-838e-4d3ce46c3656" src="https://github.com/user-attachments/assets/95468742-9be0-438c-bc61-ca229202ae4f" />
