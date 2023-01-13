# TwinCATが対応するリアルタイムEthernetドライバの互換性はどのように調べますか？

[関連InfoSys](https://infosys.beckhoff.com/content/1033/tc3_overview/9309844363.html?id=1489698440745036069)

デバイスマネージャからEthernetボードを選択し、詳細タブからプロパティにて「ハードウェアID」を選ぶと一覧される内容から読み取れます。
VEN_に続く文字がベンダーIDで、DEV_に続く文字がデバイスIDです。

![](image003.png)

この値が、 [InfoSysサイト](https://infosys.beckhoff.com/content/1033/tc3_overview/9309844363.html?id=1489698440745036069) で案内しているサポートするリアルタイムEthernetドライバに含まれるか確認してください。

BSDの場合、 ``lspci`` に ``-nn`` オプションを付けて、その出力からethernetという文字が含まれる行をフィルタリングして得られます。

```shell
$ lspci -nn | grep -i ethernet
00:1f.6 Ethernet controller [0200]: Intel Corporation Ethernet Connection (2) I219-LM [8086:15b7] (rev 31)
```

の様に末尾に "[vendor ID:device ID]" の書式で表示されます。

# サイトに掲載されているNICなのですがCompatibleとして認識されません

掲載一覧に記されているベンダIDとデバイスIDは、先頭に記載されている、 ``Last updated: TwinCAT *.* ****`` のTwinCATバージョンで対応したものです。
このバージョンより古いために未対応の可能性があります。記載されているTwinCATへのアップグレードをご検討ください。
