---
description: LSA 原則提供數個函式，可讓您用來建立、列舉及刪除信任的網域，以及設定和取得受信任的網域資訊。
ms.assetid: 0c7534d7-3372-49c4-992c-9b519279982d
title: 管理受信任的網域資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7df297b8c83ebe9054ca6f04b657905c21fae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194360"
---
# <a name="managing-trusted-domain-information"></a><span data-ttu-id="e7c02-103">管理受信任的網域資訊</span><span class="sxs-lookup"><span data-stu-id="e7c02-103">Managing Trusted Domain Information</span></span>

<span data-ttu-id="e7c02-104">LSA 原則提供數個函式，可讓您用來建立、列舉及刪除信任的網域，以及設定和取得受信任的網域資訊。</span><span class="sxs-lookup"><span data-stu-id="e7c02-104">LSA Policy provides several functions that you can use to create, enumerate, and delete trusted domains and to set and retrieve trusted domain information.</span></span>

<span data-ttu-id="e7c02-105">在您可以管理受信任的網域資訊之前，您的應用程式必須取得 [**原則**](policy-object.md) 物件的控制碼，如 [開啟原則物件控制碼](opening-a-policy-object-handle.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="e7c02-105">Before you can manage trusted domain information, your application must get a handle to a [**Policy**](policy-object.md) object, as explained in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span>

<span data-ttu-id="e7c02-106">您可以藉由呼叫 [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)來列舉受信任的網域。</span><span class="sxs-lookup"><span data-stu-id="e7c02-106">You can enumerate the trusted domains by calling [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span></span>

<span data-ttu-id="e7c02-107">若要取得受信任網域的相關資訊，請呼叫 [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo) 或 [**>lsaquerytrusteddomaininfobyname**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname)。</span><span class="sxs-lookup"><span data-stu-id="e7c02-107">To retrieve information about a trusted domain, call either [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo) or [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname).</span></span> <span data-ttu-id="e7c02-108">這兩個函數都會傳回相同的資訊。不過， **LsaQueryTrustedDomainInfo** 會依 SID 識別受信任的網域，而 **>lsaquerytrusteddomaininfobyname** 會依名稱識別受信任的網域。</span><span class="sxs-lookup"><span data-stu-id="e7c02-108">Both functions return the same information; however, **LsaQueryTrustedDomainInfo** identifies the trusted domain by SID, and **LsaQueryTrustedDomainInfoByName** identifies the trusted domain by name.</span></span>

<span data-ttu-id="e7c02-109">若要設定受信任網域的資訊，請呼叫 [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation) 或 [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname)。</span><span class="sxs-lookup"><span data-stu-id="e7c02-109">To set information for a trusted domain, call either [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation) or [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname).</span></span> <span data-ttu-id="e7c02-110">如同查詢函式， **LsaSetTrustedDomainInformation** 會依 SID 識別受信任的網域，而 **LsaSetTrustedDomainInfoByName** 會依名稱識別受信任的網域。</span><span class="sxs-lookup"><span data-stu-id="e7c02-110">As with the query functions, **LsaSetTrustedDomainInformation** identifies the trusted domain by SID, while **LsaSetTrustedDomainInfoByName** identifies the trusted domain by name.</span></span>

<span data-ttu-id="e7c02-111">您的應用程式可以藉由呼叫 [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain)來撤銷受信任網域的信任關係。</span><span class="sxs-lookup"><span data-stu-id="e7c02-111">Your application can revoke a trust relationship for a trusted domain by calling [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain).</span></span>

<span data-ttu-id="e7c02-112">下列範例會列舉本機系統的受信任網域。</span><span class="sxs-lookup"><span data-stu-id="e7c02-112">The following example enumerates the trusted domains for the local system.</span></span>


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



 

 



