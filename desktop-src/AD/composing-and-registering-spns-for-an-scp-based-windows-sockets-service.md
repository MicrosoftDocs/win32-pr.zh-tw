---
title: 針對 SCP 型 Windows 通訊端服務撰寫和註冊 Spn
description: 下列程式碼範例示範如何撰寫和註冊服務的 Spn。 請在呼叫 CreateService 並建立服務的服務連接點 (SCP) 之後，從您的服務安裝程式呼叫此程式碼。
ms.assetid: 3957af10-974a-415f-b8fb-d9b52ac5a82d
ms.tgt_platform: multiple
keywords:
- 服務主體名稱 AD、撰寫及註冊以 SCP 為基礎之 Windows sockets 服務的 Spn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d754d51c0ad34b1623bdc84fc8178b04d33515ed
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681687"
---
# <a name="composing-and-registering-spns-for-scp-based-windows-sockets-service"></a>針對 SCP 型 Windows 通訊端服務撰寫和註冊 Spn

下列程式碼範例示範如何撰寫和註冊服務的 Spn。 請在呼叫 [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) 並建立服務的服務連接點 (SCP) 之後，從您的服務安裝程式呼叫此程式碼。

下列程式碼範例會呼叫撰寫和註冊 SPN 的 **SpnCompose** 和 **SpnRegister** 範例函式。 如需詳細資訊和 **SpnCompose** 原始程式碼，請參閱 [使用 SCP 撰寫服務的 spn](composing-the-spns-for-a-service-with-an-scp.md)。 如需詳細資訊和 **SpnRegister** 原始碼，請參閱 [註冊服務的 spn](registering-the-spns-for-a-service.md)。

此範例會使用服務類別名稱及其 SCP 的分辨名稱來建立其服務主體名稱。 如需詳細資訊和示範用戶端如何系結至服務 SCP 以取得這些名稱字串的程式碼範例，請參閱 [用戶端如何尋找和使用服務連接點](how-clients-find-and-use-a-service-connection-point.md)。 請注意，用來撰寫 SPN 的程式碼會根據服務的類型和用來發行服務的機制而有所不同。

服務會將其 SPN 儲存在目錄的服務帳戶物件的 **servicePrincipalName** 屬性中，以註冊其 SPN。 如果服務是在 LocalSystem 帳戶下執行，而不是在服務帳戶下執行，則會在目錄中的本機電腦帳戶物件下註冊其 SPN。


```C++
TCHAR szDNofSCP[MAX_PATH]; // DN of SCP. Initialize by querying SCP.
TCHAR szServiceClass[]=TEXT("ADSockAuth");
LPCTSTR szServiceAccountDN;   // DN of a service logon account. 
 
DWORD dwStatus;
TCHAR **pspn = NULL;
ULONG ulSpn = 1;
 
// Compose the SPNs.
dwStatus = SpnCompose(
        &pspn,              // Receives pointer to the SPN array.
        &ulSpn,             // Receives number of SPNs returned.
        szDNofSCP,          // Input: DN of the SCP.
        szServiceClass);    // Input: the service class string.
 
// Register the SPNs
if (dwStatus == NO_ERROR) 
    dwStatus = SpnRegister(
       szServiceAccountDN,  // Logon account to register SPNs on
       pspn,                // Array of SPNs
       ulSpn,               // Number of SPNs in array
       DS_SPN_ADD_SPN_OP);  // Add SPNs to the account
 
// Free the array of SPNs returned by SpnCompose.
DsFreeSpnArray(ulSpn, pspn); 
```



卸載您的服務時，您可以使用類似的程式碼取消註冊 Spn。 指定 **ds \_ spn \_ 刪除 \_ spn \_** 操作操作，而不是 **ds \_ spn \_ 新增 \_ spn \_** 作業。

 

 