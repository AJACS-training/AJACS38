# 遺伝子発現DB・解析ツールの紹介　　担当: 小野 浩雅

<p>目次</p>
<div class="contents">
<a id="contents_1"></a>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="#taf036b7"> 遺伝子発現データベースに関する統合TV </a></li>
<li><a href="#h2a90094"> 講習に必要な基礎知識「遺伝子のDB・ウェブツールの基礎」 </a></li>
<li><a href="#bb55f671"> BioGPS </a>
<ul class="list2" style="padding-left:16px;margin-left:16px"><li><a href="#b7dd172e"> 【実習1】BioGPSを使ってある遺伝子の発現プロファイルを調べる </a></li></ul></li>
<li><a href="#s29e8caa"> RefEx?（Reference Expression dataset） </a>
<ul class="list2" style="padding-left:16px;margin-left:16px"><li><a href="#d71c8bae"> 【実習2】RefExを使って、組織特異的遺伝子を検索する </a></li></ul></li></ul>
</div>

<h3 id="content_1_0"><a id="taf036b7" href="http://MotDB.DBCLS.jp/?AJACS38%2Fhono1#taf036b7" title="taf036b7"><span class="sanchor">_</span></a> <span style="font-size:20px;display:inline-block;line-height:130%;text-indent:0px">遺伝子発現データベース</span>に関する統合TV  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/index.rb?category=%E7%99%BA%E7%8F%BE%E6%83%85%E5%A0%B1" rel="nofollow">旧 統合TVの「発現情報」タグ </a>をクリック！</li>
<li><a href="http://togotv.dbcls.jp/ja/contents/category/expression#%E9%81%BA%E4%BC%9D%E5%AD%90%E3%83%BB%E3%82%BF%E3%83%B3%E3%83%91%E3%82%AF%E8%B3%AA%E7%99%BA%E7%8F%BE%E3%82%92%E7%B6%B2%E7%BE%85%E7%9A%84%E3%81%AB%E8%AA%BF%E3%81%B9%E3%81%9F%E3%81%84" rel="nofollow">統合TV の発現制御解析 カテゴリー</a>から探す</li></ul>

<div class="jumpmenu"><a href="#navigator">&uarr;</a></div><h3 id="content_1_1"><a id="h2a90094" href="http://MotDB.DBCLS.jp/?AJACS38%2Fhono1#h2a90094" title="h2a90094"><span class="sanchor">_</span></a> 講習に必要な基礎知識「遺伝子のDB・ウェブツールの基礎」  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://motdb.dbcls.jp/?AJACS33%2Fmeso#e3b0f070" rel="nofollow">過去の講習会ページ</a>をご参照ください。</li></ul>

<div class="jumpmenu"><a href="#navigator">&uarr;</a></div><h3 id="content_1_2"><a id="bb55f671" href="http://MotDB.DBCLS.jp/?AJACS38%2Fhono1#bb55f671" title="bb55f671"><span class="sanchor">_</span></a> <a href="http://biogps.org/" rel="nofollow"><span style="font-size:20px;display:inline-block;line-height:130%;text-indent:0px">BioGPS</span></a>  </h3>
<p><span style="color:green">ヒト、マウス、ラットのさまざまな組織や細胞(株)における遺伝子発現プロファイルのデータベース</span></p>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://biogps.org/" rel="nofollow">BioGPS</a>はAffymetrix社製のマイクロアレイである<span class="noexists">GeneChip<a href="http://MotDB.DBCLS.jp/?cmd=edit&amp;page=GeneChip&amp;refer=AJACS38%2Fhono1">?</a></span>を用いたさまざまな組織や細胞(株)遺伝子発現プロファイルのデータベース。</li>
<li>検索した遺伝子に対して、種々の外部データベースを横断検索することができるだけでなく、それらの設定を保存したり、表示方法を自由にカスタマイズすることができる「Gene annotation portal」。</li>
<li>外部データベースには、Wikipedia(Gene Wiki)、著名な試薬会社の検索窓へのリンク集、pathway、Nature系DB、モデル生物DB、文献DBなど多種多様</li>
<li>マウスのエキソンアレイのデータから遺伝子のスプライシングバリアント(Splicing variant)の発現状況も調べることが可能。最近ではCircadian関係のデータも。</li>
<li>さらに最近のアップデートで、NCBI Gene Expression Omnibus (GEO)中から選抜されたデータセットに切り替えて発現状況を調べることが可能に。</li></ul>

