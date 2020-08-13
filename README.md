# Erebus
Erebus is a rescue simulation competition environment designed for semi-experienced to highly experienced programmers. 

<p align="center"><img src="/docs/images/environment.JPG" width="500"><p/>  

## [Changelog](https://github.com/Shadow149/RescueMaze/blob/master/CHANGELOG.md)

### [Release 4] - 2020-08-05

#### Added
- Robots are now placed into the world by the supervisor
- Export log of events after each game
- Positions of tiles, humans and obstacles randomly generated and automatically calculated based on tile scale
- Added an extra camera on the front of the robot. The cameras are labelled `camera_left` and `camera_right`.
- Start tile changes from green to white when the robots move off it and doesn't change back.

#### Changed
- There is now no need to specify robot type when sending data for estimated victim detection and exit messages.   
For example from `struct.pack('i i i c', data, data1, data2, data3)` to `struct.pack('i i c', data, data1, data2)`
- Thermal victims radius decreased
- Tiles are now much smaller
- Victims are now much smaller
- Increased distance sensor range
- Moved colour camera to a less obstructive position to avoid shadows
- Moved starting tile to within the maze
- Removed automatic object recognition from the camera
- Heated victims are now only a point light. Removed white box.
- Changed robot sensor configuration internally however it shouldn't affect anything.
- Distance sensor values are now linear ranging from 0 to 0.8, with a max range of around 2x tile size.

#### Removed
- Start 'bay' on outside of maze removed
- Robots not in generated world file
- Obstacles are not placed into the map due to smaller tile size

#### Fixed
- Attempting to relocate with no robot no longer causes a crash

## Getting started
[Installation](https://github.com/Shadow149/Erebus/wiki/Installation)  

[Programming a controller](https://github.com/Shadow149/Erebus/wiki/Programming-a-controller)  

## Challenge Week 1
Two worlds are up for [testing](https://github.com/Shadow149/Erebus/releases/tag/v0.1.1-alpha-w1) as part of Challenge Week 1. Upload your scores to the discord if you would like.
