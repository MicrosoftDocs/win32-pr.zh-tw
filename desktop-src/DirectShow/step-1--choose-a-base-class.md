---
description: 步驟 1：
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: 步驟 1： 選擇基類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4679873e78e75b350335b5294db63579fd41f36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850360"
---
# <a name="step-1-choose-a-base-class"></a><span data-ttu-id="37a4d-104">步驟 1：</span><span class="sxs-lookup"><span data-stu-id="37a4d-104">Step 1.</span></span> <span data-ttu-id="37a4d-105">選擇基類</span><span class="sxs-lookup"><span data-stu-id="37a4d-105">Choose a Base Class</span></span>

<span data-ttu-id="37a4d-106">這是 [撰寫轉換篩選](writing-transform-filters.md)之教學課程的步驟1。</span><span class="sxs-lookup"><span data-stu-id="37a4d-106">This is step 1 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="37a4d-107">假設您決定要撰寫篩選而不是，則第一個步驟是選擇要使用的基類。</span><span class="sxs-lookup"><span data-stu-id="37a4d-107">Assuming that you decide to write a filter and not a DMO, the first step is choosing which base class to use.</span></span> <span data-ttu-id="37a4d-108">下列類別適用于轉換篩選：</span><span class="sxs-lookup"><span data-stu-id="37a4d-108">The following classes are appropriate for transform filters:</span></span>

-   <span data-ttu-id="37a4d-109">[**CTransformFilter**](ctransformfilter.md) 是針對使用不同輸入和輸出緩衝區的轉換篩選所設計。</span><span class="sxs-lookup"><span data-stu-id="37a4d-109">[**CTransformFilter**](ctransformfilter.md) is designed for transform filters that use separate input and output buffers.</span></span> <span data-ttu-id="37a4d-110">這種篩選有時稱為複製轉換篩選。</span><span class="sxs-lookup"><span data-stu-id="37a4d-110">This kind of filter is sometimes called a copy-transform filter.</span></span> <span data-ttu-id="37a4d-111">當複製轉換篩選收到輸入範例時，它會將新的資料寫入至輸出範例，並將輸出範例傳遞給下一個篩選準則。</span><span class="sxs-lookup"><span data-stu-id="37a4d-111">When a copy-transform filter receives an input sample, it writes new data to an output sample and delivers the output sample to the next filter.</span></span>
-   <span data-ttu-id="37a4d-112">[**CTransInPlaceFilter**](ctransinplacefilter.md) 是針對修改原始緩衝區中資料的篩選準則所設計，也稱為「就地記錄篩選準則」。</span><span class="sxs-lookup"><span data-stu-id="37a4d-112">[**CTransInPlaceFilter**](ctransinplacefilter.md) is designed for filters that modify data in the original buffer, also called trans-in-place filters.</span></span> <span data-ttu-id="37a4d-113">當就地篩選收到範例時，它會變更該範例內的資料，並傳遞相同的範例下游。</span><span class="sxs-lookup"><span data-stu-id="37a4d-113">When a trans-in-place filter receives a sample, it changes the data inside that sample and delivers the same sample downstream.</span></span> <span data-ttu-id="37a4d-114">篩選器的輸入釘選和輸出 pin 一律會與相符的媒體類型連接。</span><span class="sxs-lookup"><span data-stu-id="37a4d-114">The filter's input pin and output pin always connect with matching media types.</span></span>
-   <span data-ttu-id="37a4d-115">[**CVideoTransformFilter**](cvideotransformfilter.md) 主要是針對影片解碼器所設計。</span><span class="sxs-lookup"><span data-stu-id="37a4d-115">[**CVideoTransformFilter**](cvideotransformfilter.md) is designed primarily for video decoders.</span></span> <span data-ttu-id="37a4d-116">它衍生自 **CTransformFilter**，但是如果下游轉譯器落在後方，則包含卸載框架的功能。</span><span class="sxs-lookup"><span data-stu-id="37a4d-116">It derives from **CTransformFilter**, but includes functionality for dropping frames if the downstream renderer falls behind.</span></span>
-   <span data-ttu-id="37a4d-117">[**CBaseFilter**](cbasefilter.md) 是泛型篩選類別。</span><span class="sxs-lookup"><span data-stu-id="37a4d-117">[**CBaseFilter**](cbasefilter.md) is a generic filter class.</span></span> <span data-ttu-id="37a4d-118">這份清單中的其他類別全都衍生自 **CBaseFilter**。</span><span class="sxs-lookup"><span data-stu-id="37a4d-118">The other classes in this list all derive from **CBaseFilter**.</span></span> <span data-ttu-id="37a4d-119">如果它們都不適用，您可以回到這個類別。</span><span class="sxs-lookup"><span data-stu-id="37a4d-119">If none of them is suitable, you can fall back on this class.</span></span> <span data-ttu-id="37a4d-120">不過，此類別也需要您最多的工作。</span><span class="sxs-lookup"><span data-stu-id="37a4d-120">However, this class also requires the most work on your part.</span></span>
-   <span data-ttu-id="37a4d-121">\[!重要\]</span><span class="sxs-lookup"><span data-stu-id="37a4d-121">\[!Important\]</span></span>  
    > <span data-ttu-id="37a4d-122">就地影片轉換可能會對轉譯效能產生嚴重的影響。</span><span class="sxs-lookup"><span data-stu-id="37a4d-122">In-place video transforms can have a serious impact on rendering performance.</span></span> <span data-ttu-id="37a4d-123">就地轉換需要緩衝區上的讀寫寫入作業。</span><span class="sxs-lookup"><span data-stu-id="37a4d-123">In-place transforms require read-modify-write operations on the buffer.</span></span> <span data-ttu-id="37a4d-124">如果記憶體位於圖形配接器上，讀取作業的速度會明顯較慢。</span><span class="sxs-lookup"><span data-stu-id="37a4d-124">If the memory resides on a graphics card, read operations are significantly slower.</span></span> <span data-ttu-id="37a4d-125">此外，即使您不小心執行複製轉換，也可能會造成非預期的讀取作業。</span><span class="sxs-lookup"><span data-stu-id="37a4d-125">Moreover, even a copy transform can cause unintended read operations if you do not implement it carefully.</span></span> <span data-ttu-id="37a4d-126">因此，如果您撰寫影片轉換，則應該一律執行效能測試。</span><span class="sxs-lookup"><span data-stu-id="37a4d-126">Therefore, you should always do performance testing if you write a video transform.</span></span>

     

