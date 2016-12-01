## 開発環境で必要な準備

#### 暗号化キーを設定する 

1. GnuPGのインストール(_すでにGnuPGがインストールされている場合は不要_)  
 以下のサイトから"`GPG Suite`"をダウンロードし、インストールする 
 <https://gpgtools.org>

2. 鍵を作成する
  - 「GPG Keychain」を起動して、「`New`」ボタンをクリックする
  - 「`Full name`」に"`vasappliance`"を入力して、「`Generate key`」ボタンを押す
  - `"パスフレーズがありません"`と警告が表示されるが、「`パスワード無しで続ける`」ボタンを押す
  - 一覧に"`vasappliance`"のキーが表示されれば終了

3. LocalMac.propertysに以下の設定を追加
```
# GPGの暗号・復号化キー
vasappliance.key.id=vasappliance
```
#### LocalMac.propertysに以下の設定を追加
対象ファイル：src/test/resource/properties/environment/localMac.properties

- NASに見立てたディレクトリ
vasappliance.nas.root=`/Users/xxxxx/Document/tmp`

- GPGの暗号・復号化キー
vasappliance.key.id=`vasappliance`


・上記の環境あるなしでテストコードの変更点true/false
・ビルドが通らない時の対処
