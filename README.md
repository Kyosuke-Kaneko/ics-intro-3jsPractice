# 3js-ics-media初級
[https://ics.media/tutorial-three/quickstart/](https://ics.media/tutorial-three/quickstart/)

## three,js基本構造
## THREE.Sceneクラス

3Dの空間を表すクラス。3Dの作成されたオブジェクト(メッシュ)はシーンにadd()メソッドを利用して追加することで表示できます。

## THREE.PerspectiveCameraクラス

3D空間を撮影するカメラ。視点を制御するために使用します。3D空間のどの視点で撮影しているのかの情報が必要となります。<br>
画角、アスペクト比、描画開始距離、描画終了距離の4つを作成し、position.setする

## THREE.WebGLRendererクラス

3D空間のレンダリングを行います。レンダリングとは、データを元に一定の処理や計算を行い、画像や映像、音声をさくせいすることです。この場合は、Three.jsで計算した3Dのオブジェクトを画面に表示することです。内部的にはThree.jsがWebGLのAPIを使って、GPUで座標を計算させ画面に表示させています。Three.jsではrequestAnimationFrameのタイミングにあわせて、レンダリングを行うように設定しましょう。
