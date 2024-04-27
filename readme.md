# Fast Global Registration

### Windows

Configure VS2019+PCL1.11.1 as follows：

First，proceed as https://blog.csdn.net/Wxy971122/article/details/117018767

Second，use the FGR directory "...\FastGlobalRegistration-master\source\External\flann" instead of the pcl installation directory “...\PCL 1.11.1\3rdParty\FLANN\include\flann
...\PCL 1.11.1\3rdParty\FLANN\include\flann”

Third，at "...\External\flann\algorithms\dist.h"， in front of line 520-522
“HammingLUT lut;
 result = lut(reinterpret_cast<const unsigned char*>(a),
             reinterpret_cast<const unsigned char*>(b), size * sizeof(pop_t)); ”，
add “typedef unsigned long long pop_t;”
