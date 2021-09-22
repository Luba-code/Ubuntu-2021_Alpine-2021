# Ubuntu-Server 的基本介紹 part2

---

* 建立一般使用者帳號、密碼

![](https://i.imgur.com/cANkiVQ.jpg)

sudo useradd -m -s /bin/bash luba 就是創建luba這個帳號

sudo passwd luba 就是給luba 這個使用者新增密碼，系統會請你在輸入一次

我們使用前一篇的cat來看我們帳號密碼有沒有新建成功

![](https://i.imgur.com/JzkW2tN.jpg)

sudo userdel -r 就是刪除一般使用者

---

* 更改網路設定

![](https://i.imgur.com/3BFfgmQ.jpg)

原本的網路IP位址是用DHCP自動配發

![](https://i.imgur.com/68U1CUc.jpg)

改成自己手動更改，由於是yaml檔案，空格的對齊需要注意，錯了IP就改不了

![](https://i.imgur.com/nSY6sgZ.jpg)

改完yaml檔案之後，可以用sudo netplan try先測試看看有沒有錯誤，假如有錯它會提示你，並且部會讓你按enter，如果確定更改後sudo netplan apply 就可以更改IP，遮罩等等，不用reboot

ping 看看 google 有沒有回應，有代表網路是通的

---

* Linux的自創別名:alias

![](https://i.imgur.com/8PgYIJT.jpg)

alias ping='ping -c 4'把ping -c 4 這段名稱命為ping 就可以更精簡指令

另一個是'ls -al'換成dir

---

* sudo權限免密碼

![](https://i.imgur.com/zQPHNe7.jpg)

在%sudo 那行改成 %sudo ALL=(ALL:ALL)  NOPASSWD:ALL

這裡改錯那系統就毀了，不然就是在開機開始時按F4以root帳號進來這裡(/ect/sudoers改好)

---

* 檔案的壓縮、複製

![](https://i.imgur.com/1sHPmfp.jpg)

先創一個空的資料夾，把text1.txt這個文件使用cp複製進去test空目錄裡面，再以ls -al 檢查家目錄和test資料夾有沒有此文件

![](https://i.imgur.com/sSdgKg2.jpg)

先用zip把 test目錄所有的檔案壓縮成test.zip這個檔案，zip -r test test/*

再來刪除原本的目錄，把剛剛的壓縮檔解壓縮下來，確認壓縮成功unzip test.zip，unzip 檔名 -d (指定目錄)，可以把檔案解壓縮到指定目錄

---

* busybox架站

![](https://i.imgur.com/kD5l8K3.jpg)

使用busybox httpd -p 9467 -h (目錄位置，裡面要有index.html)，把製作的簡易網站架起來，使用ps -aux | grep 去看busybox的程序有沒有啟動

![](https://i.imgur.com/uvgei6W.jpg)

用curl 這指令去檢查建的網站內容


###### tags: `Ubuntu`