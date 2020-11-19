# [robotcar_msgs](../README.md)/RelativeVelocityMessage #

## File: robotcar_msgs/Accelerometer.msg
## Raw Message Definition

Header header  \# timestamp in the header is the time the ranger  
               \# returned the distance reading  
  
\# Radiation type enums  
\# If you want a value added to this list, send an email to the ros-users list  
uint8 ULTRASOUND=0  
uint8 INFRARED=1  
  
uint8 radiation_type    \# the type of radiation used by the sensor  
                        \# (sound, IR, etc) [enum]  
  
float32 field_of_view   \# the size of the arc that the distance reading is  
                        \# valid for [rad]  
                        \# the object causing the range reading may have  
                        \# been anywhere within -field_of_view/2 and  
                        \# field_of_view/2 at the measured range.  
                        \# 0 angle corresponds to the x-axis of the sensor.  
  
float32 relative_velocity   \# range data [m]  
                            \# (Note: values < range_min or > range_max  
                            \# should be discarded)  
                            \# Fixed distance rangers only output -Inf or +Inf.  
                            \# -Inf represents a detection within fixed distance.  
                            \# (Detection too close to the sensor to quantify)  
                            \# +Inf represents no detection within the fixed distance.  
                            \# (Object out of range)  
  

## Compact Message Definition

[std_msgs/Header](http://docs.ros.org/en/melodic/api/std_msgs/html/msg/Header.html) header  
  
std_msgs/uint8 ULTRASOUND=0  
std_msgs/uint8 INFRARED=1  
  
[std_msgs/uint8](http://docs.ros.org/en/melodic/api/std_msgs/html/msg/UInt8.html) radiation_type  
[std_msgs/float32](http://docs.ros.org/en/melodic/api/std_msgs/html/msg/Float32.html) field_of_view  
[std_msgs/float32](http://docs.ros.org/en/melodic/api/std_msgs/html/msg/Float32.html) relative_velocity  
