# テスト自動化パタン言語 オーバービュー

<object type="image/svg+xml" data="patterns.svg"></object>

# 自動化開始のためのパターン
## 求む！英雄
### 文脈
現場で、自動化しようという意識はあり、改善のアイデアもあり、世の中のツールを使用すると効率が良くなると感じている。「ないものは作れ」で自力で作成することがあたりまえになっている。

### 問題
* 世にあるツールと同程度もしくは程度の低いツールを作成するために、リソースを浪費している。リソースの制約により自動化が進まない。
* 世の中には便利なツールがあるにもかかわらず、それを知らない。
* 世の中には便利なツールがあるにもかかわらず、それを知ろうとしない。
* 世の中の便利なツールは知っていても、導入に至らない。

### フォース
* 組織内でツールを導入するプロセスが重たく、新規のツールを導入しづらい。
* 導入しづらい環境では、外部のツールを導入するより自分で道具を作ってしまう方が効果的と考えてしまう場合がある。

### 解決
* [3分クッキング]による変化の第一歩。誰かがツールを使えるようになり、実際に使って見せて、効果を知る機会をつくる。作業担当者が気軽に使いたいと思えるようにしていく。
* [インディ・ジョーンズ]の遺産の発見により、一気に自動化が進むこともある。
* [強くてニューゲーム]した強者を発見できれば、今後の運用も含めて貴重な意見を聞くことができる。

### 結果
現場においてツールの導入や選定ができるようになり、自動化が少しずつ進み始めた。

## 3分クッキング
### 文脈
自動化は組織にとって殆ど初めての経験であり、知見などはほとんど蓄積されていない。識者も「自分だけ」という状況である。

### 問題
* 自動化ツールのハードルが高く、どうやって導入すればいいか分からない
* 自動化の導入に工数を割くことが難しい

### フォース
* 開発の中で、うまくいくかわからないものに時間を割くことが難しいことが多い
* 仮に苦しんで自動化ツールを導入できたとしても、時間だけがかかり効果があまり目に見えるものにならなかった場合、あまりインパクトを与えられない。
* 導入においては、コストパフォーマンスが高いように見せることが重要である。

### 解決
* 事前に自分の環境で、ある程度の構築をしておき、ツールなどを紹介すると同時に一気に運用までもっていけるよう紹介した。

### 結果
* まず第一関門を突破。これ以降、[クラウドトーク（もやもやした会話）]に陥らないようコミュニケーションを取りながら、まず[全体像を描き][全体像を描く]、堅実に進めていくことが重要である。

## インディ・ジョーンズ
### 文脈
* 現在稼働している自動化環境はない。
* 過去にすごいエンジニアが何やらすごいことをしていた、という噂が流れている。

### 問題
* 自動化対象のシステムが複雑すぎて、どこから手を付ければいいか分からない状態になってしまっている。

### フォース
* すでに稼働している環境に対して自動テストを追加するのは、対象システムの深い理解と自動テストに対する理解両方が必要になり、非常に困難な作業である。

### 解決
* 過去に構築していた自動化システムを再稼働し、短期間で自動テストを行えるように持っていく

### 結果
* 過去の遺産により、ひとまず導入の第一歩を超えることができた。しかし、これらのシステムは[験担ぎ]に成り下がった後に[原住民放棄]により打ち捨てられたものである可能性が高く、平行して[全体像を描き][全体像を描く]見直しを行うことが必要となる。



# 自動化導入時〜初期稼働までのパターン
## クラウドトーク（もやもやした会話）
### 文脈
[求む！英雄]の登場により、自動化の環境開発を進める活動を開始したが、開発対象を特定する際に「テスト自動化」という1つの言葉で説明しようとしてしまう。
（例えば、テストデータの生成のツールを作る話と、テスト結果を判定するツールの内容を「自動化ツール」と表現してしまうことにより、話し手と受け手の理解が異なってしまう。）
結果として、話し手と受け手の理解が異なるもやもやした会話となっていまい、意思疎通が図れない状態となってしまう。

