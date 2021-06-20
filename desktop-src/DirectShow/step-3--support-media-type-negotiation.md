---
description: 在撰寫轉換篩選時，實作為媒體類型協商的支援。 媒體類型描述資料的格式。
ms.assetid: b2b5dafc-d38d-4ec3-a390-55229495b4f9
title: 步驟 3： 支援媒體類型的協商
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a23784e70330f751325fc5f780463d5a3904d20
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410041"
---
# <a name="step-3-support-media-type-negotiation"></a><span data-ttu-id="feca1-105">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="feca1-105">Step 3.</span></span> <span data-ttu-id="feca1-106">支援媒體類型的協商</span><span class="sxs-lookup"><span data-stu-id="feca1-106">Support Media Type Negotiation</span></span>

<span data-ttu-id="feca1-107">這是 [撰寫轉換篩選](writing-transform-filters.md)之教學課程的步驟3。</span><span class="sxs-lookup"><span data-stu-id="feca1-107">This is step 3 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="feca1-108">當兩個 pin 連線時，他們必須同意連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="feca1-108">When two pins connect, they must agree on a media type for the connection.</span></span> <span data-ttu-id="feca1-109">媒體類型描述資料的格式。</span><span class="sxs-lookup"><span data-stu-id="feca1-109">The media type describes the format of the data.</span></span> <span data-ttu-id="feca1-110">如果沒有媒體類型，篩選器可能會提供一種資料，只是讓另一個篩選器將它視為其他的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="feca1-110">Without the media type, a filter might deliver one kind of data, only to have another filter treat it as something else.</span></span>

<span data-ttu-id="feca1-111">協商媒體類型的基本機制是 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 方法。</span><span class="sxs-lookup"><span data-stu-id="feca1-111">The basic mechanism for negotiating media types is the [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) method.</span></span> <span data-ttu-id="feca1-112">輸出圖釘會以建議的媒體類型，在輸入 pin 上呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="feca1-112">The output pin calls this method on the input pin with a proposed media type.</span></span> <span data-ttu-id="feca1-113">輸入 pin 接受連接或拒絕連接。</span><span class="sxs-lookup"><span data-stu-id="feca1-113">The input pin accepts the connection or rejects it.</span></span> <span data-ttu-id="feca1-114">如果拒絕連線，輸出 pin 可以嘗試其他媒體類型。</span><span class="sxs-lookup"><span data-stu-id="feca1-114">If it rejects the connection, the output pin can try another media type.</span></span> <span data-ttu-id="feca1-115">如果找不到適合的類型，連接就會失敗。</span><span class="sxs-lookup"><span data-stu-id="feca1-115">If no suitable types are found, the connection fails.</span></span> <span data-ttu-id="feca1-116">輸入 pin 可以選擇性地透過 [**IPin：： EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) 方法，通告其慣用的類型清單。</span><span class="sxs-lookup"><span data-stu-id="feca1-116">Optionally, the input pin can advertise a list of types that it prefers, through the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span> <span data-ttu-id="feca1-117">當輸出 pin 提議媒體類型時，就可以使用這份清單，雖然不需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="feca1-117">The output pin can use this list when it proposes media types, although it does not have to.</span></span>

<span data-ttu-id="feca1-118">**CTransformFilter** 類別會為此程式實作為一般架構，如下所示：</span><span class="sxs-lookup"><span data-stu-id="feca1-118">The **CTransformFilter** class implements a general framework for this process, as follows:</span></span>

