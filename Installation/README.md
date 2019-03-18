## 樹莓派安裝
#
#### 工具程式及系統：
* 1. [SD Formater](https://www.sdcard.org/downloads/formatter_4/)
![image](https://github.com/jumbokh/rpi_class/blob/master/sdformater.JPG)
* 2. [Win32DiskImager](https://sourceforge.net/projects/win32diskimager/)
* 3. [putty 終端機程式](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
* 4. [作業系統](https://www.raspberrypi.org/downloads/)
* 5. [無線網路監控](https://briian.com/8293/)
#
### [安裝請參考:28頁](https://drive.google.com/file/d/1r3nSUufSA0wO9MLPtAdbwjtJ5fbfT7e9/view)
#
##### 燒錄系統至 SD卡
#
##### config.txt 於檔案最後加以下3行：
###### dtoverlay=pi3-miniuart-bt
###### core_freq=250
###### enable_uart=1
#
##### cmdline.txt 修改成：
###### dwc_otg.lpm_enable=0 console=ttyAMA0,115200 kgdboc=ttyAMA0,115200 root=PARTUUID=22dedadf-02 rootfstype=ext4 elevator=deadline 
###### fsck.repair=yes rootwait splash plymouth.ignore-serial-consoles
#
##### 放一個空的檔案： SSH 至根目錄下 (SD卡目錄最頂端)
#
##### 接下來把 USB-TTL 線連接至樹莓派，先不連接電腦
#
##### 連接樹莓派電源，開啟 "無線網路監控程式"
#
##### 執行 putty 連接
