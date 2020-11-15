# 5班中間発表
---
## テーマ
 CRANE-X7で捺印をさせる
## 何でこれをやるか・何が面白いか
 デジタル化が進む中ハンコは必要だと河野大臣に反抗するためにハンコを押すロボットを開発する．

---
## 計画・活動・進捗
- ### 当初の計画と実際の進捗の比較
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

- ### リアル・面白さを追求
  ただ捺印するのでは面白くない...ため，以下の要素を追加した．
  - お辞儀する礼儀正しさ　
  - 文章をなぞって確認する慎重さ
  - 持つものを迷う人間らしさ
  - 朱肉がついたかを確認する几帳面さ
  - 使った後にハンコを拭き元に戻すきれい好き

- ### 作業
  - CRANE-X7
    [RT crane_x7_ros リポジトリ](https://github.com/rt-net/crane_x7_ros)をForkし，各自ブランチを分けて作業
    |名前|ブランチ|
    |----|----|
    |master|[master](https://github.com/RobotDesign3-Team5/crane_x7_ros/tree/master)|
    |実機調整用|[dev](https://github.com/RobotDesign3-Team5/crane_x7_ros/tree/dev)|
    |久保寺|[masato](https://github.com/RobotDesign3-Team5/crane_x7_ros/tree/masato)|
    |朱|[shu](https://github.com/RobotDesign3-Team5/crane_x7_ros/tree/shu)|
    |白須|[kazuki_robo3](https://github.com/RobotDesign3-Team5/crane_x7_ros/tree/kazuki_robo3)|
    |高橋|[naoya](https://github.com/RobotDesign3-Team5/crane_x7_ros/tree/naoya)|
    |横尾|[rikuyokoo](https://github.com/RobotDesign3-Team5/crane_x7_ros/tree/rikuyokoo)|

  - 月曜日・木曜日にdiscordで作業進捗の確認・タスクの振り分けを行った．

- ### 最終的なタスク・進捗表
  <img src="https://user-images.githubusercontent.com/53966390/99192445-3e702480-27b6-11eb-8a06-aa3df815000c.png" width="640px">

---
## はんこを確実に持つために
  直径10mm円柱のハンコをCRANE-X7で持つには限界があり，補助パーツを作成し確実につかめるように改良しました．
- ### 初期バージョン(10/20時点)
  <img src="https://user-images.githubusercontent.com/53966390/98897015-bce67100-24ed-11eb-9c73-90998d6492cb.png" width="320px">

  [![初期モデルの動作](https://img.youtube.com/vi/Y_glLZigQeE/maxresdefault.jpg)](https://youtu.be/Y_glLZigQeE)
  ※画像をクリックするとYoutubeに飛びます．

- ### 中間発表バージョン
  滑り止めに輪ゴムを巻いた．

  <img src="https://user-images.githubusercontent.com/53966390/98893993-15fed680-24e7-11eb-913e-333a53b3b8e3.jpg" width="320px">
  <img src="https://user-images.githubusercontent.com/53966390/98893997-17300380-24e7-11eb-9199-25a2cc9a4085.jpg" width="320px">

---
## gazebo シミュレーション
- ### 現実とできるだけ同じ環境を
  gazebo上に実際と同じ外形・質量のモデルを作成．

  [![gazeboシミュレーション](https://img.youtube.com/vi/7QZ74cGi8V4/maxresdefault.jpg)](https://youtu.be/7QZ74cGi8V4)
  ※画像をクリックするとYoutubeに飛びます．

- ### マニュアル
  [gazeboセットアップマニュアル](https://github.com/RobotDesign3-Team5/setup_manual#gazebo%E3%82%92%E4%BD%BF%E7%94%A8%E3%81%99%E3%82%8B%E5%A0%B4%E5%90%88)

---
## 実機動作
- ### 使用するもの
  - ハンコ
  - 朱肉
  - 紙(同意書)
  - ハンコマット
  - 雑巾
  - のり
  - 富士山消しゴム
  - 電池

  <img src="https://user-images.githubusercontent.com/53966390/98886454-77b74480-24d7-11eb-9144-1a447d2191e7.png" width="640px">

- ### 配置図
  <img src="https://user-images.githubusercontent.com/53966271/98900657-90ceee00-24f5-11eb-842a-0d17a6daa277.jpg" width="640px">

- ### 実機動作動画
  - #### 前方カメラ
    [![Watch the video](https://user-images.githubusercontent.com/53966390/98893099-19915e00-24e5-11eb-9425-247b738c1b3d.png)](https://youtu.be/xeJfs4FgBNw)
    ※画像をクリックするとYoutubeに飛びます．

  - ####  後方カメラ
    [![Watch the video2](https://img.youtube.com/vi/b-fXhM-V2vc/maxresdefault.jpg)](https://youtu.be/b-fXhM-V2vc)
    ※画像をクリックするとYoutubeに飛びます．

- ### 捺印した書類
  <img src="https://user-images.githubusercontent.com/53966390/98889012-78060e80-24dc-11eb-8049-21da81ebe235.png" width="640px">

- ### マニュアル
  [実機動作マニュアル](https://github.com/RobotDesign3-Team5/setup_manual#%E5%AE%9F%E6%A9%9F%E3%82%92%E4%BD%BF%E3%81%86%E5%A0%B4%E5%90%88)


---
## 久保寺
- ### 基となるプログラムの作成
  - ハンコを掴み，朱肉につけ，捺印する動作の作成
  - 関数の作成

- ### gazeboモデルの作成
  モデルを inventor & blender で作成，config・sdfを作成しgazeboに反映，リポジトリ化
    - [ハンコ＋補助モデル](https://github.com/RobotDesign3-Team5/asstseal_model)

        <img src="https://user-images.githubusercontent.com/53966390/98900675-988e9280-24f5-11eb-9e70-8b6100c64a77.jpg" width="320px">
        <img src="https://user-images.githubusercontent.com/53966390/98900678-99272900-24f5-11eb-96c8-c785c0fa6082.jpg" width="320px">

    - [ハンコ台](https://github.com/RobotDesign3-Team5/storage_model)

        <img src="https://user-images.githubusercontent.com/53966390/98900668-96c4cf00-24f5-11eb-8b81-0fe8388586a7.jpg" width="320px">

    - [朱肉](https://github.com/RobotDesign3-Team5/inkpad_model)

        <img src="https://user-images.githubusercontent.com/53966390/98900671-97f5fc00-24f5-11eb-95a0-b5781d9777db.jpg" width="320px">

    - [ハンコマット](https://github.com/RobotDesign3-Team5/sealmat_model)

        <img src="https://user-images.githubusercontent.com/53966390/98900670-97f5fc00-24f5-11eb-8ccf-9839927e9fd1.jpg" width="320px">

    - [雑巾](https://github.com/RobotDesign3-Team5/TissuePaper_model)

        <img src="https://user-images.githubusercontent.com/53966390/98900677-988e9280-24f5-11eb-8647-7b0109d05435.jpg" width="320px">

    - 下記のモデルinventor設計は主に**朱広樹**が担当し，リポジトリ化を行った．
    
      - [消しゴム](https://github.com/RobotDesign3-Team5/eraser_model)
      - [電池](https://github.com/RobotDesign3-Team5/battery_model)
      - [スティックのり](https://github.com/RobotDesign3-Team5/GlueStick_model)

      <img src="https://user-images.githubusercontent.com/53966390/99193064-d4597e80-27b9-11eb-84df-2da3eb9a9b98.png" width="640px">
 

- ### ハンコ補助モデルの３Dプリントパーツの作成
    <img src="https://user-images.githubusercontent.com/53966390/98897896-bbb64380-24ef-11eb-9a95-c6d6a5ef4a4b.jpg" width="320px">

    <img src="https://user-images.githubusercontent.com/53966390/98897898-bce77080-24ef-11eb-8e18-c336e494b526.jpg" width="320px">

- ### ハンコを朱肉につける動作を追加
  [![拭く](https://img.youtube.com/vi/CECq17Bn3L4/maxresdefault.jpg)](https://youtu.be/CECq17Bn3L4)
  ※画像をクリックするとYoutubeに飛びます．

  ![image](https://user-images.githubusercontent.com/53966390/98916783-ee236900-250e-11eb-81d6-cd313a33d9f2.png)
- ### セットアップマニュアル(README)を作成
  -  [セットアップマニュアル](https://github.com/RobotDesign3-Team5/setup_manual)

---
## 朱
- ### 物品の購入・研修・採寸
	- ハンコ・ハンコマット・朱肉の購入，研修，採寸を行った．
-	### gazeboモデルの作成
    inventorでモデルを作成した．

    - スティックのり
    <img src="https://user-images.githubusercontent.com/53966390/99193306-7ded3f80-27bb-11eb-8427-b42d823f35fc.png" width="320px">

    - 消しゴム
    <img src="https://user-images.githubusercontent.com/53966390/99193302-7c237c00-27bb-11eb-8dd6-60ff91708fcb.png" width="320px">

    - 電池
    <img src="https://user-images.githubusercontent.com/53966390/99193305-7d54a900-27bb-11eb-91aa-d076194d8d56.png" width="320px">

-	### ハンコを選び，迷う動作を追加
	-	スティックのり・消しゴム・電池を掴みそうになる動作
      [![ハンコ選び](https://img.youtube.com/vi/fH9kEs87PPY/maxresdefault.jpg)](https://youtu.be/fH9kEs87PPY)
      ※画像をクリックするとYoutubeに飛びます．

      ![image](https://user-images.githubusercontent.com/53966390/98916291-59207000-250e-11eb-9548-71232c884ea7.png)

---
## 白須
- ### アームにお辞儀をさせる動作を追加
	-	前左右の方向に深々とお辞儀する．
    [![お辞儀](https://img.youtube.com/vi/5FEK7ri63Ec/maxresdefault.jpg)](https://youtu.be/5FEK7ri63Ec)
    ※画像をクリックするとYoutubeに飛びます．

    ![image](https://user-images.githubusercontent.com/53966390/98916408-7d7c4c80-250e-11eb-8509-656f195f815c.png)

-	### ハンコを拭く動作を追加
	-	雑巾に擦りつけ朱肉汚れを落とす．
    [![拭く](https://img.youtube.com/vi/8uCIRfLJ1HA/maxresdefault.jpg)](https://youtu.be/8uCIRfLJ1HA)
    ※画像をクリックするとYoutubeに飛びます．

    ![image](https://user-images.githubusercontent.com/53966390/98916510-9a188480-250e-11eb-8c6c-ae675615a52b.png)

---
## 高橋
-	### 書類に目を通す動作を追加
	- 書類の上でアームを左右に動かす．
    [![書類に目を通す](https://img.youtube.com/vi/-X19rAL2V-g/maxresdefault.jpg)](https://youtu.be/-X19rAL2V-g)
    ※画像をクリックするとYoutubeに飛びます．

    ![image](https://user-images.githubusercontent.com/53966390/98916202-34c49380-250e-11eb-9cca-03c7ddaa7809.png)


---
## 横尾
- ### 基となるプログラムの作成
  - ハンコを掴み，朱肉につけ，捺印する動作の作成
  - 関数の作成

- ### ハンコを押すときのリアルを追求
	- 力を入れて押すのをイメージしてアームを動かしたが、押す部分がずれてしまいきれいに映らなかったため導入しなかった。
    [![グリグリ](https://img.youtube.com/vi/7w3rHCQwpf0/maxresdefault.jpg)](https://youtu.be/7w3rHCQwpf0)
    ※画像をクリックするとYoutubeに飛びます．
    
    ![image](https://user-images.githubusercontent.com/53966390/98916671-c8965f80-250e-11eb-9e4c-69f21f92c725.png)

- ### 移動経路が毎回異なる問題を解決
	- 経路が違うことで、ハンコの向きが毎回異なりキレイにハンコが押せないという問題があり、srdfでハンコをつかむ前と押す前の姿勢を指定することで解決した。

      <img src="https://user-images.githubusercontent.com/53966390/98891101-d1703c80-24e0-11eb-90f5-d5230ef050fb.png" width="640px">

      <img src="https://user-images.githubusercontent.com/53966390/98891114-daf9a480-24e0-11eb-934e-b3447273864f.png" width="320px">

      <img src="https://user-images.githubusercontent.com/53966390/98891115-dc2ad180-24e0-11eb-8742-0e384b49c550.png" width="320px">

- ### セットアップマニュアル(README)を作成
  -  [セットアップマニュアル](https://github.com/RobotDesign3-Team5/setup_manual)
---
## 今後の課題・反省

  今は座標指定でアームを動かしているのでセンサなどを使いランダムの位置でも実行できるようにする。
