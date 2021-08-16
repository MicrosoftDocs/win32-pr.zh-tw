---
description: 在票證授與票證 (TGT) 和用戶端已建立工作階段金鑰之後，用戶端就可以要求個別的工作階段金鑰和服務的票證。
ms.assetid: b4f63642-9282-4e11-b40c-eec406b2dd2b
title: 票證授權服務交換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a691235b3e7f0faed68f38f0663c7792e381666f441399397f7e653bbb550080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786566"
---
# <a name="ticket-granting-service-exchange"></a>票證授權服務交換

在票證授與票證 (TGT) 和用戶端已建立 [*工作階段金鑰*](../secgloss/s-gly.md) 之後，用戶端就可以要求個別的工作階段金鑰和服務的票證。

**為另一個服務要求票證**

1.  使用者工作站上的 Kerberos 用戶端會藉由傳送至 [*金鑰發佈中心*](../secgloss/k-gly.md) (KDC) 的訊息來要求服務的 [*認證*](../secgloss/c-gly.md)，該訊息類型為 KRB \_ TGS \_ 要求 (Kerberos Ticket-Granting 服務要求) 。 此訊息包含用戶端要求認證的服務身分識別、以使用者的新登入 [*工作階段金鑰*](../secgloss/s-gly.md)加密的驗證器訊息，以及從 [驗證服務](authentication-service-exchange.md)取得的 TGT Exchange。
2.  當 KDC 收到 KRB 的 TGS 要求時 \_ \_ ，kdc 會使用其秘密金鑰來解密 TGT，並解壓縮使用者的登入工作階段金鑰。
3.  KDC 會使用登入 [*工作階段金鑰*](../secgloss/s-gly.md) 來解密使用者的驗證器訊息，並進行評估。 如果驗證器通過測試，KDC 會從 TGT 解壓縮使用者的授權資料，並 invents 工作階段金鑰，讓使用者與要求的伺服器共用。
4.  KDC 會使用使用者的登入工作階段金鑰，加密一份服務工作階段金鑰。
5.  KDC 會將服務工作階段金鑰的另一份複本內嵌在票證中，連同使用者的授權資料，並使用伺服器的 [*主要金鑰*](../secgloss/m-gly.md)來加密票證。
6.  KDC 會以 KRB \_ TGS \_ 代表 (Kerberos Ticket-Granting 服務回復) 的訊息來回複，將這些認證傳送回用戶端。
7.  當用戶端收到回復時，它會使用使用者的登入工作階段金鑰來解密服務工作階段金鑰，並將服務工作階段金鑰儲存在其票證快取中。
8.  用戶端會將票證解壓縮至伺服器，並將其儲存在其票證快取中。

 

 
