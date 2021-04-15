---
description: 設定設定檔和其他 ASF 檔案屬性
ms.assetid: c43df556-9d8a-4010-9ed6-f84d8ac6d9bc
title: 設定設定檔和其他 ASF 檔案屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e26dcbb49cb5ff8309dccafc3f1d8d66397871
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385759"
---
# <a name="configuring-profiles-and-other-asf-file-properties"></a><span data-ttu-id="9c9da-103">設定設定檔和其他 ASF 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="9c9da-103">Configuring Profiles and Other ASF File Properties</span></span>

<span data-ttu-id="9c9da-104">下列專案說明如何執行與建立 ASF 檔案相關的各種工作。</span><span class="sxs-lookup"><span data-stu-id="9c9da-104">The following items describe how to perform various tasks related to the creation of ASF files.</span></span> <span data-ttu-id="9c9da-105">本主題所提及的部分介面記載于 Windows Media Format SDK 檔中。</span><span class="sxs-lookup"><span data-stu-id="9c9da-105">Some of the interfaces mentioned in this topic are documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="9c9da-106">建立設定檔</span><span class="sxs-lookup"><span data-stu-id="9c9da-106">Creating a Profile</span></span>

<span data-ttu-id="9c9da-107">ASF 設定檔會在 Windows Media Format SDK 中詳細討論;基本上，它們會描述 Windows Media 格式檔案的屬性，例如位元速率、資料流程的數目和類型，以及壓縮品質。</span><span class="sxs-lookup"><span data-stu-id="9c9da-107">ASF profiles are discussed in detail in the Windows Media Format SDK; essentially, they describe attributes of a Windows Media Format file such as bit rate, number and type of streams, and compression quality.</span></span> <span data-ttu-id="9c9da-108">此篩選器會使用設定檔來決定要寫入的 Windows Media 格式檔案種類、必須設定多少輸入 pin，以及它們可以接受的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="9c9da-108">The filter uses the profile to determine what kind of Windows Media Format file to write, how many input pins it must set up, and what media types they can accept.</span></span>

