---
description: 用戶端和伺服器都必須先取得認證，才能建立訊息交換的安全性內容。
ms.assetid: a72404b8-1ec9-4f58-b3a6-09811070ea29
title: 取得預設摘要認證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12e870d6bad1c3b4ef9e889a91444e98159bc758
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192629"
---
# <a name="obtaining-default-digest-credentials"></a><span data-ttu-id="d5ce8-103">取得預設摘要認證</span><span class="sxs-lookup"><span data-stu-id="d5ce8-103">Obtaining Default Digest Credentials</span></span>

<span data-ttu-id="d5ce8-104">用戶端和伺服器都必須先取得 [*認證*](../secgloss/c-gly.md) ，才能建立訊息交換的 [*安全性內容*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="d5ce8-104">Both clients and servers must obtain [*credentials*](../secgloss/c-gly.md) before they can establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="d5ce8-105">[**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)函式的預設行為是提供與目前登入 [*會話*](../secgloss/s-gly.md)相關聯之安全性主體的認證。</span><span class="sxs-lookup"><span data-stu-id="d5ce8-105">The default behavior of the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function is to provide credentials for the security principal associated with the current logon [*session*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="d5ce8-106">下列範例示範用來取得預設認證的伺服器端呼叫。</span><span class="sxs-lookup"><span data-stu-id="d5ce8-106">The following example demonstrates a server-side call to obtain the default credentials.</span></span>


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



<span data-ttu-id="d5ce8-107">預設認證的用戶端呼叫完全相同，不同之處在于第三個參數必須指定 SECPKG 的 \_ \_ 認證輸出，以指出用戶端將會使用函式所傳回的認證控制碼。</span><span class="sxs-lookup"><span data-stu-id="d5ce8-107">The client-side call for default credentials is identical, except the third parameter must specify SECPKG\_CRED\_OUTBOUND to indicate that the client will use the credentials handle returned by the function.</span></span>

<span data-ttu-id="d5ce8-108">如需示範如何取得已登入使用者以外的安全性主體認證的範例，請參閱 [取得替代認證](obtaining-alternate-digest-credentials.md)。</span><span class="sxs-lookup"><span data-stu-id="d5ce8-108">For an example that demonstrates obtaining credentials for a security principal other than the logged on user, see [Obtaining Alternate Credentials](obtaining-alternate-digest-credentials.md).</span></span>

 

 
