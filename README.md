# mypkg
![test](https://github.com/0111-daisuke/mypkg/actions/workflows/test.yml/badge.svg)

# このパッケージについて
これは数字を送信するtalker.pyと受け取ったメッセージを表示するlistener.pyに関するパッケージです.

## 動作手順
ros2上でmypkgをクローンする
```
$ git clone https://github.com/0111-daisuke/mypkg.git
```
ビルドをする
```
$ colcon build
$ source ~/ros2_ws/install/setup.bash
$ source ~/ros2_ws/install/local_setup.bash
$ source ~/.bashrc
$ ros2 pkg list | grep mypkg
$ ros2 pkg list | grep person_msgs
```
端末を2つ開き下記の実行コマンドを入力する

1
```
$ ros2 run mypkg talker
```
2
```
$ ros2 run mypkg listener
[INFO] [1672380076.318295700] [listener]: Listen: 47                       
[INFO] [1672380076.773725600] [listener]: Listen: 48                                                     
[INFO] [1672380077.273496100] [listener]: Listen: 49                                            
[INFO] [1672380077.773575500] [listener]: Listen: 50                                         
[INFO] [1672380078.273591900] [listener]: Listen: 51                                                 
[INFO] [1672380078.772615400] [listener]: Listen: 52                                                        
[INFO] [1672380079.273691200] [listener]: Listen: 53                                                                    
[INFO] [1672380079.773548900] [listener]: Listen: 54                                          
[INFO] [1672380080.273539100] [listener]: Listen: 55                                           
[INFO] [1672380080.773590100] [listener]: Listen: 56 
```

その他、launch/talk_listen.launch.pyを利用して以下のように一つの端末で実行することも可能
```
$ ros2 launch mypkg talk_listen.launch.py
[INFO] [launch]: All log files can be found below /home/daisuke/.ros/log/2022-12-30-15-18-18-815708-DESKTOP-80O9FF0-12077
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [12078]
[INFO] [listener-2]: process started with pid [12080]
[listener-2] [INFO] [1672381099.549987600] [listener]: Listen: 0
[listener-2] [INFO] [1672381100.043506700] [listener]: Listen: 1
[listener-2] [INFO] [1672381100.543237100] [listener]: Listen: 2
[listener-2] [INFO] [1672381101.043337500] [listener]: Listen: 3
[listener-2] [INFO] [1672381101.543357800] [listener]: Listen: 4
[listener-2] [INFO] [1672381102.043345400] [listener]: Listen: 5
[listener-2] [INFO] [1672381102.543442000] [listener]: Listen: 6
[listener-2] [INFO] [1672381103.043370300] [listener]: Listen: 7               
[listener-2] [INFO] [1672381103.543373900] [listener]: Listen: 8                                                        
[listener-2] [INFO] [1672381104.043371700] [listener]: Listen: 9                 
[listener-2] [INFO] [1672381104.543374700] [listener]: Listen: 10            
[listener-2] [INFO] [1672381105.043392600] [listener]: Listen: 11
```
# 作者の使用したソフトウェア
* Python 3.10.6
* ROS2 humbl

# 実行環境
* Ubuntu 22.04.1 LTS

これらはロボットシステム学の授業内で作成したものです.
このソフトウェアパッケージは、３条項BSDライセンスの下、再頒布および使用が許可されます.

©2022 Daisuke Mori
