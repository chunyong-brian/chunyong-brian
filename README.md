# HomeBox

**自己的主機，自己的部署平台。**
把 GitHub 上的專案部署到自己家裡、公司裡的硬體上，有 HTTPS 網址、有範本、有管家，不用把程式碼和資料交給任何雲端。

*Self-hosted PaaS in a box: deploy from GitHub to your own hardware, with HTTPS, templates and an AI steward. Your code and data stay with you.*

---

## 它做什麼

- **貼 GitHub repo 就能部署**：連結自己的 GitHub 帳號、選 repo，HomeBox 自動讀 Dockerfile／compose／.env.example，列出要填的變數、要建的資料庫，按下去幾分鐘後網址就打得開。推送新版自動重新部署。
- **幾百個範本一鍵裝**：WordPress、n8n、PostgreSQL、Redis、Ghost……每個範本都經過自動安全檢查與資源上限，HomeBox 驗證過的另外標示。
- **自動 HTTPS 網址**：透過 Cloudflare Tunnel，家裡沒有固定 IP、不用開防火牆，每個服務都有自己的 `https://` 網址；也能綁自己的網域。
- **多人工作區**：平台擁有者邀請成員，成員用 Google 登入、各自連結 GitHub；誰能用多少 CPU／記憶體、幾個服務，都在後台設。一個人用就只要本機帳號＋TOTP。
- **管家（AI 助手）**：在工作區對管家說「幫我建一個 n8n」「看一下這個服務為什麼掛了」，它會動手；會動到東西的操作都要你按確認才做。
- **全部在後台設定，不用 SSH、不用寫腳本**：安裝、更新、引擎、網域、登入方式、GitHub App、額度，一頁一頁點完就能用。

## 它跑在哪

- 一台 Raspberry Pi 5（或任何 Linux 小主機）就夠。
- 部署引擎用 [Coolify](https://coolify.io)，HomeBox 負責把它包成「不用懂 DevOps 也能用」的產品：隔離的工作區網路、每個容器的資源上限、主機加固、版本盤點與一鍵更新。
- 資料和執行環境都在你自己的機器上；Google 登入、GitHub、Cloudflare 是唯一的外部依賴。

## 為什麼做這個

雲端 PaaS 很方便，但月費會一直長，程式碼和資料也不在自己手上。
HomeBox 的目標是：**買一台小盒子插上網路，就得到一個自己的 Zeabur／Vercel**，而且是你完全掌握的。

---

<sub>HomeBox 還在開發中，功能與畫面會持續變動。</sub>
