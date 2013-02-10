# このプログラムについて

YukkuriTalkClientは、引数に与えた文字列をゆっくり声で喋らせるというプログラムです。  
YukkuriTalkServerとセットで使うことを前提に作られています。  
クライアントは指定された文字列をサーバ側にPOSTし、wavファイルをダウンロードし再生します。  
発声処理など主要な処理は全てサーバで行っています。  

* @author 松井 健太郎 (Kentaro Matsui) <info@ke-tai.org>
* @copyright ke-tai.org
* @license BSD
* @link http://www.a-quest.com/products/aquestalk.html
* @link http://github.com/ketaiorg/YukkuriTalkServer/

----

## インストール方法

Ubuntu12.10へのインストールを例に説明します。  


### 必要なパッケージのインストール

- php5 : このプログラムはPHPで書かれており実行に必要です  
`$ sudo apt-get install php5-cli`

- php5-curl : PHP内からcurl_*関数を利用するのに必要です  
`$ sudo apt-get install php5-curl`

----

### 設定

通常サーバ側が正しく設定されていれば、次の箇所のみ変更するだけで実行が可能です。  
`protected $api_url = 'http://localhost/YukkuriTalkServer/yukkuritalk.php';`  
このURLを設置したYukkuriTalkServerのURLに設定します。  


### 実行

実行プログラム本体に実行権があることを確認し、次のように実行します。

`$ ./yukkuritalkclient "あいうえお"`  

> [talked] （あいうえお）

のように表示され発声されます。

----