### 問題
自動化の用語特定が出来ていない。
それぞれが頭に考えている自動化を言葉で特定することが出来ないため、対話時に浮かぶイメージが異なってしまうことで意識齟齬に繋がってしまう。
また、必要な技術要素の特定が出来ないことから、実施したい目標や成果物が不明確となり、自動化の環境構築を推し進めるコトが困難となる。

結果の1つとして、[建て増し旅館]風のイマイチな自動化システムを作りこんでしまう可能性が高い。

### フォース
* 自動化を進める際には、ついつい手が先になり、用語や知見が十分で無い状態に陥ることがある。
* （一般的にも）用語が整備されていないことも背景として存在する。
* 上記の知見が仮にあったとしても、チーム全体の共通認識がない状態で、突っ走ってしまいがち([自動化ハイ])である。

### 解決
* 具体的に自動化の範囲、対象を特定する用語を定義する。
* さらに、モデル図で整理した表現と組合せることにより、意思疎通を行いやすくなる。

### 結果
自動化の開発を進めるための用語認識が統一されており、意思疎通が出来る状況となっている。
また、自動化を特定する用語を分けることによる副次効果として分割特定した項目を深堀、イメージしやすくなり、より高度な技術へとつなげることが出来る可能性が発生している。


## 全体像を描く
### 文脈
[3分クッキング]により、自動化の導入は進み始めているが、まだまだテスト自動化の初期段階である。

### 問題
自動化をまず導入しては見たものの、このまま全体に適用するのは難しいように思える。

### フォース
* まず自動化を導入できたとしても、現在の設計では自動化が不可能な場合も多い。このまま邁進しても、強引な手段で自動化を行うことになり、[ついで症候群]に陥りやすい。
* 自動化をさっさと行い、先に進みたい要求も強くなってくる（[自動化ハイ]）

### 解決
* システムの全体像を描き、その中に自動テストをどうすれば効果的に適用できるかを考える。
* システムの中に自動テストに不都合な箇所があり、かつそこを自動化するのが効果的ならば設計にも手を入れることを考える。

### 結果
* 全体像を定義することで、[クラウドトーク（もやもやした会話）]から脱却することができる。
* [建て増し旅館]的なメンテナンスしにくい自動化を行わない力が働くようになる。
* 全体を俯瞰することで、[まずは"効く"ところから]始められるようになる


## まずは"効く"ところから
### 文脈
[3分クッキング]により、自動化の導入は進み始めている。最初に手を付けたところから次の場所を探そうとしている。

### 問題
次に手を付ける場所について、決定することができない。

### フォース
* 自動化の効果に対しある程度イメージが湧くと、どうしても重厚長大なシステムを計画し[ビッグバン自動化]を行ってしまいがちである。
* また、自動化が実装され始めると、[自動化ハイ]に浮かされ、[ついで症候群]に羅患し、闇雲な自動化が行われることになる。

### 解決
* まずは[全体像を描き][全体像を描く]、自動化しようとしているシステムの特徴について捉える。そののち、全体の中で自動化の効果が早く見込める場所、即ちもっとも少ない投資で最大の効果を発揮する箇所を見定め、ターゲットを決定する。
* 効果の算定の際には、現状のシステムの自動化に対する適合度、手動テストの負荷や頻度などを考慮する。
* 効果をトラッキング・表示するために適切な[ダッシュボード]を設定するとよい。

### 結果
* 自動化のスタートアップとして、効果を組織内にアピールすることができる。
* 成功例があがることで、即効性はあまりないが長期的効果は大きいような改善につなげることができる。目指すは[文明の曙]である。

## ダッシュボード
### 文脈
[3分クッキング]などにより自動化そのものを取り入れることはできたが、まだ自動化を活用できているとは言いがたい。

### 問題
テスト結果を適切に分析し、活用することができていない。取られてはいるものの、活用されていない結果レポートが多く存在する。

### フォース
自動ビルドツールによって、多くのメトリクスを並べることができる。ただし多くの情報を解釈するには担当者のリソースが必要となる。無目的に結果を垂れ流してしまった場合、メトリクスに意味はなくなってしまう。

