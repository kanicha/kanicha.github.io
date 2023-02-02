&nbsp;  
**TIMESCALE** [Github](https://github.com/kanicha/TIMESCALE-Public)

## プレイ動画
<iframe width="560" height="315" src="https://www.youtube.com/embed/EeYeuuupJBc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## コンセプト
ゲーム画面下部にあるスキルを使い、敵を倒す 戦略性カードゲームです。  

## アピールポイント
iOS向けの開発は過去に数回行ったことがあるので、スムーズに制作を行っていました。  
今回、SEGA様から学校を通してお仕事を頂き、制作を行い、滋慶グループのイベント COMゲームショウで出展を行いました。  
同時に、学校の中で優秀賞を頂き、COMゲームショウのステージに上り、こちらのゲームの発表を行いました。  
ゲームを一本、半年間という期間で一人で制作を行うのは初めての試みでしたが、楽しく遊べるゲームになったと思っております。  

### 制作意図
SEGA様の企業プロジェクト制作作品  
2022 COMゲームショウ展示用作品  
一人でゲーム制作を行う 経験・学習のため  

### プラットフォーム
iOS 12Pro  

### 使用言語・エンジン
C#  
Unity 2021.2.15f1  

### スキル基底クラス
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/TIMESCALE/SkillBaseClass/Pics1.png?raw=true">
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/TIMESCALE/SkillBaseClass/Pics2.PNG?raw=true">
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/TIMESCALE/SkillBaseClass/Pics3.PNG?raw=true">  
今回スキルが3種類あるということが仕様で分かっていたので、スキルの基底クラスを制作することで追加と削除がしやすくなるように実装しました。  
スキル一つ一つにTypeというEnumを作ってあげて設定していることで、他のスクリプトからも参照できるようになり処理しやすい書き方にできたと思っています。  

### スキル発動
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/TIMESCALE/SkillActive/Pics1.PNG?raw=true">
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/TIMESCALE/SkillActive/Pics2.PNG?raw=true">  
スキルを順に処理していく仕様だったので、リストに追加された時に処理関数を呼ぶように実装しました。  
スキルのタイプをEnumで宣言しているため、タイプを見て各処理を行う関数へと分岐処理を行い、発動タイミングがあっていたら発動する実装にしています。  
タイプによって細かな処理変更を加える事ができるため、追加ができるように意識し制作を行いました。  

### ステート管理
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/TIMESCALE/State/pics1.PNG?raw=true">  
ステートをビット演算の形にすることで、複数のフラグ管理を一つのステートで管理しております。  
結果、ソースコードを実際に変更を行う際にも変数が一つのため、参照先がわかりやすく  
ステートの変更イベントを各処理で呼ぶことで、ステートの追加と削除をしやすくしており、変更と管理を見据えた実装を行いました。  

### バフ・デバフ
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/TIMESCALE/Buff/Pics2.PNG?raw=true">
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/TIMESCALE/Buff/pics1.PNG?raw=true">  
各バフの管理を、バフの名前を列挙したEnum型Dictionaryを使って管理を行っています。  
バフの名前をEnumで宣言することで、視覚的に追加しやすく且つ、Switch文等で分岐を行う際に素早く処理を行えるので、この実装を行いました。  
Dictionaryにすることで、残りバフ回数を名前と同時に管理できるように実装しています。  

**[トップページへ戻る](../index.md)**
