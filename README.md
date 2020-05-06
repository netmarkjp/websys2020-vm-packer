# WEBSYS2020 VMセットアップ

WEBSYS2020の実習用VMを模したイメージをPackerで作る

## 実行の前提条件

- 実習用VMではなく各自のPCなどで実行する
- packerがインストールされている
- VirtualBoxがインストールされている

## 実行手順

初期パスワードを変更する場合は `http/ks.cfg` の該当箇所を検索などで探して書き換える

- `user` ユーザ： `UserPassword`
- `root` ユーザ： `RootPassword`

```sh
# CentOS-7-x86_64-DVD-1804.iso` をダウロードして `files`直下に置く
curl -o files/CentOS-7-x86_64-DVD-1804.iso \
  http://mirror.nsc.liu.se/centos-store/7.5.1804/isos/x86_64/CentOS-7-x86_64-DVD-1804.iso

packer build centos7.json
```
