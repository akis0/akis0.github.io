+++
title = "第0章　先行研究と本書の位置"
date = 2026-08-09
template = "page.html"
path = "tech/2026/product-tragedy/chapter0"
aliases = ["/tech/2026/product-tragedy/chapter0.html"]
+++

> 私がより遠くまで見渡せたとすれば、それは巨人の肩の上に立っていたからである。<br>
>　――アイザック・ニュートン「ロバート・フック宛書簡」

## 0.1　本書の目的

　本書の目的は、個々の部門がそれぞれの職務をおおむね適切に遂行しているにもかかわらず、製品全体としては顧客にも企業にも十分な価値をもたらさないという、プロダクト開発上の反復的な失敗を説明することにある。

　ここでいうプロダクトには、量産される工業製品だけでなく、ソフトウェア、継続的に提供されるサービス、およびそれらを組み合わせたシステムを含む。個々の機能が仕様どおりに動くか、製造工程が効率的か、広告が十分な人数へ届いたかという個別の成否ではなく、それらを組み合わせた全体が、特定の顧客の特定の状況において価値を持つかを問題にする。

　本書が「悲劇」と呼ぶのは、失敗が不可避だからではない。各主体が置かれた評価制度、利益責任、情報経路および権限の範囲に従って合理的に行動した結果、誰も意図しなかった不合理が再生産されるからである。企画部門が売る理由を追加し、マーケティング部門が競合との差を埋め、技術部門が性能を高め、品質保証部門が危険を減らす。そのどれもが単独では誤りでなくとも、製品全体が良くなるとは限らない。

　したがって、本書の問いは「誰が間違えたのか」ではない。

> 顧客価値と会社全体の利益を考えるべき局面で、なぜ組織は部門別の問題しか認識できなくなるのか。

## 0.2　利益を生む雛形としてのプロダクト開発

　量産型製品の利益は、ごく単純化すれば次のように表せる。

`P = Q(p - c) - F`

　ここで、`P` は利益、`Q` は販売数量、`p` は販売価格、`c` は一単位当たりの変動費、`F` は開発費、設備費その他の固定費である。量産工程の改善は、歩留まりを高め、工数や材料の無駄を減らすことによって、主として `c` と供給可能な `Q` に作用する。しかし、どの顧客がいくらで何台買うかという `p` と需要としての `Q`、さらに原価の相当部分を拘束する製品構造は、量産開始より前の製品企画と設計によって大きく決まる。

　この意味で、プロダクト開発とは単に製造の準備をする活動ではない。市場で反復販売され、工場やソフトウェア配信基盤によって複製される「収益構造の雛形」を作る活動である。量産は、良い設計判断だけでなく、悪い設計判断も高い精度で大量に複製する。製造現場の改善によって良い製品の利益をさらに増やすことはできるが、誰も欲しない製品を低コストで作るだけでは、市場不適合を救済できない。

　これは製造能力を軽視する主張ではない。品質、供給能力および原価競争力を欠けば、良い製品構想も利益にはならない。ただし、量産段階の失敗が価値の実現を妨げるのに対し、製品構想の失敗は、そもそも実現すべき価値を失わせる。両者にはこの非対称性がある。

## 0.3　プロダクト・マーケット・フィットと需要の軽視

　プロダクト・マーケット・フィット（PMF）という語は、とりわけスタートアップ論において広く用いられてきた。マーク・アンドリーセンはPMFを「その市場を満足させられる製品を持って、良い市場にいること」と定義し、スタートアップにとって最も重要な条件だと論じた。[^pmf]

　もっとも、PMFを唱えれば問題が解けるわけではない。PMFは、製品と市場の関係を評価する強力な観点ではあるが、大企業の内部で誰がその適合を定義し、複数部門の目標が衝突したときに誰がそれを優先させるのかまでは定めない。市場調査、顧客アンケート、ペルソナ、販売予測が存在していても、その情報が機能の採否、重量、消費電力、価格、納期その他のトレードオフを裁定する権威を持つとは限らない。

