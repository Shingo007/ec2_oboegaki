#　概要
## 何がしたいか
## ec2-userでSFTPでログインした際にapacheのグループに登録しアップロード許可する

# apacheグループにec2-userを登録
$ sudo usermod -a -G apache ec2-user

# 該当ディレクトリの権限書き換え
$ sudo chown -R ec2-user:apache /hoge/fuga/
$ sudo chmod 2775 /hoge/fuga/