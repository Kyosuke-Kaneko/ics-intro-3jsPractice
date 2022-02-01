# ジオメトリとは
形状（ジオメトリとも言います）を指定することで「球体」や「直方体」、「平面」などさまざまな3Dのオブジェクトを表示できます。

Three.jsで扱える基本的な形状として、いくつか用意されています。代表的なものを紹介します。

- 平面
- 球体
- 直方体
- 三角錐
- 円柱
- 円錐
- ドーナツ形状

## 球体
半径<br>
radius — sphere radius. Default is 1.

水平の線分割数<br>
widthSegments — number of horizontal segments. Minimum value is 3, and the default is 32.

垂直の線の分割数<br>
heightSegments — number of vertical segments. Minimum value is 2, and the default is 16.

どの角度から水平の線分割をはじめるか？？
phiStart — specify horizontal starting angle. Default is 0.

水平方向の掃引角の大きさ
phiLength — specify horizontal sweep angle size. Default is Math.PI * 2.

どの角度から垂直の線分割をはじめるか？？
thetaStart — specify vertical starting angle. Default is 0.

垂直方向の掃引角の大きさ
thetaLength — specify vertical sweep angle size. Default is Math.PI.

## 球体
width — Width; that is, the length of the edges parallel to the X axis. Optional; defaults to 1.

height — Height; that is, the length of the edges parallel to the Y axis. Optional; defaults to 1.

depth — Depth; that is, the length of the edges parallel to the Z axis. Optional; defaults to 1.

widthSegments — Number of segmented rectangular faces along the width of the sides. Optional; defaults to 1.

heightSegments — Number of segmented rectangular faces along the height of the sides. Optional; defaults to 1.

depthSegments — Number of segmented rectangular faces along the depth of the sides. Optional; defaults to 1.

## 平面
width — Width along the X axis. Default is 1.

height — Height along the Y axis. Default is 1.

widthSegments — Optional. Default is 1.

heightSegments — Optional. Default is 1.

