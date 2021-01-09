---
title: "SpiderBUG"
excerpt: "BSc and MSc Poject on Mobile Robot Navigation<br/><img src='/images/spider.png'>"
collection: portfolio
---

Both my Bachelor and Master projects focused on this novel local path-finding algorithm called SpiderBUG. It is based on the well-known TangentBug algorithm but allows for moving obstacles. It observes obstacle positions, estimates their speeds and directions and plans paths in a 3D web in space-time. This allows fast switching between high-quality goal-connecting paths in real-time.

_You can find the git project page [here](https://github.com/the-jojo/SpiderBUG)_

## Properties

The defining qualities of this path-planner are its _local_ nature, the emphasis on _smooth_ and _minimal_ paths as well as being able to account for _dynamic_ obstacles. 

* _local_ path-planners do not have access to a global map and have to rely on local sensing information, such as depth-sensors or depth-cameras. 
* paths are _smooth_ when robot motion is continuous at multiple derivatives. Not only are there no sharp corners (where the robot would have to stop, turn, continue), but also no sudden curves. // TODO link continuity wikipedia
* TangentBug paths are proven to be of _minimal_ length since the robot always steers toward obstacle tangent points. Given local sensing information, no shorter paths exist.
* _dynamic_ or moving obstacles are particularly challenging, since movement is not known beforehand and uncertainties upset planned paths, requiring on-the-fly replanning
