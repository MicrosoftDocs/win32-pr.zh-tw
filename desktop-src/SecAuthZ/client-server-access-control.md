---
description: 伺服器應用程式會為用戶端提供服務。
ms.assetid: 8301ed4f-9458-410b-af19-4f055656005a
title: 用戶端/伺服器存取控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c943d9d1e1f1cc5dcc405f49ab200aa30618f7eefb86c7f26342f005f23249fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782723"
---
# <a name="clientserver-access-control"></a>用戶端/伺服器存取控制

伺服器應用程式會為用戶端提供服務。 例如，伺服器可以代表用戶端執行下列服務：

-   從私用資料庫儲存和取出資訊
-   存取網路資源
-   在伺服器電腦上的用戶端 [*安全性內容*](/windows/desktop/SecGloss/s-gly)中啟動 [*處理*](/windows/desktop/SecGloss/p-gly)程式

受保護的伺服器可控制其服務的存取權。 Windows 提供可讓伺服器執行下列動作的安全性支援：

-   模擬用戶端的 [*安全性內容*](/windows/desktop/SecGloss/s-gly)，這會導致系統對用戶端的 [*存取權杖*](/windows/desktop/SecGloss/a-gly)執行大部分的存取和 [*許可權*](/windows/desktop/SecGloss/p-gly)檢查，而不是伺服器的
-   將用戶端登入伺服器的電腦
-   使用用戶端的安全性內容連線到網路資源
-   建立 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 以保護私用物件
-   判斷安全描述項是否允許存取用戶端
-   判斷是否已在用戶端的權杖中啟用一組許可權
-   在安全性事件記錄檔中產生審核訊息，以記錄用戶端存取物件或使用許可權的嘗試

 

 
