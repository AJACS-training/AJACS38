# AJACS38/hono2


<p>目次</p>
<div class="contents">
<a id="contents_1"></a>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="#x426b06b"> DAVID: The Database for Annotation, Visualization and Integrated Discovery </a>
<ul class="list2" style="padding-left:16px;margin-left:16px"><li><a href="#wd2c65be"> マイクロアレイデータの準備 </a></li>
<li><a href="#t120060f"> 【実習3】DAVIDを用いて、発現データの結果を生物学的に解釈する </a></li>
<li><a href="#t120060f"> 【実習3-2】PANTHERを用いて、発現データの結果を生物学的に解釈する </a></li></ul></li>
<li><a href="#z337008a"> NCBI Gene Expression Omnibus (GEO) </a>
<ul class="list3" style="padding-left:32px;margin-left:32px"><li><a href="#lca52056"> GEOのエントリについて </a></li></ul>
<ul class="list2" style="padding-left:16px;margin-left:16px"><li><a href="#p112cdc5"> 【実習4】データセットブラウザ(Dataset browser)を利用して、GEOに登録されているマイクロアレイデータを解析する </a></li>
<li><a href="#r4b74645"> 【省略】GEO2Rを利用して、GEOに登録されているマイクロアレイデータを解析する </a></li>
<li><a href="#a83d5bfe"> 【省略】GEOを使って、自分の興味のある遺伝子の（ある実験条件下における）発現状況を調べる </a></li>
<li><a href="#ze44dc22"> 【省略】GEOを使って、自分の興味のあるマイクロアレイ実験データセットを検索&amp;生データをダウンロードする </a></li></ul></li>
<li><a href="#b6353d6e"> 【参考1】遺伝子発現バンク(GEO)目次、通称「GEO目次」 </a></li></ul>
</div>

<h3 id="content_1_0"><a id="x426b06b" href="http://MotDB.DBCLS.jp/?AJACS38%2Fhono2#x426b06b" title="x426b06b"><span class="sanchor">_</span></a> <a href="http://david.abcc.ncifcrf.gov/" rel="nofollow"><span style="font-size:20px;display:inline-block;line-height:130%;text-indent:0px">DAVID: The Database for Annotation, Visualization and Integrated Discovery</span></a>  </h3>
<p><span style="color:green">マイクロアレイデータの生物学的な解釈</span></p>
<blockquote><p class="quotation"><a href="http://david.abcc.ncifcrf.gov/" rel="nofollow">http://david.abcc.ncifcrf.gov/</a></p></blockquote>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>マイクロアレイ実験の一般的な目的は、実験条件によって得られたある遺伝子群の発現が生物学的にどういう意味を持つかを考えることです。
<div class="img_margin" style="text-align:left"><a href="http://MotDB.DBCLS.jp/?plugin=attach&amp;refer=AJACS14%2Fthecla&amp;openfile=microarray.analysis.005.png" title="microarray.analysis.005.png"><img src="http://MotDB.DBCLS.jp/?plugin=ref&amp;page=AJACS14%2Fthecla&amp;src=microarray.analysis.005.png" alt="microarray.analysis.005.png" title="microarray.analysis.005.png" width="410" height="242" /></a></div>
</li>
<li>今回は、その方法の一つとして、マイクロアレイの結果に<a href="http://www.google.co.jp/url?sa=t&amp;source=web&amp;cd=4&amp;ved=0CEEQFjAD&amp;url=http%3A%2F%2Fja.wikipedia.org%2Fwiki%2F%25E9%2581%25BA%25E4%25BC%259D%25E5%25AD%2590%25E3%2582%25AA%25E3%2583%25B3%25E3%2583%2588%25E3%2583%25AD%25E3%2582%25B8%25E3%2583%25BC&amp;ei=ve9QTd6XMtG6cbeW1KUH&amp;usg=AFQjCNF8U-O4ktlMGoR9DNC0wKltmbjtmw" rel="nofollow">Gene Ontology</a>の用語を付与することで、生物学的な解釈を行います。</li></ul>

