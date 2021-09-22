# Nginx Conf

개발용 리눅스에서 사용하는 nginx 설정.

## nginx.conf 세팅

nginx.conf 를 오픈.

    $ cd /etc/nginx
    $ sudo mv nginx.conf nginx.conf.org
    $ sudo cp ~/projects/nginx-conf-linux/nginx.conf .

    $ sudo nginx -s reload 

## 사이트 활성화

abc 사이트를 활성화 할 수 있다.

    $ ln -s ../abc.conf sites/enabled
    $ sudo nginx -s reload

## 계정 설정

mac에서는 brew로 nginx를 설치한다.
사용자 계정으로 동작하니 퍼미션 설정이 별도로 필요없다.

linux에서는 기본 http계정으로 동작한다.\
http로 동작하면 개발중인 디렉터리에 접근하지 못한다.\
`nginx.conf`에서 `user`를 세팅해줘야 한다.\

    user drypot wheel;  # arch

## 기타

자세한 내용은 아래를 참고.

<https://github.com/drypot/web-memo>
