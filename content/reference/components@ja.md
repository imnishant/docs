---
$title: コンポーネント
---

[TOC]

AMP HTML ライブラリで提供されるコンポーネントは、次のように分類されます。

- **組み込みコンポーネント**: `amp-img` や `amp-pixel` のような、基本ライブラリに含まれるコンポーネント。
- **拡張コンポーネント**: 基本ライブラリを拡張するもので、カスタム要素としてドキュメントに明示的に含める必要のあるコンポーネント（例: `<script async custom-element="amp-audio" ...`）。
- **[試験運用コンポーネント](experimental.html)**: リリースされているが、まだ一般公開する前の段階にあるコンポーネント。

関連するカテゴリで使用可能なコンポーネントの一覧を以下に示します。

### 広告と分析

| コンポーネント | 説明 |
| --------- | ----------- |
| [`amp-ad`](components/amp-ad.html) | 広告を表示するコンテナです。|
| [`amp-ad-exit`](components/amp-ad-exit.html) | A4A（AMP for Ads）の広告を終了する動作を提供します（設定可能）。|
| [`amp-analytics`](components/amp-analytics.html) | AMP ドキュメントからアナリティクス データを収集します。|
| [`amp-auto-ads`](components/amp-auto-ads.html) | リモートで提供される設定ファイルを使用して、AMP ページに広告を動的に挿入します。|
| [`amp-call-tracking`](components/amp-call-tracking.html) | ハイパーリンク内の電話番号を動的に置き換えて、コール トラッキングを有効にします。|
| [`amp-experiment`](components/amp-experiment.html) | AMP ドキュメントのユーザー エクスペリエンス テストを行うために使用できます。|
| [`amp-pixel`](components/amp-pixel.html) | ページビューをカウントするトラッキング ピクセルです。|
| [`amp-sticky-ad`](components/amp-sticky-ad.html) | ページの下部に広告コンテンツを表示して貼り付けることができます。|

### 動的コンテンツ

