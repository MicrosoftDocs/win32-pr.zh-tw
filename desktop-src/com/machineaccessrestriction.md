---
title: MachineAccessRestriction
description: 針對元件存取設定整個電腦的限制原則。
ms.assetid: aeb37e49-6425-4058-968e-f9d00acf4fc2
keywords:
- MachineAccessRestriction 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d99e747b8a38dbb41cb8a6a8adc0935d3f9fa8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966813"
---
# <a name="machineaccessrestriction"></a><span data-ttu-id="fa3cb-104">MachineAccessRestriction</span><span class="sxs-lookup"><span data-stu-id="fa3cb-104">MachineAccessRestriction</span></span>

<span data-ttu-id="fa3cb-105">針對元件存取設定整個電腦的限制原則。</span><span class="sxs-lookup"><span data-stu-id="fa3cb-105">Sets the computer-wide restriction policy for component access.</span></span>

> [!Caution]  
> <span data-ttu-id="fa3cb-106">變更這個值將會影響所有的 COM 伺服器應用程式，而且可能會讓它們無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="fa3cb-106">Changing this value will affect all COM server applications, and might prevent them from working properly.</span></span> <span data-ttu-id="fa3cb-107">如果有 COM 伺服器應用程式的限制低於全電腦限制，則減少整個電腦的限制可能會將這些應用程式公開給不必要的存取。</span><span class="sxs-lookup"><span data-stu-id="fa3cb-107">If there are COM server applications that have restrictions that are less stringent than the computer-wide restrictions, reducing the computer-wide restrictions may expose these applications to unwanted access.</span></span> <span data-ttu-id="fa3cb-108">相反地，如果您增加全電腦的限制，則呼叫應用程式可能無法再存取某些 COM 伺服器應用程式。</span><span class="sxs-lookup"><span data-stu-id="fa3cb-108">Conversely, if you increase the computer-wide restrictions, some COM server applications might no longer be accessible by calling applications.</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="fa3cb-109">登錄項目</span><span class="sxs-lookup"><span data-stu-id="fa3cb-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineAccessRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a><span data-ttu-id="fa3cb-110">備註</span><span class="sxs-lookup"><span data-stu-id="fa3cb-110">Remarks</span></span>

<span data-ttu-id="fa3cb-111">這是 **REG \_ 二進位** 值。</span><span class="sxs-lookup"><span data-stu-id="fa3cb-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="fa3cb-112">如果主體未授與許可權，則無法取得它們，即使許可權是由 [DefaultAccessPermission](defaultaccesspermission.md) 登錄值或 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 函數授與。</span><span class="sxs-lookup"><span data-stu-id="fa3cb-112">Principals not given permissions here cannot obtain them even if the permissions are granted by the [DefaultAccessPermission](defaultaccesspermission.md) registry value or by the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function.</span></span>

<span data-ttu-id="fa3cb-113">依預設，Everyone 群組的成員可以取得本機和遠端存取許可權，而且匿名使用者可以取得本機存取權限。</span><span class="sxs-lookup"><span data-stu-id="fa3cb-113">By default, members of the Everyone group can obtain local and remote access permissions, and anonymous users can obtain local access permissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa3cb-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa3cb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa3cb-115">設定 COM 應用程式的安全性</span><span class="sxs-lookup"><span data-stu-id="fa3cb-115">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




