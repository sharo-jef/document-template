# クラン内共有文書テンプレート

クラン内共有文書のテンプレート。

## 使い方

`document.tex` を書き換えてビルドを行う。ビルド手順は後述。

### 環境

`platex`, `dvipdfmx` を利用できる環境が必要。

環境がない場合は[W32TeX](https://www.ms.u-tokyo.ac.jp/~abenori/soft/abtexinst.html)等を用いて環境を構築する。

### ビルド

`dvi`, `pdf` ファイルのビルド方法を解説する。

#### 手動

##### Windows10

`build.bat` を実行するか、以下のコマンドを実行する。

```
platex document.tex
dvipdfmx document.dvi
```

##### その他

`build.sh` を実行するか、以下のコマンドを実行する。

```
platex document.tex
dvipdfmx document.dvi
```

#### VSCode

[Run on Save (emeraldwalk)](https://marketplace.visualstudio.com/items?itemName=emeraldwalk.RunOnSave)をインストールする。

##### Windows10

デフォルト設定の状態で保存時にビルドが行われる。

##### その他

`.vscode/settings.json` の `cmd` 項目を `build` から `./build.sh` に変更することで、保存時にビルドが行われる。

### 環境

#### zenryaku環境

前略-草創 を自動挿入する環境。

```latex
\begin{zenryaku}
主文
\end{zenryaku}
```

<div style="border: 1px solid #000000;">
    前略<br />
    　主文
    <div style="text-align: right;">草々</div>
</div>

#### haikei環境

拝啓, 敬具 を自動挿入する環境。

```latex
\begin{haikei}
主文
\end{haikei}
```

<div style="border: 1px solid #000000;">
    拝啓<br />
    　主文
    <div style="text-align: right;">敬具</div>
</div>

#### kinkei環境

謹啓, 謹白 を自動挿入する環境。

```latex
\begin{kinkei}
主文
\end{kinkei}
```

<div style="border: 1px solid #000000;">
    謹啓<br />
    　主文
    <div style="text-align: right;">謹白</div>
</div>

#### kigaki環境

記書き用の環境。

```latex
\begin{kigaki}
\begin{enumerate}
    \item a
    \item b
\end{enumerate}
\end{kigaki}
```

<div style="border: 1px solid #000000;">
    <div style="text-align: center;">記</div>
    <div style="padding-left: 40px;">
        <ol>
            <li>a</li>
            <li>b</li>
        </ol>
    </div>
    <div style="text-align: right;">以 上</div>
</div>

### コマンド

#### `\jikou`

時候の挨拶を挿入するコマンド。

#### `\kansha`

感謝の挨拶を挿入するコマンド。
