# NCMBiOSUser
ニフティクラウド mobile backendを使ったユーザログイン、ログアウトのデモアプリです。

## サンプルアプリケーション概要

ニフティクラウド mobile backendのデータストアを使用した簡単なTodoアプリです。Todoの一覧、登録、編集、削除が可能です。
**会員登録機能**を使って認証を行っています。 Swift 1.2で記述しています。

## 事前知識

- CocoaPodsの利用の仕方やブリッジヘッダーの設定の仕方。
- [クイックスタート](http://mb.cloud.nifty.com/doc/quickstart_ios.html)の内容。

## 動作確認環境

- OS X Yosemite Version 10.10.4 (14E46)
- Xcode Version 6.4 (6E35b)
- ruby 2.1.5p273 (2014-11-13 revision 48405) [x86_64-darwin14.0]
- cocoppods 0.37.2


## 注意事項

Podfileは次のように設定してください。2015年7月14日時点では `use_frameworks!` オプションは利用できませんので注意してください。

### Podfile

```
platform :ios, '8.3'

inhibit_all_warnings!

# # 2015/07/14時点では、このオプションを指定するとビルドエラーが発生します。
# use_frameworks!

pod 'NCMB', :git => 'https://github.com/NIFTYCloud-mbaas/ncmb_ios.git'
```

### APIキー

`Settings.swift` の次の箇所をご自分の環境に合わせて書き換えてください。

```swift
/// アプリケーションキー
let kNCMBiOSApplicationKey = "YOUR_APPLICATION_KEY"
/// クライアントキー
let kNCMBiOSClientKey = "YOUR_CLIENT_KEY"
```

## 関連情報

- [ニフティクラウド mobile backend](http://mb.cloud.nifty.com/)

データストア関連
- [機能ガイド : データストア | ニフティクラウド mobile backend](http://mb.cloud.nifty.com/doc/current/fnguide/datastore.html)
- [ダッシュボードの使い方 : データストア | ニフティクラウド mobile backend](http://mb.cloud.nifty.com/doc/current/dashboard/datastore.html)
- [SDKガイド (iOS) : オブジェクト操作 | ニフティクラウド mobile backend](http://mb.cloud.nifty.com/doc/current/sdkguide/ios/datastore.html)
- [SDKガイド (iOS) : クエリの使い方 | ニフティクラウド mobile backend](http://mb.cloud.nifty.com/doc/current/sdkguide/ios/query.html)
- [SDKガイド (iOS) : サブクラス | ニフティクラウド mobile backend](http://mb.cloud.nifty.com/doc/current/sdkguide/ios/subclass.html)

会員登録関連
- [機能ガイド : 会員管理 | ニフティクラウド mobile backend](http://mb.cloud.nifty.com/doc/current/fnguide/user.html)
- [ダッシュボードの使い方 : 会員管理 | ニフティクラウド mobile backend](http://mb.cloud.nifty.com/doc/current/dashboard/user.html)
- [SDKガイド (iOS) : 会員管理 | ニフティクラウド mobile backend](http://mb.cloud.nifty.com/doc/current/sdkguide/ios/user.html)

類似のサンプルアプリケーション
- [moongift/NCMBiOSTodo](https://github.com/moongift/NCMBiOSTodo)
- [moongift/NCMBiOSFaceook](https://github.com/moongift/NCMBiOSFaceook  )
- [moongift/NCMBiOSTwitter](https://github.com/moongift/NCMBiOSTwitter)
- [moongift/NCMBiOSGoogle](https://github.com/moongift/NCMBiOSGoogle)

## ライセンス

The MIT License (MIT)
