# ファイル紹介

このリポジトリには、通販価格・定期券・時間計測・文章処理・画像変換・ChatGPT連携などを試すための、単体HTMLの試作・検証用ページがまとめられています。現在のルート直下には、45個のHTMLページと、ライセンス・READMEなどの補助ファイルがあります。

GitHub Pagesで公開しているHTMLは、基本的に次の形式で開けます。

https://uni928.github.io/TestYou/ファイル名

index.html はファイル名を省略したURLでも開けます。

## 先に確認した注意点

- 現行READMEに掲載されているリンク先は、確認した実ファイルと対応しています。ただし、TestYou1 などの表示名はページの実タイトルを表していないため、下表ではファイル名と実装内容を基準に整理しています。
- index24.html〜index26.html は視覚障がい者向けの実験的なカメラデモです。画像の単純な変化を検出するものなので、歩行時の安全確認や障害物検出を保証するものではありません。
- index30.html・index31.html・index45.html はカメラ画像をOpenAI APIへ送信して説明を生成します。API利用料金、画像の取り扱い、通信環境を確認してから使用してください。
- index31.html と index45.html はURLの ?key= からAPIキーを受け取り、ブラウザ内へ保存します。APIキーがブラウザ履歴や共有URLなどに残る可能性があるため、キーを含むURLは共有しない方が安全です。
- URLに文章やアンケート内容を埋め込むページでは、URL自体に入力内容が含まれます。機密情報や個人情報をそのままURL化しないでください。

## ルート直下のHTML・ツール