<h3 id="content_1_1"><a id="wd2c65be" href="http://MotDB.DBCLS.jp/?AJACS38%2Fhono2#wd2c65be" title="wd2c65be">_</a> マイクロアレイデータの準備  </h3>
<p>サンプルデータとして、<a href="http://www.ncbi.nlm.nih.gov/geo/" rel="nofollow">NCBI GEO</a>より取得した公共の遺伝子発現データを用います。このデータは、ある実験の前後の2群間で有意に発現減少した遺伝子群のリストです。
<br class="spacer" />
→ <a href="http://motdb.dbcls.jp/?plugin=attach&amp;refer=AJACS24%2Fhono&amp;openfile=110208_IDlist.txt" rel="nofollow">マル秘遺伝子リスト</a>
<br class="spacer" />
（右クリックして「新しいタブで開く」もしくは「名前を付けてリンク先を保存」してください。）
<br class="spacer" />
このデータは、どのような実験から得られたデータなのか、どのように解釈できるのかをDAVIDを使って考察してみましょう！</p>

<h3 id="content_1_2"><a id="t120060f" href="http://MotDB.DBCLS.jp/?AJACS38%2Fhono2#t120060f" title="t120060f">_</a> 【実習3】DAVIDを用いて、発現データの結果を生物学的に解釈する  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/20120927.html#p01" rel="nofollow">【復習用】DAVIDを使ってマイクロアレイデータを解析する 2012</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li><a href="http://togotv.dbcls.jp/20130528.html#p01" rel="nofollow">【復習用】DAVIDの使い方 実践編</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li>1. 上部メニューの「Start Analysis」をクリックします。</li>
<li>2. 画面左側バーで、probe IDリストをコピペ or ファイルを指定します。</li>
<li>3. リストのIDの種類タイプを選択します。 … 今回は、「AFFY_ID」と「Gene List」</li>
<li>4. Submit List をクリックするとリストが読み込まれます。</li>
<li>5. アップロードしたリストは、左側バーの「List Manager」で「Uploaded List_1」として保存されています。削除やrenameもできます。</li>
<li>6. 解析を続けます。真ん中の「Functional Annotation Tool」をクリックします。</li>
<li>7. 「Gene Ontology」をクリックすると、Gene Ontologyを用いた解析の細かいメニューが表示されます。</li>
<li>8. 今回は、GOTERM_BP_FAT (BP=Biological Process)に注目します。その右の「Chart」をクリックすると結果がポップアップされます。</li>
<li>9. P-value を2回クリックしてp-valueが小さい（統計的に有意である）順にしてみましょう … p-value小さい順は、一度やればしばらく覚えているので、次からはしばらくは必要ないです
<a name="plugin_fold_anchor1"></a>
<div class="plugin_fold_title_plus" onclick="return plugin_fold_onclick(this,event,'plugin_fold_anchor1')"><p>結果</p>
</div>
<div class="plugin_fold_body"><div class="img_margin" style="text-align:left"><a href="http://MotDB.DBCLS.jp/?plugin=attach&amp;refer=AJACS24%2Fhono&amp;openfile=david_go_bp.png" title="david_go_bp.png"><img src="http://MotDB.DBCLS.jp/?plugin=ref&amp;page=AJACS24%2Fhono&amp;src=david_go_bp.png" alt="david_go_bp.png" title="david_go_bp.png" width="989" height="833" /></a></div>

