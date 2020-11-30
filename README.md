# crane_x7_d435

## Description
[CRANE-X7](https://rt-net.jp/products/crane-x7/)の手先にD435をとりつけたURDFです。取り付け位置は[crane_x7_Hardware](https://github.com/rt-net/crane_x7_Hardware/blob/master/Drawing/CRANE-X7_with_RealSenseD435.pdf)に記載されているとおりです。

## Requirements
下記環境で動作確認しています  
* Ubuntu18.04
* ROS Melodic
* [rt-net/crane_x7_ros](https://github.com/rt-net/crane_x7_ros)
* [IntelRealSense/realsense-ros](https://github.com/IntelRealSense/realsense-ros)

## Installation
* [crane_x7_ros](https://github.com/rt-net/crane_x7_ros)をインストールします
* 実機を使う際は[realsense-ros](https://github.com/IntelRealSense/realsense-ros)をインストールします
* 本リポジトリをクローン、ビルドします  
    ```
    $ cd ~/catkin_ws/src
    $ git clone https://github.com/Kuwamai/crane_x7_d435.git
    $ cd ~/catkin_ws && catkin_make
    $ source ~/catkin_ws/devel/setup.bash
    ```

## Usage
* robot_description等に読み込む際、`crane_x7.urdf.xacro`だった箇所を`crane_x7_d435.xacro`に変更して使用してください
* 動作を保証していませんが簡易的に試すことのできるlaunchファイルがあります
    * 実機を動かす際は下記のコマンドを実行します
        ```
        $ roslaunch crane_x7_d435 bringup.launch
        $ roslaunch realsense2_camera rs_camera.launch
        ```
    * シミュレータ(GAZEBO)を起動する際は下記のコマンドを実行します
        ```
        $ roslaunch crane_x7_d435 bringup_sim.launch
        ```

## License
This repository is licensed under the MIT license, see [LICENSE](./LICENSE).
