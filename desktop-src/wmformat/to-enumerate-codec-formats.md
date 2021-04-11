---
title: 列舉編解碼器格式
description: 列舉編解碼器格式
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- 串流，列舉編解碼器格式
- 編解碼器，列舉
- 資料流程、編解碼器格式
- 編解碼器，格式
- 編解碼器，IWMCodecInfo 介面
- IWMCodecInfo，編解碼器格式
- 編解碼器，IWMCodecInfo3 介面
- IWMCodecInfo3，編解碼器格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ea062723ec1480a82b45fd025fb7a8c37020d5
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104023162"
---
# <a name="to-enumerate-codec-formats"></a><span data-ttu-id="5f2f7-111">列舉編解碼器格式</span><span class="sxs-lookup"><span data-stu-id="5f2f7-111">To Enumerate Codec Formats</span></span>

<span data-ttu-id="5f2f7-112">編解碼器格式是以編解碼器資料填入的串流設定物件。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-112">A codec format is a stream configuration object populated with data from a codec.</span></span> <span data-ttu-id="5f2f7-113">每個編解碼器格式都包含編解碼器所支援的媒體設定。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-113">Each codec format contains a media configuration supported by the codec.</span></span> <span data-ttu-id="5f2f7-114">大部分音訊編解碼器都支援有限數量的格式，每個都是由編解碼器列舉，而且可以使用 [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)的方法來存取。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-114">Most audio codecs support a finite number of formats, each of which is enumerated by the codec and can be accessed using the methods of [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo).</span></span> <span data-ttu-id="5f2f7-115">另一方面，視頻編解碼器只提供單一格式。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-115">Video codecs, on the other hand, provide only a single format.</span></span> <span data-ttu-id="5f2f7-116">這是因為影片串流具有比音訊串流設定更具彈性的變數，例如框架大小。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-116">This is because video streams have variables, like frame size, that are more flexible than the settings of an audio stream.</span></span> <span data-ttu-id="5f2f7-117">使用影片串流時，您必須填入部分串流設定值;音訊串流設定只能進行編輯，以指派名稱、連線名稱和串流號碼。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-117">With a video stream, you must fill in some of the stream configuration values; audio stream configurations should only be edited to assign a name, connection name, and stream number.</span></span> <span data-ttu-id="5f2f7-118">如需詳細資訊，請參閱 [所有資料流程的通用](configuration-common-to-all-streams.md)設定。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-118">For more information, see [Configuration Common to All Streams](configuration-common-to-all-streams.md).</span></span>

<span data-ttu-id="5f2f7-119">列舉的編解碼器格式取決於目前使用 [**IWMCodecInfo3：： SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting)設定的編解碼器列舉設定。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-119">The codec formats enumerated depend upon the current codec enumeration settings, which are set using [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting).</span></span> <span data-ttu-id="5f2f7-120">目前只支援兩種編解碼器屬性： g \_ wszNumPasses，它會指定編解碼器將執行的編碼傳遞數目，而 g \_ wszVBREnabled 則指定編解碼器是否會使用可變的位元速率編碼。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-120">Currently, only two codec properties are supported: g\_wszNumPasses, which specifies the number of encoding passes that the codec will perform, and g\_wszVBREnabled, which specifies whether the codec will use variable bit rate encoding.</span></span> <span data-ttu-id="5f2f7-121">任何編解碼器支援的最大編碼傳遞數目是兩個，因此有四個不同的設定可供您抓取編解碼器，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-121">The maximum number of encoding passes supported by any of the codecs is two, so there are four distinct configurations for which you can retrieve codecs, as shown in the following table.</span></span>