<div class="jumpmenu"><a href="#navigator">&uarr;</a></div><h3 id="content_1_3"><a id="b7dd172e" href="http://MotDB.DBCLS.jp/?AJACS38%2Fhono1#b7dd172e" title="b7dd172e">_</a> 【実習1】BioGPSを使ってある遺伝子の発現プロファイルを調べる  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/20120911.html#p01" rel="nofollow">【復習用】遺伝子発現プロファイルデータベースBioGPSを使い倒す2012</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li><a href="http://togotv.dbcls.jp/20100829.html#p01" rel="nofollow">【以前の講習会動画】遺伝子発現データベースの活用法</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li>1. <a href="http://biogps.org/" rel="nofollow">http://biogps.org/</a>を開きます。</li>
<li>2.骨格筋の分化決定遺伝子であるMyogenic differentiation 1(MyoD)の発現プロファイルを調べてみましょう。中央の検索窓に「myod」と入力し、「search」を押します。</li>
<li>3. 表示された検索結果の中から「ID 4654」をクリックします。</li>
<li>4. 最初はヒトのマイクロアレイデータが表示されます。</li>
<li>5. 画面左側の&quot;Current Gene List&quot;は右上の&lt;&lt;アイコンをクリックすると非表示にできます。非表示にすることで画面を広く使うことができます。</li>
<li>6. ページ内のウインドウは通常のウインドウと同じようにドラッグによる移動やサイズの変更などを行うことができます。 歯車マークのメニューから&quot;Open in browser&quot; を選択すると、新しいタブで表示できます。</li>
<li>7. &quot;Search&quot; と書かれた窓に単語(組織名など)を入力すると、その単語の含まれた部分が赤くハイライト表示されます。今回は &quot;Muscle&quot; と入力してみます。</li>
<li>8. &quot;Zoom&quot; のバーを用いることで、グラフの表示範囲を調整することが出来ます。</li>
<li>9. 発現量を示すバーをクリックすると発現強度の値が表示されます。</li>
<li>10. マイクロアレイデータ右上の&quot;Species: Hs&quot;をクリックするとマウスやラットを選択できるので、&quot;M. musculus (Mouse)&quot;をクリックしてマウスのデータを表示できます。</li>
<li>11. MyoDはどの組織、細胞で強く発現しているでしょうか？</li>
<li>12. 場合によっては&quot;Probeset&quot;のプルダウンメニューから複数の項目を選択できる場合があります。これはどのようなケースが考えられるでしょうか？</li>
<li>13. &quot;Static Image&quot; をクリックすると、ズームや検索機能などのついていない、画像だけのグラフで表示されます。低スペックなマシンでは、こちらの方が軽快に動作するでしょう。</li>
<li>14. &quot;Correlation&quot;タブをクリックして検索すると、発現パターンが似ている他の遺伝子を検索できますが、どのような遺伝子が出てくるでしょうか？</li>
<li>15. &quot;Downloads&quot; をクリックすると現在表示している遺伝子の発現データを CSV 形式でダウンロードできます。</li>
<li>16. &quot;Dataset&quot;の右にある'change&quot;をクリックすると、デフォルトで用意されているデータセットやNCBI GEO中のデータセットを検索でき、それらのデータに表示を切り替えることができます。&quot;Species: Hs&quot;に切り替えてから、&quot;change&quot;をクリックしたあと、&quot;Default Datasets&quot;から&quot;Barcode on normal tissues (262 samples)&quot;を選択します。どのようにデータが変わったでしょうか。</li>
<li>17. さらに&quot;Search&quot;からキーワード検索で、GEOのデータを検索してみましょう。&quot;C2C12&quot;と検索するとどのようなデータが選択できるでしょうか。</li>
<li>18. 右上の「default rayout」をクリックすると、検索した遺伝子に関して種々の外部データベースを横断検索できますが、どのようなデータが閲覧できるのか調べてみましょう。</li>
<li>19. 左上の「Search」タグをクリックして検索画面にもどり、自分の興味ある遺伝子について同様に検索してみましょう。
すぐに自分の興味ある遺伝子が浮かばない場合は、著名な<a href="http://ja.wikipedia.org/wiki/%E4%BA%BA%E5%B7%A5%E5%A4%9A%E8%83%BD%E6%80%A7%E5%B9%B9%E7%B4%B0%E8%83%9E" rel="nofollow">iPS細胞</a>を作るために必要な4因子（Oct3/4・Sox2・Klf4・c-Myc）がどの組織で発現しているか、またデータを切り替えて検索してみましょう。</li></ul>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>【余談】
<a href="http://biogps.org/iphone/" rel="nofollow">BioGPSのiPhoneアプリ</a>が無料で公開されていますので、「あの遺伝子はどの組織で発現してるのかな？」とふと調べたいときにお手持ちのiPhoneで遺伝子発現を調べられます。</li></ul>

