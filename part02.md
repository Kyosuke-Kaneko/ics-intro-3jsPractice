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
```js
SphereGeometry(radius : Float, widthSegments : Integer, heightSegments : Integer, phiStart : Float, phiLength : Float, thetaStart : Float, thetaLength : Float)
```

width — Width; that is, the length of the edges parallel to the X axis. Optional; defaults to 1.

height — Height; that is, the length of the edges parallel to the Y axis. Optional; defaults to 1.

depth — Depth; that is, the length of the edges parallel to the Z axis. Optional; defaults to 1.

widthSegments — Number of segmented rectangular faces along the width of the sides. Optional; defaults to 1.

heightSegments — Number of segmented rectangular faces along the height of the sides. Optional; defaults to 1.

depthSegments — Number of segmented rectangular faces along the depth of the sides. Optional; defaults to 1.

## 直方体
```js
BoxGeometry(width : Float, height : Float, depth : Float, widthSegments : Integer, heightSegments : Integer, depthSegments : Integer)
```

width — Width; that is, the length of the edges parallel to the X axis. Optional; defaults to 1.

height — Height; that is, the length of the edges parallel to the Y axis. Optional; defaults to 1.

depth — Depth; that is, the length of the edges parallel to the Z axis. Optional; defaults to 1.

widthSegments — Number of segmented rectangular faces along the width of the sides. Optional; defaults to 1.

heightSegments — Number of segmented rectangular faces along the height of the sides. Optional; defaults to 1.

depthSegments — Number of segmented rectangular faces along the depth of the sides. Optional; defaults to 1.

## 平面
```js
PlaneGeometry(width : Float, height : Float, widthSegments : Integer, heightSegments : Integer)
```

width — Width along the X axis. Default is 1.

height — Height along the Y axis. Default is 1.

widthSegments — Optional. Default is 1.

heightSegments — Optional. Default is 1.

## 円錐
```js
ConeGeometry(radius : Float, height : Float, radialSegments : Integer, heightSegments : Integer, openEnded : Boolean, thetaStart : Float, thetaLength : Float)
```

底面の半径<br>
radius — Radius of the cone base. Default is 1.

底面からの高さ<br>
height — Height of the cone. Default is 1.

radialSegments — Number of segmented faces around the circumference of the cone. Default is 8

heightSegments — Number of rows of faces along the height of the cone. Default is 1.

底面が描画されているかどうか<br>
openEnded — A Boolean indicating whether the base of the cone is open or capped. Default is false, meaning capped.

thetaStart — Start angle for first segment, default = 0 (three o'clock position).

thetaLength — The central angle, often called theta, of the circular sector. The default is 2*Pi, which makes for a complete cone.

## 円柱
```js
CylinderGeometry(radiusTop : Float, radiusBottom : Float, height : Float, radialSegments : Integer, heightSegments : Integer, openEnded : Boolean, thetaStart : Float, thetaLength : Float)
```
円のてっぺんの半径
radiusTop — Radius of the cylinder at the top. Default is 1.

円の底面の半径
radiusBottom — Radius of the cylinder at the bottom. Default is 1.

円柱の高さ
height — Height of the cylinder. Default is 1.

radialSegments — Number of segmented faces around the circumference of the cylinder. Default is 8

heightSegments — Number of rows of faces along the height of the cylinder. Default is 1.

openEnded — A Boolean indicating whether the ends of the cylinder are open or capped. Default is false, meaning capped.

thetaStart — Start angle for first segment, default = 0 (three o'clock position).

thetaLength — The central angle, often called theta, of the circular sector. The default is 2*Pi, which makes for a complete cylinder.

## ドーナツ形状
```js
TorusGeometry(radius : Float, tube : Float, radialSegments : Integer, tubularSegments : Integer, arc : Float)
```

円の半径
radius - Radius of the torus, from the center of the torus to the center of the tube. Default is 1.

円周状からどれだけ埋めるか
tube — Radius of the tube. Default is 0.4.

radialSegments — Default is 8

tubularSegments — Default is 6.

描画する中心角度
arc — Central angle. Default is Math.PI * 2.

## パラメーターについて
上記で紹介した形状ですが、それぞれにクラスのコンストラクターの引数で大きさ等を指定できます。ほとんどのクラスで同じ引数を取るのですが、代表的なものを紹介すると次の通りです。

width : 横幅
height : 高さ
depth : Cubeにおける奥行き
radius : 半径。Sphereでは球体の半径で、ConeとCylinderでは底辺の半径。
segmentsW : 横方向の分割数
segmentsH : 縦方向の分割数
segments（セグメント）というパラメーターは2次元表現にないので、見慣れないパラメーターだと思います。3Dでは表示オブジェクトをポリゴン化して表示させるのですが、** セグメントというパラメーターは大雑把にいうとポリゴンの細分化の分割数** となります。たとえばセグメントを増やすと、球体（SphereGeometry）ではより滑らかになります。