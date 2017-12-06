# samba
テープドライブを接続したLinuxで解凍したログを、<br>
オフィス内のプライベートネットワークでファイル共有するための構築。

「とりあえずWindowsからファイルが見れればよし」のノーガードな設定。

# 環境
CentOS Linux release 7.4.1708 (Core)<br>
samba-4.6.2-11.el7_4.x86_64


【おまけ】
# ノートPCを閉じてもスリープさせない設定
設定ファイルをバックアップ<br>
$ cp /etc/systemd/logind.conf /etc/systemd/logind.conf.bak<br>
$ vi /etc/systemd/logind.conf<br>

HandleLidSwitch=suspend
この行を以下のように変更<br>
HandleLidSwitch=ignore
変更後、以下のコマンドで反映
$ systemctl restart systemd-logind.service
