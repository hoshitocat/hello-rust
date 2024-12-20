# Hello Rust

- Rustを学習するために作成

# どうしてRustか？

作者がGraydon Hoareが作ったプログラミング言語であり、その誕生の経緯や思想がすごいと思った
- メモリ安全性
- 並列処理

そして、何よりハイパフォーマンスであることが良いと思った理由
簡単にGPTで経緯について調べた結果がよかった

<details>
<summary>GPTのアウトプット結果</summary>

Rustは、2006年にMozillaのエンジニアであるGraydon Hoareによって開発が始まりました。当初は個人的なプロジェクトとしてスタートしましたが、その後Mozillaがプロジェクトを支援し、公式な開発が進められるようになりました。Rustの誕生と進化の背景には、高性能なプログラミング言語における安全性と開発効率の両立という目標がありました。

Rust誕生の背景と目的

1. 安全性への課題
    - CやC++などの従来のシステムプログラミング言語は、柔軟性や性能面では優れていましたが、メモリ安全性に関する問題が頻繁に発生していました（例: バッファオーバーフロー、ダングリングポインタ、データ競合）。
    - Graydon Hoareは、これらの問題を解決しつつ、パフォーマンスを損なわない新しい言語を作りたいと考え、Rustの開発を開始しました。
2. 並列処理の重要性
    - マルチコアプロセッサが一般化する中で、スレッドセーフな並列処理を簡単かつ安全に記述できる言語が必要とされていました。
3. Mozillaの目的
    - Mozillaは、Rustを利用してFirefoxのブラウザエンジンの次世代版を構築し、ブラウザの安全性やパフォーマンスを向上させることを目指していました。このプロジェクトは後にServoとして知られるようになります。

Rustの歴史的な出来事

2006年: 開発の開始

- Graydon HoareがRustの開発を始める。
- 名前の由来は、 **錆びた（Rusty）金属** と、 **robust(堅牢)** という言葉にかけたもの。

2009年: Mozillaによる支援

- Mozillaがプロジェクトに関心を持ち、公式にRustの開発を支援開始。
- 開発チームが拡大し、本格的な言語設計が進む。

2010年: 初期のコンパイラ

- Rustの初期のコンパイラはOCamlで実装されていた。この段階では、言語としてまだ未成熟だったが、基本的な概念が形作られていった。

2011年: LLVMへの移行

- コンパイラがLLVMバックエンドを使用するようになり、Rustの性能が大幅に向上。
- この時点でRustは実用に耐えうる性能を持つようになる。

2012年: バージョン0.1公開

- 初めて公式にRustの公開バージョンがリリースされる。

2015年: Rust 1.0 リリース

- Rustの最初の安定版であるバージョン1.0がリリースされる。
- 安定性を重視した開発ポリシーが導入され、「1.0以降は後方互換性を維持する」という方針が打ち出された。

2016年以降: 成長期

- Rustは「システムプログラミングだけでなく、Webアプリケーションやツール開発でも使える」という認識が広まり、エコシステムが急速に成長。
- 開発者満足度調査（Stack Overflow Developer Survey）で、**「最も愛される言語」**に連続して選出されるようになる。

2020年: Mozillaからの分離

- Mozillaのリストラの影響で、Rustの開発チーム（Rust Core Team）は独立し、Rust Foundationを設立。
- この独立により、Rustはより広範なコミュニティベースのプロジェクトとなる。

Rustの設計思想

1. ゼロコスト抽象化
    - 高レベルなプログラミング構造を提供しつつ、パフォーマンスに悪影響を与えない設計。
2. 安全性の保証
    - 所有権モデルと借用チェッカーにより、メモリの誤用をコンパイル時に防止。
3. 表現力の高い型システム
    - ジェネリクスやトレイトによる柔軟なコード設計が可能。
4. 並列性の簡易化
    - スレッドセーフなコードを書くための言語的なサポート。

Rustの影響

Rustは現在、システムプログラミング言語の分野だけでなく、Web開発（例: Rocket）、ゲームエンジン、ブロックチェーン開発、さらには組み込みシステムなど、多岐にわたる用途で使用されています。また、CやC++の代替としての期待も高く、多くのプロジェクトで採用されています。

もしRustの具体的な技術や特徴についてさらに知りたい場合は、詳しく解説しますので気軽に聞いてください！

</details>

# 自分の目指すべきところ

2024/11/24

Rustをキャッチアップしつつ、OSSのRustで書かれたPJにContributeしたい
そして、転職する段階でRustを使って働ける環境にいきたいと思う
今の所どういう会社があるのか調べていないが、今は詳細は気にしないこととする

勉強してみてやはりしっくりこないとかもあると思うから、そこまで深く考えない。

# キャッチアップのマイルストーン

- November
    - 書籍を一冊やりきる
        - ゼロから学ぶRust（システムプログラミングの基礎から線形型システムまで）
            - おそらくざっくり構文はキャッチアップできると思う
    - LeetCodeでEasyレベルの問題を10問以上やる
        - GoだったらサクッとかけそうなものをRustでやりきる
        - Middleとかだとそもそもむずいものがあるので、それは対象外とした（本質はRustのキャッチアップのため）
- December
    - OSSのプロジェクトを調べる
        - 自分にとって刺激的なプロジェクトをやりたい
        - できれば未来に可能性を感じているWASM系に関われると良いと思ってはいる
            - エッジコンピューティングの未来
            - めちゃ流行っているようにみえるw
            - CloudFlareがホットにみえる
            - 実際この辺の解像度は低いので信憑性に薄く調査をする必要があるという点でもキャッチアップしていきたいと思っている
- 今年中にOSSにContributeするところまではいきたいと思っている

# 実行環境

compose.ymlがあるのでそれで実行環境を作成
