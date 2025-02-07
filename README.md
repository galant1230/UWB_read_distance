# 📌 GIPS Guide

本指南提供 **GIPS** 設置與距離讀取方式的詳細說明。

## 📥 軟體下載與設置
- **讀取距離程式**：使用 `read_GIPS_distance.py` 來讀取距離。
- **Anchor ID 範圍**：05-09
- **Tag ID 範圍**：01
- **更改 Anchor ID 或 Tag**：
  - 下載 **GIPS 設定 APK**：[點擊下載](https://lan.gips.com.tw:5001/sharing/m5QmXeE9U)
  - 參考 **HackMD 設置指南**：[點擊查看](https://hackmd.io/6aXQLZ-BSSiBUSbpytr1Hw?view)

---

## 🛠 1. 讀取距離設定
- **在電腦上執行**：
  - 修改 `COM_PORT = 'COMX'`，其中 `X` 為電腦的 Port 號碼。
- **在 Raspberry Pi (RPI) 上執行**：
  - 修改 `COM_PORT = '/dev/ttyUSBX'`，其中 `X` 為 USB Port 號碼。

---

## 🔄 2. 更改 Anchor ID
若需更改 **Anchor ID**，需先：
1. **使用 APK 重新燒入韌體**（參考上方下載連結）。
2. 修改下列程式碼內的 **if 判斷式封包數值**：
   ```python
   if packet[0] == 0x02:  # 02 表示基站 ID 為 02
       # 若需更改為 04，請改成：
       if packet[0] == 0x04:

# 📌 研創 Guide

- **讀取距離程式**：使用 read_YCH_distance.py 來讀取距離。 
