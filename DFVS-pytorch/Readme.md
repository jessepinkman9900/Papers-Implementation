#### Summary
* Approaches to Visual Servoing
  * Classical Methods
    * Extract a set of hand crafted features from the images.
    
  * Pose Based Methods
    * Approaches uses these visual features to estimate the camera pose directly in CArtesian space from a given image.
    * Sensitive to camera calibration errors.
    
  * Image Based Methods
    * Uses an image as a reference to the controllers.
    * Also uses handcrafted features.
    * Robust to calibration errors.
    * Direct methods avoid the feature extraction step and operate directly on the image measurements. python3
    * Direct methods avoid the feature extraction step and operate directly on the image measurements.

* Core Idea of Paper
  * No handcrafted features.
  * Integration of depth correspondences with depth estimates allows network to generalise well.
  
* Approach
  * Calculate the flow using FlowNet2.
  * Calculate the depth using a network.
    * Also could be estimated using the flow.
  * Flow and Depth plugged into the interaction matrix.
  * Control law is defined.
  * Flow is the feature error.
  
  * Magnitude of the optical flow difference can be seen as inverted scaled representation of underlying depth. 

* Simulation Benchmark  :
  * Easy
    * More translational motions(1.4m) with small rotations(15 degrees).
  * Medium
    * Translation(1.5m) and Rotation(20 degrees).
  * Hard
    * Huge amount of rotation(>=20 m) and translation(>=30 degrees).



What is dense correspondence?
* Correspondence, namely how pixels in one image correspond to pixels in another image, is a fundamental problem in computer vision.