-   <span data-ttu-id="feca1-119">輸入 pin 沒有慣用的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="feca1-119">The input pin has no preferred media types.</span></span> <span data-ttu-id="feca1-120">它完全依賴上游篩選器來提議媒體類型。</span><span class="sxs-lookup"><span data-stu-id="feca1-120">It relies entirely on the upstream filter to propose the media type.</span></span> <span data-ttu-id="feca1-121">對於影片資料而言很有意義，因為媒體類型包含影像大小和畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="feca1-121">For video data, this makes sense, because the media type includes the image size and the frame rate.</span></span> <span data-ttu-id="feca1-122">一般而言，該資訊必須由上游來源篩選器或剖析器篩選器提供。</span><span class="sxs-lookup"><span data-stu-id="feca1-122">Typically, that information must be supplied by an upstream source filter or parser filter.</span></span> <span data-ttu-id="feca1-123">在音訊資料的情況下，可能會有一組較小的格式，因此輸入 pin 可能會提供一些慣用的類型。</span><span class="sxs-lookup"><span data-stu-id="feca1-123">In the case of audio data, the set of possible formats is smaller, so it may be practical for the input pin to offer some preferred types.</span></span> <span data-ttu-id="feca1-124">在此情況下，請覆寫輸入釘選上的 [**CBasePin：： GetMediaType**](cbasepin-getmediatype.md) 。</span><span class="sxs-lookup"><span data-stu-id="feca1-124">In that case, override [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) on the input pin.</span></span>
-   <span data-ttu-id="feca1-125">當上游篩選提議媒體類型時，輸入 pin 會呼叫 [**CTransformFilter：： CheckInputType**](ctransformfilter-checkinputtype.md) 方法，以接受或拒絕該類型。</span><span class="sxs-lookup"><span data-stu-id="feca1-125">When the upstream filter proposes a media type, the input pin calls the [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method, which accepts or rejects the type.</span></span>
-   <span data-ttu-id="feca1-126">除非先連接輸入 pin，否則輸出 pin 將不會連接。</span><span class="sxs-lookup"><span data-stu-id="feca1-126">The output pin will not connect unless the input pin is connected first.</span></span> <span data-ttu-id="feca1-127">這是轉換篩選準則的一般行為。</span><span class="sxs-lookup"><span data-stu-id="feca1-127">This behavior is typical for transform filters.</span></span> <span data-ttu-id="feca1-128">在大部分的情況下，篩選準則必須先判斷輸入類型，才能設定輸出類型。</span><span class="sxs-lookup"><span data-stu-id="feca1-128">In most cases, the filter must determine the input type before it can set the output type.</span></span>
-   <span data-ttu-id="feca1-129">當輸出連接連接時，它會有一份向下游篩選器提出的媒體類型清單。</span><span class="sxs-lookup"><span data-stu-id="feca1-129">When the output pin does connect, it has a list of media types that it proposes to the downstream filter.</span></span> <span data-ttu-id="feca1-130">它會呼叫 [**CTransformFilter：： GetMediaType**](ctransformfilter-getmediatype.md) 方法來產生這份清單。</span><span class="sxs-lookup"><span data-stu-id="feca1-130">It calls the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method to generate this list.</span></span> <span data-ttu-id="feca1-131">輸出釘選也會嘗試下游篩選準則所建議的任何媒體類型。</span><span class="sxs-lookup"><span data-stu-id="feca1-131">The output pin will also try any media types that the downstream filter proposes.</span></span>
-   <span data-ttu-id="feca1-132">若要檢查特定的輸出類型是否與輸入類型相容，輸出圖釘會呼叫 [**CTransformFilter：： CheckTransform**](ctransformfilter-checktransform.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="feca1-132">To check whether a particular output type is compatible with the input type, the output pin calls the [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method.</span></span>

<span data-ttu-id="feca1-133">先前所列的三個 **CTransformFilter** 方法是純虛擬方法，因此您的衍生類別必須執行這些方法。</span><span class="sxs-lookup"><span data-stu-id="feca1-133">The three **CTransformFilter** methods listed previously are pure virtual methods, so your derived class must implement them.</span></span> <span data-ttu-id="feca1-134">這些方法都不屬於 COM 介面;它們只是基類所提供之實作為的一部分。</span><span class="sxs-lookup"><span data-stu-id="feca1-134">None of these methods belongs to a COM interface; they are simply part of the implementation provided by the base classes.</span></span>

<span data-ttu-id="feca1-135">下列各節會更詳細地說明每個方法：</span><span class="sxs-lookup"><span data-stu-id="feca1-135">The following sections describe each method in more detail:</span></span>

-   [<span data-ttu-id="feca1-136">步驟3A。執行 CheckInputType 方法</span><span class="sxs-lookup"><span data-stu-id="feca1-136">Step 3A. Implement the CheckInputType Method</span></span>](step-3a--implement-the-checkinputtype-method.md)
-   [<span data-ttu-id="feca1-137">步驟3B。執行 GetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="feca1-137">Step 3B. Implement the GetMediaType Method</span></span>](step-3b--implement-the-getmediatype-method.md)
-   [<span data-ttu-id="feca1-138">步驟3C。執行 CheckTransform 方法</span><span class="sxs-lookup"><span data-stu-id="feca1-138">Step 3C. Implement the CheckTransform Method</span></span>](step-3c--implement-the-checktransform-method.md)

## <a name="related-topics"></a><span data-ttu-id="feca1-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="feca1-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="feca1-140">篩選準則的連接方式</span><span class="sxs-lookup"><span data-stu-id="feca1-140">How Filters Connect</span></span>](how-filters-connect.md)
</dt> <dt>

[<span data-ttu-id="feca1-141">撰寫 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="feca1-141">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



