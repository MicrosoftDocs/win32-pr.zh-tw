---
title: 使用智慧型 Recompression 轉碼內容
description: 使用智慧型 Recompression 轉碼內容
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- Windows Media Format SDK，轉碼內容
- Windows Media Format SDK、smart recompression
- Windows Media Format SDK、recompression
- Windows Media 格式 SDK，Windows Media 音訊編解碼器
- Advanced Systems Format (ASF) 、轉碼內容
- ASF (Advanced Systems Format) 、轉碼內容
- Advanced Systems Format (ASF) 、smart recompression
- ASF (Advanced Systems Format) 、smart recompression
- Advanced Systems Format (ASF) ，recompression
- ASF (Advanced Systems Format) ，recompression
- Advanced Systems Format (ASF) 、Windows Media 音訊編解碼器
- ASF (Advanced Systems Format) Windows Media 音訊編解碼器
- 轉碼內容
- 智慧型 recompression
- recompression
- Windows Media 音訊編解碼器、轉碼內容
- 編解碼器，Windows Media 音訊編解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1317989ea9384d4a9747d712af1ce5c61d484c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314292"
---
# <a name="to-transcode-content-with-smart-recompression"></a><span data-ttu-id="111da-120">使用智慧型 Recompression 轉碼內容</span><span class="sxs-lookup"><span data-stu-id="111da-120">To Transcode Content with Smart Recompression</span></span>

<span data-ttu-id="111da-121">您可以使用 Windows Media Format SDK，從一個位元速率轉碼內容到另一個位元速率。</span><span class="sxs-lookup"><span data-stu-id="111da-121">You can transcode content from one bit rate to another using the Windows Media Format SDK.</span></span> <span data-ttu-id="111da-122">一般來說，這牽涉到直接解碼內容，再將它編碼為所需的位元速率。</span><span class="sxs-lookup"><span data-stu-id="111da-122">Normally, this involves simply decoding the content and encoding it again to the desired bit rate.</span></span> <span data-ttu-id="111da-123">Windows Media 音訊9編解碼器支援智慧型 recompression，可讓轉碼比平常更高的品質。</span><span class="sxs-lookup"><span data-stu-id="111da-123">The Windows Media Audio 9 codec supports smart recompression, which enables transcoding that achieves better quality than normal.</span></span>

<span data-ttu-id="111da-124">針對智慧型 recompression，原始音訊資料流程必須以 Windows Media 音訊編解碼器編碼。</span><span class="sxs-lookup"><span data-stu-id="111da-124">For smart recompression, the original audio stream must be encoded with the Windows Media Audio codec.</span></span> <span data-ttu-id="111da-125">所有版本的編解碼器都受到支援，但特製化音訊編解碼器 (Windows Media 音訊 9 Professional 和 Windows Media 音訊 9 Voice) 不會。</span><span class="sxs-lookup"><span data-stu-id="111da-125">All versions of the codec are supported, but the specialized audio codecs (Windows Media Audio 9 Professional and Windows Media Audio 9 Voice) are not.</span></span> <span data-ttu-id="111da-126">如果原始音訊使用 Windows Media 音訊9無失真編解碼器編碼，則不需要使用智慧型 recompression，因為原始編碼未遺失任何資訊。</span><span class="sxs-lookup"><span data-stu-id="111da-126">If the original audio was encoded with the Windows Media Audio 9 Lossless codec, there is no need to use smart recompression, because no information was lost in the original encoding.</span></span>

<span data-ttu-id="111da-127">若要使用智慧型 recompression，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="111da-127">To use smart recompression, perform the following steps.</span></span>

