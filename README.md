# SportsAI
This program is able to detect joints through the GCP Cloud Vision APIs and then analyzes any sports/exercise video for related injuries. 

You will need a GCP account and a custom bucket with an input video (.mp4 preferably) to run this notebook. The first results provided are that of basic joint annotations:

![Initial Data](JointAnnotations.png)

We can now graph the positions of joints in respect to time:

![Joint Positions](positions.png)

Using the law of cosines, we can then extract the angles between certain joints"

![Joint Angles](angles.png)

To deduce injury risk (jerk, also known as the third derivative of position), we can differentiate using a UnivariateSpline:

![Joint Stress](jointstress.png)

