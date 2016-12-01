
___
  
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

#### NASに見立てたディレクトリを作成する

1. ユーザホームディレクトリに任意のディレクトリを作成する
(ホームディレクトリ配下であれば、ディレクトリの深さは関係しません)

```
 ~$ pwd
 /Users/YourAccount/
 
 ~$ mkdir `tmp`
 
 ~$ chmod 777 `tmp`
```
  

2. LocalMac.propertysに以下の設定を追加
```
# NASに見立てたディレクトリ
vasappliance.nas.root=`/Users/YourAccount/tmp`
```

・上記の環境あるなしでテストコードの変更点true/false
・ビルドが通らない時の対処