| コンポーネント | 説明 |
| --------- | ----------- |
| [`amp-access-laterpay`](components/amp-access-laterpay.html) | このコンポーネントにより、サイト運営者は [LaterPay](https://www.laterpay.net/) マイクロペイメント プラットフォームと簡単に統合できます。
| [`amp-access`](components/amp-access.html) | AMP ペイウォールとサブスクリプションのサポートを提供します。|
| [`amp-bind`](components/amp-bind.html) | データ バインディングや JS に似た単純な式を使用して、ユーザーの操作やデータの変更に応じた要素の変更を可能にします。|
| [`amp-byside-content`](components/amp-byside-content.html) | [BySide サービス](http://www.byside.com/)の動的コンテンツを表示します。|
| [`amp-consent`](components/amp-consent.html) | ユーザー インターフェース コントロールを通じて、ユーザーの同意を収集、保存する機能を提供します。|
| [`amp-date-picker`](components/amp-date-picker.html) | 日付を選択するためのカレンダー ウィジェットを提供します。|
| [`amp-form`](components/amp-form.html) | フォームのサポートを提供します。|
| [`amp-geo`](components/amp-geo.html) | 国単位のおおよその位置情報を把握するためのインターフェースを提供します。|
| [`amp-gist`](components/amp-gist.html) | [GitHub Gist](https://gist.github.com/) を表示します。|
| [`amp-install-serviceworker`](components/amp-install-serviceworker.html) | ServiceWorker をインストールします。|
| [`amp-list`](components/amp-list.html) | データを動的にダウンロードし、テンプレートを使用してリスト項目を作成します。|
| [`amp-live-list`](components/amp-live-list.html) | コンテンツの表示と更新をライブで行えるようにします。|
| [`amp-mustache`](components/amp-mustache.html) | [`Mustache.js`](https://github.com/janl/mustache.js/) テンプレートのレンダリングを可能にします。|
| [`amp-next-page`](components/amp-next-page.html) | ユーザーにおすすめする関連ドキュメントを動的に読み込みます。|
| [`amp-selector`](components/amp-selector.html) | オプションのメニューを表示して、ユーザーに選択を求めるコントロールを表示します。|
| [`amp-user-notification`](components/amp-user-notification.html) | 非表示に切り替えることが可能な通知をユーザーに表示します。|
| [`amp-web-push`](components/amp-web-push.html) | ユーザーが[ウェブプッシュ通知](https://developers.google.com/web/fundamentals/engage-and-retain/push-notifications/)を受け取れるようにします。|

### レイアウト

| コンポーネント | 説明 |
| --------- | ----------- |
| [`amp-accordion`](components/amp-accordion.html) | 閲覧者がコンテンツの概要を一目で把握し、選択した任意のセクションにジャンプできるようにします。|
| [`amp-app-banner`](components/amp-app-banner.html) | アプリのインストールを促すフレーズが表示されたクロスプラットフォームの固定位置バナー用ラッパーと最小限の UI です。|
| [`amp-carousel`](components/amp-carousel.html) | 横軸に沿って複数の類似コンテンツを表示します。|
| [`amp-fx-flying-carpet`](components/amp-fx-flying-carpet.html) | 子画面を固有の全画面スクロール コンテナにラップして、ビューポート全体を占めることなく全画面広告を表示できるようにします。|
| [`amp-fx-collection`](components/amp-fx-collection.html) | パララックスなど、一連のプリセットの視覚効果を提供します。|
| [`amp-iframe`](components/amp-iframe.html) | iframe を表示します。|
| [`amp-image-lightbox`](components/amp-image-lightbox.html) | 指定された画像に対してライトボックス効果を提供します。|
| [`amp-layout`](components/amp-layout.html) | 任意の要素に AMP の便利な[レイアウト](https://www.ampproject.org/ja/docs/guides/responsive/control_layout#the-layout-attribute)機能を適用する、汎用的で多目的なコンテナ要素を提供します。|
| [`amp-lightbox`](components/amp-lightbox.html) | フルビューポートの「ライトボックス」モーダルで要素を表示します。|
| [`amp-lightbox-gallery`](components/amp-lightbox-gallery.html) | 「ライトボックス」エクスペリエンスを提供します。ユーザーの操作に応じて、ユーザー インターフェース コンポーネントがビューポート全体に拡大されます。ユーザーがビューポートを閉じるまでその状態が維持されます。|
| [`amp-position-observer`](components/amp-position-observer.html) | ユーザーがスクロールするときのビューポート内の要素の位置を監視し、他のコンポーネントとともに使用できるイベントをディスパッチします。|
| [`amp-sidebar`](components/amp-sidebar.html) | ナビゲーション、リンク、ボタン、メニューなど、一時的なアクセスを意図したメタコンテンツを表示できます。|


### メディア

| コンポーネント | 説明 |
| --------- | ----------- |
| [`amp-3d-gltf`](components/amp-3d-gltf.html) | GL Transmission Format（gITF）の 3D モデルを表示します。|
| [`amp-3q-player`](components/amp-3q-player.html) | [3Q SDN](https://www.3qsdn.com) の動画を埋め込みます。|
| [`amp-anim`](components/amp-anim.html) | アニメーション画像（通常は GIF）を管理します。|
| [`amp-apester-media`](components/amp-apester-media.html) | [Apester](https://apester.com/) スマート ユニットを表示します。|
| [`amp-audio`](components/amp-audio.html) | HTML5 の `audio` タグを置き換えます。|
| [`amp-bodymovin-animation`](components/amp-bodymovin-animation.html) | [AirBnB Bodymovin アニメーション プレーヤー](http://airbnb.io/lottie/)を表示します。このツールを使うと、[Adobe After Effects](https://www.adobe.com/products/aftereffects.html) で生成した JSON からアニメーションをレンダリングできます。|
| [`amp-brid-player`](components/amp-brid-player.html) | [Brid.tv](https://www.brid.tv/) プレーヤーを表示します。|
| [`amp-brightcove`](components/amp-brightcove.html) | Brightcove [Video Cloud](https://www.brightcove.com/en/online-video-platform) または [Perform](https://www.brightcove.com/en/perform) プレーヤーを表示します。|
| [`amp-dailymotion`](components/amp-dailymotion.html) | [Dailymotion](https://www.dailymotion.com) の動画を表示します。|
| [`amp-google-vrview-image`](components/amp-google-vrview-image) | VR イメージを表示します。|
| [`amp-hulu`](components/amp-hulu.html) | [Hulu](http://www.hulu.com/) のシンプルな埋め込み動画を表示します。|
| [`amp-ima-video`](components/amp-ima-video.html) | [IMA SDK](https://developers.google.com/interactive-media-ads/docs/sdks/html5/) に統合されたインストリーム動画広告用の動画プレーヤーを埋め込みます。|
| [`amp-img`](components/amp-img.html) | HTML5 の `img` タグを置き換えます。|
| [`amp-imgur`](components/amp-imgur.html)  | [Imgur](http://imgur.com/) の投稿を表示します。|
| [`amp-izlesene`](components/amp-izlesene.html)  | [Izlesene](https://www.izlesene.com/) の動画を表示します。|
| [`amp-jwplayer`](components/amp-jwplayer.html) | クラウドでホストされる [JW Player](https://www.jwplayer.com/) を表示します。|
| [`amp-kaltura-player`](components/amp-kaltura-player.html) | [Kaltura 動画プラットフォーム](https://corp.kaltura.com/)で使用される Kaltura Player を表示します。|
| [`amp-nexxtv-player`](components/amp-nexxtv-player.html) | nexxOMNIA プラットフォームからのメディア ストリームを表示します。|
| [`amp-o2-player`](components/amp-o2-player.html) | [AOL O2Player](http://on.aol.com/) を表示します。|
| [`amp-ooyala-player`](components/amp-ooyala-player.html) | [Ooyala](https://www.ooyala.com/) の動画を表示します。|
| [`amp-playbuzz`](components/amp-playbuzz.html) | [Playbuzz](http://www.playbuzz.com/) の任意のコンテンツ（リスティクルや投票など）を表示します。|
| [`amp-reach-player`](components/amp-reach-player.html) | [Beachfront Reach](https://beachfrontreach.com/) の動画プレーヤーを表示します。|
| [`amp-soundcloud`](components/amp-soundcloud.html) | [Soundcloud](https://soundcloud.com/) のクリップを再生します。|
| [`amp-springboard-player`](components/amp-springboard-player.html) | [Springboard Platform](http://publishers.springboardplatform.com/users/login) の動画プレーヤーを表示します。|
| [`amp-video`](components/amp-video.html) | HTML5 の `video` タグを置き換えます。|
| [`amp-vimeo`](components/amp-vimeo.html) | [Vimeo](https://vimeo.com/) の動画を表示します。|
| [`amp-wistia-player`](components/amp-wistia-player.html) | [Wistia](https://wistia.com/) の動画を表示します。|
| [`amp-youtube`](components/amp-youtube.html) | [YouTube](https://www.youtube.com/) の動画を表示します。|

### プレゼンテーション

| コンポーネント | 説明 |
| --------- | ----------- |
| [`amp-animation`](components/amp-animation.html) | アニメーションを定義して表示します。|
| [`amp-dynamic-css-classes`](components/amp-dynamic-css-classes.html) | CSS の動的なクラス名を HTML 要素にいくつか追加します。|
| [`amp-fit-text`](components/amp-fit-text.html) | 任意のスペースにコンテンツが収まるようにフォント サイズを拡大または縮小します。|
| [`amp-font`](components/amp-font.html) | カスタム フォントの読み込みをトリガーし、処理を監視します。|
| [`amp-mathml`](components/amp-mathml.html) | [MathML の数式](https://www.w3.org/Math/)を表示します。|
| [`amp-story`](components/amp-story.html) | 訴求力のあるビジュアルを使ったストーリーテリングを提供します。|
| [`amp-timeago`](components/amp-timeago.html) | 日付と時刻の形式に「*time ago*」の記述を加え（「3 時間前」など）、大まかなタイムスタンプを提供します。|
| [`amp-viz-vega`](components/amp-viz-vega.html) | [Vega](https://vega.github.io/vega/) のデータ可視化の文法を使用して作成したビジュアル要素を表示します。|


### ソーシャル

| コンポーネント | 説明 |
| --------- | ----------- |
| [`amp-beopinion`](components/amp-beopinion.html) | [BeOpinion](https://beopinion.com/) のコンテンツを埋め込みます。|
| [`amp-addthis`](components/amp-addthis.html) | [AddThis](https://www.addthis.com/) の埋め込みウェブサイト ツールを表示します。|
| [`amp-facebook-comments`](components/amp-facebook-comments.html) | Facebook のコメント プラグインを埋め込みます。|
| [`amp-facebook-like`](components/amp-facebook-like.html) | Facebook のいいね！ボタン プラグインを埋め込みます。|
| [`amp-facebook-page`](components/amp-facebook-page.html) | [Facebook のページ プラグイン](https://developers.facebook.com/docs/plugins/page-plugin)を埋め込みます。|
| [`amp-facebook`](components/amp-facebook.html) | Facebook の投稿や動画を表示します。|
| [`amp-gfycat`](components/amp-gfycat.html) | [Gfycat](https://gfycat.com) の動画 GIF を表示します。|
| [`amp-instagram`](components/amp-instagram.html) | Instagram の埋め込みを表示します。|
| [`amp-pinterest`](components/amp-pinterest.html) | Pinterest のウィジェットや Pin It ボタンを表示します。|
| [`amp-reddit`](components/amp-reddit.html) |  Reddit のコメントや投稿の埋め込みを表示します。|
| [`amp-riddle-quiz`](components/amp-riddle-quiz.html) |  [Riddle](https://www.riddle.com/) のコンテンツ（クイズ、リスト、アンケートなど）を表示します。|
| [`amp-social-share`](components/amp-social-share.html) | ソーシャル共有ボタンを表示します。|
| [`amp-twitter`](components/amp-twitter.html) | Twitter のツイートを表示します。|
| [`amp-vine`](components/amp-vine.html) | Vine の「Simple」スタイルの埋め込みを表示します。|
| [`amp-vk`](components/amp-vk.html) | [VK](https://vk.com/) の投稿またはアンケート ウィジェットを埋め込みます。|
 
