name: inverse
layout: true
class: center, middle, inverse
---
# 設計製作論3 知能コース 5班
最終発表計画プレゼン
2020/11/30

<img src="https://user-images.githubusercontent.com/53966390/99927589-30f40500-2d89-11eb-9776-83326d2bec44.png" width="480px">

---
layout:false

## ハンコの認識方法
- 3Dプリントしたハンコのモデルを3つ用意し，上部にそれぞれ赤・青・緑のマーカーをつける．

<img src="https://user-images.githubusercontent.com/53966390/99941288-20578500-2db1-11eb-873f-12765206f6c1.png" width="200px">
<img src="https://user-images.githubusercontent.com/53966390/99941310-28172980-2db1-11eb-82c6-7e293706884f.png" width="200px">
<img src="https://user-images.githubusercontent.com/53966390/99941299-2483a280-2db1-11eb-8bd8-9e2d2b43186e.png" width="200px">

※写真は試作品段階です．

---
## RealSenseの使用方法

- RealSenseでマーカーの色を読み取り，目標の色のマーカーがついたハンコを選び掴む．
    -  ハンコは指定座標に配置し，アームを動かす．
    -  指定座標上でハンコのマーカー色を判別する．
    -  3つのハンコの順番が異なっていても，目標の色のマーカーがついたハンコを掴む．
