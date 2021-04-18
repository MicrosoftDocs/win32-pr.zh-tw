---
title: " (QASF) 設定設定檔和其他檔案屬性"
description: " (QASF) 設定設定檔和其他檔案屬性"
ms.assetid: a462fc8b-5a2e-4c93-828d-177d1965b734
keywords:
- 'Windows Media 格式 SDK，設定設定檔 (QASF) '
- 'Windows Media 格式 SDK，設定檔案屬性 (QASF) '
- 'Windows Media 格式 SDK，中繼資料 (QASF) '
- 'Advanced Systems Format (ASF) 、設定設定檔 (QASF) '
- 'ASF (Advanced Systems Format) 、設定設定檔 (QASF) '
- 'Advanced Systems Format (ASF) ，設定檔案屬性 (QASF) '
- 'ASF (Advanced Systems Format) ，設定檔案屬性 (QASF) '
- 'Advanced Systems Format (ASF) 、metadata (QASF) '
- 'ASF (Advanced Systems Format) ，metadata (QASF) '
- Windows Media Format SDK、QASF
- Advanced Systems Format (ASF) ，QASF
- ASF (Advanced Systems Format) ，QASF
- 中繼資料、QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb6afedfa00813e7447e5bcaefe1f251c02575
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463456"
---
# <a name="configuring-profiles-and-other-file-properties-qasf"></a><span data-ttu-id="c9889-116"> (QASF) 設定設定檔和其他檔案屬性</span><span class="sxs-lookup"><span data-stu-id="c9889-116">Configuring Profiles and Other File Properties (QASF)</span></span>

<span data-ttu-id="c9889-117">下列專案說明如何執行與建立 ASF 檔案相關的各種工作。</span><span class="sxs-lookup"><span data-stu-id="c9889-117">The following items describe how to perform various tasks related to the creation of ASF files.</span></span>

## <a name="creating-a-profile-qasf"></a><span data-ttu-id="c9889-118"> (QASF) 建立設定檔</span><span class="sxs-lookup"><span data-stu-id="c9889-118">Creating a Profile (QASF)</span></span>

<span data-ttu-id="c9889-119">若要建立自訂設定檔，請使用 Windows Media Format SDK，直接使用 [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) 函式建立配置檔案管理員物件。</span><span class="sxs-lookup"><span data-stu-id="c9889-119">To create a custom profile, use the Windows Media Format SDK directly to create a profile manager object by using the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span> <span data-ttu-id="c9889-120">接下來，使用 [**IConfigASFWriter：： ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md)方法建立設定檔，並將其傳遞至 [WM ASF 寫入器](wm-asf-writer-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="c9889-120">Next, create the profile, and pass it to the [WM ASF Writer](wm-asf-writer-filter.md) by using the [**IConfigASFWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) method.</span></span> <span data-ttu-id="c9889-121">這是使用 Windows Media 音訊和 Video 9 系列編解碼器的設定檔來設定篩選器的唯一方式。</span><span class="sxs-lookup"><span data-stu-id="c9889-121">This is the only way to configure the filter with a profile that uses the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="c9889-122">您可以使用 [**IConfigASFWriter：： ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md) 方法，新增這些編解碼器舊版的系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="c9889-122">System profiles for earlier versions of these codecs can be added by using the [**IConfigASFWriter::ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md) method.</span></span>

## <a name="adding-metadata-qasf"></a><span data-ttu-id="c9889-123">新增中繼資料 (QASF) </span><span class="sxs-lookup"><span data-stu-id="c9889-123">Adding Metadata (QASF)</span></span>

<span data-ttu-id="c9889-124">若要將中繼資料新增至檔案，請從 [WM ASF 寫入器](wm-asf-writer-filter.md)上的 **IBaseFilter** 介面呼叫 **QueryInterface** ，以取出 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)介面。</span><span class="sxs-lookup"><span data-stu-id="c9889-124">To add metadata to a file, call **QueryInterface** from the **IBaseFilter** interface on the [WM ASF Writer](wm-asf-writer-filter.md) to retrieve the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface.</span></span> <span data-ttu-id="c9889-125">將設定檔提供給篩選器之後，請使用 **IWMHeaderInfo** 介面方法來寫入中繼資料。</span><span class="sxs-lookup"><span data-stu-id="c9889-125">After the filter has been given a profile, use the **IWMHeaderInfo** interface methods to write the metadata.</span></span>

