# samba
オフィス内で、テープドライブから解答したログを共有するための、簡単なファイル共有サーバの構築
「とりあえずWindowsからファイルが見れればよし」のノーガードな設定です。

【環境】
CentOS Linux release 7.4.1708 (Core)
samba-4.6.2-11.el7_4.x86_64






【おまけ】
[ノートPCを閉じてもスリープさせない設定]
設定ファイルをバックアップ
# cp /etc/systemd/logind.conf /etc/systemd/logind.conf.bak
# vi /etc/systemd/logind.conf

#HandleLidSwitch=suspend
この行を以下のように変更
HandleLidSwitch=ignore
変更後、以下のコマンドで反映
systemctl restart systemd-logind.service
