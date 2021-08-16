---
description: 檢查安全描述項允許用戶端的存取權限。
ms.assetid: de21968e-4590-4798-9152-43204d55521f
title: 在 c + + 中使用 Acl 確認用戶端存取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2160b48a3b88a617eaaea1e8fae63168db5a85e82cad62be5aef248ff51581
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906688"
---
# <a name="verifying-client-access-with-acls-in-c"></a>在 c + + 中使用 Acl 確認用戶端存取

下列範例顯示伺服器如何檢查 [*安全描述項*](/windows/desktop/SecGloss/s-gly) 允許用於用戶端的存取權限。 此範例使用 [**ImpersonateNamedPipeClient**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient) 函數;不過，它的運作方式與其他任何模擬函數相同。 模擬用戶端之後，此範例會呼叫 [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) 函數來取得模擬 [*權杖*](/windows/desktop/SecGloss/i-gly)。 然後，它會呼叫 [**MapGenericMask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) 函式，根據 [**泛型 \_**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) 對應結構中指定的對應，將任何泛型存取權限轉換為對應的特定和標準許可權。

[**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)函式會根據用戶端在安全描述項的 DACL 中允許的許可權，檢查要求的存取權限。 若要檢查存取權，並在安全性事件記錄檔中產生專案，請使用 [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) 函數。


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



 

 
