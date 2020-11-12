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
    - [久保寺 : masato](https://github.com/RobotDesign3-Team5/crane_x7_ros/tree/masato)
    - [朱 : shu](https://github.com/RobotDesign3-Team5/crane_x7_ros/tree/shu)
    - [白須 : kazuki_robo3](https://github.com/RobotDesign3-Team5/crane_x7_ros/tree/kazuki_robo3)
    - [高橋 : naoya](https://github.com/RobotDesign3-Team5/crane_x7_ros/tree/naoya)
    - [横尾 : rikuyokoo](https://github.com/RobotDesign3-Team5/crane_x7_ros/tree/rikuyokoo)

    - [実機調整用ブランチ : dev](https://github.com/RobotDesign3-Team5/crane_x7_ros/tree/dev)
    - [master](https://github.com/RobotDesign3-Team5/crane_x7_ros/tree/master)
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
- お辞儀する礼儀正しさ　
- 文章をなぞって確認する慎重さ
- 持つものを迷う人間らしさ
- 朱肉がついたかを確認する几帳面さ
- 使った後にハンコを拭き元に戻すきれい好き

---
## 最終的なタスク・進捗表
  <img src="https://user-images.githubusercontent.com/53966390/98914660-4442dd00-250c-11eb-80bc-f432447c7950.png" width="640px">

---
## はんこを確実に持つために
  直径10mm円柱のハンコをCRANE-X7で持つには限界があり，補助パーツを作成し確実につかめるように改良しました．
- ### 初期バージョン(10/20)
  <img src="https://user-images.githubusercontent.com/53966390/98897015-bce67100-24ed-11eb-9c73-90998d6492cb.png" width="320px">

  [![初期モデルの動作](https://img.youtube.com/vi/Y_glLZigQeE/maxresdefault.jpg)](https://youtu.be/Y_glLZigQeE)
  [動作の様子](https://youtu.be/Y_glLZigQeE)

- ### 中間発表バージョン
  <img src="https://user-images.githubusercontent.com/53966390/98893993-15fed680-24e7-11eb-913e-333a53b3b8e3.jpg" width="320px">
  <img src="https://user-images.githubusercontent.com/53966390/98893997-17300380-24e7-11eb-9199-25a2cc9a4085.jpg" width="320px">

---
## gazebo シミュレーション
gazebo上に実際と同じ形のモデルを作成することで，シミュレーションを容易に行えるようにした．
  <img src="https://user-images.githubusercontent.com/53966390/98899884-e30f0f80-24f3-11eb-924f-7da3aa69754d.png" width="320px">

  -  [5班 gazeboセットアップマニュアル](https://github.com/RobotDesign3-Team5/setup_manual#gazebo%E3%82%92%E4%BD%BF%E7%94%A8%E3%81%99%E3%82%8B%E5%A0%B4%E5%90%88)

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

<img src="https://user-images.githubusercontent.com/53966390/98886454-77b74480-24d7-11eb-9144-1a447d2191e7.png" width="640px">

## 配置
<img src="https://user-images.githubusercontent.com/53966271/98900657-90ceee00-24f5-11eb-842a-0d17a6daa277.jpg" width="640px">

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
<img src="https://user-images.githubusercontent.com/53966390/98889012-78060e80-24dc-11eb-8049-21da81ebe235.png" width="640px">
  
---
## 久保寺真仁
- ### モデルを inventor & blender で作成，gazeboに反映
    - modelごとにリポジトリを作成
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

      - モデルinventor設計は主に**朱広樹**が担当
      
        - [消しゴム](https://github.com/RobotDesign3-Team5/eraser_model)
        - [電池](https://github.com/RobotDesign3-Team5/battery_model)
        - [スティックのり](https://github.com/RobotDesign3-Team5/GlueStick_model)

      <img src="https://user-images.githubusercontent.com/53966390/98899884-e30f0f80-24f3-11eb-924f-7da3aa69754d.png" width="640px">

- ### ハンコ補助モデルの３Dプリントパーツの作成
    <img src="https://user-images.githubusercontent.com/53966390/98897896-bbb64380-24ef-11eb-9a95-c6d6a5ef4a4b.jpg" width="320px">

    <img src="https://user-images.githubusercontent.com/53966390/98897898-bce77080-24ef-11eb-8e18-c336e494b526.jpg" width="320px">

- ### ハンコを朱肉につける動作を追加
  [![拭く](https://img.youtube.com/vi/CECq17Bn3L4/maxresdefault.jpg)](https://youtu.be/CECq17Bn3L4)
  ※画像をクリックするとYoutubeに飛びます．
- ### セットアップマニュアル(README)を作成
  -  [セットアップマニュアル](https://github.com/RobotDesign3-Team5/setup_manual)

---
## 朱広樹
- ### 物品の購入・研修・採寸
	- ハンコ・ハンコマット・朱肉
-	### モデル作成
	- スティックのり・消しゴム・電池モデルをInventorで作成
  
      <img src="https://user-images.githubusercontent.com/53966390/98897377-9e34aa00-24ee-11eb-9d2e-8dc23c2430b9.png" width="320px">

      <img src="https://user-images.githubusercontent.com/53966390/98897378-9e34aa00-24ee-11eb-8533-5c8a92231288.png" width="320px">

      <img src="https://user-images.githubusercontent.com/53966390/98897373-9d037d00-24ee-11eb-96a3-888be10ec1c4.png" width="320px">

-	### ハンコを選び，迷う動作を追加
	-	スティックのり・消しゴム・電池を掴みそうになる動作
      [![ハンコ選び](https://img.youtube.com/vi/fH9kEs87PPY/maxresdefault.jpg)](https://youtu.be/fH9kEs87PPY)
      ※画像をクリックするとYoutubeに飛びます．

---
## 白須和暉
-	### ハンコを拭く動作を追加
	-	雑巾に擦りつけ朱肉汚れを落とす．
    [![拭く](https://img.youtube.com/vi/8uCIRfLJ1HA/maxresdefault.jpg)](https://youtu.be/8uCIRfLJ1HA)
    ※画像をクリックするとYoutubeに飛びます．

- ### アームにお辞儀をさせる動作を追加
	-	前左右の方向に深々とお辞儀する．
    [![お辞儀](https://img.youtube.com/vi/5FEK7ri63Ec/maxresdefault.jpg)](https://youtu.be/5FEK7ri63Ec)
    ※画像をクリックするとYoutubeに飛びます．

---
## 高橋直也
-	### 書類に目を通す動作を追加
	- 書類の上でアームを左右に動かす．
    [![書類に目を通す](https://img.youtube.com/vi/-X19rAL2V-g/maxresdefault.jpg)](https://youtu.be/-X19rAL2V-g)
    ※画像をクリックするとYoutubeに飛びます．

---
## 横尾陸
- ### ハンコを押すときのリアルを追求
	- 力を入れて押すのをイメージしてアームを動かしたが、押す部分がずれてしまいきれいに映らなかったため導入しなかった。
    [![グリグリ](https://img.youtube.com/vi/7w3rHCQwpf0/maxresdefault.jpg)](https://youtu.be/7w3rHCQwpf0)
    ※画像をクリックするとYoutubeに飛びます．

- ### 移動経路が毎回異なる問題を解決
	- 経路が違うことで、ハンコの向きが毎回異なりキレイにハンコが押せないという問題があり、srdfでハンコをつかむ前と押す前の姿勢を指定することで解決した。

      <img src="https://user-images.githubusercontent.com/53966390/98891101-d1703c80-24e0-11eb-90f5-d5230ef050fb.png" width="640px">

      <img src="https://user-images.githubusercontent.com/53966390/98891114-daf9a480-24e0-11eb-934e-b3447273864f.png" width="320px">

      <img src="https://user-images.githubusercontent.com/53966390/98891115-dc2ad180-24e0-11eb-8742-0e384b49c550.png" width="320px">

- ### セットアップマニュアル(README)を作成

---
## 今後の課題・反省

  今は座標指定でアームを動かしているのでセンサなどを使いランダムの位置でも実行できるようにする。