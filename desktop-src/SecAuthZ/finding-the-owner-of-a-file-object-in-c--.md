---
description: 尋找並列印檔案擁有者的名稱。
ms.assetid: b0dbc785-58a7-4f39-ab39-b96abece5b93
title: 在 c + + 中尋找檔案物件的擁有者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fa4b63de3f16629d3de2102521477ff8ed90e2ca5af8e858ebed63038be7cfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117781663"
---
# <a name="finding-the-owner-of-a-file-object-in-c"></a>在 c + + 中尋找檔案物件的擁有者

下列範例會使用 [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) 和 [**LookupAccountSid**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountsida) 函數來尋找和列印檔案擁有者的名稱。 檔案存在於本機伺服器上的目前工作目錄中。


```C++
#include <stdio.h>
#include <windows.h>
#include <tchar.h>
#include "accctrl.h"
#include "aclapi.h"
#pragma comment(lib, "advapi32.lib")

int main(void)
{
DWORD dwRtnCode = 0;
PSID pSidOwner = NULL;
BOOL bRtnBool = TRUE;
LPTSTR AcctName = NULL;
LPTSTR DomainName = NULL;
DWORD dwAcctName = 1, dwDomainName = 1;
SID_NAME_USE eUse = SidTypeUnknown;
HANDLE hFile;
PSECURITY_DESCRIPTOR pSD = NULL;


// Get the handle of the file object.
hFile = CreateFile(
                  TEXT("myfile.txt"),
                  GENERIC_READ,
                  FILE_SHARE_READ,
                  NULL,
                  OPEN_EXISTING,
                  FILE_ATTRIBUTE_NORMAL,
                  NULL);

// Check GetLastError for CreateFile error code.
if (hFile == INVALID_HANDLE_VALUE) {
          DWORD dwErrorCode = 0;

          dwErrorCode = GetLastError();
          _tprintf(TEXT("CreateFile error = %d\n"), dwErrorCode);
          return -1;
}



// Get the owner SID of the file.
dwRtnCode = GetSecurityInfo(
                  hFile,
                  SE_FILE_OBJECT,
                  OWNER_SECURITY_INFORMATION,
                  &pSidOwner,
                  NULL,
                  NULL,
                  NULL,
                  &pSD);

// Check GetLastError for GetSecurityInfo error condition.
if (dwRtnCode != ERROR_SUCCESS) {
          DWORD dwErrorCode = 0;

          dwErrorCode = GetLastError();
          _tprintf(TEXT("GetSecurityInfo error = %d\n"), dwErrorCode);
          return -1;
}

// First call to LookupAccountSid to get the buffer sizes.
bRtnBool = LookupAccountSid(
                  NULL,           // local computer
                  pSidOwner,
                  AcctName,
                  (LPDWORD)&dwAcctName,
                  DomainName,
                  (LPDWORD)&dwDomainName,
                  &eUse);

// Reallocate memory for the buffers.
AcctName = (LPTSTR)GlobalAlloc(
          GMEM_FIXED,
          dwAcctName);

// Check GetLastError for GlobalAlloc error condition.
if (AcctName == NULL) {
          DWORD dwErrorCode = 0;

          dwErrorCode = GetLastError();
          _tprintf(TEXT("GlobalAlloc error = %d\n"), dwErrorCode);
          return -1;
}

    DomainName = (LPTSTR)GlobalAlloc(
           GMEM_FIXED,
           dwDomainName);

    // Check GetLastError for GlobalAlloc error condition.
    if (DomainName == NULL) {
          DWORD dwErrorCode = 0;

          dwErrorCode = GetLastError();
          _tprintf(TEXT("GlobalAlloc error = %d\n"), dwErrorCode);
          return -1;

    }

    // Second call to LookupAccountSid to get the account name.
    bRtnBool = LookupAccountSid(
          NULL,                   // name of local or remote computer
          pSidOwner,              // security identifier
          AcctName,               // account name buffer
          (LPDWORD)&dwAcctName,   // size of account name buffer 
          DomainName,             // domain name
          (LPDWORD)&dwDomainName, // size of domain name buffer
          &eUse);                 // SID type

    // Check GetLastError for LookupAccountSid error condition.
    if (bRtnBool == FALSE) {
          DWORD dwErrorCode = 0;

          dwErrorCode = GetLastError();

          if (dwErrorCode == ERROR_NONE_MAPPED)
              _tprintf(TEXT
                  ("Account owner not found for specified SID.\n"));
          else 
              _tprintf(TEXT("Error in LookupAccountSid.\n"));
          return -1;

    } else if (bRtnBool == TRUE) 

        // Print the account name.
        _tprintf(TEXT("Account owner = %s\n"), AcctName);

    return 0;
}
```



 

 



