## 自動販売機（データ構造と各種処理）のミニレポート
### Q5-1. 自動販売機の商品データついて説明せよ。
* データ構造（各項目とその説明）
* 商品の各種データが、商品を定義する番号である「id」、名前を意味する「name」、価格を意味する「price」、残数を意味する「stock」に分けられており、これらが連想配列の配列として定義されている。
*  連想配列の配列として定義するメリット
*  for文でまとめて処理をする際に便利。実際に、item.id、item.nameと、目当ての変数を簡単に呼び出せた。
### Q5-2. showItemListの処理内容について説明せよ。
* 配列の繰り返し処理
* for文を使って、items配列のすべてのデータを順番に処理している。
* 連想配列の参照方法
* item.id、item.name、item.price、item.stockといったように、ドットとキーを組み合わせることで参照している。
### Q5-3. buyItemの処理内容について説明せよ。
* 商品購入の可否判定
* 入力された商品番号に一致する商品をitems配列から探し、stockの値が1以上であれば購入でき、0である場合は「在庫切れ」と表示する。
* 商品在庫を減らす処理
* 商品を発見し、在庫があった場合には--でstockの値を-1する。
* 商品番号のエラー処理
* 商品番号noに該当する商品がitems配列に存在しない場合には、item === nullによって判定し、trueを返した場合には「存在しません」と表示する。
### Q5-4. プログラムの考察
* データ構造について
* 商品情報を連想配列を使って定義したことによって、簡単に変数を呼び出せるようになっている。
* また、新たに項目を追加する際も、連想配列に入れるだけで簡単に管理することができる。
* 商品一覧表示と購入処理を関数化したメリット
* 関数にすることによって、同じ処理を何度も呼び出す際に役に立つ。
### Q5-5. 感想
* 今回の課題で苦労したこと
*item.id、items[i].idといった似たようなドット記法の入力を多く行ったため、途中で混乱して書き直すことがとても多く、苦戦した。
また、===やnullといった初めて扱うような表現も多かったため、手探りでプログラムを打ち込んでいるような気持ちになり終始不安だった。
連想関数も今回初めて扱ったが、ある程度扱いに慣れるまではfor文で使うのがとても難しく、自分ではあっているつもりなのにエラーが消えないのがとても苦しかった。
* 演習を通して理解できたこと
* letで変数を定義するという基本の事から、変数関数の運用方法、キーと値のペアでデータを管理するということも理解できた。
* この自動販売機プログラムの追加機能や課題など
* 購入者の残金を登録して、既に登録してある価格を参照して、残金があるだけ買えるといったプログラムにできたらより面白そうだなと感じた
