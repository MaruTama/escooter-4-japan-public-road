# 回路
## 配線


### 操舵
#### 前照灯
|色|電圧(v)|
|--|--|
|黄|2.8|
|黒|0|

#### アクセル
|色|電圧|
|--|--|
|黒||
|緑||
|赤||

#### 制動
|色|電圧|
|--|--|
|赤||
|青||
|黒||

#### 電源
|色|電圧|
|--|--|
|赤|5|
|緑|39|
|黄|3|
|黒|0|


### 底板
#### 底部灯
youtube  
8:00, 16:55

青は制動灯。黄色は信号線。赤−黒は電源ライン。  

|色|電圧|
|--|--|
|赤|4.9v|
|青|4.6v|
|黄|70~15mv|
|黒|0v|

#### 制動灯
自己点滅ではない。ボード側で点滅制御してる。

|色|電圧(v)|
|--|--|
|青|点灯時：4.6|
|黒|0|

## 改造箇所
### ブレーキランプ
74HC123(モノステーブルマルチバイブレーター)を使うと、ブレーキランプを作れそう。

[NaPiOnでインテリジェントLED...page.1/3](https://www.zea.jp/audio/iled/iled_01.htm)  
>74HC123はリトリガ可能なモノステーブルマルチバイブレーターですから時定数の時間内にトリガ入力があると、その時点から再度時定数だけQ出力がHレベルになります。即ち、LEDがタイマー点灯していてもNaPiOnの周囲で人が動いてパルスが出ている間はリトリガが掛かりLEDは点灯し続けます。

[暇つぶし電子工作](https://jp.finalfantasyxiv.com/lodestone/character/29585/blog/2298440)

説明  
[Monostable](https://en.wikipedia.org/wiki/Monostable)  
![Green line shows input waveform to monostable multivibrator. Red line shows converted output. It can act as frequency divider.](https://en.wikipedia.org/wiki/Monostable#/media/File:Monostable_multivibrator_input_output.png)  
[モノステーブル・マルチバイブレータ](https://kotobank.jp/word/%E3%83%A2%E3%83%8E%E3%82%B9%E3%83%86%E3%83%BC%E3%83%96%E3%83%AB%E3%83%BB%E3%83%9E%E3%83%AB%E3%83%81%E3%83%90%E3%82%A4%E3%83%96%E3%83%AC%E3%83%BC%E3%82%BF-142651)


[静電容量の温度特性](https://www.murata.com/ja-jp/products/emiconfun/capacitor/2012/10/15/en-20121015-p1)  
導電性高分子アルミ電解コンデンサが温度特性が良い。
