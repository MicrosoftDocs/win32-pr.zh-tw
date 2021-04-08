---
title: SRPRunningObjectChecks
description: 決定是否要針對相容的軟體限制原則（ (SRP) 信任層級）篩選連接到執行中物件的嘗試。
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- SRPRunningObjectChecks 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad307856bcfdd30cfaa6c731551ac6570d2bec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672487"
---
# <a name="srprunningobjectchecks"></a><span data-ttu-id="fd9c2-104">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="fd9c2-104">SRPRunningObjectChecks</span></span>

<span data-ttu-id="fd9c2-105">決定是否要針對相容的軟體限制原則（ (SRP) 信任層級）篩選連接到執行中物件的嘗試。</span><span class="sxs-lookup"><span data-stu-id="fd9c2-105">Determines whether attempts to connect to running objects are screened for compatible software restriction policy (SRP) trust levels.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="fd9c2-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="fd9c2-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a><span data-ttu-id="fd9c2-107">備註</span><span class="sxs-lookup"><span data-stu-id="fd9c2-107">Remarks</span></span>

<span data-ttu-id="fd9c2-108">這是 **REG \_ SZ** 值。</span><span class="sxs-lookup"><span data-stu-id="fd9c2-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="fd9c2-109">字串值 {N，N，NO，No，no} 表示不會針對相容的 SRP 信任層級篩選連接到執行物件的嘗試。</span><span class="sxs-lookup"><span data-stu-id="fd9c2-109">String values of {N, n, NO, No, no} indicate that attempts to connect to running objects are not screened for compatible SRP trust levels.</span></span> <span data-ttu-id="fd9c2-110">如果此登錄值設定為任何其他值或不存在，則執行中的物件不能有比用戶端物件更嚴格的 SRP 信任層級。</span><span class="sxs-lookup"><span data-stu-id="fd9c2-110">If this registry value is set to any other value or does not exist, the running object cannot have a less stringent SRP trust level than the client object.</span></span> <span data-ttu-id="fd9c2-111">例如，如果用戶端物件具有不受限制的信任層級，則執行中的物件不能有不允許的信任層級。</span><span class="sxs-lookup"><span data-stu-id="fd9c2-111">For example, the running object cannot have a Disallowed trust level if the client object has an Unrestricted trust level.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd9c2-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="fd9c2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd9c2-113">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="fd9c2-113">SRPTrustLevel</span></span>](srptrustlevel.md)
</dt> </dl>

 

 




