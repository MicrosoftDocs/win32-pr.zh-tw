---
description: MJPEG 解壓縮程式篩選器
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: MJPEG 解壓縮程式篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23a3e3c09d218a83f5243bf6702d3b5fc3ae1c16
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910016"
---
# <a name="mjpeg-decompressor-filter"></a><span data-ttu-id="986b3-103">MJPEG 解壓縮程式篩選器</span><span class="sxs-lookup"><span data-stu-id="986b3-103">MJPEG Decompressor Filter</span></span>

<span data-ttu-id="986b3-104">此篩選會將影片串流從動畫 JPEG 解碼成未壓縮的影片。</span><span class="sxs-lookup"><span data-stu-id="986b3-104">This filter decodes a video stream from motion JPEG to uncompressed video.</span></span> <span data-ttu-id="986b3-105">有些數位攝影機會產生運動 JPEG 影片串流。</span><span class="sxs-lookup"><span data-stu-id="986b3-105">Some digital video cameras produce a motion JPEG video stream.</span></span>



| <span data-ttu-id="986b3-106">標籤</span><span class="sxs-lookup"><span data-stu-id="986b3-106">Label</span></span> | <span data-ttu-id="986b3-107">值</span><span class="sxs-lookup"><span data-stu-id="986b3-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="986b3-108">篩選介面</span><span class="sxs-lookup"><span data-stu-id="986b3-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="986b3-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="986b3-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="986b3-110">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="986b3-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="986b3-111">媒體媒體 \_ 、MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="986b3-111">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                               |
| <span data-ttu-id="986b3-112">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="986b3-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="986b3-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="986b3-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="986b3-114">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="986b3-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="986b3-115">媒體媒體 \_ 、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="986b3-115">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                               |
| <span data-ttu-id="986b3-116">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="986b3-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="986b3-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="986b3-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="986b3-118">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="986b3-118">Filter CLSID</span></span>                             | <span data-ttu-id="986b3-119">CLSID \_ MjpegDec</span><span class="sxs-lookup"><span data-stu-id="986b3-119">CLSID\_MjpegDec</span></span>                                                                                                                                    |
| <span data-ttu-id="986b3-120">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="986b3-120">Property Page CLSID</span></span>                      | <span data-ttu-id="986b3-121">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="986b3-121">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="986b3-122">可執行檔</span><span class="sxs-lookup"><span data-stu-id="986b3-122">Executable</span></span>                               | <span data-ttu-id="986b3-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="986b3-123">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="986b3-124">優點</span><span class="sxs-lookup"><span data-stu-id="986b3-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="986b3-125">一般的業績 \_</span><span class="sxs-lookup"><span data-stu-id="986b3-125">MERIT\_NORMAL</span></span>                                                                                                                                      |
| [<span data-ttu-id="986b3-126">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="986b3-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="986b3-127">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="986b3-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="986b3-128">備註</span><span class="sxs-lookup"><span data-stu-id="986b3-128">Remarks</span></span>

<span data-ttu-id="986b3-129">此篩選與使用 FOURCC 碼 ' MJPG ' 的動畫 JPEG 影片相容。</span><span class="sxs-lookup"><span data-stu-id="986b3-129">This filter is compatible with motion JPEG video that uses the FOURCC code 'MJPG'.</span></span> <span data-ttu-id="986b3-130">它無法解碼其他各種不同的動畫 JPEG。</span><span class="sxs-lookup"><span data-stu-id="986b3-130">It cannot decode other varieties of motion JPEG.</span></span> <span data-ttu-id="986b3-131">在這些情況下，您將需要使用協力廠商的解碼篩選器。</span><span class="sxs-lookup"><span data-stu-id="986b3-131">For these, you will need to use a third-party decoder filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="986b3-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="986b3-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="986b3-133">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="986b3-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



