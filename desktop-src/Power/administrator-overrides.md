---
description: 系統管理員覆寫
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: 系統管理員覆寫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c43e16c9aa3eb3ab9fd5ee7c8d17b9bb4536315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001368"
---
# <a name="administrator-overrides"></a><span data-ttu-id="b39c0-103">系統管理員覆寫</span><span class="sxs-lookup"><span data-stu-id="b39c0-103">Administrator Overrides</span></span>

<span data-ttu-id="b39c0-104">Windows 在所有的電源原則物件上都有 (ACL) 的單一預設存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="b39c0-104">Windows has a single default access control list (ACL) on all power policy objects.</span></span> <span data-ttu-id="b39c0-105">ACL 會授與「讀取」、「寫入」和「變更」許可權給已驗證的使用者群組的成員。</span><span class="sxs-lookup"><span data-stu-id="b39c0-105">The ACL grants read, write, and change permissions to members of the Authenticated Users group.</span></span> <span data-ttu-id="b39c0-106">所有其他使用者都會被授與唯讀許可權。</span><span class="sxs-lookup"><span data-stu-id="b39c0-106">All other users are granted read-only permission.</span></span> <span data-ttu-id="b39c0-107">呼叫電源原則函式的應用程式可以使用 [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) 函式，來判斷使用者是否具有指定之電源設定的許可權。</span><span class="sxs-lookup"><span data-stu-id="b39c0-107">Applications that call power policy functions can determine whether a user has permissions for a specified power setting by using the [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) function.</span></span>

<span data-ttu-id="b39c0-108">您可以透過群組原則覆寫電源設定。</span><span class="sxs-lookup"><span data-stu-id="b39c0-108">Power settings may be overridden via Group Policy.</span></span> <span data-ttu-id="b39c0-109">您可以透過網域群組原則或本機群組原則來設定覆寫。</span><span class="sxs-lookup"><span data-stu-id="b39c0-109">Overrides can be set through domain group policy or local group policy.</span></span> <span data-ttu-id="b39c0-110">[**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) 將會報告指定的電源設定是否有群組原則覆寫。</span><span class="sxs-lookup"><span data-stu-id="b39c0-110">[**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) will report if a specified power setting has a group policy override.</span></span>

<span data-ttu-id="b39c0-111">當命令無法完成時，命令列工具 **PowerCfg.exe** 會顯示錯誤訊息，因為使用者沒有變更電源設定的許可權，或因為電源設定有群組原則覆寫。</span><span class="sxs-lookup"><span data-stu-id="b39c0-111">The command line tool **PowerCfg.exe** displays an error message when a command cannot be completed either because the user did not have permissions to change the power setting or because the power setting has a group policy override.</span></span>

<span data-ttu-id="b39c0-112">主控台中的電源選項應用程式不支援設定電源原則存取權限。</span><span class="sxs-lookup"><span data-stu-id="b39c0-112">The Power Options application in Control Panel does not provide support for configuring power policy access permissions.</span></span> <span data-ttu-id="b39c0-113">變更許可權必須透過 **PowerCfg.exe** 完成。</span><span class="sxs-lookup"><span data-stu-id="b39c0-113">Changing permissions must be done via **PowerCfg.exe**.</span></span>

 

 



