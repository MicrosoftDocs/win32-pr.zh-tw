---
description: DV 分隔器篩選
ms.assetid: 099d1cc7-f0c5-4c50-a1d5-f2defde7e104
title: DV 分隔器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ca8e856f1a49ff22ee05f7dc0ae341fad6aa91
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908406"
---
# <a name="dv-splitter-filter"></a><span data-ttu-id="b1861-103">DV 分隔器篩選</span><span class="sxs-lookup"><span data-stu-id="b1861-103">DV Splitter Filter</span></span>

<span data-ttu-id="b1861-104">此篩選器會將交錯數位視訊 (DV) stream 分割成其元件的影片和音訊串流。</span><span class="sxs-lookup"><span data-stu-id="b1861-104">This filter splits an interleaved digital video (DV) stream into its component video and audio streams.</span></span>



| <span data-ttu-id="b1861-105">標籤</span><span class="sxs-lookup"><span data-stu-id="b1861-105">Label</span></span> | <span data-ttu-id="b1861-106">值</span><span class="sxs-lookup"><span data-stu-id="b1861-106">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1861-107">篩選介面</span><span class="sxs-lookup"><span data-stu-id="b1861-107">Filter Interfaces</span></span>                        | <span data-ttu-id="b1861-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)、 [ **IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)</span><span class="sxs-lookup"><span data-stu-id="b1861-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)</span></span>                                                                             |
| <span data-ttu-id="b1861-109">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="b1861-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="b1861-110">媒體 \_ 中交錯、MEDIASUBTYPE \_ DVSD、格式 \_ DvInfo</span><span class="sxs-lookup"><span data-stu-id="b1861-110">MEDIATYPE\_Interleaved, MEDIASUBTYPE\_dvsd, FORMAT\_DvInfo</span></span>                                                                                         |
| <span data-ttu-id="b1861-111">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="b1861-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="b1861-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="b1861-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="b1861-113">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="b1861-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="b1861-114">**影片**：媒體媒體 \_ ，格式 \_ DvInfo</span><span class="sxs-lookup"><span data-stu-id="b1861-114">**Video**: MEDIATYPE\_Video, FORMAT\_DvInfo</span></span><br/> <span data-ttu-id="b1861-115">**音訊**：媒體媒體 \_ 、MEDIASUBTYPE \_ PCM、格式 \_ WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="b1861-115">**Audio**: MEDIATYPE\_Audio, MEDIASUBTYPE\_PCM, FORMAT\_WaveFormatEx</span></span><br/>             |
| <span data-ttu-id="b1861-116">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="b1861-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="b1861-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)、 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)、 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)、 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="b1861-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="b1861-118">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="b1861-118">Filter CLSID</span></span>                             | <span data-ttu-id="b1861-119">CLSID \_ DVSplitter</span><span class="sxs-lookup"><span data-stu-id="b1861-119">CLSID\_DVSplitter</span></span>                                                                                                                                  |
| <span data-ttu-id="b1861-120">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="b1861-120">Property Page CLSID</span></span>                      | <span data-ttu-id="b1861-121">沒有屬性頁。</span><span class="sxs-lookup"><span data-stu-id="b1861-121">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="b1861-122">可執行檔</span><span class="sxs-lookup"><span data-stu-id="b1861-122">Executable</span></span>                               | <span data-ttu-id="b1861-123">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="b1861-123">qdv.dll</span></span>                                                                                                                                            |
| [<span data-ttu-id="b1861-124">優點</span><span class="sxs-lookup"><span data-stu-id="b1861-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="b1861-125">一般的業績 \_</span><span class="sxs-lookup"><span data-stu-id="b1861-125">MERIT\_NORMAL</span></span>                                                                                                                                      |
| [<span data-ttu-id="b1861-126">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="b1861-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="b1861-127">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="b1861-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="b1861-128">備註</span><span class="sxs-lookup"><span data-stu-id="b1861-128">Remarks</span></span>

<span data-ttu-id="b1861-129">DV 框架在相同的框架中包含音訊和影片。</span><span class="sxs-lookup"><span data-stu-id="b1861-129">DV frames contain audio and video in the same frame.</span></span> <span data-ttu-id="b1861-130">DV 分隔器篩選器會將音訊資料解壓縮，並以一或兩個音訊串流的形式從音訊輸出圖釘傳遞。</span><span class="sxs-lookup"><span data-stu-id="b1861-130">The DV Splitter filter extracts the audio data and delivers it as one or two audio streams, from the audio output pins.</span></span> <span data-ttu-id="b1861-131">原始的 DV 框架是從影片輸出圖釘以影片框架的形式傳遞。</span><span class="sxs-lookup"><span data-stu-id="b1861-131">The original DV frame is delivered from the video output pin, as a video frame.</span></span> <span data-ttu-id="b1861-132">影片畫面上的媒體類型已從 [媒體媒體類型] 變更為 [媒體類型] \_ \_ 影片，否則不會修改資料。</span><span class="sxs-lookup"><span data-stu-id="b1861-132">The media type on the video frame is changed from MEDIATYPE\_Interleaved to MEDIATYPE\_Video, but otherwise the data is not modified.</span></span> <span data-ttu-id="b1861-133">媒體類型會變更，以表示應忽略畫面中的音訊資料。</span><span class="sxs-lookup"><span data-stu-id="b1861-133">The media type is changed to signal that the audio data into the frame should be ignored.</span></span> <span data-ttu-id="b1861-134">DV 分隔器不會在其輸出範例上設定媒體時間;如果您要撰寫需要媒體時間的下游篩選器，則可以從框架計數衍生時間。</span><span class="sxs-lookup"><span data-stu-id="b1861-134">The DV Splitter does not set a media time on its output samples; if you are writing a downstream filter that requires the media times, then you can derive the times from the frame count.</span></span>

<span data-ttu-id="b1861-135">一次只有一個輸出圖釘會公開 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 和 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面。</span><span class="sxs-lookup"><span data-stu-id="b1861-135">Only one output pin at a time exposes the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interfaces.</span></span>

<span data-ttu-id="b1861-136">DV 分隔器篩選器可以接受音訊資料流程中的動態格式變更。</span><span class="sxs-lookup"><span data-stu-id="b1861-136">The DV Splitter filter can accept dynamic format changes in the audio stream.</span></span> <span data-ttu-id="b1861-137">但是，如果 [AVI Mux](avi-mux-filter.md) 篩選器是下游的，則會拒絕格式變更。</span><span class="sxs-lookup"><span data-stu-id="b1861-137">However, if the [AVI Mux](avi-mux-filter.md) filter is downstream, it will reject the format change.</span></span> <span data-ttu-id="b1861-138">如果發生這種情況，DV 分隔器會停止產生音訊串流。</span><span class="sxs-lookup"><span data-stu-id="b1861-138">If this happens, the DV Splitter stops producing an audio stream.</span></span> <span data-ttu-id="b1861-139">這項限制只會影響類型2的檔案捕捉。</span><span class="sxs-lookup"><span data-stu-id="b1861-139">This limitation only affects type-2 file capture.</span></span> <span data-ttu-id="b1861-140">針對類型1檔案，交錯資料流程不會在第一個位置進行分割。</span><span class="sxs-lookup"><span data-stu-id="b1861-140">For type-1 files, the interleaved stream is not split in the first place.</span></span> <span data-ttu-id="b1861-141">若為預覽版本，則不會下游有 AVI Mux 篩選。</span><span class="sxs-lookup"><span data-stu-id="b1861-141">For preview, there is no AVI Mux filter downstream.</span></span>

<span data-ttu-id="b1861-142">如果 DV 來源是即時攝影機，則通常不會有變更音訊格式的原因。</span><span class="sxs-lookup"><span data-stu-id="b1861-142">If the DV source is a live camera, there is normally no reason for the audio format to change.</span></span> <span data-ttu-id="b1861-143">但是，如果您從包含數個異類來源的 VTR 磁帶進行傳輸，格式可能會變更。</span><span class="sxs-lookup"><span data-stu-id="b1861-143">However, the format might change if you transmit from a VTR tape that contains several heterogeneous sources.</span></span>

<span data-ttu-id="b1861-144">除了音訊和影片資料之外，每個 DV 框架還包含中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b1861-144">Each DV frame contains metadata, in addition to the audio and video data.</span></span> <span data-ttu-id="b1861-145">此中繼資料可以從框架變更為框架。</span><span class="sxs-lookup"><span data-stu-id="b1861-145">This metadata can change from frame to frame.</span></span> <span data-ttu-id="b1861-146">應用程式可以藉由檢查輸入範例或影片輸出範例來剖析中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b1861-146">Applications can parse the metadata by examining either the input samples or the video output samples.</span></span> <span data-ttu-id="b1861-147">但是，DirectShow 並不提供任何直接支援來剖析 DV 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b1861-147">However, DirectShow does not provide any direct support for parsing DV metadata.</span></span> <span data-ttu-id="b1861-148">如需詳細資訊，請參閱 IEC 61834-4。</span><span class="sxs-lookup"><span data-stu-id="b1861-148">Consult IEC 61834-4 for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1861-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="b1861-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1861-150">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="b1861-150">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="b1861-151">DirectShow 中的數位視訊</span><span class="sxs-lookup"><span data-stu-id="b1861-151">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 




