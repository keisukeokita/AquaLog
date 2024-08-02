■サービス概要
AquaLogは、水族館の情報をリアルタイムで共有し、写真の整理や、来館履歴の管理を簡単にすることで、水族館好きがより快適に楽しめるサービスです。

■ このサービスへの思い・作りたい理由
私自身、水族館に行くことが好きで、何度も訪れていますが、情報の取得や写真の整理、来館記録の管理に不便を感じていました。そこで、これらの課題を解決し、より快適に水族館を楽しめるサービスを考案しました。
AquaLogでは、水族館の情報をユーザー同士がリアルタイムで共有できる機能や、写真を水族館ごとに整理できる機能、訪れた水族館の記録を簡単に管理できる機能を実装することで、水族館好きの方が水族館に行く前や行った後でも楽しめるようなサービスにしていきたいと考えています。

■ ユーザー層について
ユーザー層：水族館を頻繁に訪れる人
理由：水族館内だけでなく、訪れる前や後でも楽しめるアプリがあれば、水族館好きの人がもっと楽しめると思ったからです。

■サービスの利用イメージ
ユーザーがメインで使う機能は「投稿機能」「My図鑑機能」「Myマップ機能」の３つです。
投稿機能を使う事で、水族館の公式サイトなどでは取得できない情報（例えば、混雑状況や、餌やりの時間、イベントの時間、生物に関する情報など）を、気軽にユーザー同士で情報を共有し合い最短で欲しい情報を得ることができます。
My図鑑機能では、水族館で撮った生き物の写真を、水族館ごとに図鑑のように管理ができるため、自分だけのオリジナルな水族館体験を詳細に記録することできますし、記録を通じて水族館や生物に関する知識を深めることができます。
Myマップ機能では、来館したことのある水族館とそうでない水族館を一目で判別できます。「行ったことのない水族館を把握したい」というユーザーにとっては、水族館を調べる時間を無くせますし、「全国の水族館を回りたい」というユーザーにとっては、達成感を感じることができます。

■ ユーザーの獲得について
SNSを活用して、アプリの宣伝を行う。

■ サービスの差別化ポイント・推しポイント
撮った写真を図鑑のように管理ができることが一番のポイントです。
自分の撮った写真を図鑑のように管理することで、単に写真を見返すよりも楽しめますし、他のユーザーの図鑑も閲覧できるので、行ったことのない水族館への興味が増しワクワク感が味わえます。

■ 機能候補
**MVPリリース時に作っていたいもの：**

**会員登録、ログイン機能**
　ユーザー名、メールアドレス、パスワードでのアカウント登録
　メール認証による会員登録の完了
　パスワード再設定機能

**投稿機能**
　投稿の種類、水族館名、画像や動画、本文の投稿
　投稿の種類、水族館名、本文での絞り込み
　投稿に対するいいね、コメント機能

**図鑑機能**
　水族館名での画像アップロードと保存
　図鑑の画像の名前、メモの記入機能

**地図機能**
　日本地図の表示と全国の水族館をマークできる機能
　地図の拡大縮小
　行ったことのある水族館をタップで色が変わる機能

**お問い合わせ機能**
　名前、メールアドレス、お問い合わせタイトル、お問い合わせ内容の入力
　入力内容の確認後の送信

**本リリースまでに作っていたいもの：**

**会員登録、ログイン機能**
　利用規約とプライバシーポリシーへの同意機能

**掲示板投稿機能**
　コメントのメンション機能
　いいねやコメントに対する通知機能

**図鑑機能**
　図鑑の水族館名、画像の名前での絞り込み機能
　ユーザー名、ユーザーのアイコン画像の変更機能

**地図機能**
　行った水族館と行っていない水族館の判別機能の強化

**お問い合わせ機能**
　お問い合わせに対する自動返信機能
　お問い合わせ内容の履歴管理機能

■ 機能の実装方針予定 **（サイトなどで調べて、「これで実装できるかな？」くらいのレベルです。）**
**ユーザー認証機能**
　　ログイン・新規会員登録機能：Devise
　　パスワードリセット機能：Devise
　　メールアドレス認証機能：Devise

**投稿機能**
　　絞り込み機能（基本は、登録されている情報をユーザーが選択する）： Ransack（検索機能）、Stimulus Autocomplete（オートコンプリート）、JavaScript（動的更新）
　　画像・動画のアップロード：CarrierWave
　　画像リサイズ機能：MiniMagick
　　いいね、コメント機能： Ajax（非同期通信）、WebSockets（Action Cable）
　　
**図鑑機能**
　　絞り込み機能（基本は、登録されている情報をユーザーが選択する）： Ransack（検索機能）、StimulusAutocomplet（オートコンプリート）、JavaScript（動的更新）
　　画像アップロード：CarrierWave
　　画像リサイズ機能：MiniMagick
　　図鑑の詳細編集機能：JavaScript（インライン編集）、Ajax（非同期通信）

**地図機能**
　　地図の表示と操作：日本地図に水族館だけが表示されているようなシンプルな地図にしたいと思っていますが、実装の方法が分かっておらず未定です。

**デプロイ後の画像保存**
　　CarrierWave、ストレージ（Amazon S3）

**コンポーメントデザイン**
　　Bootstrap

**日本語化対応**
　　i18n

## 画面遷移図のURL
https://www.figma.com/board/3lrKZVlBvT3HxOC0wcaUiT/AquaLog%EF%BC%88%E7%94%BB%E9%9D%A2%E9%81%B7%E7%A7%BB%E5%9B%B3%E3%83%BB%E3%83%A6%E3%83%BC%E3%82%B6%E3%83%BC%E3%83%95%E3%83%AD%E3%83%BC%EF%BC%89?node-id=0-1&t=RQjQS3HjOE0YwcaM-1

## UIのURL
https://www.figma.com/design/hreL7WcaUHmqdwgBUIn89L/AquaLog%EF%BC%88UI%EF%BC%89?node-id=0-1&t=fMiTfdDdP17hD2zP-1