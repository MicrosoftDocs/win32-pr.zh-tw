---
description: 當用戶端收到摘要挑戰以回應資源的要求時，用戶端必須傳送摘要挑戰回應給伺服器。
ms.assetid: a9a30255-a78a-41aa-9dfd-340902f4c550
title: 摘要挑戰回應的內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7168a7e6a468ecc7d573ef0bd853ec6db255b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193283"
---
# <a name="contents-of-a-digest-challenge-response"></a>摘要挑戰回應的內容

當用戶端收到摘要挑戰以回應資源的要求時，用戶端必須傳送摘要挑戰回應給伺服器。 用戶端必須再次傳送要求，並提供包含挑戰回應的授權標頭。 下表說明構成摘要挑戰回應的指示詞。



| 指示詞          | Description                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| username           | 要求資源之 [*安全性主體*](/windows/desktop/SecGloss/s-gly) 的帳戶名稱。                                                                  |
| Realm              | 包含使用者名稱所指出之帳戶的功能變數名稱。                                                                                                                                                    |
| nonce              | 摘要挑戰中所收到的 nonce。                                                                                                                                                                                |
| uri                | 要求的資源 (URI) 的通用資源識別碼。                                                                                                                                                         |
| qop                | [保護的品質](quality-of-protection.md)。                                                                                                                                                                    |
| 數控                 | Nonce 計數。 用戶端使用 nonce 傳送挑戰回應的次數。 如需詳細資訊，請參閱 nonce 指示詞。                                                                              |
| cnonce             | 用戶端為每個挑戰回應所產生的唯一編碼值。                                                                                                                                                |
| 回應           | 根據摘要存取規格 ([RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)) 所計算的值。 精確的回應決定性證明使用者的密碼在用戶端上是已知的。 |
| 演算法          | 摘要挑戰中所收到的演算法。                                                                                                                                                                            |
| 不透明             | 摘要挑戰中收到的不透明值。                                                                                                                                                                         |
| 僅 (SASL) cipher | 摘要挑戰中所收到的其中一個加密值。 如需加密的詳細資訊，請參閱 [保護品質和密碼](quality-of-protection-and-ciphers.md)。                                                             |



 

Microsoft Digest 支援下列使用者名稱/領域格式：

-   使用者名稱領域
-   AccountName 網域 (一般) 
-   UPN "" (空白) 
-   NetBIOS "" (空白) 

雖然支援大寫字元，但為了達到符合伺服器預先計算之摘要雜湊值的最佳效能，建議使用小寫字元。

使用預先計算的雜湊是一項新功能，可讓系統操作員略過在網域控制站上使用可還原的加密密碼。 當使用者的密碼變更時，會為使用者形成預先計算的雜湊。

Microsoft Digest 會產生用戶端應用程式的摘要挑戰回應字串。 如需詳細資訊，請參閱 [產生摘要挑戰回應](generating-the-digest-challenge-response.md)。

 

 
