名前: Breez ポイントオブセール

説明: Breez POS を使用してビットコインを受け入れるためのガイド

---

![カバー](assets/cover.jpeg)

# Breez ポイントオブセール

_このテキストは Breez のドキュメンテーションウェブサイトから取得されています: https://doc.breez.technology/How-to-Get-Started-with-Breez-POS.html_

## Breez POS とは何ですか？

**Breez** は、フルサービスの非保管型ライトニングアプリです。以下に詳細を説明します:

- **ライトニング** は、トランザクション時間を数分から数ミリ秒に、トランザクション手数料を数ドルから数セント以下に短縮するビットコインの支払いネットワークです。ライトニングは、ビットコインをデジタル通貨に変えながら、ビットコインの優れた特性をすべて保持します。
- **非保管型** とは、Breez がユーザーのお金を保有しないことを意味します。多くのライトニングアプリは、ユーザーのお金を保有します。つまり、ビットコインの銀行のようなものです。Breez のような非保管型アプリでは、すべてのユーザーが自分自身の銀行となります。
- **フルサービス** とは、Breez がほとんどの技術的な操作を自動的にバックグラウンドで処理することを意味します。チャネルの作成、インバウンドの流動性、ルーティングなどは、裏側で行われます。（ただし、Breez はオープンソースなので、技術の監査に興味がある方は自由に行うことができます！）

**Breez POS** は、ポイントオブセールモードの略称です。つまり、Breez はビジネスや商店がライトニング支払いを受け入れるためのデジタルなレジのような役割を果たします（ビットコインのデジタル版の革財布や次世代のポッドキャストプレーヤーのような「標準」モードもあります）。では、ビジネスのために Breez をライトニングレジとして設定する方法を見てみましょう。

## Breez の始め方

1. 最初のステップは、アプリをダウンロードすることです。Android と iOS 用のアプリが利用可能です（TestFlight をインストールし、デバイスからリンクをクリックしてください）。
2. Breez は自動的に Google Drive、iCloud、または任意の WebDav サーバーにバックアップすることができます。
   > 各デバイスは独自のライトニングノードを実行します。POS モードを複数のデバイスで実行することができますが、残高は別々になります。
3. アプリを開いた状態で、左上のアイコンをクリックしてポイントオブセールモードを見つけます。

## POS の設定

1. 左上のアイコンをクリックし、ポイントオブセール > POS 設定をクリックします。

### マネージャーパスワード

POS 設定では、マネージャーパスワードを作成するオプションがあります。マネージャーパスワードを設定すると、Breez アプリからの出金が承認なしに不可能になります。販売スタッフはデバイスからの支払いのみを受け取ることができます。このオプションを使用する場合、Breez のバックアップへのアクセスを制限することも検討してください。外部の WebDav アカウント（例: Nextcloud）を使用することをおすすめします。

### 商品リスト

商品リストは、販売用の商品とその価格のカタログです。商品をリストに追加する方法は2つあります:

- 1つずつ商品を入力するには、メインの POS ビューの上部にある「商品」をクリックし、右下の「+」マークをクリックします。ここで、1つの商品の種類の名前、価格（選択した通貨の等価表示）、SKU（その商品の一意の内部識別子、オプション）を入力できます。
- 一度に多くのアイテムを入力するには、左上の電卓アイコンをクリックし、ポイントオブセール>設定>POS設定をクリックし、アイテムリストの右側にある3つの点をクリックし、CSVからインポートをクリックします。これにより、事前に準備したアイテムの名前、価格、およびSKUが含まれるCSVファイルをインポートすることができます。
### フィアットディスプレイ

Breezはビットコインの送受信のみを行い、通常は小額の取引が多いため、合計金額は通常Satoshis（1 BTC = 100,000,000 sats）で表示されます。ただし、多くの商人は、購入の価値を現地の法定通貨で表示できることが実用的であると考えています。

メインのPOSビューでは、現在表示されている通貨が右側に表示されます（デフォルトはSAT）。表示する他の通貨のドロップダウンリストもあります。このドロップダウンリストから通貨を追加または削除するには、ポイントオブセール>設定>フィアット通貨をクリックします。その後、ドロップダウンメニューに表示する通貨をチェックし、省略する通貨をチェックを外します。

表示される値は、為替レートデータの信頼性のある情報源であるyadioから取得され、ほぼリアルタイムで更新されます。ただし、現在表示されている通貨の値に関係なく、支払い自体はビットコインです。

### 注文の請求

注文を作成するには、アイテムリストからアイテムを追加するか、キーパッドに金額を入力します。その後、メインのPOSビューの上部にある「請求」をクリックします。その後、お客様がライトニングアプリでスキャンできるQRコードが表示されます。また、デバイス上の別のアプリから直接共有したり、必要に応じてコピーして貼り付けることもできます。

そのコードをスキャンするか、共有/貼り付けられた請求書をクリックすると、お客様はライトニングアプリで請求書を表示し、すぐに支払いを行い取引を解決するオプションがあります。

Breezアプリの商人のデバイスで「支払い承認済み！」のアニメーションが表示されたら、お客様に領収書を生成するためにプリンターアイコンをクリックできます。Androidで領収書プリンターを使用するには、このドライバーを使用してみてください。過去の取引も取引画面から印刷することができます。

### 売上レポート

売上の日次/週次/月次レポートを表示するには（会計目的など）、左上のアイコンをクリックし、次に「取引」をクリックします。レポートアイコンをクリックしてレポートを表示し、カレンダーアイコンをクリックして選択した日付範囲を変更します。

### 取引のエクスポート

Breezで受け取った支払いのリストを表示するには、左上のアイコンをクリックし、次に「取引」をクリックします。右上の3つの点をクリックし、CSV形式での受信支払いリストをエクスポートするには、「エクスポート」をクリックします。リストを特定の期間に制限するには、カレンダーアイコンをクリックして日付範囲を設定します。

### 領収書の印刷

販売の領収書を印刷するには、支払い確認ダイアログの右上にある印刷アイコンをクリックします。または、左上のアイコンをクリックし、次に「取引」をクリックします。印刷する販売を見つけ、開き、右上の印刷アイコンをクリックします。

> 注意：ポータブルな58mm / 80mm Bluetooth / USBサーマルプリンターで印刷するには、このドライバーを使用してください。

## もっと学びたいです

- ライトニングとBreezについての詳細は、[ブログ](https://breez.technology/blog)をご覧ください。
- アプリを最大限に活用し、一般的な操作を行うための技術的なヒントについては、[ドキュメンテーション](https://breez.technology/documentation)をご覧ください。
- 弊社のヘルプ文献で答えが見つからない場合は、[Telegram](https://t.me/breez_labs)でお問い合わせいただくか、[メール](mailto:support@breez.technology)でお問い合わせください。
- Breez POSモードのデモンストレーション動画を、ファンやユーザーが作成したものでご覧になりたい場合は、[こちら](https://www.youtube.com/watch?v=xxxx)が素晴らしい短い動画で、[こちら](https://www.youtube.com/watch?v=xxxx)がより詳細な長い動画です。