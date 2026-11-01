# Lecture 02 Answers

## Exercises

- Model and settings used (from `config` in `result.json`): Qwen/Qwen3.5-0.8B、LoRA（量子化なし）、20エポック、40ステップ、学習率2e-4、LoRA rank 16、alpha 32、seed 42。設定は初期値のまま使用した。
- Did you run training yourself (`executed_training_myself`): Yes。Google ColabのT4 GPUで20エポック（40ステップ）の学習を実行した。学習時間は180秒。
- Before training: `format_rate` = 0.9524（20/21） / `content_rate` = 0.3810（8/21）
- After training: `format_rate` = 1.0000（21/21） / `content_rate` = 0.9524（20/21）
- Questions that regressed: なし。
- Failures remaining after training and their types (assertion without evidence / evasion through a confirmation request despite evidence being present / broken format): 1問だけ内容の誤りが残った。オフィスアワーに予約が必要かという質問に対して、FAQに予約の記載がないにもかかわらず、別の情報を流用して `needs_review: false` と回答した。形式の誤りはなかった。
- Results of knowledge questions (section 6; classification before → after training) and observations:
  - 最終課題の締切：asserted → asserted。通常課題の締切を誤って流用した。
  - 講師名：needs_review → needs_review。確認が必要という判断を維持した。
  - 次回講義の内容：needs_review → needs_review。確認が必要という判断を維持した。
  - 通常課題の締切：asserted → asserted。FAQに根拠があるため適切な回答だった。
- What changed and what stayed the same with training: JSON形式遵守率は95.2%から100%、内容正確率は38.1%から95.2%に改善した。回答もFAQの文章に近づいた。一方、FAQにない情報を断定する問題は残った。

## Homework

- Level attempted: Basic
- Settings or data changed: 設定とデータは変更せず、初期設定を使用した。14件の学習データを使い、LoRAで20エポック（40ステップ）学習した。
- Results (comparison tables or numbers):

  | 評価項目 | 学習前 | 学習後 |
  | --- | --- | --- |
  | JSON形式遵守率 | 95.2%（20/21） | 100%（21/21） |
  | 内容正確率 | 38.1%（8/21） | 95.2%（20/21） |
  | 両方合格 | 38.1%（8/21） | 95.2%（20/21） |
  | 評価時間 | 36.3秒 | 39.7秒 |

- Discussion of when fine-tuning is and is not suitable: ファインチューニングは、回答形式や一定の応答パターンを学習させる用途に適していると考えた。今回のLoRA学習では、少量のデータでも形式遵守率と内容正確率が大きく改善した。一方、FAQに存在しない情報については、学習後も根拠のない断定が残った。そのため、正確性が重要な場面では、信頼できる情報源との照合や、根拠がない場合に確認を求める仕組みが必要だと考える。
