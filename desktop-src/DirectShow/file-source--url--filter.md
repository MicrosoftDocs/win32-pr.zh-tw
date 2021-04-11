---
description: 檔案來源 (URL) 篩選
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: 檔案來源 (URL) 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caea04b74a6880452210f1a43d5dfb29f8753dd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109572"
---
# <a name="file-source-url-filter"></a><span data-ttu-id="5ac26-103">檔案來源 (URL) 篩選</span><span class="sxs-lookup"><span data-stu-id="5ac26-103">File Source (URL) Filter</span></span>

<span data-ttu-id="5ac26-104">URL 檔案來源篩選器是一般的非同步來源篩選，可搭配可透過統一資源定位器識別的任何原始程式檔 (URL) ，以及其媒體主要類型為 stream。</span><span class="sxs-lookup"><span data-stu-id="5ac26-104">The URL File Source filter is a generic asynchronous source filter that works with any source file that can be identified by a Uniform Resource Locator (URL) and whose media major type is stream.</span></span> <span data-ttu-id="5ac26-105">這包括 AVI、MOV、MPEG 和 WAV 檔案。</span><span class="sxs-lookup"><span data-stu-id="5ac26-105">This includes AVI, MOV, MPEG, and WAV files.</span></span> <span data-ttu-id="5ac26-106">下游篩選器需要是剖析器，例如 [MPEG 1 串流分隔](mpeg-1-stream-splitter-filter.md)器、 [AVI 分隔器](avi-splitter-filter.md)或 [QuickTime Movie](quicktime-movie-parser-filter.md)剖析器。</span><span class="sxs-lookup"><span data-stu-id="5ac26-106">It requires the downstream filter to be a parser, such as the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), the [AVI Splitter](avi-splitter-filter.md), or the [QuickTime Movie Parser](quicktime-movie-parser-filter.md).</span></span>



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac26-107">篩選介面</span><span class="sxs-lookup"><span data-stu-id="5ac26-107">Filter Interfaces</span></span>                        | <span data-ttu-id="5ac26-108">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="5ac26-108">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>       |
| <span data-ttu-id="5ac26-109">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="5ac26-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="5ac26-110">不適用</span><span class="sxs-lookup"><span data-stu-id="5ac26-110">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="5ac26-111">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="5ac26-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="5ac26-112">不適用</span><span class="sxs-lookup"><span data-stu-id="5ac26-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="5ac26-113">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="5ac26-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="5ac26-114">媒體 \_ 的串流。</span><span class="sxs-lookup"><span data-stu-id="5ac26-114">MEDIATYPE\_Stream.</span></span> <span data-ttu-id="5ac26-115">子類型相依于媒體格式。</span><span class="sxs-lookup"><span data-stu-id="5ac26-115">The subtype depends on the media format.</span></span> <span data-ttu-id="5ac26-116">\_如果篩選無法辨識格式， (MEDIASUBTYPE Null。 ) </span><span class="sxs-lookup"><span data-stu-id="5ac26-116">(MEDIASUBTYPE\_NULL if the filter doesn't recognize the format.)</span></span>         |
| <span data-ttu-id="5ac26-117">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="5ac26-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="5ac26-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling)、 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="5ac26-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="5ac26-119">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="5ac26-119">Filter CLSID</span></span>                             | <span data-ttu-id="5ac26-120">CLSID \_ URLReader</span><span class="sxs-lookup"><span data-stu-id="5ac26-120">CLSID\_URLReader</span></span>                                                                                                                     |
| <span data-ttu-id="5ac26-121">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="5ac26-121">Property Page CLSID</span></span>                      | <span data-ttu-id="5ac26-122">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="5ac26-122">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="5ac26-123">可執行檔</span><span class="sxs-lookup"><span data-stu-id="5ac26-123">Executable</span></span>                               | <span data-ttu-id="5ac26-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="5ac26-124">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="5ac26-125">優點</span><span class="sxs-lookup"><span data-stu-id="5ac26-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="5ac26-126">不 \_ 太可能</span><span class="sxs-lookup"><span data-stu-id="5ac26-126">MERIT\_UNLIKELY</span></span>                                                                                                                      |
| [<span data-ttu-id="5ac26-127">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="5ac26-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="5ac26-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="5ac26-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="5ac26-129">備註</span><span class="sxs-lookup"><span data-stu-id="5ac26-129">Remarks</span></span>

<span data-ttu-id="5ac26-130">此篩選器會使用 Urlmon.dll，並支援字碼頁。</span><span class="sxs-lookup"><span data-stu-id="5ac26-130">This filter uses URLMon and supports code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ac26-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="5ac26-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ac26-132">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="5ac26-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



