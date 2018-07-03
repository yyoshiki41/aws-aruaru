# AWS あるある

## What is this?

個人的なAWS周りで、やってしまったこと（あるある）のメモ

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
