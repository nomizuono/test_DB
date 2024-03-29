# 論理設計と物理設計
## 学習のポイント
- 論理設計は物理設計に先立つ
- ファイルレベルで物理設計を考える
- サイジングは難しい
- RAIDは信頼性、性能、そして”財布”を考慮して決める
- バックアップおよびリカバリの設計は地味なタスクだがおろそかにしない。
  - 新聞に載るかも？w
## 概念スキーマと論理設計
- 「整合的で筋道が通っている」という意味ではなく、「物理層の制約にとらわれない」といった考えで設計をする。
- システム開発におけるデータベース設計は、以下の手順
1. 概念スキーマ(論理設計)
2. 内部スキーマ(物理設計)
### 論理設計のSTEP
1. エンティティの抽出
2. エンティティの定義
3. 正規化
4. ER図の作成
### エンティティの実態
- 日本語では「実態」と訳す。具体的には「顧客」や「社員」「店舗」といった物理的実体を伴ったもの
- 「税」や「会社」「注文履歴」のように物理的実体を伴わない、単なる概念というニュアンスもある
- リレーショナルデータベースでは、エンティティを最終的に、「テーブル」という物理的単位で格納することになる
- このタスクの一部は「要件定義」である
- どのようなエンティティが必要になるかという問いは、どういうデータベースを扱いたいという問いになる
- エンティティ抽出は、ある程度、顧客やシステム利用者と要件を詰めていく中で実施することになる
### エンティティの定義
- エンティティは、データを「属性(attribute)」という形で保持する
  - 二次元表における「列」と同義である
- 各表がどのような「列」を持つか、ということを定義する
- 特に重要なのが「キー(key)」という列の定義
  - ある特定の列の値を決定するための列
  - 基礎概念である※3-1節で解説

### 正規化
- エンティティについて、システムでの利用がスムーズに行えるよう整理する作業のこと
- フォーマットを整理することが重要な目的
- 属性を定義しただけでは、利用にたえる状態ではない
- リレーショナルデータベースの論理設計において、正規化が最も重要な土台をなす
- 論理設計を理解する鍵といっても過言ではない

### ER図の作成
- 正規化を行うとエンティティの数が増える。
  - 細かく分割していく作業だから
  - このままだとエンティティ動詞の関係が把握できず、問題が発生して効率が落ちる
- 上記の問題解決にER図（エンティティの見取り図）が必要となる