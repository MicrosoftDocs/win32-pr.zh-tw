---
title: 建立新的電腦帳戶
description: 下列程式碼範例示範如何使用 NetUserAdd 函數建立新的電腦帳戶。
ms.assetid: 1e180b8e-b948-4836-b789-cb9dff0829e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd02a9d2053310c50e40957e6afee6e3a4a5ab1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965238"
---
# <a name="creating-a-new-computer-account"></a><span data-ttu-id="6ac7f-103">建立新的電腦帳戶</span><span class="sxs-lookup"><span data-stu-id="6ac7f-103">Creating a New Computer Account</span></span>

<span data-ttu-id="6ac7f-104">下列程式碼範例示範如何使用 [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) 函數建立新的電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-104">The following code sample demonstrates how to create a new computer account using the [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) function.</span></span>

<span data-ttu-id="6ac7f-105">以下是管理電腦帳戶的考慮：</span><span class="sxs-lookup"><span data-stu-id="6ac7f-105">The following are considerations for managing computer accounts:</span></span>

-   <span data-ttu-id="6ac7f-106">電腦帳戶名稱應該全部大寫，以與帳戶管理公用程式一致。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-106">The computer account name should be all uppercase for consistency with account management utilities.</span></span>
-   <span data-ttu-id="6ac7f-107">電腦帳戶名稱的尾端貨幣正負號 ($) 。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-107">A computer account name always has a trailing dollar sign ($).</span></span> <span data-ttu-id="6ac7f-108">任何用來管理電腦帳戶的函式都必須建立電腦名稱稱，使電腦帳戶名稱的最後一個字元是 ($) 的貨幣符號。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-108">Any functions used to manage computer accounts must build the computer name such that the last character of the computer account name is a dollar sign ($).</span></span> <span data-ttu-id="6ac7f-109">若為限域信任，帳戶名稱為 TrustingDomainName $。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-109">For interdomain trust, the account name is TrustingDomainName$.</span></span>
-   <span data-ttu-id="6ac7f-110">電腦名稱稱長度上限是 \_ (15) 的最大 COMPUTERNAME \_ 長度。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-110">The maximum computer name length is MAX\_COMPUTERNAME\_LENGTH (15).</span></span> <span data-ttu-id="6ac7f-111">此長度不包含尾端貨幣正負號 ($) 。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-111">This length does not include the trailing dollar sign ($).</span></span>
-   <span data-ttu-id="6ac7f-112">新電腦帳戶的密碼應為電腦帳戶名稱的小寫標記法，但不含尾端的貨幣正負號 ($) 。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-112">The password for a new computer account should be the lowercase representation of the computer account name, without the trailing dollar sign ($).</span></span> <span data-ttu-id="6ac7f-113">若為限域信任，密碼可以是與關聯性信任端上指定之值相符的任意值。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-113">For interdomain trust, the password can be an arbitrary value that matches the value specified on the trust side of the relationship.</span></span>
-   <span data-ttu-id="6ac7f-114">最大密碼長度為 LM20 \_ PWLEN (14) 。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-114">The maximum password length is LM20\_PWLEN (14).</span></span> <span data-ttu-id="6ac7f-115">如果電腦帳戶名稱超過此長度，則應將密碼截斷為此長度。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-115">The password should be truncated to this length if the computer account name exceeds this length.</span></span>
-   <span data-ttu-id="6ac7f-116">在電腦帳戶建立時所提供的密碼，只有在電腦帳戶變成網域上的作用中時才有效。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-116">The password provided at computer-account-creation time is valid only until the computer account becomes active on the domain.</span></span> <span data-ttu-id="6ac7f-117">在啟用信任關係時，會建立新的密碼。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-117">A new password is established during trust relationship activation.</span></span>


