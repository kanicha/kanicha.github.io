&nbsp;  
**TIMESCALE** [Github](https://github.com/kanicha/HageExplosion)

## プレイ動画
<iframe width="560" height="315" src="https://www.youtube.com/embed/8AaDiDjRnw4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## コンセプト
Enterキーでハゲのおじさんを爆発させるゲームです。  
爆発させればスコアが増えていきそのスコアで競うゲームになっています。

## アピールポイント
1年生の時に、授業の一環で一人で制作を行ったゲームです。
当時習ったばかりのfor文やif文を使い、どこまで制作を行えるか  
挑戦した作品でもあります。  

### 制作意図
自分一人でゲーム作れるかの学習の為  

### プラットフォーム
Windows  

### 使用言語・エンジン
C#  
Unity 2019.2.21f1  

### ハゲ管理クラス
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/HageExprosion/HageController/pics1.PNG?raw=true">  
Input関数を使って、Enterキーで爆発するように実装しています。  
それと同時にハゲの生成を行っています、当時覚えたてのInstatiateを使って生成を行いました。  

### スコア管理
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/HageExprosion/Score/pics1.PNG?raw=true">  
スコアの上昇を管理してるクラスです。  
ボタンが押されるたびにスコアの値を参照を行い、決められた値よりスコアが多くなった場合、スコアが跳ね上がるようになっており    
Enterキーを押せば押すほど値が増えるので、一定で値が増えるより面白いと考え実装を行いました。

**[トップページへ戻る](../index.md)**
