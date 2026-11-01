# Lecture 01 Answers

## Exercises

- Model's answer to the course-specific question (the 3 homework levels; a summary is fine):Geminiは、3つのレベルをFundamentals、Intermediate、Advancedと回答した。
- What you noticed when comparing it with the correct meaning in the glossary:実際の3段階はBasic、Implementation、Advancedだった。Geminiは講座固有の情報を知らず、一般的な構成から推測して回答していた。
- Token counts you displayed (input / output):- Token counts you displayed (input / output): LoRAについて質問した結果、入力6トークン、出力722トークンだった。

## Homework

- Level attempted: Basic
- What you did:- What you did: gemini-3.5-flash-liteを使い、AIE2026講座の宿題の3段階について同じ質問を3回実行し、回答内容と入出力トークン数を比較した。
- Results:
  - 1回目：Basic、Intermediate、Advancedなどと推測して回答。入力18トークン、出力292トークン。
  - 2回目：講座固有の情報を知らないと回答。入力18トークン、出力73トークン。
  - 3回目：講座固有の情報を知らないと回答。入力18トークン、出力74トークン。
  - モデル変更：gemini-3.5-flashでは、Core / Fundamental、Intermediate / Application、Advanced / Stretch Goalと推測して回答。入力18トークン、出力342トークン。
- Observations and questions: 同じモデルに同じ質問を3回したが、1回目は講座の情報を推測して回答し、2回目と3回目は知らないと回答した。出力トークン数も292、73、74と変化した。LLMの回答は一定ではなく、講座固有の情報については資料との照合が必要だとわかった。
