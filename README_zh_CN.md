# XXTEA 加密算法的 Java 实现

## 简介

XXTEA 是一个快速安全的加密算法。本项目是 XXTEA 加密算法的 Java 实现。

它不同于原始的 XXTEA 加密算法。它是针对 byte[] 类型数据进行加密的，而不是针对 32 位整型数组。同样，密钥也是 byte[]。

为了用户使用方便，除了提供对 byte[] 进行加解密的 API 之外，还提供了一些辅助方法来处理字符串和 Base64 编码。

## 使用

```java
package org.xxtea.test;

import org.xxtea.XXTEA;

public class Main {
    public static void main(String[] args) {
        String str = "Hello World! 你好，中国！";
        String key = "1234567890";
        byte[] encrypt_data = XXTEA.encrypt(str, key);
        String decrypt_data = XXTEA.decryptToString(encrypt_data, key);
        assert(str.equals(decrypt_data));
    }
}
```
