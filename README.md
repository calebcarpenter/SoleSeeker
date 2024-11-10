# SoleSeeker

## Inspiration
Shopping for shoes can be an overwhelming experience. With thousands of shoes claiming to be the best for your feet, it is no wonder that more than two-thirds of people wear misfitting shoes. Thus, we created SoleSeeker, an insole device that detects your specific foot type with a companion app that allows for customized shoe recommendations.  

## What it does
Our project utilizes capacitance to detect the relative force at various areas in the feet when walking. Using the force data collected we compared the pressure at the balls, small toe, arch, lateral edge, and the heel of the feet at different time intervals. These values would serve as data for the app to find weaknesses in the individual’s foot and allow for specialized recommendations based on which support would best fit them. 

## How we built it
Our device is composed of hand-made capacitance sensors which took the place of typical force sensors. Capacitors are essentially parallel plates, one charged and one grounded, that are separated by a dielectric component. The charged plate sends charge towards the grounded plate through the dielectric, which holds onto the charges and allows for a slow discharge. Capacitance in parallel plates varies with the distance between them, and the time it takes to discharge increases as they get closer. We were able to use this principle to detect areas of high pressure by sending a short pulse of energy into the capacitor, then measuring the time it takes to discharge. A higher discharge time indicates a higher capacitance and thus more force on that sensor. We connected five of these sensors to an Arduino Uno, and placed them at different areas of interest around a cardboard insole to measure the distribution of force across the foot.

## Challenges we ran into
One challenge we faced was not having all the necessary hardware available to us. The Arduino Uno was not capable of reading any meaningful data from the 50kg load sensors. If we had access to load cell amps to amplify the force read, it would have been possible to distinguish which force sensor was carrying a higher load. In turn, the Arduino Uno would have been able to provide data that we could use in order to create data for the app’s pressure map and sneaker recommendations.


Additionally, we struggled with finding a dataset that would allow us to train a model due to medical data often being confidential and the specific needs of our project. This lack of a dataset with foot pressure measurements made it difficult to develop a model that could take our data and give shoe recommendations based off of it.

## Accomplishments that we're proud of
We are especially proud of the makeshift force sensors that two members of the team worked on. It was not something that was planned out beforehand, but after speaking with a mentor from the MakerSpace, we decided that it was worth a shot. The end result was not completely functional, as creating a sensor with the materials we were provided proved to be extremely difficult and required a set-up with tools more precise than what was offered, but with more time and better materials we believe that these sensors could provide the intended force data.

## What we learned
We learned to use Figma, which was completely new to all of us. This allowed us to experiment with different approaches regarding the UI/UX of the app. We also explored using flutter and flutterflow to export our figma file into an actual app. There was also the makeshift load sensor, which taught us about the schematics of the original load sensors we were planning on using, as well as how that could be created using provided materials such as tin foil and rubber sheets. 

## What's next for Sole Seeker
An important step is finding a dataset regarding different types of sneakers and what part of the foot they support to train a machine learning model so that the app can return different shoes that the user may benefit from. Currently, our app does not have that capability, so we are just providing five different options depending on which sensor reads the most force. In addition to that, the app would be remodeled so that it returns the most compatible sneaker, as well as the next four options, to create a top-five list. Furthermore, further testing would be required to find the right amount of sensors as well as the best location for these sensors to be. Sensor locations were based on a literature analysis however a precise series of tests using our specific sensor would be ideal. 
