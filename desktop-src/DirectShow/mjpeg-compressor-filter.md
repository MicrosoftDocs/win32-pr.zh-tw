---
description: MJPEG 壓縮程式篩選器
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: MJPEG 壓縮程式篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a20c559bb889750959a4868fa08c03b3eb12dfb5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972534"
---
# <a name="mjpeg-compressor-filter"></a><span data-ttu-id="6b2ef-103">MJPEG 壓縮程式篩選器</span><span class="sxs-lookup"><span data-stu-id="6b2ef-103">MJPEG Compressor Filter</span></span>

<span data-ttu-id="6b2ef-104">此篩選器會使用動畫 JPEG 壓縮來壓縮未壓縮的影片串流。</span><span class="sxs-lookup"><span data-stu-id="6b2ef-104">This filter compresses an uncompressed video stream, using motion JPEG compression.</span></span>



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b2ef-105">篩選介面</span><span class="sxs-lookup"><span data-stu-id="6b2ef-105">Filter Interfaces</span></span>                        | <span data-ttu-id="6b2ef-106">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="6b2ef-106">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="6b2ef-107">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="6b2ef-107">Input Pin Media Types</span></span>                    | <span data-ttu-id="6b2ef-108">媒體媒體 \_ 、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="6b2ef-108">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="6b2ef-109">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="6b2ef-109">Input Pin Interfaces</span></span>                     | <span data-ttu-id="6b2ef-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="6b2ef-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="6b2ef-111">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="6b2ef-111">Output Pin Media Types</span></span>                   | <span data-ttu-id="6b2ef-112">媒體媒體 \_ 、MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="6b2ef-112">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="6b2ef-113">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="6b2ef-113">Output Pin Interfaces</span></span>                    | <span data-ttu-id="6b2ef-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)、 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)、 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="6b2ef-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="6b2ef-115">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="6b2ef-115">Filter CLSID</span></span>                             | <span data-ttu-id="6b2ef-116">CLSID \_ MJPGEnc</span><span class="sxs-lookup"><span data-stu-id="6b2ef-116">CLSID\_MJPGEnc</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="6b2ef-117">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="6b2ef-117">Property Page CLSID</span></span>                      | <span data-ttu-id="6b2ef-118">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="6b2ef-118">No property page</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="6b2ef-119">可執行檔</span><span class="sxs-lookup"><span data-stu-id="6b2ef-119">Executable</span></span>                               | <span data-ttu-id="6b2ef-120">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="6b2ef-120">quartz.dll</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="6b2ef-121">優點</span><span class="sxs-lookup"><span data-stu-id="6b2ef-121">Merit</span></span>](merit.md)                       | <span data-ttu-id="6b2ef-122">\_ \_ 未 \_ 使用的業績</span><span class="sxs-lookup"><span data-stu-id="6b2ef-122">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="6b2ef-123">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="6b2ef-123">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="6b2ef-124">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="6b2ef-124">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="6b2ef-125">備註</span><span class="sxs-lookup"><span data-stu-id="6b2ef-125">Remarks</span></span>

<span data-ttu-id="6b2ef-126">此篩選準則會使用 \_ 對應至 FOURCC 碼 ' MJPG ' 的媒體子類型 MEDIASUBTYPE MJPG 來進行編碼。</span><span class="sxs-lookup"><span data-stu-id="6b2ef-126">This filter encodes using the media subtype MEDIASUBTYPE\_MJPG, which corresponds to the FOURCC code 'MJPG'.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b2ef-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="6b2ef-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b2ef-128">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="6b2ef-128">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



