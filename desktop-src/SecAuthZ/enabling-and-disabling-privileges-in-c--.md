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
# <a name="enabling-and-disabling-privileges-in-c"></a><span data-ttu-id="df4d8-103">在 c + + 中啟用和停用許可權</span><span class="sxs-lookup"><span data-stu-id="df4d8-103">Enabling and Disabling Privileges in C++</span></span>

<span data-ttu-id="df4d8-104">啟用存取權杖中的許可權，可讓程式執行先前無法執行的系統層級動作。</span><span class="sxs-lookup"><span data-stu-id="df4d8-104">Enabling a privilege in an access token allows the process to perform system-level actions that it could not previously.</span></span> <span data-ttu-id="df4d8-105">您的應用程式應該徹底驗證許可權是否適合帳戶的類型，特別是針對下列強大的許可權。</span><span class="sxs-lookup"><span data-stu-id="df4d8-105">Your application should thoroughly verify that the privilege is appropriate to the type of account, especially for the following powerful privileges.</span></span>



| <span data-ttu-id="df4d8-106">許可權常數</span><span class="sxs-lookup"><span data-stu-id="df4d8-106">Privilege constant</span></span>           | <span data-ttu-id="df4d8-107">字串值</span><span class="sxs-lookup"><span data-stu-id="df4d8-107">String value</span></span>                  | <span data-ttu-id="df4d8-108">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="df4d8-108">Display name</span></span>                        |
|------------------------------|-------------------------------|-------------------------------------|
| <span data-ttu-id="df4d8-109">SE \_ ASSIGNPRIMARYTOKEN \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="df4d8-109">SE\_ASSIGNPRIMARYTOKEN\_NAME</span></span> | <span data-ttu-id="df4d8-110">SeAssignPrimaryTokenPrivilege</span><span class="sxs-lookup"><span data-stu-id="df4d8-110">SeAssignPrimaryTokenPrivilege</span></span> | <span data-ttu-id="df4d8-111">取代處理序層級權杖</span><span class="sxs-lookup"><span data-stu-id="df4d8-111">Replace a process-level token</span></span>       |
| <span data-ttu-id="df4d8-112">SE \_ 備份 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="df4d8-112">SE\_BACKUP\_NAME</span></span>             | <span data-ttu-id="df4d8-113">SeBackupPrivilege</span><span class="sxs-lookup"><span data-stu-id="df4d8-113">SeBackupPrivilege</span></span>             | <span data-ttu-id="df4d8-114">備份檔案及目錄</span><span class="sxs-lookup"><span data-stu-id="df4d8-114">Back up files and directories</span></span>       |
| <span data-ttu-id="df4d8-115">SE \_ DEBUG \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="df4d8-115">SE\_DEBUG\_NAME</span></span>              | <span data-ttu-id="df4d8-116">SeDebugPrivilege</span><span class="sxs-lookup"><span data-stu-id="df4d8-116">SeDebugPrivilege</span></span>              | <span data-ttu-id="df4d8-117">偵錯程式</span><span class="sxs-lookup"><span data-stu-id="df4d8-117">Debug programs</span></span>                      |
| <span data-ttu-id="df4d8-118">SE \_ 增加 \_ 配額 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="df4d8-118">SE\_INCREASE\_QUOTA\_NAME</span></span>    | <span data-ttu-id="df4d8-119">SeIncreaseQuotaPrivilege</span><span class="sxs-lookup"><span data-stu-id="df4d8-119">SeIncreaseQuotaPrivilege</span></span>      | <span data-ttu-id="df4d8-120">調整處理程序的記憶體配額</span><span class="sxs-lookup"><span data-stu-id="df4d8-120">Adjust memory quotas for a process</span></span>  |
| <span data-ttu-id="df4d8-121">SE \_ TCB \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="df4d8-121">SE\_TCB\_NAME</span></span>                | <span data-ttu-id="df4d8-122">SeTcbPrivilege</span><span class="sxs-lookup"><span data-stu-id="df4d8-122">SeTcbPrivilege</span></span>                | <span data-ttu-id="df4d8-123">作為作業系統的一部分</span><span class="sxs-lookup"><span data-stu-id="df4d8-123">Act as part of the operating system</span></span> |



 

<span data-ttu-id="df4d8-124">在啟用上述任何可能危險的許可權之前，請先判斷程式碼中的函式或作業確實需要許可權。</span><span class="sxs-lookup"><span data-stu-id="df4d8-124">Before enabling any of these potentially dangerous privileges, determine that functions or operations in your code actually require the privileges.</span></span> <span data-ttu-id="df4d8-125">例如，作業系統中很少的函式實際上需要 **SeTcbPrivilege**。</span><span class="sxs-lookup"><span data-stu-id="df4d8-125">For example, very few functions in the operating system actually require the **SeTcbPrivilege**.</span></span> <span data-ttu-id="df4d8-126">如需所有可用許可權的清單，請參閱 [許可權常數](authorization-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="df4d8-126">For a list of all the available privileges, see [Privilege Constants](authorization-constants.md).</span></span>

<span data-ttu-id="df4d8-127">下列範例示範如何啟用或停用 [*存取權杖*](/windows/desktop/SecGloss/a-gly)中的許可權。</span><span class="sxs-lookup"><span data-stu-id="df4d8-127">The following example shows how to enable or disable a privilege in an [*access token*](/windows/desktop/SecGloss/a-gly).</span></span> <span data-ttu-id="df4d8-128">此範例會呼叫 [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) 函數，以取得本機系統用來識別許可權的 [*本機唯一識別碼*](/windows/desktop/SecGloss/l-gly) (LUID) 。</span><span class="sxs-lookup"><span data-stu-id="df4d8-128">The example calls the [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) function to get the [*locally unique identifier*](/windows/desktop/SecGloss/l-gly) (LUID) that the local system uses to identify the privilege.</span></span> <span data-ttu-id="df4d8-129">然後，此範例會呼叫 [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) 函數，以啟用或停用相依于 *bEnablePrivilege* 參數值的許可權。</span><span class="sxs-lookup"><span data-stu-id="df4d8-129">Then the example calls the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function, which either enables or disables the privilege that depends on the value of the *bEnablePrivilege* parameter.</span></span>


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



 