<span data-ttu-id="37a4d-127">若為範例 RLE 編碼器，最佳選擇是 **CTransformFilter** 或 **CVideoTransformFilter**。</span><span class="sxs-lookup"><span data-stu-id="37a4d-127">For the example RLE encoder, the best choice is either **CTransformFilter** or **CVideoTransformFilter**.</span></span> <span data-ttu-id="37a4d-128">事實上，它們之間的差異大多是內部的，因此很容易就能從一個轉換成另一個。</span><span class="sxs-lookup"><span data-stu-id="37a4d-128">In fact, the differences between them are largely internal, so it is easy to convert from one to the other.</span></span> <span data-ttu-id="37a4d-129">因為這兩個 pin 上的媒體類型必須不同，所以 **CTransInPlaceFilter** 類別不適合此篩選器。</span><span class="sxs-lookup"><span data-stu-id="37a4d-129">Because the media types must be different on the two pins, the **CTransInPlaceFilter** class is not appropriate for this filter.</span></span> <span data-ttu-id="37a4d-130">此範例會使用 **CTransformFilter**。</span><span class="sxs-lookup"><span data-stu-id="37a4d-130">This example will use **CTransformFilter**.</span></span>

<span data-ttu-id="37a4d-131">下一 [步：步驟2。宣告篩選類別](step-2--declare-the-filter-class.md)。</span><span class="sxs-lookup"><span data-stu-id="37a4d-131">Next: [Step 2. Declare the Filter Class](step-2--declare-the-filter-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="37a4d-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="37a4d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37a4d-133">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="37a4d-133">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



