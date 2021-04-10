---
title: 將音訊解碼為 S/PDIF
description: 將音訊解碼為 S/PDIF
ms.assetid: b56c2d0a-a7c6-44f8-832a-bbbe7ae053e6
keywords:
- Windows Media Format SDK，將音訊解碼為 S/PDIF
- 'Windows Media Format SDK、索尼/Philips 數位互連格式 (S/PDIF) '
- Advanced Systems Format (ASF) ，將音訊解碼為 S/PDIF
- ASF (Advanced Systems Format) ，將音訊解碼成 S/PDIF
- 'Advanced Systems Format (ASF) 、索尼/Philips 數位互連格式 (S/PDIF) '
- 'ASF (Advanced Systems Format) 、索尼/Philips 數位互連格式 (S/PDIF) '
- 索尼/Philips 數位互連格式 (S/PDIF) ，解碼音訊
- S/PDIF (索尼/Philips 數位互連格式) ，解碼音訊
- 解碼音訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa063baa8e9a88c2fb7a4d9c67375965282167
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103681558"
---
# <a name="to-decode-audio-to-spdif"></a><span data-ttu-id="c3fdf-112">將音訊解碼為 S/PDIF</span><span class="sxs-lookup"><span data-stu-id="c3fdf-112">To Decode Audio to S/PDIF</span></span>

<span data-ttu-id="c3fdf-113">使用 Windows Media 音訊 9 Professional 編解碼器編碼的音訊可以解碼成索尼/Philips 數位互連格式 (S/PDIF) 。</span><span class="sxs-lookup"><span data-stu-id="c3fdf-113">Audio encoded with the Windows Media Audio 9 Professional codec can be decoded to Sony/Philips Digital Interconnect Format (S/PDIF).</span></span> <span data-ttu-id="c3fdf-114">若要產生 S/PDIF 輸出，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="c3fdf-114">To generate S/PDIF output, perform the following steps:</span></span>

