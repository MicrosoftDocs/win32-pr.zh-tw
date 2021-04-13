---
description: MJPEG 解壓縮程式篩選器
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: MJPEG 解壓縮程式篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebe8f5f19cb94d75c1ce01cd94dc723100560de
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510275"
---
# <a name="mjpeg-decompressor-filter"></a><span data-ttu-id="2b307-103">MJPEG 解壓縮程式篩選器</span><span class="sxs-lookup"><span data-stu-id="2b307-103">MJPEG Decompressor Filter</span></span>

<span data-ttu-id="2b307-104">此篩選會將影片串流從動畫 JPEG 解碼成未壓縮的影片。</span><span class="sxs-lookup"><span data-stu-id="2b307-104">This filter decodes a video stream from motion JPEG to uncompressed video.</span></span> <span data-ttu-id="2b307-105">有些數位攝影機會產生運動 JPEG 影片串流。</span><span class="sxs-lookup"><span data-stu-id="2b307-105">Some digital video cameras produce a motion JPEG video stream.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b307-106">篩選介面</span><span class="sxs-lookup"><span data-stu-id="2b307-106">Filter Interfaces</span></span>                        | [<span data-ttu-id="2b307-107">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="2b307-107">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="2b307-108">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="2b307-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="2b307-109">媒體媒體 \_ 、MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="2b307-109">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                               |
| <span data-ttu-id="2b307-110">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="2b307-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="2b307-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="2b307-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="2b307-112">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="2b307-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="2b307-113">媒體媒體 \_ 、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="2b307-113">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                               |
| <span data-ttu-id="2b307-114">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="2b307-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="2b307-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="2b307-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="2b307-116">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="2b307-116">Filter CLSID</span></span>                             | <span data-ttu-id="2b307-117">CLSID \_ MjpegDec</span><span class="sxs-lookup"><span data-stu-id="2b307-117">CLSID\_MjpegDec</span></span>                                                                                                                                    |
| <span data-ttu-id="2b307-118">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="2b307-118">Property Page CLSID</span></span>                      | <span data-ttu-id="2b307-119">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="2b307-119">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="2b307-120">可執行檔</span><span class="sxs-lookup"><span data-stu-id="2b307-120">Executable</span></span>                               | <span data-ttu-id="2b307-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="2b307-121">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="2b307-122">優點</span><span class="sxs-lookup"><span data-stu-id="2b307-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="2b307-123">一般的業績 \_</span><span class="sxs-lookup"><span data-stu-id="2b307-123">MERIT\_NORMAL</span></span>                                                                                                                                      |
| [<span data-ttu-id="2b307-124">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="2b307-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="2b307-125">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="2b307-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="2b307-126">備註</span><span class="sxs-lookup"><span data-stu-id="2b307-126">Remarks</span></span>

<span data-ttu-id="2b307-127">此篩選與使用 FOURCC 碼 ' MJPG ' 的動畫 JPEG 影片相容。</span><span class="sxs-lookup"><span data-stu-id="2b307-127">This filter is compatible with motion JPEG video that uses the FOURCC code 'MJPG'.</span></span> <span data-ttu-id="2b307-128">它無法解碼其他各種不同的動畫 JPEG。</span><span class="sxs-lookup"><span data-stu-id="2b307-128">It cannot decode other varieties of motion JPEG.</span></span> <span data-ttu-id="2b307-129">在這些情況下，您將需要使用協力廠商的解碼篩選器。</span><span class="sxs-lookup"><span data-stu-id="2b307-129">For these, you will need to use a third-party decoder filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b307-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="2b307-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b307-131">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="2b307-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



