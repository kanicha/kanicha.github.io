&nbsp;  
**AIの歌** [Github](https://github.com/KURO-Games/songForAI)

## プレイ動画
<iframe width="560" height="315" src="https://www.youtube.com/embed/dH-3s-zMx2k" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## コンセプト
複数の楽器で遊べるiPad用リズムゲームです。 

## アピールポイント
入学して、プログラミングを初めて3ヶ月未満の時に、先生から推薦され  
2年生から参加できるプロジェクトに参加させて頂き、作業を行っていたプロジェクトです。  
右も左も分からなかったので、先輩を頼りながら作業を行っていました。

### 制作意図
東京ゲームショウ2020出展用ゲームのチーム制作作品

### プラットフォーム
iOS iPadMini

### 使用言語・エンジン
C#  
Unity 2019.2.21f1  

### 曲選択画面
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/SongForAI/SongSelectUI/pics1.PNG?raw=true">  
CSVで読み取ったデータを使い、各難易度やクリア状況を表示するクラスです。
配列やSwitchを使って分岐を行いSerializeFieldを使って表示を行っています。
当時から忘れないように、コメントを付けるように意識して実装を行っていました、結果時間が立って見直しても  
見やすいソースコードになったと思います。  

### CSVファイルからデータの習得
<img width="500" src="https://github.com/kanicha/kanicha.github.io/blob/Master/image/SongForAI/ReadCSV/pics1.PNG?raw=true">  
曲のマスターデータ(曲名、難易度の値など)をCSVで管理していたので、
スクリプトを通しデータを習得する処理を書いていました。  

**[トップページへ戻る](../index.md)**
