# Issue対応表 — うのっち承認済みP0

承認済みソース: [概要](01_OVERVIEW.md)、[要件](02_REQUIREMENTS.md)、[詳細設計](03_DETAILED_DESIGN.md)。公開Issue本文は文書の同期前から単独で読めるよう自己完結させた。Issue作成と設計文書の公開は実装開始の許可ではない。

| 順序 | Issue | 文書からの対応 | 前提 |
| --- | --- | --- | --- |
| 01 | [#1 正本化・パッケージ凍結](https://github.com/sanpeita/lowpoly-character-maker/issues/1) | 概要: 作業順、詳細: 境界／ゲート | うのっちの別途公開・実装許可 |
| 02 | [#2 パーツ・パレット／シーン](https://github.com/sanpeita/lowpoly-character-maker/issues/2) | 要件 R2・R5、詳細: Parts | #1 |
| 03 | [#3 決定的Generator](https://github.com/sanpeita/lowpoly-character-maker/issues/3) | 要件 R1・R3、詳細: CharacterRecipe | #2 |
| 04 | [#4 三角形／色数Validator](https://github.com/sanpeita/lowpoly-character-maker/issues/4) | 要件 R4・R5・R7、詳細: Validator | #2・#3 |
| 05 | [#5 PC単一画面UI／プレビュー](https://github.com/sanpeita/lowpoly-character-maker/issues/5) | 要件 R1・R8、詳細: UI/State | #3・#4 |
| 06 | [#6 静止GLB出力／往復検証](https://github.com/sanpeita/lowpoly-character-maker/issues/6) | 要件 R6・R7、詳細: Exporter | #1・#3・#4 |
| 07 | [#7 E2E受入／権利・運用](https://github.com/sanpeita/lowpoly-character-maker/issues/7) | 要件: 完了条件、詳細: Build/Test | #5・#6 |
| Later | [#8 リグ／アニメーション次期設計](https://github.com/sanpeita/lowpoly-character-maker/issues/8) | 概要・要件: 将来アップデート | P0受入後、改めて承認 |

## 必須ゲート

- 初版はPC向け・ブラウザ単一画面。スマートフォンは対象外。リグ／アニメーションは将来の別設計。
- 完成キャラ全体の**三角形256枚以下・不透明ベースRGB8色以下**を機械検証し、静止GLBを独立ローダーで再読込して確認。
- 実装チームの書込み権限、独立レビュー／Terraゲート、技術選定は #1 で凍結する。未確定のモデル名だけで委任しない。
- 今後のコード変更のcommit、push、公開変更はうのっちの明示許可を別途要する。
