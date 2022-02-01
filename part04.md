# カメラの制御(OrbitControls)
Three.jsにはカメラの動きを自動的に制御する THREE.OrbitControls クラスが存在します。

次の用途で役立つ機能です。

 - 周回軌道を描くように、カメラを配置する 
 - ポインター操作でカメラの配置やアングルを変更する

CDN等で読み込んで利用する

## 使い方
THREE.OrbitControlsは次の書式で利用します。THREE.OrbitControlsクラスのコンストラクターへ、カメラのインスタンスとDOM要素を引数として指定します。これだけで、自動的にマウスと連動してインタラクションが効くようになります。

```
// カメラを作成
const camera = new THREE.PerspectiveCamera(/*省略*/);
// カメラの初期座標を設定
camera.position.set(0, 0, 1000);

// カメラコントローラーを作成。カメラのインスタンスとDOM要素を引数として指定
const controls = new THREE.OrbitControls(camera, document.body);
```

マウス操作で次のようにカメラを制御できます。

 - オービット（周回軌道）: 左ボタンでドラッグ
 - ズーム: マウスホイール
 - パン: 右ボタンでドラッグ

 ## 滑らかにコントロールする
THREE.OrbitControlsインスタンスのenableDampingやdampingFactorプロパティーを設定すると、ドラッグ時にカメラが滑らかに動くようになります。デフォルトだと機械的な動きになってしまいますが、これらのプロパティーを設定するだけで心地良い操作感になります。

enableDampingやdampingFactorプロパティーを使う場合は、requestAnimationFrame内でTHREE.OrbitControlsインスンタンスのupdateメソッドを呼び出す必要があります。