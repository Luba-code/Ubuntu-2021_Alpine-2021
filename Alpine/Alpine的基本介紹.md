# Alpine的基本介紹

---

Alpine大部分操作都跟ubuntu類似，只是alpine是更精簡的系統，很適合做一些小型機器的系統，而且也很適合改裝

---

* 檢查更新清單以其更新

![](https://i.imgur.com/wXBoGIh.jpg)

跟ubuntu很類似，只是apt install 改成 apk add

---

* 創建使用者帳號、密碼

![](https://i.imgur.com/TxEy1eN.jpg)

sudo adduser -s /bin/bash -h /home/luba -D luba

是指創建一個luba的帳號以bash來執行程式，alpine預設是sh，然後家目錄設定在/home/luba

addgroup luba wheel是指把luba加入到root權限之下，這邊已經有用bigred做設定了

![](https://i.imgur.com/vGF3o4O.jpg)

去%wheel nopasswd 把那行的註解拿掉，就可以跟ubuntu一樣sudo免密碼了

---

* 更改網路IP、遮罩、預設砸道

![](https://i.imgur.com/qbnfXTh.jpg)

這邊也類似ubuntu，但格式沒那麼嚴謹，gateway都是照VMware預設的，更改完必須重開機

---

* 查網路資訊

![](https://i.imgur.com/qjKtKO0.jpg)

跟ubuntu一樣，只是多了一個ip addr 可以查詢

###### tags: `Alpine`