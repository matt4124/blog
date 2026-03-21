## Medical Communication Application developed for ENG20010 - Engineering Technology Design Project
*Semester 2, 2024*

#### The Problem
For this unit we were given the problem to solve of connecting GPs and specialists to connect to patients. Basically a medical software application similar to skype that allows for video, audio, text, and sensor data to be sent between devices. The main difficulty with this project would be in figuring out how to implement all of the required features within Labview. 

> [!Note]
> Labview is a "graphical system design and development environment", in other words it can be thought of as a programming language that uses a GUI to program instead of the usual text based programming.
> An example of Labview in action:
> ![Labview Example](/blog/images/uni_projects/medi_app_example.jpeg)

#### My Part
I basically worked on most parts of this project, the whole software ran in an event loop. Host's are able to connect to eachother via a TCP connection, and all data was properly formatted in a very basic protocol that I was able to design. The following data was able to be transmitted between devices using the software:
- Live Audio chat from the PC microphone
- Live Video streaming from the PC camera
- Images sent from the PC camera
- Texts
- Temperature

The temperature data was sent via a DAQ unit, which is basically a microcontroller that is able to be programmed via Labview. 
