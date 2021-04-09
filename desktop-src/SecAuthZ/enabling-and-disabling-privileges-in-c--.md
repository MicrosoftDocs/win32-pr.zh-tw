---
description: 啟用存取權杖中的許可權，可讓程式執行先前無法執行的系統層級動作。
ms.assetid: aa2d3fe7-01ee-4243-b72c-3e8b90068e22
title: 在 c + + 中啟用和停用許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354f3ac2b27a7c027bd7c48e753263c43b676dd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027247"
---
# <a name="enabling-and-disabling-privileges-in-c"></a>在 c + + 中啟用和停用許可權

啟用存取權杖中的許可權，可讓程式執行先前無法執行的系統層級動作。 您的應用程式應該徹底驗證許可權是否適合帳戶的類型，特別是針對下列強大的許可權。



| 許可權常數           | 字串值                  | 顯示名稱                        |
|------------------------------|-------------------------------|-------------------------------------|
| SE \_ ASSIGNPRIMARYTOKEN \_ 名稱 | SeAssignPrimaryTokenPrivilege | 取代處理序層級權杖       |
| SE \_ 備份 \_ 名稱             | SeBackupPrivilege             | 備份檔案及目錄       |
| SE \_ DEBUG \_ 名稱              | SeDebugPrivilege              | 偵錯程式                      |
| SE \_ 增加 \_ 配額 \_ 名稱    | SeIncreaseQuotaPrivilege      | 調整處理程序的記憶體配額  |
| SE \_ TCB \_ 名稱                | SeTcbPrivilege                | 作為作業系統的一部分 |



 

在啟用上述任何可能危險的許可權之前，請先判斷程式碼中的函式或作業確實需要許可權。 例如，作業系統中很少的函式實際上需要 **SeTcbPrivilege**。 如需所有可用許可權的清單，請參閱 [許可權常數](authorization-constants.md)。

下列範例示範如何啟用或停用 [*存取權杖*](/windows/desktop/SecGloss/a-gly)中的許可權。 此範例會呼叫 [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) 函數，以取得本機系統用來識別許可權的 [*本機唯一識別碼*](/windows/desktop/SecGloss/l-gly) (LUID) 。 然後，此範例會呼叫 [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) 函數，以啟用或停用相依于 *bEnablePrivilege* 參數值的許可權。


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "cmcfg32.lib")

BOOL SetPrivilege(
    HANDLE hToken,          // access token handle
    LPCTSTR lpszPrivilege,  // name of privilege to enable/disable
    BOOL bEnablePrivilege   // to enable or disable privilege
    ) 
{
    TOKEN_PRIVILEGES tp;
    LUID luid;

    if ( !LookupPrivilegeValue( 
            NULL,            // lookup privilege on local system
            lpszPrivilege,   // privilege to lookup 
            &luid ) )        // receives LUID of privilege
    {
        printf("LookupPrivilegeValue error: %u\n", GetLastError() ); 
        return FALSE; 
    }

    tp.PrivilegeCount = 1;
    tp.Privileges[0].Luid = luid;
    if (bEnablePrivilege)
        tp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED;
    else
        tp.Privileges[0].Attributes = 0;

    // Enable the privilege or disable all privileges.

    if ( !AdjustTokenPrivileges(
           hToken, 
           FALSE, 
           &tp, 
           sizeof(TOKEN_PRIVILEGES), 
           (PTOKEN_PRIVILEGES) NULL, 
           (PDWORD) NULL) )
    { 
          printf("AdjustTokenPrivileges error: %u\n", GetLastError() ); 
          return FALSE; 
    } 

    if (GetLastError() == ERROR_NOT_ALL_ASSIGNED)

    {
          printf("The token does not have the specified privilege. \n");
          return FALSE;
    } 

    return TRUE;
}

```



 