<div class="jumpmenu"><a href="#navigator">&uarr;</a></div><h3 id="content_1_4"><a id="s29e8caa" href="http://MotDB.DBCLS.jp/?AJACS38%2Fhono1#s29e8caa" title="s29e8caa"><span class="sanchor">_</span></a> <a href="http://refex.dbcls.jp/" rel="nofollow"><span style="font-size:20px;display:inline-block;line-height:130%;text-indent:0px"><span class="noexists">RefEx?</span>（Reference Expression dataset）</span></a>  </h3>
<p><span style="color:green">ヒト、マウス、ラットの4つの異なる実験手法によって得られた40種類の正常組織における遺伝子発現リファレンスデータセット</span></p>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>正常組織・臓器における遺伝子発現のリファレンス
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>4つの異なる実験手法によって得られた40種類の正常組織・臓器における遺伝子発現データを並列に表現することで、手法間の比較とともに各遺伝子の発現量を直感的に比較することができます。</li></ul></li>
<li>調べたいデータに素早くたどり着くための目的別に異なる5つの検索窓
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>もっとも基本的なキーワード・遺伝子名検索では逐次的に検索語候補が提示されます。</li>
<li>『転写因子』や『Gタンパク質共役受容体』などのようなあるカテゴリーに属した遺伝子群についてまとめて検索できるよう整理されています。</li>
<li>さまざまな実験において比較対照などによく用いられる『組織特異的遺伝子』を一覧することができます。</li></ul></li>
<li>3D人体モデルを用いた遺伝子発現データの可視化
<ul class="list2" style="padding-left:16px;margin-left:16px"><li>検索結果の一覧や個々の遺伝子についての詳細ページでは、人体3Dモデルに発現量を反映させたヒートマップを表示しています。これによって、臓器・組織間における遺伝子発現の差異をより直感的に理解することができます。</li></ul></li>
<li>再利用可能で有用なパブリックデータの活用例
<ul class="list2" style="padding-left:16px;margin-left:16px"><li><span class="noexists">RefEx<a href="http://MotDB.DBCLS.jp/?cmd=edit&amp;page=RefEx&amp;refer=AJACS38%2Fhono1">?</a></span>で使用しているデータは公的データベースの中から、正常組織・臓器における遺伝子発現データのリファレンスとするにふさわしいデータセットを、測定サンプルの広範さなどを基準に選び出し、クオリティチェックを行い、互いに比較できるように整理しなおしたものです。さらに、<span class="noexists">RefEx<a href="http://MotDB.DBCLS.jp/?cmd=edit&amp;page=RefEx&amp;refer=AJACS38%2Fhono1">?</a></span>が提供するすべてのデータもまた、クリエイティブ・コモンズ (CC) ライセンス ( &#65533; DBCLS Licensed under CC 表示 2.1 日本 )のもとで、自由にダウンロードおよび再利用することができます。</li></ul></li></ul>

<div class="jumpmenu"><a href="#navigator">&uarr;</a></div><h3 id="content_1_5"><a id="d71c8bae" href="http://MotDB.DBCLS.jp/?AJACS38%2Fhono1#d71c8bae" title="d71c8bae">_</a> 【実習2】<span class="noexists">RefEx<a href="http://MotDB.DBCLS.jp/?cmd=edit&amp;page=RefEx&amp;refer=AJACS38%2Fhono1">?</a></span>を使って、組織特異的遺伝子を検索する  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>1. <a href="http://refex.dbcls.jp/" rel="nofollow">http://refex.dbcls.jp/</a>を開きます。</li>
<li>2. 画面中央の「組織特異的に発現する遺伝子を見る」の臓器アイコンにカーソルを合わせると、更に詳細な部位のアイコンが出るので、調べたい臓器（例は肝臓）をクリックします。</li>
<li>3. 一覧表示画面では、左のバーから「絞り込み検索」や「ソート項目」の切り替えができます。</li>
<li>4. 「Download」アイコンをクリックすると検索結果のタブ区切りテキストがダウンロードされます。</li>
<li>5. 各遺伝子の青字の部分（例 <a href="http://refex.dbcls.jp/gene_info.php?lang=ja&amp;db=human&amp;geneID=2243&amp;refseq=NM_000508&amp;unigene=Hs.351593&amp;probe=205649_s_at" rel="nofollow">fibrinogen alpha chain</a>）をクリックすると詳細情報を閲覧できます。</li>
<li>6. 「ヒートマップ on Bodyparts3D」では、表示する部位の切り替え（全身・体幹部・頭部）ができます。「皮膚・骨格筋を表示」もしくは「アニメーション表示」にチェックを入れるとどのように表示されるでしょうか。</li>
<li>7. 「組織40分類別データ」では、バーの上にマウスオーバーすると測定部位と発現値が表示されます。</li>
<li>8. 「Download」をクリックすると、表示中の遺伝子の組織40分類別の発現データがタブ区切り形式でダウンロードできます。</li>
<li>9. 「Probe set ID」のリンク先をクリックすると、どういう情報が参照できるでしょうか。</li>
<li>10. オーソログ対応遺伝子について、ヒトとマウスで比較してみましょう。どのような違いがあるでしょうか。</li>
<li>11. 自分の研究テーマに関連する、また興味のある遺伝子について検索してみましょう。</li></ul>