```C++
#include <windows.h>
#include <lm.h>
#pragma comment(lib, "netapi32.lib")

BOOL AddMachineAccount(
    LPWSTR wTargetComputer,
    LPWSTR MachineAccount,
    DWORD AccountType
    )
{
    LPWSTR wAccount;
    LPWSTR wPassword;
    USER_INFO_1 ui;
    DWORD cbAccount;
    DWORD cbLength;
    DWORD dwError;

    //
    // Ensure a valid computer account type was passed.
    //
    if (AccountType != UF_WORKSTATION_TRUST_ACCOUNT &&
        AccountType != UF_SERVER_TRUST_ACCOUNT &&
        AccountType != UF_INTERDOMAIN_TRUST_ACCOUNT
        ) 
    {
        SetLastError(ERROR_INVALID_PARAMETER);
        return FALSE;
    }

    //
    // Obtain number of chars in computer account name.
    //
    cbLength = cbAccount = lstrlenW(MachineAccount);

    //
    // Ensure computer name doesn't exceed maximum length.
    //
    if(cbLength > MAX_COMPUTERNAME_LENGTH) {
        SetLastError(ERROR_INVALID_ACCOUNT_NAME);
        return FALSE;
    }

    //
    // Allocate storage to contain Unicode representation of
    // computer account name + trailing $ + NULL.
    //
    wAccount=(LPWSTR)HeapAlloc(GetProcessHeap(), 0,
        (cbAccount + 1 + 1) * sizeof(WCHAR)  // Account + '$' + NULL
        );

    if(wAccount == NULL) return FALSE;

    //
    // Password is the computer account name converted to lowercase;
    //  you will convert the passed MachineAccount in place.
    //
    wPassword = MachineAccount;

    //
    // Copy MachineAccount to the wAccount buffer allocated while
    //  converting computer account name to uppercase.
    //  Convert password (in place) to lowercase.
    //
    while(cbAccount--) {
        wAccount[cbAccount] = towupper( MachineAccount[cbAccount] );
        wPassword[cbAccount] = towlower( wPassword[cbAccount] );
    }

    //
    // Computer account names have a trailing Unicode '$'.
    //
    wAccount[cbLength] = L'$';
    wAccount[cbLength + 1] = L'\0'; // terminate the string

    //
    // If the password is greater than the max allowed, truncate.
    //
    if(cbLength > LM20_PWLEN) wPassword[LM20_PWLEN] = L'\0';

    //
    // Initialize the USER_INFO_1 structure.
    //
    ZeroMemory(&ui, sizeof(ui));

    ui.usri1_name = wAccount;
    ui.usri1_password = wPassword;

    ui.usri1_flags = AccountType | UF_SCRIPT;
    ui.usri1_priv = USER_PRIV_USER;

    dwError=NetUserAdd(
                wTargetComputer,    // target computer name
                1,                  // info level
                (LPBYTE) &ui,       // buffer
                NULL
                );

    //
    // Free allocated memory.
    //
    if(wAccount) HeapFree(GetProcessHeap(), 0, wAccount);

    //
    // Indicate whether the function was successful.
    //
    if(dwError == NO_ERROR)
        return TRUE;
    else {
        SetLastError(dwError);
        return FALSE;
    }
}
```



<span data-ttu-id="6ac7f-118">呼叫帳戶管理功能的使用者必須具有目的電腦的系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-118">The user that calls the account management functions must have Administrator privilege on the target computer.</span></span> <span data-ttu-id="6ac7f-119">如果是現有的電腦帳戶，則不論系統管理成員資格為何，帳戶的建立者都可以管理該帳戶。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-119">In the case of existing computer accounts, the creator of the account can manage the account, regardless of administrative membership.</span></span> <span data-ttu-id="6ac7f-120">如需呼叫需要系統管理員許可權之函式的詳細資訊，請參閱 [以特殊許可權](/windows/desktop/SecBP/running-with-special-privileges)執行。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-120">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="6ac7f-121">您可以在目的電腦上授與 SeMachineAccountPrivilege，讓指定的使用者能夠建立電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-121">The SeMachineAccountPrivilege can be granted on the target computer to give specified users the ability to create computer accounts.</span></span> <span data-ttu-id="6ac7f-122">這讓非系統管理員能夠建立電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-122">This gives non-administrators the ability to create computer accounts.</span></span> <span data-ttu-id="6ac7f-123">呼叫端必須先啟用此許可權，才能新增電腦帳戶。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-123">The caller needs to enable this privilege prior to adding the computer account.</span></span> <span data-ttu-id="6ac7f-124">如需帳戶許可權的詳細資訊，請參閱 [許可權](/windows/desktop/SecAuthZ/privileges) 和 [授權常數](/windows/desktop/SecAuthZ/authorization-constants)。</span><span class="sxs-lookup"><span data-stu-id="6ac7f-124">For more information about account privileges, see [Privileges](/windows/desktop/SecAuthZ/privileges) and [Authorization Constants](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

 

 