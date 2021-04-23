---
description: 檔案來源 (Async) 篩選
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: 檔案來源 (Async) 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddeea7398ce332a8b1db444b6b74fe3841f9053
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909696"
---
# <a name="file-source-async-filter"></a><span data-ttu-id="1adb0-103">檔案來源 (Async) 篩選</span><span class="sxs-lookup"><span data-stu-id="1adb0-103">File Source (Async) Filter</span></span>

<span data-ttu-id="1adb0-104">非同步檔案來源篩選會開啟並讀取許多不同資料格式的本機檔案，並將資料傳遞至剖析器篩選器。</span><span class="sxs-lookup"><span data-stu-id="1adb0-104">The Async File Source filter opens and reads local files of many different data formats and passes the data to a parser filter.</span></span>

<span data-ttu-id="1adb0-105">若要透過 HTTP 從 web 下載媒體檔案，請使用檔案 [來源 (URL) ](file-source--url--filter.md) 篩選。</span><span class="sxs-lookup"><span data-stu-id="1adb0-105">To download media files from the web through HTTP, use the [File Source (URL)](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="1adb0-106">若要讀取 ASF 檔案，請使用 [ [WM Asf 讀取](wm-asf-reader-filter.md) 器] 篩選器。</span><span class="sxs-lookup"><span data-stu-id="1adb0-106">To read ASF files, use the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>



| <span data-ttu-id="1adb0-107">標籤</span><span class="sxs-lookup"><span data-stu-id="1adb0-107">Label</span></span> | <span data-ttu-id="1adb0-108">值</span><span class="sxs-lookup"><span data-stu-id="1adb0-108">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1adb0-109">篩選介面</span><span class="sxs-lookup"><span data-stu-id="1adb0-109">Filter Interfaces</span></span>                        | <span data-ttu-id="1adb0-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="1adb0-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>                                                   |
| <span data-ttu-id="1adb0-111">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="1adb0-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="1adb0-112">不適用</span><span class="sxs-lookup"><span data-stu-id="1adb0-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="1adb0-113">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="1adb0-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="1adb0-114">不適用</span><span class="sxs-lookup"><span data-stu-id="1adb0-114">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="1adb0-115">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="1adb0-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="1adb0-116">**媒體媒體 \_資料流程**。</span><span class="sxs-lookup"><span data-stu-id="1adb0-116">**MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="1adb0-117">子類型相依于媒體格式。</span><span class="sxs-lookup"><span data-stu-id="1adb0-117">The subtype depends on the media format.</span></span> <span data-ttu-id="1adb0-118">如果篩選無法辨識格式， (**MEDIASUBTYPE \_ Null** 。 ) </span><span class="sxs-lookup"><span data-stu-id="1adb0-118">(**MEDIASUBTYPE\_NULL** if the filter doesn't recognize the format.)</span></span> |
| <span data-ttu-id="1adb0-119">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="1adb0-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="1adb0-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling)、 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="1adb0-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="1adb0-121">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="1adb0-121">Filter CLSID</span></span>                             | <span data-ttu-id="1adb0-122">**CLSID \_ AsyncReader**</span><span class="sxs-lookup"><span data-stu-id="1adb0-122">**CLSID\_AsyncReader**</span></span>                                                                                                               |
| <span data-ttu-id="1adb0-123">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="1adb0-123">Property Page CLSID</span></span>                      | <span data-ttu-id="1adb0-124">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="1adb0-124">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="1adb0-125">可執行檔</span><span class="sxs-lookup"><span data-stu-id="1adb0-125">Executable</span></span>                               | <span data-ttu-id="1adb0-126">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="1adb0-126">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="1adb0-127">優點</span><span class="sxs-lookup"><span data-stu-id="1adb0-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="1adb0-128">**不 \_ 太可能**</span><span class="sxs-lookup"><span data-stu-id="1adb0-128">**MERIT\_UNLIKELY**</span></span>                                                                                                                  |
| [<span data-ttu-id="1adb0-129">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="1adb0-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="1adb0-130">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="1adb0-130">**CLSID\_LegacyAmFilterCategory**</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="1adb0-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="1adb0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1adb0-132">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="1adb0-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



