# 第九週上課筆記-	posix/thread

## vmem.c
* 程式碼
```
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[]) {
    printf("location of code : %p\n", main); 
    printf("location of heap : %p\n", malloc(100e6)); 
    int x = 3;
    printf("location of stack: %p\n", &x); 
    return 0;
}
```
* 結果
```
ubuntu@foo1:~/sp/08-posix/01-basic$ gcc vmem.c -o vmem
ubuntu@foo1:~/sp/08-posix/01-basic$ ./vmem
location of code : 0x563a6a86d189
location of heap : 0x7f4855b70010
location of stack: 0x7ffc816b14d4
```
## pthread函式庫

* 執行
```
#include <pthread.h>
#include <unistd.h>
#include <stdlib.h>
#include <stdio.h> 

void *print_george(void *argu) 
{    
  while (1) {    
    printf("George\n");    
    sleep(1);    
  }    
  return NULL;    
}    

void *print_mary(void *argu) 
{     
  while (1) {    
    printf("Mary\n");    
    sleep(2);    
  }    
  return NULL;    
}    

int main() 
{    
  pthread_t thread1, thread2;     
  pthread_create(&thread1, NULL, &print_george, NULL);    
  pthread_create(&thread2, NULL, &print_mary, NULL);    
  while (1)
   {     
    printf("----------------\n");  
    sleep(1);     
  }    
  return 0;    
}

```
* 結果
```
ubuntu@foo1:~/sp/08-posix/02-thread$ ./georgeMary
----------------
Mary
George
----------------
George
Mary
----------------
George
----------------
George
Mary
----------------
George
```

## 其他補充
* [延伸補充教材，到p.46](https://www.slideshare.net/ccckmit/10-73472927?fbclid=IwAR07sm0gCA4DQmWWz9P2ECZtMDa2jfx23z_-8JmE7ThxfwYeEWwopt1YRhE)