## <a name="indexing-a-file-qasf"></a><span data-ttu-id="c9889-126"> (QASF) 為檔案編制索引</span><span class="sxs-lookup"><span data-stu-id="c9889-126">Indexing a File (QASF)</span></span>

<span data-ttu-id="c9889-127">在預設情況下，WM ASF 寫入器會建立暫時的索引檔案。</span><span class="sxs-lookup"><span data-stu-id="c9889-127">The WM ASF Writer creates temporally indexed files by default.</span></span> <span data-ttu-id="c9889-128">若要建立框架索引檔案，請使用 [**IConfigAsfWriter：： SetIndexMode**](iconfigasfwriter-setindexmode.md) 方法來停用所有的索引，然後建立檔案。</span><span class="sxs-lookup"><span data-stu-id="c9889-128">To create a frame-indexed file, use the [**IConfigAsfWriter::SetIndexMode**](iconfigasfwriter-setindexmode.md) method to disable all indexing, then create the file.</span></span> <span data-ttu-id="c9889-129">完成時，請直接使用 Windows Media Format SDK 來建立檔案的框架型索引。</span><span class="sxs-lookup"><span data-stu-id="c9889-129">When it is complete, use the Windows Media Format SDK directly to create a frame-based index for the file.</span></span>

## <a name="performing-two-pass-encoding-qasf"></a><span data-ttu-id="c9889-130">執行 Two-Pass 編碼 (QASF) </span><span class="sxs-lookup"><span data-stu-id="c9889-130">Performing Two-Pass Encoding (QASF)</span></span>

<span data-ttu-id="c9889-131">只有在第8版和更新版本的 Windows 媒體編解碼器上，才支援雙通過編碼。</span><span class="sxs-lookup"><span data-stu-id="c9889-131">Two-pass encoding is supported only on Windows Media codecs of version 8 and later.</span></span> <span data-ttu-id="c9889-132">藉由呼叫 [**IConfigAsfWriter2：： SetParam**](iconfigasfwriter2-setparam.md)並在 \_ \_ DWPARAM 參數中指定 AM CONFIGASFWRITER PARAM \_ MULTIPASS，並在 *dwParam1* 參數中指定 **TRUE** ，將 WM ASF 寫入器放入前置處理模式。</span><span class="sxs-lookup"><span data-stu-id="c9889-132">Put the WM ASF Writer into preprocess mode by calling [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) and specifying AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS in the *dwParam* parameter and **TRUE** in the *dwParam1* parameter.</span></span>

<span data-ttu-id="c9889-133">然後執行篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="c9889-133">Then run the filter graph.</span></span> <span data-ttu-id="c9889-134">當所有前置處理階段完成時 (通常只會執行一次前置處理階段) ，應用程式會從篩選器收到 EC 前置處理 **\_ \_ 完成** 事件。</span><span class="sxs-lookup"><span data-stu-id="c9889-134">When all the preprocessing passes are done (typically only one preprocessing pass will be performed), the application will receive an **EC\_PREPROCESS\_COMPLETE** event from the filter.</span></span> <span data-ttu-id="c9889-135">收到此事件時，請使用 **IMediaSeeking：： SetPositions** 將資料流程指標重設回開頭，然後再次執行篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="c9889-135">When this event is received, use **IMediaSeeking::SetPositions** to reset the stream pointer back to the beginning, and run the filter graph again.</span></span> <span data-ttu-id="c9889-136">最後一次通過之後 (通常是第二次傳遞) ，應用程式將會收到 **EC \_ 完成** 事件，以表示編碼程式已完成。</span><span class="sxs-lookup"><span data-stu-id="c9889-136">After the last pass (typically the second pass), the application will receive an **EC\_COMPLETE** event to signify that the encoding process is complete.</span></span> <span data-ttu-id="c9889-137">如果在收到 EC 前置處理 **\_ \_ 完成** 事件之前取消前置處理階段，請先呼叫 [**IConfigAsfWriter2：： ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) 來重設篩選，然後再嘗試執行其他前置處理。</span><span class="sxs-lookup"><span data-stu-id="c9889-137">If a preprocessing pass is canceled before the **EC\_PREPROCESS\_COMPLETE** event is received, call [**IConfigAsfWriter2::ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) to reset the filter before attempting another preprocessing run.</span></span>

