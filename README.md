# simple_arm_moveit_demo
6自由度持つロボットアームのurdfを使ってmoveit2のデモを行うパッケージ
この記事はzennの[Moveit2を使ってロボットアームを制御するまで (3)](https://zenn.dev/robohase01/articles/ae66de3b4b6c19)に対応しています。
# 環境
- OS: Ubuntu 22.04
- ROS: ROS 2 Humble Hawksbill
# インストール
```bash
source /opt/ros/humble/setup.bash
rosdep update
cd ~/

git clone https://github.com/Nexis-R/simple_arm_moveit_demo
cd ~/simple_arm_moveit_demo
rosdep install -r -y -i --from-paths .
```
# ビルド
```bash
cd ~/simple_arm_moveit_demo
colcon build --symlink-install
source install/setup.bash
```
# 実行
```bash
ros2 launch simple_arm_moveit_config demo.launch.py
```