</div></li>
<li>[応用編] Pathways &gt; KEGG_PATHWAY や Tissue Expression &gt; UP_TISSUE なども見てみましょう。生物学的にどういうことが言えるでしょうか。
<a name="plugin_fold_anchor2"></a>
<div class="plugin_fold_title_plus" onclick="return plugin_fold_onclick(this,event,'plugin_fold_anchor2')"><p>サンプルデータの答え</p>
</div>
<div class="plugin_fold_body"><p>Arabidopsis thaliana (シロイヌナズナ)の植物細胞と細胞壁分解酵素を用いて取り除いた植物細胞（<a href="http://ja.wikipedia.org/wiki/%E3%83%97%E3%83%AD%E3%83%88%E3%83%97%E3%83%A9%E3%82%B9%E3%83%88" rel="nofollow">プロトプラスト</a>）との比較（＝植物細胞の<a href="http://ja.wikipedia.org/wiki/%E3%82%AB%E3%83%AB%E3%82%B9_%28%E6%A4%8D%E7%89%A9%29" rel="nofollow">脱分化</a>前・後）</p>
</div></li></ul>
<p><br class="spacer" /></p>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>ところで、DAVIDと似たようなWebツールに<a href="http://pantherdb.org/" rel="nofollow">PANTHER</a>があります。</li></ul>
<blockquote><p class="quotation"><a href="http://pantherdb.org/" rel="nofollow">http://pantherdb.org/</a></p></blockquote>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>先ほどと同じデータを使って、解析結果にどのような違いがあるか調べてみましょう。
<br class="spacer" /></li></ul>
<p><br class="spacer" /></p>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>しかし、<a href="http://pantherdb.org/" rel="nofollow">PANTHER</a>では、<a href="http://pantherdb.org/tips/tips_batchIdSearch_supportedId.jsp" rel="nofollow">サポートされているID</a>が少なく、先ほどのデータのIDはそのまま使えません。</li>
<li>そこで、まずはIDの変換をします。ID変換ツールとして<a href="http://www.biomart.org/" rel="nofollow">BioMart</a><a id="notetext_1" href="#notefoot_1" class="note_super" title="参考統合TV">*1</a>などが有名ですが、今回はDAVIDのID変換機能を紹介します。
<br class="spacer" /></li></ul>
<p><br class="spacer" /></p>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>ID変換は、「<a href="http://david.abcc.ncifcrf.gov/tools.jsp" rel="nofollow">Start Analysis</a>」をクリックした先の「Analysis Wizard」の下部にある<a href="http://david.abcc.ncifcrf.gov/conversion.jsp" rel="nofollow">Gene ID Conversion Tool</a> から行います。</li>
<li>ID変換したいリストが既にアップロードしてある場合には、そのまま「Option 1: Convert the gene list being selected in left panel to」の項目を、変換したいIDに変え(今回はENTREZ_GENE_ID)、「Submit to Conversion tool」をクリックします。</li>
<li>ID変換の対応表が出力されます。右上の「Download File」から対応表をダウンロードできます。
<br class="spacer" /></li></ul>
<p><br class="spacer" /></p>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>その後、Entrez Gene ID行のみに整形したテキストファイルをPANTHERにSubmitします。
<br class="spacer" />
→ <a href="http://motdb.dbcls.jp/?plugin=attach&amp;pcmd=open&amp;file=affy_to_geneid.txt&amp;refer=AJACS35%2Fhono" rel="nofollow">変換済みマル秘遺伝子リスト</a>
<br class="spacer" /></li></ul>

<h3 id="content_1_3"><a id="t120060f" href="http://MotDB.DBCLS.jp/?AJACS38%2Fhono2#t120060f" title="t120060f">_</a> 【実習3-2】PANTHERを用いて、発現データの結果を生物学的に解釈する  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/20130430.html#p01" rel="nofollow">【復習用】PANTHERを使ってマイクロアレイデータを機能解析する</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li>1. トップページのGene List Analysisから遺伝子リストのアップロードをします。</li>
<li>2. 「Enter IDs:」にコピペするか、「Upload IDs:」から遺伝子リストのファイルをアップロードします。</li>
<li>3. 「Select List Type:	」でアップロードするリストの種類を選択します。今回は、「ID List」を選択します。</li>
<li>4. 続いて、「2.Select organism.」 で生物種を選択します。今回は、「Arabidopsis thaliana」を選択します。</li>
<li>5. 「3.Select Analysis.」で「Statistical overrepresentation test」を選択し、Submit します。</li>
<li>6. 「Select lists to analyze」で、解析するリストを確定します。続けてアップロードするリストがある場合には、ここで追加します。リストが選択されていることを確認したら、「Finished selecting lists」をクリックします。</li>
<li>7. 次にSelect Reference Listを選択します。(デフォルトではSelect List(s)で選んだ生物種のwhole-genome listが選択されるので、他の生物種と比較を行いたい場合は適宜選び直してください。)</li>
<li>8. 最後に、Search optionsを指定します。今回はデフォルトのまま GO Biological Process にチェックを入れておきます。</li>
<li>9. Launch Analysisをクリックして分析結果を表示します。</li>
<li>7. まず、P-valueの昇順でリストが表示されます。どのようなGO termが上位に来ているでしょうか。またそれらをDAVIDと比較してみましょう。</li>
<li>8. [応用編] Viewを切り替えて、さまざまなグラフ形式で解析結果を見てみましょう。生物学的にどういうことが言えるでしょうか。</li>
<li>9. その他のデータではどのような結果が表示されるでしょうか。<a href="http://motdb.dbcls.jp/?plugin=attach&amp;pcmd=open&amp;file=gse1657_adipo_up500_geneid.txt&amp;refer=AJACS38%2Fhono2" rel="nofollow">参考動画で使われているヒトの脂肪細胞の分化過程(GSE1657)で発現増加した上位500個の遺伝子群のEntrez Gene IDリスト</a></li></ul>
<hr class="full_hr" />