<span data-ttu-id="c9889-138">只有呼叫 **IConfigAsfWriter：： SetParam** (AM \_ CONFIGASFWRITER \_ PARAM \_ MULTIPASS，) **FALSE** 才能將篩選器完全移出前置處理模式。</span><span class="sxs-lookup"><span data-stu-id="c9889-138">It is only necessary to call **IConfigAsfWriter::SetParam**(AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS, **FALSE**) if you want to put the filter out of preprocessing mode completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c9889-139">應用程式會負責根據將用於編碼的設定檔來啟用前置處理模式。</span><span class="sxs-lookup"><span data-stu-id="c9889-139">It is the application's responsibility to enable preprocessing mode based on the profile that will be used for encoding.</span></span> <span data-ttu-id="c9889-140">有些設定檔需要兩次傳遞編碼;如果您嘗試使用這類設定檔來編碼檔案，且未將 AM \_ CONFIGASFWRITER \_ PARAM MULTIPASS 設定 \_ 為 **TRUE**，則 \_ 會產生 EC USERABORT 錯誤。</span><span class="sxs-lookup"><span data-stu-id="c9889-140">Some profiles require two-pass encoding; if you attempt to encode a file with such a profile, and do not set AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS to **TRUE**, an EC\_USERABORT error will result.</span></span> <span data-ttu-id="c9889-141">如需如何判斷指定的設定檔是否需要雙向編碼的詳細資訊，請參閱 [使用 Two-Pass 編碼](using-two-pass-encoding.md) 或 [撰寫變數位速率資料流程](writing-variable-bit-rate-streams.md)。</span><span class="sxs-lookup"><span data-stu-id="c9889-141">For more information on how to determine whether a given profile requires two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md) or [Writing Variable Bit Rate Streams](writing-variable-bit-rate-streams.md).</span></span>

 

## <a name="getting-and-setting-buffer-properties-at-run-time-qasf"></a><span data-ttu-id="c9889-142">在執行時間取得和設定緩衝區屬性 (QASF) </span><span class="sxs-lookup"><span data-stu-id="c9889-142">Getting and Setting Buffer Properties at Run Time (QASF)</span></span>

<span data-ttu-id="c9889-143">在某些情況下（例如，如果您想要在寫入檔案時強制插入金鑰框架），應用程式可能需要在執行時間取得或設定 Windows Media 緩衝區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c9889-143">In some scenarios, for example if you want to force key-frame insertion when writing a file, an application may need to get or set information about a Windows Media buffer at run time.</span></span> <span data-ttu-id="c9889-144">[WM Asf 讀取](wm-asf-reader-filter.md)器和 [WM asf 寫入](wm-asf-writer-filter.md)器篩選器都支援回呼機制，可讓應用程式在讀取或寫入檔案期間，存取每個個別媒體緩衝區上的 [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3)介面。</span><span class="sxs-lookup"><span data-stu-id="c9889-144">The [WM ASF Reader](wm-asf-reader-filter.md) and [WM ASF Writer](wm-asf-writer-filter.md) filters both support a callback mechanism that enables an application to access the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface on each individual media buffer during file reading or file writing.</span></span> <span data-ttu-id="c9889-145">應用程式可以使用此介面將特定範例指定為主要畫面格（或 [*cleanpoints*](wmformat-glossary.md)），以設定 SMPTE 時間代碼、指定交錯設定，或將任何類型的私用資料新增至資料流程。</span><span class="sxs-lookup"><span data-stu-id="c9889-145">Applications can use this interface to designate specific samples as key frames, or [*cleanpoints*](wmformat-glossary.md), to set SMPTE time codes, to specify interlace settings, or add any type of private data to a stream.</span></span>

