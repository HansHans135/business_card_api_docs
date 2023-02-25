# API文檔
https://mycard.lol
---
## 說明:
</br>
api響應格式: json</br>
api網址: https://mycard.lol/api</br></br>
文黨標示說明:</br>
若遇到[ ]例如 demo.com/api/[id] </br>
請將[id]替換成自己的文字(無須加[])</br>

---
## 1. /api/alldata
</br>
> get</br>
回傳所有用戶資訊:</br>
json:</br>
</br></br>響應200

```json
{
  "alluser":["612471739217346561.json","864362079459475477.json"],
  "allcode":["hans.json","nana.json"]
}
```

</br>
json項目:</br>
allfilt:所有用戶資訊檔案(list)</br>
alldata:所有代碼資訊檔案(list)

---
## 2. /api/user/[id]
</br>
> get</br>
顯示用戶資訊</br>
json:</br>
</br></br>響應200

```json
{
  "address":"\u7121",
  "code":"hans",
  "email":"ccoccc14@gmail.com",
  "facebook":"https://www.facebook.com/dripweb.cf/",
  "hand":"https://cdn.discordapp.com/avatars/851062442330816522/9a53bcd00399a42a4155622c86f516bc.png?size=1024",
  "id":851062442330816522,
  "info":"\u4f60\u4e0d\u597d\n\u5f88\u4e0d\u9ad8\u8208\u8a8d\u8b58\u4f60",
  "instagram":"https://www.instagram.com/n.ahans._/",
  "look":2,
  "name":"\u4ea8.",
  "phone":"\u7121",
  "title":"\u958b\u767c\u8005",
  "web":"\u95dc\u65bc\u6211-hans",
  "youtube":"https://www.youtube.com/@hans0805/",
  "webhook_send":"HI HI"
}
```

</br>
響應404

```json
{
  "error":"404",
}
```

</br>
json項目:</br>
code:短網址</br>
email:電子郵件</br>
facebook:fb網址</br>
hand:頭像網址</br>
id:用戶id</br>
info:自我介紹</br>
instagram:ig網址</br>
look:網頁瀏覽次數</br>
name:名子</br>
phone:電話號碼</br>
title:標題</br>
web:網頁標題</br>
youtube:yt網址</br>
webhook_send:指令/webhook自訂項目</br>
(若無設定將不會有值)</br>


---
## 3. /api/code/[code]
</br>
> get</br>
顯示代碼資訊</br>
json:</br>
</br></br>響應200

```json
{
  "page":"777451145592700928"
}
```

</br>
響應404

```json
{
  "error":"404",
}
```

</br>
json項目:</br>
page:要導向的用戶ID</br>

---
## 4. /api/edit/user/[id]
</br>
> post</br>
更改用戶資訊</br>


</br>
可設定項目(未標示表示可選,用json傳送):</br>
key:apikey(必填)</br>
email:電子郵件</br>
facebook:fb網址</br>
info:自我介紹</br>
instagram:ig網址</br>
phone:電話號碼</br>
title:標題</br>
web:網頁標題</br>
youtube:yt網址</br>
webhook_send:指令/webhook自訂項目</br>

</br></br>響應200

```json
{
  "ok":["web","info"]
  #list裡面為成功修改的項目
}
```

</br>
響應403

```json
{
  "error":"403",
}
```

</br>
響應400

```json
{
  "error":"400",
}
```


