# Honeypot

----

## ハニーポット？

----

- 実際のシステムのように見える囮となるシステムを用意して、それに対する攻撃を観測・記録すること。

## ハニーポットの分類

----

### サーバ型とクライアント型

- サーバ型
  - サーバを置いて、攻撃者からアクセスされるのを待つ。
- クライアント型
  - 不審なサイトにアクセスしマルウェアに自分から観戦されに行く。

### 環境

- 高対話型
  - 実際の環境を作る。
  - 本物と特定されにくい。
  - 本当に乗っ取られたりすることがある。
- 中対話型
  - 高対話型と低対話型とを組み合わせたもの。
  - 仮想環境で動かす。
- 低対話型
  - ハニーポット用のソフトウェアを用いて仮想的な環境を作る。
  - 攻撃者にバレる可能性が高いが、構築しやすい。

## 何を使う？(1代目)

----

- 何型のハニーポットか？
  - 低対話型or 中対話型のサーバ型

- Webサーバを目的に
  - OS:Dionaea
    - ネットワークに繋がっているサービスの脆弱性をつくマルウェアを捕まえ、マルウェアのコピーを得る。
    - 対応しているサービス
      - Black Hole(
        - 送信されたデータには応答しない
      - EPMAP
        - Port135の監視：Windowsのファイル共有のプロトコル
      - FTP
      - HTTP
      - Memache
        - アプリケーションの処理効率化、サーバ上のキャッシュを使う
        - 別のところからロード可能な情報に対する一時的なストレージをメモリー内に提供
      [参考URL](https://www.ibm.com/developerworks/jp/opensource/library/os-memcached/index.html)
    - Mirror
    - MongoDB
    - MQTT
    - MSSQL
    - MySQL
    - nfq
      - ポートスキャン
    - PPTP
    - SIP (VoIP)
    - SMB
      - リモート
    - TFTP
      - ファイルを扱うことができるポート69でtftpサーバーを提供
    - UPnP
      - ネットワーク機器同士の相互自動認識のプロトコル。
- Ubuntuを推奨
- sshを目的に
- ラズパイを使ってハニーポットを作る
- 観察する

## 参考URL

----

- [ハニーポットをdionaeaで構築してみた](https://qiita.com/k-onishi/items/600b14f5bc25a2418945)