<span data-ttu-id="c9889-146">使用 [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) 介面，從處理影片串流的 pin 註冊回呼。</span><span class="sxs-lookup"><span data-stu-id="c9889-146">Use the [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) interface to register for callbacks from the pin that is handling the video stream.</span></span> <span data-ttu-id="c9889-147">當 pin 呼叫您的 [**IAMWMBufferPassCallback：： Notify**](iamwmbufferpasscallback-notify.md) 方法時，請檢查緩衝區上的時間戳記，並在適當的情況下呼叫 [**INSSBuffer3：： SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) 將緩衝區上的 **WM \_ SampleExtensionGUID \_ OutputCleanPoint** 屬性設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="c9889-147">When the pin calls your [**IAMWMBufferPassCallback::Notify**](iamwmbufferpasscallback-notify.md) method, examine the time stamps on the buffer and, if appropriate, call [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) to set the **WM\_SampleExtensionGUID\_OutputCleanPoint** property on the buffer to **TRUE**.</span></span>

## <a name="non-square-pixel-support-qasf"></a><span data-ttu-id="c9889-148"> (QASF) 的非方形圖元支援</span><span class="sxs-lookup"><span data-stu-id="c9889-148">Non-Square Pixel Support (QASF)</span></span>

<span data-ttu-id="c9889-149">WM ASF 寫入器會連接到輸出圖元外觀比例資訊的上游篩選器，例如 DV 解碼器。</span><span class="sxs-lookup"><span data-stu-id="c9889-149">The WM ASF Writer connects to an upstream filter, such as the DV Decoder, that outputs pixel aspect ratio information.</span></span> <span data-ttu-id="c9889-150">WM ASF 寫入器會將這項資訊寫入檔案中每個範例的資料單位延伸模組。</span><span class="sxs-lookup"><span data-stu-id="c9889-150">The WM ASF Writer will write this information as data unit extensions for every sample in the file.</span></span>

<span data-ttu-id="c9889-151">當 WM ASF 讀取器遇到檔案標頭中的圖元外觀比例資訊，或在範例的資料單位延伸中，它會提供 **VIDEOINFOHEADER2** 媒體類型作為其輸出圖釘的第一個選擇。</span><span class="sxs-lookup"><span data-stu-id="c9889-151">When the WM ASF Reader encounters pixel aspect ratio information in the file header or in data unit extensions for the samples, it will offer a **VIDEOINFOHEADER2** media type as a first choice on its output pin.</span></span> <span data-ttu-id="c9889-152">結構的 **dwPictAspectRatioX** 和 **dwPictAspectRatioY** 成員（描述影片矩形的外觀比例）將會正確調整以考慮圖元外觀比例。</span><span class="sxs-lookup"><span data-stu-id="c9889-152">The **dwPictAspectRatioX** and **dwPictAspectRatioY** members of the structure, which describe the video rectangle's aspect ratio, will be correctly adjusted to account for the pixel aspect ratio.</span></span>

## <a name="maintaining-interlaced-format"></a><span data-ttu-id="c9889-153">維護交錯格式</span><span class="sxs-lookup"><span data-stu-id="c9889-153">Maintaining Interlaced Format</span></span>

