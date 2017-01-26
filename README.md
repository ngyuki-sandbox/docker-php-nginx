# docker-php-nginx

alpine ベースの nginx と php-fpm のイメージで PHP アプリを実行するサンプル。

- php の apache こみのイメージよりもトータルのサイズはかなり軽量
    - php の apache こみだと alpine ベースがないため
- nginx と php-fpm の通信は unix ドメインソケット
    - /var/run をボリュームにして共用
- php-fpm のイメージに nginx を追加して runit で両方動かすとかのが良いかも？
