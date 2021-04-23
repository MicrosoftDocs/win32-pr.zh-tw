---
description: AVI 解壓縮程式篩選
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: AVI 解壓縮程式篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ccfeee18a01fa9c8d52ffbf4593b9de5664bb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910096"
---
# <a name="avi-decompressor-filter"></a><span data-ttu-id="892b9-103">AVI 解壓縮程式篩選</span><span class="sxs-lookup"><span data-stu-id="892b9-103">AVI Decompressor Filter</span></span>

<span data-ttu-id="892b9-104">AVI 解壓縮程式篩選器可讓影片壓縮管理員 (BC-VCM-LVM-HYPERV) 編解碼器來聯結篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="892b9-104">The AVI Decompressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="892b9-105">應用程式不需要將篩選新增至篩選圖形;篩選圖形管理員會在需要時自動提取。</span><span class="sxs-lookup"><span data-stu-id="892b9-105">The application does not need to add the filter to the filter graph; it is pulled in automatically by the Filter Graph Manager when needed.</span></span>

<span data-ttu-id="892b9-106">當篩選圖形管理員建立圖形來轉譯 AVI 檔案時，它會檢查檔案的 AVI 標頭中的 FOURCC，以判斷影片資料流程是否已壓縮。</span><span class="sxs-lookup"><span data-stu-id="892b9-106">When the Filter Graph Manager is building a graph to render an AVI file, it checks the FOURCC in the file's AVI header to determine whether the video stream is compressed.</span></span> <span data-ttu-id="892b9-107">如果是，則篩選圖形管理員會新增 AVI 解壓縮程式，然後在登錄中搜尋可處理檔案的已安裝解壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="892b9-107">If it is, the Filter Graph Manager adds the AVI Decompressor, which then searches the registry for an installed decompressor that can handle the file.</span></span>

> [!Note]  
> <span data-ttu-id="892b9-108">MPEG decompressors 絕不會實作為 BC-VCM-LVM-HYPERV 編解碼器，而只會實作為原生的 DirectShow 篩選。</span><span class="sxs-lookup"><span data-stu-id="892b9-108">MPEG decompressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 

<span data-ttu-id="892b9-109">在其上游釘選上，AVI 解壓縮器通常會連接到 [Avi 分隔器](avi-splitter-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="892b9-109">On its upstream pin the AVI Decompressor typically connects to the [AVI Splitter](avi-splitter-filter.md).</span></span> <span data-ttu-id="892b9-110">在其輸出釘選上，通常會連接到 [影片](video-renderer-filter.md) 轉譯 [器或 AVI Mux 篩選器](avi-mux-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="892b9-110">On its output pin it typically connects to the [Video Renderer](video-renderer-filter.md) or the [AVI Mux Filter](avi-mux-filter.md).</span></span>



| <span data-ttu-id="892b9-111">標籤</span><span class="sxs-lookup"><span data-stu-id="892b9-111">Label</span></span> | <span data-ttu-id="892b9-112">值</span><span class="sxs-lookup"><span data-stu-id="892b9-112">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="892b9-113">篩選介面</span><span class="sxs-lookup"><span data-stu-id="892b9-113">Filter Interfaces</span></span>                        | [<span data-ttu-id="892b9-114">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="892b9-114">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| <span data-ttu-id="892b9-115">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="892b9-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="892b9-116">主要類型：媒體類型 \_ VideoSubtype：必須對應到壓縮類型的 FOURCC 程式碼。</span><span class="sxs-lookup"><span data-stu-id="892b9-116">Major type: MEDIATYPE\_VideoSubtype: Must correspond to the FOURCC code for the compression type.</span></span> <span data-ttu-id="892b9-117">如需詳細資訊，請參閱 [FOURCC 代碼](fourcc-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="892b9-117">For more information, see [FOURCC Codes](fourcc-codes.md).</span></span><br/> <span data-ttu-id="892b9-118">格式類型： \_ VIDEOINFO 格式</span><span class="sxs-lookup"><span data-stu-id="892b9-118">Format type: FORMAT\_VideoInfo</span></span><br/> |
| <span data-ttu-id="892b9-119">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="892b9-119">Input Pin Interfaces</span></span>                     | <span data-ttu-id="892b9-120">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="892b9-120">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                             |
| <span data-ttu-id="892b9-121">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="892b9-121">Output Pin Media Types</span></span>                   | <span data-ttu-id="892b9-122">媒體媒體 \_ 、MEDIASUBTYPE \_ Null、FORMAT \_ VideoInfo</span><span class="sxs-lookup"><span data-stu-id="892b9-122">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL, FORMAT\_VideoInfo</span></span>                                                                                                                                                            |
| <span data-ttu-id="892b9-123">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="892b9-123">Output Pin Interfaces</span></span>                    | <span data-ttu-id="892b9-124">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="892b9-124">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                 |
| <span data-ttu-id="892b9-125">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="892b9-125">Filter CLSID</span></span>                             | <span data-ttu-id="892b9-126">CLSID \_ AVIDec</span><span class="sxs-lookup"><span data-stu-id="892b9-126">CLSID\_AVIDec</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="892b9-127">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="892b9-127">Property Page CLSID</span></span>                      | <span data-ttu-id="892b9-128">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="892b9-128">No property page.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="892b9-129">可執行檔</span><span class="sxs-lookup"><span data-stu-id="892b9-129">Executable</span></span>                               | <span data-ttu-id="892b9-130">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="892b9-130">quartz.dll</span></span>                                                                                                                                                                                                         |
| [<span data-ttu-id="892b9-131">優點</span><span class="sxs-lookup"><span data-stu-id="892b9-131">Merit</span></span>](merit.md)                       | <span data-ttu-id="892b9-132">一般的業績 \_</span><span class="sxs-lookup"><span data-stu-id="892b9-132">MERIT\_NORMAL</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="892b9-133">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="892b9-133">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="892b9-134">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="892b9-134">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="892b9-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="892b9-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="892b9-136">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="892b9-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