<h3 id="content_1_4"><a id="z337008a" href="http://MotDB.DBCLS.jp/?AJACS38%2Fhono2#z337008a" title="z337008a"><span class="sanchor">_</span></a> <a href="http://www.ncbi.nlm.nih.gov/geo/" rel="nofollow"><span style="font-size:20px;display:inline-block;line-height:130%;text-indent:0px">NCBI Gene Expression Omnibus (GEO)</span></a>  </h3>
<p><span style="color:green">世界最大の遺伝子発現（<a href="http://ja.wikipedia.org/wiki/DNA%E3%83%9E%E3%82%A4%E3%82%AF%E3%83%AD%E3%82%A2%E3%83%AC%E3%82%A4" rel="nofollow">マイクロアレイ</a>）データベース（レポジトリ）</span></p>
<blockquote><p class="quotation"><a href="http://www.ncbi.nlm.nih.gov/geo/" rel="nofollow">http://www.ncbi.nlm.nih.gov/geo/</a></p></blockquote>

<h4 id="content_1_5"><a id="lca52056" href="http://MotDB.DBCLS.jp/?AJACS38%2Fhono2#lca52056" title="lca52056">_</a> <a href="http://www.ncbi.nlm.nih.gov/geo/" rel="nofollow">GEO</a>のエントリについて  </h4>
<pre>    GEO ID 番号の最初の3文字が
    GPL:  プラットフォーム（マイクロアレイ等の型番）
    GSM: サンプル（1枚のマイクロアレイから出たデータ）
    GSE:  シリーズ（1つの実験で出たデータを集めたもの。通常複数の GSM からなる）
    GDS:  データセット（NCBIで比較可能なデータを集めて再編成したもの。GEO上で簡単な解析が可能）</pre>
<p><br class="spacer" /><br class="spacer" /></p>

