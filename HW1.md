# 第一週上課筆記-簡介與環境安裝

## 上課前需要安裝的程式

* Visual Studio Code (vscode)
* CodeBlocks
* git + bash
* msys2

## gcc

* -c:不連結，輸出fib
* -S:只編一不連結，輸出fib.s(組合元)
* $ gcc -S sum.c -o sum.s(組合語言)
* $ gcc -c sum.s -o sum.o(轉換成目的碼)


## .cpp/.c

*  g++ hello.cpp -o hello(編譯成執行檔)
* C語言中沒有 cout << ，std 的用法


## Markdown
* [什麼是Markdown?](http://programmermedia.org/root/%E7%A8%8B%E5%BC%8F%E4%BA%BA%E5%AA%92%E9%AB%94/%E6%8A%80%E8%83%BD/Markdown.md?fbclid=IwAR2mvWFpBup1JykyLqNkIDw3Vb8_VHS-nJEzdv-Ny0JpmXMg8V91fzK9XD8)

## 這一堂課的主要操作

* gcc sum.c
* ./a.out
* gcc sum.c -o sum
* ./sum
* gcc fib.c
* gcc -c fib.c -o fib
* gcc -S fib.c -o fib.s

### Makefile 特殊符號
```
$@ : 該規則的目標文件 
$* : 代表 targets 所指定的檔案，但不包含副檔名。
$< : 依賴文件列表中的第一個依賴文件。 
$^ : 依賴文件列表中的所有依賴文件。
$? : 依賴文件列表中新於目標文件的文件列表。

?= 語法 : 若變數未定義，則替它指定新的值。
:= 語法 : make 會將整個 Makefile 展開後，再決定變數的值。
```