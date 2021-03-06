# LeapMotionとは
LeapMotionは、LeapMotion社から販売された手のジェスチャーによってコンピュータを操作ができる NUIデバイスです。

マウスや画面タッチを用いずに操作ができる体感型のシステムで、ジェスチャーによって直観的に操作することが可能となる、1/100mmミリの間隔で動作を認識します。
 
## 購入方法
国内では、BBソフトサービス株式会社が正規販売代理店になります。

[BBソフトサービス株式会社](http://www.bbss.co.jp/product/leapmotion/index.html)
### 価格
定価　$ 99
## 仕様
### スペック
* サイズ W80×D30×H11mm
* インターフェース USB 3.0/2.0
* 対応OS　Windows 7/8、Mac OS X 10.7、Ubuntu Linux 12.04LTS/13.04
* CMOSイメージセンサー　半径50センチ、中心角110度の空間で、手、指、ペンのポイントを0.01ミリの精度で認識

### ソフトウェア
* コントロールパネル
* * 設定やソフトウェアアップデートなど
* Leap Motion Visualizer
* * Leap Motion のセンシングデータをキレイに可視化
* Airspace
* * Leap Motion アプリケーションのストア 
* Leap Motion Diagnostics Visualizer
* * Leap Motion のセンシングデータを可視化

### ステータス表示
* 黒 未接続 LEAPデバイスが未接続
* 緑 通常モード 正常動作
* 黄 Robust モード 明るい環境下でもトラッキングできるように自動調整
* 茶 汚染 LEAPデバイスのセンサーウィンドウに汚れなどがある
* 赤 エラー エラーの発生、詳細はログで確認

### 開発言語について
#### APIの種類
ネイティブ・アブリケーション・インターフェース:

Leapのサービスからネイティブのライブラリを利用して直接データを受け取る方法。 ネイティブのライブラリはC++、Objective-Cで作られていて、そこからラッバーライブラリを使っ てC#、Java、Pythonを使って開発を行う。

Web Socketインターフェイス:

LeapサービスはWebSocketサーバーの機能を持っており、アブリケーションから接続し、JSON 形式でデータを受け取る方法。

http://127.0.0.1:6437でサーバーを提供します。
* JavaScript
* Unity/C#
* UnrealEngine/C++, BluePrint
* C++
* Java
* Python
* Objective-C

### 開発環境の準備
#### SDKのインストール
1. LeapMotion TOP

    デベロッバーサイトの「サインイン」でログインモーダルを開き、 登録したアカウント情報を入力して「サインイン」をクリック します。
2. LeapMotion Developerサイト

    「I accept the SDK terms and conditions.」にチェックをいれて、ダウンロードボタンをクリックします。

3. ログインモーダル画面

    ダウンロードベージに遷移し、ダウンロードが開始します。

4. ダウンロード完了

    ダウンロードフォルダに.tgzフォルダがあるのでダブルクリックします
解凍されるとフォルダ内にSDK一式が入っています。


