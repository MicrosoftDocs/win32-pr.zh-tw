---
description: 無限圖釘指標篩選
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: 無限圖釘指標篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e9a80baf047cdd5559fadaa0f13ea1352d4ed0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385764"
---
# <a name="infinite-pin-tee-filter"></a><span data-ttu-id="978b7-103">無限圖釘指標篩選</span><span class="sxs-lookup"><span data-stu-id="978b7-103">Infinite Pin Tee Filter</span></span>

<span data-ttu-id="978b7-104">此篩選器會將傳遞給其輸入圖釘的樣本傳遞給變數的輸出接點數目。</span><span class="sxs-lookup"><span data-stu-id="978b7-104">This filter delivers samples delivered to its input pin to a variable number of output pins.</span></span> <span data-ttu-id="978b7-105">當篩選準則的實例建立時，它會有一個輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="978b7-105">When an instance of the filter is created, it has one output pin.</span></span> <span data-ttu-id="978b7-106">每次連線輸出連接時，篩選器會建立另一個輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="978b7-106">Each time an output pin is connected, the filter creates another output pin.</span></span> <span data-ttu-id="978b7-107">所有輸出圖釘都會共用與輸入 pin 相同的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="978b7-107">All output pins share the same media type as the input pin.</span></span>

<span data-ttu-id="978b7-108">此篩選器的版本也會以 SDK 範例的形式提供。</span><span class="sxs-lookup"><span data-stu-id="978b7-108">A version of this filter is also provided as an SDK sample.</span></span> <span data-ttu-id="978b7-109">請參閱 [InfTee 篩選範例](inftee-filter-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="978b7-109">See [InfTee Filter Sample](inftee-filter-sample.md).</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="978b7-110">篩選介面</span><span class="sxs-lookup"><span data-stu-id="978b7-110">Filter Interfaces</span></span>                        | [<span data-ttu-id="978b7-111">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="978b7-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="978b7-112">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="978b7-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="978b7-113">任何媒體類型</span><span class="sxs-lookup"><span data-stu-id="978b7-113">Any media type</span></span>                                                                                                                                     |
| <span data-ttu-id="978b7-114">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="978b7-114">Input Pin Interfaces</span></span>                     | <span data-ttu-id="978b7-115">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="978b7-115">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="978b7-116">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="978b7-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="978b7-117">任何媒體類型。</span><span class="sxs-lookup"><span data-stu-id="978b7-117">Any media type.</span></span> <span data-ttu-id="978b7-118">輸出類型永遠符合輸入類型，適用于所有輸出釘選</span><span class="sxs-lookup"><span data-stu-id="978b7-118">The output type always matches the input type, for all output pins</span></span>                                                                 |
| <span data-ttu-id="978b7-119">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="978b7-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="978b7-120">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="978b7-120">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="978b7-121">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="978b7-121">Filter CLSID</span></span>                             | <span data-ttu-id="978b7-122">CLSID \_ InfTee</span><span class="sxs-lookup"><span data-stu-id="978b7-122">CLSID\_InfTee</span></span>                                                                                                                                      |
| <span data-ttu-id="978b7-123">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="978b7-123">Property Page CLSID</span></span>                      | <span data-ttu-id="978b7-124">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="978b7-124">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="978b7-125">可執行檔</span><span class="sxs-lookup"><span data-stu-id="978b7-125">Executable</span></span>                               | <span data-ttu-id="978b7-126">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="978b7-126">qcap.dll</span></span>                                                                                                                                           |
| [<span data-ttu-id="978b7-127">優點</span><span class="sxs-lookup"><span data-stu-id="978b7-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="978b7-128">\_ \_ 未 \_ 使用的業績</span><span class="sxs-lookup"><span data-stu-id="978b7-128">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="978b7-129">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="978b7-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="978b7-130">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="978b7-130">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="978b7-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="978b7-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="978b7-132">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="978b7-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