### 解決
考えなしにレポートを出すのではなく、目的をもった結果レポートを出力するようにする。また、多くの指標を理解できるよう担当者のレベルを上げるとともに、差分を表示し変化を追うことにより、特徴的な指標をみつけやすくする。場合によっては、結果レポートのエラーから自動でバグチケットを作成するなど、レポートからアクションを行う部分も自動化し、省力化する。

### 結果
* 自動化したテストの恩恵を最大化し、素早い対応が行えるようになる。
* 記録したメトリクスを[テスト仕分け]など自動化システムの改良に用いることができるようになる。


## 自動化ハイ
### 文脈
[3分クッキング]などにより、自動化の導入には成功している。いよいよこれからが、自動化を全体に進めていく時である。

### 問題
試験的に導入した自動化の面白さに取り憑かれ、全体の設計をしないままに自動化をどんどん推し進めようとしている。その結果、似たようなシステムが乱立し、以後の管理が困難な状態（[建て増し旅館]）になりかけている。

### フォース
* 特に現場手動で自動化を行っている場合、どんどん実装を行い自動化を進めて行きたくなってしまう。
* プログラマの性として、一度うまく行き始めると、その勢いのままコードを書き進めてしまうことは大いに有り得る。

### 解決
一度冷静になり、[全体像を描く]ようにしよう。我々の目的はテスト作業の省力化・効率化であり、自動テストの実装はその手段にすぎない。どのようなテストが本当に必要なのか、メンテナンス性も含めて全体最適されているのか、現在の自動化システムで今後の拡張に耐えうるのか、冷静に判断をしよう。

### 結果
自動化の[全体像を描き][全体像を描く]、今後の拡張やメンテナンス性を考慮した自動化システムを構築することができるようになる。

## ビッグバン自動化
### 文脈
もしくはバズワードとして自動化を受け取ったエライ人がトップダウンで自動化を推奨しようとした結果、全て（もしくは大部分）の自動化を作りこんだ後に一気に実施しようとして、全体のシステムを作りこむ事態が発生する。
そして、一度に自動化を開始しようとした結果、まったく動かない状況が発生してデスマーチ的に不具合対処に追われてしまう。

### 問題
一度に全ての試験を自動実行しようとしてしまっている。
SUTのテストを、自動化システムを含めてまとめて実行してしまおうとしてしまう。
また、自動化システムのデバッグも同時発生する状況になるケースがあり、SUTの不具合か、自動化システムの不具合かを切り分けることも困難になる状況も発生する可能性が高い。
結果として、[原住民蜂起]が発生して自動化システムが使われない状況になるか、自動化システムの構築が原因で工期が延びてしまう。

### フォース
WFの環境や自動化に過剰に期待を持つ組織で発生しやすい。本現象はビックバンテストの発生と同様の状況で起こりうる。SUTと自動化システムの双方のデバッグが必要であるため、少しずつ積み上げながらSUTと自動化環境を構築しないと厳しい。

### 解決
* [信頼性バトル（信頼性イタチゴッコ）]により、SUTと自動化システムのボトルネックとなる部分を1つずつ解決していく。
* 開発やテストのプロセスに、自動化システムをどう組み込むかを考え、全体プロセスを構築して活動を行う。（[全体像を描く]活動を積極的に行う。）

### 結果
開発に関わるメンバー担当者がSUTと自動化システムを一つずつ積み上げながら動作確認して、出来る範囲を広げている。
エライ人や暴走した人がまとめて自動化システムを一気に実施する！といった発言をしない。


## ついで症候群
### 文脈
自動化に対する組織の理解が不足しているが、導入自体はできている。

### 問題
自動化ツールのマーケティングを鵜呑みにして導入してしまい、増大する維持コストを抑えられない。あれもこれもと自動化ツールに押しつけてしまい、身動きが取れなくなっている。

### フォース
自動化に対する誤解は根深く、実体験を伴わないとわかり辛いものである。説明されれば理解は示すが、いざ実践するとなると「ついでに」と適用範囲を拡げがち。知識は持っていても、自分がまさに誤解のパターンに当てはまっていることはわかりづらいものである。

