---
description: Smart t 篩選
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Smart t 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c52077066f69e50fbb5218012a402a8d556c15c1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909296"
---
# <a name="smart-tee-filter"></a><span data-ttu-id="aa36e-103">Smart t 篩選</span><span class="sxs-lookup"><span data-stu-id="aa36e-103">Smart Tee Filter</span></span>

<span data-ttu-id="aa36e-104">影片捕獲圖形中會使用智慧 t a 濾波器，將影片串流分割成預覽資料流程和捕獲資料流程。</span><span class="sxs-lookup"><span data-stu-id="aa36e-104">The Smart Tee filter is used in video capture graphs to split the video stream into a preview stream and a capture stream.</span></span> <span data-ttu-id="aa36e-105">這是在沒有任何額外的資料複製的情況下完成。</span><span class="sxs-lookup"><span data-stu-id="aa36e-105">This is done without any additional data copying.</span></span> <span data-ttu-id="aa36e-106">輸出圖釘支援下游連線支援的任何媒體類型。</span><span class="sxs-lookup"><span data-stu-id="aa36e-106">The output pins support whatever media types are supported on the downstream connection.</span></span>

<span data-ttu-id="aa36e-107">當影片捕獲篩選未提供個別的 pin 供捕捉和預覽時，智慧的 t a 濾波器會很有用。</span><span class="sxs-lookup"><span data-stu-id="aa36e-107">The Smart Tee filter is useful when a video capture filter does not provide separate pins for capture and preview.</span></span> <span data-ttu-id="aa36e-108">只有在這種情況不會影響到捕捉效能時，智慧的 t 濾波器才會提供預覽資料。</span><span class="sxs-lookup"><span data-stu-id="aa36e-108">The Smart Tee filter delivers preview data only if doing so does not hurt capture performance.</span></span> <span data-ttu-id="aa36e-109">它也會從預覽資料流程中移除時間戳記。</span><span class="sxs-lookup"><span data-stu-id="aa36e-109">It also removes the time stamps from the preview stream.</span></span> <span data-ttu-id="aa36e-110">[Capture graph builder] 會在需要時自動插入智慧的 t a 濾波器。</span><span class="sxs-lookup"><span data-stu-id="aa36e-110">The capture graph builder automatically inserts the Smart Tee filter when needed.</span></span> <span data-ttu-id="aa36e-111">如需詳細資訊，請參閱 [結合影片捕獲和預覽](combining-video-capture-and-preview.md)。</span><span class="sxs-lookup"><span data-stu-id="aa36e-111">For more information, see [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="aa36e-112">下圖顯示使用智慧型 t a 濾波器的一般 capture graph。</span><span class="sxs-lookup"><span data-stu-id="aa36e-112">The following illustration shows a typical capture graph that uses the Smart Tee filter.</span></span>

![使用智慧的 t a 濾波器](images/smarttee.png)



| <span data-ttu-id="aa36e-114">標籤</span><span class="sxs-lookup"><span data-stu-id="aa36e-114">Label</span></span> | <span data-ttu-id="aa36e-115">值</span><span class="sxs-lookup"><span data-stu-id="aa36e-115">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa36e-116">篩選介面</span><span class="sxs-lookup"><span data-stu-id="aa36e-116">Filter Interfaces</span></span>                        | [<span data-ttu-id="aa36e-117">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="aa36e-117">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| <span data-ttu-id="aa36e-118">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="aa36e-118">Input Pin Media Types</span></span>                    | <span data-ttu-id="aa36e-119">媒體媒體 \_ 、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="aa36e-119">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="aa36e-120">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="aa36e-120">Input Pin Interfaces</span></span>                     | <span data-ttu-id="aa36e-121">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="aa36e-121">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>         |
| <span data-ttu-id="aa36e-122">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="aa36e-122">Output Pin Media Types</span></span>                   | <span data-ttu-id="aa36e-123">媒體媒體 \_ 、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="aa36e-123">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="aa36e-124">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="aa36e-124">Output Pin Interfaces</span></span>                    | <span data-ttu-id="aa36e-125">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="aa36e-125">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="aa36e-126">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="aa36e-126">Filter CLSID</span></span>                             | <span data-ttu-id="aa36e-127">CLSID \_ SmartTee</span><span class="sxs-lookup"><span data-stu-id="aa36e-127">CLSID\_SmartTee</span></span>                                                                                                |
| <span data-ttu-id="aa36e-128">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="aa36e-128">Property Page CLSID</span></span>                      | <span data-ttu-id="aa36e-129">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="aa36e-129">No property page.</span></span>                                                                                              |
| <span data-ttu-id="aa36e-130">可執行檔</span><span class="sxs-lookup"><span data-stu-id="aa36e-130">Executable</span></span>                               | <span data-ttu-id="aa36e-131">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="aa36e-131">qcap.dll</span></span>                                                                                                       |
| [<span data-ttu-id="aa36e-132">優點</span><span class="sxs-lookup"><span data-stu-id="aa36e-132">Merit</span></span>](merit.md)                       | <span data-ttu-id="aa36e-133">\_ \_ 未 \_ 使用的業績</span><span class="sxs-lookup"><span data-stu-id="aa36e-133">MERIT\_DO\_NOT\_USE</span></span>                                                                                            |
| [<span data-ttu-id="aa36e-134">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="aa36e-134">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="aa36e-135">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="aa36e-135">CLSID\_LegacyAmFilterCategory</span></span>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="aa36e-136">備註</span><span class="sxs-lookup"><span data-stu-id="aa36e-136">Remarks</span></span>

<span data-ttu-id="aa36e-137">捕捉釘是輸出針腳0，而預覽 pin 則是輸出 pin 1。</span><span class="sxs-lookup"><span data-stu-id="aa36e-137">The capture pin is output pin 0, and the preview pin is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa36e-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa36e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa36e-139">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="aa36e-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



