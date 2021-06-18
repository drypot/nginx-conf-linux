# Nginx Conf

개발용 리눅스에서 사용하는 nginx 설정.

## nginx.conf 세팅

nginx.conf 를 오픈.

    $ cd /usr/local/etc/nginx
    $ sudo vim nginx.conf

nginx.conf 설정 적당한 곳에 아래 행을 삽입.

    include /home/drypot/projects/nginx-conf-linux/sites/enabled/*;

    $ sudo nginx -s reload 

## 사이트 활성화

abc 사이트를 활성화 할 수 있다.

    $ cd sites  
    $ ln -s ../abc.conf enabled

    $ sudo nginx -s reload

## 기타

자세한 내용은 아래를 참고.

<https://github.com/drypot/linux-memo>
