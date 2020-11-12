# 5班中間発表
---
## テーマ
 CRANE-X7で捺印をさせる
## 何でこれをやるか・何が面白いか
 デジタル化が進む中ハンコは必要だと河野大臣に反抗するためにハンコを押すロボットを開発する．

---
## 活動方針
 - 10月12日にGitHub Organizationを作成．
 - RT crane_x7_ros リポジトリをForkし，各自ブランチを分けて作業．
 - 木曜日にミーティングを行い，進捗を確認．

---
## 動作
|No.|中間発表の動作|当初の予定動作|
|----|----|----|
|1.|お辞儀をする|指定の座標に置いたハンコまで移動する|
|2.|書類の文章をハンドでなぞって確認する|ハンコを掴む|
|3.|ハンコを選ぶ動作をする|朱肉につける|
|4.|ハンコを掴む|紙に捺印する|
|5.|朱肉をつける||
|6.|朱肉がついたか確認する||
|7.|書類の指定された位置に捺印する||
|8.|雑巾を用いてハンコについた朱肉を落とす||
|9.|ハンコを元の位置に戻す||
|10.|ホームポジションに戻る||

動作のリアルさを追求することや，動作の確実性を求めて活動．

---
### 
- お辞儀する礼儀正しさ　
- 文章をなぞって確認する慎重さ
-   持つものを迷う人間らしさ
-   使った後にハンコを拭き元に戻す几帳面さ

---
## 最終的なタスク表
# 要変更

---
## はんこ

---
## gazebo シミュレーション
  2週目までに実際と同じ環境をgazeboで．．．．．
 # ※ここの写真変更する必要あり
![gazebo](https://user-images.githubusercontent.com/53966271/98534167-65ff5280-22c7-11eb-99b9-e28816c1ab5a.png)

---
## 環境
- ### 実機動作
  - ネイティブ ubuntu18.04
  - CRANE-X7
- ### シミュレーション
  - ubuntu18.04
    - ネイティブ OR Windows Subsystem for Linux(WSL)
  - gazebo

---
## 使用するもの
- ハンコ
- 朱肉
- 紙
- ハンコマット
- 雑巾
- のり
- 消しゴム
- 電池

![image](https://user-images.githubusercontent.com/53966390/98886454-77b74480-24d7-11eb-9144-1a447d2191e7.png)

---
## 実機動作動画（前方カメラ）
[![Watch the video](https://user-images.githubusercontent.com/53966390/98893099-19915e00-24e5-11eb-9425-247b738c1b3d.png)](https://youtu.be/xeJfs4FgBNw)
※画像をクリックするとYoutubeに飛びます．

---
## 実機動作動画（後方カメラ）
[![Watch the video2](https://img.youtube.com/vi/b-fXhM-V2vc/maxresdefault.jpg)](https://youtu.be/b-fXhM-V2vc)
※画像をクリックするとYoutubeに飛びます．

---
## 捺印した書類
![image](https://user-images.githubusercontent.com/53966390/98889012-78060e80-24dc-11eb-8049-21da81ebe235.png)

---
## 久保寺真仁
- モデルを inventor & blender で作成，gazeboに反映
    - modelごとにリポジトリを作成
      - [ハンコ＋補助モデル](https://github.com/RobotDesign3-Team5/asstseal_model)
      - [ハンコ台](https://github.com/RobotDesign3-Team5/storage_model)
      - [朱肉](https://github.com/RobotDesign3-Team5/inkpad_model)
      - [ハンコマット](https://github.com/RobotDesign3-Team5/sealmat_model)
      - [雑巾](https://github.com/RobotDesign3-Team5/TissuePaper_model)
      - [消しゴム](https://github.com/RobotDesign3-Team5/eraser_model)
      - [電池](https://github.com/RobotDesign3-Team5/battery_model)
      - [スティックのり](https://github.com/RobotDesign3-Team5/GlueStick_model)

- ハンコ補助モデルの３Dプリントパーツの作成
  - [ハンコ＋補助モデル 3Dデータ](https://github.com/RobotDesign3-Team5/asstseal_model)
  - [ハンコ台 3Dデータ](https://github.com/RobotDesign3-Team5/storage_model)
  
  ![補助モデル１](https://user-images.githubusercontent.com/53966390/98893993-15fed680-24e7-11eb-913e-333a53b3b8e3.jpg)
  ![補助モデル２](https://user-images.githubusercontent.com/53966390/98893997-17300380-24e7-11eb-9199-25a2cc9a4085.jpg)

- ハンコを朱肉につける動作を追加
- セットアップマニュアル(README)を作成
  -  [セットアップマニュアル](https://github.com/RobotDesign3-Team5/setup_manual)

---
## 朱広樹
- 物品の購入・研修・採寸
	- ハンコ・ハンコマット・朱肉
-	モデル作成
	- スティックのり・消しゴム・電池モデルをInventorで作成
-	ハンコを選び，迷う動作を追加
	-	スティックのり・消しゴム・電池を掴みそうになる動作
---
## 白須和暉
-	ハンコを拭く動作を追加
	-	雑巾に擦りつけ朱肉汚れを落とす．
    [![拭く](https://img.youtube.com/vi/8uCIRfLJ1HA/maxresdefault.jpg)](https://youtu.be/8uCIRfLJ1HA)
    [動作の様子](https://youtu.be/8uCIRfLJ1HA)
- 	アームにお辞儀をさせる動作を追加
	-	前左右の方向に深々とお辞儀する．
    [![お辞儀](https://img.youtube.com/vi/5FEK7ri63Ec/maxresdefault.jpg)](https://youtu.be/5FEK7ri63Ec)
    [動作の様子](https://youtu.be/5FEK7ri63Ec)

---
## 高橋直也
-	書類に目を通す動作を追加
	- 書類の上でアームを左右に動かす．
    [![書類に目を通す](https://img.youtube.com/vi/-X19rAL2V-g/maxresdefault.jpg)](https://youtu.be/-X19rAL2V-g)
    [動作の様子](https://youtu.be/-X19rAL2V-g)

---
## 横尾陸
-   ハンコを押すときのリアルを追求
	- 力を入れて押すのをイメージしてアームを動かしたが、押す部分がずれてしまいきれいに映らなかったため導入しなかった。
    [![グリグリ](https://img.youtube.com/vi/7w3rHCQwpf0/maxresdefault.jpg)](https://youtu.be/7w3rHCQwpf0)
    [動作の様子](https://youtu.be/7w3rHCQwpf0

-   移動経路が毎回異なる問題を解決
	- 経路が違うことで、ハンコの向きが毎回異なりキレイにハンコが押せないという問題があり、srdfでハンコをつかむ前と押す前の姿勢を指定することで解決した。

      ![SRDF](https://user-images.githubusercontent.com/53966390/98891101-d1703c80-24e0-11eb-90f5-d5230ef050fb.png)

      ![PICK1](https://user-images.githubusercontent.com/53966390/98891114-daf9a480-24e0-11eb-934e-b3447273864f.png)

      ![BEFORE](https://user-images.githubusercontent.com/53966390/98891115-dc2ad180-24e0-11eb-8742-0e384b49c550.png)

---
## 今後の課題・反省

  今は座標指定でアームを動かしているのでセンサなどを使いランダムの位置でも実行できるようにする。


