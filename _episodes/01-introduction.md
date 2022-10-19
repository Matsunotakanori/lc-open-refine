---
title: "Introduction to OpenRefine"
teaching: 15
exercises: 0
questions:
- "What is OpenRefine? What can it do?"
objectives:
- "Explain what the OpenRefine software does"
- "Explain how the OpenRefine software can help work with data files"
keypoints:
- "OpenRefine is 'a tool for working with messy data'"
- "OpenRefine works best with data in a simple tabular format"
- "OpenRefine can help you split data up into more granular parts"
- "OpenRefine can help you match local data up to other data sets"
- "OpenRefine can help you enhance a data set with data from other sources"
---
questions:
- "What is OpenRefine? What can it do?"
> 質問<p>
OpenReinfeとは何か？。どんなことができるのか？<p>

objectives:
- "Explain what the OpenRefine software does"
> 目的
> OpencRefineのソフトウェアできることを説明すること。
- "Explain how the OpenRefine software can help work with data files"
> OpenRefineのソフトウェアがデータファイルの操作を助けてくれることを説明すること。

keypoints:
- "OpenRefine is 'a tool for working with messy data'"
>　キーポイント<p>
OpenRefineは、乱雑なデータを操作するためのツールです。

- "OpenRefine works best with data in a simple tabular format"
> OpenRefineは、単純な表形式のデータで最適に機能します。

- "OpenRefine can help you split data up into more granular parts"
> - OpenRefine は、データを細かい部分に分割するのに役立ちます

- "OpenRefine can help you match local data up to other data sets"
> OpenRefineは、ローカルデータと他のデータセットとの照合に役立ちます。

- "OpenRefine can help you enhance a data set with data from other sources"
> OpenRefineは、他の情報源のデータでデータセットを拡張することに役立ちます。
---

