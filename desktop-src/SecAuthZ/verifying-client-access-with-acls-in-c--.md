---
description: 檢查安全描述項允許用戶端的存取權限。
ms.assetid: de21968e-4590-4798-9152-43204d55521f
title: 在 c + + 中使用 Acl 確認用戶端存取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda629338d731d6e93f316fc15a6338c99bc1609
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850140"
---
# <a name="verifying-client-access-with-acls-in-c"></a><span data-ttu-id="6355c-103">在 c + + 中使用 Acl 確認用戶端存取</span><span class="sxs-lookup"><span data-stu-id="6355c-103">Verifying Client Access with ACLs in C++</span></span>

<span data-ttu-id="6355c-104">下列範例顯示伺服器如何檢查 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 允許用於用戶端的存取權限。</span><span class="sxs-lookup"><span data-stu-id="6355c-104">The following example shows how a server could check the access rights that a [*security descriptor*](/windows/desktop/SecGloss/s-gly) allows for a client.</span></span> <span data-ttu-id="6355c-105">此範例使用 [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) 函數;不過，它的運作方式與其他任何模擬函數相同。</span><span class="sxs-lookup"><span data-stu-id="6355c-105">The example uses the [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) function; however, it would work the same using any of the other impersonation functions.</span></span> <span data-ttu-id="6355c-106">模擬用戶端之後，此範例會呼叫 [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) 函數來取得模擬 [*權杖*](/windows/desktop/SecGloss/i-gly)。</span><span class="sxs-lookup"><span data-stu-id="6355c-106">After impersonating the client, the example calls the [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) function to get the [*impersonation token*](/windows/desktop/SecGloss/i-gly).</span></span> <span data-ttu-id="6355c-107">然後，它會呼叫 [**MapGenericMask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) 函式，根據 [**泛型 \_**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) 對應結構中指定的對應，將任何泛型存取權限轉換為對應的特定和標準許可權。</span><span class="sxs-lookup"><span data-stu-id="6355c-107">Then, it calls the [**MapGenericMask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) function to convert any generic access rights to the corresponding specific and standard rights according to the mapping specified in the [**GENERIC\_MAPPING**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) structure.</span></span>

<span data-ttu-id="6355c-108">[**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)函式會根據用戶端在安全描述項的 DACL 中允許的許可權，檢查要求的存取權限。</span><span class="sxs-lookup"><span data-stu-id="6355c-108">The [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) function checks the requested access rights against the rights allowed for the client in the DACL of the security descriptor.</span></span> <span data-ttu-id="6355c-109">若要檢查存取權，並在安全性事件記錄檔中產生專案，請使用 [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) 函數。</span><span class="sxs-lookup"><span data-stu-id="6355c-109">To check access and generate an entry in the security event log, use the [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) function.</span></span>


```C++
#include <windows.h>
#pragma comment(lib, "advapi32.lib")

BOOL ImpersonateAndCheckAccess(
  HANDLE hNamedPipe,               // handle of pipe to impersonate
  PSECURITY_DESCRIPTOR pSD,        // security descriptor to check
  DWORD dwAccessDesired,           // access rights to check
  PGENERIC_MAPPING pGeneric,       // generic mapping for object
  PDWORD pdwAccessAllowed          // returns allowed access rights
) 
{
   HANDLE hToken;
   PRIVILEGE_SET PrivilegeSet;
   DWORD dwPrivSetSize = sizeof( PRIVILEGE_SET );
   BOOL fAccessGranted=FALSE;

// Impersonate the client.

   if (! ImpersonateNamedPipeClient(hNamedPipe) ) 
      return FALSE;

// Get an impersonation token with the client's security context.

   if (! OpenThreadToken( GetCurrentThread(), TOKEN_ALL_ACCESS,
         TRUE, &hToken ))
   {
      goto Cleanup;
   }

// Use the GENERIC_MAPPING structure to convert any 
// generic access rights to object-specific access rights.

   MapGenericMask( &dwAccessDesired, pGeneric );

// Check the client's access rights.

   if( !AccessCheck( 
      pSD,                 // security descriptor to check
      hToken,              // impersonation token
      dwAccessDesired,     // requested access rights
      pGeneric,            // pointer to GENERIC_MAPPING
      &PrivilegeSet,       // receives privileges used in check
      &dwPrivSetSize,      // size of PrivilegeSet buffer
      pdwAccessAllowed,    // receives mask of allowed access rights
      &fAccessGranted ))   // receives results of access check
   {
      goto Cleanup;
   }

Cleanup:

   RevertToSelf();

   if (hToken != INVALID_HANDLE_VALUE)
      CloseHandle(hToken);  

   return fAccessGranted;
}
```



 

 
