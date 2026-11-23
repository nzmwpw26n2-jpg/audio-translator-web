# 錄音翻譯中心（第一版）

## 功能
- MP3、WAV、M4A 上傳（單檔 25 MB）
- OpenAI Whisper 語音轉文字
- 逐段保留英文並翻譯成繁體中文
- TXT 下載
- 手機與電腦響應式介面

## 尚未包含
- 甲、乙說話者自動區分
- 大於 25 MB 音檔的自動切割
- 使用者登入及歷史紀錄

## 部署設定
在 Vercel 專案的 Settings → Environment Variables 新增 `OPENAI_API_KEY`，再重新部署。金鑰只放在伺服器環境變數，不要提交到 GitHub。

OpenAI API 與 ChatGPT 訂閱分開計費；音檔會傳送至 OpenAI API 處理。部署前請先確認 API 帳戶可用額度及用量限制。

## 本機執行
```bash
npm install
cp .env.example .env.local
# 編輯 .env.local，填入 OPENAI_API_KEY
npm run dev
```
