1. httpd-vhosts.conf
    <!-- webmusic.todo.vn: Domain name
    DocumentRoot: nơi lưu trữ code để chạy Laravel -->
    <VirtualHost webmusic.todo.vn:443>
        DocumentRoot "F:/Music/public"
        ServerName  webmusic.todo.vn
        <Directory "F:/Music/public">
            Options FollowSymLinks
            AllowOverride All
            DirectoryIndex index.php
            Require all granted
        </Directory>
    SSLEngine on
        SSLCertificateFile "conf/ssl.crt/server.crt"
        SSLCertificateKeyFile "conf/ssl.key/server.key" 
    </VirtualHost>
2. host
    <!-- webmusic.todo.vn: Domain name -->
    127.0.0.1  webmusic.todo.vn
3. Apache(httpd.conf)
    Listen 127.0.0.1:443
    Listen 80
4. Run https://webmusic.todo.vn/
    - Nếu báo nguy hiểm chọn Advance    
