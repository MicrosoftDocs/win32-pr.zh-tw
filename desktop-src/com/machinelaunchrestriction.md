---
title: MachineLaunchRestriction
description: 設定元件啟動和啟用的全電腦限制原則。
ms.assetid: 274e3d08-1f38-4179-b7e7-b218d6e184ee
keywords:
- MachineLaunchRestriction 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14dfcfe5535871c6b5b0fe310c94b920c522f05a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184009"
---
# <a name="machinelaunchrestriction"></a><span data-ttu-id="55b8f-104">MachineLaunchRestriction</span><span class="sxs-lookup"><span data-stu-id="55b8f-104">MachineLaunchRestriction</span></span>

<span data-ttu-id="55b8f-105">設定元件啟動和啟用的全電腦限制原則。</span><span class="sxs-lookup"><span data-stu-id="55b8f-105">Sets the computer-wide restriction policy for component launch and activation.</span></span>

> [!Caution]  
> <span data-ttu-id="55b8f-106">變更這個值將會影響所有的 COM 伺服器應用程式，而且可能會讓它們無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="55b8f-106">Changing this value will affect all COM server applications, and might prevent them from working properly.</span></span> <span data-ttu-id="55b8f-107">如果有 COM 伺服器應用程式的限制低於全電腦限制，則減少整個電腦的限制可能會將這些應用程式公開給不必要的存取。</span><span class="sxs-lookup"><span data-stu-id="55b8f-107">If there are COM server applications that have restrictions that are less stringent than the computer-wide restrictions, reducing the computer-wide restrictions may expose these applications to unwanted access.</span></span> <span data-ttu-id="55b8f-108">相反地，如果您增加全電腦的限制，則呼叫應用程式可能無法再存取某些 COM 伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="55b8f-108">Conversely, if you increase the computer-wide restrictions, some COM server applications might no longer be accessible by calling applications.</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="55b8f-109">登錄項目</span><span class="sxs-lookup"><span data-stu-id="55b8f-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineLaunchRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a><span data-ttu-id="55b8f-110">備註</span><span class="sxs-lookup"><span data-stu-id="55b8f-110">Remarks</span></span>

<span data-ttu-id="55b8f-111">這是 **REG \_ 二進位** 值。</span><span class="sxs-lookup"><span data-stu-id="55b8f-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="55b8f-112">如果主體未授與許可權，則無法取得它們，即使許可權是由 [DefaultAccessPermission](defaultaccesspermission.md) 登錄值或 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 函數授與。</span><span class="sxs-lookup"><span data-stu-id="55b8f-112">Principals not given permissions here cannot obtain them even if the permissions are granted by the [DefaultAccessPermission](defaultaccesspermission.md) registry value or by the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function.</span></span>

<span data-ttu-id="55b8f-113">依預設，系統管理員可以取得本機和遠端啟動和啟用許可權，而 Everyone 群組的成員可能會取得本機啟用和啟動許可權。</span><span class="sxs-lookup"><span data-stu-id="55b8f-113">By default, administrators may obtain local and remote launch and activation permissions, and members of the Everyone group may obtain local activation and launch permissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55b8f-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="55b8f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55b8f-115">設定 COM 應用程式的安全性</span><span class="sxs-lookup"><span data-stu-id="55b8f-115">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




