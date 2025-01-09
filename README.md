# Roundabout-Video-Dataset-for-ITS
## Video Links: https://pan.baidu.com/s/15wdjXxt5BXVRke6lBoidLQ Extraction  Code: 12qw 
### Project Overview
  This dataset is designed to advance the development of advanced driver-assistance systems (ADAS) and autonomous vehicles by enabling precise prediction of vehicle turning intentions at roundabouts. Vehicle information, including timestamps, pixel coordinates, and heading angles, is extracted from video data using YOLOv8 for object detection and DeepSORT for multi-target tracking. These data points enhance situational awareness, reducing collision risks and facilitating smoother traffic flow by providing a detailed understanding of dynamic interactions in roundabout environments.
  
  Captured in Wuhan, China, this compilation features videos recorded between 8 a.m. and 6 p.m. in December 2024. It comprises 235 video clips with a total duration of 226.9 minutes, captured from seven viewpoints across two roundabouts. The dataset covers various traffic conditions during peak and off-peak hours, recorded under clear weather conditions in daylight to ensure optimal visibility. High-resolution videos from multiple angles capture diverse traffic scenarios, making it a comprehensive resource for detailed analysis.
  
  The dataset's trajectory data can be used to optimize traffic flow by predicting vehicle paths, speeds, and interactions, allowing for better traffic signal timings and route planning. In ADAS, it supports real-time vehicle tracking, alerting drivers to potential collisions and enhancing safety. Additionally, the dataset aids in detecting abnormal driving behaviors, such as sudden lane changes or harsh braking, enabling timely alerts for both drivers and traffic systems. 

### Data Description
  The dataset provides detailed information on 4,343 labeled vehicles, including precise timestamps marking their appearance in the video frames, pixel coordinates indicating their position within the image, and real-world coordinates derived through monocular ranging. Additionally, heading angles, calculated from adjacent frame coordinates, are included to indicate the vehicle's movement direction. In total, there are 724,615 trajectory records documenting the vehicles' movement over time, with updates for each frame to capture dynamic changes in their positions and movements.
  
  The dataset utilizes the YOLOv8 algorithm integrated with the DeepSORT tracker for object detection and tracking. YOLOv8 quickly identifies traffic entities such as vehicles, pedestrians, and other objects within video frames, while DeepSORT ensures stable multi-target tracking by using ReID features and motion states to maintain the identity of each detected target over time. To convert pixel coordinates into real-world positions, monocular ranging is applied, leveraging key camera parameters like focal length, principal point, and frame size, and constructing an intrinsic matrix via OpenCV. By considering the camera's height, angle, and triangulation geometry, the real-world coordinates of vehicles are accurately calculated. The bottom-center of each detected vehicle's bounding box serves as the target pixel coordinate, with the camera position as the origin, allowing for the precise determination of vehicle positions in real-world coordinates. This process enables the creation of a comprehensive vehicle trajectory dataset for roundabout scenarios.
  
![流程图vvvvv](https://github.com/user-attachments/assets/f2de8a17-fd3a-4d3c-b0db-eb515f823ae0)
### Licensing Information
  This dataset is provided under the MIT license. By using this dataset, you agree to the following terms:

* Usage: You are permitted to use this dataset for [academic/research/commercial] purposes, including but not limited to [list specific use cases, e.g., training machine learning models, developing ADAS systems, etc.].

* Attribution: If you use this dataset in any published work (e.g., papers, presentations), you must provide proper attribution as follows:
"This work uses the "Roundabout-Video-Dataset-for-ITS", which was provided by Ruichun Zhou(周瑞淳). Available at https://github.com/zhoudashi2016/Roundabout-Video-Dataset-for-ITS"

* Redistribution: You may share or redistribute this dataset, but you must do so under the same terms as specified here, and provide appropriate attribution. You may not use the dataset for unlawful or unethical purposes.

* Modifications: You may modify and adapt the dataset for your purposes. However, if you distribute modified versions, you must clearly indicate the changes made and include the same licensing terms.

* No Warranty: The dataset is provided "as-is" without any warranties or guarantees, either express or implied. The creators are not responsible for any damages or losses that may result from its use.

For more detailed licensing terms or inquiries, please contact 302027@whut.edu.cn.

### Acknowledgments
  We would like to sincerely thank Yi Yang(易阳), Wang Yihong(汪毅弘), Su Zhenghao(苏政浩), Zhang Zhiyuan(张志远), Li Zhongzhe(李忠哲), and Liu Yudong(刘玉东)  for their invaluable contributions to the collection of roundabout videos for this dataset. Their efforts have been instrumental in supporting the research and development process.
