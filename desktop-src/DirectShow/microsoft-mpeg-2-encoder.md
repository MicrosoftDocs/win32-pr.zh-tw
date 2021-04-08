---
description: Microsoft MPEG-2 編碼器篩選器會編碼 MPEG-2 音訊和影片，並將分離信號串流以產生 MPEG-2 程式資料流程或傳輸串流。
ms.assetid: 61e8918b-7f5a-4720-bb3b-df9ac7614894
title: 'Microsoft MPEG-2 編碼器 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5fad3b316db9ac4e47efcb9de761227cdd3279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687660"
---
# <a name="microsoft-mpeg-2-encoder"></a><span data-ttu-id="015d1-103">Microsoft MPEG-2 編碼器</span><span class="sxs-lookup"><span data-stu-id="015d1-103">Microsoft MPEG-2 Encoder</span></span>

<span data-ttu-id="015d1-104">Microsoft MPEG-2 編碼器篩選器會編碼 MPEG-2 音訊和影片，並將分離信號串流以產生 MPEG-2 程式資料流程或傳輸串流。</span><span class="sxs-lookup"><span data-stu-id="015d1-104">The Microsoft MPEG-2 Encoder filter encodes MPEG-2 audio and video and multiplexes the streams to generate an MPEG-2 program stream or transport stream.</span></span>

> [!Note]  
> <span data-ttu-id="015d1-105">以 IA-64 為基礎的平臺不支援此篩選器。</span><span class="sxs-lookup"><span data-stu-id="015d1-105">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="015d1-106">篩選資訊</span><span class="sxs-lookup"><span data-stu-id="015d1-106">Filter Information</span></span>

<span data-ttu-id="015d1-107">篩選介面</span><span class="sxs-lookup"><span data-stu-id="015d1-107">Filter Interfaces</span></span>

