---
title: BypassNegotiation
description: BypassNegotiation 登錄機碼會判斷伺服器和用戶端之間是否有功能協商，或是否使用預先設定的設定。
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fdf883249fc5af7a37be83bb153a670295ba1d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104374027"
---
# <a name="bypassnegotiation"></a><span data-ttu-id="9eac2-103">BypassNegotiation</span><span class="sxs-lookup"><span data-stu-id="9eac2-103">BypassNegotiation</span></span>

<span data-ttu-id="9eac2-104">BypassNegotiation 登錄機碼會判斷伺服器和用戶端之間是否有功能協商，或是否使用預先設定的設定。</span><span class="sxs-lookup"><span data-stu-id="9eac2-104">The BypassNegotiation registry key determines if capabilities negotiation between the server and client occurs or if pre-configured settings are used.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="9eac2-105">登錄項目</span><span class="sxs-lookup"><span data-stu-id="9eac2-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   BypassNegotiation = value
```

## <a name="remarks"></a><span data-ttu-id="9eac2-106">備註</span><span class="sxs-lookup"><span data-stu-id="9eac2-106">Remarks</span></span>

<span data-ttu-id="9eac2-107">這是 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="9eac2-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="9eac2-108">值</span><span class="sxs-lookup"><span data-stu-id="9eac2-108">Value</span></span>   | <span data-ttu-id="9eac2-109">描述</span><span class="sxs-lookup"><span data-stu-id="9eac2-109">Description</span></span>                                                                                                                                                                                          |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eac2-110">0</span><span class="sxs-lookup"><span data-stu-id="9eac2-110">0</span></span>       | <span data-ttu-id="9eac2-111">伺服器和用戶端會協商 EAP 功能。</span><span class="sxs-lookup"><span data-stu-id="9eac2-111">Server and client negotiate EAP capabilities.</span></span>                                                                                                                                                        |
| <span data-ttu-id="9eac2-112">零</span><span class="sxs-lookup"><span data-stu-id="9eac2-112">nonzero</span></span> | <span data-ttu-id="9eac2-113">伺服器和用戶端不會協調 EAP 功能。</span><span class="sxs-lookup"><span data-stu-id="9eac2-113">Server and client do not negotiate EAP capabilities.</span></span> <span data-ttu-id="9eac2-114">伺服器和用戶端會使用 [AssumePhase2Fragmentation](assumephase2fragmentation.md) 登錄機碼值來尋找另一方的功能。</span><span class="sxs-lookup"><span data-stu-id="9eac2-114">Server and client use the [AssumePhase2Fragmentation](assumephase2fragmentation.md) registry key value to find the other party's capabilities.</span></span> |



 

<span data-ttu-id="9eac2-115">如果此登錄值不存在，伺服器和用戶端會協商 EAP 功能。</span><span class="sxs-lookup"><span data-stu-id="9eac2-115">If this registry value is not present, the server and client negotiate EAP capabilities..</span></span>

## <a name="related-topics"></a><span data-ttu-id="9eac2-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="9eac2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9eac2-117">EAPHost 登錄設定</span><span class="sxs-lookup"><span data-stu-id="9eac2-117">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




