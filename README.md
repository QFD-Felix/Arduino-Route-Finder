# Arduino-Route-Finder
This project was completed during the cmput 274 at University of Alberta. 

The client.cpp was modified to accept coordinates from joystick button presses
and pass them as a request msg to the python server (server.py). The server
acknowledges said request if it is in the right format and parses to pass to
the least_cost_path function to find the optimal path.

The number of waypoints is sent to the client which is acknowledged and then
the waypoints themselves are sent. They are stored in an array of LatLon struct
created. This array is then used to draw the path.

The srv_get_pathlen(start, end) and srv_get_waypoints(waypoints, path_len,
max_path_len) have been modified (to be found in serial_handling.cppto
accept path length and waypoints respectively as well as send acknowledgements.
When tested all of this functionality works and behaves as expected.

In client.cpp file The drawing function is made at the place where "Your Task" 
is showing. With another function called "is_waypoints_visible(x,y)", Arduino
could draw the shortest route way points by way points. The function
"is_waypoints_visible(x,y)" make sure that we would not draw the route that out
of the screen. 

![alt text](https://github.com/QFD-Felix/Arduino-Route-Finder/blob/master/Project%20Pics.JPG)