<h3 id="content_1_6"><a id="p112cdc5" href="http://MotDB.DBCLS.jp/?AJACS38%2Fhono2#p112cdc5" title="p112cdc5">_</a> 【実習4】データセットブラウザ(Dataset browser)を利用して、GEOに登録されているマイクロアレイデータを解析する  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/20120128.html#p01" rel="nofollow">【復習用1】NCBI GEOの使い方3～データセットブラウザの使い方1～ 2012</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li><a href="http://togotv.dbcls.jp/20120227.html#p01" rel="nofollow">【復習用2】NCBI GEOの使い方4～データセットブラウザの使い方2～ 2012</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li>1. <a href="http://www.ncbi.nlm.nih.gov/geo/" rel="nofollow">http://www.ncbi.nlm.nih.gov/geo/</a>を開きます。</li>
<li>2.「Gene profiles」に自分の検索したい遺伝子名を入力します。</li>
<li>3. 今回は例として「<a href="http://www.google.co.jp/search?hl=ja&amp;q=Nanog%E9%81%BA%E4%BC%9D%E5%AD%90" rel="nofollow">nanog</a>」という遺伝子を検索してみましょう。入力終了後、「GO」をクリックします。</li>
<li>4. GEOに登録されている様々な実験条件で行なわれたマイクロアレイ実験におけるnanog遺伝子の発現データが表示されます。</li>
<li>5. 検索結果の<a href="http://www.ncbi.nlm.nih.gov/sites/GDSbrowser?acc=GDS2294" rel="nofollow">アクセッション番号（今回は GDS2294）</a>をクリックすると、解析用の「データセットブラウザ」が開きます。</li>
<li>6. 「<a href="http://MotDB.DBCLS.jp/?%5B%5Bhttp%3A%2F%2Fwww.ncbi.nlm.nih.gov%2Fgeoprofiles%3Fterm%3DGDS2294%5BACCN%5D%5D" title="http://www.ncbi.nlm.nih.gov/geoprofiles?term=GDS2294[ACCN" rel="nofollow">Expression profiles</a>」をクリックすると、<a href="http://MotDB.DBCLS.jp/?%5B%5Bhttp%3A%2F%2Fwww.ncbi.nlm.nih.gov%2Fsites%2Fentrez%3Fdb%3Dgeo%26cmd%3Dsearch%26term%3DGDS2294%5BACCN%5D%5D" title="http://www.ncbi.nlm.nih.gov/sites/entrez?db=geo&amp;cmd=search&amp;term=GDS2294[ACCN" rel="nofollow">この実験データセットにおける個々の遺伝子発現状況を検索できるページ</a>に飛びます。</li>
<li>7. 検索窓に表示されているアクセッション番号の後に続けて遺伝子名を追加（今回は例として <a href="http://www.google.co.jp/search?q=Oct4" rel="nofollow">Oct4</a> ）すると、この実験データセット内におけるその遺伝子の発現データが検索できます。</li>
<li>8. 「データセットブラウザ」の「<a href="http://www.ncbi.nlm.nih.gov/sites/GDSbrowser?acc=GDS2294#details" rel="nofollow">Data Analysis Tools</a>」では詳細なデータ解析が可能です。</li>
<li>9. 「Find gene name or symbol:」のところに自分の興味ある遺伝子名を入れてみましょう。</li>
<li>10. 「Find genes that are up/down for this condition(s):」の「GO」をクリックするとどのような遺伝子がヒットするでしょうか。</li>
<li>11. 「Compare 2 sets of samples」では2群間で発現に差のある遺伝子を（統計学的に）検索できます。step1で発現量の違いを検出する方法を設定します。step.2で比較する2群の設定をします。step.3の「Query Group A vs. B」をクリックすると、検索が始まります。</li>
<li>12. 「Cluster heatmaps」では、マイクロアレイデータ解析でよく用いられる<a href="http://MotDB.DBCLS.jp/?%5B%5Bhttp%3A%2F%2Fimages.google.co.jp%2Fimages%3Fq%3D%A5%D2%A1%BC%A5%C8%A5%DE%A5%C3%A5%D7%5D%5D" title="http://images.google.co.jp/images?q=ヒートマップ" rel="nofollow">ヒートマップ</a>でのデータ表示が行なえます。分類方法としてHierarchical、Partitional (K-means/K-medians)、By location on chromosomeの3種類が選べますが、それぞれどのようにデータが分類されるか試してみましょう。</li>
<li>13. ヒートマップ上をクリックすると領域選択が開始されます。リサイズや移動で範囲を決定した後、Stack up をクリックすると選択した範囲が拡大されます。</li>
<li>14. サンプルの内容とIDの対応は、元のページに戻って、Sample Subsets から確認できます。</li>
<li>15. さらに範囲選択して、Plot values をクリックすると、各遺伝子のサンプルごとの発現の様子がプロットで確認できます。</li>
<li>16. 範囲選択して、View in Entrez をクリックすると、選択範囲内のデータを棒グラフで見られます。</li>
<li>17. 範囲選択して、Download をクリックすると、選択範囲内のデータがテキスト形式でダウンロードできます。</li>
<li>18.  「Experiment design and value distribution」では実験データにおける発現の分布を参照できます。これにより、各サンプルのデータが互いに比較可能か（実験上のミスがないか）チェックすることができます。</li></ul>