1.  <span data-ttu-id="c3fdf-115">藉由呼叫 [**IWMReader：： open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) 方法，開啟包含 Windows Media 音訊 9 Professional 串流的檔案。</span><span class="sxs-lookup"><span data-stu-id="c3fdf-115">Open a file that contains a Windows Media Audio 9 Professional stream by calling the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method.</span></span>
2.  <span data-ttu-id="c3fdf-116">識別您想要的資料流程輸出編號。</span><span class="sxs-lookup"><span data-stu-id="c3fdf-116">Identify the output number of the stream that you want.</span></span> <span data-ttu-id="c3fdf-117">如需詳細資訊，請參閱 [識別輸出數目](to-identify-output-numbers.md)。</span><span class="sxs-lookup"><span data-stu-id="c3fdf-117">For more information, see [To Identify Output Numbers](to-identify-output-numbers.md).</span></span>
3.  <span data-ttu-id="c3fdf-118">呼叫 [**IWMReaderAdvanced2：： SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) 方法來設定 S/PDIF 輸出。</span><span class="sxs-lookup"><span data-stu-id="c3fdf-118">Call the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method to configure S/PDIF output.</span></span> <span data-ttu-id="c3fdf-119">請使用 g \_ wszEnableWMAProSPDIFOutput 作為設定名稱。</span><span class="sxs-lookup"><span data-stu-id="c3fdf-119">Use g\_wszEnableWMAProSPDIFOutput for the setting name.</span></span> <span data-ttu-id="c3fdf-120">資料類型為 **WMT \_ 類型 \_ BOOL**; 將值設定為 **TRUE** 以啟用 S/PDIF 輸出。</span><span class="sxs-lookup"><span data-stu-id="c3fdf-120">The data type is **WMT\_TYPE\_BOOL**; set the value to **TRUE** to enable S/PDIF output.</span></span>
4.  <span data-ttu-id="c3fdf-121">藉由呼叫 [**IWMReader：： GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat)方法，取得所需輸出格式的輸出屬性介面 ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) 。</span><span class="sxs-lookup"><span data-stu-id="c3fdf-121">Get the output properties interface ([**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) of the desired output format by calling the [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) method.</span></span> <span data-ttu-id="c3fdf-122">如需列舉輸出格式的詳細資訊，請參閱 [指派輸出格式](assigning-output-formats.md)。</span><span class="sxs-lookup"><span data-stu-id="c3fdf-122">For more information about enumerating output formats, see [Assigning Output Formats](assigning-output-formats.md).</span></span>
5.  <span data-ttu-id="c3fdf-123">藉由呼叫 [**IWMReader：： SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) 方法來設定輸出格式。</span><span class="sxs-lookup"><span data-stu-id="c3fdf-123">Set the output format by calling the [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) method.</span></span> <span data-ttu-id="c3fdf-124">將指標傳入在步驟4中取得的 **IWMOutputMediaProps** 介面。</span><span class="sxs-lookup"><span data-stu-id="c3fdf-124">Pass in a pointer to the **IWMOutputMediaProps** interface obtained in step 4.</span></span>
6.  <span data-ttu-id="c3fdf-125">進行任何其他設定變更並開始播放。</span><span class="sxs-lookup"><span data-stu-id="c3fdf-125">Make any other configuration changes and begin playback.</span></span>

> [!Note]  
> <span data-ttu-id="c3fdf-126">您可以使用 [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) 介面的對應方法，在同步讀取器上執行上述步驟。</span><span class="sxs-lookup"><span data-stu-id="c3fdf-126">You can perform the preceding steps on the synchronous reader by using the corresponding methods of the [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) interface.</span></span>

 

<span data-ttu-id="c3fdf-127">下列範例程式碼示範如何設定音訊串流，以將音訊輸出為 S/PDIF 資料。</span><span class="sxs-lookup"><span data-stu-id="c3fdf-127">The following example code demonstrates how to set an audio stream to output audio as S/PDIF data.</span></span> <span data-ttu-id="c3fdf-128">此函式會假設已在讀取器中載入檔案，且已識別出輸出編號。</span><span class="sxs-lookup"><span data-stu-id="c3fdf-128">This function assumes that a file has already been loaded in the reader and that the output number has been identified.</span></span> <span data-ttu-id="c3fdf-129">如需使用此程式碼的詳細資訊，請參閱 [使用程式碼範例](using-the-code-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="c3fdf-129">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT SetSPDIF(DWORD dwOutputNum, IWMReader* pReader)
{
    HRESULT hr = S_OK;

    IWMReaderAdvanced2*  pReaderAdv   = NULL;
    IWMOutputMediaProps* pOutputProps = NULL; 

    BOOL fValue = TRUE;

    // Get the advanced reader interface.
    hr = pReader->QueryInterface(IID_IWMReaderAdvanced2,
                                 (void**)&pReaderAdv);
    GOTO_EXIT_IF_FAILED(hr);

    // Set S/PDIF output.
    hr = pReaderAdv->SetOutputSetting(dwOutputNum, 
                                      g_wszEnableWMAProSPDIFOutput, 
                                      WMT_TYPE_BOOL, 
                                      (BYTE*)&fValue, 
                                      sizeof(BOOL));
    GOTO_EXIT_IF_FAILED(hr);

    // Get the first output format for the stream.
    // NOTE: You could also enumerate the available output formats
    // and pick one to use.

    hr = pReader->GetOutputFormat(dwOutputNum, 0, &pOutputProps);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the output properties back on the reader.
    hr = pReader->SetOutputProps(dwOutputNum, pOutputProps);

Exit:
    SAFE_RELEASE(pReaderAdv);
    SAFE_RELEASE(pOutputProps);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c3fdf-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="c3fdf-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3fdf-131">**Advanced 主題**</span><span class="sxs-lookup"><span data-stu-id="c3fdf-131">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="c3fdf-132">**讀取 ASF 檔案**</span><span class="sxs-lookup"><span data-stu-id="c3fdf-132">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="c3fdf-133">**IWMReader 介面**</span><span class="sxs-lookup"><span data-stu-id="c3fdf-133">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="c3fdf-134">**IWMReaderAdvanced2 介面**</span><span class="sxs-lookup"><span data-stu-id="c3fdf-134">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="c3fdf-135">**IWMSyncReader 介面**</span><span class="sxs-lookup"><span data-stu-id="c3fdf-135">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> </dl>

 

 




