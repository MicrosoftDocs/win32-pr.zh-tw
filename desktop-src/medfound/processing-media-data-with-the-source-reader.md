---
description: 本主題說明如何使用來源讀取器來處理媒體資料。
ms.assetid: 583f5736-f767-47c5-8fdc-b3645aed59f6
title: 使用來源讀取器來處理媒體資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b19bce4d83298693825037aef92a220d78ed7c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321448"
---
# <a name="using-the-source-reader-to-process-media-data"></a>使用來源讀取器來處理媒體資料

本主題說明如何使用 [來源讀取器](source-reader.md) 來處理媒體資料。

若要使用來源讀取器，請遵循下列基本步驟：

1.  建立來源讀取器的實例。
2.  列舉可能的輸出格式。
3.  設定每個資料流程的實際輸出格式。
4.  處理來自來源的資料。

本主題的其餘部分將詳細說明這些步驟。

-   [建立來源讀取器](#creating-the-source-reader)
-   [列舉輸出格式](#enumerating-output-formats)
-   [設定輸出格式](#setting-output-formats)
-   [處理媒體資料](#using-the-source-reader-to-process-media-data)
-   [清空資料管線](#draining-the-data-pipeline)
-   [取得檔案持續時間](#getting-the-file-duration)
-   [尋求](#seeking)
-   [播放速率](#playback-rate)
-   [硬體加速](#hardware-acceleration)
-   [相關主題](#related-topics)

## <a name="creating-the-source-reader"></a>建立來源讀取器

若要建立來源讀取器的實例，請呼叫下列其中一項功能：



| 函式                                                                                                                                                                                                                                                        | 描述                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)<br/>                                         | 使用 URL 做為輸入。 此函數會使用 [來源解析程式](source-resolver.md) ，從 URL 建立媒體來源。<br/>                                                                       |
| <span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)<br/>      | 取得位元組資料流程的指標。 此函數也會使用來源解析程式來建立媒體來源。<br/>                                                                                        |
| <span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)<br/> | 使用已建立之媒體來源的指標。 這項功能適用于來源解析程式無法建立的媒體來源，例如捕獲裝置或自訂媒體來源。<br/> |



 

通常，針對媒體檔案，請使用 [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)。 針對裝置（例如網路攝影機），請使用 [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)。  (需 Microsoft 媒體基礎中捕捉裝置的詳細資訊，請參閱 [音訊/影片捕獲](audio-video-capture.md)) 。

這些函式中的每一個都採用選擇性的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標，此指標可用來在來源讀取器上設定各種選項，如這些函式的參考主題所述。 若要取得預設行為，請將此參數設定為 **Null**。 每個函式都會傳回 [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) 指標作為輸出參數。 在呼叫任何這些函式之前，您必須先呼叫 **CoInitialize (例如)** 和 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 函式。

下列程式碼會從 URL 建立來源讀取器。


```C++
int __cdecl wmain(int argc, __in_ecount(argc) PCWSTR* argv)
{
    if (argc < 2)
    {
        return 1;
    }

    const WCHAR *pszURL = argv[1];

    // Initialize the COM runtime.
    HRESULT hr = CoInitializeEx(0, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        // Initialize the Media Foundation platform.
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            // Create the source reader.
            IMFSourceReader *pReader;
            hr = MFCreateSourceReaderFromURL(pszURL, NULL, &pReader);
            if (SUCCEEDED(hr))
            {
                ReadMediaFile(pReader);
                pReader->Release();
            }
            // Shut down Media Foundation.
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="enumerating-output-formats"></a>列舉輸出格式

每個媒體來源都至少有一個資料流程。 例如，影片檔案可能包含影片串流和音訊串流。 每個資料流程的格式都會使用 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面所代表的媒體類型來描述。 如需媒體類型的詳細資訊，請參閱 [媒體類型](media-types.md)。 您必須檢查媒體類型，以瞭解您從來源讀取器取得的資料格式。

一開始，每個資料流程都有預設格式，您可以藉由呼叫 [**IMFSourceReader：： GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) 方法來找到此格式：

針對每個資料流程，媒體來源會提供該資料流程可能的媒體類型清單。 類型數目取決於來源。 如果來源代表媒體檔案，則每個資料流程通常只有一種類型。 另一方面，網路攝影機可能能夠以數種不同的格式串流影片。 在此情況下，應用程式可以從媒體類型清單中選取要使用的格式。

若要取得資料流程的其中一種媒體類型，請呼叫 [**IMFSourceReader：： GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) 方法。 這個方法會採用兩個索引參數：資料流程的索引，以及資料流程的媒體類型清單中的索引。 若要列舉資料流程的所有型別，請在保留資料流程索引常數時遞增清單索引。 當清單索引超出範圍時， **GetNativeMediaType** 會傳回 **MF \_ E \_ NO \_ 其他 \_ 類型**。


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



若要列舉每個資料流程的媒體類型，請遞增資料流程索引。 當資料流程索引超出範圍時， [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) 會傳回 **MF \_ E \_ INVALIDSTREAMNUMBER**。


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



## <a name="setting-output-formats"></a>設定輸出格式

若要變更輸出格式，請呼叫 [**IMFSourceReader：： SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) 方法。 這個方法會採用資料流程索引和媒體類型：

``` syntax
hr = pReader->SetCurrentMediaType(dwStreamIndex, pMediaType);
```

針對媒體類型，它取決於您是否要插入解碼器。

-   若要直接從來源取得資料，而不將其解碼，請使用 [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype)所傳回的其中一個類型。
-   若要解碼資料流程，請建立新的媒體類型，以描述所需的未壓縮格式。

在解碼器的案例中，建立媒體類型，如下所示：

1.  呼叫 [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) 來建立新的媒體類型。
2.  將 [ [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md) ] 屬性設定為指定音訊或影片。
3.  設定 [ [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md) ] 屬性，以指定解碼格式的子類型。  (查看 [音訊子類型 guid](audio-subtype-guids.md) 和 [影片子類型 guid](video-subtype-guids.md)。 ) 
4.  呼叫 [**IMFSourceReader：： SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)。

來源讀取器將會自動載入該解碼器。 若要取得已解碼格式的完整詳細資料，請在呼叫 [**SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)之後呼叫 [**IMFSourceReader：： GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype)

下列程式碼會設定 RGB-32 的影片串流，以及 PCM 音訊的音訊串流。


```C++
HRESULT ConfigureDecoder(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    IMFMediaType *pNativeType = NULL;
    IMFMediaType *pType = NULL;

    // Find the native format of the stream.
    HRESULT hr = pReader->GetNativeMediaType(dwStreamIndex, 0, &pNativeType);
    if (FAILED(hr))
    {
        return hr;
    }

    GUID majorType, subtype;

    // Find the major type.
    hr = pNativeType->GetGUID(MF_MT_MAJOR_TYPE, &majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Define the output type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Select a subtype.
    if (majorType == MFMediaType_Video)
    {
        subtype= MFVideoFormat_RGB32;
    }
    else if (majorType == MFMediaType_Audio)
    {
        subtype = MFAudioFormat_PCM;
    }
    else
    {
        // Unrecognized type. Skip.
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the uncompressed format.
    hr = pReader->SetCurrentMediaType(dwStreamIndex, NULL, pType);
    if (FAILED(hr))
    {
        goto done;
    }

done:
    SafeRelease(&pNativeType);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="processing-media-data"></a>處理媒體資料

若要從來源取得媒體資料，請呼叫 [**IMFSourceReader：： ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) 方法，如下列程式碼所示。


```C++
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );
```



第一個參數是您想要取得資料之資料流程的索引。 您也可以指定 **MF \_ 來源 \_ 讀取器 \_ 任何 \_ 串流** ，以從任何串流取得下一個可用的資料。 第二個參數包含選擇性旗標;如需這些的清單，請參閱 [**MF \_ 來源 \_ 讀取器 \_ 控制 \_ 旗**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) 標。 第三個參數會接收實際產生資料之資料流程的索引。 如果您將第一個參數設定為 **MF \_ 來源 \_ 讀取器 \_ 任何 \_ 資料流程**，您將需要此資訊。 第四個參數會接收狀態旗標，指出讀取資料時可能發生的各種事件，例如資料流程中的格式變更。 如需狀態旗標的清單，請參閱 [**MF \_ 來源 \_ 讀取器 \_ 旗**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag)標。

如果媒體來源可以產生所要求資料流程的資料，則 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) 的最後一個參數會接收媒體範例物件的 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面指標。 使用媒體範例：

-   取得媒體資料的指標。
-   取得簡報時間和取樣持續時間。
-   取得描述交錯、欄位支配和其他範例層面的屬性。

媒體資料的內容取決於資料流程的格式。 針對未壓縮的影片資料流程，每個媒體範例都包含單一的影片畫面。 針對未壓縮的音訊串流，每個媒體範例都包含一連串的音訊畫面格。

[**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)方法可以傳回「 **\_ 確定**」，但不會傳回 *pSample* 參數中的媒體範例。 例如，當您到達檔案結尾時， **ReadSample** 會在 *DwFlags* 中設定 **MF \_ 來源 \_ READERF \_ ENDOFSTREAM** 旗標，並將 *pSample* 設定為 **Null**。 在此情況下， **ReadSample** 方法會傳回 S，因為未發生任何錯誤，即使 *pSample* 參數設定為 **Null** 也是一樣。 **\_** 因此，請一律先檢查 *pSample* 的值，再進行取值。

下列程式碼示範如何在迴圈中呼叫 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) ，並檢查方法傳回的資訊，直到到達媒體檔案的結尾為止。


```C++
HRESULT ProcessSamples(IMFSourceReader *pReader)
{
    HRESULT hr = S_OK;
    IMFSample *pSample = NULL;
    size_t  cSamples = 0;

    bool quit = false;
    while (!quit)
    {
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );

        if (FAILED(hr))
        {
            break;
        }

        wprintf(L"Stream %d (%I64d)\n", streamIndex, llTimeStamp);
        if (flags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            wprintf(L"\tEnd of stream\n");
            quit = true;
        }
        if (flags & MF_SOURCE_READERF_NEWSTREAM)
        {
            wprintf(L"\tNew stream\n");
        }
        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            wprintf(L"\tNative type changed\n");
        }
        if (flags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            wprintf(L"\tCurrent type changed\n");
        }
        if (flags & MF_SOURCE_READERF_STREAMTICK)
        {
            wprintf(L"\tStream tick\n");
        }

        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            // The format changed. Reconfigure the decoder.
            hr = ConfigureDecoder(pReader, streamIndex);
            if (FAILED(hr))
            {
                break;
            }
        }

        if (pSample)
        {
            ++cSamples;
        }

        SafeRelease(&pSample);
    }

    if (FAILED(hr))
    {
        wprintf(L"ProcessSamples FAILED, hr = 0x%x\n", hr);
    }
    else
    {
        wprintf(L"Processed %d samples\n", cSamples);
    }
    SafeRelease(&pSample);
    return hr;
}
```



## <a name="draining-the-data-pipeline"></a>清空資料管線

在資料處理期間，解碼器或其他轉換可能會緩衝輸入範例。 在下圖中，應用程式會呼叫 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) ，並接收表示時間等於 *t1* 的範例。 此解碼器持有 *t2* 和 *t3* 的範例。

![顯示在解碼器中緩衝的圖例。](images/sourcereader02.png)

在下一次呼叫 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)時，來源讀取器可能會將 *t4* 提供給該解碼，並將 *t2* 傳回給應用程式。

如果您想要將目前在解碼器中緩衝處理的所有樣本解碼，而不將任何新的範例傳遞給該解碼器，請在 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)的 *dwControlFlags* 參數中設定 **MF \_ 來源 \_ 讀取器 \_ CONTROLF \_ 清空** 旗標。 繼續在迴圈中執行此動作，直到 **ReadSample** 傳回 **Null** 範例指標為止。 視解碼器緩衝範例的方式而定，這可能會在 **ReadSample** 的數個呼叫之後立即發生。

## <a name="getting-the-file-duration"></a>取得檔案持續時間

若要取得媒體檔案的持續時間，請呼叫 [**IMFSourceReader：： GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) 方法，並要求 [**MF \_ PD \_ duration**](mf-pd-duration-attribute.md) 屬性，如下列程式碼所示。


```C++
HRESULT GetDuration(IMFSourceReader *pReader, LONGLONG *phnsDuration)
{
    PROPVARIANT var;
    HRESULT hr = pReader->GetPresentationAttribute(MF_SOURCE_READER_MEDIASOURCE, 
        MF_PD_DURATION, &var);
    if (SUCCEEDED(hr))
    {
        hr = PropVariantToInt64(var, phnsDuration);
        PropVariantClear(&var);
    }
    return hr;
}
```



此處顯示的函式會取得 100-毫微秒單位的持續時間。 除以10000000以取得持續時間（以秒為單位）。

## <a name="seeking"></a>尋求

從本機檔案取得資料的媒體來源通常可以搜尋檔案中的任意位置。 捕捉設備（例如網路攝影機）通常無法搜尋，因為資料是即時的。 根據網路串流通訊協定，在網路上串流資料的來源可能可以搜尋。

若要找出媒體來源是否可以搜尋，請呼叫 [**IMFSourceReader：： GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) ，並要求 [ [MF \_ 來源 \_ 讀取器 \_ MEDIASOURCE \_ 特性](mf-source-reader-mediasource-characteristics.md) ] 屬性，如下列程式碼所示：


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



此函數會從來源取得一組功能旗標。 這些旗標定義于 [**MFMEDIASOURCE \_ 特性**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) 列舉中。 與搜尋相關的兩個旗標：



| 旗標                                                                                                                                      | 描述                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE \_ 可以 \_ 搜尋**<br/>                 | 來源可以搜尋。<br/>                                                                                                                                                                            |
| <span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE \_ 有 \_ 緩慢的 \_ 搜尋**<br/> | 搜尋可能需要很長的時間才能完成。 例如，來源可能需要先下載整個檔案，才能進行搜尋。  (沒有任何嚴格準則可讓來源傳回此旗標。 ) <br/> |



 

下列程式碼 **會測試 MFMEDIASOURCE \_ 可以 \_ 搜尋** 旗標。


```C++
BOOL SourceCanSeek(IMFSourceReader *pReader)
{
    BOOL bCanSeek = FALSE;
    ULONG flags;
    if (SUCCEEDED(GetSourceFlags(pReader, &flags)))
    {
        bCanSeek = ((flags & MFMEDIASOURCE_CAN_SEEK) == MFMEDIASOURCE_CAN_SEEK);
    }
    return bCanSeek;
}
```



若要搜尋，請呼叫 [**IMFSourceReader：： SetCurrentPosition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) 方法，如下列程式碼所示。


```C++
HRESULT SetPosition(IMFSourceReader *pReader, const LONGLONG& hnsPosition)
{
    PROPVARIANT var;
    HRESULT hr = InitPropVariantFromInt64(hnsPosition, &var);
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentPosition(GUID_NULL, var);
        PropVariantClear(&var);
    }
    return hr;
}
```



第一個參數會提供您用來指定搜尋位置的時間格式。 媒體基礎中的所有媒體來源都必須支援 100-納秒的單位，由值 **GUID \_ Null** 表示。 第二個參數是包含搜尋位置的 **PROPVARIANT** 。 若為 100-納秒的時間單位，資料類型為 **LONGLONG**。

請注意，並非每個媒體來源都提供框架精確的搜尋。 搜尋的精確度取決於數個因素，例如主要畫面格間隔、媒體檔案是否包含索引，以及資料是否具有固定或變數位元速率。 因此，在您搜尋檔案中的位置之後，就無法保證下一個範例中的時間戳記會完全符合要求的位置。 一般來說，實際的位置不會晚于要求的位置，因此您可以捨棄樣本，直到到達資料流程中的所需點為止。

## <a name="playback-rate"></a>播放速率

雖然您可以使用來源讀取器來設定播放速率，但這通常不太實用，原因如下：

-   來源讀取器不支援反向播放，即使媒體來源確實如此。
-   應用程式會控制呈現時間，讓應用程式可以在不設定來源的速率的情況下，執行快速或緩慢的播放。
-   有些媒體來源支援 *thinning* 模式，其中來源提供較少的樣本，通常只是主要畫面格。 但是，如果您想要卸載非主要畫面格，您可以檢查每個範例中的 [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md) 屬性。

若要使用來源讀取器設定播放速率，請呼叫 [**IMFSourceReader：： GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) 方法，以從媒體來源取得 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) 和 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) 介面。

## <a name="hardware-acceleration"></a>硬體加速

來源讀取器相容于 Microsoft DirectX Video 加速 (DXVA) 2.0 進行硬體加速影片解碼。 若要搭配使用 DXVA 與來源讀取器，請執行下列步驟。

1.  建立 Microsoft Direct3D 裝置。
2.  呼叫 [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) 函式來建立 Direct3D 裝置管理員。 此函式會取得 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 介面的指標。
3.  使用 Direct3D 裝置的指標來呼叫 [**IDirect3DDeviceManager9：： ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) 方法。
4.  藉由呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 函數來建立屬性存放區。
5.  建立來源讀取器。 在建立函數的 *pAttributes* 參數中傳遞屬性存放區。

當您提供 Direct3D 裝置時，來源讀取器會配置與 DXVA video 處理器 API 相容的影片範例。 您可以使用 DXVA 影片處理來執行硬體去交錯或視頻混合。 如需詳細資訊，請參閱 [DXVA 影片處理](dxva-video-processing.md)。 此外，如果此解碼器支援 DXVA 2.0，則會使用 Direct3D 裝置來執行硬體加速解碼。

> [!IMPORTANT]
> 從 Windows 8 開始，可以使用 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) ，而不是 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)。 針對 Windows Store 應用程式，您必須使用 **IMFDXGIDeviceManager**。 如需詳細資訊，請參閱 [Direct3D 11 影片 api](direct3d-11-video-apis.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[來源讀取程式](source-reader.md)
</dt> </dl>

 

 




