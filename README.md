根据自己需求修改，仅使用iOS客户端。
感谢 nondanee 大佬！

配合Surge食用


```
[Rule]
URL-REGEX,https?://interface3?.music.163.com/eapi/batch,NeteaseMusicUnlock
URL-REGEX,https?://interface3?.music.163.com/eapi/v1/search,NeteaseMusicUnlock
URL-REGEX,https?://interface3?.music.163.com/eapi/v1/playlist/manipulate/tracks,NeteaseMusicUnlock
URL-REGEX,https?://interface3?.music.163.com/eapi/song/like,NeteaseMusicUnlock
URL-REGEX,https?://interface3?.music.163.com/eapi/song/enhance/player/url,NeteaseMusicUnlock
URL-REGEX,https?://interface3?.music.163.com/eapi/song/enhance/download/url,NeteaseMusicUnlock
URL-REGEX,https?://interface3?.music.163.com/eapi/artist/top/song,NeteaseMusicUnlock
URL-REGEX,https?://interface3?.music.163.com/eapi/album/privilege,NeteaseMusicUnlock
URL-REGEX,https?://interface3?.music.163.com/eapi/playlist/privilege,NeteaseMusicUnlock
URL-REGEX,https?://interface3?.music.163.com/eapi/v6/playlist/detail,NeteaseMusicUnlock
URL-REGEX,https?://interface3?.music.163.com/(store|eapi/(ad|usersafe|theme|skin|banner|sp|cloudvideo|webcache|experiment|socialsquare|comment|weixin|share|hot|mlivestream|mlog|v1/user/info|appcustomconfig|search/(specialkeyword|defaultkeyword|hot))),REJECT-TINYGIF

AND,((USER-AGENT,%E7%BD%91%E6%98%93%E4%BA%91%E9%9F%B3%E4%B9%90*), (NOT,((DOMAIN,YOUR MUSIC DOMAIN))), (OR,((NOT,((DOMAIN-SUFFIX,music.126.net))), (DOMAIN-KEYWORD,admusic)))),REJECT-TINYGIF
AND,((USER-AGENT,NeteaseMusic*), (NOT,((URL-REGEX,https?://interface3?.music.163.com)))),REJECT-TINYGIF
USER-AGENT,neteasemusic*,REJECT-TINYGIF


[MITM]
skip-server-cert-verify = true
hostname = interface.music.163.com, interface3.music.163.com, YOUR MUSIC DOMAIN
```
