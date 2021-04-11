---
description: 媒體參數
ms.assetid: 48b2bc2e-897d-4aa9-8a50-c2855a17dca5
title: 媒體參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9276a3d38b9176458299bfd1a47057cac6236e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103853356"
---
# <a name="media-parameters"></a><span data-ttu-id="9ccfb-103">媒體參數</span><span class="sxs-lookup"><span data-stu-id="9ccfb-103">Media Parameters</span></span>

<span data-ttu-id="9ccfb-104">媒體參數可讓應用程式設定物件的屬性，讓它們以數學決定性的方式變更一段時間。</span><span class="sxs-lookup"><span data-stu-id="9ccfb-104">Media parameters enable an application to configure an object's properties so that they change over time in a mathematically deterministic way.</span></span>

<span data-ttu-id="9ccfb-105">例如，假設音效工程師正在混用數位主磁帶，而且想要對關切這個領域區段套用稍微延遲，以填滿音效。</span><span class="sxs-lookup"><span data-stu-id="9ccfb-105">For example, suppose that a sound engineer is mixing a digital master tape and wants to apply a slight delay to a vocal section, to fill out the sound.</span></span> <span data-ttu-id="9ccfb-106">如果延遲突然剪下，則會 jarring 效果。</span><span class="sxs-lookup"><span data-stu-id="9ccfb-106">The effect will be jarring if the delay cuts in abruptly.</span></span> <span data-ttu-id="9ccfb-107">相反地，效果應該會開始100% 的 (不會有延遲) ，而且濕/試混合應該會逐漸增加，直到達到所需的層級為止。</span><span class="sxs-lookup"><span data-stu-id="9ccfb-107">Instead, the effect should begin 100 percent dry (no delay), and the wet/dry mix should increase gradually until it reaches the desired level.</span></span> <span data-ttu-id="9ccfb-108">此外，這種轉換應該遵循平滑曲線或線性進展。</span><span class="sxs-lookup"><span data-stu-id="9ccfb-108">Moreover, this transition should follow a smooth curve or linear progression.</span></span> <span data-ttu-id="9ccfb-109">為了支援此案例，您可以公開下列介面：</span><span class="sxs-lookup"><span data-stu-id="9ccfb-109">To support this scenario, a DMO can expose the following interfaces:</span></span>

-   <span data-ttu-id="9ccfb-110">[**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) 包含探索所支援屬性之相關資訊的方法。</span><span class="sxs-lookup"><span data-stu-id="9ccfb-110">[**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) contains methods for discovering information about the supported properties.</span></span> <span data-ttu-id="9ccfb-111">一般而言，用戶端會在開始串流資料之前呼叫這些方法。</span><span class="sxs-lookup"><span data-stu-id="9ccfb-111">Typically, the client will call these methods before it begins to stream data.</span></span>
-   <span data-ttu-id="9ccfb-112">[**IMediaParams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) 包含的方法可設定在串流期間參數將遵循的曲線。</span><span class="sxs-lookup"><span data-stu-id="9ccfb-112">[**IMediaParams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) contain methods for setting the curves that a parameter will follow during streaming.</span></span>

<span data-ttu-id="9ccfb-113">這些介面的設計主要是為了 DMOs，但是任何物件都可以支援它們。</span><span class="sxs-lookup"><span data-stu-id="9ccfb-113">These interfaces are designed primarily for DMOs, but any object can support them.</span></span> <span data-ttu-id="9ccfb-114">在本節中，term *參數* 會參考任何支援這兩個介面的屬性。</span><span class="sxs-lookup"><span data-stu-id="9ccfb-114">Within this section, the term *parameter* refers to any property that supports these two interfaces.</span></span>

<span data-ttu-id="9ccfb-115">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="9ccfb-115">This section contains the following topics:</span></span>

-   [<span data-ttu-id="9ccfb-116">參數曲線</span><span class="sxs-lookup"><span data-stu-id="9ccfb-116">Parameter Curves</span></span>](parameter-curves.md)
-   [<span data-ttu-id="9ccfb-117">參數資訊</span><span class="sxs-lookup"><span data-stu-id="9ccfb-117">Parameter Information</span></span>](parameter-information.md)
-   [<span data-ttu-id="9ccfb-118">信封區段</span><span class="sxs-lookup"><span data-stu-id="9ccfb-118">Envelope Segments</span></span>](envelope-segments.md)
-   [<span data-ttu-id="9ccfb-119">計算參數值</span><span class="sxs-lookup"><span data-stu-id="9ccfb-119">Calculating Parameter Values</span></span>](calculating-parameter-values.md)

## <a name="related-topics"></a><span data-ttu-id="9ccfb-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="9ccfb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ccfb-121">DirectX 媒體物件</span><span class="sxs-lookup"><span data-stu-id="9ccfb-121">DirectX Media Objects</span></span>](directx-media-objects.md)
</dt> </dl>

 

 



