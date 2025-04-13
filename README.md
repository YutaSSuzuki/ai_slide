## 概要

生成AIを用いてスライドを作成するためのリポジトリ<br>
スライド生成を行うAIはどれも有料課金になるため、無料でスライド作成を行うために作成した<br>
スライドの作成にはquartoを使用する。<br>

スライド化したい内容を生成AIにqmd形式で作成するように投げる。<br>
出力された内容に対し、styles.sccを適用するようにしてPDFで出力させる。


## プロンプト

とりあえず以下は埋める

1. スライドの目的
2. スライドの枚数
3. 1枚あたりの話す時間
4. スライドの内容

## ファイルに設定すべき内容

### qmd

``` qmd
---
title: "月次報告"
format:
  revealjs:
    theme: [default, styles.scss]
---
```

色を変えたい場合<br>
scssで定義した色の使い方

``` qmd
<span class="main-color-text">色付きのタイトル</span>
```



以下のコマンドでスライドを出力する。

``` bash
#スライドを確認
quarto preview slides.qmd

#スライドをhtmlに変換
quarto render slides.qmd

```

