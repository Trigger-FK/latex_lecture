## \documentclass
documentclassとは，「どんな文章を書くのか」というのを設定できるものだと思っています．  
以下のように記述します．
```tex
\documentclass[option]{paper class}
```
optionには文字サイズだったり，紙のサイズだったりを入力します．  
また，`paper class`では`article`, `report`, `book`の設定ができます．  
ここで，ファイル内のコードを見てみましょう．
```tex
\documentclass[11pt, a4paper, titlepage]{jsarticle}
```
訳：**文字サイズ11ptで，A4サイズのarticleを生成してくれ．あ，表紙込みでｵﾅｼｬｽ．**