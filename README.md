# App_RFT
This project contains the application "RFT2.exe" files for the VR rod and frame test (RFT).  

It was developed for the 2023/24 study "In Rod we Trust - The evaluation of virtual Rod and Frame Test as a cybersickness screening instrument" by J. Josupeit. 

To get access to the original Unity scene (v.2019.1.11f1) and custom-created scripts, go to [RFT:Project_RFT](https://github.com/JudiJ/RFT/tree/main).

In addition to downloading the zip folder, the requirements are Unity (v2019.1.11f1), Steam VR, and for interaction a HTC Vive controller. 

## The Application
After unpacking the zip-folder the “RFT2.exe” will start in Windowed mode. The VR version of the RFT will start in a grey waiting room in which a participant's code needs to be entered. Thereafter, a rectangular frame and a rod, represented by two dots will be presented in perfect vertical alignment. The User can start a new trial by pressing the trigger. At the start of each trial, the frame is rotated either +/-33° or 0° along the z-axis and the rod is either +/-22° or +/- 11°. Using the trackpad of the controller, the rod can be rotated (counter-)clockwise by pressing the (left) right side of the trackpad. To confirm the estiamtion the trigger needs to be pressed again, which will start a new trial. After 14, 26, and 38 trials a waiting room for the assessment of questionnaires is displayed. 

This application was programmed for the HTC Vive controllers. The application should work independently from the head-mounted display, but other custom key-bindings will be required for the interaction. 

The application should run in Windows, Linux, MacOS, indiscriminately. 

### Functions
- GUI with a input field to insert a participant's code [enabled by pressing enter on the numbpad]
- dark waiting room while the menu is open before the RFT is displayed [enabled by pulling the HTC Vive's trigger]
- rotate the rod clockwise with the right side, counterclockwise with the left side on the controller trackpad 
- confirm the adjustment of the rod and start a new trial by pulling the trigger at the back of the controller
- option to reset the current trial to the starting position by pressing escape
- end the application by right-clicking the mouse or closing the window
- each trial is automatically recorded in a CSV file (the delimiter is "/" the decimal separator is ",") after confirmation of the entered participant's code:
    - The following information will be logged every frame:
        - the system-time ("yy/MM/dd HH:mm:ss:fffff")
        - the trial number
        - the event of pulling the trigger (unequal to the trial number in cases in which resetting a trial is necessary)
        - z-rotational axis of the frame and the rod global Unity coordinates
        - the input on the x- and y-axis of the controller
        - the position and rotation of the virtual camera in global Unity coordinates

## Project Layout
The first files in this project are the "RFT2.exe" application, the files for the key and controller bindings, as well as the Unity player and crash handler files. 

Additionally, this project includes two folders:

- [MonoBleedingEdge](https://github.com/JudiJ/Application_RFT/tree/main/MonoBleedingEdge) contains autogenerated information by Unity
- [RFT2_Data](https://github.com/JudiJ/Application_RFT/tree/main/RFT_Data) contains the game managing files, Unity default and built-in resources, plugins, as well as global game manager, resource and shared assets.
    - The sub-folder [Managed](https://github.com/JudiJ/Application_RFT/tree/main/RFT_Data/Managed) contains all dll-, pdb- and mdb-files for the application

### Supplementary
Unity game engine version v2019.1.11f1, Steam VR (version 2.3.2) enhanced with custom-designed features. 


The application was originally run with a Windows 10 (64 bit) computer, NVIDIA GeForce RTX 2070 GPU and Intel Core i7-9700K processor.

Shield: [![CC BY 4.0][cc-by-shield]][cc-by]

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg
