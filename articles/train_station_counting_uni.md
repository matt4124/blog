# Improving the train station efficiency for ENG30002 - Engineering Technology Sustainability Project
*Semester 1, 2025*

#### The Problem
During this project we were tasked as a group to design a solution to a sustainability challenge within our chosen majors. 
Within my group we had 2 software majors, 1 mechatronics and 1 electrical/electronic engineering major (me).
Our group initially decided to opt for the challenge of improving the efficiency of the Melbourne metro train network.  
Obviously this was a very general problem, so we narrowed it down to specifically improving the ability of the train network to more efficiently move people to their destinations.
The general idea behind this was basically to attract more people towards public transport, thus reducing cars on the road. 

#### The Project Solution
The solution we came to was basically a way to try to optimise the train times and number of train carriages of each individual train. 
Our method to achieve this was a workflow, where data on the number of people was collected for each train platforms via platform sensors/cameras/ptv, then sent to an AI in order to predict the future number of people at each platform. This information would then be used in deciding on train times, and how many train carriages to send for each route.  
![Project Plan](/blog/images/uni_projects/sustainability_project_plan.png)

#### My Part 
My part in this project was the initial part of the workflow, where the number of people at each platform would be obtained and sent to the AI for predicting the future number of people. At first I explored a couple of options, platform pressure sensors, IR sensors and even a wifi network to count the number of phones in the area. Eventually though I settled for people counting via an image AI connected to a camera. 
There were a few advantages of this approach, for one the image AI is one of the most accurate methods. As well, many train station platforms around Melbourne already possess security cameras. Which can be accessed securely. 





![Project Explanation](/blog/images/uni_projects/sustainability_project_explanation.JPG)

![Project Demonstration](/blog/images/uni_projects/sustainability_project_demonstration.gif)

- Developing a plan to improve the current metro train network efficiency
  - Efficiency measured in how quickly and effectively can we move people en mass.
- I worked on implementing a people counting algorithm for a proof of concept.
- 
