---
title: "Importing data into OpenRefine"
> OpenRefineへのデータのインポート

teaching: 10
exercises: 5
questions:
- "How do I get data into OpenRefine?"
> データを OpenRefine に取り込むにはどうすればよいですか?

objectives:
- "Successfully import data into OpenRefine"
>データを OpenRefine に正常にインポートする

keypoints:
- "Use the `Create Project` option to import data"
>「プロジェクトの作成」オプションを使用してデータをインポートします

- "You can control how data imports using options on the import screen"
> インポート画面のオプションを使用して、データのインポート方法を制御できます

- "Several files types may be imported into OpenRefine."
> OpenRefine には、いくつかのファイルタイプをインポートできます。
---

## Importing data
> データのインポート

>## What kinds of data files can I import?
> どのような種類のデータ ファイルをインポートできますか?

>There are several options for getting your data set into OpenRefine. You can upload or import files in a variety of formats including:
>>データセットを OpenRefine に取り込むためのオプションがいくつかあります。次のようなさまざまな形式のファイルをアップロードまたはインポートできます。

>* TSV (tab-separated values)
>* CSV (comma-separated values)
>* TXT
>* Excel
>* JSON (javascript object notation)
>* XML (extensible markup language)
>* Google Spreadsheet
{: .callout}

>## Create your first OpenRefine project (using provided data)
>> 最初の OpenRefine プロジェクトを作成します (提供されたデータを使用)
>
> To import the data for the exercise below, follow the instructions in [Setup](https://librarycarpentry.github.io/lc-open-refine/setup.html) to download the data and run OpenRefine. *NOTE: If OpenRefine does not open in a browser window, open your browser and type the address <http://127.0.0.1:3333/> to take you to the OpenRefine interface.*
>> 以下の演習用のデータをインポートするには、セットアップの指示に従ってデータをダウンロードし、OpenRefine を実行します。注: OpenRefine がブラウザ ウィンドウで開かない場合は、ブラウザを開いてアドレスhttp://127.0.0.1:3333/を入力し、OpenRefine インターフェイスに移動します。

>
>1. Once OpenRefine is launched in your browser, click `Create Project` from the left hand menu and select `Get data from This Computer`
>> 1. ブラウザーで OpenRefine が起動したらCreate Project、左側のメニューからをクリックして、Get data from This Computer

>2. Click `Choose Files` (or 'Browse', depending on your setup) and locate the file which you have downloaded called `doaj-article-sample.csv`
>> 2. Choose Files(またはセットアップに応じて「参照」) をクリックし、doaj-article-sample.csvと呼ばれるダウンロードしたファイルを見つけます。

>3. Click `Next»` - the next screen (see below) gives you options to ensure the data is imported into OpenRefine correctly. The options vary depending on the type of data you are importing.
>> Nextをクリック、»- 次の画面 (以下を参照) で、データが OpenRefine に正しくインポートされるようにするためのオプションが表示されます。オプションは、インポートするデータのタイプによって異なります。

>4. Click in the `Character encoding` box and set it to `UTF-8`. This ensures that OpenRefine correctly interprets the imported data as UTF-8 encoded. If you don't select this you may find that some special characters (e.g. smart quotation marks) are not displayed correctly.
>> 4. Character encodingボックス内をクリックして、UTF-8に設定します。これにより、OpenRefine がインポートされたデータをUTF-8 エンコードとして正しく解釈することが確実になります。これを選択しないと、一部の特殊文字 (スマート引用符など) が正しく表示されないことがあります。

>5. Ensure the first row is used to create the column headings by checking the box `Parse next 1 line(s) as column headers`
>> 5. ボックス(次の1行を列ヘッダとしてパースする)をチェックして、最初の行が列見出しの作成に使用されるようにします。

>6. OpenRefine will automatically select “Use character” to enclose cells containing column separators (such as a comma) as part of their data. This will make sure that OpenRefine doesn't misinterpret any commas (or other characters) within the column data as a delimiter. Keep this option selected.
>> 6. OpenRefine は自動的に「利用する文字」を選択して、データの一部として列区切り文字 (コンマなど) を含むセルを囲みます。これにより、OpenRefine が列データ内の複数のコンマ (またはその他の文字) を区切り文字として誤って解釈しないことが保証されます。このオプションは、選択したままにします。

>7. From OpenRefine 3.4 onwards there is an option to Trim leading & trailing whitespace from strings when importing separator-based files. Keeping this checked will ensure that values like `English` and `English `, which differ by a single trailing space, are not treated as different values after the import
>> 7. OpenRefine3.4 以降では、セパレーターベースのファイルをインポートするときに、文字列から先頭と末尾の空白をトリムするオプションがあります。これをチェックしたままにしておく「English」と「English 」のような末尾のスペースが1つ異なる値が、インポート後に異なる値として扱われないことが保証されます。
>8. Make sure the `Attempt to parse cell text into numbers` box is not checked, so OpenRefine doesn't try to automatically detect numbers as it may cause errors such as confusion between date formats (e.g. DD/MM/YYYY vs MM/DD/YYYY)
>> 8. セルのテキストを数値に変換するボックスがチェックされていないことを確認してください。これにより、OpenRefineは数値を自動的に検出しようとしません。これは、日付形式間の混同のようなエラーを引き起こす可能性があるためです (例: DD/MM/YYYY と MM/DD/YYYY)。

>9. The Project Name box in the upper right corner will default to the title of your imported file. Click in the `Project Name` box to give your project a different name, if desired.
>> 9. 右上隅の プロジェクト名ボックスには、インポートしたファイルのタイトルがデフォルトで表示されます。必要に応じて、プロジェクト名ボックスをクリックし、プロジェクトに別の名前を付けます。

>10. Once you have selected the appropriate options for your project, click the `Create project »` button at the top right of the screen. This will create the project and open it for you. Projects are saved as you work on them, there is no need to save copies as you go along.
>> 10. プロジェクトに適切なオプションを選択したら、Create projectという画面の右上にあるボタンをクリックします。これにより、プロジェクトが作成され、プロジェクトが開かれます。プロジェクトは作業中に保存されます。作業中にコピーを保存する必要はありません。

>   
> ![Screenshot of Open Refine Create Project Screen](../assets/img/openrefine_ui.png)
{: .checklist}

To open an existing project in OpenRefine you can click `Open Project` from the main OpenRefine screen (in the left hand menu). When you click this, you will see a list of the existing projects and can click on a project's name to open it.
> OpenRefine で既存のプロジェクトを開くには、OpenRefineOpen Projectのメイン画面 (左側のメニュー) をクリックします。これをクリックすると、既存のプロジェクトのリストが表示され、プロジェクト名をクリックして開くことができます。

### Going Further
>> もっと遠く行く

* Look at the other options on the Import screen - try changing some of these options and see how that changes the Preview and how the data appears after import.
> インポート画面の他のオプションを見てください。これらのオプションのいくつかを変更してみて、プレビューがどのように変化するか、およびインポート後にデータがどのように表示されるかを確認してください。

* Do you have access to JSON or XML data? If so the first stage of the import process will prompt you to select a 'record path' - that is the parts of the file that will form the data rows in the OpenRefine project.
> JSON または XML データにアクセスできますか? その場合、インポート プロセスの最初の段階で、「レコード パス」を選択するよう求められます。これは、OpenRefine プロジェクトのデータ行を形成するファイルの部分です。

