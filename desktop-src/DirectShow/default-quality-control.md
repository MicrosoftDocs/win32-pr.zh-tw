---
description: 預設品質控制項
ms.assetid: 91c4b8cf-3d24-4a11-b19c-b0297734e52b
title: 預設品質控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864cd187df71c56441edcfd00fcd6785d96afe84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025613"
---
# <a name="default-quality-control"></a><span data-ttu-id="2fcf0-103">預設品質控制項</span><span class="sxs-lookup"><span data-stu-id="2fcf0-103">Default Quality Control</span></span>

<span data-ttu-id="2fcf0-104">[DirectShow 基類](directshow-base-classes.md)會針對視頻品質控制項來實行一些預設行為。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-104">The [DirectShow Base Classes](directshow-base-classes.md) implement some default behaviors for video quality control.</span></span>

<span data-ttu-id="2fcf0-105">品質訊息從轉譯器開始。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-105">Quality messages start at the renderer.</span></span> <span data-ttu-id="2fcf0-106">影片轉譯器的基類是 [**CBaseVideoRenderer**](cbasevideorenderer.md)，其行為如下：</span><span class="sxs-lookup"><span data-stu-id="2fcf0-106">The base class for video renderers is [**CBaseVideoRenderer**](cbasevideorenderer.md), which has the following behavior:</span></span>

1.  <span data-ttu-id="2fcf0-107">當影片轉譯器收到範例時，它會比較範例上的時間戳記與目前的參考時間。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-107">When the video renderer receives a sample, it compares the time stamp on the sample with the current reference time.</span></span>
2.  <span data-ttu-id="2fcf0-108">影片轉譯器會產生品質訊息。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-108">The video renderer generates a quality message.</span></span> <span data-ttu-id="2fcf0-109">在基類中，品質訊息的 **比例** 成員限制為 500 (50% ) 到 2000 (200% ) 。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-109">In the base class, the **Proportion** member of the quality message is limited to a range of 500 (50%) to 2000 (200%).</span></span> <span data-ttu-id="2fcf0-110">超出此範圍的值可能會導致高品質的變更。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-110">Values outside this range could result in abrupt quality changes.</span></span>
3.  <span data-ttu-id="2fcf0-111">根據預設，影片轉譯器會將品質訊息傳送至上游輸出 pin， (連接到其輸入 pin) 的 pin。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-111">By default, the video renderer sends the quality message to the upstream output pin (the pin connected to its input pin).</span></span> <span data-ttu-id="2fcf0-112">應用程式可以藉由呼叫 **SetSink** 方法來覆寫此行為。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-112">Applications can override this behavior by calling the **SetSink** method.</span></span>

<span data-ttu-id="2fcf0-113">接下來會發生什麼事取決於上游篩選準則。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-113">What happens next depends on the upstream filter.</span></span> <span data-ttu-id="2fcf0-114">一般來說，這是轉換篩選。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-114">Typically, this is a transform filter.</span></span> <span data-ttu-id="2fcf0-115">轉換篩選準則的基類是 [**CTransformFilter**](ctransformfilter.md)，它會使用 [**CTransformInputPin**](ctransforminputpin.md) 和 [**CTransformOutputPin**](ctransformoutputpin.md) 類別來執行輸入和輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-115">The base class for transform filters is [**CTransformFilter**](ctransformfilter.md), which uses the [**CTransformInputPin**](ctransforminputpin.md) and [**CTransformOutputPin**](ctransformoutputpin.md) classes to implement input and output pins.</span></span> <span data-ttu-id="2fcf0-116">這些類別一起具有下列行為：</span><span class="sxs-lookup"><span data-stu-id="2fcf0-116">Together, these classes have the following behavior:</span></span>

