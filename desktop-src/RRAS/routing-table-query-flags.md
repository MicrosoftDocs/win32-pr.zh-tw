---
title: 路由表查詢旗標
description: 將這些常數用於路由器資料表查詢。
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- 路由表查詢旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37ab647efb192e29aae421e02bef1dec065e3b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840911"
---
# <a name="routing-table-query-flags"></a><span data-ttu-id="41304-104">路由表查詢旗標</span><span class="sxs-lookup"><span data-stu-id="41304-104">Routing Table Query Flags</span></span>

<span data-ttu-id="41304-105">將這些常數用於路由器資料表查詢。</span><span class="sxs-lookup"><span data-stu-id="41304-105">Use these constants for router table queries.</span></span>



| <span data-ttu-id="41304-106">常數</span><span class="sxs-lookup"><span data-stu-id="41304-106">Constant</span></span>              | <span data-ttu-id="41304-107">值</span><span class="sxs-lookup"><span data-stu-id="41304-107">Value</span></span>      | <span data-ttu-id="41304-108">描述</span><span class="sxs-lookup"><span data-stu-id="41304-108">Description</span></span>                                                                |
|-----------------------|------------|----------------------------------------------------------------------------|
| <span data-ttu-id="41304-109">RTM \_ 相符項 \_ 無</span><span class="sxs-lookup"><span data-stu-id="41304-109">RTM\_MATCH\_NONE</span></span>      | <span data-ttu-id="41304-110">0x00000000</span><span class="sxs-lookup"><span data-stu-id="41304-110">0x00000000</span></span> | <span data-ttu-id="41304-111">不符合任何準則;系統會傳回目的地的所有路由。</span><span class="sxs-lookup"><span data-stu-id="41304-111">Matches none of the criteria; all routes for the destination are returned.</span></span> |
| <span data-ttu-id="41304-112">RTM \_ 相符的 \_ 擁有者</span><span class="sxs-lookup"><span data-stu-id="41304-112">RTM\_MATCH\_OWNER</span></span>     | <span data-ttu-id="41304-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="41304-113">0x00000001</span></span> | <span data-ttu-id="41304-114">與相同擁有者的路由相符。</span><span class="sxs-lookup"><span data-stu-id="41304-114">Matches routes with same owner.</span></span>                                            |
| <span data-ttu-id="41304-115">RTM \_ 相符 \_ NEIGHBOUR</span><span class="sxs-lookup"><span data-stu-id="41304-115">RTM\_MATCH\_NEIGHBOUR</span></span> | <span data-ttu-id="41304-116">0x00000002</span><span class="sxs-lookup"><span data-stu-id="41304-116">0x00000002</span></span> | <span data-ttu-id="41304-117">符合相同鄰近的路由。</span><span class="sxs-lookup"><span data-stu-id="41304-117">Matches routes with the same neighbor.</span></span>                                     |
| <span data-ttu-id="41304-118">RTM \_ 相符 \_ PREF</span><span class="sxs-lookup"><span data-stu-id="41304-118">RTM\_MATCH\_PREF</span></span>      | <span data-ttu-id="41304-119">0x00000004</span><span class="sxs-lookup"><span data-stu-id="41304-119">0x00000004</span></span> | <span data-ttu-id="41304-120">符合具有相同喜好設定的路由。</span><span class="sxs-lookup"><span data-stu-id="41304-120">Matches routes that have the same preference.</span></span>                              |
| <span data-ttu-id="41304-121">RTM \_ 符合 \_ NEXTHOP</span><span class="sxs-lookup"><span data-stu-id="41304-121">RTM\_MATCH\_NEXTHOP</span></span>   | <span data-ttu-id="41304-122">0x00000008</span><span class="sxs-lookup"><span data-stu-id="41304-122">0x00000008</span></span> | <span data-ttu-id="41304-123">符合具有相同下一個躍點的路由。</span><span class="sxs-lookup"><span data-stu-id="41304-123">Matches routes that have the same next hop.</span></span>                                |
| <span data-ttu-id="41304-124">RTM \_ 相符 \_ 介面</span><span class="sxs-lookup"><span data-stu-id="41304-124">RTM\_MATCH\_INTERFACE</span></span> | <span data-ttu-id="41304-125">0x00000010</span><span class="sxs-lookup"><span data-stu-id="41304-125">0x00000010</span></span> | <span data-ttu-id="41304-126">符合相同介面上的路由。</span><span class="sxs-lookup"><span data-stu-id="41304-126">Matches routes that are on the same interface.</span></span>                             |
| <span data-ttu-id="41304-127">RTM \_ \_ 完全相符</span><span class="sxs-lookup"><span data-stu-id="41304-127">RTM\_MATCH\_FULL</span></span>      | <span data-ttu-id="41304-128">0x0000FFFF</span><span class="sxs-lookup"><span data-stu-id="41304-128">0x0000FFFF</span></span> | <span data-ttu-id="41304-129">符合所有準則的路由。</span><span class="sxs-lookup"><span data-stu-id="41304-129">Matches routes with all criteria.</span></span>                                          |
| <span data-ttu-id="41304-130">RTM \_ 最佳 \_ 通訊協定</span><span class="sxs-lookup"><span data-stu-id="41304-130">RTM\_BEST\_PROTOCOL</span></span>   | <span data-ttu-id="41304-131">0</span><span class="sxs-lookup"><span data-stu-id="41304-131">0</span></span>          | <span data-ttu-id="41304-132">傳回路由，不論哪一個通訊協定擁有它。</span><span class="sxs-lookup"><span data-stu-id="41304-132">Returns a route regardless of which protocol owns it.</span></span>                      |
| <span data-ttu-id="41304-133">RTM \_ 此 \_ 通訊協定</span><span class="sxs-lookup"><span data-stu-id="41304-133">RTM\_THIS\_PROTOCOL</span></span>   | <span data-ttu-id="41304-134">~0</span><span class="sxs-lookup"><span data-stu-id="41304-134">~0</span></span>         | <span data-ttu-id="41304-135">傳回呼叫通訊協定的最佳路由。</span><span class="sxs-lookup"><span data-stu-id="41304-135">Returns the best route for the calling protocol.</span></span>                           |



 

 

 




