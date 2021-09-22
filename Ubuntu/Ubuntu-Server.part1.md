# Ubuntu-Server 的基本介紹 part1

---
* 家目錄

![](https://i.imgur.com/F6MHeac.jpg)

bigred是我們使用者的帳號，@後面的web-ubs2004是主機名稱，~這符號代表我們的家目錄

---

* 元件清單檢查及更新

![](https://i.imgur.com/5uugSXi.jpg)

update 檢查更新清單

![](https://i.imgur.com/nzRqJYw.jpg)

upgrade 更新，更新完reboot

---

* 看目前位置以及cd用法

![](https://i.imgur.com/PDfvY8n.jpg)

pwd 看目前位置

cd 是指返回當前使用者的家目錄，cd / 是去根目錄，cd .. 是指去上一個目錄

---

* 查詢目前主機的IP詳細資訊

![](https://i.imgur.com/j5mayBB.jpg)

hostname -I 是看本機IP

ifocnfig 是整個網路的詳細資訊(遮罩，廣播位址，IPV6，網卡等等)

route 看路由表，目的端和預設砸道

---

* 建立刪除移動檔案和目錄，查看目錄檔案詳細資料

![](https://i.imgur.com/Q3OQYsY.jpg)

1. drwxr-xr-x 前面的d指目錄，假如是-就是指檔案，後面各三個的rwx是指可讀可寫可執行，後面會在container篇介紹到， 後面兩個bigred是擁有者和群組
mkdir 是指建立目錄，touch 是指建立檔案 ，也可以一次建立多個目錄和檔案，例:mkdir -p dvvv/cvvv/bvvv

![](https://i.imgur.com/OUzsVRQ.jpg)

2. 移動檔案和目錄或從新命名

![](https://i.imgur.com/hLY4zY4.jpg)

第一個mv是改名稱，可以看到把test1改成test2了

第二個mv是移動位置，把test2移動到dvvv目錄底下

3. 刪除檔案和目錄

![](https://i.imgur.com/FInL867.jpg)

rm -f 是指刪除檔案，可以看到test1.txt被刪掉了

rm -d 是指刪除目錄，假如目錄之下有東西，它就會提醒你不能刪除，如果要連同目錄和目錄底下的整個檔案都刪除，就需要使用rm -rf

4. ls -al 和 cat 

![](https://i.imgur.com/Ed8FzfE.jpg)

可以看到ls -a 和 ls -al 的差別，一個是簡單呈現，一個是詳細呈現

cat 是指看檔案內容，以電腦名稱來作範例

---

* 查看記憶體、CPU、硬碟

![](https://i.imgur.com/WEukmv0.jpg)

free -mh 就是看記憶體，swap就是當電腦實體記憶體不夠用時，會使用硬碟局部空間作為記憶體的擴充，一旦使用了swap 電腦速度會變非常慢(虛擬記憶體)

CPU部分我們用grep(抓)的概念來擷取我們想要的CPU資訊

df -h 就是看主機的硬體規個，目前是安裝在虛擬機上的系統所呈現的規格
 
---

* 輸出echo和編輯指令nano

![](https://i.imgur.com/xnJ3Jrd.jpg)

echo就是輸出的意思，可以輸出變數，文字和特殊字元

![](https://i.imgur.com/OUE1OJj.jpg)

nano就是編寫的指令，可以用來寫bash也可以更改/目錄的檔案等等

下面的`^O，^K，^X`在nano裡就是儲存，切下和離開


###### tags: `Ubuntu`

















