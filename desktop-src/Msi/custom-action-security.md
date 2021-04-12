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
# <a name="custom-action-security"></a><span data-ttu-id="b8318-103">自訂動作安全性</span><span class="sxs-lookup"><span data-stu-id="b8318-103">Custom Action Security</span></span>

<span data-ttu-id="b8318-104">安裝程式預設會以使用者權限執行自訂動作，以限制對系統的自訂動作的存取。</span><span class="sxs-lookup"><span data-stu-id="b8318-104">The installer runs custom actions with user privileges by default in order to limit the access of custom actions to the system.</span></span> <span data-ttu-id="b8318-105">如果正在安裝受管理的應用程式，或已針對較高的許可權指定系統原則，則安裝程式可能會以更高的許可權執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="b8318-105">The installer may run custom actions with elevated privileges if a managed application is being installed or if the system policy has been specified for elevated privileges.</span></span>

<span data-ttu-id="b8318-106">您應該使用 [**MsiHiddenProperties**](msihiddenproperties.md) 屬性和 **msidbCustomActionTypeHideTarget** 來防止記錄自訂動作所使用的機密資訊。</span><span class="sxs-lookup"><span data-stu-id="b8318-106">You should use the [**MsiHiddenProperties**](msihiddenproperties.md) property and **msidbCustomActionTypeHideTarget** to prevent logging of sensitive information used by the custom action.</span></span> <span data-ttu-id="b8318-107">如需 **msidbCustomActionTypeHideTarget** 的詳細資訊，請參閱 [自訂動作隱藏目標選項](custom-action-hidden-target-option.md)。</span><span class="sxs-lookup"><span data-stu-id="b8318-107">For more information about **msidbCustomActionTypeHideTarget** see [Custom Action Hidden Target Option](custom-action-hidden-target-option.md).</span></span>

<span data-ttu-id="b8318-108">設定之後，請清除 [CustomActionData] 屬性，以確保機密資料無法再使用。</span><span class="sxs-lookup"><span data-stu-id="b8318-108">Clear the CustomActionData property after setting it to ensure that sensitive data is no longer available.</span></span> <span data-ttu-id="b8318-109">下列範例程式碼是由立即 DLL 自訂動作所使用的程式碼片段，它會設定資料供延遲的自訂動作（稱為 "MyDeferredCA"）使用：</span><span class="sxs-lookup"><span data-stu-id="b8318-109">Example code below is a snippet used by an immediate DLL custom action that is setting up data for use by a deferred custom action called "MyDeferredCA":</span></span>


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



<span data-ttu-id="b8318-110">請注意，只有 [延後執行自訂動作](deferred-execution-custom-actions.md) 可以使用 **msidbCustomActionTypeNoImpersonate** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b8318-110">Note that only [deferred execution custom actions](deferred-execution-custom-actions.md) can use the **msidbCustomActionTypeNoImpersonate** attribute.</span></span> <span data-ttu-id="b8318-111">如需詳細資訊，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。</span><span class="sxs-lookup"><span data-stu-id="b8318-111">For more information see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="b8318-112">如果未設定自訂動作的 **msidbCustomActionTypeNoImpersonate** 位，安裝程式會使用使用者層級許可權來執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="b8318-112">If the **msidbCustomActionTypeNoImpersonate** bit is not set for a custom action, the installer runs the custom action with user-level privileges.</span></span> <span data-ttu-id="b8318-113">如需詳細資訊，請參閱 [自訂動作 In-Script 執行選項](custom-action-in-script-execution-options.md)。</span><span class="sxs-lookup"><span data-stu-id="b8318-113">For more information, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="b8318-114">如果已設定 **msidbCustomActionTypeNoImpersonate** 位，且使用系統管理員許可權來安裝受控應用程式，安裝程式可能會以較高的許可權執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="b8318-114">If the **msidbCustomActionTypeNoImpersonate** bit is set and a managed application is being installed with administrator permission, the installer may run the custom action with elevated privileges.</span></span> <span data-ttu-id="b8318-115">不過，如果使用者嘗試在沒有系統管理員許可權的情況下安裝受管理的應用程式，則安裝程式會使用使用者層級許可權來執行應用程式，而不論是否已設定 **msidbCustomActionTypeNoImpersonate** 。</span><span class="sxs-lookup"><span data-stu-id="b8318-115">However, if a user attempts to install the managed application without administrator permission, the installer runs the application with user level privileges regardless of whether **msidbCustomActionTypeNoImpersonate** is set.</span></span>

<span data-ttu-id="b8318-116">請注意，即使未設定 **msidbCustomActionTypeNoImpersonate** 位，自訂動作也可能會以系統許可權執行。</span><span class="sxs-lookup"><span data-stu-id="b8318-116">Note that a custom action may run with system privileges even when the **msidbCustomActionTypeNoImpersonate** bit is not set.</span></span> <span data-ttu-id="b8318-117">如果系統管理員為執行終端機伺服器角色2000服務的伺服器上的所有使用者安裝應用程式，且該動作未標記為 **msidbCustomActionTypeTSAware**，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="b8318-117">This occurs if an administrator installs the application for all users on a server running the Terminal Server role service using Windows 2000 and the action is not marked with **msidbCustomActionTypeTSAware**.</span></span> <span data-ttu-id="b8318-118">如果在沒有使用者內容的情況中叫用安裝，自訂動作也可以使用系統許可權來執行。</span><span class="sxs-lookup"><span data-stu-id="b8318-118">A custom action may also run with system privileges if the installation is invoked when there is no user context.</span></span> <span data-ttu-id="b8318-119">例如，在 Windows 2000 應用程式部署所叫用的安裝期間，如果目前沒有登入的使用者。</span><span class="sxs-lookup"><span data-stu-id="b8318-119">For example, if there is no currently logged-on user during an installation invoked by Windows 2000 Application Deployment.</span></span>

<span data-ttu-id="b8318-120">建立您自己的自訂動作時，您應該一律使用安全的方法來撰寫自訂動作。</span><span class="sxs-lookup"><span data-stu-id="b8318-120">When creating your own custom actions, you should always author the custom action using secure methods.</span></span> <span data-ttu-id="b8318-121">如需詳細資訊，請參閱 [保護自訂動作的指導方針](guidelines-for-securing-custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="b8318-121">For more information, see [Guidelines for Securing Custom Actions](guidelines-for-securing-custom-actions.md).</span></span>

 

 



