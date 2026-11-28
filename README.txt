【如何遊玩】
直接用瀏覽器（Chrome / Edge / Safari）開啟 index.html 即可。
第一次進入需要網路（會從 PokeAPI 下載精靈資料與圖片，之後會存在瀏覽器裡）。
若用雙擊開啟遇到音樂或圖片無法載入，可在此資料夾開終端機執行：  python3 -m http.server  再開 http://localhost:8000

【如何換圖片】image 資料夾（檔名固定、PNG、背景透明，解析度不限，遊戲依「格數」橫向等分）
  tiles.png    7 格：地面、草叢、樹、屋、門、水、出口（背景不透明）
  player.png   4 格：朝下、朝上、朝左、朝右
  npc.png      4 格：博士、女孩、店員、護理師（朝下）
  trainer.png  3 格：短褲小子、迷你裙、捕蟲少年（地圖與戰鬥共用）
  mart.png     友善商店（整棟建築，一張圖）
  center.png   寶可夢中心（整棟建築，一張圖）
  gym.png      道館（整棟建築，一張圖；目前是中心的綠色版本，可自行替換）
  house.png    一般住家／研究所（透明背景的單棟房子）
  找不到檔案時，遊戲會自動改用內建的簡易圖形。

【如何換音樂】music 資料夾
  town.mp3     城鎮／野外背景音樂（循環）
  battle.mp3   戰鬥背景音樂（循環）
  沒有檔案時遊戲靜音。瀏覽器需要點擊一次畫面後才會播放音樂。

【其他】更換圖片後若沒有變化，請按 Ctrl+F5 強制重新整理。

【劇情與地圖】
新芽鎮（我的家、研究所、中心、商店）→ 一號道路（5 位訓練家含青梅竹馬）→ 白楊鎮（中心、商店、住家、道館）。
道館在建築內部：先打贏館內訓練家，再挑戰館主風子，取得疾風徽章後東邊的路才會開放。
地圖資料集中在 index.html 的 MAPS（搜尋「多地圖系統」），可自行新增地圖、傳送點與 NPC。

【招式特效】image/fx 資料夾
  fx_名稱.png，每張 6 格橫排（透明背景）。名稱：tackle dash claw peck punch bite wind whip leaf bolt powder needle quake ring fire water ice dark rock goo
  彈道類（fire water leaf ice dark rock goo needle wind bolt powder ring）：第 1-2 格為飛行、第 3-6 格為命中；其餘為命中動畫。
  目前缺少 fx_dark.png（惡、幽靈系），缺圖時該系招式會使用內建的簡易動畫。

【依招式專屬特效】image/fx/fx_<名稱>.png（有放才會啟用，沒有就用通用特效）
  飛行類（前 2 格飛行、後 4 格命中）：acid psybeam flamewheel swift flamethrower shadowball bubble
  命中類（6 格都在目標身上）：absorb hypnosis rollout rockslide slam karate kick furyattack selfdestruct drillpeck dreameater bodyslam thunderbolt surf psychic toxic darkslash
  對應招式可在 index.html 搜尋 FXAL 修改。