<h3 id="content_1_7"><a id="r4b74645" href="http://MotDB.DBCLS.jp/?AJACS38%2Fhono2#r4b74645" title="r4b74645">_</a> 【省略】GEO2Rを利用して、GEOに登録されているマイクロアレイデータを解析する  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/20120524.html#p01" rel="nofollow">【復習用】NCBI GEOの使い方5～GEO2Rを使う～</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li>1. <a href="http://www.ncbi.nlm.nih.gov/geo/" rel="nofollow">http://www.ncbi.nlm.nih.gov/geo/</a>を開きます。</li>
<li>2. 画面中央下の「<a href="http://www.ncbi.nlm.nih.gov/geo/browse/?view=series" rel="nofollow">Series</a>」をクリックします。</li>
<li>3. 検索機能を使って興味のある実験データセットを探すことができます。</li>
<li>4. 今回は喫煙による遺伝子発現の変化に関するデータについて調べたいというモチベーションを例にするので、「cigarette smoke」と入力し、検索します。</li>
<li>5. <a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE17913" rel="nofollow">GSE17913 - Effects of Cigarette Smoke on the Human Oral Mucosal Transcriptome</a> という喫煙による口腔粘膜の遺伝子発現を調べたデータセットが見つかったので、「<a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE17913" rel="nofollow">GSE17913</a>」をクリックします。</li>
<li>6. 今回のテーマであるGEO2Rへのリンクはページ下部にあるので、リンクをクリックし<a href="http://www.ncbi.nlm.nih.gov/geo/geo2r/?acc=GSE17913" rel="nofollow">GEO2Rのページに移動</a>します。</li>
<li>7. このデータセットに含まれるサンプルの一覧が表示されます。列見出しをクリックすると各項目でソートできます。「Title」をクリックすると、今回のデータセットが、喫煙者・非喫煙者のそれぞれ男性・女性の頬粘膜(buccal mucosa)から得られたサンプルであることがわかります。</li>
<li>8. 比較したいグループをそれぞれ設定します。「Define groups」をクリックして、それぞれのグループ名を入力します。今回は、非喫煙者の女性(never_smoker_F)と、喫煙者の女性(smoker_F)のサンプルをそれぞれグループ化します。</li></ul>
<p><span style="color:red">（※GEO2Rの各ジョブの実行は時間がかかるので要注意。講習では<a href="http://togotv.dbcls.jp/20120524.html#p01" rel="nofollow">復習用統合TV</a>の実行結果を見ながら進めるので、実行しないでください。）</span></p>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li>9. グループに入れたいサンプルをクリックやドラッグで選択してからグループ名をクリックすると、サンプルがグループに登録されます。</li>
<li>10. 次に、「Samples」をクリックした後、「Value distribution」タブをクリックし、「View」をクリックすると各サンプルの発現分布を調べることができます。</li>
<li>11. 発現分布が箱ひげ図で示されます。データセットブラウザと異なり、GEO2R では投稿された生のデータを用いて解析されます。</li>
<li>12. &quot;Export&quot; をクリックすると、箱ひげ図で与えられている値をまとめたタブ区切りテキストが表示され、これらを保存できます。</li>
<li>13. GEO2R タブに戻り、&quot;Top 250&quot; をクリックすると、選択したグループ間で各遺伝子の発現量に差があるかどうかの t 検定の結果、P 値が小さい順に 250 件表示されます。&quot;P.Value&quot; は元の P 値、&quot;adj.P.Val&quot; は多重検定の補正をかけた後の P 値です。有意性の評価は adj.P.Val に基づいています。
&quot;t&quot; は普通の t の標準偏差を全遺伝子の標準偏差を用いて調整したもの (moderated-t) です。普通の t より精度が上がっていますが、普通の t 分布に従うものとして扱えます。 &quot;B&quot; は2つのグループで発現量が異なっている対数オッズ値です。exp(B)/(1+exp(B)) の値が、発現量が異なっている確率で
す。&quot;logFC&quot; は、発現量の差が何倍であるかを2底の対数にしたものです。つまり値が 2 なら 4 倍の差を示しています。ここでの解析では発現量が対数で与えられている必要がありますが、元のデータでは対数になっていないことがあります。そのような場合デフォルトでは自動検出し、対数変換して計算してくれます。その上でこのような表示がされます。</li>
<li>14. 行をクリックすると、その行の遺伝子の各サンプルでの発現量グラフが見られます。</li>
<li>15. 今回喫煙者女性・非喫煙者女性間で最も差が大きいとされた遺伝子であるシトクロム P450 (異物代謝に関わる遺伝子)は、喫煙者群で有意に発現増加したことがわかります。</li>
<li>16. &quot;Sample values&quot; をクリックすると、発現量の値が一覧できます。</li>
<li>17. &quot;Select columns&quot; をクリックすると、表示するカラムを変更できます。 &quot;logFC&quot; を消し &quot;GO.Function&quot; を追加してみましょう。</li>
<li>18. &quot;Save all results&quot; をクリックすると、結果をテキストで表示・保存できます。</li>
<li>19. Options タブをクリックすると、いくつかの設定を変更できます。右の項目は多重検定の補正法の選択です。デフォルトでは Benjamini &amp; Hochberg の方法が使われていますが、これを Bonferroni の方法に変更してみます。中央はデータの対数をとるかどうかの選択です。デフォルトでは先程説明したとおり自動検出です。左の項目はプラットフォームの注釈の選択です。&quot;NCBI generated&quot; がある場合はそれの方が信頼できます。</li>
<li>20. Options に変更を加えたら、GEO2R タブに戻って &quot;Recalculate&quot; をクリックします。 変更を反映した計算結果が表示され、多重検定の補正法を変更したため、adj.P.Val が変わっていることがわかります。</li>
<li>21. Profile graph の項目では、プローブ ID を元に、個々の遺伝子の発現状況を調べることができます。</li>
<li>22. 「View data for (platform ID)」をpクリックするとプラットフォームの情報が表示されるので、目的の遺伝子のプローブ ID を、ブラウザの検索機能 (Ctrl+F)を用いて調べます。今回は例としてNFE2L2（酸化ストレスによって活性化する転写因子）を検索してみましょう。</li>
<li>23. 一番左がプローブIDなので、これをコピーし、さきほどの&quot;Enter ID&quot; の窓にプローブ ID をペーストし、&quot;Set&quot; をクリックすると。発現量のグラフが表示されます。（なおこの操作では、何の計算も実行されないので、検定の結果の P 値を調べることはできません。）</li>
<li>24. R script タブをクリックするとこれまでに実際に実行された R のスクリプトを見ることができます。これを参考に、手元の R でパラメータを調整するなどして更なる解析を行うことができます。</li>
<li>R の使い方については、下記の統合TV のコンテンツ「統計解析ソフト「R」の使い方」シリーズをご覧ください。</li>
<li><a href="http://togotv.dbcls.jp/20090618.html#p01" rel="nofollow">統計解析ソフト「R」の使い方 ～導入編～</a></li>
<li><a href="http://togotv.dbcls.jp/20091219.html#p01" rel="nofollow">統計解析ソフト「R」の使い方 ～ヒートマップ編～</a></li>
<li><a href="http://togotv.dbcls.jp/20111107.html#p01" rel="nofollow">統計解析ソフト「R」での立廻り</a></li></ul>

