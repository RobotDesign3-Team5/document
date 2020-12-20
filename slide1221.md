# 5班最終発表
---
## テーマ
 CRANE-X7で捺印をさせる
## 何でこれをやるか・何が面白いか
 デジタル化が進む中ハンコは必要だと河野大臣に反抗するためにハンコを押すロボットを開発する．

---
## Realsense
担当：横尾

realsenseを使うためのコードを書いた．(color_detection.cpp)

---
## ノード分割
担当：久保寺・横尾(RealSense)

プログラムの長文化・GitHubでのmargeの際に起こるCONFLICTを防ぎ，プログラム見やすくした．
  - ### メインノード
    - [robotdesign3_team5.py](https://github.com/RobotDesign3-Team5/crane_x7_ros_team5/blob/master/crane_x7_examples/scripts/robotdesign3_team5.py) (**crane_x7_pick_and_place_controller**)

      - Publisher : 動作名(String)を送ることで，各ノードに動きの指示を行う．

      - Subscriber : 各ノードから終了フラグを受け取り，次の動きに移る．
        
      ```.py
      ActionNames = ["Greet", "Artifice", "Check", "Exclusion", "Detect", "PushCheck", "Seal", "Wipe", "Release", "GutsPose"]

      for i in range(len(ActionNames)):
          pub.publish(ActionNames[i])

          FinishFlag = False
          while FinishFlag != True :
              pass
      ```
      ※ノードに指示を出す部分のみ抽出

  - ### サブノード
    |プログラム名|ノード名|動作名|動作内容|動作作成者|
    |---|---|---|---|---|
    |[greet.py](https://github.com/RobotDesign3-Team5/crane_x7_ros_team5/blob/master/crane_x7_examples/scripts/greet.py)|greet|Greet|お辞儀|白須|
    |[artifice.py](https://github.com/RobotDesign3-Team5/crane_x7_ros_team5/blob/master/crane_x7_examples/scripts/artifice.py)|Artifice|Artifice|悪巧み|三渕|
    |[check.py](https://github.com/RobotDesign3-Team5/crane_x7_ros_team5/blob/master/crane_x7_examples/scripts/check.py)|check|Check|書類の確認|高橋|
    |[grab_release.py](https://github.com/RobotDesign3-Team5/crane_x7_ros_team5/blob/master/crane_x7_examples/scripts/grab_release.py)|Grab_Release|Exclusion|ハンコを掃ける|白須|
    |〃|〃|Release|ハンコを戻す|横尾|
    |||Detect|ハンコを認識して掴む|横尾|
    |[push_check.py](https://github.com/RobotDesign3-Team5/crane_x7_ros_team5/blob/master/crane_x7_examples/scripts/push_check.py)|Push_Check|PushCheck|ハンコに朱肉が付いたか確認|久保寺|
    |[seal.py](https://github.com/RobotDesign3-Team5/crane_x7_ros_team5/blob/master/crane_x7_examples/scripts/seal.py)|Seal|Seal|捺印|横尾|
    |[wipe.py](https://github.com/RobotDesign3-Team5/crane_x7_ros_team5/blob/master/crane_x7_examples/scripts/wipe.py)|Wipe|Wipe|拭く|白須|
    |[guts_pose.py](https://github.com/RobotDesign3-Team5/crane_x7_ros_team5/blob/master/crane_x7_examples/scripts/guts_pose.py)|Guts_Pose|GutsPose|ガッツポーズ!?|高橋|

    ※プログラム名(**ノード名**)

  - ### 関数
    - [move_def.py](https://github.com/RobotDesign3-Team5/crane_x7_ros_team5/blob/master/crane_x7_examples/scripts/move_def.py) : **アームやハンドの動きのオリジナル関数をまとめた.**
    各ノードで`from move_def import <関数名>`で呼び出し．
      - `arm_move(x,y,z)` : 指定座標に手先を動かす関数
      - `hand_move(rad)`  : ハンドの角度[rad]を指定し動かす関数
      - `joint_move(joint_value,deg)` : 指定関節の角度[deg]を指定し動かす関数

---
## 実機動作
担当：横尾・久保寺
- ### 使用するもの
  - CRANE-X7
  - RealSense
  - ハンコ
  
    <img src="https://user-images.githubusercontent.com/53966390/102635348-86f47680-4196-11eb-8b9b-be4c5ebab78a.png" width="160px">
    
  - 朱肉
  
    <img src="https://user-images.githubusercontent.com/53966390/102635814-2dd91280-4197-11eb-85d6-72ca9e22fbaa.png" width="160px">

  - ハンコマット
  
    <img src="https://user-images.githubusercontent.com/53966390/102636029-7b557f80-4197-11eb-894d-bb4f4c41b7a2.png" width="160px">
    
  - 雑巾
  
    <img src="https://user-images.githubusercontent.com/53966390/102636044-7f819d00-4197-11eb-9056-ad040ac64587.png" width="160px">
    
  - 紙

- ### 配置
  - 配置図
  <img src="" width="640px">
  
  - 実際の配置の様子
  
    <img src="https://user-images.githubusercontent.com/53966390/102636762-66c5b700-4198-11eb-89b8-87cf2d557c3d.png" width="640px">

- ### 実機動作動画
  [![Watch the video](https://user-images.githubusercontent.com/53966390/102637368-3af70100-4199-11eb-8645-b9c9cabc4b6d.png)](https://youtu.be/jt43LZcb014)
  ※画像をクリックするとYoutubeに飛びます．

---
- ### 捺印した書類
  - **中間発表**
  
    設計製作論3の単位保証同意書に捺印
    
    <img src="https://user-images.githubusercontent.com/53966390/98889012-78060e80-24dc-11eb-8049-21da81ebe235.png" width="640px">
   
  - **最終発表**
  
    小切手に捺印させていただきました！！
    ※UC：UedaCoinの略称

    <img src="https://user-images.githubusercontent.com/53966390/102620860-0c216080-4182-11eb-850f-dfd40e729423.png" width="640px">
  
---
- ### 最終的なタスク・進捗表
  <img src="" width="640px">

---
## 久保寺
- ### パッケージ整備
    - RT CRANE-X7パッケージ [crane_x7_ros](https://github.com/rt-net/crane_x7_ros)を基に，最終発表用パッケージ[crane_x7_ros_team5](https://github.com/RobotDesign3-Team5/crane_x7_ros_team5)を作成，整備．

- ### ノード分け
  - 詳細は上記記載．

- ### gazebo
  - gazeboシミュレーション環境を最終発表仕様に変更．
  
    <img src="" width="320px">
  
  - gazeboモデルをclone/pullを行う[bash](https://github.com/RobotDesign3-Team5/crane_x7_ros_team5/blob/master/gazebo.bash)を作成．

- ### 3Dプリンタパーツ
  [ハンコモデル](https://github.com/RobotDesign3-Team5/colorseal_model)を新たに3個作成．
  
  <img src="https://user-images.githubusercontent.com/53966390/102450774-8961ae00-407a-11eb-8e4c-a9d8131cf15f.png" width="320px">
  <img src="https://user-images.githubusercontent.com/53966390/102450782-8f578f00-407a-11eb-94bf-cd6a9f0c0975.png" width="320px">

- ### [README]()の作成
- ### [捺印書類](https://github.com/RobotDesign3-Team5/document/blob/master/%E5%B0%8F%E5%88%87%E6%89%8B.pdf)の作成

---
## 白須  
- for文を用いてお辞儀や拭く動作のコードを改善
- 使わないはんこを掃ける動作の追加

---
## 高橋
- 歓喜表現（ガッツポーズ）の追加

---
## 横尾
- ### RealSense
  - color_detection.cppでハンコの位置をpublishしdetect_seal.pyでそれをsubscribしハンコの上に移動をする。

- ### [README]()の作成

---
## 三渕
- ロボットがそこにある紙を見つけて悪巧みをする動作の追加
```python
        #紙を見つける
        arm.set_named_target("home")
        arm.go()
        arm_move(0.2 , 0.05, 0.3)
        
        #周囲に誰もいないか確認
        arm.set_named_target("home")
        arm.go()
        
        joint_move(0,-80)
        joint_move(0,160)
        joint_move(0,-160)
```
---
## 