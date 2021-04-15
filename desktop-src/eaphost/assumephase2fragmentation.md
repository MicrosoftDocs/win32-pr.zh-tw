---
title: AssumePhase2Fragmentation
description: AssumePhase2Fragmentation 登錄機碼會判斷伺服器和用戶端是否採用階段2片段。
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0fa35692ec3ac741e2bd2fdb43607dfe1cb948
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104373991"
---
# <a name="assumephase2fragmentation"></a><span data-ttu-id="47e55-103">AssumePhase2Fragmentation</span><span class="sxs-lookup"><span data-stu-id="47e55-103">AssumePhase2Fragmentation</span></span>

<span data-ttu-id="47e55-104">AssumePhase2Fragmentation 登錄機碼會判斷伺服器和用戶端是否採用階段2片段。</span><span class="sxs-lookup"><span data-stu-id="47e55-104">The AssumePhase2Fragmentation registry key determines if the server and client assume phase 2 fragmentation.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="47e55-105">登錄項目</span><span class="sxs-lookup"><span data-stu-id="47e55-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a><span data-ttu-id="47e55-106">備註</span><span class="sxs-lookup"><span data-stu-id="47e55-106">Remarks</span></span>

<span data-ttu-id="47e55-107">這是 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="47e55-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="47e55-108">值</span><span class="sxs-lookup"><span data-stu-id="47e55-108">Value</span></span>   | <span data-ttu-id="47e55-109">描述</span><span class="sxs-lookup"><span data-stu-id="47e55-109">Description</span></span>                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47e55-110">0</span><span class="sxs-lookup"><span data-stu-id="47e55-110">0</span></span>       | <span data-ttu-id="47e55-111">伺服器和用戶端假設在 PEAP 驗證期間，另一方無法進行第2階段的片段。</span><span class="sxs-lookup"><span data-stu-id="47e55-111">Server and client assume the other party is not capable of phase 2 fragmentation during PEAP authentication.</span></span> |
| <span data-ttu-id="47e55-112">零</span><span class="sxs-lookup"><span data-stu-id="47e55-112">nonzero</span></span> | <span data-ttu-id="47e55-113">伺服器和用戶端會假設另一方在 PEAP 驗證期間可以有階段2的片段。</span><span class="sxs-lookup"><span data-stu-id="47e55-113">Server and client assume the other party is capable of phase 2 fragmentation during PEAP authentication.</span></span>     |



 

<span data-ttu-id="47e55-114">如果此登錄值不存在，則伺服器和用戶端會假設另一個合作物件能夠在 PEAP 驗證期間進行階段2片段化。</span><span class="sxs-lookup"><span data-stu-id="47e55-114">If this registry value is not present, the server and client assume the other party is capable of phase 2 fragmentation during PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47e55-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="47e55-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47e55-116">EAPHost 登錄設定</span><span class="sxs-lookup"><span data-stu-id="47e55-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




