---
description: Microsoft 增強型密碼編譯提供者支援下列演算法。
ms.assetid: d58bcd99-c54b-4fda-9fe1-e10a66707d81
title: 增強型提供者演算法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a8be464a57a482fa74fef07de097508508d7e965a5c20817ccbd884bb169e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766099"
---
# <a name="enhanced-provider-algorithms"></a>增強型提供者演算法

[Microsoft 增強型密碼編譯提供者](microsoft-enhanced-cryptographic-provider.md)支援下列演算法。



| 演算法識別碼       | 描述                                                                                                                                                     | 註解                                                                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ 3des         | 三重 DES。                                                                                                                                                     | 金鑰長度：168位。預設模式：加密區塊鏈。<br/> 區塊大小：64位。<br/> 不允許 salt。<br/>                           |
| CALG \_ 3des \_ 112    | 兩個金鑰的 [*三重 DES*](../secgloss/t-gly.md) 加密。                                                            | 金鑰長度：112位。預設模式：加密區塊鏈。<br/> 區塊大小：64位。<br/> 不允許 salt。<br/>                           |
| CALG \_ DES          | DES 加密。                                                                                                                                                 | 金鑰長度：56位。預設模式：加密區塊鏈。<br/> 區塊大小：64位。<br/> 不允許 salt。<br/>                            |
| CALG \_ HMAC         | MAC 索引鍵雜湊演算法。                                                                                                                                       | HMAC 計算。                                                                                                                                          |
| CALG \_ MAC          | [*訊息驗證碼*](../secgloss/m-gly.md) (MAC) 金鑰雜湊演算法。 | 封鎖加密 MAC。                                                                                                                                          |
| CALG \_ MD2          | MD2 雜湊演算法。                                                                                                                                          | 如需詳細資訊，請參閱 [*MD2 演算法*](../secgloss/m-gly.md)。                                       |
| CALG \_ MD5          | MD5 雜湊演算法。                                                                                                                                          | 如需詳細資訊，請參閱 [*MD5 演算法*](../secgloss/m-gly.md)。                                       |
| CALG \_ RC2          | RC2 區塊加密演算法。                                                                                                                                 | 金鑰長度：128位。預設模式：加密區塊鏈。<br/> 區塊大小：64位。<br/> Salt 長度：可設定。<br/>                   |
| CALG \_ RC4          | RC4 資料流程加密演算法。                                                                                                                                | 金鑰長度：128位。Salt 長度：可設定。<br/>                                                                                                   |
| CALG \_ RSA \_ KEYX    | RSA 公開金鑰交換演算法。                                                                                                                              | 金鑰長度：可以設定為8位遞增的384位到16384位。 預設金鑰長度：1024位。<br/>                                            |
| CALG \_ RSA \_ SIGN    | RSA 公開金鑰簽章演算法。                                                                                                                             | 金鑰長度：可以設定為8位遞增的384位到16384位。 預設金鑰長度：1024位。<br/> 簽章符合 PKCS \# 6。<br/> |
| CALG \_ SHA          | SHA 雜湊演算法。                                                                                                                                          | 如需詳細資訊，請參閱 [*安全雜湊演算法*](../secgloss/s-gly.md)。               |
| CALG \_ SHA1         | 與 CALG \_ SHA 相同。                                                                                                                                              | 如需詳細資訊，請參閱 [*安全雜湊演算法*](../secgloss/s-gly.md)。               |
| CALG \_ SSL3 \_ SHAMD5 | SSL3 用戶端驗證演算法。                                                                                                                           | 如需詳細資訊，請參閱 [建立 CALG \_ SSL3 \_ SHAMD5 Hash](creating-a-calg-ssl3-shamd5-hash.md)。                                                      |



 

 

 
