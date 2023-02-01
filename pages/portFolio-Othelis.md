&nbsp;  
**オセリス** [Github](https://github.com/kanicha/ReOthelis)

## プレイ動画
<iframe width="560" height="315" src="https://www.youtube.com/embed/b96pgPBNnoA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## コンセプト
オセロとテトリスの様な落ちものパズルを組み合わせた、対戦型ゲームです。 

## アピールポイント
専門学生2年生の頃に、一年間制作を行ったパズルゲームです。  
当時、プログラマーリーダーやプランナーが消息不明になり、プランナー兼プログラマーリーダとして制作を行っていました。  
2022年7月23日と24日に開催された学園祭にて、にじさんじ様所属の周央サンゴ様と西園チグサ様に遊んでいただいた経歴があります。
<iframe width="560" height="315" src="https://www.youtube.com/embed/D6MCnh2Usbc?start=3012" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### 制作意図
東京ゲームショウ2021出展用ゲームのチーム制作作品  
(東京ゲームショウ2021がコロナの影響で中止してしまったので、学校内での展示) 

### プラットフォーム
Windows  

### 使用言語・エンジン
C#  
Unity 2020.2.5f1 

## 担当箇所

### キャラクター選択
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/Othelis/CharactorSelect/pics1.PNG?raw=true">
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/Othelis/CharactorSelect/pics2.PNG?raw=true">  
キャラクターの名前のEnumを使って実装をしているので、どのキャラクターが選択されているかを  
スクリプト上から見やすいように、気をつけて実装を行いました。  
デバッグ用に、キーボード等でも操作できるようになっております。  

### スキル
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/Othelis/Skill/pics1.PNG?raw=true">
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/Othelis/Skill/pics2.PNG?raw=true">  
スキルを発動してから着地して発動するという効果や、その場で発動する等の様々な種類があり  
様々な実装方法が必要で、とても苦労しましたが、非同期処理を初めて使い実装を行いました。  
キャラクター毎に使えるスキルが違うため、各スキルを関数化をして、キャラクターが選択された時に  
動的にリストに追加して、管理を行うように実装しています。  

### サーバー
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/Othelis/Server/pics1.PNG?raw=true">
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/Othelis/Server/pics2.PNG?raw=true">  
一年間の後半は追加要素の実装を行っていたので、サーバーの実装時間がとても少なく、2週間で実装を行っています。  
元々二人用のゲームだったので、オンライン対戦を実装する際に、全体的にクライアント側のソースコードも変更を加えています。  


### コマ生成処理
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/Othelis/PieceCreate/pics1.PNG?raw=true">
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/Othelis/PieceCreate/pics2.PNG?raw=true">  
コマの生成処理を実装
RANDOM関数を使って値を選出を行い、その数値によって分岐を行い    
前のターンと同じコマを出さないように、例外処理等を同時に行うように、実装をしています。  
選出を行った後は、タイプによって名前の付与とEnumを使ったタイプの付与を行って生成を行っています。

### 追加の回転処理の実装
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/Othelis/AddRotate/pics1.PNG?raw=true">
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/Othelis/AddRotate/pics2.PNG?raw=true">  
コマが壁に隣接している時に、回転を行った場合コマが弾かれながら回転する動作や  
両側が埋まっている場合に、回転操作を行うとコマが上下反転する処理を実装しました。
操作面でストレスを抱えずユーザーさんがプレイしやすいよう意識して発案と実装を行いました。  

### 全体的なバグ修正
天井で回転してコマが上下逆になっている時にコマがうまく着地しないバグや  
待機中に横入力を行ってしまうと、コマがコマの上に乗ってしまうバグやその他の細かいバグを修正しました。  
1からゲームのスクリプトを全て見直しを行い、アルゴリズムに不備はないか、変ではないか重点的に、原因を特定し修正しました。

**[トップページへ戻る](../index.md)**
