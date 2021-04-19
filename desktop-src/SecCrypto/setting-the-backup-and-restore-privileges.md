---
description: 若要成功呼叫憑證服務備份和還原 API，呼叫端的權杖必須包含備份和還原許可權。
ms.assetid: 409a9fad-7141-4ba8-ab3d-fb590366001e
title: 設定備份和還原許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd70c3726c435efa1f000add101bbf50b725bb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966658"
---
# <a name="setting-the-backup-and-restore-privileges"></a><span data-ttu-id="7d6e3-103">設定備份和還原許可權</span><span class="sxs-lookup"><span data-stu-id="7d6e3-103">Setting the Backup and Restore Privileges</span></span>

<span data-ttu-id="7d6e3-104">若要成功呼叫憑證服務備份和還原 API，呼叫端的權杖必須包含備份和還原 [*許可權*](../secgloss/p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="7d6e3-104">To successfully call the Certificate Services backup and restore API, the caller's token must include the backup and restore [*privileges*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="7d6e3-105">您可以透過程式設計方式設定這些許可權，而且可以使用下列範例來設定或移除這些許可權。</span><span class="sxs-lookup"><span data-stu-id="7d6e3-105">These privileges can be programmatically set, and the following example can be used to set or remove these privileges.</span></span> <span data-ttu-id="7d6e3-106">所有備份和還原應用程式都需要備份和還原許可權，而不只是憑證服務備份和還原。</span><span class="sxs-lookup"><span data-stu-id="7d6e3-106">The backup and restore privileges are required of all backup and restore applications, not merely Certificate Services backup and restore.</span></span> <span data-ttu-id="7d6e3-107">如需有關修改許可權之安全性含意的詳細資訊，請參閱 [以特殊許可權](../secbp/running-with-special-privileges.md)執行。</span><span class="sxs-lookup"><span data-stu-id="7d6e3-107">For information about the security implications of modifying privileges, see [Running with Special Privileges](../secbp/running-with-special-privileges.md).</span></span>


```C++
// The following example can be used to enable or disable the
// backup privilege. By making the indicated substitutions, you can
// also use this example to enable or disable the restore privilege 
// Use the following statement to enable the privilege:
//   hr = ModifyPrivilege(SE_BACKUP_NAME, TRUE);
// Use the following statement to disable the privilege:
//   hr = ModifyPrivilege(SE_BACKUP_NAME, FALSE);
// Use SE_RESTORE_NAME for the restore privilege.
// The main function in this example enables the backup privilege.
#pragma comment(lib, "crypt32.lib")

#include <windows.h>
#include <stdio.h>


HRESULT ModifyPrivilege(
    IN LPCTSTR szPrivilege,
    IN BOOL fEnable)
{
    HRESULT hr = S_OK;
    TOKEN_PRIVILEGES NewState;
    LUID             luid;
    HANDLE hToken    = NULL;

    // Open the process token for this process.
    if (!OpenProcessToken(GetCurrentProcess(),
                          TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY,
                          &hToken ))
    {
        printf("Failed OpenProcessToken\n");
        return ERROR_FUNCTION_FAILED;
    }

    // Get the local unique ID for the privilege.
    if ( !LookupPrivilegeValue( NULL,
                                szPrivilege,
                                &luid ))
    {
        CloseHandle( hToken );
        printf("Failed LookupPrivilegeValue\n");
        return ERROR_FUNCTION_FAILED;
    }

    // Assign values to the TOKEN_PRIVILEGE structure.
    NewState.PrivilegeCount = 1;
    NewState.Privileges[0].Luid = luid;
    NewState.Privileges[0].Attributes = 
              (fEnable ? SE_PRIVILEGE_ENABLED : 0);

    // Adjust the token privilege.
    if (!AdjustTokenPrivileges(hToken,
                               FALSE,
                               &NewState,
                               0,
                               NULL,
                               NULL))
    {
        printf("Failed AdjustTokenPrivileges\n");
        hr = ERROR_FUNCTION_FAILED;
    }

    // Close the handle.
    CloseHandle(hToken);

    return hr;
}

void main(void)
{
    HRESULT hr;

    hr = ModifyPrivilege(SE_BACKUP_NAME, TRUE);

    if (!SUCCEEDED(hr))
        printf("\nFailed to modify privilege.\n");
    else
        printf("\nSuccessfully modified privilege.\n");
}

```



 

 