## What is OpenRefine?
>OpenRefineとは？

 OpenRefine is a desktop application that uses your web browser as a graphical interface. 
 > OpenRefineは、お使いのWebブラウザのグラフィカルインターフェイスを利用するデスクトップアプリケーションです。

 It is described as "a power tool for working with messy data" ([David Huynh](http://web.archive.org/web/20141021040915/http://davidhuynh.net/spaces/nicar2011/tutorial.pdf)) - but what does this mean? 
 > David Huynhは、「乱雑なデータを処理する強力なツール」(http://web.archive.org/web/20141021040915/http://davidhuynh.net/spaces/nicar2011/tutorial.pdf)と説明してますが、これはどういう意味でしょう？
 
 It is probably easiest to describe the kinds of data OpenRefine is good at working with and the sorts of problems it can help you or your team solve.
 > これは、OpenRefineが処理を得意とするデータの種類やあなたやあなたのチームが解決できる問題の種類を説明するのことがおそらくもっとも簡単です。

OpenRefine is most useful where you have data in a simple tabular format such as a spreadsheet, a comma separated values file (csv) or a tab delimited file (tsv) but with internal inconsistencies either in data formats, or where data appears, or in terminology used. 
> OpenRefineは、スプレッドシート、カンマ区切り値ファイル（csv）、タブ区切りファイル（tsv）などの単純な表形式のデータを持っているが、データ形式、データのある位置、使用する用語のいずれかに整合性ない場合に最も有用です。

OpenRefine can be used to standardize and clean data across your file. It can help you:
> OpenRefineは、ファイル全体のデータを標準化し、きれいにすることで利用できます。それはあなたに役立ちます。

* Get an overview of a data set
> データセットの概要を取得する

* Resolve inconsistencies in a data set, for example standardizing date formatting
> 日付形式の標準化など、データ セット内の不整合を解決する

* Help you split data up into more granular parts, for example splitting up cells with multiple authors into separate cells
> 複数の作成者のセルを個別のセルに分割するなど、データをより細かい部分に分割するのに役立ちます

* Match local data up to other data sets - for example, in matching forms of personal names against name authority records in the Virtual International Authority File (VIAF)
> ローカル データを他のデータ セットと照合します。たとえば、個人名の形式をバーチャル国際典拠ファイル(VIAF) の氏名典拠レコードと照合します。

* Enhance a data set with data from other sources
> 他のソースからのデータでデータセットを拡張する。



Some common scenarios might be:
> 一般的なシナリオは次のとおり。

* Where you want to know how many times a particular value (name, publisher, subject) appears in a column in your data
> 特定の値 (氏名、出版者、件名) がデータの列に何回出現するかを知りたい場合

* Where you want to know how values are distributed across your whole data set
> データセット全体で値がどのように分布しているかを知りたい場合

* Where you have a list of dates which are formatted in different ways, and want to change all the dates in the list to a single common date format. For example:
> さまざまな方法で書式設定された日付のリストがあり、リスト内のすべての日付を単一の共通の日付形式に変更したい場合。例えば：

| Data you have   | Desired data |
|-----------------|:-------------|
| 1st January 2014| 2014-01-01   |
| 01/01/2014      | 2014-01-01   |
| Jan 1 2014      | 2014-01-01   |
| 2014-01-01      | 2014-01-01   |

* Where you have a list of names or terms that differ from each other but refer to the same people, places or concepts. For example:
> それぞれが互いに異なるが、同じ人、場所、または概念を参照する名前または用語のリストがある場合。例えば：

| Data you have   | Desired data |
|-----------------|:-------------|
| London          | London       |
| London]         | London       |
| London,]        | London       |
| london          | London       |

* Where you have several bits of data combined together in a single column, and you want to separate them out into individual bits of data with one column for each bit of the data. For example going from a single address field (in the first column), to each part of the address in a separate field:
> いくつかのデータビットを1つの列に結合し、データのビットごとに1つの列を使用して、それらを個々のデータビットに分離したい場合。たとえば、単一の住所フィールド (最初の列) から、別のフィールドの住所の各部分に移動します。

| Address in single field | Institution  | Library name  | Address 1 | Address 2 | Town/City | Region | Country | Postcode |
|-------------------------|:-------------|:-------------|:-------------|:-------------|:-------------|:-------------|:-------------|:-------------|
| University of Wales, Llyfrgell Thomas Parry Library, Llanbadarn Fawr, ABERYSTWYTH, Ceredigion, SY23 3AS, United Kingdom | University of Wales | Llyfrgell Thomas Parry Library | Llanbadarn Fawr | | Aberystwyth | Ceredigion | United Kingdom | SY23 3AS |
| University of Aberdeen, Queen Mother Library, Meston Walk, ABERDEEN, AB24 3UE, United Kingdom | University of Abderdeen | Queen Mother Library | Meston Walk | | Aberdeen | | United Kingdom | AB24 3UE |
| University of Birmingham, Barnes Library, Medical School, Edgbaston, BIRMINGHAM, West Midlands, B15 2TT, United Kingdom | University of Birmingham | Barnes Library | Medical School | Edgbaston | Birmingham | West Midlands | United Kingdom | B15 2TT |
| University of Warwick, Library, Gibbett Hill Road, COVENTRY, CV4 7AL, United Kingdom | University of Warwick | Library | Gibbett Hill Road | | Coventry | | United Kingdom | CV4 7AL |

* Where you want to add to your data from an external data source:
> 外部の情報源(データソース）からデータに追加したい場合:

| Data you have   | Date of Birth from VIAF (Virtual International Authority File) | Date of Death from VIAF (Virtual International Authority File) |
|-----------------|:-------------|:-------------|
| Braddon, M. E. (Mary Elizabeth) | 1835 | 1915 |
| Rossetti, William Michael       | 1829 | 1919 |
| Prest, Thomas Peckett           | 1810 | 1879 |

## What Should I Know When Working With OpenRefine?
> OpenRefine を使用する際に知っておくべきことは何か?

* No internet connection is needed, and none of the data or commands you enter in OpenRefine are sent to a remote server.
> インターネット接続は必要なく、OpenRefine に入力したデータやコマンドはリモート サーバーに送信されません。

* You are NOT modifying original/raw data.
> 元データや生データを変更することはありません。

* Projects are autosaved every five minutes and when OpenRefine is properly shut down (Ctrl+C). See [History in User Manual](https://docs.openrefine.org/manual/running/#history-undoredo) for details.
>「プロジェクト」は 5 分ごとに自動保存され、OpenRefine が適切にシャットダウンされたとき (Ctrl+C) に保存されます。詳細については、ユーザー マニュアルの履歴を参照してください。

* Files are saved locally such that if you are working on two computers you will have to export/import files/projects.
> ファイルはローカルに保存されるため、2台のコンピューターで作業している場合は、ファイル又はプロジェクトをエクスポート又はインポートする必要があります。
