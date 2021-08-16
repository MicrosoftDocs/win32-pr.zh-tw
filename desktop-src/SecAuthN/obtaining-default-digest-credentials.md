---
description: 用戶端和伺服器都必須先取得認證，才能建立訊息交換的安全性內容。
ms.assetid: a72404b8-1ec9-4f58-b3a6-09811070ea29
title: 取得預設摘要認證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d5a0bb39f59680f2b5232dae1e6cc5c83673cf31c7cc3e0aa1325d5641e161
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786586"
---
# <a name="obtaining-default-digest-credentials"></a>取得預設摘要認證

用戶端和伺服器都必須先取得 [*認證*](../secgloss/c-gly.md) ，才能建立訊息交換的 [*安全性內容*](../secgloss/s-gly.md) 。 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)函式的預設行為是提供與目前登入 [*會話*](../secgloss/s-gly.md)相關聯之安全性主體的認證。

下列範例示範用來取得預設認證的伺服器端呼叫。


```C++
SECURITY_STATUS SecStatus; 
TimeStamp tsLifetime; 
CredHandle hCred;
SecStatus = AcquireCredentialsHandle (
       NULL,                  // Default principal.
       WDIGEST_SP_NAME,       // Microsoft Digest SSP. 
       SECPKG_CRED_INBOUND,   // Server will use the credentials.
       NULL,                  // Use the current LOGON id.
       NULL,                  // Default credentials.
       NULL,                  // Not used with Digest SSP.
       NULL,                  // Not used with Digest SSP.
       &hCred,                // Receives the credential handle.
       &tsLifetime            // Receives the credential time limit.
);
```



預設認證的用戶端呼叫完全相同，不同之處在于第三個參數必須指定 SECPKG 的 \_ \_ 認證輸出，以指出用戶端將會使用函式所傳回的認證控制碼。

如需示範如何取得已登入使用者以外的安全性主體認證的範例，請參閱 [取得替代認證](obtaining-alternate-digest-credentials.md)。

 

 
