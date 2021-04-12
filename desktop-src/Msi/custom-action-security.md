---
description: 安裝程式預設會以使用者權限執行自訂動作，以限制對系統的自訂動作的存取。
ms.assetid: 62a3d103-a786-4727-b757-3a8229c8a53f
title: 自訂動作安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7d36e0e5c6cecc61730144fb7efdeed63ba0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320880"
---
# <a name="custom-action-security"></a>自訂動作安全性

安裝程式預設會以使用者權限執行自訂動作，以限制對系統的自訂動作的存取。 如果正在安裝受管理的應用程式，或已針對較高的許可權指定系統原則，則安裝程式可能會以更高的許可權執行自訂動作。

您應該使用 [**MsiHiddenProperties**](msihiddenproperties.md) 屬性和 **msidbCustomActionTypeHideTarget** 來防止記錄自訂動作所使用的機密資訊。 如需 **msidbCustomActionTypeHideTarget** 的詳細資訊，請參閱 [自訂動作隱藏目標選項](custom-action-hidden-target-option.md)。

設定之後，請清除 [CustomActionData] 屬性，以確保機密資料無法再使用。 下列範例程式碼是由立即 DLL 自訂動作所使用的程式碼片段，它會設定資料供延遲的自訂動作（稱為 "MyDeferredCA"）使用：


```C++
#include <windows.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall MyImmediateCA(MSIHANDLE hInstall)
{
    // set up information for deferred custom action called MyDeferredCA
    const TCHAR szValue[] = TEXT("data");
    UINT uiStat = ERROR_INSTALL_FAILURE;
    if (ERROR_SUCCESS == MsiSetProperty(hInstall, TEXT("MyDeferredCA"), szValue))
    {
        uiStat = MsiDoAction(hInstall, TEXT("MyDeferredCA"));

        // clear CustomActionData property
        if (ERROR_SUCCESS != MsiSetProperty(hInstall, TEXT("MyDeferredCA"), TEXT("")))
            return ERROR_INSTALL_FAILURE;
    }

    return (uiStat == ERROR_SUCCESS) ? uiStat : ERROR_INSTALL_FAILURE;    
}
```



請注意，只有 [延後執行自訂動作](deferred-execution-custom-actions.md) 可以使用 **msidbCustomActionTypeNoImpersonate** 屬性。 如需詳細資訊，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。

如果未設定自訂動作的 **msidbCustomActionTypeNoImpersonate** 位，安裝程式會使用使用者層級許可權來執行自訂動作。 如需詳細資訊，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。

如果已設定 **msidbCustomActionTypeNoImpersonate** 位，且使用系統管理員許可權來安裝受控應用程式，安裝程式可能會以較高的許可權執行自訂動作。 不過，如果使用者嘗試在沒有系統管理員許可權的情況下安裝受管理的應用程式，則安裝程式會使用使用者層級許可權來執行應用程式，而不論是否已設定 **msidbCustomActionTypeNoImpersonate** 。

請注意，即使未設定 **msidbCustomActionTypeNoImpersonate** 位，自訂動作也可能會以系統許可權執行。 如果系統管理員為執行終端機伺服器角色2000服務的伺服器上的所有使用者安裝應用程式，且該動作未標記為 **msidbCustomActionTypeTSAware**，就會發生這種情況。 如果在沒有使用者內容的情況中叫用安裝，自訂動作也可以使用系統許可權來執行。 例如，在 Windows 2000 應用程式部署所叫用的安裝期間，如果目前沒有登入的使用者。

建立您自己的自訂動作時，您應該一律使用安全的方法來撰寫自訂動作。 如需詳細資訊，請參閱 [保護自訂動作的指導方針](guidelines-for-securing-custom-actions.md)。

 

 



