# The Court

一個私人議事廳，負責諮詢、質詢，並協助領主將構想付諸實行。

## 概覽

The Court 是一套個人決策系統。每當領主提出一個構想，家臣團便從不同角度審視——挖掘潛力、提出疑慮、壓力測試各種假設——最終由領主裁決。

廷議在裁決後結束。裁決之後的事，屬於領主的領域。

## 家臣組成

| 成員 | 職位 | 立場 |
|------|------|------|
| **The Scribe** | 書記官 | 中立——整理提案、召集廷議、記錄討論、彙整摘要 |
| **The Advocate** | 家臣 | 支持——挖掘提案的潛力與價值 |
| **The Skeptic** | 家臣 | 質疑——挑戰假設、指出風險與盲點 |
| **The Strategist** | 家臣 | 務實——評估可行性、提出替代路徑 |

各成員完整人設詳見 [.agents/](.agents/)。

## 流程

```
領主提出構想
      ↓
The Scribe 整理結構化提案
      ↓
領主確認提案內容
      ↓
The Scribe 召集廷議
      ↓
Opening Round — 各家臣分別陳述初步立場
      ↓
Open Discussion — 領主可追問、反駁或補充
      ↓
領主宣告廷議結束
      ↓
The Scribe 彙整摘要
      ↓
領主裁決
```

## 廷議邊界

- **啟動**：領主確認結構化提案後，由 The Scribe 召集廷議
- **Opening Round**：每位家臣各給一次初步陳述，結束後進入自由討論
- **Open Discussion**：領主可隨時追問、反駁或轉換方向；家臣自由回應
- **結束**：領主宣告結束；The Scribe 彙整摘要；領主裁決
- **暫緩**：若領主尚未準備好裁決，可將提案設為 Deferred，日後重新召集

## 提案狀態

| 狀態 | 說明 |
|------|------|
| **Active** | 廷議進行中 |
| **Approved** | 領主認定此提案有執行價值 |
| **Deferred** | 暫緩，日後可重新審議 |
| **Rejected** | 駁回；提案移入 Archives |

## 目錄結構

```
The-Court/
├── .agents/                      # 家臣人設定義（AI 自動判讀）
│   ├── the-scribe.md
│   ├── the-advocate.md
│   ├── the-skeptic.md
│   └── the-strategist.md
├── Petitions/
│   ├── Dashboard.md              # 所有提案的狀態總覽
│   ├── template-petition/        # 新提案範本
│   └── P-001-[短標題]/           # 每個提案一個資料夾
│       ├── dossier.md            # 提案內容與最終裁決
│       ├── deliberations.md      # 廷議討論記錄
│       └── Research/             # 相關研究與資料
└── Archives/                     # 已駁回的提案（從 Petitions/ 移入）
```
