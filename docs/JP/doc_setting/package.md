packageは，いろんな機能を追加するものです．  
Pythonでいう「ライブラリ」，C/C++でいう「ヘッダーファイル」です．  

では，ファイルに書いてあるpackageについて説明を書いてきますね．  

## 画像系
### graphicx
画像を挿入したり，回転したり，拡大・縮小するためのpackageです．  
```tex
\usepackage[dvipdfmx]{graphicx}
```
画像の取り込みについては，実はLaTeX自体に機能として存在していません．  
そのため，packageとして追加してあげる必要があります．  

なお，画像の挿入例は，以下の通りです．  
```tex
\begin{figure}[htb]
    \centerline{\includegraphics[scale=0.3, clip]{hogefugapiyo.jpg}}
    \caption{関係図}
    \label{hogefugapiyo2}
\end{figure}
```
細かい使い方については，Google大先生に聞いてみてください．  
いっぱい画像をｷﾞｭｲﾝｷﾞｭｲﾝしましょうね．  ｷﾞｭｲﾝｷﾞｭｲﾝ．  

## 数式系
### \usepackage{amsmath, amssymb}
さまざまな数式記号を記述するためのpackageです  
二項演算子と関係演算子・累積・アクセント・句読点・点・矢印etc，大量に追加されます．  
内容については，以下のサイトがとても参考になります．  

[数学記号（等号、不等号、演算子、集合） - LaTeX入門](https://medemanabu.net/latex/operators/)

### \usepackage{amsthm}
定理や補題，それらの証明について書くときに使用するpackageです．  
それぞれに対して，勝手に通し番号を付けてくれます．僕は理論屋さんなので，めちゃくちゃ使っています．  

初期設定で，"theorem"や"Lemma"といった感じで英語表示されるので，```\newtheorem```を使って好きなように設定し直してください．  
以下，僕のサンプルです．  
```tex
\newtheorem{thm}{定理}
\newtheorem{lem}{補題}
\newtheorem{asm}{前提}
\newtheorem{rmk}{注意}
\newtheorem*{prb}{問題設定}
```

### \usepackage{ascmac}
枠付き文章を書くためのpackageです，研究の進捗報告書内の定理紹介とかでよく使います．  

![image](https://user-images.githubusercontent.com/64090468/203939835-e7dbf794-3241-40b4-aae9-be2afe45470c.png)

数学の教科書とカで見る感じのやつですね．  
ちなみに，生成コードは
```tex
\begin{itembox}[l]{hogeの定理}
    hogeの定理は，hoge・fugaによってhogehoge年に発表されたfugafugaについての定理である．  
    hogeは特定のfuga空間について，piyoの関係性から以下のburiburiを満たす．  
    \begin{align*}
        piyopiyo = \max_{fugafuga \in fuga} \left(\nabla buri - \nabla hoge \right)
    \end{align*}
\end{itembox}
```

## アルゴリズム系
### \usepackage{algorithmic}, \usepackage{algorithm}
模擬アルゴリズムを記載するためのpackageです．  最適化とか，最適制御の論文でよく見るやつですね．  以下のようなものが生成できるようになります．  

![image](https://user-images.githubusercontent.com/64090468/203940769-cf8035aa-dd14-4012-86c8-c190e97ed0ab.png)

ちなみに，これのコードは
```tex
\begin{algorithm}[H]
    \caption{Calculate hoge theorem with buriburi Algorithm}
    \label{BRA}
    \begin{algorithmic}[1]
        \STATE hogehoge
        \FOR{$k = 0, 1, 2, \dots$}
        \STATE 現在の$buriburi$における$buri$の$piyopiyo$を計算
        \STATE buri空間内の最大値$fugafuga$を次の$\nabla hoge$と更新
        \ENDFOR
    \end{algorithmic}
\end{algorithm}
```

以下のサイトが参考になります．  

[TeX論文にアルゴリズム（疑似コード）を書く方法 - Qiita](https://qiita.com/jirojiro/items/0ae13aac9112a804f8d5)

## 単位系
### \usepackage{siunitx}
国際単位系（SI単位系）を書くためのpackageです．
細かい使い方は，以下のサイトを参考にしてください．  

[LaTeX数値・単位 (siunitx) - Yamamoto's Laboratory](http://www.yamamo10.jp/yamamoto/comp/latex/make_doc/unit/index.php)，
[SI単位（国際単位系） - siunitxパッケージのマクロ - LaTeX入門](https://medemanabu.net/latex/siunitx-macro/)

