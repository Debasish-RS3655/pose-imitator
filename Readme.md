## Pose Imitator

A program which analyses a person's body-keypoints using [Tensorflow PoseNet](https://www.tensorflow.org/lite/examples/pose_estimation/overview). Euclidean distance between any two keypoints are mapped into an angle (0 to 180 degrees) between a fixed and a movable servo. This is done for all the body keypoints, which are then sent over Serial to a connected robotic body.

## Warning
Pose Estimator is still alpha.

## Credits
The program is primarily based on pose estimation using Tensorflow PoseNet.

## External Circuit

For safety and capacity limitations three Arduinos are used in the external circuit. The program sends the degrees for 13 servos located as in a typical upper body humanoid. The Serial data is sent to an RF transmitter built on Arduino. An RF receiver (built on Arduino) is connected through Serial to another Arduino which controls the servos.

## Platform
Tested on Windows 10 64 bit

## Installation
Requires NodeJS and Arduino IDE installed.
```bash
npm install
```

## Running
Connect the TX Arduino, specify the Serial port in backend.js and then: 
```bash
node backend.js
```

The frontend is available at http://127.0.0.1:4040/file/poseImitatorFrontend.html
