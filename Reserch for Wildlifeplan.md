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

**Ai research summery** 

Find research papers about computer vision motion detection while the camera is moving

Detecting independently moving objects from a moving camera—commonly referred to as Moving Object Detection (MOD)—requires isolating object dynamics from background shifts caused by camera egomotion.

**Global Motion Compensation & Motion Cues**

* **Hybrid Motion Compensation & Local Fusion:** Recent frameworks combine global motion compensation with dense optical flow to address dynamic scenes and unconstrained camera movement (Chen et al., 2024). Fusing local spatial information with compensated global motion suppresses background interference while maintaining precise foreground boundaries.  
* **Background Orientation Field Reconstruction:** Optical flow orientation in background regions remains continuous and independent of scene depth. Poisson fusion can reconstruct background orientation fields from optical flow gradients, allowing algorithms to generate motion saliency maps that reveal moving objects without requiring explicit scene depth estimation (Zhang et al., 2020).

**Geometric Constraints & Sensor Fusion**

* **IMU-Assisted Epipolar Geometry:** Integrating hardware sensors like Inertial Measurement Units (IMUs) with vision algorithms yields an accurate initial fundamental matrix for motion compensation (Jung et al., 2019). Point correspondences across consecutive frames are categorized as foreground or background based on their distance from estimated epipolar lines, improving target detection under sudden camera motion.  
* **Multi-View Geometry & Trifocal Tensors:** Incorporating multi-frame geometric constraints—such as plane-plus-parallax representations, fundamental matrices, and trifocal tensors—allows systems to enforce temporal rigidity constraints and segment moving objects across dynamic urban scenes (ter Haar et al., 2010).

**References**

Chen, Z., Zhao, R., Guo, X., Xie, J., & Han, X. (2024). Moving Object Detection in Freely Moving Camera via Global Motion Compensation and Local Spatial Information Fusion. *Sensors*, *24*(9), 2859\. [https://doi.org/10.3390/s24092859](https://doi.org/10.3390/s24092859) Cited by: 5

Jung, S., Cho, Y., Kim, D., & Chang, M. (2019). Moving Object Detection from Moving Camera Image Sequences Using an Inertial Measurement Unit Sensor. *Applied Sciences*, *10*(1), 268\. [https://doi.org/10.3390/app10010268](https://doi.org/10.3390/app10010268) Cited by: 26

ter Haar, F. B., den Hollander, R. J. M., & Dijk, J. (2010). Detection of moving objects from a moving platform in urban scenes. *SPIE Proceedings*, *7701*, 770105\. [https://doi.org/10.1117/12.848034](https://doi.org/10.1117/12.848034) Cited by: 2

Zhang, W., Sun, X., & Yu, Q. (2020). Moving Object Detection under a Moving Camera via Background Orientation Reconstruction. *Sensors*, *20*(11), 3103\. [https://doi.org/10.3390/s20113103](https://doi.org/10.3390/s20113103) Cited by: 18