<span data-ttu-id="9c9da-109">若要建立自訂設定檔，請使用 Windows Media Format SDK，直接使用 **WMCreateProfileManager** 函式建立配置檔案管理員物件。</span><span class="sxs-lookup"><span data-stu-id="9c9da-109">To create a custom profile, use the Windows Media Format SDK directly to create a profile manager object by using the **WMCreateProfileManager** function.</span></span> <span data-ttu-id="9c9da-110">接下來，使用 [**IConfigASFWriter：： ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile)方法建立設定檔，並將其傳遞至 [WM ASF 寫入器](wm-asf-writer-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="9c9da-110">Next, create the profile, and pass it to the [WM ASF Writer](wm-asf-writer-filter.md) by using the [**IConfigASFWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) method.</span></span> <span data-ttu-id="9c9da-111">這是使用 Windows Media 音訊和 Video 9 系列編解碼器的設定檔來設定篩選器的唯一方式。</span><span class="sxs-lookup"><span data-stu-id="9c9da-111">This is the only way to configure the filter with a profile that uses the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="9c9da-112">您可以使用 [**IConfigASFWriter：： ConfigureFilterUsingProfileGuid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) 方法，新增這些編解碼器舊版的系統設定檔。</span><span class="sxs-lookup"><span data-stu-id="9c9da-112">System profiles for earlier versions of these codecs can be added by using the [**IConfigASFWriter::ConfigureFilterUsingProfileGuid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) method.</span></span>

<span data-ttu-id="9c9da-113">只要新的設定檔不需要任何額外的輸入釘選，您就可以在篩選的輸入 pin 連線時重設設定檔。</span><span class="sxs-lookup"><span data-stu-id="9c9da-113">You can reset the profile while the filter's input pins are connected, as long as the new profile does not require any additional input pins.</span></span> <span data-ttu-id="9c9da-114">例如，如果您將設定檔從單一輸入的僅限音訊設定檔變更為雙輸入音訊和影片設定檔，則只會重新連線音訊 pin 碼，而且不會為影片串流建立新的 pin。</span><span class="sxs-lookup"><span data-stu-id="9c9da-114">For example, if you change the profile from a one-input audio-only profile to a two-input audio and video profile, just the audio pin will be reconnected and no new pin will be created for the video stream.</span></span>

<span data-ttu-id="9c9da-115">新增中繼資料</span><span class="sxs-lookup"><span data-stu-id="9c9da-115">Adding Metadata</span></span>

<span data-ttu-id="9c9da-116">若要將中繼資料新增至檔案，請查詢 **IWMHeaderInfo** 介面的 [WM ASF 寫入](wm-asf-writer-filter.md)器篩選器。</span><span class="sxs-lookup"><span data-stu-id="9c9da-116">To add metadata to a file, query the [WM ASF Writer](wm-asf-writer-filter.md) filter for the **IWMHeaderInfo** interface.</span></span> <span data-ttu-id="9c9da-117">將設定檔提供給篩選器之後，請使用 **IWMHeaderInfo** 介面方法來寫入中繼資料。</span><span class="sxs-lookup"><span data-stu-id="9c9da-117">After the filter has been given a profile, use the **IWMHeaderInfo** interface methods to write the metadata.</span></span>

<span data-ttu-id="9c9da-118">為檔案編制索引</span><span class="sxs-lookup"><span data-stu-id="9c9da-118">Indexing a File</span></span>

<span data-ttu-id="9c9da-119">在預設情況下，WM ASF 寫入器會建立暫時的索引檔案。</span><span class="sxs-lookup"><span data-stu-id="9c9da-119">The WM ASF Writer creates temporally indexed files by default.</span></span> <span data-ttu-id="9c9da-120">若要建立框架索引檔案，請使用 [**IConfigAsfWriter：： SetIndexMode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) 方法來停用所有的索引，然後建立檔案。</span><span class="sxs-lookup"><span data-stu-id="9c9da-120">To create a frame-indexed file, use the [**IConfigAsfWriter::SetIndexMode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) method to disable all indexing, then create the file.</span></span> <span data-ttu-id="9c9da-121">完成時，請直接使用 Windows Media Format SDK 來建立檔案的框架型索引。</span><span class="sxs-lookup"><span data-stu-id="9c9da-121">When it is complete, use the Windows Media Format SDK directly to create a frame-based index for the file.</span></span>

<span data-ttu-id="9c9da-122">Two-Pass 編碼</span><span class="sxs-lookup"><span data-stu-id="9c9da-122">Two-Pass Encoding</span></span>

<span data-ttu-id="9c9da-123">只有在第8版和更新版本的 Windows 媒體編解碼器上，才支援雙通過編碼。</span><span class="sxs-lookup"><span data-stu-id="9c9da-123">Two-pass encoding is supported only on Windows Media codecs of version 8 and later.</span></span> <span data-ttu-id="9c9da-124">藉由呼叫 [**IConfigAsfWriter2：： SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam)並在 \_ \_ DWPARAM 參數中指定 AM CONFIGASFWRITER PARAM \_ MULTIPASS，並在 *dwParam1* 參數中指定 **TRUE** ，將 WM ASF 寫入器放入前置處理模式。</span><span class="sxs-lookup"><span data-stu-id="9c9da-124">Put the WM ASF Writer into preprocess mode by calling [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) and specifying AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS in the *dwParam* parameter and **TRUE** in the *dwParam1* parameter.</span></span>

<span data-ttu-id="9c9da-125">然後執行篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="9c9da-125">Then run the filter graph.</span></span> <span data-ttu-id="9c9da-126">當所有前置處理階段完成時 (通常只會執行一次前置處理階段) ，應用程式會從篩選器收到 EC 前置處理 [**\_ \_ 完成**](ec-preprocess-complete.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="9c9da-126">When all the preprocessing passes are done (typically only one preprocessing pass will be performed), the application will receive an [**EC\_PREPROCESS\_COMPLETE**](ec-preprocess-complete.md) event from the filter.</span></span> <span data-ttu-id="9c9da-127">收到此事件時，請使用 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 將資料流程指標重設回開頭，然後再次執行篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="9c9da-127">When this event is received, use [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) to reset the stream pointer back to the beginning, and run the filter graph again.</span></span> <span data-ttu-id="9c9da-128">最後一次通過之後 (通常是第二次傳遞) ，應用程式將會收到 [**EC \_ 完成**](ec-complete.md) 事件，以表示編碼程式已完成。</span><span class="sxs-lookup"><span data-stu-id="9c9da-128">After the last pass (typically the second pass), the application will receive an [**EC\_COMPLETE**](ec-complete.md) event to signify that the encoding process is complete.</span></span> <span data-ttu-id="9c9da-129">如果在收到 EC 前置處理 **\_ \_ 完成** 事件之前取消前置處理階段，請先呼叫 [**IConfigAsfWriter2：： ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) 來重設篩選，然後再嘗試執行其他前置處理。</span><span class="sxs-lookup"><span data-stu-id="9c9da-129">If a preprocessing pass is canceled before the **EC\_PREPROCESS\_COMPLETE** event is received, call [**IConfigAsfWriter2::ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) to reset the filter before attempting another preprocessing run.</span></span>

<span data-ttu-id="9c9da-130">只有當您想要將篩選器完全移出前置處理模式時，才需要將 AM \_ CONFIGASFWRITER \_ PARAM \_ MULTIPASS 參數設定為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="9c9da-130">It is only necessary to set the AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS parameter to **FALSE** if you want to put the filter out of preprocessing mode completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9c9da-131">應用程式會負責根據將用於編碼的設定檔來啟用前置處理模式。</span><span class="sxs-lookup"><span data-stu-id="9c9da-131">It is the application's responsibility to enable the preprocessing mode based on the profile that will be used for encoding.</span></span> <span data-ttu-id="9c9da-132">有些設定檔需要兩次傳遞編碼;如果您嘗試使用這類設定檔來編碼檔案，且未將 AM \_ CONFIGASFWRITER \_ PARAM MULTIPASS 設定 \_ 為 **TRUE**，則會產生 [**EC \_ USERABORT**](ec-userabort.md) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="9c9da-132">Some profiles require two-pass encoding; if you attempt to encode a file with such a profile, and do not set AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS to **TRUE**, an [**EC\_USERABORT**](ec-userabort.md) error will result.</span></span> <span data-ttu-id="9c9da-133">如需詳細資訊，請參閱 Windows Media Format SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="9c9da-133">For more information, see the Windows Media Format SDK documentation.</span></span>

 

<span data-ttu-id="9c9da-134">在執行時間取得和設定緩衝區屬性</span><span class="sxs-lookup"><span data-stu-id="9c9da-134">Getting and Setting Buffer Properties at Run Time</span></span>

<span data-ttu-id="9c9da-135">在某些情況下（例如，如果您想要在寫入檔案時強制插入金鑰框架），應用程式可能需要在執行時間取得或設定 Windows Media 緩衝區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9c9da-135">In some scenarios, for example if you want to force key-frame insertion when writing a file, an application may need to get or set information about a Windows Media buffer at run time.</span></span> <span data-ttu-id="9c9da-136">[WM Asf 讀取](wm-asf-reader-filter.md)器和 [WM asf 寫入](wm-asf-writer-filter.md)器篩選器都支援回呼機制，可讓應用程式在讀取或寫入檔案期間，存取每個個別媒體緩衝區上的 **INSSBuffer3** 介面。</span><span class="sxs-lookup"><span data-stu-id="9c9da-136">The [WM ASF Reader](wm-asf-reader-filter.md) and [WM ASF Writer](wm-asf-writer-filter.md) filters both support a callback mechanism that enables an application to access the **INSSBuffer3** interface on each individual media buffer during file reading or file writing.</span></span> <span data-ttu-id="9c9da-137">應用程式可以使用此介面將特定範例指定為主要畫面格、設定 SMPTE 時間代碼、指定交錯設定，或將任何類型的私用資料新增至資料流程。</span><span class="sxs-lookup"><span data-stu-id="9c9da-137">Applications can use this interface to designate specific samples as key frames, set SMPTE time codes, specify interlace settings, or add any type of private data to a stream.</span></span>

<span data-ttu-id="9c9da-138">使用 [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) 介面，從處理影片串流的 pin 註冊回呼。</span><span class="sxs-lookup"><span data-stu-id="9c9da-138">Use the [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) interface to register for callbacks from the pin that is handling the video stream.</span></span> <span data-ttu-id="9c9da-139">Pin 會為每個緩衝區呼叫您的 [**IAMWMBufferPassCallback：： Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) 方法。</span><span class="sxs-lookup"><span data-stu-id="9c9da-139">The pin will call your [**IAMWMBufferPassCallback::Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) method for each buffer.</span></span>

<span data-ttu-id="9c9da-140">非正方形圖元</span><span class="sxs-lookup"><span data-stu-id="9c9da-140">Non-Square Pixels</span></span>

<span data-ttu-id="9c9da-141">WM ASF 寫入器會連接到輸出圖元外觀比例資訊的上游篩選器，例如 DV 解碼器。</span><span class="sxs-lookup"><span data-stu-id="9c9da-141">The WM ASF Writer connects to an upstream filter, such as the DV Decoder, that outputs pixel aspect ratio information.</span></span> <span data-ttu-id="9c9da-142">WM ASF 寫入器會將這項資訊寫入檔案中每個範例的資料單位延伸模組。</span><span class="sxs-lookup"><span data-stu-id="9c9da-142">The WM ASF Writer will write this information as data unit extensions for every sample in the file.</span></span>

<span data-ttu-id="9c9da-143">當 WM ASF 讀取器在檔案標頭中或在範例的資料單位延伸中遇到圖元外觀比例資訊時，它會提供 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式作為其輸出圖釘的第一個選擇。</span><span class="sxs-lookup"><span data-stu-id="9c9da-143">When the WM ASF Reader encounters pixel aspect ratio information in the file header or in data unit extensions for the samples, it will offer a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format as a first choice on its output pin.</span></span> <span data-ttu-id="9c9da-144">結構的 **dwPictAspectRatioX** 和 **dwPictAspectRatioY** 成員（描述影片矩形的外觀比例）將會正確調整以考慮圖元外觀比例。</span><span class="sxs-lookup"><span data-stu-id="9c9da-144">The **dwPictAspectRatioX** and **dwPictAspectRatioY** members of the structure, which describe the video rectangle's aspect ratio, will be correctly adjusted to account for the pixel aspect ratio.</span></span>

<span data-ttu-id="9c9da-145">維護交錯格式</span><span class="sxs-lookup"><span data-stu-id="9c9da-145">Maintaining Interlaced Format</span></span>

<span data-ttu-id="9c9da-146">如果您從電視或 DV 攝影機捕捉交錯的影片，如果您預期在電視或其他交錯顯示裝置上播放編碼的檔案，您可能會想要將原始影片保留為獨立欄位。</span><span class="sxs-lookup"><span data-stu-id="9c9da-146">If you capture interlaced video from a television or a DV camera, you might wish to preserve the original video as independent fields if you expect the encoded file to be played back on a television or other interlaced display device.</span></span> <span data-ttu-id="9c9da-147"> (電腦監視器是漸進式掃描裝置。 ) 如果您將影片進行逐行掃描，然後 reinterlace 以在電視上播放，將會產生部分資料遺失。</span><span class="sxs-lookup"><span data-stu-id="9c9da-147">(Computer monitors are progressive scanning devices.) If you deinterlace a video, and then reinterlace it for playback on a television, some loss of data will be incurred.</span></span> <span data-ttu-id="9c9da-148">在 ASF 檔案中，會使用先前所述的 [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) 方法，將交錯資訊儲存為數據單位延伸，讓應用程式套用至每個範例。</span><span class="sxs-lookup"><span data-stu-id="9c9da-148">In an ASF file, interlacing information is stored as data unit extensions that the application applies to each sample using the [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) method described previously.</span></span> <span data-ttu-id="9c9da-149">若要編碼保留原始隔行設定的檔案，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="9c9da-149">To encode a file that preserves the original interlace settings, follow these steps:</span></span>

1.  <span data-ttu-id="9c9da-150">執行支援 **IAMWMBufferPassCallback** 的類別，並撰寫可設定每個範例之交錯旗標的通知函數。</span><span class="sxs-lookup"><span data-stu-id="9c9da-150">Implement a class that supports **IAMWMBufferPassCallback** and write a Notify function that sets the interlace flags for each sample.</span></span> <span data-ttu-id="9c9da-151">在處理每個範例之前，會先由 WM ASF 寫入器呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="9c9da-151">This function will be called by the WM ASF Writer before it processes each sample.</span></span>
    ```C++
    // Set to WM_CT_TOP_FIELD_FIRST if that is your format.
    BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
    HRESULT hr = S_OK;

    hr = pNSSBuffer3->SetProperty(
        WM_SampleExtensionGUID_ContentType, 
        (void*) &flag, 
        WM_SampleExtension_ContentType_Size
        );         
    ```

    

2.  <span data-ttu-id="9c9da-152">在您將設定檔傳遞至篩選之前，請先設定設定檔上的資料單位延伸。</span><span class="sxs-lookup"><span data-stu-id="9c9da-152">Set the data unit extensions on the profile before you pass the profile to the filter.</span></span>
    ```C++
    hr = pWMStreamConfig2->AddDataUnitExtension(
        WM_SampleExtensionGUID_ContentType, 
        WM_SampleExtension_ContentType_Size, 
        NULL, 
        0 
        );
    ```

    

3.  <span data-ttu-id="9c9da-153">使用設定檔設定篩選準則之後，請從 WM ASF 寫入器取得 **IWMWriterAdvanced2** 介面，然後呼叫 **SetInputSettings** 方法。</span><span class="sxs-lookup"><span data-stu-id="9c9da-153">After you configure the filter with the profile, obtain the **IWMWriterAdvanced2** interface from the WM ASF Writer and call the **SetInputSettings** method.</span></span>

    ``

    ``

    ```C++
    // Must do this first.
    hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);
      
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

    

## <a name="related-topics"></a><span data-ttu-id="9c9da-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="9c9da-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c9da-155">在 DirectShow 中建立 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="9c9da-155">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



