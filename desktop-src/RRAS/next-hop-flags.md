---
title: 下一個躍點旗標
description: 下一個躍點旗標
ms.assetid: e4c7e9ea-21f5-491a-b005-1ef1a457cb80
keywords:
- 下一個
- 下一個躍點旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd672c9b083e47c3d0a7419d03ab890c1037ce5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021934"
---
# <a name="next-hop-flags"></a><span data-ttu-id="9b5bc-105">下一個躍點旗標</span><span class="sxs-lookup"><span data-stu-id="9b5bc-105">Next Hop Flags</span></span>

## <a name="next-hop-state-flags"></a><span data-ttu-id="9b5bc-106">下一個躍點狀態旗標</span><span class="sxs-lookup"><span data-stu-id="9b5bc-106">Next Hop State Flags</span></span>



| <span data-ttu-id="9b5bc-107">常數</span><span class="sxs-lookup"><span data-stu-id="9b5bc-107">Constant</span></span>                     | <span data-ttu-id="9b5bc-108">值</span><span class="sxs-lookup"><span data-stu-id="9b5bc-108">Value</span></span> | <span data-ttu-id="9b5bc-109">描述</span><span class="sxs-lookup"><span data-stu-id="9b5bc-109">Description</span></span>                              |
|------------------------------|-------|------------------------------------------|
| <span data-ttu-id="9b5bc-110">已 \_ 建立 RTM NEXTHOP \_ 狀態 \_</span><span class="sxs-lookup"><span data-stu-id="9b5bc-110">RTM\_NEXTHOP\_STATE\_CREATED</span></span> | <span data-ttu-id="9b5bc-111">0</span><span class="sxs-lookup"><span data-stu-id="9b5bc-111">0</span></span>     | <span data-ttu-id="9b5bc-112">指出已建立下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="9b5bc-112">Indicates that the next hop was created.</span></span> |
| <span data-ttu-id="9b5bc-113">\_ \_ 已刪除 RTM NEXTHOP 狀態 \_</span><span class="sxs-lookup"><span data-stu-id="9b5bc-113">RTM\_NEXTHOP\_STATE\_DELETED</span></span> | <span data-ttu-id="9b5bc-114">1</span><span class="sxs-lookup"><span data-stu-id="9b5bc-114">1</span></span>     | <span data-ttu-id="9b5bc-115">表示已刪除下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="9b5bc-115">Indicates that the next hop was deleted.</span></span> |



 

## <a name="next-hop-flags"></a><span data-ttu-id="9b5bc-116">下一個躍點旗標</span><span class="sxs-lookup"><span data-stu-id="9b5bc-116">Next Hop Flags</span></span>



| <span data-ttu-id="9b5bc-117">常數</span><span class="sxs-lookup"><span data-stu-id="9b5bc-117">Constant</span></span>                    | <span data-ttu-id="9b5bc-118">值</span><span class="sxs-lookup"><span data-stu-id="9b5bc-118">Value</span></span>  | <span data-ttu-id="9b5bc-119">描述</span><span class="sxs-lookup"><span data-stu-id="9b5bc-119">Description</span></span>                                                                                                                                           |
|-----------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b5bc-120">RTM \_ NEXTHOP \_ 旗標 \_ 遠端</span><span class="sxs-lookup"><span data-stu-id="9b5bc-120">RTM\_NEXTHOP\_FLAGS\_REMOTE</span></span> | <span data-ttu-id="9b5bc-121">0x0001</span><span class="sxs-lookup"><span data-stu-id="9b5bc-121">0x0001</span></span> | <span data-ttu-id="9b5bc-122">這個下一個躍點指向無法直接連線的遠端目的地。</span><span class="sxs-lookup"><span data-stu-id="9b5bc-122">This next hop points to a remote destination that is not directly reachable.</span></span> <span data-ttu-id="9b5bc-123">若要取得完整的路徑，用戶端必須執行遞迴查閱。</span><span class="sxs-lookup"><span data-stu-id="9b5bc-123">To obtain the complete path, the client must perform a recursive lookup.</span></span> |
| <span data-ttu-id="9b5bc-124">RTM \_ NEXTHOP \_ 旗標 \_ 關閉</span><span class="sxs-lookup"><span data-stu-id="9b5bc-124">RTM\_NEXTHOP\_FLAGS\_DOWN</span></span>   | <span data-ttu-id="9b5bc-125">0x0002</span><span class="sxs-lookup"><span data-stu-id="9b5bc-125">0x0002</span></span> | <span data-ttu-id="9b5bc-126">此旗標已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="9b5bc-126">This flag is reserved for future use.</span></span>                                                                                                                 |



 

## <a name="next-hop-added"></a><span data-ttu-id="9b5bc-127">新增下一個躍點</span><span class="sxs-lookup"><span data-stu-id="9b5bc-127">Next Hop Added</span></span>



| <span data-ttu-id="9b5bc-128">常數</span><span class="sxs-lookup"><span data-stu-id="9b5bc-128">Constant</span></span>                  | <span data-ttu-id="9b5bc-129">值</span><span class="sxs-lookup"><span data-stu-id="9b5bc-129">Value</span></span> | <span data-ttu-id="9b5bc-130">描述</span><span class="sxs-lookup"><span data-stu-id="9b5bc-130">Description</span></span>                 |
|---------------------------|-------|-----------------------------|
| <span data-ttu-id="9b5bc-131">RTM \_ NEXTHOP \_ 變更 \_ 新增</span><span class="sxs-lookup"><span data-stu-id="9b5bc-131">RTM\_NEXTHOP\_CHANGE\_NEW</span></span> | <span data-ttu-id="9b5bc-132">0x01</span><span class="sxs-lookup"><span data-stu-id="9b5bc-132">0x01</span></span>  | <span data-ttu-id="9b5bc-133">已建立新的下一個躍點。</span><span class="sxs-lookup"><span data-stu-id="9b5bc-133">A new next hop was created.</span></span> |



 

 

 




