(テーマ) ROOTを使ってグラフを書く
=================================

素粒子原子核分野ではROOT(http://root.cern.ch/)を使ってヒストグラム、
グラフを書くことが多い。
ヒストグラムを書く方法は周知と思うがグラフはヒストグラムよりは書かれる
機会がないと思うのでここで取り上げる。

bs/draw_graphに放物線を書くプログラムをおいてあるのでコピー、コンパイルして
動かし、コードを読みグラフの書きかたを習得すること。

ROOTではC++プログラムをコンパイルするのに必要なインクルードファイル、
ライブラリファイルの指定を簡略化するためにroot-configというコマンドを
用意している。Makefile中で以下のように指定しているので見ておく。

    CPPFLAGS += -I$(shell ${ROOTSYS}/bin/root-config --incdir)
    LDLIBS   += $(shell ${ROOTSYS}/bin/root-config --glibs)


