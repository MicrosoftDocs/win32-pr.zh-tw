---
title: EnableDCOM
description: 控制電腦的全域啟用和呼叫原則。 只有系統管理員和系統才能完整存取登錄的這個部分。 所有其他使用者都具有唯讀存取權。
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- EnableDCOM 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42cc95b24522e87e4b64f6feefc5c6c56ad5341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372034"
---
# <a name="enabledcom"></a><span data-ttu-id="53b9a-106">EnableDCOM</span><span class="sxs-lookup"><span data-stu-id="53b9a-106">EnableDCOM</span></span>

<span data-ttu-id="53b9a-107">控制電腦的全域啟用和呼叫原則。</span><span class="sxs-lookup"><span data-stu-id="53b9a-107">Controls the global activation and call policies of the machine.</span></span> <span data-ttu-id="53b9a-108">只有系統管理員和系統才能完整存取登錄的這個部分。</span><span class="sxs-lookup"><span data-stu-id="53b9a-108">Only administrators and the system have full access to this portion of the registry.</span></span> <span data-ttu-id="53b9a-109">所有其他使用者都具有唯讀存取權。</span><span class="sxs-lookup"><span data-stu-id="53b9a-109">All other users have read-only access.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="53b9a-110">登錄項目</span><span class="sxs-lookup"><span data-stu-id="53b9a-110">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a><span data-ttu-id="53b9a-111">備註</span><span class="sxs-lookup"><span data-stu-id="53b9a-111">Remarks</span></span>

<span data-ttu-id="53b9a-112">這是 **REG \_ SZ** 值。</span><span class="sxs-lookup"><span data-stu-id="53b9a-112">This is a **REG\_SZ** value.</span></span>



| <span data-ttu-id="53b9a-113">值</span><span class="sxs-lookup"><span data-stu-id="53b9a-113">Value</span></span>    | <span data-ttu-id="53b9a-114">描述</span><span class="sxs-lookup"><span data-stu-id="53b9a-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53b9a-115">N (或 n) </span><span class="sxs-lookup"><span data-stu-id="53b9a-115">N (or n)</span></span> | <span data-ttu-id="53b9a-116">沒有任何遠端用戶端可以啟動伺服器或連接到這部電腦上的物件。</span><span class="sxs-lookup"><span data-stu-id="53b9a-116">No remote clients may launch servers or connect to objects on this computer.</span></span> <span data-ttu-id="53b9a-117">本機用戶端無法存取遠端 DCOM 伺服器;封鎖所有 DCOM 流量。</span><span class="sxs-lookup"><span data-stu-id="53b9a-117">Local clients cannot access remote DCOM servers; all DCOM traffic is blocked.</span></span> <span data-ttu-id="53b9a-118">根據類別的 [**LaunchPermission**](launchpermission.md) 登錄值和 global [**DefaultLaunchPermission**](defaultlaunchpermission.md) 登錄值的值和存取權限，每個類別都允許對類別程式碼的本機啟動，並連接到物件。</span><span class="sxs-lookup"><span data-stu-id="53b9a-118">Local launching of class code and connecting to objects are allowed on a per-class basis according to the value and access permissions of the class's [**LaunchPermission**](launchpermission.md) registry value and the global [**DefaultLaunchPermission**](defaultlaunchpermission.md) registry value.</span></span> |
| <span data-ttu-id="53b9a-119">Y (或 y) </span><span class="sxs-lookup"><span data-stu-id="53b9a-119">Y (or y)</span></span> | <span data-ttu-id="53b9a-120">根據類別的 [**LaunchPermission**](launchpermission.md) 登錄值和 global [**DefaultLaunchPermission**](defaultlaunchpermission.md) 登錄值的值和存取權限，每個類別都允許啟動伺服器並連接至物件。</span><span class="sxs-lookup"><span data-stu-id="53b9a-120">Launching of servers and connecting to objects by remote clients is allowed on a per-class basis according to the value and access permissions of the class's [**LaunchPermission**](launchpermission.md) registry value and the global [**DefaultLaunchPermission**](defaultlaunchpermission.md) registry value.</span></span>                                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="53b9a-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="53b9a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53b9a-122">**DefaultLaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="53b9a-122">**DefaultLaunchPermission**</span></span>](defaultlaunchpermission.md)
</dt> <dt>

[<span data-ttu-id="53b9a-123">**LaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="53b9a-123">**LaunchPermission**</span></span>](launchpermission.md)
</dt> <dt>

[<span data-ttu-id="53b9a-124">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="53b9a-124">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




