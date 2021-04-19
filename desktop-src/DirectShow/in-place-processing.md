---
description: In-Place 處理
ms.assetid: 61e5c12c-e42a-42d8-ac5b-e60afaceda82
title: In-Place 處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ba0aa5c50fc000eadadc0f121db6f954a57c338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970296"
---
# <a name="in-place-processing"></a><span data-ttu-id="8eb0e-103">In-Place 處理</span><span class="sxs-lookup"><span data-stu-id="8eb0e-103">In-Place Processing</span></span>

<span data-ttu-id="8eb0e-104">您可以直接修改資料來完成特定的資料轉換。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-104">Certain data transformations can be accomplished by directly modifying the data.</span></span> <span data-ttu-id="8eb0e-105">這稱為就地 *處理。*</span><span class="sxs-lookup"><span data-stu-id="8eb0e-105">This is called *in-place* processing.</span></span> <span data-ttu-id="8eb0e-106">許多音訊和影片效果都可以透過這種方式來完成。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-106">Many audio and video effects can be done in this manner.</span></span> <span data-ttu-id="8eb0e-107">如果 SQL-DMO 支援就地處理，它會公開 [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) 介面。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-107">If a DMO supports in-place processing, it exposes the [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) interface.</span></span> <span data-ttu-id="8eb0e-108">就地處理比針對輸出使用不同的緩衝區，通常更有效率。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-108">In-place processing is generally more efficient than using separate buffers for the output.</span></span> <span data-ttu-id="8eb0e-109"> (一個主要的例外狀況是當緩衝區位於視訊記憶體時。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-109">(One major exception is when the buffer resides in video memory.</span></span> <span data-ttu-id="8eb0e-110">在這種情況下，讀取作業的速度會比寫入作業慢很多，因此不建議就地處理。 ) </span><span class="sxs-lookup"><span data-stu-id="8eb0e-110">In that situation, read operations are much slower than write operations, so in-place processing is not recommended.)</span></span>

<span data-ttu-id="8eb0e-111">若要就地處理資料，用戶端會對 [**IMediaObjectInPlace：:P rocess**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) 方法進行單一呼叫，而不是個別呼叫 **ProcessInput** 和 **ProcessOutput**。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-111">To process data in place, the client makes a single call to the [**IMediaObjectInPlace::Process**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) method, rather than separate calls to **ProcessInput** and **ProcessOutput**.</span></span> <span data-ttu-id="8eb0e-112">**Process** 方法是同步的;所有處理都是在呼叫內進行。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-112">The **Process** method is synchronous; all processing occurs inside the call.</span></span> <span data-ttu-id="8eb0e-113">此外，就地處理不會使用 **IMediaBuffer** 物件。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-113">Also, in-place processing does not use **IMediaBuffer** objects.</span></span> <span data-ttu-id="8eb0e-114">**Process** 方法會將指標直接帶到記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-114">The **Process** method takes a pointer directly to the memory buffer.</span></span>

<span data-ttu-id="8eb0e-115">支援就地處理的 SQL-DMO 仍必須執行 **IMediaObject** 介面，包括 **ProcessInput** 和 **ProcessOutput** 方法。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-115">A DMO that supports in-place processing still must implement the **IMediaObject** interface, including the **ProcessInput** and **ProcessOutput** methods.</span></span> <span data-ttu-id="8eb0e-116">用戶端可以選擇是要使用就地處理或使用不同的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-116">The client can choose whether to use in-place processing or use separate buffers.</span></span> <span data-ttu-id="8eb0e-117">不過，請勿混用這兩種類型的處理。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-117">However, do not mix the two types of processing.</span></span> <span data-ttu-id="8eb0e-118">如果您呼叫 **進程**，請勿呼叫 **ProcessInput** 或 **ProcessOutput**，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-118">If you call **Process**, do not call **ProcessInput** or **ProcessOutput**, and vice-versa.</span></span>

<span data-ttu-id="8eb0e-119">**效果連接結尾**</span><span class="sxs-lookup"><span data-stu-id="8eb0e-119">**Effect Tails**</span></span>

<span data-ttu-id="8eb0e-120">在輸入停止後，可能會建立一些額外的輸出。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-120">An in-place DMO might create some additional output after the input stops.</span></span> <span data-ttu-id="8eb0e-121">這稱為 *效果結尾*。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-121">This is called an *effect tail*.</span></span> <span data-ttu-id="8eb0e-122">例如，當輸入進入無回應後，就會繼續執行回音效果。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-122">For example, a reverb effect continues after the input reaches silence.</span></span> <span data-ttu-id="8eb0e-123">如果有效果結尾，則 **Process** 方法會傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-123">If there is an effect tail, the **Process** method returns S\_FALSE.</span></span> <span data-ttu-id="8eb0e-124">當應用程式處理其所有資料之後，它就可以將空的緩衝區傳送至 **Process** 方法，以產生效果結尾。</span><span class="sxs-lookup"><span data-stu-id="8eb0e-124">Once the application has processed all of its data, it can generate the effect tail by sending empty buffers to the **Process** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8eb0e-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="8eb0e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8eb0e-126">直接裝載</span><span class="sxs-lookup"><span data-stu-id="8eb0e-126">Directly Hosting a DMO</span></span>](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