1.  <span data-ttu-id="2fcf0-117">[**CTransformOutputPin：： Notify**](ctransformoutputpin-notify.md)方法會呼叫 [**CTransformFilter：： AlterQuality**](ctransformfilter-alterquality.md)，也就是篩選基類上的私用方法。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-117">The [**CTransformOutputPin::Notify**](ctransformoutputpin-notify.md) method calls [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md), a private method on the filter base class.</span></span>
2.  <span data-ttu-id="2fcf0-118">衍生的篩選可以覆寫 **AlterQuality** 來處理品質訊息。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-118">Derived filters can override **AlterQuality** to handle the quality message.</span></span> <span data-ttu-id="2fcf0-119">根據預設， **AlterQuality** 會忽略品質訊息。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-119">By default, **AlterQuality** ignores the quality message.</span></span>
3.  <span data-ttu-id="2fcf0-120">如果 **AlterQuality** 未處理品質訊息，輸出圖釘會呼叫 [**CBaseInputPin：:P assnotify**](cbaseinputpin-passnotify.md)，也就是篩選器輸入釘上的私用方法。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-120">If **AlterQuality** does not handle the quality message, the output pin calls [**CBaseInputPin::PassNotify**](cbaseinputpin-passnotify.md), a private method on the filter's input pin.</span></span>
4.  <span data-ttu-id="2fcf0-121">**PassNotify** 會將品質訊息傳遞至適當的位置，也就是下一個上游輸出 pin 或自訂品質管制員。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-121">**PassNotify** passes the quality message to the appropriate place—the next upstream output pin, or a custom quality manager.</span></span>

<span data-ttu-id="2fcf0-122">假設沒有任何轉換篩選器會處理品質訊息，訊息最後會到達來源篩選器上的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-122">Assuming that no transform filter handles the quality message, the message eventually reaches the output pin on the source filter.</span></span> <span data-ttu-id="2fcf0-123">在基類中， [**CBasePin：： Notify**](cbasepin-notify.md) 會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-123">In the base classes, [**CBasePin::Notify**](cbasepin-notify.md) returns E\_NOTIMPL.</span></span> <span data-ttu-id="2fcf0-124">特定來源篩選器處理品質訊息的方式視來源的本質而定。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-124">How a particular source filter handles quality messages depends on the nature of the source.</span></span> <span data-ttu-id="2fcf0-125">某些來源（例如即時影片捕獲）無法執行有意義的品質控制項。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-125">Some sources, such as live video capture, cannot perform meaningful quality control.</span></span> <span data-ttu-id="2fcf0-126">其他來源可以調整傳遞範例的速率。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-126">Other sources can adjust the rate at which they deliver samples.</span></span>

<span data-ttu-id="2fcf0-127">下圖說明預設行為。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-127">The following diagram illustrates the default behavior.</span></span>

![基類中的品質控制](images/quality-control.png)

<span data-ttu-id="2fcf0-129">基底影片轉譯器會 **執行 IQualityControl：： Notify**，這表示您可以將品質訊息傳遞給轉譯器本身。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-129">The base video renderer implements **IQualityControl::Notify**, which means you can pass quality messages to the renderer itself.</span></span> <span data-ttu-id="2fcf0-130">如果您將 **比例** 成員設定為小於1000的值，則影片轉譯器會在其轉譯的每個畫面格之間插入等待時間，實際上會減緩轉譯器。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-130">If you set the **Proportion** member to a value less than 1000, the video renderer inserts a wait period between each frame that it renders, in effect slowing down the renderer.</span></span> <span data-ttu-id="2fcf0-131"> (您可能會這麼做，以降低系統的使用方式。如需詳細資訊，請參閱 ) 的詳細資訊，請參閱 [**CBaseVideoRenderer：： ThrottleWait**](cbasevideorenderer-throttlewait.md)。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-131">(You might do this to reduce system usage, for example.) For more information, see [**CBaseVideoRenderer::ThrottleWait**](cbasevideorenderer-throttlewait.md).</span></span> <span data-ttu-id="2fcf0-132">將 **比例** 成員設定為大於1000的值沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="2fcf0-132">Setting the **Proportion** member to a value greater than 1000 has no effect.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fcf0-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="2fcf0-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fcf0-134">品質控制管理</span><span class="sxs-lookup"><span data-stu-id="2fcf0-134">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 



