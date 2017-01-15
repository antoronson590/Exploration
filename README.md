# Exploration
Tasks:
1. A mobile robot model available from V-REP is modified for position mapping based on the wheel sensor data.
1.1 General equation needs to be framed that can calculate the current position from the parameters: angular velocity of the wheel, time of movement, wheel data extracted from CAD model.
1.2 The data is initially validated throuh the current position extraction possiblity of V-REP.
2. The robot is allowed to navigate in the cluttered environment to study the possible free space accessible.
2.1 The robot is fitted with a proximity sensor to study the nearby objects.
2.2 When the sensor output is negative, the corresponding position is marked as path(green) in the graph.
2.3 When the sensor output is positive, the corresponding position is marked as block(red) in the graph.
2.4 Thus during the progress of time, we can study the entire room through odometric datas.
3. The path planning script is integrated to the software to to plan a 2D path for the mobile robot from start to end position.
3.1 The details of 2D path planning script can be found in Path-Planning thread
3.2 This script can be coupled with the V-REP and mobile robot simulation through plugin using Visual C++.
3.3 Thus given the start and end position, V-REP accelerates the mobile robot from start to end position
4. The next step is developing a dynamic loading where the robot reshuffles the path based on sudden block in its calculated path.
4.1 Solid blocks are made to fall on the path, thus successfully blocking the path.
4.2 Now using vision and proximity sensor, when a block is identified, our mobot choose to block the respective position of block determined as collision.
4.3 Now from the current position, our mobot calculates path to next control point( if next control point is still blocked i.e. in search of next control point, if mobot roams for a longer time, the successive control point is chosen..
4.4 Thus the aim of mobot is to return to its original track. This avoids confusion and saves memory.

Note: To run the simulation model, non limited educational version of V-Rep software from Coppelia Robotics is required. The download executable can be found at http://www.coppeliarobotics.com/downloads.html