### 解決
失敗を自覚できるようする。失敗の程度を大きくするか、失敗の判断を早くするかは組織それぞれ。

### 結果
ユメミガチなことは言わなくなった。副作用として[アンチ自動化]になる場合もある。


## 建て増し旅館
### 文脈
テスト自動化が職場に導入され、少しずつ適用範囲が増えていっている。

### 問題
自動化システムが、場当たり的な改修によりメンテナンス性が損なわれていってしまう。たとえば、類似のスクリプトをコピペで量産し始めたり、自動化対象（SUT）と自動化システムのギャップを強引な手法で解決し始めたりする。

### フォース
自動テストの実装を進めていくと、当初の想定とは異なる状況に出くわすことはよくある。そんなときに、立ち止まって考えず、「とりあえず動かそう」という気持ちで実装を進めてしまう。
特に、[自動化ハイ]に陥った自動化チームは、全体を考えずに自動化実装をまい進することが多い。

### 解決
テスト自動化はそれ自体が複雑なシステムであることを理解しよう。それぞれが勝手な実装を進めればいつかは崩壊してしまう。
まずは、実装を進める前に[全体像を描く]ことを習慣づけよう。もし、すでに建て増された部分がある場合は、[ブラックジャック][ヤブ医者とブラックジャック]に依頼して改修をするか、作りなおそう。

### 結果
建て増されたテストのうち、有用なものの効果を残しながらも、メンテナンス性を確保した自動化システムを創ることができる。

## テスト仕分け
### 文脈
シナリオベースの自動化テストで、何をテストしたいのかわからないテストコードに埋め尽くされており、プロダクトコードが価値を実現できているかわからなくなってきている。

### 問題
目的不明なテストをパスすることが足かせになり、プロダクトコードのメンテナンスが困難になっている。

### フォース
* テストを書く人が何を検証すべきなのか理解できていない。
* エンジニアにドメイン知識が伝わっていない
* エンジニア同士のコミュニケーションの断絶

### 解決
テストの意図を調べ、確認できなかったテストコードを捨てる。
重要なシナリオを抽出して、その価値を検証するテストケースを自動化する

### 結果
* 無駄なテストコードが消えることで、プロダクトコードの変更がやりやすくなる

## 信頼性バトル（信頼性イタチゴッコ）
### 文脈
SUTと自動化システムとの間で信頼性を競い合う争いが行われる。
自動化システムでテストを行おうとした場合に、片方が止まってデバッグ⇒他の課題でまた止まる⇒を繰り返す。
たとえば、自動化ツールがダウンする状況を改善したところ、今度はSUT側の不具合で自動化が進まない…という状況が発生する。
(結局は、信頼性が低い側が足枷になり続ける)

### 問題
自動化を動かして試験をするという際に、見積もり作業期間とは異なり、しばらくデバッグが続く状況が発生する。
一筋縄ではいかない、という理解が少ない場合には、 [ビッグバン自動化] を実施したうえでデバッグ期間を短く見積もってしまい、デスマーチに陥ってしまうなどが発生してしまう。
結果として「自動化はダメだ」という[原住民蜂起]に繋がる偏見的な判断を持ってしまう可能性が発生する。

### フォース
WFの環境や自動化に過剰に期待を持つ組織、SUTと自動化システムの双方に対してデバッグが必要で、信頼性が求められることを理解していない場合に発生しやすい。
[ビックバン自動化]を行ってしまったチームや組織が本対処を実施することが多い。

### 解決
信頼性が低いサブシステムを一つ一つ改善していくことで、双方の信頼性が少しずつ高める。ひとつずつ課題を解決することで、自動化システム自体を安定化させるだけでなく、SUT自体の信頼性向上も行われる事になる。

### 結果
* 双方の改善の結果、徐々に全体の品質が上がってくる
* 自動化試験を実施する場合には信頼性向上が必要で、チーム内の共通認識が行われている。
* エライ人や暴走した人による[ビッグバン自動化]に対する抑制がかかり、自動化環境の構築に時間がかかるということを体験として理解できるようになる。