|                  | <span data-ttu-id="5f2f7-122">固定位元速率 (CBR) 資料流程</span><span class="sxs-lookup"><span data-stu-id="5f2f7-122">Constant bit rate (CBR) stream</span></span> | <span data-ttu-id="5f2f7-123">2-通過 CBR 串流</span><span class="sxs-lookup"><span data-stu-id="5f2f7-123">2-pass CBR stream</span></span> | <span data-ttu-id="5f2f7-124">以品質為基礎的變數位元速率 (VBR) 資料流程</span><span class="sxs-lookup"><span data-stu-id="5f2f7-124">Quality-based variable bit rate (VBR) stream</span></span> | <span data-ttu-id="5f2f7-125">以位速率為基礎的 VBR 串流 (受限或不受限制的) </span><span class="sxs-lookup"><span data-stu-id="5f2f7-125">Bit-rate-based VBR stream (constrained or unconstrained)</span></span> |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="5f2f7-126">g \_ wszVBREnabled</span><span class="sxs-lookup"><span data-stu-id="5f2f7-126">g\_wszVBREnabled</span></span> | <span data-ttu-id="5f2f7-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="5f2f7-127">FALSE</span></span>                          | <span data-ttu-id="5f2f7-128">FALSE</span><span class="sxs-lookup"><span data-stu-id="5f2f7-128">FALSE</span></span>             | <span data-ttu-id="5f2f7-129">TRUE</span><span class="sxs-lookup"><span data-stu-id="5f2f7-129">TRUE</span></span>                                         | <span data-ttu-id="5f2f7-130">true</span><span class="sxs-lookup"><span data-stu-id="5f2f7-130">TRUE</span></span>                                                     |
| <span data-ttu-id="5f2f7-131">g \_ wszNumPasses</span><span class="sxs-lookup"><span data-stu-id="5f2f7-131">g\_wszNumPasses</span></span>  | <span data-ttu-id="5f2f7-132">1</span><span class="sxs-lookup"><span data-stu-id="5f2f7-132">1</span></span>                              | <span data-ttu-id="5f2f7-133">2</span><span class="sxs-lookup"><span data-stu-id="5f2f7-133">2</span></span>                 | <span data-ttu-id="5f2f7-134">1</span><span class="sxs-lookup"><span data-stu-id="5f2f7-134">1</span></span>                                            | <span data-ttu-id="5f2f7-135">2</span><span class="sxs-lookup"><span data-stu-id="5f2f7-135">2</span></span>                                                        |



 

<span data-ttu-id="5f2f7-136">若要列舉編解碼器支援的格式，請使用 [**IWMCodecInfo：： GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) 來尋找支援的編解碼器數目。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-136">To enumerate the formats supported for a codec, use [**IWMCodecInfo::GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) to find the number of supported codecs.</span></span> <span data-ttu-id="5f2f7-137">然後針對每個格式呼叫 [**IWMCodecInfo：： GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) 。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-137">Then call [**IWMCodecInfo::GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) for each format.</span></span> <span data-ttu-id="5f2f7-138">格式索引的範圍是從零到1，小於支援的格式總數。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-138">The format indexes range from zero, to one less than the total number of supported formats.</span></span> <span data-ttu-id="5f2f7-139">您可以藉由呼叫 [**IWMCodecInfo2：： GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc)來取出格式的描述。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-139">You can retrieve a description of the format by calling [**IWMCodecInfo2::GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc).</span></span> <span data-ttu-id="5f2f7-140">使用 **GetCodecFormatDesc** 時，您不需要使用 **GetCodecFormat**，因為這兩種方法都會抓取資料流程設定物件。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-140">When using **GetCodecFormatDesc**, you do not need to use **GetCodecFormat**, because the stream configuration object is retrieved by both methods.</span></span> <span data-ttu-id="5f2f7-141">影片編解碼器格式不包含描述。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-141">Video codec formats do not include a description.</span></span> <span data-ttu-id="5f2f7-142">每個影片編解碼器都只有一種格式，可用於該類型的所有資料流程。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-142">Each video codec has only one format that is used for all streams of that type.</span></span>

<span data-ttu-id="5f2f7-143">當您取得編解碼器格式時，您會取得包含格式設定之資料流程設定物件的 [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) 介面。</span><span class="sxs-lookup"><span data-stu-id="5f2f7-143">When you retrieve a codec format, you get the [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) interface of a stream configuration object containing the format settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f2f7-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="5f2f7-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f2f7-145">**從編解碼器取得串流設定資訊**</span><span class="sxs-lookup"><span data-stu-id="5f2f7-145">**Getting Stream Configuration Information from Codecs**</span></span>](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




