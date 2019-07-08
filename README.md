## Step 1
Getting Bluetooth Lock MAC Address through Mobile Phone
```
POST /oklock/lock/queryDevice HTTP/1.1
User-Agent: nokelockTool/1.4.5(Android 9 ; Xiaomi/MI 9)
clientType: Android
token: 6f93d29a44684e809d7104b4837968a0
language: CN
appVersion: 1.4.5
Content-Type: application/json;charset=UTF-8
Content-Length: 27
Host: api.oklock.com.cn
Connection: close
Accept-Encoding: gzip, deflate

{"mac":"18:62:E4:46:6C:F7"}
```

```
HTTP/1.1 200 
Server: nginx/1.13.3
Date: Mon, 08 Jul 2019 05:07:28 GMT
Content-Type: application/json
Content-Length: 356
Connection: close

{"result":{"alarm":0,"barcode":"GFYY00016519","chipType":"1","createAt":"2019-03-01 08:45:07.0","deviceId":"","electricity":"98","firmwareVersion":"2.3","gsmVersion":"","id":64731,"isLock":0,"lockKey":"89,89,78,74,90,43,43,70,5,88,13,51,85,54,98,43","lockPwd":"000000","mac":"18:62:E4:46:6C:F7","name":"ffg","radioName":"BlueFPL","type":0},"status":"2000"}
```

## Step 2

Getting administrator ID through barcode

```
POST /oklock/lock/getDeviceInfo HTTP/1.1
User-Agent: nokelockTool/1.4.5(Android 9 ; Xiaomi/MI 9)
clientType: Android
token: 6f93d29a44684e809d7104b4837968a0
language: CN
appVersion: 1.4.5
Content-Type: application/json;charset=UTF-8
Content-Length: 63
Host: api.oklock.com.cn
Connection: close
Accept-Encoding: gzip, deflate

{"barcode":"https://app.oklok.com.cn/app.html?id=GFYY00022393"}
```
```
POST /oklock/lock/getDeviceInfo HTTP/1.1
User-Agent: nokelockTool/1.4.5(Android 9 ; Xiaomi/MI 9)
clientType: Android
token: 6f93d29a44684e809d7104b4837968a0
language: CN
appVersion: 1.4.5
Content-Type: application/json;charset=UTF-8
Content-Length: 63
Host: api.oklock.com.cn
Connection: close
Accept-Encoding: gzip, deflate

{"barcode":"https://app.oklok.com.cn/app.html?id=GFYY00016519"}
```

## Step 3

Authorize users
```
POST /oklock/lock/authLock HTTP/1.1
User-Agent: nokelockTool/1.4.5(Android 9 ; Xiaomi/MI 9)
clientType: Android
token: 6f93d29a44684e809d7104b4837968a0
language: CN
appVersion: 1.4.5
Content-Type: application/json;charset=UTF-8
Content-Length: 45
Host: api.oklock.com.cn
Connection: close
Accept-Encoding: gzip, deflate

{"lockId":78789,"pId":"62415","userId":58740}
```