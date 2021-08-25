---
description: Microsoft 基礎密碼編譯提供者支援下列演算法。
ms.assetid: 767d5192-6e8f-488a-b954-29d56488ccbb
title: 基底提供者演算法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6b6f3af49529ad46e70dd154c06febf433f5fb483861f7c0b2530af7ebbef2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879748"
---
# <a name="base-provider-algorithms"></a>基底提供者演算法

Microsoft 基礎密碼編譯提供者支援下列演算法。



| 演算法識別碼                  | 描述                                                                                                                                                               | 註解                                                                                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CALG \_ MD2<br/>          | MD2 雜湊演算法<br/>                                                                                                                                          | 如需詳細資訊，請參閱 [*MD2 演算法*](../secgloss/m-gly.md)。<br/>                                         |
| CALG \_ MD5<br/>          | MD5 雜湊演算法<br/>                                                                                                                                          | 如需詳細資訊，請參閱 [*MD5 演算法*](../secgloss/m-gly.md)。<br/>                                         |
| CALG \_ SHA<br/>          | SHA 雜湊演算法<br/>                                                                                                                                          | 如需詳細資訊，請參閱 [*安全雜湊演算法*](../secgloss/s-gly.md)。<br/>                 |
| CALG \_ SHA1<br/>         | 與 CALG \_ SHA 相同<br/>                                                                                                                                              | 如需詳細資訊，請參閱 [*安全雜湊演算法*](../secgloss/s-gly.md)。<br/>                 |
| CALG \_ MAC<br/>          | [*訊息驗證碼*](../secgloss/m-gly.md) (MAC) 金鑰雜湊演算法<br/> | 封鎖加密 MAC。<br/>                                                                                                                                            |
| CALG \_ HMAC<br/>         | MAC 金鑰雜湊演算法<br/>                                                                                                                                       | HMAC 計算。<br/>                                                                                                                                            |
| CALG \_ SSL3 \_ SHAMD5<br/> | SLL3 用戶端驗證演算法<br/>                                                                                                                           | 如需詳細資訊，請參閱 [建立 CALG \_ SSL3 \_ SHAMD5 Hash](creating-a-calg-ssl3-shamd5-hash.md)。<br/>                                                        |
| CALG \_ RSA \_ SIGN<br/>    | RSA 公開金鑰簽章演算法<br/>                                                                                                                             | 金鑰長度：可以在8位增量中從384位設定為16384位。<br/> 預設金鑰長度：512位。<br/> 簽章符合 PKCS \# 6。<br/> |
| CALG \_ RSA \_ KEYX<br/>    | RSA 公開金鑰交換演算法<br/>                                                                                                                              | 金鑰長度：可以在8位增量中從384位設定為1024位。<br/> 預設金鑰長度：512位。<br/>                                              |
| CALG \_ RC2<br/>          | RC2 區塊加密演算法<br/>                                                                                                                                 | 金鑰長度：40位。<br/> 預設模式：加密區塊鏈。<br/> 區塊大小：64位。<br/> Salt 長度：88位。<br/>                        |
| CALG \_ RC4<br/>          | RC4 串流加密演算法<br/>                                                                                                                                | 金鑰長度：40位。<br/> Salt 長度：88位。<br/>                                                                                                        |
| CALG \_ DES<br/>          | DES 加密<br/>                                                                                                                                                 | 如需詳細資訊，請參閱 [*資料加密標準*](../secgloss/d-gly.md) (DES) 。<br/>  |



 

 

 
