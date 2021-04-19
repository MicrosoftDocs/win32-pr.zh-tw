---
title: 視圖旗標
description: 使用視圖旗標來控制路由表的流覽。
ms.assetid: 836e3400-0dca-4a21-9a5c-7da357ed72ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5192bf3e1acaa91412d8ae7e06d035e54af1ece6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "107001269"
---
# <a name="view-flags"></a><span data-ttu-id="1ec32-103">視圖旗標</span><span class="sxs-lookup"><span data-stu-id="1ec32-103">View Flags</span></span>

<span data-ttu-id="1ec32-104">使用視圖旗標來控制路由表的流覽。</span><span class="sxs-lookup"><span data-stu-id="1ec32-104">Use the View Flags to control routing table views.</span></span>



| <span data-ttu-id="1ec32-105">常數</span><span class="sxs-lookup"><span data-stu-id="1ec32-105">Constant</span></span>                 | <span data-ttu-id="1ec32-106">值</span><span class="sxs-lookup"><span data-stu-id="1ec32-106">Value</span></span>      | <span data-ttu-id="1ec32-107">描述</span><span class="sxs-lookup"><span data-stu-id="1ec32-107">Description</span></span>                                                      |
|--------------------------|------------|------------------------------------------------------------------|
| <span data-ttu-id="1ec32-108">RTM \_ \_ 位址 \_ 大小上限</span><span class="sxs-lookup"><span data-stu-id="1ec32-108">RTM\_MAX \_ADDRESS\_SIZE</span></span> | <span data-ttu-id="1ec32-109">16</span><span class="sxs-lookup"><span data-stu-id="1ec32-109">16</span></span>         | <span data-ttu-id="1ec32-110">位址系列的位址大小上限。</span><span class="sxs-lookup"><span data-stu-id="1ec32-110">Max address size for an address family.</span></span>                          |
| <span data-ttu-id="1ec32-111">RTM \_ 最大 \_ 視圖</span><span class="sxs-lookup"><span data-stu-id="1ec32-111">RTM\_MAX\_VIEWS</span></span>          | <span data-ttu-id="1ec32-112">32</span><span class="sxs-lookup"><span data-stu-id="1ec32-112">32</span></span>         | <span data-ttu-id="1ec32-113">路由表中可處於作用中狀態的最大視圖數目。</span><span class="sxs-lookup"><span data-stu-id="1ec32-113">Maximum number of views that can be active in the routing table.</span></span> |
| <span data-ttu-id="1ec32-114">RTM \_ 視圖 \_ 識別碼 \_ UCAST</span><span class="sxs-lookup"><span data-stu-id="1ec32-114">RTM\_VIEW\_ID\_UCAST</span></span>     | <span data-ttu-id="1ec32-115">0</span><span class="sxs-lookup"><span data-stu-id="1ec32-115">0</span></span>          | <span data-ttu-id="1ec32-116">指定單播視圖。</span><span class="sxs-lookup"><span data-stu-id="1ec32-116">Specifies a unicast view.</span></span>                                        |
| <span data-ttu-id="1ec32-117">RTM \_ 視圖 \_ 識別碼 \_ MCAST</span><span class="sxs-lookup"><span data-stu-id="1ec32-117">RTM\_VIEW\_ID\_MCAST</span></span>     | <span data-ttu-id="1ec32-118">1</span><span class="sxs-lookup"><span data-stu-id="1ec32-118">1</span></span>          | <span data-ttu-id="1ec32-119">指定多播視圖。</span><span class="sxs-lookup"><span data-stu-id="1ec32-119">Specifies a multicast view.</span></span>                                      |
| <span data-ttu-id="1ec32-120">RTM \_ 視圖 \_ 遮罩 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="1ec32-120">RTM\_VIEW\_MASK\_SIZE</span></span>    | <span data-ttu-id="1ec32-121">0x20</span><span class="sxs-lookup"><span data-stu-id="1ec32-121">0x20</span></span>       | <span data-ttu-id="1ec32-122">指定可以設定的最大視圖數目。</span><span class="sxs-lookup"><span data-stu-id="1ec32-122">Specifies the maximum number of views that can be configured.</span></span>    |
| <span data-ttu-id="1ec32-123">RTM \_ 視圖 \_ 遮罩 \_ 無</span><span class="sxs-lookup"><span data-stu-id="1ec32-123">RTM\_VIEW\_MASK\_NONE</span></span>    | <span data-ttu-id="1ec32-124">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ec32-124">0x00000000</span></span> | <span data-ttu-id="1ec32-125">無論視圖為何，都會傳回信息。</span><span class="sxs-lookup"><span data-stu-id="1ec32-125">Returns information regardless of the view.</span></span>                      |
| <span data-ttu-id="1ec32-126">RTM \_ 視圖 \_ 遮罩 \_ 任何</span><span class="sxs-lookup"><span data-stu-id="1ec32-126">RTM\_VIEW\_MASK\_ANY</span></span>     | <span data-ttu-id="1ec32-127">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1ec32-127">0x00000000</span></span> | <span data-ttu-id="1ec32-128">傳回所有視圖的目的地。</span><span class="sxs-lookup"><span data-stu-id="1ec32-128">Returns destinations from all views.</span></span> <span data-ttu-id="1ec32-129">這是預設值。</span><span class="sxs-lookup"><span data-stu-id="1ec32-129">This is the default value.</span></span>  |
| <span data-ttu-id="1ec32-130">RTM \_ 視圖 \_ 遮罩 \_ UCAST</span><span class="sxs-lookup"><span data-stu-id="1ec32-130">RTM\_VIEW\_MASK\_UCAST</span></span>   | <span data-ttu-id="1ec32-131">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1ec32-131">0x00000001</span></span> | <span data-ttu-id="1ec32-132">從單播視圖傳回目的地。</span><span class="sxs-lookup"><span data-stu-id="1ec32-132">Returns destinations from the unicast view.</span></span>                      |
| <span data-ttu-id="1ec32-133">RTM \_ 視圖 \_ 遮罩 \_ MCAST</span><span class="sxs-lookup"><span data-stu-id="1ec32-133">RTM\_VIEW\_MASK\_MCAST</span></span>   | <span data-ttu-id="1ec32-134">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1ec32-134">0x00000002</span></span> | <span data-ttu-id="1ec32-135">從多播視圖傳回目的地。</span><span class="sxs-lookup"><span data-stu-id="1ec32-135">Returns destinations from the multicast view.</span></span>                    |
| <span data-ttu-id="1ec32-136">RTM \_ 視圖 \_ 遮罩 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="1ec32-136">RTM\_VIEW\_MASK\_ALL</span></span>     | <span data-ttu-id="1ec32-137">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="1ec32-137">0xFFFFFFFF</span></span> | <span data-ttu-id="1ec32-138">傳回所有視圖的資訊。</span><span class="sxs-lookup"><span data-stu-id="1ec32-138">Returns information from all views.</span></span>                              |



 

 

 




