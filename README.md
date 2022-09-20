# check_my_ip_with_cloudflare
利用cloudflare的pages或1.1.1.1地址获取自己的广域网出口ip地址

很多童鞋都有利用各种网站API获取自己广域网出口ip地址作为DDNS更新的依据，但有时候这些网站访问不稳定，就会导致DDNS更新失败

下面分享一个利用cloudflare的pages或1.1.1.1地址获取自己的广域网出口ip地址的方法，
因为cloudflare的API服务相比于其它网站的API服务应该是更稳定的

curl -s https://pages.dev/cdn-cgi/trace | grep ip= | cut -c 4-

curl -s https://1.1.1.1/cdn-cgi/trace | grep ip= | cut -c 4-

curl -s https://1.0.0.1/cdn-cgi/trace | grep ip= | cut -c 4-

以上3行命令都可以获取自己的广域网出口ip地址
