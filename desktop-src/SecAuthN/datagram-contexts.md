---
description: 資料包的語義或不需連線的內容，與連接導向內容的內容稍有不同。
ms.assetid: f312796c-cbe6-4be9-9886-52fdb34ced6b
title: 資料包內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d233a0ba397e67a13b1c25588cf81b6f12c31d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113812"
---
# <a name="datagram-contexts"></a>資料包內容

[*資料包*](/windows/desktop/SecGloss/d-gly)的語義或不需連線的內容，與連接導向內容的內容稍有不同。 在資料包的無連接 [*內容*](/windows/desktop/SecGloss/c-gly)中，伺服器無法判斷用戶端何時關閉或終止連接。 換句話說，在連接導向的內容中，不會將任何終止通知從傳輸應用程式傳遞到伺服器。

若要使用資料包內容，用戶端會 \_ 在對 \_ [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 函式的呼叫中，設定 ISC 需求資料包旗標。

> [!IMPORTANT]
> [Microsoft Kerberos](microsoft-kerberos.md)套件不支援使用者到使用者模式中的資料包內容。

 

若要更妥善地支援某些模型（特別是 DCE 樣式 RPC），當用戶端使用資料包內容時，會套用下列規則：

-   在第一次呼叫 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)時，[*安全性套件*](/windows/desktop/SecGloss/s-gly)不會產生驗證 [*BLOB*](/windows/desktop/SecGloss/b-gly) (二進位大型物件) 。 不過，用戶端可以在呼叫 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 函式時使用傳回的安全性內容，以產生訊息的簽章。
-   安全性封裝必須允許重新建立內容多次，以允許伺服器在不另行通知的情況下卸載連接。 這表示 [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) 和 [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) 函式中使用的任何金鑰都可以重設為一致的 [*狀態*](/windows/desktop/SecGloss/s-gly)。
-   安全性封裝可讓呼叫者指定順序資訊，並在接收者端提供該順序資訊。 這是封裝所維護的任何順序資訊以外的資訊。

安全性套件會設定 SECPKG \_ 旗 \_ 標資料包旗標，表示它支援資料包語義。

 

 
