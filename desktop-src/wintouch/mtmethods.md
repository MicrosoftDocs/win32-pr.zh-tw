---
title: '方法 (IManipulationProcessor) '
description: 本節包含 IManipulationProcessor 介面的方法。
ms.assetid: 33736f79-cb61-449c-80b9-1358db2621e9
keywords:
- Windows Touch，IManipulationProcessor 介面
- Windows Touch，介面方法
- 操作，IManipulationProcessor 介面
- IManipulationProcessor 介面，方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 995a848e18b8308d46ceda717bf7eec291953505
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383689"
---
# <a name="methods-imanipulationprocessor"></a><span data-ttu-id="81fbf-107">方法 (IManipulationProcessor) </span><span class="sxs-lookup"><span data-stu-id="81fbf-107">Methods (IManipulationProcessor)</span></span>

<span data-ttu-id="81fbf-108">本節包含 [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) 介面的方法。</span><span class="sxs-lookup"><span data-stu-id="81fbf-108">This section contains the methods for the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>

<span data-ttu-id="81fbf-109">[**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)介面會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="81fbf-109">The following methods are exposed by the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>



| <span data-ttu-id="81fbf-110">方法</span><span class="sxs-lookup"><span data-stu-id="81fbf-110">Method</span></span>                                                                      | <span data-ttu-id="81fbf-111">描述</span><span class="sxs-lookup"><span data-stu-id="81fbf-111">Description</span></span>                                                                              |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81fbf-112">**CompleteManipulation**</span><span class="sxs-lookup"><span data-stu-id="81fbf-112">**CompleteManipulation**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-completemanipulation) | <span data-ttu-id="81fbf-113">當開發人員選擇結束操作時，就會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="81fbf-113">This method is called when the developer chooses to end the manipulation.</span></span>                |
| [<span data-ttu-id="81fbf-114">**GetAngularVelocity**</span><span class="sxs-lookup"><span data-stu-id="81fbf-114">**GetAngularVelocity**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getangularvelocity)     | <span data-ttu-id="81fbf-115">計算目標物件正在移動的旋轉速度。</span><span class="sxs-lookup"><span data-stu-id="81fbf-115">Calculates the rotational velocity that the target object is moving at.</span></span>                  |
| [<span data-ttu-id="81fbf-116">**GetExpansionVelocity**</span><span class="sxs-lookup"><span data-stu-id="81fbf-116">**GetExpansionVelocity**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getexpansionvelocity) | <span data-ttu-id="81fbf-117">計算目標物件正在擴充的速率。</span><span class="sxs-lookup"><span data-stu-id="81fbf-117">Calculates the rate that the target object is expanding at.</span></span>                              |
| [<span data-ttu-id="81fbf-118">**GetVelocityX**</span><span class="sxs-lookup"><span data-stu-id="81fbf-118">**GetVelocityX**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityx)                 | <span data-ttu-id="81fbf-119">計算並傳回目標物件的水準速度。</span><span class="sxs-lookup"><span data-stu-id="81fbf-119">Calculates and returns the horizontal velocity for the target object.</span></span>                    |
| [<span data-ttu-id="81fbf-120">**GetVelocityY**</span><span class="sxs-lookup"><span data-stu-id="81fbf-120">**GetVelocityY**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityy)                 | <span data-ttu-id="81fbf-121">計算並傳回垂直速度。</span><span class="sxs-lookup"><span data-stu-id="81fbf-121">Calculates and returns the vertical velocity.</span></span>                                            |
| [<span data-ttu-id="81fbf-122">**ProcessDown**</span><span class="sxs-lookup"><span data-stu-id="81fbf-122">**ProcessDown**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdown)                   | <span data-ttu-id="81fbf-123">將資料摘要至與目標相關聯的操作處理器。</span><span class="sxs-lookup"><span data-stu-id="81fbf-123">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="81fbf-124">**ProcessMove**</span><span class="sxs-lookup"><span data-stu-id="81fbf-124">**ProcessMove**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmove)                   | <span data-ttu-id="81fbf-125">將資料摘要至與目標相關聯的操作處理器。</span><span class="sxs-lookup"><span data-stu-id="81fbf-125">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="81fbf-126">**ProcessUp**</span><span class="sxs-lookup"><span data-stu-id="81fbf-126">**ProcessUp**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processup)                       | <span data-ttu-id="81fbf-127">將資料摘要至與目標相關聯的操作處理器。</span><span class="sxs-lookup"><span data-stu-id="81fbf-127">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="81fbf-128">**ProcessDownWithTime**</span><span class="sxs-lookup"><span data-stu-id="81fbf-128">**ProcessDownWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)   | <span data-ttu-id="81fbf-129">將資料（包括時間戳記）饋送至與目標相關聯的操作處理器。</span><span class="sxs-lookup"><span data-stu-id="81fbf-129">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |
| [<span data-ttu-id="81fbf-130">**ProcessMoveWithTime**</span><span class="sxs-lookup"><span data-stu-id="81fbf-130">**ProcessMoveWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime)   | <span data-ttu-id="81fbf-131">將資料（包括時間戳記）饋送至與目標相關聯的操作處理器。</span><span class="sxs-lookup"><span data-stu-id="81fbf-131">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |
| [<span data-ttu-id="81fbf-132">**ProcessUpWithTime**</span><span class="sxs-lookup"><span data-stu-id="81fbf-132">**ProcessUpWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime)       | <span data-ttu-id="81fbf-133">將資料（包括時間戳記）饋送至與目標相關聯的操作處理器。</span><span class="sxs-lookup"><span data-stu-id="81fbf-133">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="81fbf-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="81fbf-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81fbf-135">**IManipulationProcessor**</span><span class="sxs-lookup"><span data-stu-id="81fbf-135">**IManipulationProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




