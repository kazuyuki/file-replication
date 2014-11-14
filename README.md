file-replication
================

■参考
http://d.hatena.ne.jp/seraphy/20120506

■KdPrint とか DbgPrint の出力先であるデバグバッファの参照方法 2013.01.25

windbg を管理者権限で起動する。

	[File] menu > [Kernel Debug]　> [Local]tab > OK

以下のコマンドでデバグ出力のマスクを「すべて出力する(0x8)」へ変更する。

	> ed Kd_DEFAULT_MASK 0x8
        
以下のコマンドでデバグバッファが出力される。

	> !dbgprint
        
