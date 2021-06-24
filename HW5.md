# 第五週上課筆記-虛擬機

## 虛擬機 v.s 模擬器

```

虛擬機:電腦平台和終端使用者之間建立一種環境，而終端使用者則是基於虛擬機器這個軟體所建立的環境來操作其它軟體。
模擬器: 模擬器是利用實體電腦，建立被模擬電腦，然後將被模擬電腦的程式透過直譯器在實體電腦上執行。

```
## 堆疊機介紹
```
電腦科學中一種計算模型，這種類型的電腦，記憶體以堆疊（Stack）儲存。

這種機器，它的指令集中包含了零位址指令（"0-operand" instruction set）。
硬體在執行運算時，到堆疊的頂端去取出運算元，至運算結束時，再儲存到堆疊的頂端。

相較於累加器（採用 "1-operand instruction set"） ，和暫存器機（"2-operand instruction set" 或 "3-operand instruction set"），用零位址指令（"0-operand instruction set"）實作的堆疊機器，它的好處是程式碼密度（code density）相對較大，因此，它的程式通常較小。
```
## 堆疊機的執行

```


```
## 組合語言

一般
```  
ADD R1,R2,R3  
R1=R2+R3
```
堆疊
```  
PUSH 6  
PUSH 2  
PUSH 3  
ADD  
SUB 
```  

## Download

* make
```
sudo apt install make
```
* java

```
sudo apt install default-jre
sudo apt install default-jdk

```
## 其他補充
* [上課教材第一章](https://www.slideshare.net/ccckmit/1-73472884?fbclid=IwAR1LMD96oRnp6j_dTWSxM4DDQjVRryt3rW1Hdcps5fMqmGZDFvjpUHRnQO4)
* [上課教材第五章](https://www.slideshare.net/ccckmit/5-73472900?fbclid=IwAR1CwXMF5kxoaqtORcEI8uU0Ju8hOy_d4iFxIZH-5sY2iSGKwGxsGj7_PnU)
* [上課教材第九章](https://www.slideshare.net/ccckmit/9-73472922?fbclid=IwAR1PuGVAjUWpBHDo7lk3LR-uqyNiZQXxQjkeYYja1p-rtjoB5hv--Au4uA0)
* [Fabrice Bellard](https://en.wikipedia.org/wiki/Fabrice_Bellard?fbclid=IwAR3lJMFSs2u1vOcs1SFC4T_7HAHmhgluVrrZ5ypi86We0LE8H9bmAoTUEK8)
* [Java virtual machine](https://en.wikipedia.org/wiki/Java_virtual_machine?fbclid=IwAR14sxknDzlYCbTxBsKUWulzh6hhJoqXdg-Dp-y6Zycbv0DkwhTGau7g3iU)
