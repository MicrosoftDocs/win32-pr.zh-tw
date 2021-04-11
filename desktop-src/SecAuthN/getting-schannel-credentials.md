---
description: 下列範例示範一般用戶端如何取得安全通道認證。
ms.assetid: 8f912af8-fd64-467a-b154-28c60cb14929
title: 取得 Schannel 認證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2594b808387943cd2fc645a459dfbcd66ebc54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319343"
---
# <a name="getting-schannel-credentials"></a><span data-ttu-id="60536-103">取得 Schannel 認證</span><span class="sxs-lookup"><span data-stu-id="60536-103">Getting Schannel Credentials</span></span>

<span data-ttu-id="60536-104">下列範例示範一般用戶端如何取得安全通道認證。</span><span class="sxs-lookup"><span data-stu-id="60536-104">The following example demonstrates how a typical client would obtain Schannel credentials.</span></span> <span data-ttu-id="60536-105">此範例會遵循使用系統預設值進行加密和加密強度的建議作法。</span><span class="sxs-lookup"><span data-stu-id="60536-105">The example follows the recommended practice of using the system defaults for ciphers and cipher strengths.</span></span> <span data-ttu-id="60536-106">這可讓安全通道套件使用最強的可能演算法來保護通道。</span><span class="sxs-lookup"><span data-stu-id="60536-106">This allows the Schannel package to use the strongest possible algorithms to secure the channel.</span></span>


```C++
#include <windows.h>
#include <ntsecapi.h>
#include <stdio.h>
#include <sspi.h>
#include <schnlsp.h>

void getSchannelClientHandle(PCredHandle ppClientCred)
{
  SECURITY_STATUS SecStatus;
  TimeStamp Lifetime;
  CredHandle hCred;
  SCHANNEL_CRED credData;

  ZeroMemory(&credData, sizeof(credData));
  credData.dwVersion = SCHANNEL_CRED_VERSION;

  //-------------------------------------------------------
  // Specify the TLS V1.0 (client-side) security protocol.
  credData.grbitEnabledProtocols = SP_PROT_TLS1_CLIENT; 
    
  SecStatus = AcquireCredentialsHandle (
       NULL,                  // default principal
       UNISP_NAME,            // name of the SSP
       SECPKG_CRED_OUTBOUND,  // client will use the credentials
       NULL,                  // use the current LOGON id
       &credData,             // protocol-specific data
       NULL,                  // default
       NULL,                  // default
       &hCred,                // receives the credential handle
       &Lifetime              // receives the credential time limit
  );
  printf("Client credentials status: 0x%x\n", SecStatus);
  // Return the handle to the caller.
  if(ppClientCred != NULL)
      *ppClientCred = hCred;

  return;
  //-------------------------------------------------------
  // When you have finished with this handle,
  // free the handle by calling the 
  // FreeCredentialsHandle function.
}
```



<span data-ttu-id="60536-107">用戶端與伺服器端認證要求之間的主要差異在於，伺服器必須使用憑證 [**\_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) 結構來提供憑證，如下所示：</span><span class="sxs-lookup"><span data-stu-id="60536-107">The primary difference between the client-side and server-side request for credentials is that the server must provide a certificate using a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structure as follows:</span></span>


```C++
  PCCERT_CONTEXT serverCert; // server-side certificate
  //-------------------------------------------------------
  // Get the server certificate. 

  if (! (serverCert = getServerCertificate())) return;

  // getServerCertificate is a placeholder function.
  credData.paCred = &serverCert;
```



<span data-ttu-id="60536-108">範例函式 *getServerCertificate* 是此應用程式特定活動的預留位置函式。</span><span class="sxs-lookup"><span data-stu-id="60536-108">The example function *getServerCertificate* is a placeholder function for this application-specific activity.</span></span> <span data-ttu-id="60536-109">如需 *getServerCertificate* 函式的範例執行，請參閱 [取得憑證](getting-a-certificate-for-schannel.md)。</span><span class="sxs-lookup"><span data-stu-id="60536-109">For an example implementation of the *getServerCertificate* function, see [Getting a Certificate](getting-a-certificate-for-schannel.md).</span></span>

> [!Note]  
> <span data-ttu-id="60536-110">要求伺服器所使用的認證時，請將 [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)函式的第三個 (*fCredentialUse*) 參數從 SECPKG 認證 \_ 輸出變更為 SECPKG 的認證 \_ \_ \_ 輸入。</span><span class="sxs-lookup"><span data-stu-id="60536-110">When requesting credentials to be used by the server, change the third (*fCredentialUse*) parameter of the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function from SECPKG\_CRED\_OUTBOUND to SECPKG\_CRED\_INBOUND.</span></span>

 

 

 