[<span data-ttu-id="015d1-108">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="015d1-108">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="015d1-109">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="015d1-109">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> <span data-ttu-id="015d1-110">**IEncoderAPI**</span><span class="sxs-lookup"><span data-stu-id="015d1-110">**IEncoderAPI**</span></span><br/> [<span data-ttu-id="015d1-111">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="015d1-111">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="015d1-112">**IVideoEncoder**</span><span class="sxs-lookup"><span data-stu-id="015d1-112">**IVideoEncoder**</span></span>](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

<span data-ttu-id="015d1-113">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="015d1-113">Input Pin Media Types</span></span>

<span data-ttu-id="015d1-114">請參閱備註</span><span class="sxs-lookup"><span data-stu-id="015d1-114">See Remarks</span></span>

<span data-ttu-id="015d1-115">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="015d1-115">Input Pin Interfaces</span></span>

[<span data-ttu-id="015d1-116">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="015d1-116">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="015d1-117">**IPin**</span><span class="sxs-lookup"><span data-stu-id="015d1-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="015d1-118">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="015d1-118">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="015d1-119">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="015d1-119">Output Pin Media Types</span></span>

<span data-ttu-id="015d1-120">請參閱備註</span><span class="sxs-lookup"><span data-stu-id="015d1-120">See Remarks</span></span>

<span data-ttu-id="015d1-121">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="015d1-121">Output Pin Interfaces</span></span>

[<span data-ttu-id="015d1-122">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="015d1-122">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="015d1-123">**IPin**</span><span class="sxs-lookup"><span data-stu-id="015d1-123">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="015d1-124">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="015d1-124">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="015d1-125">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="015d1-125">Filter CLSID</span></span>

<span data-ttu-id="015d1-126">**CLSID \_** 在 wmcodecdsp 中宣告的 CMPEG2EncoderDS () </span><span class="sxs-lookup"><span data-stu-id="015d1-126">**CLSID\_CMPEG2EncoderDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="015d1-127">可執行檔</span><span class="sxs-lookup"><span data-stu-id="015d1-127">Executable</span></span>

<span data-ttu-id="015d1-128">msmpeg2enc.dll</span><span class="sxs-lookup"><span data-stu-id="015d1-128">msmpeg2enc.dll</span></span>

[<span data-ttu-id="015d1-129">優點</span><span class="sxs-lookup"><span data-stu-id="015d1-129">Merit</span></span>](merit.md)

<span data-ttu-id="015d1-130">**\_ \_ 未 \_ 使用的業績**</span><span class="sxs-lookup"><span data-stu-id="015d1-130">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="015d1-131">篩選準則分類</span><span class="sxs-lookup"><span data-stu-id="015d1-131">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="015d1-132">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="015d1-132">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="015d1-133">備註</span><span class="sxs-lookup"><span data-stu-id="015d1-133">Remarks</span></span>

<span data-ttu-id="015d1-134">此篩選器結合兩個其他篩選準則的編碼功能：</span><span class="sxs-lookup"><span data-stu-id="015d1-134">This filter combines the encoding functionality of two other filters:</span></span>

-   [<span data-ttu-id="015d1-135">**Microsoft MPEG-2 音訊編碼器**</span><span class="sxs-lookup"><span data-stu-id="015d1-135">**Microsoft MPEG-2 Audio Encoder**</span></span>](microsoft-mpeg-2-audio-encoder.md)
-   [<span data-ttu-id="015d1-136">**Microsoft MPEG 2 影片編碼器**</span><span class="sxs-lookup"><span data-stu-id="015d1-136">**Microsoft MPEG-2 Video Encoder**</span></span>](microsoft-mpeg-2-video-encoder.md)

<span data-ttu-id="015d1-137">除了所述，此篩選支援與這兩個編碼器相同的編碼功能。</span><span class="sxs-lookup"><span data-stu-id="015d1-137">Except as noted, this filter supports the same encoding features as those two encoders.</span></span>

<span data-ttu-id="015d1-138">一開始，篩選器會有一個輸入 pin，可以接受音訊或影片輸入。</span><span class="sxs-lookup"><span data-stu-id="015d1-138">Initially the filter has one input pin, which can accept audio or video input.</span></span> <span data-ttu-id="015d1-139">連接該 pin 碼時，篩選器會建立第二個輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="015d1-139">When that pin is connected, the filter creates a second input pin.</span></span> <span data-ttu-id="015d1-140">如果第一個輸入釘選到音訊，則第二個輸入 pin 只會接受影片，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="015d1-140">If the first input pin receives audio, the second input pin accepts only video, and vice versa.</span></span> <span data-ttu-id="015d1-141">每個輸入 pin 都支援與對應的編碼器篩選器相同的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="015d1-141">Each input pin supports the same media types as the corresponding encoder filter.</span></span>

<span data-ttu-id="015d1-142">如果只連接一個輸入 pin，則篩選準則支援的輸出類型與對應的音訊或影片編碼器相同。</span><span class="sxs-lookup"><span data-stu-id="015d1-142">If only one input pin is connected, the filter supports the same output types as the corresponding audio or video encoder.</span></span> <span data-ttu-id="015d1-143">如果這兩個 pin 都已連接，則篩選器支援下列類型的輸出：</span><span class="sxs-lookup"><span data-stu-id="015d1-143">If both pins are connected, the filter supports the following kinds of output:</span></span>

-   <span data-ttu-id="015d1-144">音訊-MPEG-2 程式串流中的視覺效果</span><span class="sxs-lookup"><span data-stu-id="015d1-144">Audio-visual in an MPEG-2 program stream</span></span>
-   <span data-ttu-id="015d1-145">音訊-MPEG-2 傳輸串流中的視覺效果</span><span class="sxs-lookup"><span data-stu-id="015d1-145">Audio-visual in an MPEG-2 transport stream</span></span>

<span data-ttu-id="015d1-146">這些會對應至下列輸出類型：</span><span class="sxs-lookup"><span data-stu-id="015d1-146">These correspond to the following output types:</span></span>

-   <span data-ttu-id="015d1-147">**媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG2 \_ 方案**</span><span class="sxs-lookup"><span data-stu-id="015d1-147">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>
-   <span data-ttu-id="015d1-148">**媒體媒體 \_Stream**、 **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**</span><span class="sxs-lookup"><span data-stu-id="015d1-148">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>

<span data-ttu-id="015d1-149">此篩選無法對先前編碼的資料流程進行多工處理。</span><span class="sxs-lookup"><span data-stu-id="015d1-149">This filter cannot multiplex streams that were previously encoded.</span></span> <span data-ttu-id="015d1-150">輸入資料流程必須是未壓縮的音訊/影片，這會在多工處理之前進行篩選編碼。</span><span class="sxs-lookup"><span data-stu-id="015d1-150">The input streams must be uncompressed audio/video, which the filter encodes before multiplexing.</span></span> <span data-ttu-id="015d1-151">多工資料流程受限於一個程式，包含最多一個音訊和一個影片串流。</span><span class="sxs-lookup"><span data-stu-id="015d1-151">The multiplexed stream is limited to one program, containing up to one audio and one video stream.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="015d1-152">編解碼器屬性</span><span class="sxs-lookup"><span data-stu-id="015d1-152">Codec Properties</span></span>

<span data-ttu-id="015d1-153">此篩選支援 [**Mpeg-2 音訊編碼器**](microsoft-mpeg-2-audio-encoder.md) 和 [**mpeg-2 視頻編碼器**](microsoft-mpeg-2-video-encoder.md) 篩選器的結合屬性，但有下列差異：</span><span class="sxs-lookup"><span data-stu-id="015d1-153">The filter supports the combined properties of the [**MPEG-2 Audio Encoder**](microsoft-mpeg-2-audio-encoder.md) and [**MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md) filters, with the following difference:</span></span>

-   <span data-ttu-id="015d1-154">[**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)屬性會設定影片串流的平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="015d1-154">The [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) property sets the average bit rate for the video stream.</span></span>
-   <span data-ttu-id="015d1-155">[**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md)屬性會設定音訊串流的平均位元速率。</span><span class="sxs-lookup"><span data-stu-id="015d1-155">The [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md) property sets the average bit rate for the audio stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="015d1-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="015d1-156">Requirements</span></span>



| <span data-ttu-id="015d1-157">需求</span><span class="sxs-lookup"><span data-stu-id="015d1-157">Requirement</span></span> | <span data-ttu-id="015d1-158">值</span><span class="sxs-lookup"><span data-stu-id="015d1-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="015d1-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="015d1-159">Minimum supported client</span></span><br/> | <span data-ttu-id="015d1-160">Windows Vista Home Premium、Windows Vista 旗艦版、Windows 7 Home Premium、Windows 7 Professional、Windows 7 企業版、僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="015d1-160">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="015d1-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="015d1-161">Minimum supported server</span></span><br/> | <span data-ttu-id="015d1-162">都不支援</span><span class="sxs-lookup"><span data-stu-id="015d1-162">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="015d1-163">標頭</span><span class="sxs-lookup"><span data-stu-id="015d1-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="015d1-164"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="015d1-164"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="015d1-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="015d1-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="015d1-166">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="015d1-166">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
