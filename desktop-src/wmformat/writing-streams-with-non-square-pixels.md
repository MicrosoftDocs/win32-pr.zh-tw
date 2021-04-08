---
title: 以非正方形圖元撰寫資料流程
description: 以非正方形圖元撰寫資料流程
ms.assetid: 4af7dedc-e2b8-4dc2-add4-84424e93c297
keywords:
- Windows Media Format SDK，撰寫影片串流
- Windows Media Format SDK、影片串流
- Windows Media Format SDK、非正方形圖元
- 'Windows Media 格式 SDK，圖元 (非正方形) '
- Advanced Systems Format (ASF) 、撰寫影片串流
- ASF (Advanced 系統格式) 、撰寫影片串流
- Advanced Systems Format (ASF) 、影片串流
- ASF (Advanced 系統格式) 、影片串流
- Advanced Systems Format (ASF) 、非平方圖元
- ASF (Advanced Systems Format) 、非正方形圖元
- 'Advanced Systems Format (ASF) 、圖元 (非正方形) '
- 'ASF (Advanced Systems Format) ，圖元 (非正方形) '
- 撰寫影片串流
- 影片串流，書寫
- 影片串流，非正方形圖元
- 非正方形圖元
- '圖元 (非正方形) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1349840f151ab787ba0e0512cfab8fea08aacf1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023035"
---
# <a name="writing-streams-with-non-square-pixels"></a><span data-ttu-id="25c24-120">以非正方形圖元撰寫資料流程</span><span class="sxs-lookup"><span data-stu-id="25c24-120">Writing Streams with Non-Square Pixels</span></span>

<span data-ttu-id="25c24-121">有兩種方式可以建立具有非正方形圖元的影片串流，以在 Windows Media Player 中正確顯示。</span><span class="sxs-lookup"><span data-stu-id="25c24-121">There are two ways to create video streams with non-square pixels that will be displayed correctly in Windows Media Player.</span></span> <span data-ttu-id="25c24-122">第一個技巧牽涉到在檔案標頭中設定資料流程層級的屬性。</span><span class="sxs-lookup"><span data-stu-id="25c24-122">The first technique involves setting stream-level attributes in the file header.</span></span> <span data-ttu-id="25c24-123">第二個技術牽涉到將資料單位延伸加入至設定檔中的資料流程，然後在每個寫入的範例中設定其值。</span><span class="sxs-lookup"><span data-stu-id="25c24-123">The second technique involves adding a data unit extension to a stream in the profile, and then setting a value for it in every sample that is written.</span></span>

## <a name="to-use-stream-level-header-attributes-to-set-pixel-aspect-ratio"></a><span data-ttu-id="25c24-124">若要使用資料流程層級的標頭屬性來設定圖元外觀比例</span><span class="sxs-lookup"><span data-stu-id="25c24-124">To Use Stream-level Header Attributes to Set Pixel Aspect Ratio</span></span>

1.  <span data-ttu-id="25c24-125">設定寫入器物件。</span><span class="sxs-lookup"><span data-stu-id="25c24-125">Set up the writer object.</span></span> <span data-ttu-id="25c24-126">如需詳細資訊，請參閱 [寫入 ASF](writing-asf-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="25c24-126">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="25c24-127">使用一或多個影片串流建立或載入設定檔。</span><span class="sxs-lookup"><span data-stu-id="25c24-127">Create or load a profile with one or more video streams.</span></span> <span data-ttu-id="25c24-128">如需詳細資訊，請參閱搭配 [使用設定檔與寫入器](to-use-profiles-with-the-writer.md)。</span><span class="sxs-lookup"><span data-stu-id="25c24-128">For more information, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
3.  <span data-ttu-id="25c24-129">呼叫 [**IWMWriter：： SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile)。</span><span class="sxs-lookup"><span data-stu-id="25c24-129">Call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span></span> <span data-ttu-id="25c24-130"> (一律在設定任何標頭屬性之前呼叫這個方法。 ) </span><span class="sxs-lookup"><span data-stu-id="25c24-130">(Always call this method before setting any header attributes.)</span></span>
4.  <span data-ttu-id="25c24-131">呼叫 **QueryInterface** 來取得 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) 介面並呼叫 [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) 兩次，以將 [**AspectRatioX**](aspectratiox.md) 和 [**AspectRatioY**](aspectratioy.md) 新增為影片資料流程的資料流程層級屬性。</span><span class="sxs-lookup"><span data-stu-id="25c24-131">Call **QueryInterface** to obtain the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface and call [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) twice to add [**AspectRatioX**](aspectratiox.md) and [**AspectRatioY**](aspectratioy.md) as stream-level attributes of the video stream.</span></span> <span data-ttu-id="25c24-132">這些屬性是 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="25c24-132">These attributes are **DWORD** values.</span></span>
5.  <span data-ttu-id="25c24-133">寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="25c24-133">Write the file.</span></span>