| ファイル | 紹介 |
| --- | --- |
| [index.html](https://uni928.github.io/TestYou/index.html) | 商品名を入力し、楽天市場・Yahoo!ショッピングなどの通販価格を取得して、中央値や商品一覧を確認する価格チェックツールです。レビュー3以上での絞り込みに対応し、APIキーと結果をIndexedDBに保存します。 |
| [index2.html](https://uni928.github.io/TestYou/index2.html) | 1か月・3か月・6か月定期の価格を入力し、1か月定期と比べた節約額や月あたりの費用を確認する定期券比較ツールです。入力内容はIndexedDBから次回起動時に復元されます。 |
| [index3.html](https://uni928.github.io/TestYou/index3.html) | 文章をURLに圧縮して埋め込み、X・LINE・メールなどで共有するページ作成ツールです。HTML表示とプレーンテキスト表示に対応し、localStorageやIndexedDBには保存しません。 |
| [index4.html](https://uni928.github.io/TestYou/index4.html) | コードを貼り付けたり読み込んだりして、メソッド宣言と呼び出し箇所を解析するコードリーダーです。宣言から呼び出し元へジャンプし、履歴をたどれます。 |
| [index5.html](https://uni928.github.io/TestYou/index5.html) | 手作業で登録されたチェーン飲食店と、1人1000円以内になりやすいメニューから、10件の候補をランダム表示する飲食店ガチャです。価格は店舗・地域・時期で変わるため、実際の価格確認が必要です。 |
| [index6.html](https://uni928.github.io/TestYou/index6.html) | 通常の四則演算に加えて、複数の記憶ボタンを使える電卓です。記憶ボタンの編集と、IndexedDBによる設定保存に対応しています。 |
| [index7.html](https://uni928.github.io/TestYou/index7.html) | 右奥歯など、歯磨きする場所をボタン操作で順番に案内するページです。案内方法の選択内容をIndexedDBに保存し、次回も引き継ぎます。 |
| [index8.html](https://uni928.github.io/TestYou/index8.html) | 60秒間で、表示されたひらがなの左端と入力末尾を一致させて消していくゲームです。Enterキーやボタンで入力を確定し、消去数を競います。 |
| [index9.html](https://uni928.github.io/TestYou/index9.html) | index3.htmlと同系統のURLページ作成ツールです。プレーンテキストには通常の圧縮を使い、HTMLモードには別の短縮用圧縮処理を使う派生版です。 |
| [index10.html](https://uni928.github.io/TestYou/index10.html) | 「記憶開始」から「記憶終了」までの時間をセッションとして記録するカレンダー型の時間管理ツールです。日別・月別の合計、直近30日の中央値、履歴の確認・編集をIndexedDBで管理します。 |
| [index11.html](https://uni928.github.io/TestYou/index11.html) | あいさつ、レビュー、チャット・SNS、エラー文、コードなどのダミーテキストをカテゴリ別に確認し、ボタンでコピーできるギャラリーです。 |
| [index12.html](https://uni928.github.io/TestYou/index12.html) | 文章中から符号付きの数値を取り出し、足し算・引き算として計算する基本版のツールです。複数行や空白を含む入力に対応し、8桁日付を除外する派生版へのリンクもあります。 |
| [index13.html](https://uni928.github.io/TestYou/index13.html) | 単語を事前登録し、ランダムに出題してフリック入力を練習するツールです。内部で使用するフリック対応表も画面で確認できます。 |
| [index14.html](https://uni928.github.io/TestYou/index14.html) | index12.htmlの派生版です。数値を計算するときに、20240101のような8桁の日付を計算対象から除外し、式・結果・抽出一覧を表示します。 |
| [index15.html](https://uni928.github.io/TestYou/index15.html) | 文字列中の改行トークンを実際の改行へ変換し、逆方向にも戻せる改行変換ツールです。既定の「\n」のほか、<br>や「【改行】」などのカスタムトークン、リアルタイム変換、コピーに対応します。 |
| [index16.html](https://uni928.github.io/TestYou/index16.html) | 相手ごとのお金の貸し借りを、金額・メモ付きで記録する管理ツールです。正負の金額から人別合計と計算式を表示し、IndexedDB保存とJSONのエクスポート・インポートに対応します。 |
| [index17.html](https://uni928.github.io/TestYou/index17.html) | 100から開始し、現在値の0.95倍〜1.05倍の候補を毎ターン5つから選んで数を大きくしていくゲームです。巨大数表示、最大値の記録、0.90倍〜1.10倍になるハードモードを備えています。 |
| [index18.html](https://uni928.github.io/TestYou/index18.html) | 作業時間を積み上げて100時間達成を目指すタイマーです。開始・終了の操作をセッションとして保存し、履歴の編集・削除や合計時間の確認をIndexedDBで行います。 |
| [index19.html](https://uni928.github.io/TestYou/index19.html) | URLを入力してQRコードを生成するツールです。プリセットURL、PNG保存、画像データURLのコピーに対応し、入力URLそのものは外部サーバーへ送信せずブラウザ内で処理します。 |
| [index20.html](https://uni928.github.io/TestYou/index20.html) | HTML・JavaScriptを貼り付け、行番号付きエディタからiframeで実行するHTMLエラー・プレビューコンソールです。プレビュー、console.log、JavaScriptエラーを同時に確認できます。 |
| [index21.html](https://uni928.github.io/TestYou/index21.html) | 文章をUTF-8からBase64へ変換し、RGBピクセルに埋め込んだPNG画像へ変換するツールです。画像からの文章復元、PNG保存、復元用URLの作成に対応します。 |
| [index22.html](https://uni928.github.io/TestYou/index22.html) | よく使う質問やプロンプトを登録し、編集・追加・削除してChatGPTを開く質問ランチャーです。登録内容はIndexedDBに自動保存されます。 |
| [index23.html](https://uni928.github.io/TestYou/index23.html) | index22.htmlの派生版です。登録した質問内の「ここに文章を貼ってください」を一時的な差し替え文章で置換でき、通常のChatGPT起動と一時チャット起動を選べます。差し替え欄自体はIndexedDBに保存しません。 |
| [index24.html](https://uni928.github.io/TestYou/index24.html) | カメラ画像の明るさや模様の変化を基準値と比較し、壁が近づいた可能性を音声で知らせる実験的なデモです。画像は外部サーバーへ送信しませんが、壁以外の危険は検出できません。 |
| [index25.html](https://uni928.github.io/TestYou/index25.html) | カメラを足元の斜め前へ向け、通常の地面から明るさや白っぽい部分などが変化したときに音声で知らせる実験的なデモです。歩行時の安全装置ではありません。 |
| [index26.html](https://uni928.github.io/TestYou/index26.html) | 足元の映像を数フレーム前の状態と連続比較し、地面の色や白線などの変化を音声で知らせるデモです。単純な画像差分を使うため、段差・穴・人・車などを確実に検出するものではありません。 |
| [index27.html](https://uni928.github.io/TestYou/index27.html) | スマートフォンでの範囲選択を補助する入力ツールです。文章を貼り付け、カーソルより前または後ろを削除して、テキスト全体をコピーできます。 |
| [index28.html](https://uni928.github.io/TestYou/index28.html) | アンケートのタイトル・説明・質問をURLに埋め込み、回答用URLと回答結果の閲覧用URLを作成するツールです。単一選択、複数選択、自由記述、数値、5段階評価に対応し、サーバーを使わずにやり取りします。 |
| [index29.html](https://uni928.github.io/TestYou/index29.html) | index27.htmlと同系統のスマートフォン向けコピー補助ツールです。前後削除とコピーの操作ボタンを上部に集め、入力欄を広くしたレイアウトの派生版です。 |
| [index30.html](https://uni928.github.io/TestYou/index30.html) | カメラで撮影した周囲の画像をChatGPT APIへ送り、視覚障がい者向けに風景を日本語で説明して音声読み上げするページです。APIキーはIndexedDBに保存されます。 |
| [index31.html](https://uni928.github.io/TestYou/index31.html) | index30.htmlの道案内特化版です。左右・前方、距離、道幅、段差・横断歩道・障害物などを意識して、比較的安全な進行方向を案内するプロンプトを使います。?key=からAPIキーを受け取ってIndexedDBへ保存する機能もあります。 |
| [index32.html](https://uni928.github.io/TestYou/index32.html) | ZIPファイルを、パディングなしのBase64文字列からピクセルへ変換したPNG画像に埋め込み、逆方向にZIPへ復元するコンバータです。ドラッグ＆ドロップ、プレビュー、ダウンロードに対応します。 |
| [index33.html](https://uni928.github.io/TestYou/index33.html) | ZIPのバイト列をPNG8のインデックスカラー画像へ直接格納し、PNG8からZIPへ戻すバイナリコンバータです。Canvasに依存せず、PNGの生成・解析をブラウザ内で行います。 |
| [index34.html](https://uni928.github.io/TestYou/index34.html) | 「Uni928_」を先頭に付けたランダムパスワードを生成し、タイトル・URL・パスワードを一覧管理するツールです。コピー、並べ替え、IndexedDBのリアルタイム保存、JSONバックアップに対応します。 |
| [index35.html](https://uni928.github.io/TestYou/index35.html) | 名前・時刻・メッセージをチャット形式で記録する職員向けメッセージボードです。オフラインのIndexedDB保存に加えて、テキスト形式のエクスポート・インポートによるログ共有に対応します。 |
| [index36.html](https://uni928.github.io/TestYou/index36.html) | 漫画のタイトルと最大巻数を登録し、所持・未所持の巻を管理するコレクションツールです。状態はブラウザのIndexedDBへ自動保存されます。 |
| [index37.html](https://uni928.github.io/TestYou/index37.html) | 透明度がすべて255の画像のアルファチャンネルへ、見た目を大きく変えずに文章を埋め込むツールです。埋め込み済み画像のダウンロード、文章抽出、コピーに対応します。 |
| [index38.html](https://uni928.github.io/TestYou/index38.html) | index37.htmlのバージョン3.0.0相当の派生版です。アルファ値の差分テーブルやダミー値を使い、埋め込みパターンを調整し、容量表示も実効容量を考慮します。 |
| [index39.html](https://uni928.github.io/TestYou/index39.html) | 透明度がすべて255の画像へZIPファイルをアルファチャンネルで埋め込み、後から抽出するツールです。ZIPの理論上の最大サイズは2,097,151バイトとされています。 |
| [index40.html](https://uni928.github.io/TestYou/index40.html) | 「あなた」と「ChatGPT」の会話ログを貼り付け、検索語で絞り込むログ抽出ツールです。自分の発言だけを一覧にして、クリックした発言に対応するChatGPTの回答を左下のドックへ表示できます。 |
| [index41.html](https://uni928.github.io/TestYou/index41.html) | スパワールドを中心に、温泉・食事・休憩を組み合わせた宴会のモデルコースと、快適に過ごすためのコツを紹介する静的な案内ページです。営業時間・料金などは最新情報の確認が必要です。 |
| [index42.html](https://uni928.github.io/TestYou/index42.html) | 東京ディズニーランドへ12時に入園する混雑日を想定し、ショー・パレード・アトラクションを組み合わせた1日のモデルプランを紹介する静的な資料ページです。開催内容や時間は公式情報を確認してください。 |
| [index43.html](https://uni928.github.io/TestYou/index43.html) | 商品の価格・容量・アルコール度数から純アルコール量を計算し、1円あたりの純アルコール量が多い順に比較するツールです。商品名・店名の登録とIndexedDB保存に対応します。 |
| [index44.html](https://uni928.github.io/TestYou/index44.html) | 入力した文章を固定の添削依頼プロンプトへ組み込み、ブラウザ版ChatGPTの一時チャットを開くランチャーです。送信内容のプレビューとコピーにも対応します。 |
| [index45.html](https://uni928.github.io/TestYou/index45.html) | index31.htmlの速度優先版です。道案内用のAPI呼び出しに、より上位のモデルと優先サービス設定を使う構成になっています。APIキーのURL受け取り、IndexedDB保存、カメラ画像のAPI送信を含みます。 |

## ライセンス・補助ファイル

| ファイル | 紹介 |
| --- | --- |
| [LICENSE](https://github.com/uni928/TestYou/blob/main/LICENSE) | リポジトリ内ソフトウェアに適用するMITライセンスです。 |
| [OUTPUT-RIGHTS.md](https://github.com/uni928/TestYou/blob/main/OUTPUT-RIGHTS.md) | MITライセンスに追加の制限を設けるものではなく、本リポジトリのツールで利用者が作成した成果物について、開発者が成果物自体の権利を主張しない意向を補足する文書です。第三者素材や契約上の権利は別途確認が必要です。 |
| [README.md](https://github.com/uni928/TestYou/blob/main/README.md) | TestYouで公開している主要なテスト用HTMLへのリンクと、このリポジトリをテスト用途として扱う旨を記載した現在のREADMEです。 |
| [_config.yml](https://github.com/uni928/TestYou/blob/main/_config.yml) | GitHub Pages向けのJekyll設定です。サイトマップ用プラグインを指定しています。 |

## 利用上の注意

ソースコードはLICENSEのMITライセンスに従います。ツールで作成した文章・画像・コードなどの成果物についてはOUTPUT-RIGHTS.mdを確認してください。入力内容や出力内容に第三者の著作権・商標権・プライバシー権などが関係する場合は、利用者自身で権利関係を確認してください。

APIキーを扱うページは、キーをブラウザのIndexedDBへ保存するだけで、暗号化やサーバー側の安全な保管を提供するものではありません。特にURLのクエリパラメータへキーを含める場合は、履歴・共有・ログへの露出に注意してください。

カメラ、ChatGPT API、外部ライブラリ、価格情報、施設情報、イベント情報などを使うページは、通信先・料金・情報の更新状況を確認してから利用してください。視覚支援ページの検出結果やAIによる案内は、正式な安全設備・医療機器・専門家の判断の代わりにはなりません。

URL共有型のページ作成・アンケート・画像エンコーダでは、入力データがURLや生成画像に埋め込まれます。URLやファイルを受け取った人が内容を閲覧できるため、機密情報の共有には使用しないでください。