## ヤブ医者とブラックジャック
### 文脈
[ダッシュボード]により結果も整備されるようになった。
ある日から「ソースコードもテストも修正していないのに、NGになった」「テストされていなかっただけで、デグレは起きていた」と頻繁に報告されるようになった。

### 問題
テスト自動化の信頼性が低い ( = 「テストのしかけ」の信頼性が低く、テスト結果に間違いがある。または、テスト結果は正しいがデグレード検知に向いたテストになっていない)

### フォース
* テストの結果をもって品質を判断するとした場合、その判断は「テストのしかけ」の品質に依存する。が、「テストのしかけ」の品質を評価することは導入時点では難しい。
* 人は、判断の際、定性的な報告・事実であるかどうかを確認する必要がある情報よりも、定量的な報告・機械的な情報のほうを信じたくなる。
* 回帰テストが十分であるかどうかは、テスト自動化とは直接は関係ない。が、自動的なシステムが動き出すと、そのシステムという箱で信じてしまう。

### 解決
テストのしかけの信頼性が低いことによる損失と、修理する費用とで天秤をかけよう。回帰テストが十分かどうかについて、気になった時点でテスト設計を確認しよう。ただし、そういったことを確認できる人は自動化環境を前提としたプロジェクトでは維持できていないことが多く、その場合かなりの費用を支払うことを覚悟しておきたい。

### 結果
* 直した分だけテストの結果を信用できるようになる。（ただし、老化とともに再発するが）
* 辛抱強く「テストのしかけ」を回収することで、自動化を導入した環境においても人材が成長し、[全員がブラックジャック][俺たち全員ブラックジャック]になれるかもしれない。


# 自動化の定着、あるいは終了

## 俺たち全員ブラックジャック
### 文脈
自動化システムが成長し、適宜のメンテナンスが必要な状態となっている。

### 問題
成長したシステムが、しばしば落ちるようになってしまっている。それを修正できる人間は設計者であるブラックジャックであり、属人化してしまっている。

### フォース
テスト自動化の結果、テストは文書に書かれたテストスクリプトを実行していく単純な作業ではもはやない。そんな時には、スキルの未熟な[ヤブ医者][ヤブ医者とブラックジャック]により、テスト自動化システムの全体設計を無視したようなテストのしかけを追加されることがある。またそういった不具合を修正しようとする場合、スキルの高い一部の技術者に頼ってしまうことになりがちである。


### 解決
一人のスーパーマンだけがメンテナンスするのではなく、複数人の技術者によりメンテナンスを行い、技術の継承、及びメンバーのスキルアップを図ろう。

### 結果
メンバー全員のスキルが上がり、だれでも自動化システムのメンテナンスを行うことができるようになった。また、自動テストの実装は[自動化システムだけでなく][不具合見つける、だけじゃない]テスト対象の理解を促進する効果もある。


## テストだけとか勿体無い！
自動テストを突き詰めていくと、デプロイなどテスト以外のところにも目が行くようになってくる。DevOps的な技術を活用し、テスト以外にも自動化の網をひろげていくことで、より効率的でミスの少ない開発体制の構築が可能になる、というパターン。

## もっと、人間らしく
* 元来手動で行っていた、自動化できるテストを自動化し、より人間の力が必要となるテストに集中させることができる、というパターン。

## 文明の曙
* システム全体を考え、常に改善をまわしていく、というエンジニアとしては当たり前のPDCAサイクルを、開発プロセス自体に適用できるようになるパターン。

## 験担ぎ
### 文脈
テスト自動化環境が構築されて、少なくとも一度は効果が出た状況である。継続的にテスト自動化でのテスト実施が行われている状態ではあるが、効果がある活用と運用がされていない。「このエラーは出ても問題は無い」という意思決定で運用が行われている。

### 問題
テスト自動化実施が定められているので自動化環境を動かす活動は行われている。テスト実施はされているが、明らかなエラーが検出されたとき以外は結果を誰も確認しない。
結果として、テスト資産が形骸化・陳腐化している。

### フォース
仕様変更などでテスト資産を変化に対して追従させる必要があるが、自動化環境はなぜか無視される。（担当者が異動になった場合などに発生することが多い：たこつぼ化）

