---
description: 檔案來源 (Async) 篩選
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: 檔案來源 (Async) 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403564b751e53f160ab140ac89bfda4fd9576f00
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467673"
---
# <a name="file-source-async-filter"></a><span data-ttu-id="318fd-103">檔案來源 (Async) 篩選</span><span class="sxs-lookup"><span data-stu-id="318fd-103">File Source (Async) Filter</span></span>

<span data-ttu-id="318fd-104">非同步檔案來源篩選會開啟並讀取許多不同資料格式的本機檔案，並將資料傳遞至剖析器篩選器。</span><span class="sxs-lookup"><span data-stu-id="318fd-104">The Async File Source filter opens and reads local files of many different data formats and passes the data to a parser filter.</span></span>

<span data-ttu-id="318fd-105">若要透過 HTTP 從 web 下載媒體檔案，請使用檔案 [來源 (URL) ](file-source--url--filter.md) 篩選。</span><span class="sxs-lookup"><span data-stu-id="318fd-105">To download media files from the web through HTTP, use the [File Source (URL)](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="318fd-106">若要讀取 ASF 檔案，請使用 [ [WM Asf 讀取](wm-asf-reader-filter.md) 器] 篩選器。</span><span class="sxs-lookup"><span data-stu-id="318fd-106">To read ASF files, use the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="318fd-107">篩選介面</span><span class="sxs-lookup"><span data-stu-id="318fd-107">Filter Interfaces</span></span>                        | <span data-ttu-id="318fd-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="318fd-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>                                                   |
| <span data-ttu-id="318fd-109">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="318fd-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="318fd-110">不適用</span><span class="sxs-lookup"><span data-stu-id="318fd-110">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="318fd-111">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="318fd-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="318fd-112">不適用</span><span class="sxs-lookup"><span data-stu-id="318fd-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="318fd-113">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="318fd-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="318fd-114">**媒體媒體 \_資料流程**。</span><span class="sxs-lookup"><span data-stu-id="318fd-114">**MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="318fd-115">子類型相依于媒體格式。</span><span class="sxs-lookup"><span data-stu-id="318fd-115">The subtype depends on the media format.</span></span> <span data-ttu-id="318fd-116">如果篩選無法辨識格式， (**MEDIASUBTYPE \_ Null** 。 ) </span><span class="sxs-lookup"><span data-stu-id="318fd-116">(**MEDIASUBTYPE\_NULL** if the filter doesn't recognize the format.)</span></span> |
| <span data-ttu-id="318fd-117">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="318fd-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="318fd-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling)、 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="318fd-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="318fd-119">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="318fd-119">Filter CLSID</span></span>                             | <span data-ttu-id="318fd-120">**CLSID \_ AsyncReader**</span><span class="sxs-lookup"><span data-stu-id="318fd-120">**CLSID\_AsyncReader**</span></span>                                                                                                               |
| <span data-ttu-id="318fd-121">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="318fd-121">Property Page CLSID</span></span>                      | <span data-ttu-id="318fd-122">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="318fd-122">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="318fd-123">可執行檔</span><span class="sxs-lookup"><span data-stu-id="318fd-123">Executable</span></span>                               | <span data-ttu-id="318fd-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="318fd-124">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="318fd-125">優點</span><span class="sxs-lookup"><span data-stu-id="318fd-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="318fd-126">**不 \_ 太可能**</span><span class="sxs-lookup"><span data-stu-id="318fd-126">**MERIT\_UNLIKELY**</span></span>                                                                                                                  |
| [<span data-ttu-id="318fd-127">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="318fd-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="318fd-128">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="318fd-128">**CLSID\_LegacyAmFilterCategory**</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="318fd-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="318fd-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="318fd-130">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="318fd-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



