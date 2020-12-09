<div dir = 'rtl'>

# داکر ( Docker )
خالی
## کااربرد داکر چیست؟
خالی
## راهنمای نصب داکر
خالی
## چه کسانی از Docker استفاده می کنند؟
خالی
## کانتینرها و داکر
خالی
## اصطلاحاتی که در زمینه ی داکر استفاده می شوند
خالی
### Docker file
خالی
### Docker image
خالی
### Docker containers
خالی
### Docker Hub
خالی
### Docker deployment and orchestration
خالی
### Docker compose
خالی
### kubernetes
خالی
## چگونگی استفاده از Docker و دستورات آن
### چگونه از یک Docker image کانتینر بسازیم؟
همان طور که در بالاتر گفته شد برای ساخت یک کانتینر نیاز به Image داریم. با داشتن این ایمیج و دستور docker run می توان کانتینر مورد نظر را ساخت.

```
sudo docker run -d IMAGE_ID_OR_NAME
sudo docker run -itd IMAGE_ID_OR_NAME
```
در یکی از دستورات بالا از آپشن d و در دیگری از آپشن i و t و d استفاده کردیم. در docker run آپشن های دیگری نیز وجود دارد که در زیر به آن ها اشاره می کنیم:
  - -i : stdin را حتی در صورت متصل نبودن باز نگه می دارد.
  - -t : یک tty از کانتینر می سازد.
  - -p : یک پورت از کانتینر را به یک پورت از هاست متصل می کند.
  - -v : یک مسیر از کانتینر را به یک مسیر از هاست مپ می کند.
  - -a : به STDIN و STDOUT یا STDERR متصل می شود.
  - -d : کانتینر را در بک گراند اجرا می کند.
  - --rm : به صورت اتوماتیک کانتینر را اگر وجود داشت حذف میکند.
  - --name : به کانتینر یک نام اختصاص می دهد.
  در این آدرس می توانید لیست کاملی از آپشن های Docker run را مشاهده کنید.
  https://docs.docker.com/engine/reference/run
### چگونه از حال یک کانتینر باخبر شویم ؟
در این قسمت می خواهیم نسان دهیم چگونه می توان از حال یک داکر باخبر شد.
با دستور ```  docker ps  ```  می توان تمامی کانتینر های در حال اجرا را نشان داد. به عنوان مثال در زیر می توان دید.
```
$ docker ps

CONTAINER ID        IMAGE                        COMMAND                CREATED              STATUS              PORTS               NAMES
4c01db0b339c        ubuntu:12.04                 bash                   17 seconds ago       Up 16 seconds       3300-3310/tcp       webapp
d7886598dbe2        crosbymichael/redis:latest   /redis-server --dir    33 minutes ago       Up 33 minutes       6379/tcp            redis,webapp/db
```
برای دیدن تمامی کانتینر ها  از دستور ``` sudo docker ps -a ``` استفاده می کنیم.
برای دیدن log یک کانتینر از دستور زیر استفاده می کنیم.
``` sudo docker logs ID_OR_NAME_OF_A_CONTAINER ```
برای دیدن اطلاعات یک کانتینر خاص از دستور زیر استفاده می کنیم.
``` sudo docker inspect ID_OR_NAME_OF_A_CONTAINER ```
برای استارت یا استاپ یا ریستارت کردن یک کانتینر از دستور های زیر استفاده می کنیم..
```
sudo docker start ID_OR_NAME_OF_A_CONTAINER
sudo docker stop ID_OR_NAME_OF_A_CONTAINER
sudo docker restart ID_OR_NAME_OF_A_CONTAINER
```
### چگونه وارد کانتینر شویم؟
برای وارد شدن به کانتینر از دستور ``` docker exec ``` استفاده می کنیم.
``` docker exec [OPTIONS] CONTAINER COMMAND [ARG...] ```
به عنوان مثال دستور  ``` $ docker exec -d ubuntu_bash touch /tmp/execWorks ``` فایل /tmp/execWorks را درون کانتینر ubuntu_bash در پس زمینه اجرا می کند.
### چگونه کانتینرمان را پاک کنیم؟
برای پاک کردن یک کانتینر از دستور docker rm استفاده می کنیم.
``` sudo docker rm ID_OR_NAME_OF_A_CONTAINER ``` 
با این دستور تنها کانتینر هایی که در حالت stop هستند را می توان اجرا کرد. اگر کانتینر در حالت start بود از آپشن -f استفاده می کنیم.
## مزایای Docker
خالی

</div>
