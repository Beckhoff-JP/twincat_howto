# Cam 設定手順

<!-- TOC -->

- [前提](#前提)
- [Cam の導入](#cam-の導入)
  - [NC Task を追加する](#nc-task-を追加する)
  - [Axis を追加する](#axis-を追加する)
  - [Master を追加する](#master-を追加する)
  - [Slave を追加する](#slave-を追加する)
- [Cam の作成](#cam-の作成)
  - [Motion の作成](#motion-の作成)
  - [グラフの形状を変える](#グラフの形状を変える)

## 前提

TE1510 : Cam Design Tool
Cam のデータを保存する場合に使用する。

## Cam の導入

### NC Task を追加する

![NCTaskの追加](assets/NCTaskの追加.png)  
MOTION > Add New Item...を選択する。

![NCTask追加ダイアログ](assets/NCTask追加ダイアログ.png)  
目的の NCTask を作成する。

### Axis を追加する

![Axisの追加](assets/Axisの追加.png)  
Axes > Add New Item...を選択する。

![Axis追加ダイアログ](assets/Axis追加ダイアログ.png)  
Master と Slave 用に 2 軸 Continuous Axis を追加する。

### Master を追加する

![Masterの追加](assets/Masterの追加.png)  
Tables > Add New Item...を選択する。

![Master追加ダイアログ](assets/Master追加ダイアログ.png)  
Motion Diagram で Master を追加する。

### Slave を追加する

![Slaveの追加](assets/Slaveの追加.png)  
Master > Add New Item...を選択する。

![Slave追加ダイアログ](assets/Slave追加ダイアログ.png)  
Slave を追加する。

## Cam の作成

### Motion の作成

![Slaveの選択](assets/Slaveの選択.png)  
Slave を選択します。

![Cam作成画面](assets/Cam作成画面.png)  
上がポイントの情報画面(上部)
下がプロファイル画面(下部)

![Cam作成画面2](assets/Cam作成画面2.png)

![InsertPoint選択](assets/InsertPoint選択.png)  
Insert Point を選択します。

![Pointの追加](assets/Pointの追加.png)  
下部にポイントを作る。

![Point追加上部](assets/Point追加上部.png)  
ポイントができると上部にポイントのデータが自動生成されます。

![Pointの追加2](assets/Pointの追加2.png)  
ポイントを 2 つ追加する。

![Point追加上部2](assets/Point追加上部2.png)  
上部のデータも自動追加されます。

### グラフの形状を変える

![Function](assets/Function.png)  
上部の Fuction でグラフの形状を変更できます。

![Functionの結果](assets/Functionの結果.png)  
Function に合わせてグラフが変化します。
