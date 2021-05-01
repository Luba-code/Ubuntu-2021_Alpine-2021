# Install Alpine

---
建置環境
* 先新增的一個新的虛擬機器

![](https://i.imgur.com/ChVoeKW.png)

* 選第3個自己去設定這台虛擬機器的內容

---
建置環境
* 選擇所需的系統和選擇版本

![](https://i.imgur.com/iZ6jPq7.png)

* 選 Linux
* 下拉選單:Other Linux (5.x) and later kernel 64-bit
    1.這邊選的是內核的版本就是kernel的版本

---
建置環境
* 設定虛擬機名稱和位置

![](https://i.imgur.com/r984djY.png)

* 名稱
    1.打安裝日期(測試)
        `AP0413`
    2.打要做的案子架構名稱+版本代號(正規)
        `例:web-alpine03143 ` 
* 位置
    1.方便紀錄盡量放C槽給好檔名 

---
建置環境
* 設定硬體大小和備分的情況

![](https://i.imgur.com/X7gQURl.png)

* 硬體當然越大越好，但要考慮你這台主機的硬體大小做抉擇，因為我們做測試所以設10G就好
* 因為檔案會做備份的動作，所以要選單一檔案，選下面分割的話備份檔案會很麻煩，現代備份也不會用到需要分割檔案的情況。

---
建置環境
* 使用系統iso檔

![](https://i.imgur.com/W4SJZUH.png)

---
* 使用NAT構造

![](https://i.imgur.com/eNlmHYp.png)

* 這邊選Bridge的話設定apline進去的話連結不到下載元件的網站
---
* 移除不必要的設備

![](https://i.imgur.com/3wz6PGV.png)

* USB、Sound Card、Printer

---
建置環境完成

![](https://i.imgur.com/NXAmAUm.png)

* 設定好按Finish就可以了

---
Alpine Linux 系統設定

* 打開一開始顯示的樣子

![](https://i.imgur.com/i5CWswO.png)

* 它會預設的登入帳號為 `root` ，而且沒有密碼

![](https://i.imgur.com/3ZvQ7Qq.png)

* 輸入： `root`
* 輸入： `setup-alpine` (alpine的系統設定)

---
* 鍵盤配置

![](https://i.imgur.com/vvI5Dfu.png)

* 第一行問你要選哪種配置
    輸入:`tw` (tw=taiwan)
* 第二行問你備用配置
    輸入:`tw` (tw=taiwan)

---
* 電腦名稱

![](https://i.imgur.com/rgGtDqL.png)

* 第一行我輸入`AP0413`它顯示`[a-z][0-9]or-`是指主機名稱只能小寫字母以及數字0~9符號只能用-
* 重新輸入:`web-apline-3-14-3`(使用什麼類型)(版本代號)

---
* 設定網路卡

![](https://i.imgur.com/2OwFJcs.png)

* 第一行問你要不要用etho網路卡選`eth0`(預設)
* 第二行問你要不要用DHCP選`dhcp`(預設)
    1.不想用預設可以自己打IP，但要是有效IP，不然連不到下載元件網站的清單
* 第三行問你還要不要對上兩個操作做更改`n`(預設)

---
* 設定密碼

![](https://i.imgur.com/yifjRzr.png)

* 目前還是root的權限，密碼打`root`就好

---
* 設定時區

![](https://i.imgur.com/CdmvpEt.png)

* 第一行問你哪一區的時區選:`Asia`(亞洲)
* 第二行選哪一個國家的時區:`Taipei`(台北)

---
* 設定代理伺服器和NTP協定

![](https://i.imgur.com/sCbMp2a.png)

* 第一行問你proxy是代理伺服器要不要設定，需要的話就打代理伺服器IP不用就預設`none`(預設)
    1.會用到proxy是因為企業內網需要連到外面需要一組對外伺服器，所以才需要設定這個
* 第二行問你NTP協定用哪個選預設`chrony`(預設)
    1.NTP協定是在資料網路電腦系統之間通過封包交換進行時鐘同步的一個網路協定

---
* 設定 alpine repository 與 ssh server

![](https://i.imgur.com/7OUrryH.png)

* 設定你要從哪個網站下載元件
    1.假如前面不使用DHCP自己設定IP的話，必須有效IP才會跑出清單，沒有的話只會顯示`[1]`什麼都沒有代表你必須重灌
    2.如果你前面網路架構用Bridge，這邊會顯示`[1]`也是什麼都沒有，必須重灌

![](https://i.imgur.com/rvkd9qM.png)

* 安裝ssh服務這邊選預設`openssh`(預設)

---
* 安裝 alpine 到硬碟中

![](https://i.imgur.com/F4Cqy8F.png)

* 第一行問你要用哪個硬碟選`sda`(硬碟名稱)
* 第二行問你要怎麼使用選`sys`(系統)
* 第三行問你要清空硬碟嗎`y`(預設)

---
* alpine 系統設定完成

![](https://i.imgur.com/nsuaUHG.png)

* 它會要你重開所以重開執行就完成設定了`reboot`(重開)


###### tags: `Alpine`




















