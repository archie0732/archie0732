<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F2027,50:203A43,100:2C5364&height=210&section=header&text=Yu-Chi%20Hsu&fontSize=58&fontColor=E6EDF3&fontAlignY=36&animation=fadeIn&desc=Computer%20Vision%20%C2%B7%20Deep%20Learning%20%C2%B7%20Retrieval-Augmented%20Generation&descSize=17&descAlignY=58&descColor=C9D1D9" width="100%"/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=18&duration=3200&pause=900&color=58A6FF&center=true&vCenter=true&width=640&lines=Undergraduate+Researcher+%40+Providence+University;Computer+Vision+%C3%97+Deep+Learning;Version-Aware+Retrieval+for+Evolving+Guidelines;Open-Source+Contributor" alt="Typing SVG"/>

**許育祁** · Department of Computer Science and Information Engineering, Providence University, Taiwan

[![Portfolio](https://img.shields.io/badge/Portfolio-archie0732.github.io-0A66C2?style=for-the-badge&logo=githubpages&logoColor=white)](https://archie0732.github.io/profile)
[![Email](https://img.shields.io/badge/Email-yuchi.hsu0308%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:yuchi.hsu0308@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-archie0732-181717?style=for-the-badge&logo=github)](https://github.com/archie0732)

![Papers](https://img.shields.io/badge/First--Author_Papers-2-2EA043?style=flat-square)
![AI CUP](https://img.shields.io/badge/AI_CUP_2025-Top_3.7%25-F0883E?style=flat-square)
![PUPC](https://img.shields.io/badge/ICPC_PUPC_2026-Silver-A5B4C3?style=flat-square)
![Rank](https://img.shields.io/badge/Dept._Rank-Top_5%25-8957E5?style=flat-square)

</div>

---

## 🔬 Research Interests

I am interested in computer vision and deep learning. The question I care about most is whether a reported performance gain comes from the method itself or from over-fitting to a particular dataset, especially when labels are scarce or classes are imbalanced.

I have run into this question in three places so far:

- the public / private leaderboard gap in the AI CUP aortic valve detection challenge,
- the frozen-method, held-out, and ablation design of my version-aware RAG paper,
- a dataset-split validation bug I fixed in [roboflow/supervision](https://github.com/roboflow/supervision/pull/2611).

Advisor: Prof. Meng-Yen Hsieh (謝孟諺), Providence University.

## 📰 Recent

| Date | Update |
|:--:|---|
| `2026/10` | Oral presentation at **TANET & ICS 2026** (Oct 29–31) — *Conditional Version-Aware Retrieval for Evolving Health Guidelines* |
| `2026/09` | Dataset-split validation fix merged into **[roboflow/supervision](https://github.com/roboflow/supervision/pull/2611)** |
| `2026/07` | **Silver Award**, ICPC Taiwan Private University Programming Contest (PUPC) 2026 |

---

## 📄 Publications

> Both papers come from one research line. The first builds a complete system, and its future work calls for grounding the agent's answers in retrieved medical literature. The second narrows down to one retrieval problem that surfaced there and studies it with a controlled experimental design.

### Conditional Version-Aware Retrieval for Evolving Health Guidelines: Iterative Design and Empirical Evaluation of a RAG Retrieval Policy

[![TANET](https://img.shields.io/badge/TANET_%26_ICS-2026-58A6FF?style=flat-square)](https://tanet2026.ntunhs.edu.tw/)
![Oral](https://img.shields.io/badge/Oral-Accepted-2EA043?style=flat-square)
![First Author](https://img.shields.io/badge/First_Author-Yu--Chi_Hsu-6E7681?style=flat-square)

**Yu-Chi Hsu**, Meng-Yen Hsieh

- **Problem.** Health guidelines are revised over time. Standard RAG ranks by relevance or recency, so it cannot serve both historical-comparison queries (which need evidence from several versions) and current-practice queries (which need only the applicable version).
- **Method.** Route each query by intent, and apply version-pair boosting only to explicit historical queries. All other queries keep standard recency ranking.
- **Evaluation design.** Developed on a 96-query pilot set, then froze the method, parameters, corpus, and version relations before building a separate 40-query held-out set. A query entered the test set only if three isolated LLM reviewers approved it unanimously (no majority vote). Ground truth comes from the WHO guideline text.
- **Result.** On the 20 historical-comparison queries, necessary-evidence Recall@3 improved from **0.100 → 0.525** (p = 0.000244). Ablations across six system configurations show the gain comes from version pairing, not from dropping the recency weight. The method retrieved no inapplicable outdated evidence on the 10 hard-negative queries.
- **Limitation.** This is a small-scale, retrieval-only evaluation. Generated-answer quality has not been evaluated yet.

[📖 Conference](https://tanet2026.ntunhs.edu.tw/) · [💻 Code & experiments](https://github.com/archie0732/healthy-diet-ai-agent)

<details>
<summary><b>中文摘要</b></summary>
<br>

健康指引常有新舊版本並存，傳統 RAG 只依相關度或時效排序，無法同時處理需要跨版本證據的歷史比較查詢與只需現行版本的查詢。我提出先以查詢意圖路由判斷是否需要歷史證據，只對明確的歷史查詢啟用版本配對加權。我在 96 題 pilot 上完成開發後凍結方法與參數，再另建 40 題 held-out 測試集，每題都需經三個互相隔離的 AI 審查一致通過才收錄。在 20 題歷史比較查詢中，必要證據 Recall@3 由 0.100 提升至 0.525（p = 0.000244），消融實驗顯示改善主要來自版本配對。目前的限制是評估規模仍小，且尚未驗證生成答案的品質。

</details>

### An Intelligent Healthy Diet Management System Based on Visual Recognition and Tool-Augmented Generation

[![TCSE](https://img.shields.io/badge/TCSE-2026-58A6FF?style=flat-square)](https://tcse2026.seat.org.tw/%E8%AD%B0%E7%A8%8B/%E8%AB%96%E6%96%87%E8%AD%B0%E7%A8%8B)
![Presented](https://img.shields.io/badge/Presented-22nd_TCSE-2EA043?style=flat-square)
![First Author](https://img.shields.io/badge/First_Author-Yu--Chi_Hsu-6E7681?style=flat-square)

視覺辨識與工具增強生成架構之智慧健康飲食管理系統

**Yu-Chi Hsu**, Chun-Fang Pan, Chun-Ting Wu, Yi-Wen Lin, Meng-Yen Hsieh

- A fully local, closed-loop system with no cloud API. A YOLOv12s detector with attention-augmented C2f (A2C2f) blocks and Distribution Focal Loss recognizes foods in meal photos, including occluded and sauce-covered items.
- A calorie engine estimates food weight from bounding-box area, computes energy with the Atwater system, and compares it against a personalized BMR / TDEE baseline (Mifflin-St Jeor).
- A locally deployed Gemma 4 agent decides whether a query needs tool calls. A background memory-compression module keeps the context of each interaction at roughly 500 tokens, however long the usage history grows.
- **My role.** I designed and implemented the web frontend, the Rust (Axum / Tokio / SQLx) backend and database, the agent core, the calorie engine, and the memory mechanism, and I wrote the paper. Teammates trained the YOLO models.

[📖 Conference program](https://tcse2026.seat.org.tw/%E8%AD%B0%E7%A8%8B/%E8%AB%96%E6%96%87%E8%AD%B0%E7%A8%8B) · [💻 System](https://github.com/PU-Hub/healthy-diet) · [🌐 Live demo](https://healthy-diet-web.vercel.app) (read-only demo account on the login page)

<details>
<summary><b>中文摘要</b></summary>
<br>

我設計了一套在本地端閉環運作的健康飲食管理系統。使用者上傳餐點照片後，系統以導入 A2C2f 注意力模組與 Distribution Focal Loss 的 YOLOv12s 辨識食材，再由熱量計算引擎依邊界框面積推估重量，並以 Atwater 係數與 Mifflin-St Jeor 公式估算熱量與個人化基準。決策中樞為本地部署的 Gemma 4，只有涉及健康評估時才調用工具檢索生理資料。動態記憶壓縮機制讓單次互動的 token 負載穩定在約 500 以內。我負責前端、Rust 後端與資料庫、AI 代理核心、熱量計算引擎與記憶機制，並撰寫論文，YOLO 模型由組員訓練。

</details>

---

## 🤝 Open-Source Contributions

<div align="center">

[![supervision](https://img.shields.io/github/stars/roboflow/supervision?style=for-the-badge&logo=github&label=roboflow%2Fsupervision&color=6E40C9)](https://github.com/roboflow/supervision)
[![Alexandrie](https://img.shields.io/github/stars/Smaug6739/Alexandrie?style=for-the-badge&logo=github&label=Alexandrie&color=6E40C9)](https://github.com/Smaug6739/Alexandrie)
[![ytmdesktop2](https://img.shields.io/github/stars/Venipa/ytmdesktop2?style=for-the-badge&logo=github&label=ytmdesktop2&color=6E40C9)](https://github.com/Venipa/ytmdesktop2)
[![DPIP](https://img.shields.io/badge/ExpTechTW-DPIP-6E40C9?style=for-the-badge&logo=github)](https://github.com/ExpTechTW/DPIP)

</div>

| Project | Contribution | Status |
|---|---|:--:|
| **[roboflow/supervision](https://github.com/roboflow/supervision)** <br><sub>Computer vision library</sub> | [#2611](https://github.com/roboflow/supervision/pull/2611) — `DetectionDataset.split()` and `ClassificationDataset.split()` silently accepted ratios outside [0, 1], which could produce a split with no held-out data. Added validation, tests for nine invalid and boundary cases, docs, and a changelog entry. I took over the issue after its discussion had stalled. | ![Merged](https://img.shields.io/badge/-Merged-8957E5?style=flat-square) |
| **[ExpTechTW/DPIP](https://github.com/ExpTechTW/DPIP)** <br><sub>Taiwan earthquake early-warning app</sub> | [#546](https://github.com/ExpTechTW/DPIP/pull/546) — Spoken announcement of the estimated intensity before the alarm sound, with foreground detection, two-level timeouts, and fallback when TTS fails. <br>[#568](https://github.com/ExpTechTW/DPIP/pull/568) — Revised after code review: moved to accessibility settings (off by default), added replay announcements, and updated translations for 12 languages. | ![Merged](https://img.shields.io/badge/-Merged-8957E5?style=flat-square) |
| **[Smaug6739/Alexandrie](https://github.com/Smaug6739/Alexandrie)** <br><sub>Open-source note-taking system</sub> | [#694](https://github.com/Smaug6739/Alexandrie/pull/694) — Traditional and Simplified Chinese localization (32 files), adapting regional terminology and fixing locale resolution for `zh-*` tags. Also [#690](https://github.com/Smaug6739/Alexandrie/pull/690) and [#681](https://github.com/Smaug6739/Alexandrie/pull/681). | ![Merged](https://img.shields.io/badge/-Merged-8957E5?style=flat-square) |
| **[Venipa/ytmdesktop2](https://github.com/Venipa/ytmdesktop2)** <br><sub>YouTube Music desktop client</sub> | [#255](https://github.com/Venipa/ytmdesktop2/pull/255) — Always-on-top, click-through desktop lyrics overlay. The plugin sends a clock signal only when the playback state changes, and the overlay interpolates time locally at 60 fps. | ![In review](https://img.shields.io/badge/-In_Review-D29922?style=flat-square) |

---

## 🚀 Selected Projects

<div align="center">

<a href="https://github.com/archie0732/healthy-diet-ai-agent"><img width="48%" src="https://github-readme-stats.vercel.app/api/pin/?username=archie0732&repo=healthy-diet-ai-agent&theme=github_dark&hide_border=true&border_radius=10" alt="healthy-diet-ai-agent"/></a>
<a href="https://github.com/archie0732/AICUP-2025-Aortic-Valve-Detection"><img width="48%" src="https://github-readme-stats.vercel.app/api/pin/?username=archie0732&repo=AICUP-2025-Aortic-Valve-Detection&theme=github_dark&hide_border=true&border_radius=10" alt="AICUP-2025-Aortic-Valve-Detection"/></a>
<a href="https://github.com/archie0732/auto-check-hw"><img width="48%" src="https://github-readme-stats.vercel.app/api/pin/?username=archie0732&repo=auto-check-hw&theme=github_dark&hide_border=true&border_radius=10" alt="auto-check-hw"/></a>
<a href="https://github.com/archie0732/manga-discord-bot"><img width="48%" src="https://github-readme-stats.vercel.app/api/pin/?username=archie0732&repo=manga-discord-bot&theme=github_dark&hide_border=true&border_radius=10" alt="manga-discord-bot"/></a>

</div>

| Project | Highlight |
|---|---|
| 🍎 **[healthy-diet-ai-agent](https://github.com/archie0732/healthy-diet-ai-agent)** | Agent and RAG component of VerHealth Agent, with the experiments for the version-aware retrieval paper. Written entirely by me. |
| 🫀 **[AICUP-2025-Aortic-Valve-Detection](https://github.com/archie0732/AICUP-2025-Aortic-Valve-Detection)** | My AI CUP 2025 entry. Keeps every version of the code, training configs, score history, and failed attempts. |
| 🧪 **[auto-check-hw](https://github.com/archie0732/auto-check-hw)** | An online judge I built as a C/C++ teaching assistant so students could submit work and get results right away. It grew out of [coding-bot-v2](https://github.com/archie0732/coding-bot-v2), a Discord bot. |
| 📝 **[TA-auto-script](https://github.com/archie0732/TA-auto-script)** | OCR plus web automation for tutoring records. The university approved it and passed it on to later TAs. It cut each entry from about 30 minutes to about 5. |
| 🤖 **[manga-discord-bot](https://github.com/archie0732/manga-discord-bot)** | A long-running update-notification bot that serves 214 Discord servers. |

<sub>Other: npm packages, a VS Code extension (Dot Art In Code), and competitive-programming solution repositories in C++ and Rust.</sub>

---

## 🏆 Competitions

| | Year | Competition | Result |
|:--:|:--:|---|---|
| 🏅 | 2025 | AI CUP 2025 Fall — Aortic Valve Detection in CT | **Honorable Mention** (Ministry of Education). 20th of 536 teams on the private leaderboard (top 3.7%). I led data preprocessing, model training, and analysis. |
| 🎖️ | 2025 | AI CUP 2025 Fall — Cardiac Muscle Segmentation I | Top 25% of 536 teams. I took part in method discussion and selection. |
| 🥈 | 2026 | ICPC Taiwan Private University Programming Contest (PUPC) | **Silver Award** |
| 🎖️ | 2025 | ICPC Taiwan Private University Programming Contest (PUPC) | Honorable Mention |
| 🥉 | 2024 | ICPC Taiwan Private University Programming Contest (PUPC) | Bronze Award |
| 🥉 | 2025 | ICPC Asia Taiwan Online Programming Contest (TOPC) | Bronze Medal |
| 🎖️ | 2025 | ICPC Asia Taichung Regional Contest | Honorable Mention |

<sub>I have also competed in NCPC (preliminary and final rounds) and solved 700+ problems on LeetCode.</sub>

---

## 🎓 Education

**B.S. in Computer Science and Information Engineering** · Providence University, Taichung, Taiwan · *2023 – 2027 (expected)*

- Ranked in the top 5% of the department in most semesters, and 1st of 124 in the fall semester of my second year.
- Relevant coursework: Image Processing, Advanced Deep Learning, Introduction to Computer Vision, Artificial Intelligence, Algorithms, Data Structures, Operating Systems, Linear Algebra, Probability and Statistics.

## 💼 Experience

- **Research Assistant (part-time)** · NSTC-funded project on speech and publication control in Taiwan before the lifting of martial law (1975–1987), PI Prof. Yao-Chung Su · *2024 – 2026*
  I digitized martial-law-era publications through scanning, OCR, and proofreading, and I adapted an open-source OCR tool to handle vertical layouts, legacy typefaces, and degraded scans.
- **Teaching Assistant** · C/C++ Programming, Java Programming, and Programming for the International College (taught in English)
- **Lab Administrator** · Department of CSIE, since my second year

---

## 🧰 Tech Stack

<div align="center">

**Languages**

<img src="https://skillicons.dev/icons?i=cpp,c,python,ts,rust,go,java,kotlin,dart&perline=9" alt="Languages"/>

**Machine Learning & Computer Vision**

<img src="https://skillicons.dev/icons?i=pytorch,opencv&perline=2" alt="ML and CV"/>

<sub>Ultralytics YOLO · llama.cpp</sub>

**Backend, Systems & Tools**

<img src="https://skillicons.dev/icons?i=nodejs,flutter,postgres,docker,linux,git,githubactions,vercel&perline=8" alt="Backend and tools"/>

<sub>Rust Axum · Tokio · SQLx</sub>

</div>

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F2027,50:203A43,100:2C5364&height=100&section=footer" width="100%"/>

</div>