<h3 id="content_1_8"><a id="a83d5bfe" href="http://MotDB.DBCLS.jp/?AJACS38%2Fhono2#a83d5bfe" title="a83d5bfe">_</a> 【省略】GEOを使って、自分の興味のある遺伝子の（ある実験条件下における）発現状況を調べる  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/20111020.html#p01" rel="nofollow">【復習用】NCBI GEOの使い方2～遺伝子プロファイルの検索・処理済みデータの取得～ 2011</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li>1. <a href="http://www.ncbi.nlm.nih.gov/geo/" rel="nofollow">http://www.ncbi.nlm.nih.gov/geo/</a>を開きます。</li>
<li>2.「Gene profiles」に自分の検索したい遺伝子名を入力します。</li>
<li>3. 今回は例として「<a href="http://www.google.co.jp/search?hl=ja&amp;q=Nanog%E9%81%BA%E4%BC%9D%E5%AD%90" rel="nofollow">nanog</a>」という遺伝子を検索してみましょう。入力終了後、「GO」をクリックします。</li>
<li>4. GEOに登録されている様々な実験条件で行なわれたマイクロアレイ実験における「nanog」遺伝子の発現データが表示されます。</li>
<li>5. 検索結果の右端にある画像をクリックすると、<a href="http://www.ncbi.nlm.nih.gov/geo/gds/profileGraph.cgi?&amp;dataset=DEAryz&amp;dataset=yyyzzz$&amp;gmin=5173.000000&amp;gmax=11680.000000&amp;absc=&amp;gds=2294&amp;idref=161072_at&amp;annot=Nanog" rel="nofollow">発現データの詳細をみる</a>ことができます。</li>
<li>6. <a href="http://www.ncbi.nlm.nih.gov/sites/GDSbrowser?acc=GDS2294" rel="nofollow">このサンプル（GDS2294）</a>では、nanogはどういう細胞のどういう実験条件で発現が増減しているか調べてみましょう。</li>
<li>7. ページ下部の「samples」に列挙された<a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM130365" rel="nofollow">リンク</a>をクリックすると、そのサンプル（一枚のマイクロアレイ）の詳細を閲覧できます。</li>
<li>8. <a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM130365" rel="nofollow">リンク先のページ</a>の中ほどにある<a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE5583" rel="nofollow">「series」のリンク</a>をクリックすると、この実験全体の詳細情報が見られます。</li>
<li>9. <a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE5583" rel="nofollow">この実験全体の詳細情報ページ</a>の下部にある<a href="ftp://ftp.ncbi.nih.gov/pub/geo/DATA/SeriesMatrix/GSE5583/" rel="nofollow">「Series Matrix File(s)」</a>をクリックすると、この実験の正規化補正済みのマイクロアレイデータをダウンロードすることができます。</li></ul>