　したがって、本書が問題にする「PMFの軽視」は、顧客について何も調べていないという素朴な無知に限られない。顧客の声は収集されているが、競合比較、部門売上、技術目標、品質基準などと並ぶ一評価項目へ格下げされ、製品全体を統治する原理にはなっていない状態を含む。顧客の声は数えられているが、主権者ではないのである。

　クリステンセンの「イノベーションのジレンマ」も、この問題に隣接する。破壊的イノベーション論は、既存企業が単に需要を観察しなかったというより、既存顧客、既存の利益率および既存の資源配分過程に照らして、低価格領域や新市場の初期需要を合理的に低く評価しうることを示した。[^disruption]　本書では、そこから競争企業が下位市場を起点に性能を向上させる過程全体へは踏み込まない。ここで重要なのは、需要が物理的に見えなかったのではなく、既存組織にとって重要な需要として認識されなかったという点である。

## 0.4　分かれて発達した先行研究

　本書が扱う問題の各部分は、すでに複数の研究領域によって論じられてきた。

| 研究領域 | 主として説明してきたこと | 本書が接続する問い |
| --- | --- | --- |
| PMF、顧客開発、マーケティング | 製品と市場需要の適合 | 市場適合を部門横断の判断へ変換する権限はどこにあるか |
| 破壊的イノベーション論 | 既存企業が新しい需要を合理的に軽視する機構 | 軽視された需要が製品要求から脱落する過程 |
| 要求工学、システムズエンジニアリング | 利害関係者要求の定義、配分、検証およびシステム統合 | 正しく管理された個別要求が、なぜ誤った製品全体を作りうるか |
| 製品アーキテクチャ論 | 部品間の依存関係と、統合・モジュール化の条件 | 顧客価値にとって重要な依存関係を誰が所有するか |
| 組織設計論、ミラーリング仮説 | 技術的依存関係と組織内の連絡関係の対応 | 製品と組織の対応が、市場との不適合まで複製する場合 |
| 管理会計、責任センター論 | 事業部別利益、移転価格、目標整合性 | 会社全体の利益と事業部別利益が乖離する局面 |
| リーン製品開発 | 顧客価値、チーフエンジニア、部門横断統合 | その仕組みが、どのような悲劇を防いでいるのか |

　ヘンダーソンとクラークは、個々の部品技術が大きく変わらなくても、部品間の結合関係が変わる「アーキテクチャル・イノベーション」が既存企業を困難に陥れると論じた。結合関係についての知識は、組織構造や情報処理手続に埋め込まれているためである。[^architectural]

　これと関連するミラーリング仮説は、製品内の技術的依存関係と、それを開発する人々の組織的な結びつきが対応する傾向を扱う。[^mirroring]　この見方は、製品構造と組織構造を別々に設計できないことを明らかにする。ただし、両者がよく対応していること自体は、市場適合を保証しない。過去の製品分類に沿って組織が編成され、その組織が次の製品を同じ分類で切り分けるなら、誤った市場認識まで精密に再生産されうる。

　一方、トヨタの製品開発については、車種全体に責任を負うチーフエンジニア、顧客価値を記述するコンセプト、機能部門の専門性と部門横断統合の両立などが論じられてきた。チーフエンジニアは単なる日程管理者ではなく、製品構想、事業性、技術設計、生産準備および市場投入を横断して製品系列に責任を負う役割として説明される。[^chief]

　本書は、これらの研究のいずれかを置き換えるものではない。需要、製品アーキテクチャ、組織構造、利益責任および統合権限について別々に発達してきた議論を、「一つの製品が市場へ送り出されるまで」という同じ分析単位の上へ置き直す。

## 0.5　利益単位の境界と、誰のものでもない市場

　事業部制やカンパニー制には、意思決定を迅速にし、成果責任を明確にする利点がある。しかし、利益を測定する単位は、組織が認識できる機会の単位にもなる。

　会社全体の利益を単純化して、次のように表す。

`P_firm = P_1 + P_2 + ... + P_n`<br>
`　　　　 + S_12 + S_13 + ... + S_1n`<br>
`　　　　 + S_23 + S_24 + ... + S_2n`<br>
`　　　　 + ...`<br>
`　　　　 + S_(n-1)n - C_coord`

