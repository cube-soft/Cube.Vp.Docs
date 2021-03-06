CubeVPM
====

Copyright © 2010 CubeSoft, Inc.  
support@cube-soft.jp  
https://www.cube-soft.jp/cubevp/

## はじめに

Cube VirtualPrinter Manager (CubeVPM) は、仮想プリンターのインストール
およびアンインストールを実行するための GUI アプリケーションです。
CubeVPM を使用するには .NET Framework 3.5 以降が必要です（4.5.2 以降を強く推奨）。
もし、ご利用の端末にインストールされていない場合、以下の URL からダウンロードして下さい。

* Download .NET Framework  
  https://dotnet.microsoft.com/download/dotnet-framework

## 使用方法

![新しい仮想プリンターを追加](https://github.com/cube-soft/Cube.Vp.Docs/blob/master/Documents/Assets/Cube.Vp.Installer.Gui.ja.01.png?raw=true)

CubeVPM を初めて起動すると、まず、新しい仮想プリンターを追加する画面が表示されます。
追加時に設定する項目は下記の通りです。

* **プリンター名**  
  指定された名前で新しい仮想プリンターが作成されます。
  プリンター名には英数字の他、日本語を指定する事も可能です。
* **アプリケーション**  
  印刷が実行された時に実行されるアプリケーションへのパスを指定します。
  指定されたアプリケーションに対して何らかの引数が必要な場合、
  その下のテキストボックスに入力します。
  尚、仮想プリンターは印刷データを一時保存したパスや印刷時に指定されたドキュメント名など、
  いくつかの引数は必ず指定されます。
* **作業フォルダ**  
  仮想プリンターが印刷データを一時保存するフォルダを指定します。
  特に理由がなければ初期設定をそのままご利用下さい。
  尚、作業フォルダは SYSTEM アカウントおよびログオン中のユーザーがともにアクセス可能な必要があります。
  「ユーザー (Users)」フォルダは SYSTEMアカウントがアクセスできないのでご注意下さい。
* **アプリケーションが終了するまで次の印刷ジョブを実行しない**  
  このオプションを有効にすると、プリントスプーラに複数の印刷ジョブが登録された場合に、
  指定されたアプリケーションの実行が終了するまで次の印刷ジョブの開始を待つようになります。
  無効の場合はアプリケーションが実行中かどうかに関わらず、
  印刷ジョブが登録されると即座にアプリケーションの実行を試みます。
* **アプリケーションをユーザーアカウントで実行する**  
  印刷は SYSTEM アカウントで実行されるため、そのままの状態だと指定されたアプリケーションも
  SYSTEM アカウントで実行される事となります。
  このオプションを有効にすると、ログオン中のユーザーで指定されたアプリケーションを実行するようになります。
  尚、ログオン中のアカウントを特定する際、印刷コマンドを発行したアプリケーションのユーザー名を利用します。
  このため、サービス経由など、ログオン中のユーザー以外のアカウントから印刷を実行した場合、
  このオプションが有効に機能しないのでご注意下さい。

登録された仮想プリンターは、下記の画面で管理されます。

![登録された仮想プリンター一覧](https://github.com/cube-soft/Cube.Vp.Docs/blob/master/Documents/Assets/Cube.Vp.Installer.Gui.ja.02.png?raw=true)

プリンター名以外の項目は、追加後に変更する事ができます。
変更したい項目を修正した後、適用ボタンを押して下さい。
また、仮想プリンターが不要になった場合は、削除ボタンを押して下さい。

## 注意

CubeVPM は、登録された仮想プリンターの構成を独自に管理しています。
そのため、設定やコントロールパネル経由で仮想プリンターの構成を変更すると予期せぬ不都合が発生する事があるので、ご注意下さい。