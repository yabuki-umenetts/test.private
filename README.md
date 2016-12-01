# test.private
1. 以下のサイトから"`GPG Suite`"をダウンロードし、インストールする
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
