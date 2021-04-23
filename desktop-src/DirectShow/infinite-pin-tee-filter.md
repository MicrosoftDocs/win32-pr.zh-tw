---
description: 無限圖釘指標篩選
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: 無限圖釘指標篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3433a0c2f5fe55fa59c42ed6e02d34f6e2cf0e6d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909226"
---
# <a name="infinite-pin-tee-filter"></a><span data-ttu-id="acc8b-103">無限圖釘指標篩選</span><span class="sxs-lookup"><span data-stu-id="acc8b-103">Infinite Pin Tee Filter</span></span>

<span data-ttu-id="acc8b-104">此篩選器會將傳遞給其輸入圖釘的樣本傳遞給變數的輸出接點數目。</span><span class="sxs-lookup"><span data-stu-id="acc8b-104">This filter delivers samples delivered to its input pin to a variable number of output pins.</span></span> <span data-ttu-id="acc8b-105">當篩選準則的實例建立時，它會有一個輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="acc8b-105">When an instance of the filter is created, it has one output pin.</span></span> <span data-ttu-id="acc8b-106">每次連線輸出連接時，篩選器會建立另一個輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="acc8b-106">Each time an output pin is connected, the filter creates another output pin.</span></span> <span data-ttu-id="acc8b-107">所有輸出圖釘都會共用與輸入 pin 相同的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="acc8b-107">All output pins share the same media type as the input pin.</span></span>

<span data-ttu-id="acc8b-108">此篩選器的版本也會以 SDK 範例的形式提供。</span><span class="sxs-lookup"><span data-stu-id="acc8b-108">A version of this filter is also provided as an SDK sample.</span></span> <span data-ttu-id="acc8b-109">請參閱 [InfTee 篩選範例](inftee-filter-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="acc8b-109">See [InfTee Filter Sample](inftee-filter-sample.md).</span></span>



| <span data-ttu-id="acc8b-110">標籤</span><span class="sxs-lookup"><span data-stu-id="acc8b-110">Label</span></span> | <span data-ttu-id="acc8b-111">值</span><span class="sxs-lookup"><span data-stu-id="acc8b-111">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acc8b-112">篩選介面</span><span class="sxs-lookup"><span data-stu-id="acc8b-112">Filter Interfaces</span></span>                        | [<span data-ttu-id="acc8b-113">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="acc8b-113">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="acc8b-114">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="acc8b-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="acc8b-115">任何媒體類型</span><span class="sxs-lookup"><span data-stu-id="acc8b-115">Any media type</span></span>                                                                                                                                     |
| <span data-ttu-id="acc8b-116">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="acc8b-116">Input Pin Interfaces</span></span>                     | <span data-ttu-id="acc8b-117">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="acc8b-117">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="acc8b-118">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="acc8b-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="acc8b-119">任何媒體類型。</span><span class="sxs-lookup"><span data-stu-id="acc8b-119">Any media type.</span></span> <span data-ttu-id="acc8b-120">輸出類型永遠符合輸入類型，適用于所有輸出釘選</span><span class="sxs-lookup"><span data-stu-id="acc8b-120">The output type always matches the input type, for all output pins</span></span>                                                                 |
| <span data-ttu-id="acc8b-121">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="acc8b-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="acc8b-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="acc8b-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="acc8b-123">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="acc8b-123">Filter CLSID</span></span>                             | <span data-ttu-id="acc8b-124">CLSID \_ InfTee</span><span class="sxs-lookup"><span data-stu-id="acc8b-124">CLSID\_InfTee</span></span>                                                                                                                                      |
| <span data-ttu-id="acc8b-125">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="acc8b-125">Property Page CLSID</span></span>                      | <span data-ttu-id="acc8b-126">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="acc8b-126">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="acc8b-127">可執行檔</span><span class="sxs-lookup"><span data-stu-id="acc8b-127">Executable</span></span>                               | <span data-ttu-id="acc8b-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="acc8b-128">qcap.dll</span></span>                                                                                                                                           |
| [<span data-ttu-id="acc8b-129">優點</span><span class="sxs-lookup"><span data-stu-id="acc8b-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="acc8b-130">\_ \_ 未 \_ 使用的業績</span><span class="sxs-lookup"><span data-stu-id="acc8b-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="acc8b-131">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="acc8b-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="acc8b-132">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="acc8b-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="acc8b-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="acc8b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acc8b-134">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="acc8b-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