<span data-ttu-id="c9889-154">如果您從電視或 DV 攝影機捕捉交錯的影片，如果您預期在電視或其他交錯顯示裝置上播放編碼的檔案，您可能會想要將原始影片保留為獨立欄位。</span><span class="sxs-lookup"><span data-stu-id="c9889-154">If you capture interlaced video from a television or a DV camera, you might wish to preserve the original video as independent fields if you expect the encoded file to be played back on a television or other interlaced display device.</span></span> <span data-ttu-id="c9889-155"> (電腦監視器是漸進式掃描裝置。 ) 如果您將影片進行逐行掃描，然後 reinterlace 以在電視上播放，將會產生部分資料遺失。</span><span class="sxs-lookup"><span data-stu-id="c9889-155">(Computer monitors are progressive scanning devices.) If you deinterlace a video, and then reinterlace it for playback on a television, some loss of data will be incurred.</span></span> <span data-ttu-id="c9889-156">在 ASF 檔案中，會使用先前所述的 **IAMWMBufferPassCallback** 方法，將交錯資訊儲存為數據單位延伸，讓應用程式套用至每個範例。</span><span class="sxs-lookup"><span data-stu-id="c9889-156">In an ASF file, interlacing information is stored as data unit extensions that the application applies to each sample using the **IAMWMBufferPassCallback** method described previously.</span></span> <span data-ttu-id="c9889-157">若要編碼保留原始隔行設定的檔案，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="c9889-157">To encode a file that preserves the original interlace settings, follow these steps:</span></span>

-   <span data-ttu-id="c9889-158">執行支援 **IAMWMBufferPassCallback** 的類別，並撰寫可設定每個範例之交錯旗標的通知函數。</span><span class="sxs-lookup"><span data-stu-id="c9889-158">Implement a class that supports **IAMWMBufferPassCallback** and write a Notify function that sets the interlace flags for each sample.</span></span> <span data-ttu-id="c9889-159">在處理每個範例之前，會先由 WM ASF 寫入器呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="c9889-159">This function will be called by the WM ASF Writer before it processes each sample.</span></span>


```C++
// Set to WM_CT_TOP_FIELD_FIRST if that is your format.
BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
            HRESULT hr = pNSSBuffer3->SetProperty(WM_SampleExtensionGUID_ContentType, (void*) &flag, WM_SampleExtension_ContentType_Size);
           
```



-   <span data-ttu-id="c9889-160">在您將設定檔傳遞至篩選之前，請先設定設定檔上的資料單位延伸。</span><span class="sxs-lookup"><span data-stu-id="c9889-160">Set the data unit extensions on the profile before you pass the profile to the filter.</span></span>


```C++
hr = pWMStreamConfig2->AddDataUnitExtension( WM_SampleExtensionGUID_ContentType, WM_SampleExtension_ContentType_Size, NULL, 0 );
```



-   <span data-ttu-id="c9889-161">使用設定檔設定篩選準則之後，請從 WM ASF 寫入器取得 **IWMWriterAdvanced2** 介面，然後呼叫 **SetInputSettings** 方法。</span><span class="sxs-lookup"><span data-stu-id="c9889-161">After you configure the filter with the profile, obtain the **IWMWriterAdvanced2** interface from the WM ASF Writer and call the **SetInputSettings** method.</span></span>

`// Must do this first.`

`hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);`


```C++
  
CComPtr<IServiceProvider> pProvider;
  CComPtr<IWMWriterAdvanced2> pWMWA2;
  hr = pConfigAsfWriter2->QueryInterface( __uuidof(IServiceProvider),
                                         (void**)&pProvider);
  if (SUCCEEDED(hr))
  {
      hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
                    IID_IWMWriterAdvanced2,
                    (void**)&pWMWA2);
  }
  BOOL pValue = TRUE;
 // Set the first parameter to your actual input number.
 hr = pWMWA2->SetInputSetting(0, g_wszInterlacedCoding,
              WMT_TYPE_BOOL, (BYTE*) &pValue, sizeof(WMT_TYPE_BOOL));
            
```



 

 