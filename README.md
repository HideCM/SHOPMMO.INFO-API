

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/othneildrew/Best-README-Template">
    <img src="https://i.ibb.co/t8HXXSf/fav-den.png" alt="Logo" width="120" height="120">
  </a>

  <h3 align="center">SHOPMMO.INFO API</h3>

  <p align="center">
Sau đây là hướng dẫn cách nối API. Ngôn ngữ sử dụng là cURL
    <br />
    <a href="https://shopmmo.info"><strong>VÀO CỬA HÀNG</strong></a>
    <br />
    <br />
    <a href="https://luxproxy.com">Proxy Giá Rẻ</a>
    ·
    <a href="https://zalo.me/0354459420/" target=_blank>Liên hệ qua Zalo</a>
    ·
    <a href="https://github.com/HideCM/SHOPMMO.INFO-API/issues">Request Feature</a>
  </p>
</div>

## 🛒GET - Lấy Danh Sách Tài Khoản Đang Bán

*{domain}/api/**ListResource**.php?**username**=admin&**password**=admin*

 - ***username*** :admin (Tài khoản đăng nhập website **shopmmo.info**)
 - ***password***: admin (Mật khẩu đăng nhập website **shopmmo.info**)

> Website của bạn cần phải sử dụng SSL

**Example Request:** 
```bash
curl --location -g --request GET '{domain}/api/ListResource.php?username=admin&password=admin'
```
<!-- TABLE OF CONTENTS -->
<details>
  <summary>Example Response - Header</summary>
  
```JSON
    {
      "status": "success",
      "categories": [
        {
          "id": "7",
          "name": "DANH SÁCH TÀI KHOẢN GMAIL",
          "image": "https://localhost/assets/storage/images/category_1NS5B048Q2FU.png",
          "accounts": [
            {
              "id": "8",
              "name": "GMAIL RANDOM TÊN TIẾNG ANH +AVATAR+POP3+IMAP+LIVE77H",
              "price": "500",
              "amount": 0,
              "country": "vn",
              "description": "test"
            }
          ]
        },
        {
          "id": "6",
          "name": "DANH SÁCH CLONE FACEBOOK",
          "image": "https://localhost/assets/storage/images/category_8GKUR69W7HJS.png",
          "accounts": [
            {
              "id": "19",
              "name": "Clone very phone",
              "price": "100",
              "amount": 138,
              "country": "vn",
              "description": ""
            },
            {
              "id": "20",
              "name": "Clone novery",
              "price": "100",
              "amount": 0,
              "country": "vn",
              "description": ""
            }
          ]
        },
        {
          "id": "4",
          "name": "DANH SÁCH VIA FACEBOOK",
          "image": "https://localhost/assets/storage/images/category_R36HMAODF14C.png",
          "accounts": [
            {
              "id": "11",
              "name": " Via Cổ Philipin Change Full XMDT",
              "price": "80000",
              "amount": 0,
              "country": "ph",
              "description": "Full backup"
            }
          ]
        },
        {
          "id": "9",
          "name": "TÀI KHOẢN TRAODOISUB.COM",
          "image": "https://localhost/assets/storage/images/category_DXMP3BA8W0RO.png",
          "accounts": [
            {
              "id": "15",
              "name": "Tài khoản TDS 1m xu",
              "price": "20000",
              "amount": 0,
              "country": "vn",
              "description": "Không cấu hình"
            }
          ]
        },
        {
          "id": "10",
          "name": "TÀI KHOẢN AZURE",
          "image": "https://localhost/assets/storage/images/category_SR4GYUE5WLQJ.png",
          "accounts": [
            {
              "id": "18",
              "name": "Tài khoản Azure 1000$",
              "price": "99999",
              "amount": 0,
              "country": "",
              "description": "Vui lòng nhập nội dung mô tả sản phẩm"
            }
          ]
        }
      ]
    }
```
</details>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Example Response - Body</summary>
  

```pmresponseheaders
Date: Fri, 20 Aug 2022 12:58:01 GMT
Server: Apache/2.4.48 (Unix) OpenSSL/1.1.1k PHP/7.3.29 mod_perl/2.0.11 Perl/v5.32.1
X-Powered-By: PHP/7.3.29
Set-Cookie: PHPSESSID=c65a5bd228364ca106caf3c25a780abb; path=/
Expires: Thu, 19 Nov 1981 08:52:00 GMT
Cache-Control: no-store, no-cache, must-revalidate
Pragma: no-cache
Content-Length: 3108
Keep-Alive: timeout=5, max=100
Connection: Keep-Alive
Content-Type: text/html; charset=UTF-8
```

</details>



## 💰GET - Mua Tài Nguyên

*{domain}/api/**BResource**.php?**username**=admin&**password**=admin&**id**=19&**amount**=1*

 - ***username*** :admin (Tài khoản đăng nhập website **shopmmo.info**)
 - ***password***: admin (Mật khẩu đăng nhập website **shopmmo.info**)
 - ***id***: 19 (ID sản phẩm mà bạn đã get được ở API trên)
- ***amount***: 1 (Số lượng tài nguyên bạn cần mua)

> Website của bạn cần phải sử dụng SSL

**Example Request:** 
```bash
curl --location -g --request GET '{domain}/api/BResource.php?username=admin&password=admin&id=19&amount=1'
```
<!-- TABLE OF CONTENTS -->
<details>
  <summary>Example Response - Header</summary>
  

```JSON
    {
      "status": "success",
      "msg": "Thanh toán đơn hàng thành công.",
      "data": {
        "trans_id": "D8TS1629417861",
        "category": "DANH SÁCH CLONE FACEBOOK",
        "name": "Clone very phone",
        "amount": "1",
        "time": 1629417861,
        "lists": [
          {
            "account": "100057821045983|@Khoi2020|c_user=100057821045983; xs=33:lDe8oEsO0mNZdw:2:1605533837:-1:-1; fr=1IEd2imTg4HcSLuHi.AWUnqsmFkVxrq4E2-V5WzMIULSg.BfsoCN.Ml.AAA.0.0.BfsoCN.AWUYILalGXE; datr=hoCyX2pM-zBCa5HT2c9VTCsU\r"
          }
        ]
      }
    }

```
</details>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Example Response - Body</summary>
  

```pmresponseheaders
Date: Fri, 20 Aug 2022 00:04:04 GMT
Server: Apache/2.4.48 (Unix) OpenSSL/1.1.1k PHP/7.3.29 mod_perl/2.0.11 Perl/v5.32.1
X-Powered-By: PHP/7.3.29
Expires: Thu, 19 Nov 1981 08:52:00 GMT
Cache-Control: no-store, no-cache, must-revalidate
Pragma: no-cache
Content-Length: 461
Keep-Alive: timeout=5, max=100
Connection: Keep-Alive
Content-Type: text/html; charset=UTF-8
```

</details>


## 💁‍♀️GET - Thông Tin Sản Phẩm

*{domain}/api/**InfoResource**.php?**username**=admin&**password**=admin&**id**=19*

 - ***username*** :admin (Tài khoản đăng nhập website **shopmmo.info**)
 - ***password***: admin (Mật khẩu đăng nhập website **shopmmo.info**)
 - ***id***: 19 (ID sản phẩm mà bạn đã get được ở API trên)

> Website của bạn cần phải sử dụng SSL

**Example Request:** 
```bash
curl --location -g --request GET '{domain}/api/InfoResource.php?username=admin&password=admin&id=19'
```
<!-- TABLE OF CONTENTS -->
<details>
  <summary>Example Response - Header</summary>
  

```JSON
{
  "status": "success",
  "msg": "Lấy thông tin sản phẩm thành công",
  "data": [
    {
      "id": "19",
      "name": "Clone very phone",
      "price": "100",
      "amount": 53,
      "country": "vn",
      "description": ""
    }
  ]
}

```
</details>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Example Response - Body</summary>
  

```pmresponseheaders
Date: Thu, 19 Aug 2022 23:21:59 GMT
Server: Apache/2.4.48 (Unix) OpenSSL/1.1.1k PHP/7.3.29 mod_perl/2.0.11 Perl/v5.32.1
X-Powered-By: PHP/7.3.29
Expires: Thu, 19 Nov 1981 08:52:00 GMT
Cache-Control: no-store, no-cache, must-revalidate
Pragma: no-cache
Content-Length: 197
Keep-Alive: timeout=5, max=100
Connection: Keep-Alive
Content-Type: text/html; charset=UTF-8
```

</details>


## 💸GET - Xem Số Dư

*{domain}/api/**GetBalance**.php?**username**=admin&**password**=admin*

 - ***username*** :admin (Tài khoản đăng nhập website **shopmmo.info**)
 - ***password***: admin (Mật khẩu đăng nhập website **shopmmo.info**)

> Website của bạn cần phải sử dụng SSL

**Example Request:** 
```bash
curl --location -g --request GET '{domain}/api/InfoResource.php?username=admin&password=admin&id=19'
```
<!-- TABLE OF CONTENTS -->
<details>
  <summary>Example Response - Header</summary>
  

```JSON
199.994.860đ
```
</details>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Example Response - Body</summary>
  

```pmresponseheaders
Date: Thu, 19 Aug 2022 23:21:59 GMT
Server: Apache/2.4.48 (Unix) OpenSSL/1.1.1k PHP/7.3.29 mod_perl/2.0.11 Perl/v5.32.1
X-Powered-By: PHP/7.3.29
Expires: Thu, 19 Nov 1981 08:52:00 GMT
Cache-Control: no-store, no-cache, must-revalidate
Pragma: no-cache
Content-Length: 197
Keep-Alive: timeout=5, max=100
Connection: Keep-Alive
Content-Type: text/html; charset=UTF-8
```
</details>
