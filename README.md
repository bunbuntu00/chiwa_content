# CHIWA Content — Content OS

> AI 驅動的多平台內容工廠（Content Factory）

---

## 0. Snapshot（本 repo 的一眼重點）

- **Keyword Map skeleton**：**65 / 65 ✅ 完成**
- **Content Arsenal nodes**：**65 / 65**（每個 keyword 一個節點）
- **Platform Variants**：**6 平台 × 65 rows = 390 handles**（Shopee PDP / IG / Threads / Blog / Reels Script / TikTok）
- **總檔案數**：**520**（65 keyword × 8 類別）
- **現在位置**：Phase 9（同步完成）→ 進入 **Cleanup / Enrichment / 重寫**

---

## 1. Repository 結構與命名規則

```
keyword_map/                  # 每個關鍵字 1 檔，frontmatter = 語意欄位
content_arsenal/
  └─ nodes/                   # 內容節點（各平台共用的中心）
platform_variants/            # 平台變體（六個目錄）
  ├─ shopee_pdp/              # 商詳/問答/權威型
  ├─ ig/                      # 共鳴/敘事/社群互動
  ├─ threads/                 # 討論/反應/短評論
  ├─ blog/                    # SEO 長文
  ├─ reels_script/            # 直入 hook 的腳本
  └─ tiktok/                  # 高節奏短影音腳本
```

**Slug 規則**：`km-<row_index>-294ff9`（固定長度、可追蹤）

---

## 2. 目前進度（Progress）

- ✅ Phase 0 — Repo initialized
- ✅ Phase 1 — Content pillars scaffolded
- ✅ Phase 2 — Templates added (content + keyword)
- ✅ Phase 3 — Keyword Map skeleton
- ✅ Phase 4 — Content Arsenal scaffold
- ✅ Phase 5 — Visual Library scaffold
- ✅ Phase 6 — Mamá Chiwa voice library
- ✅ Phase 8 — Demo content seeds
- ✅ Phase 9 — Keyword Map → GitHub **65 / 65** 初始化完成

---

## 3. Cleanup Rules（這一輪要做什麼）

> 目標：將 `keyword_map/*.md` 與 `content_arsenal/nodes/*.md` 的 frontmatter 從 TODO → 真實值。

**必填欄位**
- `content_intent`: ["Search (SEO)", "Blog", "PDP (Shopee)", "Social (IG/Threads/Facebook)"]
- `emotion_tags`: 例如 ["濕", "熱", "焦慮", "擔心生病", "臭"]
- `journey_stage`: `SEE / THINK / DO`（與你在 Notion 的 Stage 對齊）
- `value_props`: 例如 ["不悶熱", "乾爽", "涼感", "透氣", "可機洗", "抗臭", "抗菌", "快乾", "敏感肌膚友善", "溫度管理"]
- `template_type`: `Problem / Feature / Context / Education / Brand / Comparison`
- `platforms`: 需要開啟之平台陣列（6 選多）
- `notes`, `progress`, `updated_at`

**標準化規則**
- Emotion 值以 Notion 原值為主，允許多選；不同用詞以等義詞表校正（例如："濕氣重" → "濕"）。
- Stage 僅允許 `SEE/THINK/DO`，若 CSV/Notion 出現中文對應，做映射。
- Value Props 僅允許上面列出的 10 個白名單詞彙。
- Template Type 收斂到 6 類。
- Platforms 僅 6 類：`shopee_pdp, ig, threads, blog, reels_script, tiktok`。
- Progress 欄位將由 `未開始/進行中/已清理` 三態組成。

---

## 4. Emotion × Journey Matrix（設計原則）

| Journey \ Emotion | 濕 | 熱 | 臭 | 焦慮 | 擔心生病 |
|---|---:|---:|---:|---:|---:|
| SEE  | 感知問題、共鳴、環境類比 | 季節/環境對照 | 嗅覺畫面、生活情境 | 同理家長情緒 | 健康安全提醒 |
| THINK| 解法探索、原理解釋 | 材質/溫控科普 | 抑菌/快乾機制 | 選擇比較指南 | 小兒科/衛教引用 |
| DO   | 清單、規格、QA | 尺寸/使用情境 | 清潔維護 | 退換/保固 | 合規/敏感肌證明 |

---

## 5. Platform Variant 指南（寫法風格）

- **Shopee PDP**：清單化、規格、QA、信任訊號、退換與保固
- **IG**：故事切入、媽媽視角、共鳴留言引導
- **Threads**：一語破題、丟議題釣回饋
- **Blog**：SEO 結構（H2/H3、內部連結、FAQ schema）
- **Reels Script**：3 秒 hook、5 段節奏、CTA 場景化
- **TikTok**： punchy 句型、節奏更快、字幕易拍

---

## 6. 貢獻流程（Workflow）

1. **Keyword → Node**：以 `keyword_map/*` 為準，先清理 frontmatter。
2. **Node → Variants**：自動生成平台變體骨架與指令。
3. **PR Review**（如需要）：語意與風格校對。
4. **Merge → Deploy**：未來可串 CI 產出 Preview/Export。

---

## 7. Roadmap（下一步）

- 🔧 **Cleanup Pass**：從 Notion/CSV 回填語意欄位（標準化）
- ✨ **Enrichment Pass**：加入情緒鋪陳、反直覺角度、統計佐證
- 🧰 **Platform Rewrite**：依平台風格自動重寫
- 🔗 **Internal Linking**：跨主題關聯、系列化
- 🖼️ **Visual Library**：自動圖像指令槽位（鏡頭、色調、材質、場景）
- 🤖 **CI/CD**：Push → Preview → Auto export / posting

---

## 8. Changelog

- 2025-10-27 重新編排 README，升級為 **產品級 Extended 版本**（包含規範、矩陣與 Roadmap）。

---

## 9. Boot Prompt

> See `docs/BOOT_PROMPT.md` for the boot prompt.
