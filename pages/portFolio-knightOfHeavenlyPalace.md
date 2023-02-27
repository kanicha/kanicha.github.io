&nbsp;  
**天上宮殿の騎士** [Github](https://github.com/letconst/knight-of-heavenly-palace-public)

## プレイ動画
<iframe width="560" height="315" src="https://www.youtube.com/embed/L-TG0qn3S3A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## コンセプト
剣を投げて相手にワープし剣を切ることで敵を倒す、3Dアクションゲームです。  

## アピールポイント
2Dゲームのみを今まで制作してきましたが、3DゲームでありNintendo Switch向けのゲーム開発という初めての試みで、新しい知識や新しい技術に挑戦を行った作品です。  
Nintendo SwitchのJoy-Conを振ることでキャラクターが攻撃を行い、剣を振る楽しさを追求しました。  

### 制作意図
東京ゲームショウ2022出展用ゲームのチーム制作作品  
Nintendo Switchのゲーム開発を体験、学習の為  

### プラットフォーム
Nintendo Switch  

### 使用言語・エンジン
C#  
Unity 2021.2.15f1  

## 担当箇所

### 剣の投擲
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/HevenlyPlace/Throwing/pics1.PNG?raw=true">
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/HevenlyPlace/Throwing/pics2.PNG?raw=true">  
ボタンが押された時にカーソルの方向にあるオブジェクトに対しRayを飛ばし、そのRayがhitしたら投擲処理を行います。
プレイヤーのレイヤーや、当たってはいけないオブジェクトを対象から除外や、右手と左手に両手に剣を持っているため、入力によって情報を分けたりなど意識をし、実装を行っていました。
ゲームのとても大事な部分なので、実装と基本設計を綺麗にする事を意識しておりました。

### ぶら下がり処理
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/HevenlyPlace/Hanging/pics1.PNG?raw=true">
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/HevenlyPlace/Hanging/pics2.PNG?raw=true">  
一定の角度で剣が投げられ、着弾したらぶら下がり状態に変更を行う処理を担当させていただきました。  
剣が着弾された時に、右手か左手の情報と角度の算出処理に苦戦し、調べながら実装を行いました。  
結果、非同期処理でイベントを通して情報が渡される処理になり、綺麗に実装できたと思います。  

### プレイヤーのアクション
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/HevenlyPlace/PlayerAction/pics1.PNG?raw=true">
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/HevenlyPlace/PlayerAction/pics2.PNG?raw=true">
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/HevenlyPlace/PlayerAction/pics3.PNG?raw=true">  
プレイヤーの移動処理、ジャンプ処理、緊急回避処理を担当させていただきました。  
移動速度の変更等をし易い様に、引数で値を受け取りその値に応じて変更を行えるように気を使いながら  
カメラの向きを前として処理を行う様にし、直感的な操作が出来るように実装を行いました。


### イベント発行管理処理
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/HevenlyPlace/EventIssueClass/pics1.PNG?raw=true">
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/HevenlyPlace/EventIssueClass/pics2.PNG?raw=true">  
Joy-Conの入力を受け取り、入力によって対応する行動のイベントをUniRXを通して発行する処理の担当させていただきました。  
主に例外処理等を行っていて、処理を行うクラスでは無駄な処理は少なくし、処理だけを書くように意識をして、制作を行っていました。  

**[トップページへ戻る](../index.md)**
