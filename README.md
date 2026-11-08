# PAYDAY 2 模組與火拼配置筆記

資料查證時間：2026-09-28～29（遊戲版本 Update 248.2 之後）。

- [HUD 模組推薦與安裝](#hud-模組推薦與安裝)（本頁）
- [火拼流派：槍枝選擇＋天賦點法](loud-builds.md)

## HUD 模組推薦與安裝

### 結論：裝 VanillaHUD Plus（VHUD+）一個就夠

- WolfHUD 的後續版本，資訊最完整，有中文，持續更新中，支援 64 位元新版遊戲。
- **中文只有簡體。** 遊戲官方和 VHUD+ 都只有簡中；VHUD+ 的簡中語系檔與英文版字串一一對應（1283 條全部有翻）。目前沒有還在更新的繁中化模組，只有一個 2020 年的「Traditional Chinese Fonts 繁體中文字庫」讓聊天和名字能顯示繁體，不翻譯介面。
- **不推薦：** WolfHUD（已停更）、VoidUI（有簡中，但 2024/4 後沒更新，64 位元更新後有人回報進標題畫面就當掉）。
- HUD 模組只裝一個，不要和 VoidUI 等其他 HUD 同時裝，容易衝突。

### 安裝（2026 年 8 月 Update 247 起遊戲改為 64 位元，舊教學的 SuperBLT 不能用）

1. Steam 對 PAYDAY 2 按右鍵 → 內容 → 一般 → 語言，改成簡體中文。**開遊戲前先做**：VHUD+ 第一次建立設定時會照遊戲語言決定語言，存好後就不會再跟著遊戲改。
2. 安裝 [SuperBLT 64-bit](https://modworkshop.net/mod/58342)（目前為 beta）：把 `WSOCK32.dll` 放到 `PAYDAY2.exe` 同一個資料夾。啟動時問要不要下載 basemod，選 Yes。
   以前裝過 32 位元版的，先刪掉舊的 `IPHLPAPI.dll`／`WSOCK32.dll` 和 `mods/base`。
3. 下載 [VHUD+](https://modworkshop.net/mod/25629)（實際檔案在作者的 [GitLab](https://gitlab.com/steam-test1/alternative-updates/-/raw/main/update/vanhudplus.zip)），解壓到 `PAYDAY 2/mods/`，結構為 `mods/VanillaHUD Plus/mod.txt`。
4. 如果 VHUD+ 還是英文：選項 → Mod Options → VanillaHUD Plus Settings → Language → Chinese，重新載入地圖後生效。
5. VHUD+ 之後有新版會在遊戲內提示更新。

### 這台電腦的安裝狀態（2026-09-28）

- 遊戲路徑：`C:\Program Files (x86)\Steam\steamapps\common\PAYDAY 2`（64 位元版，`PAYDAY2.exe`）
- `WSOCK32.dll`：SuperBLT 4.0.4-beta，SHA256 `D75EBC83A210CD7D521C289CECB508F7DC5D2D782C43C05C5CB7DBCACCCB2FE0`，簽章有效（簽署者 Sidetrack Games B.V.）
- `mods/VanillaHUD Plus/`：VHUD+ 3.4.18，91 個檔案，含 `loc/schinese.json`
- 尚未完成：Steam 語言切換、第一次啟動下載 basemod（需手動點 Yes）

### 看現況建議開啟的設定（VanillaHUD设置）

| 選單 | 開啟項目 | 用途 |
|---|---|---|
| HUD信息选项 | 计时器、对讲机與计数、人质／平民／敌人數量、ECM、摄像头回路、战利品、BUFF | 看現況最主要的面板（鑽頭進度、對講機剩餘、人數等） |
| 横幅选项 | 高级突击横幅、波次计数器 | 看突擊階段與第幾波 |
| 警戒度设置 | 显示警戒数值 | 潛入時以百分比顯示被發現程度 |
| 常规HUD面板选项 | 显示倒地计数器 | 看隊友還能倒幾次 |
| 敌人血量指示器、受击指示器 | 開啟 | 戰鬥時看敵人血量與受擊方向 |

### 來源

- [VanillaHUD Plus – ModWorkshop](https://modworkshop.net/mod/25629)
- [VPlusHUD – GitHub（語系檔）](https://github.com/steam-test1/VPlusHUD)
- [Void UI – ModWorkshop](https://modworkshop.net/mod/20997)
- [SuperBLT 官網](https://superblt.znix.xyz/)
- [SuperBLT 64-bit Beta – ModWorkshop](https://modworkshop.net/mod/58342)
- [PAYDAY 2 Update 247 Changelog](https://www.paydaythegame.com/news/payday2/2026/08/payday-2-update-247-changelog/)
- [Diesel Engine 3.0 for Modders – Steam](https://steamcommunity.com/app/218620/discussions/15/563661122262044019/)
- [Traditional Chinese Fonts – ModWorkshop](https://modworkshop.net/mod/34512)
