# robot_localization
wheel Odometry+IMUによるekfを用いた自己位置補正のノードである

# 使い方
このノードは既存のリポジトリであるが、turtlebot3を用いたodometry+IMUの位置補正のために自分でlaunchを作成する必要があったため、作成した

  ```shell
  $ roslaunch robot_localization robot_localization.launch
  ```
  これを用いれば,topic名で"/fusion/odom"がpublishされるのでこの値が位置補正後のロボット位置である
  
  ※注意
  以下のコマンドをやってみた際に、"odom"と比較すると初期時は、poseとorientationに関しては同等であるが,twistに関してはなぜかうまくいってない...
  今後修正する必要あり？
   ```shell
  $ rostopic echo /fusion/odom
  ```
  
