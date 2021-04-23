---
description: MJPEG 壓縮程式篩選器
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: MJPEG 壓縮程式篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02928df4d09b50c0ac152aed99ed87dc6362fb70
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910006"
---
# <a name="mjpeg-compressor-filter"></a><span data-ttu-id="83227-103">MJPEG 壓縮程式篩選器</span><span class="sxs-lookup"><span data-stu-id="83227-103">MJPEG Compressor Filter</span></span>

<span data-ttu-id="83227-104">此篩選器會使用動畫 JPEG 壓縮來壓縮未壓縮的影片串流。</span><span class="sxs-lookup"><span data-stu-id="83227-104">This filter compresses an uncompressed video stream, using motion JPEG compression.</span></span>



| <span data-ttu-id="83227-105">標籤</span><span class="sxs-lookup"><span data-stu-id="83227-105">Label</span></span> | <span data-ttu-id="83227-106">值</span><span class="sxs-lookup"><span data-stu-id="83227-106">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83227-107">篩選介面</span><span class="sxs-lookup"><span data-stu-id="83227-107">Filter Interfaces</span></span>                        | <span data-ttu-id="83227-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="83227-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="83227-109">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="83227-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="83227-110">媒體媒體 \_ 、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="83227-110">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="83227-111">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="83227-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="83227-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="83227-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="83227-113">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="83227-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="83227-114">媒體媒體 \_ 、MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="83227-114">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="83227-115">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="83227-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="83227-116">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)、 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)、 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="83227-116">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="83227-117">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="83227-117">Filter CLSID</span></span>                             | <span data-ttu-id="83227-118">CLSID \_ MJPGEnc</span><span class="sxs-lookup"><span data-stu-id="83227-118">CLSID\_MJPGEnc</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="83227-119">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="83227-119">Property Page CLSID</span></span>                      | <span data-ttu-id="83227-120">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="83227-120">No property page</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="83227-121">可執行檔</span><span class="sxs-lookup"><span data-stu-id="83227-121">Executable</span></span>                               | <span data-ttu-id="83227-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="83227-122">quartz.dll</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="83227-123">優點</span><span class="sxs-lookup"><span data-stu-id="83227-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="83227-124">\_ \_ 未 \_ 使用的業績</span><span class="sxs-lookup"><span data-stu-id="83227-124">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="83227-125">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="83227-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="83227-126">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="83227-126">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="83227-127">備註</span><span class="sxs-lookup"><span data-stu-id="83227-127">Remarks</span></span>

<span data-ttu-id="83227-128">此篩選準則會使用 \_ 對應至 FOURCC 碼 ' MJPG ' 的媒體子類型 MEDIASUBTYPE MJPG 來進行編碼。</span><span class="sxs-lookup"><span data-stu-id="83227-128">This filter encodes using the media subtype MEDIASUBTYPE\_MJPG, which corresponds to the FOURCC code 'MJPG'.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83227-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="83227-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83227-130">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="83227-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