　`P_i` は事業部 `i` が単独で計上する利益、`S_ij` は事業部 `i` と事業部 `j` の補完によって初めて生じる価値、`C_coord` は統合に必要な調整費用である。各事業部が `P_i` の最大化について厳格に評価される一方、`S_ij` に責任を持つ主体がいなければ、会社全体では有望な機会が、各事業部にとっては採算の悪い依頼として現れる。

　たとえば、ある統合製品によってA事業部の利益が10減り、B事業部の利益が5増える一方、両者の統合によって新たに20の価値が生じるとする。会社全体では15の利益増である。しかし、統合価値20を誰の損益にも帰属させられず、A事業部に10の損失だけが計上されるなら、A事業部が計画に反対するのは合理的である。ここでは、会社への忠誠心の不足ではなく、測定単位と意思決定単位の不一致が問題となる。

　ソニーの携帯音楽事業は、この問題を考えるための典型的な事例である。ソニーは携帯音楽機器、音楽コンテンツ、ソフトウェアおよび消費者ブランドを保有していた。ところが、2006年の同社年次報告書は、自社の競争力を妨げる問題として、サイロ化した組織、製品間の限定的な相互運用性、ソフトウェアおよびサービス開発の弱さを自ら挙げている。[^sony-ar]　同時期のNetwork Walkmanについても、ハードウェアとソフトウェアの開発が十分に統合されず、音楽を機器へ移す体験が煩雑になったと報じられている。[^sony-walkman]

　これは、ソニーに部品や技術がなかったという話ではない。携帯音楽という市場が、音響機器事業、ソフトウェア、コンテンツ事業のいずれか一つに収まらなかったという話である。各事業の内側には責任者がいても、それらの間に生じる利用体験と会社全体の収益機会には、十分な権限を持つ所有者がいなかった――本書では、このように解釈する。後年にソニーが「One Sony」を掲げ、グループ全体の資産を利用する方針を明示したことも、少なくとも同社自身が事業横断統合を経営課題として認識していたことを示している。[^one-sony]

## 0.6　長期成長をめぐる問題提起

　この問題が企業成長をどの程度説明するかを、本書だけで厳密に識別することはできない。ただし、日本の代表的な大規模製造企業について、2006年3月期と2025年3月期の連結売上高を比較すると、問題を考えるための示唆的な差が見える。

| 企業 | 2006年3月期 | 2025年3月期 | 倍率 | 名目年平均成長率 |
| --- | ---: | ---: | ---: | ---: |
| トヨタ自動車 | 21.03兆円 | 48.04兆円 | 2.28倍 | 4.44% |
| ソニー | 7.48兆円 | 12.96兆円 | 1.73倍 | 2.94% |
| 日立製作所 | 9.46兆円 | 9.78兆円 | 1.03倍 | 0.17% |
| パナソニック | 8.89兆円 | 8.46兆円 | 0.95倍 | -0.26% |
| 東芝 | 6.34兆円 | 3.51兆円 | 0.55倍 | -3.06% |

　この五社に限れば、売上規模を明瞭に倍増させたのはトヨタである。日立とパナソニックの売上高はおおむね横ばいであり、東芝は事業売却を伴いながら大幅に縮小した。他方、ソニーは約73%成長しているため、「トヨタ以外は成長していない」と一括するのは必ずしも正確でない。また、日立は売上規模が横ばいでも収益性を大きく改善しており、企業価値や経営成果を売上だけで測るのは適切ではない。

　この比較には、物価上昇、為替変動、会計基準、買収・売却、連結範囲および産業ごとの世界需要の差を調整していないという限界もある。したがって、この表から、トヨタの成長を製品統合の仕組みだけに帰属させることはできない。この表が示すのは、選んだ日本の大企業群のなかでトヨタの売上成長が際立っており、他方で電機系企業の多くが、豊富な技術、人材および事業資産を持ちながら同程度には規模を拡大できなかった、という出発点にすぎない。

　問うべきなのは、トヨタを無条件に模倣すべきかではない。なぜ、技術的資産の豊富さが製品全体の価値へ自動的には変換されないのか。そして、トヨタの製品開発に見られる全体責任、現地現物および部門横断統合が、その変換にどのような役割を果たしてきたのかである。

