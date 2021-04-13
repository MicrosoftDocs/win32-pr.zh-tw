---
title: 選取位元速率
description: 選取位元速率
ms.assetid: 466524a6-2473-4768-8ae3-0ac18807f88c
keywords:
- 設定檔，選擇位元速率
- 設定檔，位元速率
- 編解碼器，選擇位元速率
- 編解碼器、位元速率
- 設定檔，選取位元速率
- 編解碼器，選取位元速率
- 位元速率，選取
- 位元速率，設定檔
- 位元速率，編解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd8c125aacc5add255962ca37e6060af20d66f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104299999"
---
# <a name="selecting-bit-rates"></a><span data-ttu-id="a4e93-112">選取位元速率</span><span class="sxs-lookup"><span data-stu-id="a4e93-112">Selecting Bit Rates</span></span>

<span data-ttu-id="a4e93-113">針對將透過網路進行串流處理的檔案，您必須仔細考慮應該使用的位速度。</span><span class="sxs-lookup"><span data-stu-id="a4e93-113">For files that will be streamed over a network, you must consider carefully what bit rates you should use.</span></span> <span data-ttu-id="a4e93-114">在大多數情況下，您可以將檔案中所有資料流程的位元速率加在一起，以取得串流處理檔案所需的可用頻寬的一般概念。</span><span class="sxs-lookup"><span data-stu-id="a4e93-114">Under most circumstances you can add the bit rates of all of the streams in a file together to get a general idea of the available bandwidth required to stream the file.</span></span> <span data-ttu-id="a4e93-115">不過，每個串流也都需要特定的負荷量。</span><span class="sxs-lookup"><span data-stu-id="a4e93-115">However, a certain amount of overhead is also required for each stream.</span></span> <span data-ttu-id="a4e93-116">下表摘要說明此額外負荷。</span><span class="sxs-lookup"><span data-stu-id="a4e93-116">This overhead is summarized in the following table.</span></span>



| <span data-ttu-id="a4e93-117">位速率範圍 (Kbps) </span><span class="sxs-lookup"><span data-stu-id="a4e93-117">Bit-rate range (Kbps)</span></span> | <span data-ttu-id="a4e93-118">額外負荷 (Kbps 所需的頻寬) </span><span class="sxs-lookup"><span data-stu-id="a4e93-118">Additional bandwidth required for overhead (Kbps)</span></span> |
|-----------------------|---------------------------------------------------|
| <span data-ttu-id="a4e93-119">10–16</span><span class="sxs-lookup"><span data-stu-id="a4e93-119">10 – 16</span></span>               | <span data-ttu-id="a4e93-120">3</span><span class="sxs-lookup"><span data-stu-id="a4e93-120">3</span></span>                                                 |
| <span data-ttu-id="a4e93-121">17–30</span><span class="sxs-lookup"><span data-stu-id="a4e93-121">17 – 30</span></span>               | <span data-ttu-id="a4e93-122">4</span><span class="sxs-lookup"><span data-stu-id="a4e93-122">4</span></span>                                                 |
| <span data-ttu-id="a4e93-123">31-45</span><span class="sxs-lookup"><span data-stu-id="a4e93-123">31 – 45</span></span>               | <span data-ttu-id="a4e93-124">5</span><span class="sxs-lookup"><span data-stu-id="a4e93-124">5</span></span>                                                 |
| <span data-ttu-id="a4e93-125">46–70</span><span class="sxs-lookup"><span data-stu-id="a4e93-125">46 – 70</span></span>               | <span data-ttu-id="a4e93-126">6</span><span class="sxs-lookup"><span data-stu-id="a4e93-126">6</span></span>                                                 |
| <span data-ttu-id="a4e93-127">71–225</span><span class="sxs-lookup"><span data-stu-id="a4e93-127">71 – 225</span></span>              | <span data-ttu-id="a4e93-128">7</span><span class="sxs-lookup"><span data-stu-id="a4e93-128">7</span></span>                                                 |
| <span data-ttu-id="a4e93-129">>225</span><span class="sxs-lookup"><span data-stu-id="a4e93-129">>225</span></span>               | <span data-ttu-id="a4e93-130">9</span><span class="sxs-lookup"><span data-stu-id="a4e93-130">9</span></span>                                                 |



 

<span data-ttu-id="a4e93-131">資料流程所需的一般負擔不會將資料單位延伸列入考慮。</span><span class="sxs-lookup"><span data-stu-id="a4e93-131">The normal overhead required for a stream does not take data unit extensions into account.</span></span> <span data-ttu-id="a4e93-132">每個資料單位延伸都會新增至附加的範例大小。</span><span class="sxs-lookup"><span data-stu-id="a4e93-132">Every data unit extension adds to the size of the sample to which it is attached.</span></span> <span data-ttu-id="a4e93-133">視資料單位延伸模組的類型而定，這可能會大幅增加資料流程的位元速率。</span><span class="sxs-lookup"><span data-stu-id="a4e93-133">Depending upon the type of data unit extension, this can greatly increase the bit rate for the stream.</span></span>

<span data-ttu-id="a4e93-134">您也必須考慮到可透過網路連線使用的理論最大頻寬並不是實際的目標位元速率。</span><span class="sxs-lookup"><span data-stu-id="a4e93-134">You must also consider that the theoretical maximum bandwidth available over a network connection is not a practical target bit rate.</span></span> <span data-ttu-id="a4e93-135">由於網路流量及許多其他因素，任何指定連線的平均可用頻寬都是連接的頻寬容量很短。</span><span class="sxs-lookup"><span data-stu-id="a4e93-135">The average available bandwidth for any given connection falls well short of the bandwidth capacity of the connection, because of network traffic and many other factors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4e93-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="a4e93-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4e93-137">**設計設定檔**</span><span class="sxs-lookup"><span data-stu-id="a4e93-137">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> </dl>

 

 




