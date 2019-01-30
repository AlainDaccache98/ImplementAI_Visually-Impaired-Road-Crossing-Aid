## Inspiration
Of the 37 million people across the globe who are blind, over 15 million are from India. Living in a developing country with little infrastructure for the disabled could be very harsh and isolating. We take this issue at heart, and we want to make a difference to not let their disabilities hinder their day to day life.

## What it does
Our application provides the visually impaired population with an application that helps them navigate the intersections easier. The user can point their phone in front of them and move the phone around them to capture a range of images. The application will then vocally guide them to either rotate left, rotate right, go straight, or wait based on their position (whether there's a zebra crossing, a red light, etc.). For now, we limit the functionality to crossing at intersections.

## How we built it
We used the Google Maps API to locate when the user reaches an intersection to indicate the direction. The user then takes a video of it's surroundings and based on the Google Maps inputs, a field of vision is selected. Then the video is segmented to a few images and the Clarifai API is used to recognize tracks, red/green lights, and a few other features constituting a crossing which then sets a flag on the images having these features. Then using a policy gradient method, a reinforcement learning agent learns to navigate in this environment and sends navigation instructions to the mobile application, which then vocally directs the user in the correct direction at the intersection.

## Challenges we ran into
Datasets - because we didn't have access to a large marked dataset of the appropriate actions to be taken at intersections, we were bound to use a reinforcement learning approach, which provides the necessary tools for a deep-learning algorithm given that our approach over time provides us with the set dataset. Computation - Our phones didn't have enough GPU power to run it in real time. However, perhaps a device could be built to support our implementation. Mathematical challenge: Selecting the right model for the reinforcement learning agent Another small challenge we ran into was to get the camera in the mobile app working (all of us had only limited experience in mobile app development). We finally, got over this hurdle by using the Camera feature in the Expo toolchain.

## Accomplishments that we're proud of
Observing the artificial intelligence component of the project. Gaining insights to navigate, moreover, doing so in an optimal fashion way in a limited timeframe. We are also very proud of finishing major parts of what we aimed to accomplish in this hackathon project.

## What we learned
Building a mobile app from scratch using React-Native. Also, we learnt how to pre-process the data before adding it to the database and train the model. Furthermore, since it was most of our first hackathons, we learnt about the real-life applications of what learnt in class.

## What's next for Visually Impaired Road Crossing Aid
The main task at hand here was navigation, and we achieved it through function approximation using linear features. For our purposes the linear features were enough and worked very well, however one could implement a more sophisticated function approximation mechanism such as deep models. The other issue we would like to improve upon is the computation time so that the computations could be done online and in real time. Also, we could further add functionality to help the visually impaired user "see" other things around them, such as restaurants, fountains, or other places of interests.