1.  <span data-ttu-id="111da-128">設定讀取來源檔案的讀取器物件。</span><span class="sxs-lookup"><span data-stu-id="111da-128">Set up a reader object with the source file for reading.</span></span> <span data-ttu-id="111da-129">如需詳細資訊，請參閱 [讀取 ASF](reading-asf-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="111da-129">For more information, see [Reading ASF Files](reading-asf-files.md).</span></span>
2.  <span data-ttu-id="111da-130">設定要用於轉碼檔案的寫入器物件。</span><span class="sxs-lookup"><span data-stu-id="111da-130">Set up a writer object to use for transcoding the file.</span></span> <span data-ttu-id="111da-131">設定新檔案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="111da-131">Set the file name for the new file.</span></span> <span data-ttu-id="111da-132">選取要用於新檔案的設定檔。</span><span class="sxs-lookup"><span data-stu-id="111da-132">Select a profile to use for the new file.</span></span> <span data-ttu-id="111da-133">在寫入器物件中設定選取的設定檔。</span><span class="sxs-lookup"><span data-stu-id="111da-133">Set the selected profile in the writer object.</span></span> <span data-ttu-id="111da-134">如需詳細資訊，請參閱 [寫入 ASF](writing-asf-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="111da-134">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
3.  <span data-ttu-id="111da-135">藉由呼叫 **IWMReader：： QueryInterface**，取得讀取器物件之 [**IWMProfile**](iwmprofile.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="111da-135">Get a pointer to the [**IWMProfile**](iwmprofile.md) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
4.  <span data-ttu-id="111da-136">藉由呼叫 [**IWMProfile：： GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)，取得要轉碼之音訊資料流程的 [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)介面。</span><span class="sxs-lookup"><span data-stu-id="111da-136">Retrieve the [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) interface for the audio stream to be transcoded by calling [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span></span>
5.  <span data-ttu-id="111da-137">藉由呼叫 **IWMStreamConfig：： QueryInterface** 來取得資料流程設定物件的 [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)介面。</span><span class="sxs-lookup"><span data-stu-id="111da-137">Get the [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) interface for the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
6.  <span data-ttu-id="111da-138">對 [**IWMMediaProps：： GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)進行兩次呼叫，以抓取資料流程的 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)結構。</span><span class="sxs-lookup"><span data-stu-id="111da-138">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the stream by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="111da-139">在第一次呼叫時取得結構的大小，並為緩衝區配置記憶體，以在第二次呼叫時傳遞。</span><span class="sxs-lookup"><span data-stu-id="111da-139">Get the size of the structure on the first call, and allocate memory for a buffer to pass on the second call.</span></span>
7.  <span data-ttu-id="111da-140">藉由呼叫 [**IWMWriter：： GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)，取得寫入器中輸入的 [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)介面指標。</span><span class="sxs-lookup"><span data-stu-id="111da-140">Get a pointer to the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input in the writer by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>
8.  <span data-ttu-id="111da-141">藉由呼叫 **IWMInputMediaProps：： QueryInterface** 來取得輸入媒體屬性物件的 [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)介面。</span><span class="sxs-lookup"><span data-stu-id="111da-141">Get the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface for the input media properties object by calling **IWMInputMediaProps::QueryInterface**.</span></span>
9.  <span data-ttu-id="111da-142">使用 [**IWMPropertyVault：： SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) 方法來設定 g \_ wszOriginalWaveFormat 屬性。</span><span class="sxs-lookup"><span data-stu-id="111da-142">Use the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method to set the g\_wszOriginalWaveFormat property.</span></span> <span data-ttu-id="111da-143">使用在步驟6中取得的 **WAVEFORMATEX** 結構做為屬性的值。</span><span class="sxs-lookup"><span data-stu-id="111da-143">Use the **WAVEFORMATEX** structure obtained in step 6 as the value of the property.</span></span>
10. <span data-ttu-id="111da-144">藉由呼叫 [**IWMWriter：： SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) ，並將指標傳遞至 **IWMInputMediaProps** 介面，來包含對輸入媒體屬性所做的變更。</span><span class="sxs-lookup"><span data-stu-id="111da-144">Include changes made to the input media properties by calling [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) and passing it a pointer to the **IWMInputMediaProps** interface.</span></span>
11. <span data-ttu-id="111da-145">開始讀取原始檔案中的範例，並透過呼叫 [**IWMWriter：： WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)將它們傳遞給寫入器。</span><span class="sxs-lookup"><span data-stu-id="111da-145">Begin reading samples from the original file and passing them to the writer with calls to [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span></span>

## <a name="related-topics"></a><span data-ttu-id="111da-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="111da-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="111da-147">**Advanced 主題**</span><span class="sxs-lookup"><span data-stu-id="111da-147">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="111da-148">**IWMInputMediaProps 介面**</span><span class="sxs-lookup"><span data-stu-id="111da-148">**IWMInputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)
</dt> <dt>

[<span data-ttu-id="111da-149">**IWMMediaProps 介面**</span><span class="sxs-lookup"><span data-stu-id="111da-149">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="111da-150">**IWMProfile 介面**</span><span class="sxs-lookup"><span data-stu-id="111da-150">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="111da-151">**IWMPropertyVault 介面**</span><span class="sxs-lookup"><span data-stu-id="111da-151">**IWMPropertyVault Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)
</dt> <dt>

[<span data-ttu-id="111da-152">**IWMStreamConfig 介面**</span><span class="sxs-lookup"><span data-stu-id="111da-152">**IWMStreamConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> </dl>

 

 




