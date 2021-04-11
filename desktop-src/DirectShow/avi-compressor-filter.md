---
description: AVI 壓縮程式篩選
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: AVI 壓縮程式篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3ef342d1ea740503d9fc1e9e9b898aadc3801
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845719"
---
# <a name="avi-compressor-filter"></a><span data-ttu-id="eace2-103">AVI 壓縮程式篩選</span><span class="sxs-lookup"><span data-stu-id="eace2-103">AVI Compressor Filter</span></span>

<span data-ttu-id="eace2-104">AVI 壓縮程式篩選器可讓影片壓縮管理員 (BC-VCM-LVM-HYPERV) 編解碼器來聯結篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="eace2-104">The AVI Compressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="eace2-105">每個編解碼器都會顯示為篩選準則的個別實例。</span><span class="sxs-lookup"><span data-stu-id="eace2-105">Each codec appears as a separate instance of the filter.</span></span> <span data-ttu-id="eace2-106">您無法使用 CoCreateInstance 直接建立此篩選器。</span><span class="sxs-lookup"><span data-stu-id="eace2-106">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="eace2-107">相反地，您必須使用系統裝置枚舉器。</span><span class="sxs-lookup"><span data-stu-id="eace2-107">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="eace2-108">如需詳細資訊，請參閱 [使用系統裝置枚舉器](using-the-system-device-enumerator.md)。</span><span class="sxs-lookup"><span data-stu-id="eace2-108">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="eace2-109">篩選器的輸入 pin 會連接至輸出未壓縮影片資料的篩選器，例如影片捕獲篩選器或 [AVI 分隔器篩選器](avi-splitter-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="eace2-109">The filter's input pin connects to filters that output uncompressed video data, such as video capture filters or the [AVI Splitter Filter](avi-splitter-filter.md).</span></span> <span data-ttu-id="eace2-110">篩選器的輸出圖釘通常會連接到 MUX 篩選器，例如 [AVI Mux 篩選器](avi-mux-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="eace2-110">The filter's output pin typically connects to a MUX filter, such as the [AVI Mux Filter](avi-mux-filter.md).</span></span>

<span data-ttu-id="eace2-111">如果編解碼器支援舊樣式的 VFW 設定對話方塊或 [關於] 對話方塊，則應用程式可以使用 [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) 介面來顯示它。</span><span class="sxs-lookup"><span data-stu-id="eace2-111">If the codec supports an old-style VFW configuration dialog box or About dialog box, an application can display it using the [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) interface.</span></span>

> [!Note]  
> <span data-ttu-id="eace2-112">MPEG 壓縮機絕不會實作為 BC-VCM-LVM-HYPERV 編解碼器，而只會實作為原生的 DirectShow 篩選。</span><span class="sxs-lookup"><span data-stu-id="eace2-112">MPEG compressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eace2-113">篩選介面</span><span class="sxs-lookup"><span data-stu-id="eace2-113">Filter Interfaces</span></span>                        | <span data-ttu-id="eace2-114">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)、 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、IPersistPropertyBag、ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="eace2-114">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span></span>                                                                                                             |
| <span data-ttu-id="eace2-115">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="eace2-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="eace2-116">媒體媒體 \_ 、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="eace2-116">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="eace2-117">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="eace2-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="eace2-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="eace2-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="eace2-119">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="eace2-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="eace2-120">媒體媒體 \_ 、MEDIASUBTYPE \_ Null</span><span class="sxs-lookup"><span data-stu-id="eace2-120">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="eace2-121">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="eace2-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="eace2-122">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)、 [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)、 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="eace2-122">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="eace2-123">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="eace2-123">Filter CLSID</span></span>                             | <span data-ttu-id="eace2-124">不適用</span><span class="sxs-lookup"><span data-stu-id="eace2-124">Not applicable</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="eace2-125">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="eace2-125">Property Page CLSID</span></span>                      | <span data-ttu-id="eace2-126">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="eace2-126">No property page.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="eace2-127">可執行檔</span><span class="sxs-lookup"><span data-stu-id="eace2-127">Executable</span></span>                               | <span data-ttu-id="eace2-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="eace2-128">qcap.dll</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="eace2-129">優點</span><span class="sxs-lookup"><span data-stu-id="eace2-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="eace2-130">\_ \_ 未 \_ 使用的業績</span><span class="sxs-lookup"><span data-stu-id="eace2-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="eace2-131">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="eace2-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="eace2-132">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="eace2-132">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="eace2-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="eace2-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eace2-134">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="eace2-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



