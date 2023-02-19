## Inspiration
I love purchasing products online. The trade off is that my packages take forever to arrive due to delays such as traffic jams. For a supply chain, traffic jams aren’t just affecting their timeline — they can negatively affect their entire business and even end up costing extra money. Google Maps is convenient with tracking traffic, but there are some caveats. One guy tricked Google Maps by pulling a wagon full of phones, thus creating a traffic jam. 
You can watch the video here: https://www.youtube.com/watch?v=k5eL_al_m7Q&t=1s

## What it does
Recon is an application that is designed to be installed into the cameras of traffic or street lights. By comparing the sizes of bounding boxes and the number of vehicles moving away, it can evaluate traffic. If the traffic is busy, vehicles will close to each other, causing the bounding boxes to be drawn larger and have a greater width and height.

## How I built it
I build it with Python code using the OpenCV library to detect and count vehicles passing a certain line and tested it with a pre-recorded video file. The code reads each frame from the video stream, converts it to grayscale and applies a Gaussian blur to reduce noise. It uses the findContours function to identify and extract the contours of the objects in the binary image. For each contour that satisfies certain criteria (minimum width and height), the code draws a bounding box around it and computes its center. For each point in the list, the code checks if it is close enough to the counting line (within a certain offset). If so, it increments a counter. If the bounding box is detected to be large in comparison to the counter, Twilio will send an SMS notification to the truck driving of the traffic. This way, our workers can avoid traffic and deliver packages with little delay.

## Challenges I ran into
One challenge that I ran into was trying to create a real-life application without hardware. I had to use pre-recorded traffic feed in order to mimic the function of Recon.

## What I learned
This was my first time using machine learning, Python, and Twilio. I learned how to hook up a notification system using Twilio and also how to use the OpenCV library.

## What's next for Recon
I hope the hardware aspect of Recon can be built. I do not have any knowledge of microchips or mechatronics, but I am excited to learn.
