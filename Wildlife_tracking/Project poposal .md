New idea work solely on the wild life tracking tech tracking, The main way I can market this is by making a more efficient model 

**DATA GAP**

Most of the papers that I read talk about accuracy not power consumption or use powerful compute on separate discrete systems not on a self contained system on the drone itself (why? Because doing it on the drone is retarded because lack of compute and also battery drain) Also they have pictures of louse folage and I want to 

This will mostly just deal with optimization, and making the map   
**BIG problem**

For a drone use of this we need to overcome natural motion like trees and wind

**Implementation idea.**

Do a form of background substitution on the image then isolate movement that is not ‘inline’ with the other movement aka according to wind and stuff. Then send only the area counted by the on board model as not inline, plus some extra pixels for buffer near the area, to the detection algorithm on a discrete system, and all of those sent data packets are logged and labeled with either the systems guess at what is on it’s confidence of accuracy then the time and location, or if its not confident it detects anything it just labels it as unknown and logs time and location of unknown. These will all later or at logging time be put on a map

**Plan.**

Make math model to make the motion mask specifically to overlay a fucer image on a past one and see the difference between them 

Train learning model to identify said not inline motion 

Then test on a discrete jetson or some sort of tensor unit/ neural processor.

Make a FPV drone

How to get into FPV drones \-  
[https://www.youtube.com/watch?v=Xs\_P7T9G49o](https://www.youtube.com/watch?v=Xs_P7T9G49o) 

