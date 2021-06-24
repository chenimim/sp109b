# 第八週上課筆記-函式庫 + Thread

## pkg-config
```
pkg-config 是一個在原始碼編譯時查詢已安裝的函式庫的使用介面的電腦工具軟體。
C/C++編譯器需要的輸入參數
連結器需要的輸入參數
已安裝軟體包的版本資訊
```

## 指令
```
sudo apt-get install libglib2.0-dev = 安裝glib函式庫
-lm = 連結math.h這個函式庫，因為在c語言中math非標準函式庫，但c++則是
apt install libsqlite3-dev = 安裝sqlite3函式庫
ps = 查看背景及前景執行的程式
& = 背景執行
#ifndef = 如果沒定義則做後續
define = 定義某物
endif = 結束if
```
## vim使用

```
i = 進入編輯模式
Esc = 離開編輯模式
o = 插入一行
yy = 複製一行
dd = 刪除一行
cc = 剪下一行
p = 貼上

```

## 01-basic
```
        #include <stdio.h>
        #include <unistd.h>
        #include <assert.h>
        #include <fcntl.h>
        #include <sys/stat.h>
        #include <sys/types.h>
        #include <string.h>

        int main(int argc, char *argv[]) {
            int fd = open("hello.txt", O_WRONLY | O_CREAT | O_TRUNC, S_IRUSR | S_IWUSR);
            assert(fd >= 0);
            char buffer[20];
            sprintf(buffer, "hello world!\n");
            int rc = write(fd, buffer, strlen(buffer));
            assert(rc == (strlen(buffer)));
            fsync(fd);
            close(fd);
            return 0;
        }
```

## 其他補充
* [延伸補充教材](https://www.slideshare.net/ccckmit/10-73472927?fbclid=IwAR07sm0gCA4DQmWWz9P2ECZtMDa2jfx23z_-8JmE7ThxfwYeEWwopt1YRhE)