# rosbag_to_video_cpp

Download the code and put it in catkin_ws src folder. then run catkin_make to compile it

run with 

  roscore

  rosrun ros_bag_to_video_cpp ros_bag_to_video_cpp

then play you bag by

  rosbag play $youbag$


To change your file directory and format , just changes parameter in 


ros::Subscriber sub = nh.subscribe("/raspicam_node/image/compressed", 1, imagecompressedCallback);
 
cv::VideoWriter video_out("out.avi",CV_FOURCC('M','J','P','G'),10, cv::Size(640,480),true);

for new opencv 4 series change the fourcc accordinly.
