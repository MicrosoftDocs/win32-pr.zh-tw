---
description: 金鑰發佈中心 (KDC) 會實作為網域服務。 它會使用 Active Directory 作為其帳戶資料庫和通用類別目錄，以將參考導向其他網域中的 Kdc。
ms.assetid: f2a7c87c-9be7-4fd8-8ecd-4edf1f2336ef
title: 金鑰發佈中心
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eef410ccb9289d30507708dc35000e1c15d5d4c9998b28b33a2e51d1a15b1e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013338"
---
# <a name="key-distribution-center"></a>金鑰發佈中心

金鑰發佈中心 (KDC) 會實作為網域服務。 它會使用 Active Directory 作為其帳戶資料庫和通用類別目錄，以將參考導向其他網域中的 Kdc。

如同 [*Kerberos 通訊協定*](../secgloss/k-gly.md)的其他執行方式，KDC 是提供兩項服務的單一進程：

-   驗證服務 (為) 

    這項服務會發出票證授與票證 (Tgt) ，以連接到其本身網域或任何受信任網域中的票證授與服務。 用戶端必須先從用戶端帳戶網域中的驗證服務要求 TGT，用戶端才能要求票證給另一部電腦。 驗證服務會傳回目的電腦網域中票證授與服務的 TGT。 TGT 可以重複使用到到期為止，但第一次存取任何網域的票證授與服務時，一律需要前往用戶端帳戶網域中的驗證服務。

-   Ticket-Granting 服務 (TGS) 

    這項服務會發出票證，以連接到其本身網域中的電腦。 當用戶端想要存取電腦時，會在目的電腦的網域中，與票證授與服務聯繫，出示 TGT，然後要求該電腦的票證。 票證可以重複使用到到期為止，但第一次存取任何電腦一律需要前往目的電腦帳戶網域中的票證授與服務。

網域的 KDC 位於網域控制站上，如同網域的 Active Directory。 網域控制站的 [*本地安全性授權*](../secgloss/l-gly.md) 單位會自動啟動這兩個服務 (lsa) 並在 lsa 的進程中執行。 這兩個服務都無法停止。 如果網路用戶端無法使用 KDC，則 Active Directory 也無法使用，而且網域控制站不再控制網域。 系統可讓每個網域擁有數個網域控制站（所有對等），以確保這些網域服務和其他網域服務的可用性。 任何網域控制站都可以接受向網域的 KDC 定址的驗證要求和票證授與要求。

在任何網域中，KDC 所使用的 [*安全性主體*](../secgloss/s-gly.md) 名稱是 "krbtgt"，如 [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt)所指定。 建立新網域時，會自動建立此安全性主體的帳戶。 無法刪除帳戶，也無法變更名稱。 系統會在建立網域期間，自動將隨機密碼值指派給帳戶。 KDC 帳戶的密碼用來衍生密碼編譯金鑰，以加密和解密其所發出的 Tgt。 網域信任帳戶的密碼用來衍生範圍內的金鑰，以加密參考票證。

網域內的所有 KDC 實例都使用網域帳戶做為安全性主體 "krbtgt"。 用戶端會將服務的主體名稱 "krbtgt" 和網域的名稱包含在內，以將訊息定址到網域的 KDC。 這兩項資訊也會用於票證，以識別發行授權單位。 如需名稱表單和定址慣例的詳細資訊，請參閱 [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt)。

 

 
