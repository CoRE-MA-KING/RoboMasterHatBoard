# RoboMasterHatBoard
ロボマス開発ボード用ハットです。  
CoREに出場するロボットに利用しているメインボードとして[RoboMaster 開発ボードタイプA](https://store.dji.com/jp/product/rm-development-board-type-a?vid=42041)を利用しているので、このボードから2024年大会用に必要なピンをコネクタにまとめるための基板。

![](./docs/RoboMasterHatBoard.png)


# 機能
ロボマス開発ボードにはピンヘッダからいくつかのピンが出ているので、そこから今回のロボットで利用するピンを取り出します。

[回路図](https://ausdroid.co/wp-content/uploads/2020/08/RoboMaster-Development-Board-Type-A-Schematic.pdf)より
![](./docs/RoboMasteDevBoard_sch1.png)
![](./docs/RoboMasteDevBoard_sch2.png)

具体的に以下のピンを取り出します。
|ピン名|ペリフェラル|用途|備考|
||---|---|---|  
|PD12|TIM4_CH1| モータ1PWM用||
|PD13|TIM4_CH2| モータ2PWM用||
|PA0|TIM2_CH1| エンコーダ1 A相||
|PA1|TIM2_CH2| エンコーダ1 B相||
|PA2|GPIO_INPUT| エンコーダ1 Z相||
|PI5|TIM8_CH1| エンコーダ2 A相||
|PI6|TIM8_CH2| エンコーダ2 B相||
|PI7|GPIO_INPUT| エンコーダ2 Z相||
|PF0|GPIO_INPUT|フォトインタラプタ1入力||
|PF1|GPIO_INPUT|フォトインタラプタ2入力||
|PE6|GPIO_INPUT|非常停止ボタン読み取り|マイコンの内部プルアップ必須|
|PE12|GPIO_OUTPUT|リレー駆動信号||
|PC1|GPIO|汎用GPIO|予備ポート|

v0.1の基板上のシルクと回路図上の信号線が逆になっているので注意。回路図が間違っているということにして基板のシルクに従うようにすること。上の表に従えばOK。
