(テーマ)ログの確認
====================================

ログはコンポーネントごとに作成され、/tmp/daqmw/log.(コンポーネント名)Compに置かれる。
ここではSampleReaderのログを確認し、SampleReaderの状態遷移の確認を行う。


ログの確認
--------------------------------
ターミナルを開いて

    % daq-emulator

サンプルコンポーネントのソースコードは /usr/share/daqmw/examples ディレクトリ
以下に入っているのでそれをコピーする。

    % mkdir ~/MyDaq
    % cd ~/MyDaq
    % cp -r /usr/share/daqmw/examples/SampleReader .
    % cp -r /usr/share/daqmw/examples/SampleMonitor .




SampleReaderの編集
--------------------------------
SampleReaderを含む/usr/share/daqmw/example以下にある全てのコンポーネントソースファイルでは
m_debug変数が定義されている。デフォルトではm_debug変数がfalseになっているが、この変数を
trueにすることによって、デバッグメッセージをログに出力させることができる。