## <a name="to-use-data-unit-extensions-to-set-pixel-aspect-ratio"></a><span data-ttu-id="25c24-134">使用資料單位延伸設定圖元外觀比例</span><span class="sxs-lookup"><span data-stu-id="25c24-134">To Use Data Unit Extensions to Set Pixel Aspect Ratio</span></span>

<span data-ttu-id="25c24-135">**撰寫之前：**</span><span class="sxs-lookup"><span data-stu-id="25c24-135">**Before writing:**</span></span>

1.  <span data-ttu-id="25c24-136">設定寫入器物件。</span><span class="sxs-lookup"><span data-stu-id="25c24-136">Set up the writer object.</span></span> <span data-ttu-id="25c24-137">如需詳細資訊，請參閱 [寫入 ASF](writing-asf-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="25c24-137">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="25c24-138">使用一或多個影片串流建立或載入設定檔。</span><span class="sxs-lookup"><span data-stu-id="25c24-138">Create or load a profile with one or more video streams.</span></span> <span data-ttu-id="25c24-139">如需詳細資訊，請參閱搭配 [使用設定檔與寫入器](to-use-profiles-with-the-writer.md)。</span><span class="sxs-lookup"><span data-stu-id="25c24-139">For more information, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
3.  <span data-ttu-id="25c24-140">針對) 在設定檔中任何媒體類型的每個資料流程 (，呼叫 [**IWMStreamConfig：： SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) 來指定您選擇的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="25c24-140">For each stream (of any media type) in the profile, call [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) to specify a unique name of your choice.</span></span> <span data-ttu-id="25c24-141">請勿提供兩個相同名稱的資料流程。</span><span class="sxs-lookup"><span data-stu-id="25c24-141">Do not give two streams the same name.</span></span>
4.  <span data-ttu-id="25c24-142">使用影片串流上的 [**IWMStreamConfig2：： AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) 來新增圖元外觀比例的資料單位延伸。</span><span class="sxs-lookup"><span data-stu-id="25c24-142">Use [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) on the video stream to add a data unit extension for pixel aspect ratio.</span></span>
5.  <span data-ttu-id="25c24-143">呼叫 [**IWMWriter：： SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile)。</span><span class="sxs-lookup"><span data-stu-id="25c24-143">Call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span></span>
6.  <span data-ttu-id="25c24-144">寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="25c24-144">Write the file.</span></span>

<span data-ttu-id="25c24-145">**撰寫時：**</span><span class="sxs-lookup"><span data-stu-id="25c24-145">**While writing:**</span></span>

-   <span data-ttu-id="25c24-146">針對每個範例，呼叫 [**INSSBuffer3：： SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) 並指定 WM \_ SampleExtensionGUID \_ PixelAspectRatio 屬性以及正確的值。</span><span class="sxs-lookup"><span data-stu-id="25c24-146">For each sample, call [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) and specify the WM\_SampleExtensionGUID\_PixelAspectRatio property along with the correct value.</span></span> <span data-ttu-id="25c24-147">外觀比例值會以兩個串連的兩位數值寫入。</span><span class="sxs-lookup"><span data-stu-id="25c24-147">Aspect ratio values are written as two concatenated two-digit values.</span></span> <span data-ttu-id="25c24-148">例如，16:9 是以1609或0x0649 撰寫。</span><span class="sxs-lookup"><span data-stu-id="25c24-148">For example, 16:9 is written as 1609 or 0x0649.</span></span> <span data-ttu-id="25c24-149">這一律是2個位元組的值。</span><span class="sxs-lookup"><span data-stu-id="25c24-149">This is always a 2-byte value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25c24-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="25c24-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25c24-151">**使用非正方形圖元讀取和寫入影片串流**</span><span class="sxs-lookup"><span data-stu-id="25c24-151">**To Read and Write Video Streams with Non-Square Pixels**</span></span>](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




