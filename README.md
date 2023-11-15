# frontYardMonitoring
This is my final year project. It monitors for human presence within a defined restricted area, and checks for violent activities. 

It first allows the user to manually select dots to form a polygon, this will be the region of interest. 
Then it starts human detection with YOLOv7, and check whether their bottom center point of the bounding box is within the polygon. 
If so, the status will be set to warning as it may be a potential intrusion. 

Now, it starts the monitor the magnitudes generated by the Dense Optical Flow to check for potential violent activities. 
Whenever a large magnitude of motion is detected, the motion intensity bar will increase by some value. And when nothing is happening, the motion intensity bar will decrease little by little. 

When the motion intensity crosses the set threshold, the status board indicates that there may be danger occuring. 
The motion intensity increment and slow decrement is for the system to not be susceptible to random large movements. In short, in order for a DANGER warning to be given, the occurence of large magnitude of motion has to appear for consecutive number of frames (just like how it is in a real life crime violent scene) 

Another thing it will check for is the number of person(s) existing when the motion intensity goes above the threshold. This is to prevent a false alarm made by a single person (eg: dancing, exercising) 

Do refer to the demo video for a better understanding!