## 0.7　本書の位置

　本書は、需要の構造を `D`、製品の構造を `A`、組織の構造を `O` として捉える。

　需要の構造 `D` には、誰が、どのような状況で、何を解決したいのかという関係が含まれる。製品の構造 `A` には、その仕事を実現する機能、部品、ソフトウェア、物理的制約および相互依存関係が含まれる。組織の構造 `O` には、担当部門、情報経路、評価指標、損益責任および意思決定権限が含まれる。

　プロダクト統合が成功するためには、需要から製品への翻訳 `D → A` と、製品から組織への責任配分 `A → O` が、重要な関係を保存していなければならない。たとえば顧客の仕事が複数機能の組合せによってのみ達成されるなら、その機能間の関係は製品設計で保存され、さらに組織上も誰かが全体として所有しなければならない。部品だけを各部門へ配り、部品間の関係を誰にも配らなければ、統合価値は組織図の隙間へ落ちる。

　本書の独自性を、新しい万能理論の提示に求めるべきではない。本書の位置は、従来別々に論じられやすかった次の問いを、一つの失敗過程として接続することにある。

1. 誰の、どのような需要を製品の基準とするのか。
2. 複数の価値が衝突したとき、何を守り、何を捨てるのか。
3. 重量、原価、電力、注意力、開発期間などの共有資源に、誰が価格を付けるのか。
4. 事業部の境界をまたぐ顧客価値を、誰の損益として認識するのか。
5. 完成済みの機能であっても、製品全体のために拒否できるのは誰か。
6. 市場で得られた知識を、次の製品構想と組織設計へ戻す経路はあるか。

　要求分析は、何を満たせば成功なのかを明らかにする。プロダクト統合は、複数の成功条件が衝突したときに、どれを優先するのかを決める。組織設計は、その判断に必要な情報、責任および権限を誰へ与えるのかを決める。この三つを切り離せば、精密な要求、優秀な部品、厳格な工程から、顧客の生活には適合しない製品を作ることができる。

　次章以降では、架空の家電製品が企画され、各部門の善意と局所合理性によって機能を強化し、すべての試験に合格しながら、市場では失敗する過程を追う。そこには、無知な悪役も、意図的な虚偽も必要ない。

---

## 注・本文中で直接用いた資料

