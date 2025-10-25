# ITエンジニアと眺める言語学 — Notebooks

このリポジトリは、書籍
**『ITエンジニアと眺める言語学』（岸山健 著、教養検定会議、2025年）**
で紹介されている分析や可視化の一部を、Jupyter Notebook で再現したものです。

* **書名:** ITエンジニアと眺める言語学
* **著者:** 岸山健（キシヤマ タケシ）
* **出版社:** 教養検定会議
* **ISBN:** 978-4-910292-11-3
* **判型・頁数:** 新書判／149頁
* **定価:** 1,650円（税込）
* **初版:** 2025年10月10日

---

## 書籍紹介

本書では、単語や音、言葉の構造に関するトピックを紹介するのですが、
タヌキやホーミー（喉歌）の音響解析、聴力シミュレーション、
カードゲームにおける文構造の解析など、幅広い話題を扱っています。
Python／Colab 環境で誰でも再現できるよう、
このリポジトリに各章のサンプル Notebook を収録しました。

---

## 章別ノートブック対応表

| 章 | 章タイトル | Notebookファイル | 内容概要 |
|--------|-------------|------------------|-----------|
| 02 | タヌキから見る言語表現 | [tanuki.ipynb](https://github.com/kishiyamat/la-kentei-yaminabe/blob/main/notebooks/tanuki.ipynb) | タヌキ・ムジナの法的区別を題材に、画像の数値化とクラスタリングを体験する。 |
| 03 | エンタメ施設も博物館？ | [haripota_museum.ipynb](https://github.com/kishiyamat/la-kentei-yaminabe/blob/main/notebooks/haripota_museum.ipynb) | 口コミデータを用いたTF-IDF・ロジスティック回帰による分類。テーマパークと博物館の境界を探る。 |
| 04 | ホーミーから眺める音声と知覚 | [khoomii_feedback_minimal.ipynb](https://github.com/kishiyamat/la-kentei-yaminabe/blob/main/notebooks/khoomii_feedback_minimal.ipynb) | モンゴルの喉歌「ホーミー」の音響特性を可視化。スペクトログラム解析を通じて声道共鳴を理解する。 |
| 05 | 音脈分凝 | [speech_analysis.ipynb](https://github.com/kishiyamat/la-kentei-yaminabe/blob/main/notebooks/speech_analysis.ipynb) | 音声波形とスペクトログラムを通して、音の多義性と知覚分離を観察する。 |
| 06 | 計算機上の渋谷と日比谷 | [hearing_loss_simulation.ipynb](https://github.com/kishiyamat/la-kentei-yaminabe/blob/main/notebooks/hearing_loss_simulation.ipynb) | 聴力図データを用いて難聴をシミュレート。音の聞こえ方を体験的に理解する。 |
| 07 | 意味を考慮した聞き間違えの再現 | [talking_aid_word_freq.ipynb](https://github.com/kishiyamat/la-kentei-yaminabe/blob/main/notebooks/talking_aid_word_freq.ipynb) / [talking_aid_minimal.ipynb](https://github.com/kishiyamat/la-kentei-yaminabe/blob/main/notebooks/talking_aid_minimal.ipynb) | Word2Vec による単語類似度と音韻距離の統合。聞き間違え予測の原理を実装。 |
| 08 | カードの翻訳に学ぶ、文構造の複雑さ | [mtg.ipynb](https://github.com/kishiyamat/la-kentei-yaminabe/blob/main/notebooks/mtg.ipynb) / [mtg-original.ipynb](https://github.com/kishiyamat/la-kentei-yaminabe/blob/main/notebooks/mtg-original.ipynb) | Magic: The Gatheringのテキストを題材に、センター埋め込み構文と翻訳の難しさを可視化。 |
| 09 | 言葉が生む複数の解釈 | [time_flies.ipynb](https://github.com/kishiyamat/la-kentei-yaminabe/blob/main/notebooks/time_flies.ipynb) / [time_flies-original.ipynb](https://github.com/kishiyamat/la-kentei-yaminabe/blob/main/notebooks/time_flies-original.ipynb) | “Time flies like an arrow.” の構文解析。構造的多義性と意味の曖昧さをPythonで検証。 |
| 10 | AIは頼もしい相棒？ | [別リポジトリ: chatgpt-like-clone-clone](https://github.com/kishiyamat/chatgpt-like-clone-clone) | 生成AIや言語モデルを用いた文章生成・データ整理のハンズオン例。 |

---

## 環境設定

### Google Colaboratory

https://github.com/kishiyamat/la-kentei-yaminabe/tree/main/notebooks
にある各ノートブックを開き、「Google Colabで開く」ボタンをクリックしてください。
Google Colaboratory で実行可能です。

### Local 

Python 3.10 以上を推奨しています。

```bash
git clone https://github.com/kishiyamat/la-kentei-yaminabe.git
cd la-kentei-yaminabe/notebooks
```

---

## 正誤表

| ページ          | 箇所      | 誤                              | 正                    | 備考                         |
| ------------ | ------- | ------------------------------ | -------------------- | -------------------------- |
| p.5 下から6行目   | 文中      | 観察できます                         | 観察できる                | 文体の統一（常体）に合わせた修正。          |
| p.11 第二段落3行目 | 文中      | 図3上の                           | 図2上の                 | 図番号の誤記。図2を参照する内容。          |
| p.23 第二段落    | 括弧内     | （傾きと読んでいた）                     | （傾きと呼んでいた）           | 用語の誤記訂正。                   |
| p.25 5行目     | 文頭      | さて、                            | さて（段落始まりのスペースが落ちている） | レイアウト上の不備。                 |
| p.26 下から1行目     | 文中      | そういういう                            | そういう（「いう」が重複） | 誤記。                 |
| p.36         | 図キャプション | 「ウポポイという…」（図2のキャプションが本文になっている） | キャプション位置修正予定         | レイアウト調整時の混入。               |
| p.129        | 文中      | 頭語構造                           | 統語構造                 | 用語の誤記。syntax structureの訳語。 |

---

## 補足・解説

| ページ   | 該当箇所                                  | 補足内容                                                                                      |
| ----- | ------------------------------------- | ----------------------------------------------------------------------------------------- |
| p.42  | 「同じ高さの声を出す、というのはいうほど簡単ではないことに気づきました。」 | 同一の音高（ピッチ）を維持する発声は、息の圧・声帯の緊張・共鳴腔の角度などが微妙に影響し、実際には難しい作業である。声の高さを「同じ」と感じるには、聴覚上の相対的な安定も関わる。 |
| p.120 | 「写真の色の」とあるが、掲載写真は白黒                   | “orange cat”（オレンジの猫）を検索すると、日本語話者の感覚では「茶色の猫」が多く出てくる。この差異は色カテゴリの文化差に関する好例。脚注や注釈で補足するのが適当。   |

---

## 備考・更新予定

* 今後の増刷では上記の誤植を修正予定（おそらく電子書籍になるとのことです）。
* 参照図の番号・キャプション位置・文体統一（常体への統一）を中心に整備する。

---

## 著者コメント（2025年10月追記）

初版の執筆・編集にあたっては、データ処理や図版生成をすべてPython／Colab上で行いました。
文中で使用している図番号・キャプションは自動生成に基づいており、編集時に差し替え漏れが生じた箇所があります。
正誤表を参照のうえ、必要に応じてリポジトリ内のノートブックを確認していただければ幸いです。

- 2025/10/22: [ブログ](https://www.kishiyamat.work/2025/10/22/yaminabe-book.html)を更新しました。
- 2025/10/25: 本ページ（README.md）を作成しました。

---

## 収録ノートブック一覧

| ファイル名                            | 概要            |
| -------------------------------- | ------------- |
| `haripota_data_prep.ipynb`       | データ収集と前処理。    |
| `haripota_museum.ipynb`          | 博物館・テーマパーク分類。 |
| `hearing_loss_simulation.ipynb`  | 難聴シミュレーション。   |
| `khoomii_feedback_minimal.ipynb` | ホーミーの音声解析。    |
| `mtg-original.ipynb`             | カードテキストの分析（もとのバージョン）。 |
| `mtg.ipynb`                      | カード文構造解析。     |
| `speech_analysis.ipynb`          | 音声波形解析。       |
| `talking_aid_minimal.ipynb`      | 音声補助アプリの試作。   |
| `talking_aid_word_freq.ipynb`    | 単語頻度と類似度分析。   |
| `tanuki.ipynb`                   | 動物名とクラスタリング。  |
| `time_flies-original.ipynb`      | 英文構文の解析（もとのバージョン）。  |
| `time_flies.ipynb`               | 意味構造の多義性解析。   |

---

## 著者について

**岸山健（Kishiyama Takeshi）**
東京都生まれ。東京大学大学院総合文化研究科博士（学術）。
音声知覚・心理言語学・自然言語処理を専門とし、
AI・機械学習を活用した研究開発にも従事。

代表著書：

* 『ITエンジニアと眺める言語学』（教養検定会議, 2025）
* 『jsPsychによるオンライン音声実験レシピ』（共著, 教養検定会議, 2024）

---

## License

This repository is distributed under the MIT License.
Educational and research reuse is encouraged with citation of the book.

```
Kishiyama, T. (2025). ITエンジニアと眺める言語学. 教養検定会議.
```
