---
tags: [医療DX, AI導入, 国際比較, 病院経営, 診療報酬]
created: 2026-02-23
---

# 海外と日本の病院AI導入比較 Web調査資料

## 1. 米国の病院AI導入率と主要事例

### 全体的な導入状況（2024-2025年）

米国の病院AI導入は、規模・地域・系列によって大きく差がある。

- 大規模病院（400床以上）：AI使用率 90〜96%
- 小規模病院（100床未満）：53〜59%
- 多病院グループ系列院：81〜86%
- 完全独立型病院：31〜37%
- 都市部病院：77〜81%
- 農村部病院：48〜56%

分野別の導入率（2024年秋 Scottsdale Institute 調査、67ヘルスシステムが対象）：
- 画像診断・放射線AI：90% が少なくとも限定的に導入
- アンビエント記録（AI音声による診療記録自動作成）：60% が導入、100% が開発または試験段階
- 早期敗血症検知：67%
- 臨床悪化リスク予測：56%
- 予期しない再入院リスク予測：52%
- インバスケット自動化（メッセージ整理等）：51%

出典：[AI in Hospitals: 2025 Adoption Trends & Statistics | IntuitionLabs](https://intuitionlabs.ai/articles/ai-adoption-us-hospitals-2025)、[PMC - Adoption of artificial intelligence in healthcare survey 2025](https://pmc.ncbi.nlm.nih.gov/articles/PMC12202002/)

### Epic × Microsoft の連携事例（2024-2025年）

EpicはAmerica最大のEHR（電子カルテ）ベンダーで、約4億人の患者データを管理している。2023年にMicrosoftとの生成AIパートナーシップを正式発表し、2024〜2025年にかけて急速に機能展開している。

**Dragon Copilot（アンビエント診療記録）**
- Nuance Dragon Ambient AIをEpicに直接統合
- 医師が患者と会話しながらAIが自動で高品質な診療記録ドラフトを生成
- ドキュメント作成時間を最大50%削減、燃え尽き症候群感覚を70%減少という報告
- Advocate Health、Baptist Health、Duke Healthなど170〜180組織が導入

**Art（臨床アシスタントAI）**
- カルテを要約し、関連する臨床インサイトをリアルタイムで医師に提示
- Azure OpenAIモデルとEpicの Cosmos データベース（160億件以上の臨床データ）を活用

**Emmie（患者向けAIアシスタント）**
- MyChartアプリ上で患者が検査結果の説明を受けたり、受診予約ができる
- 日本語で言えば「患者のためのAIコンシェルジュ」

**Penny（収益サイクル管理AIエージェント）**
- 医療機関の請求・保険処理を自動化するAIエージェント

2025年8月のEpic UGM25では「AIエージェント」と「新しい基盤モデル」を発表。Epic内だけで160以上のAIプロジェクトが進行中。

出典：[Microsoft for Healthcare - Epic AI Solutions](https://www.microsoft.com/en-us/health-solutions/ehr-partnerships/epic)、[Epic EHR AI Trends For 2025 | SPSoft](https://spsoft.com/tech-insights/epic-ehr-ai-trends-in-2025-reshaping-care/)、[Epic taps Microsoft to accelerate generative AI-powered tools | Fierce Healthcare](https://www.fiercehealthcare.com/ai-and-machine-learning/epic-expands-ai-partnership-microsoft-rolls-out-copilot-tools-help)

---

## 2. シンガポール・韓国のアジア先進事例

### シンガポール：国家統合型ヘルスITの実現

シンガポールは人口約600万人の小国という利点を活かし、国家主導で医療ITインフラを統合している。

**NEHR（国家電子健康記録システム）**
- 2011年から公的医療機関がデータ提供を開始
- 「One Patient, One Health Record（1人の患者に1つの健康記録）」を国家ビジョンとして掲げる
- 2024年7月時点でNGEMR（次世代電子カルテ）が37医療機関に導入完了
- 保健省（MOH）が所有し、Synapxe（国家ヘルステック機関）が管理
- 民間病院も接続義務化に向け段階的に移行中

**BRAINプラットフォーム**
- NHS全体で共有されるビジネスインテリジェンス・分析・AI処理の中央プラットフォーム
- NEHRデータを活用した予測モデルの入力データソース

**具体的なAI事例：PEACHチャットボット（シンガポール総合病院）**
- 術前評価クリニック向けのAIチャットボット
- 麻酔関連の質問対応、紹介状の下書き、患者への指示書作成、ケアプラン生成が可能
- 年間600時間以上の研修医業務時間を削減

**Project ENTenna（Ng Teng Fong総合病院）**
- 保健省ヘルスイノベーションファンド支援プロジェクト
- アジア初の人口ベースアレルギーデータベース（アレルギー性鼻炎）を構築
- 専門外来から一般診療への適切な紹介率が45%向上

出典：[AI in Healthcare in Singapore | Kaopiz](https://kaopiz.com/en/articles/ai-in-healthcare-in-singapore/)、[SingHealth and Philips MOU | PR Newswire](https://www.prnewswire.com/apac/news-releases/singhealth-and-philips-sign-mou-to-advance-digital-first-healthcare-to-future-proof-care-delivery-302379667.html)、[NEHR - Synapxe](https://www.synapxe.sg/healthtech/national-programmes/national-electronic-health-record-nehr)

### 韓国：大学病院主導のAI実装と大手IT企業参入

**Y-KNOTプロジェクト（延世大学セブランス病院）**
- 2024年11月から日常臨床への本格導入開始
- 院内オンプレミス型の2言語対応LLMを電子カルテに統合
- 目的：退院サマリなどの臨床文書作成を自動化
- 結果：救急科での退院サマリ記載完了率が92.7%（2024年4〜5月）→ 98.0%（2025年4〜5月）に向上

出典：[PMC - Y-KNOT Project Bilingual AI Agent for Clinical Drafting](https://pmc.ncbi.nlm.nih.gov/articles/PMC12643392/)

**NaverとKakaoのデジタルヘルス参入**
- Kakao Healthcare：「Pasta」というAIパーソナライズド健康管理サービスを展開。2024年5月に日本法人設立、肥満治療薬管理機能も追加
- Naver Healthcare：症状入力で適切な診療科を推薦し、受診予約が可能な統合ヘルスサービスを一般公開
- 韓国デジタルヘルス市場：2024年に約33億ドルの規模、2030年に110億ドル超に拡大予測（CAGR 19%）

出典：[Beyond the clinic: How Korean IT giants spur digital health evolution | Healthcare IT News](https://www.healthcareitnews.com/news/asia/beyond-clinic-how-korean-it-giants-spur-digital-health-evolution)、[Naver, Kakao to compete in digital healthcare | Korea Times](https://www.koreatimes.co.kr/www/tech/2024/09/129_321620.html)

---

## 3. 日本の電子カルテ・AI導入の現状数値（2024-2025年）

### 電子カルテ普及率（2024年調査）

| 区分 | 普及率 |
|------|--------|
| 400床以上の大規模病院 | 93.7% |
| 病院全体 | 77.7% |
| 200床未満の病院 | 59.0% |
| 一般診療所 | 71.0% |

比較：米国の病院全体のEHR普及率は2014年時点で既に約76%に達していた。

出典：[電子カルテの普及率と今後の動向 | メディコム](https://www.phchd.com/jp/medicom/park/tech/ehr-penetrationrate)

### 医療AI市場規模

日本の医療AI市場は2024年に14.2億ドルに達し、2033年には148億ドルへと急拡大する見込み（CAGR 36.5%）。ただし、これは市場規模であり、実際の現場導入率は依然として低い。

出典：[Japan AI in Healthcare Market 2025-2033 | openPR](https://www.openpr.com/news/4291330/japan-ai-in-healthcare-market-2025-2033-high-36-5-cagr)

---

## 4. 日本の医療DX推進政策の現状

### 電子処方箋の普及状況（2025年）

| 区分 | 導入率 |
|------|--------|
| 薬局 | 86.5% |
| 医科診療所 | 23.3% |
| 病院 | 17.3% |

薬局は急速に普及が進んだが、医療機関（特に病院）は深刻に遅れている。

### マイナ保険証の利用率推移

- 2025年10月時点：47.26%
- 政府目標ステップ：2025年9月まで45%、10月〜2026年2月60%、2026年3月〜70%
- 2024年12月に従来の保険証廃止（マイナ保険証への完全移行）

### 医療DX推進体制整備加算

医療機関がマイナ保険証の利用率基準を満たすと加算点数が得られる仕組み。2025年4月から電子処方箋導入有無でも差別化された点数設定が適用。

出典：[医療DXの進捗状況 | 厚生労働省](https://www.mhlw.go.jp/content/10808000/001511374.pdf)、[GemMed - 医療DX推進体制整備加算](https://gemmed.ghc-j.com/?p=68778)

### 医療DX令和ビジョン2030の目標

- 2030年までに標準型電子カルテを全医療機関に導入
- 全国医療情報プラットフォームの整備（医療機関間でのデータ共有基盤）
- PHR（個人の健康記録）の整備・普及

当初の目標「2025年3月までに概ね全国の医療機関・薬局に普及」は見直しとなり、2026年夏に電子カルテと電子カルテ情報共有サービスの普及計画を再策定する方針に転換。

出典：[Roadmap for the Promotion of Healthcare DX | 厚生労働省](https://www.mhlw.go.jp/english/policy/health-medical/healthcare-dx/dl/Roadmap-for-the-Promotion-of-Healthcare-DX(Digital-Transformation).pdf)

---

## 5. 日本のデジタル化を阻害する構造的要因

### 診療報酬制度の構造的問題

- 医療機関は診療報酬という公定価格でしか収入を得られない（市場価格設定が不可）
- IT投資を行っても診療報酬に反映される仕組みが極めて限定的
- 「設備投資の有無や大小は診療報酬に関係ない」という構造
- 新しいAIツールを導入しても、コスト回収の見通しが立たない
- 新技術の診療報酬収載には相当のエビデンスと時間が必要

出典：[日本の医療のIT化が進まない現状の理由 | LINQUA](https://linqua.jp/news/medical-itization-not-progressing/)、[病院経営とDX | PwC Japan](https://www.pwc.com/jp/ja/knowledge/column/hospital-management/vol03.html)

### ベンダーロックインと標準化不足

- 各医療機関が個別に電子カルテを導入した歴史的経緯から、ベンダーごとに異なる仕様のシステムが乱立
- 異なるベンダー間でのデータ互換性がほぼない
- 電子的な患者紹介状（データ共有）はわずか0.4%に留まる（紙や郵送が主流）
- ベンダー変更・データ移行が極めて困難なため、老朽システムの更新が進まない

出典：[なぜ日本の医療DXは遅れる？ベンダーロックインという壁 | note](https://note.com/realworld/n/n3c7a10020468)

### 経営的制約と病院の財務状況

- 日本の病院の医業利益率は平均1%前後（多くは赤字）
- 2024年度診療報酬改定後も病院経営の悪化が継続
- 中小病院・診療所はIT投資に充てる余剰資金がない
- IT人材の確保が困難（採用・育成のコストが高い）

出典：[GemMed - 病院経営悪化 2024年度診療報酬改定後](https://gemmed.ghc-j.com/?p=71209)

### 組織・文化的要因

- 高齢の医療従事者の間でのデジタルリテラシー格差
- 部署横断の合意形成に時間がかかる
- 「失敗が許されない」文化による新技術導入への慎重さ
- セキュリティ懸念による心理的抵抗

---

## 6. 日本の医療AIの強み：内視鏡画像診断

特筆すべき例外として、日本は内視鏡AIの分野では世界トップクラスの水準にある。

- AI内視鏡診断（大腸ポリープ検出など）の分野では日本発のシステムが世界をリード
- 富士フイルム：2024年10月に肋骨骨折検出AI「FS-AI691」の薬機承認取得
- エルピクセル：「EIRL」シリーズ（肺結節、眼底など）
- NICTと大学連携：プライバシー保護連合学習技術「DeepProtect」を用いた放射線AI研究

出典：[内視鏡画像診断支援AI、日本が世界でリードできる分野に | 日経メディカル](https://medical.nikkeibp.co.jp/leaf/all/series/aileaders/202505/587443.html)

---

## ソース一覧

- [AI in Hospitals: 2025 Adoption Trends & Statistics | IntuitionLabs](https://intuitionlabs.ai/articles/ai-adoption-us-hospitals-2025)
- [PMC - Adoption of artificial intelligence in healthcare survey 2025](https://pmc.ncbi.nlm.nih.gov/articles/PMC12202002/)
- [Microsoft for Healthcare - Epic AI Solutions](https://www.microsoft.com/en-us/health-solutions/ehr-partnerships/epic)
- [Epic EHR AI Trends For 2025 | SPSoft](https://spsoft.com/tech-insights/epic-ehr-ai-trends-in-2025-reshaping-care/)
- [Epic taps Microsoft to accelerate generative AI-powered tools | Fierce Healthcare](https://www.fiercehealthcare.com/ai-and-machine-learning/epic-expands-ai-partnership-microsoft-rolls-out-copilot-tools-help)
- [Epic unveils AI agents | Healthcare IT News](https://www.healthcareitnews.com/news/epic-unveils-ai-agents-showcases-new-foundational-models)
- [AI in Healthcare in Singapore | Kaopiz](https://kaopiz.com/en/articles/ai-in-healthcare-in-singapore/)
- [NEHR - Synapxe](https://www.synapxe.sg/healthtech/national-programmes/national-electronic-health-record-nehr)
- [PMC - Y-KNOT Project Bilingual AI Agent Korea](https://pmc.ncbi.nlm.nih.gov/articles/PMC12643392/)
- [Korea AI Healthcare | Nucamp Blog](https://www.nucamp.co/blog/coding-bootcamp-south-korea-kor-healthcare-how-ai-is-helping-healthcare-companies-in-south-korea-cut-costs-and-improve-efficiency)
- [Beyond the clinic: How Korean IT giants | Healthcare IT News](https://www.healthcareitnews.com/news/asia/beyond-clinic-how-korean-it-giants-spur-digital-health-evolution)
- [Japan AI in Healthcare Market 2025-2033 | openPR](https://www.openpr.com/news/4291330/japan-ai-in-healthcare-market-2025-2033-high-36-5-cagr)
- [電子カルテの普及率と今後の動向 | メディコム](https://www.phchd.com/jp/medicom/park/tech/ehr-penetrationrate)
- [医療DXの進捗状況 | 厚生労働省](https://www.mhlw.go.jp/content/10808000/001511374.pdf)
- [Roadmap for the Promotion of Healthcare DX | 厚生労働省（英語版）](https://www.mhlw.go.jp/english/policy/health-medical/healthcare-dx/dl/Roadmap-for-the-Promotion-of-Healthcare-DX(Digital-Transformation).pdf)
- [GemMed - 医療DX推進体制整備加算](https://gemmed.ghc-j.com/?p=68778)
- [GemMed - 2024年度診療報酬改定後の病院経営悪化](https://gemmed.ghc-j.com/?p=71209)
- [なぜ日本の医療DXは遅れる？ベンダーロックインという壁 | note](https://note.com/realworld/n/n3c7a10020468)
- [日本の医療DXは遅れている？諸外国との比較 | 慢性期.com](https://manseiki.com/news/%E6%97%A5%E6%9C%AC%E3%81%AB%E3%81%8A%E3%81%91%E3%82%8B%E5%8C%BB%E7%99%82dx%E3%81%AF%E9%81%85%E3%82%8C%E3%81%A6%E3%81%84%E3%82%8B%EF%BC%9F%E2%80%95%E2%80%95%E8%AB%B8%E5%A4%96%E5%9B%BD%E3%81%A8%E3%81%AE)
- [Digital Healthcare 2025 - Japan | Chambers and Partners](https://practiceguides.chambers.com/practice-guides/digital-healthcare-2025/japan/trends-and-developments)
- [内視鏡画像診断支援AI、日本が世界でリードできる分野に | 日経メディカル](https://medical.nikkeibp.co.jp/leaf/all/series/aileaders/202505/587443.html)
- [IDC - AI-Powered Healthcare in Asia Pacific 2025](https://www.idc.com/resource-center/blog/ai-powered-healthcare-in-asia-pacific-whats-next-for-2025-and-beyond/)
