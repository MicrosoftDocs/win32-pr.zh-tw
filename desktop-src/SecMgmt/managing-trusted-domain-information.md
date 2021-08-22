---
description: LSA 原則提供數個函式，可讓您用來建立、列舉及刪除信任的網域，以及設定和取得受信任的網域資訊。
ms.assetid: 0c7534d7-3372-49c4-992c-9b519279982d
title: 管理受信任的網域資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a945705efaedf56920ee2170deeab9da0d01802259a57aca5cda2fac9d531aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894088"
---
# <a name="managing-trusted-domain-information"></a>管理受信任的網域資訊

LSA 原則提供數個函式，可讓您用來建立、列舉及刪除信任的網域，以及設定和取得受信任的網域資訊。

在您可以管理受信任的網域資訊之前，您的應用程式必須取得 [**原則**](policy-object.md) 物件的控制碼，如 [開啟原則物件控制碼](opening-a-policy-object-handle.md)中所述。

您可以藉由呼叫 [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)來列舉受信任的網域。

若要取得受信任網域的相關資訊，請呼叫 [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo) 或 [**>lsaquerytrusteddomaininfobyname**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname)。 這兩個函數都會傳回相同的資訊。不過， **LsaQueryTrustedDomainInfo** 會依 SID 識別受信任的網域，而 **>lsaquerytrusteddomaininfobyname** 會依名稱識別受信任的網域。

若要設定受信任網域的資訊，請呼叫 [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation) 或 [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname)。 如同查詢函式， **LsaSetTrustedDomainInformation** 會依 SID 識別受信任的網域，而 **LsaSetTrustedDomainInfoByName** 會依名稱識別受信任的網域。

您的應用程式可以藉由呼叫 [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain)來撤銷受信任網域的信任關係。

下列範例會列舉本機系統的受信任網域。


```C++
#include <windows.h>

void EnumerateTrusts(LSA_HANDLE PolicyHandle)
{
  LSA_ENUMERATION_HANDLE hEnum=0; 
  PLSA_TRUST_INFORMATION TrustInfo = NULL;
  ULONG ulReturned = 0;               
  NTSTATUS Status = 0;
  ULONG i;
  WCHAR StringBuffer[256];

  // Enumerate the trusted domains until there are no more to return.
  do 
  {
    Status = LsaEnumerateTrustedDomains(
       PolicyHandle,         // an open policy handle
       &hEnum,               // enumeration tracker
       (PVOID*)&TrustInfo,   // buffer to receive data
       32000,                // recommended buffer size
       &ulReturned           // number of items returned in TrustInfo
    );

    // Check the return status for errors.
    if((Status != STATUS_SUCCESS) &&
       (Status != STATUS_MORE_ENTRIES) &&
     (Status != STATUS_NO_MORE_ENTRIES))
      {
        // Handle the error.
        wprintf(L"Error occurred enumerating domains %lu\n",
        LsaNtStatusToWinError(Status));
        return;
      } 

      wprintf(L"Status %lu\n", LsaNtStatusToWinError(Status));
      // Process the trusted domain information.
      for (i=0;i<ulReturned; i++) 
      {
        // LSA_Unicode strings might not be null-terminated.
        if(TrustInfo[i].Name.Length < 256)
        {
            wcsncpy_s(StringBuffer,
                256,
                TrustInfo[i].Name.Buffer,
                TrustInfo[i].Name.Length
            );
            // Guarantee that StringBuffer is null-terminated.
            StringBuffer[TrustInfo[i].Name.Length] = NULL; 
        }
        else
        {
            fprintf(stderr, "Name too long for string buffer.\n");
            exit(1);
        }
        
        wprintf(L"Enum Trusted Domain - %ws ", StringBuffer);
      }
      // Free the buffer.
      if (TrustInfo != NULL) 
      {
        LsaFreeMemory(TrustInfo);
        TrustInfo = NULL;
      }
    } while (Status != STATUS_NO_MORE_ENTRIES);
    return;
}
```



 

 



