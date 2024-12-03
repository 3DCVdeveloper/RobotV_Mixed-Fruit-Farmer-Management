# RobotV_Mixed-Fruit-Farmer-Management
Mixed Fruit Farmer Management

# Brief Introduction
This guide will introduce how to reproduce an orchard robot demo using Solidworks and Isaac Sim. This demo demonstrates how to use OmniGraph to control robot joints, and use the a and b keys to retract the front and rear four tripods, and use the c key to automatically expand the tripod with one click.

# step
1. Solidworks modeling
   
Build an orchard robot model in Solidworks, including all components and joints.

Ensure that the coordinate system of the model is located at the center of the robot base.

2. Export URDF

Install the Export as URDF plugin for Solidworks.

Configure the baseline axis and coordinate system of the model.

3. Convert to USD
   
Select lsaac Utils ->Workflow ->URDF lmporter menu in the lsaac sim menu to access the urdf extension.

Import URDF file and convert URDF to USD.

4. Using OmniGraph to Control Robot Joints

Select Window ->Visual Writing ->Action Graph in the lsaac sim menu

Create a new OmniGraph script.

Use the Read Keyboard State Node to listen for keyboard input.

Using Articulation Controller to Control Robot Joints

Use Constant Toke Node to store robot joint names.

Convert keyboard Bool signals to numerical values using To Double Node

Create an array using Make Array

Creating Double Floating Point Numbers with Constant Double

Using On Playback Tick Node clock source to control robot loop cycle

Using Delay for Waiting Control

The above are the functions used in the example program,

The example program operation is as follows:

Click on 'a' to create the left and right front brackets for the recycling robot in the interface, click 'b' to create the left and right rear brackets for the recycling robot, and click 'c' to extend the brackets in order with one click.
