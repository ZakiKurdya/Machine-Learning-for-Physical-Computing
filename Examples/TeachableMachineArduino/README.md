# Steps:
- [Download](https://www.arduino.cc/en/main/software) Arduino IDE
- [Download](https://github.com/p5-serial/p5.serialcontrol/releases) p5 serial app
- Upload Arduino code to the Arduino board (you can find it in the `SoundClassifier`/ `ImageClassifier` / `PoseClassifier` folder)
- Open p5 serial app (if cannot open, change firewall settings)

## Sound:
- Running this [p5 sketch](https://editor.p5js.org/yining/sketches/eHYnYa5BR) on p5 web editor, remember to update the `portName` and `mySoundModelURL`, and update class names to your own classes.
- [Demo](https://youtu.be/7xPDbbHCjLw)
- [Demo made by Cara Neels](https://vimeo.com/363431151)

## Sound with Servo Motor
- Upload the [Arduino Sketch](https://github.com/yining1023/Machine-Learning-for-Physical-Computing/tree/master/Examples/TeachableMachineArduino/SoundClassifier_with_Servo/SoundClassifier_Servo) to the Arduino board
- Running this [p5 sketch](https://editor.p5js.org/yining/sketches/q8JEPDwK7), remember to update the `portName` and `mySoundModelURL`, and update class names to your own classes.
- [Video Demo](https://youtu.be/RnStPxTfEnU)
- Circuit
  - Connect D2,3,4 to 3 LEDs
  - Connect servo signal pin to D9. [More about](https://github.com/yining1023/Machine-Learning-for-Physical-Computing/tree/master/Examples/ServoMotor) how to use servo motor with arduino.
<img src="../../images/sound_servo.jpg" alt="sound_servo" width="400px">


## Image:
- Running this [p5 sketch](https://editor.p5js.org/yining/sketches/Ob8Zkf_FZ) on p5 web editor, remember to update the `portName` and `myImageModelURL`, and update class names to your own classes.
- [Demo](https://youtu.be/ZGafimlnLw8)
- Circuit
  - Connect Ground to the 2 LEDs Ground pin
  - Connect Pin 2, 3(or 12, 13) to the LED power pin
  An example circuit on Arduino Nano 33 BLE sense:
  <img src="../../images/tmarduino.jpeg" alt="sound_servo" width="400px">


## Pose:
- Running this [p5 sketch](https://editor.p5js.org/yining/sketches/WqhmvWzoo) on p5 web editor, remember to update the `portName` and `poseModelUrl`, and update class names to your own classes.
- [Demo](https://youtu.be/2E0LpbdPjMs)

Trouble shooting:
- The models works in p5 web editor, but my LEDs are not lighted up
  1. Light up LEDs in the arduino code directly to test if there is anything wrong with the LEDs.
  2. Make sure p5 serialis working: There shouldn't be any error in the console. The p5 serial app should be open, but do NOT connect to the port inside of the p5 serial app, otherwise p5 serial app will be using the port, then p5 web editor cannot use the port.
  3. You can find your portname in the p5 serial app. But there is no need to connect to the port in the p5 serial app.
  4. When you are re-uploading Arduino sketch, you need to stop p5 sketch in the editor and close the p5 serial app.
- Cannot download/open p5 serial app
  Cannot open p5 serial app: change the firewall settings, turn the firewall
  Cannot download p5 serial app in Chrome(`p5.serialcontrol.zip is dangerous, so Chrome has blocked it`): try download it in other browers, like Safari, Firefox
  
