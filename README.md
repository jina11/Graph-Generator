# Graph-Generator
2軸グラフ、対数グラフ、近似曲線を手早く作成するプログラム

![キャプチャ](https://user-images.githubusercontent.com/44617952/54919611-95234d80-4f44-11e9-9c6e-d6a9b0031c3a.PNG)

「Import file」からグラフにしたいcsvファイルを取り込むと、上のような画面になります。

点や線のスタイル、対数軸設定、Y1軸・Y2軸のどちらに描画するかなどを決めることができます。X軸として用いるデータ系列も設定する必要があります。

![キャプチャ2](https://user-images.githubusercontent.com/44617952/54919640-a704f080-4f44-11e9-86d6-c7411f1cb0ec.PNG)


「Output」でグラフが出力されます。

グラフの凡例は、ドラッグ&ドロップで移動させることが可能です。

![キャプチャ3](https://user-images.githubusercontent.com/44617952/54919652-b3894900-4f44-11e9-8fcf-4788c0a14332.PNG)


## 各設定項目の詳細

- X-axis name：X軸のラベル名称
- Y1-axis name：Y1軸のラベル名称
- Y2-axis name：Y2軸のラベル名称
- X-range X軸について、beginからendの範囲を描画し、tick間隔で目盛を描画
- Y1-range Y1軸について、beginからendの範囲を描画し、tick間隔で目盛を描画
- Y2-range Y2軸について、beginからendの範囲を描画し、tick間隔で目盛を描画
- Dataname データファイルのheaderを表示
- Label：描画するデータの凡例名称、空欄で凡例なし
- Marker：データ点に用いるマーカー
- Line：線の選択
- Approx：n次多項式による近似曲線
- Degree：n次多項式のn
- Approx Label：近似曲線の凡例名称、空欄で凡例なし

## 注意点

- 近似曲線を描画するときは、元のデータ点を結ぶ直線は描画されません

## 更新内容

- 2018/11/23 

csvにヘッダがある場合に動作しない不具合を解消しました。

横軸が対数の場合（周波数など）に、近似曲線に補正をかける機能を実装しました。多項式の係数決定に用いるxの値をlog10としています。

- 2019/3/25

描画範囲、主目盛間隔、x軸データ選択を行えるようにしました。

- 2019/8/8

デフォルトで日本語に対応、Datanameの追加、encoding指定の追加を行いました。この更新で、ファイルにheaderが必須となりました。

- 2019/10/3

グラフ出力時に設定を保存し、import時に設定を呼び出すようにしました。

## 今後実装予定

- 近似直線・曲線のスムージング
