---
title: 建立新的電腦帳戶
description: 下列程式碼範例示範如何使用 NetUserAdd 函數建立新的電腦帳戶。
ms.assetid: 1e180b8e-b948-4836-b789-cb9dff0829e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9b54b3e3b157bfed33b3f2429024e005b9b859bba563c0173b2ca02ab5f499
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912298"
---
# <a name="creating-a-new-computer-account"></a>建立新的電腦帳戶

下列程式碼範例示範如何使用 [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) 函數建立新的電腦帳戶。

以下是管理電腦帳戶的考慮：

-   電腦帳戶名稱應該全部大寫，以與帳戶管理公用程式一致。
-   電腦帳戶名稱的尾端貨幣正負號 ($) 。 任何用來管理電腦帳戶的函式都必須建立電腦名稱稱，使電腦帳戶名稱的最後一個字元是 ($) 的貨幣符號。 若為限域信任，帳戶名稱為 TrustingDomainName $。
-   電腦名稱稱長度上限是 \_ (15) 的最大 COMPUTERNAME \_ 長度。 此長度不包含尾端貨幣正負號 ($) 。
-   新電腦帳戶的密碼應為電腦帳戶名稱的小寫標記法，但不含尾端的貨幣正負號 ($) 。 若為限域信任，密碼可以是與關聯性信任端上指定之值相符的任意值。
-   最大密碼長度為 LM20 \_ PWLEN (14) 。 如果電腦帳戶名稱超過此長度，則應將密碼截斷為此長度。
-   在電腦帳戶建立時所提供的密碼，只有在電腦帳戶變成網域上的作用中時才有效。 在啟用信任關係時，會建立新的密碼。


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



呼叫帳戶管理功能的使用者必須具有目的電腦的系統管理員許可權。 如果是現有的電腦帳戶，則不論系統管理成員資格為何，帳戶的建立者都可以管理該帳戶。 如需呼叫需要系統管理員許可權之函式的詳細資訊，請參閱 [以特殊許可權](/windows/desktop/SecBP/running-with-special-privileges)執行。

您可以在目的電腦上授與 SeMachineAccountPrivilege，讓指定的使用者能夠建立電腦帳戶。 這讓非系統管理員能夠建立電腦帳戶。 呼叫端必須先啟用此許可權，才能新增電腦帳戶。 如需帳戶許可權的詳細資訊，請參閱 [許可權](/windows/desktop/SecAuthZ/privileges) 和 [授權常數](/windows/desktop/SecAuthZ/authorization-constants)。

 

 