<h3 id="content_1_9"><a id="ze44dc22" href="http://MotDB.DBCLS.jp/?AJACS38%2Fhono2#ze44dc22" title="ze44dc22">_</a> 【省略】GEOを使って、自分の興味のあるマイクロアレイ実験データセットを検索&amp;生データをダウンロードする  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/20110711.html#p01" rel="nofollow">【復習用】NCBI GEOの使い方1～マイクロアレイデータの検索・取得～ 2011</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li>1. <a href="http://www.ncbi.nlm.nih.gov/geo/" rel="nofollow">http://www.ncbi.nlm.nih.gov/geo/</a>を開きます。</li>
<li>2. 画面中央の「Platforms」をクリックします。</li>
<li>3. <a href="http://www.informatics.jax.org/javawi2/servlet/WIFetch?page=imageSummaryByMrk&amp;key=25000&amp;imageType=8" rel="nofollow">Platform(マイクロアレイの種類)の一覧画面が現れる</a>ので、上部の「FIND PLATFORM」をクリックします。</li>
<li>4. <a href="http://www.ncbi.nlm.nih.gov/geo/query/browse.cgi?mode=findplatform" rel="nofollow">platformの検索画面</a>が現れるので、「Company name」に「Affymetrix」、「organism」に「Homo sapiens」を選択し、「FIND PLATFORM」をクリックします。</li>
<li>5. <a href="http://www.ncbi.nlm.nih.gov/geo/query/browse.cgi?mode=foundplatform" rel="nofollow">Affymetrixのヒトのマイクロアレイの検索結果</a>が表示されるので、中程にある「Affymetrix <span class="noexists">GeneChip<a href="http://MotDB.DBCLS.jp/?cmd=edit&amp;page=GeneChip&amp;refer=AJACS38%2Fhono2">?</a></span> Human Genome U133 Plus 2.0 Array」の左端にある<a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GPL570" rel="nofollow">「GPL570」というID</a>をクリックします。</li>
<li>6. <a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GPL570" rel="nofollow">表示された画面</a>の真ん中あたりにある「series」下の「More...」をクリックすると、登録されているデータセットを閲覧できます。</li>
<li>7. ブラウザの検索ボタンなどを使って「reprogramming」という単語を検索するとどういうデータがヒットするでしょうか？</li>
<li>8. ヒットしたデータの左端にあるIDをクリックすると、<a href="http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE9832" rel="nofollow">そのデータセットの詳細情報</a>が閲覧できます</li>
<li>9. ページ下部の「Download family」の中にある「Series Matrix File(s)」をクリックすると正規化済みのデータのダウンロードリンクが表示されます。</li>
<li>10. ページ最下部の「Supplementary file」にあるリンクから生データをダウンロードすることができます。</li>
<li>11. 自分の研究テーマに近い、また興味のあるマイクロアレイデータが利用可能か検索してみましょう。</li></ul>

<h3 id="content_1_10"><a id="b6353d6e" href="http://MotDB.DBCLS.jp/?AJACS38%2Fhono2#b6353d6e" title="b6353d6e"><span class="sanchor">_</span></a> 【参考1】<a href="http://lifesciencedb.jp/geo/" rel="nofollow">遺伝子発現バンク(GEO)目次、通称「GEO目次」</a>  </h3>
<ul class="list1" style="padding-left:16px;margin-left:16px"><li><a href="http://togotv.dbcls.jp/20080623.html#p01" rel="nofollow">使い方参考動画 遺伝子発現バンク(GEO)目次を使い倒す－その壱</a> <a href="http://lifesciencedb.jp/image/small_video_icon.png" rel="nofollow"><img src="http://lifesciencedb.jp/image/small_video_icon.png" alt="http://lifesciencedb.jp/image/small_video_icon.png" /></a></li>
<li>NCBI GEO を日本語のインターフェイスで快適に使い、データの全容を俯瞰するための仕組みです。数多く登録されている遺伝子発現データの大まかな傾向をつかむのに役に立つことでしょう。</li>
<li>検索結果のRSS配信機能があるので、これを活用して、遺伝子発現データの新規登録の有無をチェックできます（便利！）。</li></ul>