### 解決
* 最新のSUTと自動化環境の差を分析して、テスト資産を追従させる。
* エラーが出ていることが、現場でもみ消せないようにプロセスを整備する。
* エラーが出ない環境を作り、そのためのチームの規律を構築する。
* 自動化環境の保守を行う担当者{自動化奉行}を決める。
* 改善コストがあわないなら、そんな自動化やめちまえ。

### 結果
SUTに適した自動化環境が整備され、変化に追従されている。
変化に追従した環境により、テスト自動化の効果が得られる状態になっている。
意味のないテスト自動化環境が無くなっている。

## アンチ自動化
### 文脈
* [ついで症候群]にこりて、「自動化は面倒臭い」という誤解が根付いてしまっている
* [験担ぎ]のテストが増加し、自動テストから便益を享受できていない、という間隔が大きくなっている。

### 問題
自動化に対する不信感により、手動テストへの回帰を望む人が多くなっている。

### フォース
多くの人にとって、やはり手動が自然な状態で、自動化は特殊な状態である。なので、自動化による便益が少ないという考えが起こってしまうと簡単に自動化に不信感を抱いてしまう。

### 解決
* 自動化への誤解を一つ一つといていこう。たった一つのツールで全てが賄われることはない。ツールベンダの言葉に踊らされず、自分たちなりの活用方法をアピールしよう。場合によっては、別のツールを試そう。
* 動きの怪しい自動化システムに意味は無い。懐疑する人々を勢いづかせないためにも、[信頼性バトル（信頼性イタチごっこ）]と[ブラックジャックによる治療][ヤブ医者とブラックジャック]、[テスト仕分け]で土台を固めていこう。

### 結果
自動化への誤解が解け、気持よく自動化を推進して行くことができる。

## 原住民蜂起
### 文脈
昔ながらの製法で、伝統を大切に守りながらのテストが行われている組織である。自動化をする開発環境ではなく、周りに自動テストの事例が殆どない状態にある。そんな中で、一部の興味を持った人が自動テストを導入しようとしている。

### 問題
推進できる人が自動化に関する追加の作業で忙しくなり、取り組みに対する効果が出てこない。また、管理職からの支援がなく、工数に見合った結果が出ていないとの評価で取り組みが失敗に終わる。

### フォース
歴史をもつ保守的な組織は、変化を好まない傾向にある。自動テストを導入しようとしている人達には伝統的なテストを壊すだけの力を持ち合わせていない。

### 解決
* 自動テストをやりたい人が、手探りながら事例を積み上げる。
* 組織を変えるために理解を求める努力を行う。
* 裏で対抗組織の力を蓄える(能力)。

### 結果
* 自動テストに対する理解が高まりつつある。
* 自動テストを実施可能な知識や技術が蓄えられている。
* 10週打ち切りまでに、上位の理解を得ていく。


## 強くてニューゲーム
### 文脈
自動化を試みていたが、[原住民蜂起]により既存の手動テストが復活し、文化は一度滅びてしまった。

### 問題
一度滅びてしまったものを立て直せず、再手動化されたテストを淡々とこなしてしまっている。

### フォース
自動化を取り巻く環境は厳しく、諦めさせられるような罠も各所にある。手探りで自動化を運用し始めた場合には、それらを避けて自動化を実施することは非常に困難である。

### 解決
一度失敗したとしても、どこに失敗があったのかを振り返ろう。例えば…

* [自動化ハイ]になったせいでメンテナンス不能な[建て増し旅館]を構築してしまった
* [テスト仕分け]を怠ったせいで[験担ぎ]の意味が無いテストが増えすぎた

### 結果
失敗を活かし、同じ罠にはまらないようにテスト自動化を進めていくことが可能になる。

---

#### ライセンスについて

<a rel="license" href="http://creativecommons.org/licenses/by/3.0/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by/3.0/88x31.png" /></a><br />この 作品 は <a rel="license" href="http://creativecommons.org/licenses/by/3.0/">クリエイティブ・コモンズ 表示 3.0 非移植 ライセンスの下に提供されています。</a>