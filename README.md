# AWS あるある

## What is this?

AWS周りで、やってしまったこと（あるある）の個人的メモ

## 2018/12/20

- CloudFrontで限定公開する際の、`Signed URLs`, `Signed Cookies` のどちらを選択するか。
https://docs.aws.amazon.com/ja_jp/AmazonCloudFront/latest/DeveloperGuide/private-content-choosing-signed-urls-cookies.html

HLS の場合、`playlist.m3u8`（プレイリストファイル）に記載されている全体をプライベートコンテンツにする必要がある。=> `Signed Cookies`

## 2018/11/17

- Amazon SNS テキストメッセージ(SMS)の初期のアカウント使用制限は、$1 なので申請必要。

## 2018/07/04

- CloudFrontで、ACMで発行した証明書を使用する場合、N.Virginia region で発行した証明書が必要。
https://docs.aws.amazon.com/ja_jp/AmazonCloudFront/latest/DeveloperGuide/cnames-and-https-requirements.html

## 2018/03/23

- NAT Instance を作成する場合、`Source/Dest.Check` を無効にする。
https://docs.aws.amazon.com/ja_jp/AmazonVPC/latest/UserGuide/VPC_NAT_Instance.html

## 2018/03/15

- VPC設定で以下が`Off`になっていると、Private hostnameの名前解決出来なくてハマる。
https://docs.aws.amazon.com/ja_jp/AmazonVPC/latest/UserGuide/vpc-dns.html#vpc-dns-updating
- NAT Gateway は、まだipv6対応していない。
- Certificate Manager で、 `*.example.com` のワイルドカード証明書を申請する際は、webのインデックスになるような `example.com`, `www.example.com` も忘れずに申請。
- Internet facing な ALB作成には、minimumで2コのPublic Subnet必要。
- RDS には、minimumで2コのPrivate Subnet必要。
