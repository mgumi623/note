---
tags: [医療, DX, 内製化, AI, クラウド, コスト]
created: 2026-02-23
related: []
---

# 病院ソフトウェア内製化とAIプラットフォームコスト Web調査資料

## 1. 先進的な内製化事例

### NTT東日本関東病院（東京都品川区）

- Microsoft 365 E5 を活用した現場主導の「市民開発」を推進
- 院内SEがPower AppsやPower Automateを使い、業務アプリをノーコードで内製
- 議事録や院内閲覧物の電子回覧、会議資料の自動作成などを実現
- 厳しいセキュリティ要件をMicrosoft 365 E5で解決しながら内製化を実現
- 出典: [NTT東日本関東病院 Microsoft Customer Stories](https://www.microsoft.com/ja-jp/customers/story/1672898070162413662-nmct-ntt-east-health-provider-microsoft-ja-japan) / [医療テックニュース](https://medicaltech-news.com/special-feature/751/)

### HITO病院（愛媛県四国中央市、病床228床）

2024年8月にMicrosoft記者説明会で発表された生成AI活用の5事例：

1. **診療報酬請求の自動化**: Azure OpenAI Service + 電子カルテ連携で「症状詳記」を自動生成。医師の文書作成負担を大幅削減
2. **経営ダッシュボード**: Microsoft Fabric + Power BIで病院・チームの業務負担をリアルタイム可視化。看護師の適正配置予測に活用
3. **多言語対応**: 海外介護人材向け自動翻訳機能。海外看護補助者単独での夜勤対応が可能に
4. **糖尿病教育支援**: SharePointに格納した病院独自レシピ・情報をAIが抽出し、個別化した食事・リハビリ指導を生成
5. **職員向けCopilot**: 看護師・リハビリスタッフ全員のスマートフォンにCopilot導入

- 出典: [Microsoft News Center Japan](https://news.microsoft.com/ja-jp/2024/08/16/240816-hito-case-study-of-generative-ai-application-in-hito-hospitals-and-microsofts-latest-initiatives-in-the-healthcare-field/) / [ITmedia AIプラス](https://www.itmedia.co.jp/aiplus/articles/2407/26/news136.html) / [AI総合研究所](https://www.ai-souken.com/case/427)

### 済生会熊本病院（病床400床、急性期病院）

- 2021〜2024年の中期事業計画でMicrosoft Power Appsによる市民開発プロジェクトを展開
- 購買案件管理システムをPower Appsで内製化（申請〜納品ログ、電子承認、発注書類の自動化）
- 老朽化した既存システムの段階的な内製刷新を並行推進
- 出典: [Microsoft Customer Stories](https://www.microsoft.com/ja-jp/customers/story/1611631180787811819-saiseikai-kumamoto-health-provider-microsoft-365-ja-japan) / [済生会熊本病院お知らせ](https://sk-kumamoto.jp/info/22164/)

### さきがけホスピタル（岡山県高梁市、精神科・200床以下）

- 2017年に当時の院長がClaris FileMakerによる内製を開始
- 2022年に「情報管理・心理室」を新設し組織的内製体制を確立
- 独自業務システム「Sakigakeシステム」を院長主導で開発
- 売店・在庫管理システム（バーコードリーダー + iPad）を内製。手作業を自動化
- 200床以下の精神科病院では紙カルテが主流だが、FileMakerが中小規模病院の内製起点として有効
- 出典: [Claris blog 2024](https://www.claris.com/ja/blog/2024/sakigake-hispital)

### 東北大学病院 × NEC（医療LLM共同開発）

- 2024年4月施行の「医師の時間外労働上限規制」対応を目的に産学医連携で開発
- 院内電子カルテテキスト約10万件を学習データとして活用
- 文書作成の効率化に特化した医療分野LLMを開発

---

## 2. AIプラットフォーム構築のAPI料金（2025年時点）

### Amazon Bedrock（Claude系モデル）

| モデル | 入力トークン単価 | 出力トークン単価 |
|--------|-----------------|-----------------|
| Claude 3 Haiku | $0.25 / 100万トークン | $1.25 / 100万トークン |
| Claude 3.5 Sonnet | $3.00 / 100万トークン | $15.00 / 100万トークン |
| Claude Sonnet 4.5（最新） | $3.00 / 100万トークン | $15.00 / 100万トークン |

**日本語換算の目安**（1USD = 150円）：
- 日本語は1〜2文字で約1トークン
- 1,000文字の日本語テキスト = 約500〜700トークン
- Claude 3 Haiku で1,000文字の処理 = 約0.02〜0.03円（入力）
- Claude Sonnet で1,000文字の処理 = 約0.2〜0.3円（入力）

**日本リージョン（クロスリージョン推論）**: グローバル比で+10%プレミアム

- 出典: [Amazon Bedrock Pricing](https://aws.amazon.com/jp/bedrock/pricing/) / [Claude API Pricing](https://platform.claude.com/docs/ja/about-claude/pricing) / [cloudpack Bedrock料金ガイド](https://cloudpack.jp/column/generative-ai/amazon-bedrock-pricing-guide-cost-optimization.html)

### Azure OpenAI Service（GPT-4系モデル）

| モデル | 入力トークン単価 | 出力トークン単価 |
|--------|-----------------|-----------------|
| GPT-4o | $2.50 / 100万トークン | $10.00 / 100万トークン |
| GPT-4o mini | $0.15 / 100万トークン | $0.60 / 100万トークン |
| GPT-4（旧来） | $30.00 / 100万トークン | $60.00 / 100万トークン |

- HIPAA・GDPRに対応済み（医療・金融業界での利用可能）
- 日本東日本リージョン利用時は円建て請求対応
- 出典: [Azure OpenAI Service 価格](https://azure.microsoft.com/ja-jp/pricing/details/azure-openai/) / [AI総合研究所 Azure OpenAI料金解説](https://www.ai-souken.com/article/azure-openai-service-pricing)

---

## 3. クラウドインフラ費用（AWS / Azure 月額）

### AWS（医療向けシステム構築）

| 構成規模 | 月額目安 |
|---------|---------|
| 小規模（社内ワークフロー・業務アプリ） | 5万〜15万円 |
| 中規模（外来〜入院管理、API連携あり） | 10万〜30万円 |
| 大規模（電子カルテ・DWH・AI連携） | 30万〜100万円以上 |

- AWSは厚労省・経産省・総務省のガイドライン準拠の「医療情報システム向けAWS利用リファレンス」を提供
- 2024年診療報酬改定で「診療録管理体制加算」のオフライン保管要件にクラウドが適合と認定
- 出典: [AWS 医療機関向けクラウド資料](https://pages.awscloud.com/rs/112-TZM-766/images/AWS_Summit_2025_I-36A_%E5%8C%BB%E7%99%82%E6%A9%9F%E9%96%A2%E5%90%91%E3%81%91%E3%81%93%E3%82%8C%E3%81%8B%E3%82%89%E5%AD%A6%E3%81%B5%E3%82%99AWS%E3%82%AF%E3%83%A9%E3%82%A6%E3%83%88%E3%82%99.pdf)

---

## 4. ローコード・ノーコードプラットフォームの活用

### Microsoft Power Platform（Power Apps / Power Automate）

- **費用**: Microsoft 365 E3（1ユーザー約2,400円/月）またはE5（約4,700円/月）に含まれる基本機能
- Power Apps スタンドアロン: 約2,200円/ユーザー/月（Pay-as-you-go）
- **開発期間**: ローコードにより通常の3〜6倍のスピードで開発（NTT東日本事例では3ヶ月でリリース）
- **病院での採用理由**: 既存Microsoft 365環境との親和性・電子カルテとのSharePoint連携
- 出典: [Microsoft Power Apps製品ページ](https://www.microsoft.com/ja-jp/power-platform/products/power-apps)

### Claris FileMaker

- **費用**: FileMaker Cloud（クラウド版）= 約6,000〜10,000円/ユーザー/月
- セルフホスト版は初期費用方式（1ユーザーライセンスで数万円〜）
- **向き不向き**: 中小規模病院（200床以下）での独自業務アプリ開発に適合。大規模病院では限界あり
- 出典: [Claris FileMaker価格](https://www.claris.com/pricing/self-hosted.html)

---

## 5. 院内エンジニア・医療情報技師の採用状況

### 年収相場（2025年時点）

| 職種 | 平均年収 | レンジ |
|------|---------|--------|
| 院内SE（一般） | 510〜542万円 | 335万〜852万円 |
| 医療情報技師 | 500〜550万円 | 400万〜700万円 |
| 医療IT上位職（DX推進リーダーなど） | 600〜800万円 | 〜1,000万円超 |

- 大手病院グループ（徳洲会グループなど）はSE専用リクルートサイトを開設
- 2025〜2026年にかけ、日本全体でIT人材不足が約22万人規模に拡大する見込み
- 医療機関のIT職はITベンダー・事業会社より給与が低い傾向があり、採用競争力が課題
- 出典: [院内SE年収解説 Geekly](https://www.geekly.co.jp/column/cat-position/in-hospital-se/) / [levtech院内SE解説](https://career.levtech.jp/guide/knowhow/article/181058/) / [Japan Dev 2026](https://yotru.com/blog/hiring-trends-in-japan)

### 主な求められるスキル・資格

- 医療情報技師（HCIT）資格
- 基本情報技術者・応用情報技術者
- クラウド資格（AWS SAA、Azure Administrator）
- 電子カルテ・HIS周辺の運用知識

---

## 6. 内製化 vs 外部委託のコスト比較

### 外部委託（SIer・ベンダー）の開発費用相場

| 規模・内容 | 費用相場 |
|-----------|---------|
| 最小限機能のみ（小規模アプリ） | 50〜150万円 |
| 基本的な機能実装 | 150〜400万円 |
| 複雑・多機能システム | 400万円〜数千万円 |
| 電子カルテ（オンプレミス型） | 300〜500万円（初期） |
| 電子カルテ（クラウド型） | 100〜200万円（初期）+ 月額費用 |
| 大規模医療情報システム（HIS全体） | 数千万〜数億円 |

- AIコンサルタント日当: 15〜20万円（外部委託時）
- AIエンジニア人月単価（外部）: 80〜250万円/人月
- 出典: [発注ラウンジ 医療システム費用](https://hnavi.co.jp/knowledge/blog/medical-system-cost/) / [アイミツ 電子カルテ費用](https://imitsu.jp/cost/web-system/electronic-medical-record-introduction-cost) / [AI Front Trend 生成AI開発費用](https://ai-front-trend.jp/ai-development-cost/)

### 内製化の人件費概算

| 役割 | 月額人件費（社員） | 備考 |
|------|------------------|------|
| 院内SE（中級） | 40〜55万円/月 | 年収500〜660万円換算 |
| DX推進エンジニア（上級） | 55〜75万円/月 | 年収660〜900万円換算 |
| AIエンジニア（内製化対応） | 60〜80万円/月 | 市場競争が激しく採用困難 |

---

## 7. 段階的AI機能追加（アジャイル開発）の費用感

### スプリント単位の費用構造

- **1スプリント（2週間）の外注費用**: エンジニア1〜2名で約160〜500万円
- **内製チームでの1スプリント費用**: 人件費のみで約20〜40万円（1〜2名）
- **POC（概念実証）フェーズ**: 外注なら100〜300万円、内製なら30〜80万円

### 段階別の想定コスト（医療AIアプリ・外注の場合）

| フェーズ | 期間 | 費用目安 |
|---------|------|---------|
| コンサルティング・要件定義 | 1〜3ヶ月 | 40〜200万円 |
| POC（プロトタイプ作成） | 1〜3ヶ月 | 100〜500万円 |
| MVP（最小限機能）開発 | 3〜6ヶ月 | 300〜1,000万円 |
| 機能追加・改善（継続） | 月次 | 80〜300万円/月 |

### 東京都の補助金（2025年度）

- 医療機関におけるAI技術活用促進事業
- 基準額: 1,000万円（コンサルティング実施時は2,000万円）
- 補助率: 1/2（最大500万〜1,000万円の補助）
- 対象: AI問診、電子カルテへのAI音声入力、多言語対応システムなど
- 出典: [東京都保健医療局](https://www.hokeniryo.metro.tokyo.lg.jp/iryo/jigyo/ai)

---

## 参考URL一覧

- [さきがけホスピタル 内製開発事例 (Claris)](https://www.claris.com/ja/blog/2024/sakigake-hispital)
- [NTT東日本関東病院 医療DX事例 (Microsoft)](https://www.microsoft.com/ja-jp/customers/story/1672898070162413662-nmct-ntt-east-health-provider-microsoft-ja-japan)
- [済生会熊本病院 Power Apps市民開発 (Microsoft)](https://www.microsoft.com/ja-jp/customers/story/1611631180787811819-saiseikai-kumamoto-health-provider-microsoft-365-ja-japan)
- [HITO病院 生成AI活用事例 (Microsoft News)](https://news.microsoft.com/ja-jp/2024/08/16/240816-hito-case-study-of-generative-ai-application-in-hito-hospitals-and-microsofts-latest-initiatives-in-the-healthcare-field/)
- [Amazon Bedrock 料金](https://aws.amazon.com/jp/bedrock/pricing/)
- [Azure OpenAI Service 価格](https://azure.microsoft.com/ja-jp/pricing/details/azure-openai/)
- [院内SE 年収・仕事内容 (Geekly)](https://www.geekly.co.jp/column/cat-position/in-hospital-se/)
- [医療システム開発費用相場 (発注ラウンジ)](https://hnavi.co.jp/knowledge/blog/medical-system-cost/)
- [東京都 医療AI補助金](https://www.hokeniryo.metro.tokyo.lg.jp/iryo/jigyo/ai)
- [AI開発費用ガイド 2025 (AI Front Trend)](https://ai-front-trend.jp/ai-development-cost/)
