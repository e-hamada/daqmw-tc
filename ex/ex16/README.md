(テーマ) Mergerを利用して複数台のPCからデータを収集する
===============================================================

ex11で~/MyDaq/にSampleReaderとSampleMonitorから構成される
システムを作成した。
このシステムに２つのSampleReaderとMergerを追加し、以下のようなシステムを作成する。

emulator --- SampleReader  ---\
emulator --- SampleReader2 --- Merger --- SampleMonitor
emulator --- SampleReader3 ---/


SampleReaderのコピー
--------------------------------
SampleReaderをコピーし、名前を変える

    % cd ~/MyDaq/
    % cp -r /usr/share/daqmw/examples/SampleReader/ SampleReader2
    % cp -r /usr/share/daqmw/examples/SampleReader/ SampleReader3
    % cd SampleReader2
    % cp /usr/share/daqmw/examples/change-SampleComp-name/change-SampleReader-name.sh .

change-SampleReader-name.shの中を修正
修正前）　new_name_camel_case=RawDataReader

修正後）　new_name_camel_case=SampleReader2





