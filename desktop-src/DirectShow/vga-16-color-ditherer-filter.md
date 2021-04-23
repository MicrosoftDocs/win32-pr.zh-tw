---
description: VGA 16 色 Ditherer 濾波器
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: VGA 16 色 Ditherer 濾波器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d343843b002eb205e1d0718b282546bdc19907
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908676"
---
# <a name="vga-16-color-ditherer-filter"></a><span data-ttu-id="253be-103">VGA 16 色 Ditherer 濾波器</span><span class="sxs-lookup"><span data-stu-id="253be-103">VGA 16 Color Ditherer Filter</span></span>

<span data-ttu-id="253be-104">VGA 16 色 Ditherer 濾波器會從 RGB 色彩類型轉換成4位色彩，讓 AVI 和 MPEG 視頻資料流程可以顯示在較舊的16色監視器上。</span><span class="sxs-lookup"><span data-stu-id="253be-104">The VGA 16 Color Ditherer filter converts from an RGB color type to a 4-bit color display so that AVI and MPEG video streams may be displayed on older 16-color monitors.</span></span> <span data-ttu-id="253be-105">此篩選器會在解壓縮程式篩選器和影片轉譯器篩選器之間的圖形中插入。</span><span class="sxs-lookup"><span data-stu-id="253be-105">This filter is inserted in the graph between a decompressor filter and a video renderer filter.</span></span>



| <span data-ttu-id="253be-106">標籤</span><span class="sxs-lookup"><span data-stu-id="253be-106">Label</span></span> | <span data-ttu-id="253be-107">值</span><span class="sxs-lookup"><span data-stu-id="253be-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="253be-108">篩選介面</span><span class="sxs-lookup"><span data-stu-id="253be-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="253be-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="253be-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="253be-110">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="253be-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="253be-111">媒體媒體 \_ 、MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="253be-111">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB8</span></span>                                                                                                               |
| <span data-ttu-id="253be-112">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="253be-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="253be-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="253be-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="253be-114">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="253be-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="253be-115">媒體媒體 \_ 、MEDIASUBTYPE \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="253be-115">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB4</span></span>                                                                                                               |
| <span data-ttu-id="253be-116">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="253be-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="253be-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="253be-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="253be-118">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="253be-118">Filter CLSID</span></span>                             | <span data-ttu-id="253be-119">CLSID \_ 遞色</span><span class="sxs-lookup"><span data-stu-id="253be-119">CLSID\_Dither</span></span>                                                                                                                                      |
| <span data-ttu-id="253be-120">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="253be-120">Property Page CLSID</span></span>                      | <span data-ttu-id="253be-121">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="253be-121">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="253be-122">可執行檔</span><span class="sxs-lookup"><span data-stu-id="253be-122">Executable</span></span>                               | <span data-ttu-id="253be-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="253be-123">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="253be-124">優點</span><span class="sxs-lookup"><span data-stu-id="253be-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="253be-125">不 \_ 太可能</span><span class="sxs-lookup"><span data-stu-id="253be-125">MERIT\_UNLIKELY</span></span>                                                                                                                                    |
| [<span data-ttu-id="253be-126">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="253be-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="253be-127">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="253be-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="253be-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="253be-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="253be-129">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="253be-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