[^pmf]: Marc Andreessen, [“The only thing that matters”](https://pmarchive.com/guide_to_startups_part4.html), 2007.

[^disruption]: Christensen Institute, [“Disruptive Innovation Theory”](https://www.christenseninstitute.org/theory/disruptive-innovation/).

[^architectural]: Rebecca M. Henderson and Kim B. Clark, [“Architectural Innovation: The Reconfiguration of Existing Product Technologies and the Failure of Established Firms”](https://scholarsarchive.byu.edu/facpub/8984/), *Administrative Science Quarterly*, Vol. 35, No. 1, 1990, pp. 9–30.

[^mirroring]: Lyra J. Colfer and Carliss Y. Baldwin, [“The Mirroring Hypothesis: Theory, Evidence, and Exceptions”](https://www.hbs.edu/ris/Publication%20Files/Colfer%20Baldwin%20Mirroring%20Hypothesis%20Ind%20Corp%20Change-2016_8aa320ff-6aa6-42ef-b259-d139012faaf6.pdf), *Industrial and Corporate Change*, Vol. 25, No. 5, 2016, pp. 709–738.

[^chief]: Lean Enterprise Institute, [“Chief Engineer”](https://www.lean.org/lexicon-terms/chief-engineer/); Jeffrey K. Liker and James M. Morgan, [“The Toyota Way in Services: The Case of Lean Product Development”](https://conformabledecoders.media.mit.edu/courses/2023/decoders2.0/Papers/David%20Sadat/The%20Toyota%20Way%20in%20Services_The%20Case%20of%20Lean%20Product%20Development.pdf), *Academy of Management Perspectives*, Vol. 20, No. 2, 2006, pp. 5–20.

[^sony-ar]: Sony Corporation, [*Annual Report 2006*](https://www.sony.com/en/SonyInfo/IR/library/ar/qfhh7c00000aksmr.pdf), pp. 3–6.

[^sony-walkman]: John Nathan, [“Stringer's Way”](https://www.newyorker.com/magazine/2006/06/05/stringers-way), *The New Yorker*, May 29, 2006.

[^one-sony]: Sony Corporation, [「ソニーを変革し、エレクトロニクス事業の再生、成長と新たな価値創造をめざす――“One Sony”でソニーを変える」](https://www.sony.com/ja/SonyInfo/News/Press/201204/12-056/), 2012年4月12日。

### 長期売上比較の資料

- トヨタ自動車：[2006年3月期](https://newsroom.toyota.eu/2006-toyota-reports-record-year-end-results/)、[2025年3月期](https://pressroom.toyota.com/tmc-announces-april-through-march-2025-financial-results/)
- ソニー：[2006年3月期](https://www.sony.com/en/SonyInfo/IR/library/ar/qfhh7c00000aksmr.pdf)、[2025年3月期](https://www.sony.com/en/SonyInfo/IR/library/presen/er/pdf/24q4_sony.pdf)
- 日立製作所：[2006年3月期](https://www.hitachi.com/New/cnews/070330.pdf)、[2025年3月期](https://www.hitachi.com/New/cnews/month/2025/04/250428/2024_An.pdf)
- パナソニック（旧松下電器産業）：[2006年3月期](https://news.panasonic.com/global/press/data/en060428-5/en060428-5-19.pdf)、[2025年3月期](https://news.panasonic.com/uploads/tmg_block_page_image/file/32667/en250509-4-1.pdf)
- 東芝：[2006年3月期](https://www.global.toshiba/content/dam/toshiba/migration/corp/irAssets/about/ir/en/finance/er/er2005/q4/ter2005fye.pdf)、[2025年3月期](https://www.global.toshiba/content/dam/toshiba/ww/ir/corporate/finance/pdf/tpr2024q4e.pdf)

注：比較は各社公表値を兆円単位へ丸めた。年平均成長率は19年間の名目複利成長率。物価、為替、会計基準および連結範囲の変化は未調整である。

## 参考資料

　以下は、本章の個々の記述を直接立証するための注とは別に、プロダクト統合を需要、製品アーキテクチャ、組織構造、利益責任および開発統括の関係として考えるための基礎資料である。公開版または概要を閲覧できるものにはリンクを付した。このへんの資料が重要だろうなあと並べてるけど全部通読してるわけではない。読みたい資料だったり重要らしい資料だったりする。

### プロダクト開発の全体像と経済性

- Kim B. Clark and Takahiro Fujimoto, [*Product Development Performance: Strategy, Organization, and Management in the World Auto Industry*](https://www.hbs.edu/faculty/Pages/item.aspx?num=4745), Harvard Business School Press, 1991.――自動車産業の国際比較を通じて、製品開発のリードタイム、生産性、品質および組織統合を扱う、本章の問題設定に最も近い基本文献。
- Steven C. Wheelwright and Kim B. Clark, [*Revolutionizing Product Development: Quantum Leaps in Speed, Efficiency, and Quality*](https://www.hbs.edu/faculty/Pages/item.aspx?num=155), Free Press, 1992.――個別プロジェクトだけでなく、開発プロジェクト群、資源配分、部門横断統合を含む開発組織の設計を扱う。
- Donald G. Reinertsen, [*The Principles of Product Development Flow: Second Generation Lean Product Development*](https://books.google.com/books/about/The_Principles_of_Product_Development_Fl.html?id=1HlPPgAACAAJ), Celeritas Publishing, 2009（[第1章公開PDF](https://lpd2.com/wp-content/uploads/2013/06/ReinertsenFLOWChap1.pdf)）。――遅延費用、待ち行列、バッチサイズ、仕掛品などを用い、製品開発上の判断を経済性とフローの問題として定式化する。
- Karl T. Ulrich, Steven D. Eppinger and Maria C. Yang, *Product Design and Development*, 7th ed., McGraw-Hill, 2020.――顧客ニーズの同定から製品仕様、コンセプト選択、アーキテクチャ、試験、生産立上げまでを一つの開発過程として整理する標準的教科書。
- 延岡健太郎『[MOT「技術経営」入門](https://ci.nii.ac.jp/ncid/BA78571047)』日本経済新聞社、2006年。――技術を顧客価値と事業成果へ変換するという観点から、製品開発、組織能力、事業戦略を概観する日本語の基礎文献。

### 市場適合、顧客需要および既存企業の資源配分

- Clayton M. Christensen, *The Innovator's Dilemma: When New Technologies Cause Great Firms to Fail*, Harvard Business School Press, 1997（[理論概要](https://www.christenseninstitute.org/theory/disruptive-innovation/)）。――優良企業が既存顧客と収益性を重視する合理的な資源配分によって、新しい需要を軽視しうる機構を論じる。
- Steve Blank, *The Four Steps to the Epiphany: Successful Strategies for Products that Win*, K&S Ranch, 2005.――製品開発と顧客発見を区別し、仮説検証を通じて市場を探索する顧客開発モデルの基本文献。
- Eric Ries, *The Lean Startup: How Today's Entrepreneurs Use Continuous Innovation to Create Radically Successful Businesses*, Crown Business, 2011.――構築・計測・学習の反復を通じ、製品構想を市場からの学習に接続する方法を論じる。
- Clayton M. Christensen, Taddy Hall, Karen Dillon and David S. Duncan, *Competing Against Luck: The Story of Innovation and Customer Choice*, HarperBusiness, 2016.――製品分類ではなく、顧客が特定状況で成し遂げようとする仕事を需要分析の単位とするジョブ理論を提示する。

### 製品アーキテクチャと組織構造

- Karl T. Ulrich, [“The Role of Product Architecture in the Manufacturing Firm”](https://ktulrich.com/wp-content/uploads/2022/09/ulrich-architecture-rp.pdf), *Research Policy*, Vol. 24, No. 3, 1995, pp. 419–440.――機能を物理的構成要素へ配分し、構成要素間のインターフェースを定めるものとして製品アーキテクチャを整理する。
- Melvin E. Conway, [“How Do Committees Invent?”](https://www.melconway.com/research/committees.html), *Datamation*, Vol. 14, No. 4, 1968, pp. 28–31.――設計組織のコミュニケーション構造が、産出されるシステムの構造を拘束するという議論の原典。
- Ron Sanchez and Joseph T. Mahoney, [“Modularity, Flexibility, and Knowledge Management in Product and Organization Design”](https://josephmahoney.web.illinois.edu/BA545_Fall%202013/Sanchez%20and%20Mahoney%20%281996%29.pdf), *Strategic Management Journal*, Vol. 17, Winter Special Issue, 1996, pp. 63–76.――製品のモジュール性、組織の疎結合、知識管理および戦略的柔軟性の関係を論じる。
- Alan MacCormack, John Rusnak and Carliss Y. Baldwin, [“Exploring the Duality between Product and Organizational Architectures: A Test of the Mirroring Hypothesis”](https://www.hbs.edu/ris/download.aspx?name=08-039.pdf), Harvard Business School Working Paper 08-039, 2007（のちに *Research Policy*, Vol. 41, No. 8, 2012, pp. 1309–1324）。――製品構造と開発組織の対応関係を実証的に検討する。
- Lyra J. Colfer and Carliss Y. Baldwin, [“The Mirroring Hypothesis: Theory, Evidence, and Exceptions”](https://www.hbs.edu/ris/Publication%20Files/Colfer%20Baldwin%20Mirroring%20Hypothesis%20Ind%20Corp%20Change-2016_8aa320ff-6aa6-42ef-b259-d139012faaf6.pdf), *Industrial and Corporate Change*, Vol. 25, No. 5, 2016, pp. 709–738.――ミラーリング仮説に関する142件の実証研究を整理し、成立条件と例外を検討する。

### 利益責任、事業部境界およびシナジー

- Robert N. Anthony and Vijay Govindarajan, [*Management Control Systems*](https://www.hbs.edu/faculty/Pages/item.aspx?num=48490), 12th ed., McGraw-Hill/Irwin, 2007.――責任センター、利益センター、移転価格、業績測定および目標整合性を扱う管理会計・マネジメントコントロールの基本文献。
- Wouter Dessein, Luis Garicano and Robert H. Gertner, [“Organizing for Synergies”](https://www.aeaweb.org/articles?id=10.1257%2Fmic.2.4.77), *American Economic Journal: Microeconomics*, Vol. 2, No. 4, 2010, pp. 77–114（[公開PDF](https://business.columbia.edu/sites/default/files-efs/pubfiles/3228/organizing%20for%20synergies.pdf)）。――事業部の自律性と、部門横断シナジーを実現するための調整との内生的な対立をモデル化する。
- Emilie R. Feldman, [“Corporate Strategy: Past, Present, and Future”](https://faculty.wharton.upenn.edu/wp-content/uploads/2018/07/CorporateStrategy_SMR-Paper.pdf), *Strategic Management Review*, 2020.――複数事業を保有する企業が、その境界、資源配分および事業間関係をいかに設計するかという企業戦略研究を概観する。

### トヨタの製品開発と組織能力

- James M. Morgan and Jeffrey K. Liker, [*The Toyota Product Development System: Integrating People, Process, and Technology*](https://www.routledge.com/The-Toyota-Product-Development-System-Integrating-People-Process-and-Technology/Morgan-Liker/p/book/9781563272820), Productivity Press, 2006.――人、プロセス、技術の三側面からトヨタの製品開発システムを整理し、チーフエンジニア制をその中心要素として扱う。
- Jeffrey K. Liker and James M. Morgan, [“The Toyota Way in Services: The Case of Lean Product Development”](https://conformabledecoders.media.mit.edu/courses/2023/decoders2.0/Papers/David%20Sadat/The%20Toyota%20Way%20in%20Services_The%20Case%20of%20Lean%20Product%20Development.pdf), *Academy of Management Perspectives*, Vol. 20, No. 2, 2006, pp. 5–20.――トヨタ製品開発の諸原則を概観できる短い論文。
- Lean Enterprise Institute, [“Chief Engineer”](https://www.lean.org/lexicon-terms/chief-engineer/) および [*Chief Engineer*](https://info.lean.org/hubfs/ebook%20files/Design-brief-chief-engineer-final.pdf).――チーフエンジニアが製品コンセプト、事業性、技術設計、生産準備および市場投入に対して負う全体責任の概要。
- 藤本隆宏「[自動車の設計思想と製品開発能力](https://merc.e.u-tokyo.ac.jp/mmrc/dp/pdf/MMRC74_2006.pdf)」東京大学ものづくり経営研究センター、MMRC Discussion Paper No. 74、2006年。――製品アーキテクチャと製品開発組織能力を日本語で接続して論じる公開資料。
- 藤本隆宏「[組織能力と製品アーキテクチャ](https://www.jstage.jst.go.jp/article/soshikikagaku/36/4/36_20220730-67/_pdf)」『組織科学』第36巻第4号、2003年、11–22頁。――組織能力と製品アーキテクチャの適合関係を論じる。
- 藤本隆宏『[能力構築競争――日本の自動車産業はなぜ強いのか](https://www.rieti.go.jp/jp/publications/summary/03070000.html)』中央公論新社、2003年。――日本の自動車産業の競争力を、長期的に形成される組織能力と進化の観点から説明する。

### 要求工学およびシステム統合

- ISO/IEC/IEEE, [*ISO/IEC/IEEE 29148:2018 Systems and Software Engineering—Life Cycle Processes—Requirements Engineering*](https://www.iso.org/standard/72089.html), 2018.――利害関係者ニーズからシステム要求・ソフトウェア要求までの要求工学プロセス、情報項目および良い要求の特性を定める国際規格。
- ISO/IEC/IEEE, [*ISO/IEC/IEEE 15288:2023 Systems and Software Engineering—System Life Cycle Processes*](https://www.iso.org/standard/81702.html), 2023.――構想から廃棄までのシステムライフサイクルプロセスを定め、要求、アーキテクチャ、統合、検証および妥当性確認を一連の技術プロセスとして位置づける。

[戻る：前書き](../preface/)<br>
[次へ：第1章](../chapter1/)<br>
[章立てへ](../)<br>
