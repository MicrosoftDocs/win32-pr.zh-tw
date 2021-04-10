---
description: VGA 16 色 Ditherer 濾波器
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: VGA 16 色 Ditherer 濾波器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85db9d8fad706c96f19bb5bea6b0476b0ddec735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027043"
---
# <a name="vga-16-color-ditherer-filter"></a><span data-ttu-id="43e7c-103">VGA 16 色 Ditherer 濾波器</span><span class="sxs-lookup"><span data-stu-id="43e7c-103">VGA 16 Color Ditherer Filter</span></span>

<span data-ttu-id="43e7c-104">VGA 16 色 Ditherer 濾波器會從 RGB 色彩類型轉換成4位色彩，讓 AVI 和 MPEG 視頻資料流程可以顯示在較舊的16色監視器上。</span><span class="sxs-lookup"><span data-stu-id="43e7c-104">The VGA 16 Color Ditherer filter converts from an RGB color type to a 4-bit color display so that AVI and MPEG video streams may be displayed on older 16-color monitors.</span></span> <span data-ttu-id="43e7c-105">此篩選器會在解壓縮程式篩選器和影片轉譯器篩選器之間的圖形中插入。</span><span class="sxs-lookup"><span data-stu-id="43e7c-105">This filter is inserted in the graph between a decompressor filter and a video renderer filter.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43e7c-106">篩選介面</span><span class="sxs-lookup"><span data-stu-id="43e7c-106">Filter Interfaces</span></span>                        | [<span data-ttu-id="43e7c-107">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="43e7c-107">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="43e7c-108">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="43e7c-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="43e7c-109">媒體媒體 \_ 、MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="43e7c-109">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB8</span></span>                                                                                                               |
| <span data-ttu-id="43e7c-110">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="43e7c-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="43e7c-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="43e7c-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="43e7c-112">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="43e7c-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="43e7c-113">媒體媒體 \_ 、MEDIASUBTYPE \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="43e7c-113">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB4</span></span>                                                                                                               |
| <span data-ttu-id="43e7c-114">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="43e7c-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="43e7c-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="43e7c-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="43e7c-116">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="43e7c-116">Filter CLSID</span></span>                             | <span data-ttu-id="43e7c-117">CLSID \_ 遞色</span><span class="sxs-lookup"><span data-stu-id="43e7c-117">CLSID\_Dither</span></span>                                                                                                                                      |
| <span data-ttu-id="43e7c-118">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="43e7c-118">Property Page CLSID</span></span>                      | <span data-ttu-id="43e7c-119">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="43e7c-119">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="43e7c-120">可執行檔</span><span class="sxs-lookup"><span data-stu-id="43e7c-120">Executable</span></span>                               | <span data-ttu-id="43e7c-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="43e7c-121">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="43e7c-122">優點</span><span class="sxs-lookup"><span data-stu-id="43e7c-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="43e7c-123">不 \_ 太可能</span><span class="sxs-lookup"><span data-stu-id="43e7c-123">MERIT\_UNLIKELY</span></span>                                                                                                                                    |
| [<span data-ttu-id="43e7c-124">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="43e7c-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="43e7c-125">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="43e7c-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="43e7c-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="43e7c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43e7c-127">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="43e7c-127">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



