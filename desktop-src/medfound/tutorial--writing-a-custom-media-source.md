---
description: 本主題深入探討 MPEG-2 媒體來源 SDK 範例。
ms.assetid: d392f30c-c963-4eb3-add2-1bb986919c0b
title: 案例研究： MPEG-2 媒體來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e1f72cc6ae6df119439bdae1942732bf8d2fa2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104027646"
---
# <a name="case-study-mpeg-1-media-source"></a>案例研究： MPEG-2 媒體來源

在 Microsoft 媒體基礎中，將媒體資料引進資料管線的物件稱為 *媒體來源*。 本主題深入探討 [Mpeg-2 媒體來源](mpeg1source-sample.md) SDK 範例。

-   [先決條件](#prerequisites)
-   [MPEG 1 來源中使用的 c + + 類別](#c-classes-used-in-the-mpeg-1-source)
-   [位元組資料流程處理常式](#byte-stream-handler)
-   [簡報描述項](#presentation-descriptor)
-   [串流狀態](#streaming-states)
    -   [開始](#start)
    -   [暫停](#pause)
    -   [停止](#stop)
-   [範例要求](#sample-requests)
-   [資料流程結尾](#end-of-stream)
-   [非同步作業](#asynchronous-operations)
    -   [作業佇列](#operation-queue)
-   [相關主題](#related-topics)

## <a name="prerequisites"></a>必要條件

閱讀本主題之前，您應該先瞭解下列媒體基礎概念：

-   [媒體來源物件模型](media-source-object-model.md)
-   [非同步回呼方法](asynchronous-callback-methods.md)。
-   [工作佇列](work-queues.md)
-   [媒體事件產生器](media-event-generators.md)
-   [媒體緩衝區](media-buffers.md)
-   [媒體範例](media-samples.md)
-   [媒體類型](media-types.md)

您也應該對媒體基礎架構有基本的瞭解，特別是管線中媒體來源的角色。  (需詳細資訊，請參閱 [媒體來源](media-sources.md)。 ) 

此外，您可能會想要閱讀 [撰寫自訂媒體來源](writing-a-custom-media-source.md)的主題，以提供此處所述步驟的一般總覽。

本主題不會重現 SDK 範例中的所有程式碼，因為此範例相當大。

## <a name="c-classes-used-in-the-mpeg-1-source"></a>MPEG 1 來源中使用的 c + + 類別

範例 MPEG-2 來源會使用下列 c + + 類別來執行：

-   `MPEG1ByteStreamHandler`. 針對媒體來源執行位元組資料流程處理常式。 在指定位元組資料流程的情況下，位元組資料流程處理常式會建立來源的實例。
-   `MPEG1Source`. 實行媒體來源。
-   `MPEG1Stream`. 實行媒體資料流程物件。 媒體來源會 `MPEG1Stream` 為 MPEG 1 位流中的每個音訊或影片串流建立一個物件。
-   `Parser`. 剖析 MPEG 1 位流。 在大部分的情況下，這個類別的詳細資料與媒體基礎 Api 無關。
-   SourceOp，OpQueue：這兩個類別會管理媒體來源中的非同步作業。  (查看) 的 [非同步作業](#asynchronous-operations) 。

本主題稍後將說明其他其他協助程式類別。

## <a name="byte-stream-handler"></a>Byte-Stream 處理常式

*位元組資料流程* 處理常式是建立媒體來源的物件。 位元組資料流程處理常式是由來源解析程式所建立;應用程式不會直接與位元組資料流程處理常式互動。 來源解析程式會藉由查看登錄來探索位元組資料流程處理常式。 處理常式是依副檔名或 MIME 類型來註冊。 針對 MPEG-2 來源，位元組資料流程處理常式會註冊 ". mpg" 副檔名。

> [!Note]  
> 如果您想要支援自訂 URL 配置，您也可以撰寫 *配置處理常式*。 MPEG-2 來源是針對本機檔案所設計，媒體基礎已經提供 "file://" Url 的配置處理常式。

 

位元組資料流程處理常式會執行 [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) 介面。 這個介面有兩個必須執行的最重要方法：

-   [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject)。 開始非同步作業以建立媒體來源。
-   [**EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject)。 完成非同步呼叫。

另外兩個方法是選擇性的，且未在 SDK 範例中執行：

-   [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation)。 取消 [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) 方法。 此方法適用于啟動時可能會有高延遲的網路來源。
-   [**GetMaxNumberOfBytesRequiredForResolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution)。 取得處理常式將從來來源資料流讀取的最大位元組數目。 如果您知道位元組資料流程處理常式可以建立媒體來源之前的資料量，請執行此方法。 否則，只會傳回 **E \_ >notimpl**。

以下是 [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) 方法的實作為：


```C++
HRESULT MPEG1ByteStreamHandler::BeginCreateObject(
        /* [in] */ IMFByteStream *pByteStream,
        /* [in] */ LPCWSTR pwszURL,
        /* [in] */ DWORD dwFlags,
        /* [in] */ IPropertyStore *pProps,
        /* [out] */ IUnknown **ppIUnknownCancelCookie,  // Can be NULL
        /* [in] */ IMFAsyncCallback *pCallback,
        /* [in] */ IUnknown *punkState                  // Can be NULL
        )
{
    if (pByteStream == NULL)
    {
        return E_POINTER;
    }

    if (pCallback == NULL)
    {
        return E_POINTER;
    }

    if ((dwFlags & MF_RESOLUTION_MEDIASOURCE) == 0)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFAsyncResult *pResult = NULL;
    MPEG1Source    *pSource = NULL;

    // Create an instance of the media source.
    hr = MPEG1Source::CreateInstance(&pSource);

    // Create a result object for the caller's async callback.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);
    }

    // Start opening the source. This is an async operation.
    // When it completes, the source will invoke our callback
    // and then we will invoke the caller's callback.
    if (SUCCEEDED(hr))
    {
        hr = pSource->BeginOpen(pByteStream, this, NULL);
    }

    if (SUCCEEDED(hr))
    {
        if (ppIUnknownCancelCookie)
        {
            *ppIUnknownCancelCookie = NULL;
        }

        m_pSource = pSource;
        m_pSource->AddRef();

        m_pResult = pResult;
        m_pResult->AddRef();
    }

// cleanup
    SafeRelease(&pSource);
    SafeRelease(&pResult);
    return hr;
}
```



此方法會執行下列步驟：

1.  建立 `MPEG1Source` 物件的新執行個體。
2.  建立異步結果物件。 稍後會使用此物件來叫用來源解析程式的回呼方法。
3.  呼叫 `MPEG1Source::BeginOpen` ，在類別中定義的非同步方法 `MPEG1Source` 。
4.  將 *ppIUnknownCancelCookie* 設定為 **Null**，這會通知呼叫端不支援 [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) 。

`MPEG1Source::BeginOpen`方法會執行讀取位元組資料流程和初始化物件的實際工作 `MPEG1Source` 。 這個方法不是公用 API 的一部分。 您可以在處理常式和媒體來源之間定義符合您需求的任何機制。 將大部分的邏輯放入媒體來源，可讓位元組資料流程處理常式保持相當簡單。

簡單地說， `BeginOpen` 會執行下列動作：

1.  呼叫 [**IMFByteStream：： GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) ，以驗證來源位元組資料流程是否可讀取和可搜尋。
2.  呼叫 [**IMFByteStream：： BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) 來啟動非同步 i/o 要求。

其餘的初始化會以非同步方式進行。 媒體來源會從資料流程讀取足夠的資料，以剖析 MPEG-2 序列標頭。 然後，它會建立 *展示* 描述項，這是用來描述檔案中音訊和影片資料流程的物件。  (如需詳細資訊，請參閱 [展示描述](#presentation-descriptor)項。當作業完成時 ) `BeginOpen` ，位元組資料流程處理常式會叫用來源解析程式的回呼方法。 屆時，來源解析程式會呼叫 [**IMFByteStreamHandler：： EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject)。 **EndCreateObject** 方法會傳回作業的狀態。


```C++
HRESULT MPEG1ByteStreamHandler::EndCreateObject(
        /* [in] */ IMFAsyncResult *pResult,
        /* [out] */ MF_OBJECT_TYPE *pObjectType,
        /* [out] */ IUnknown **ppObject)
{
    if (pResult == NULL || pObjectType == NULL || ppObject == NULL)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    *pObjectType = MF_OBJECT_INVALID;
    *ppObject = NULL;

    hr = pResult->GetStatus();

    if (SUCCEEDED(hr))
    {
        *pObjectType = MF_OBJECT_MEDIASOURCE;

        assert(m_pSource != NULL);

        hr = m_pSource->QueryInterface(IID_PPV_ARGS(ppObject));
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pResult);
    return hr;
}
```



如果在此程式期間任何時候發生錯誤，則會叫用具有錯誤狀態碼的回呼。

## <a name="presentation-descriptor"></a>簡報描述項

簡報描述項描述 MPEG-2 檔案的內容，包括下列資訊：

-   資料流程的數目。
-   每個資料流程的格式。
-   資料流程識別碼。
-   每個資料流程的選取狀態 (選取或取消選取) 。

就媒體基礎架構而言，表示描述項會包含一或多個 *資料流程描述* 項。 每個資料流程描述項都包含一個 *媒體類型處理常式*，可用來取得或設定資料流程上的媒體類型。 媒體基礎提供簡報描述元和資料流程描述項的內建實值;這些適用于大部分的媒體來源。

若要建立展示描述項，請執行下列步驟：

1.  針對每個資料流程：
    1.  提供資料流程識別碼和可能媒體類型的陣列。 如果資料流程支援一種以上的媒體類型，請依喜好設定排列媒體類型清單（若有的話）。  (先放置最佳類型，最後才是最不理想的類型。 ) 
    2.  呼叫 [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) 來建立資料流程描述項。
    3.  在新建立的資料流程描述項上呼叫 [**IMFStreamDescriptor：： GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) 。
    4.  呼叫 [**IMFMediaTypeHandler：： SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) 來設定資料流程的預設格式。 如果有一種以上的媒體類型，您通常應該設定清單中的第一種類型。
2.  呼叫 [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) 並傳入資料流程描述項指標的陣列。
3.  針對每個資料流程，呼叫 [**IMFPresentationDescriptor：： SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) 或 [**DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) 來設定預設選取狀態。 如果有多個相同類型的資料流程 (音訊或影片) ，預設應該只選取其中一個。

`MPEG1Source`物件會在其方法中建立展示描述項 `InitPresentationDescriptor` ：


```C++
HRESULT MPEG1Source::InitPresentationDescriptor()
{
    HRESULT hr = S_OK;
    DWORD cStreams = 0;

    assert(m_pPresentationDescriptor == NULL);
    assert(m_state == STATE_OPENING);

    if (m_pHeader == NULL)
    {
        return E_FAIL;
    }

    // Get the number of streams, as declared in the MPEG-1 header, skipping
    // any streams with an unsupported format.
    for (DWORD i = 0; i < m_pHeader->cStreams; i++)
    {
        if (IsStreamTypeSupported(m_pHeader->streams[i].type))
        {
            cStreams++;
        }
    }

    // How many streams do we actually have?
    if (cStreams > m_streams.GetCount())
    {
        // Keep reading data until we have seen a packet for each stream.
        return S_OK;
    }

    // We should never create a stream we don't support.
    assert(cStreams == m_streams.GetCount());

    // Ready to create the presentation descriptor.

    // Create an array of IMFStreamDescriptor pointers.
    IMFStreamDescriptor **ppSD =
            new (std::nothrow) IMFStreamDescriptor*[cStreams];

    if (ppSD == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    ZeroMemory(ppSD, cStreams * sizeof(IMFStreamDescriptor*));

    // Fill the array by getting the stream descriptors from the streams.
    for (DWORD i = 0; i < cStreams; i++)
    {
        hr = m_streams[i]->GetStreamDescriptor(&ppSD[i]);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Create the presentation descriptor.
    hr = MFCreatePresentationDescriptor(cStreams, ppSD,
        &m_pPresentationDescriptor);

    if (FAILED(hr))
    {
        goto done;
    }

    // Select the first video stream (if any).
    for (DWORD i = 0; i < cStreams; i++)
    {
        GUID majorType = GUID_NULL;

        hr = GetStreamMajorType(ppSD[i], &majorType);
        if (FAILED(hr))
        {
            goto done;
        }

        if (majorType == MFMediaType_Video)
        {
            hr = m_pPresentationDescriptor->SelectStream(i);
            if (FAILED(hr))
            {
                goto done;
            }
            break;
        }
    }

    // Switch state from "opening" to stopped.
    m_state = STATE_STOPPED;

    // Invoke the async callback to complete the BeginOpen operation.
    hr = CompleteOpen(S_OK);

done:
    // clean up:
    if (ppSD)
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            SafeRelease(&ppSD[i]);
        }
        delete [] ppSD;
    }
    return hr;
}
```



應用程式會藉由呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)來取得簡報描述項。 這個方法會藉由呼叫 [**IMFPresentationDescriptor：： Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone)來建立簡報描述項的淺層複本。  (複本包含原始資料流程描述項的指標。 ) 應用程式可以使用展示描述項來設定媒體類型、選取資料流程或取消選取資料流程。

（選擇性）表示描述項和資料流程描述項可以包含屬性，以提供來源的其他相關資訊。 如需屬性的清單，請參閱下列主題：

-   [展示描述項屬性](presentation-descriptor-attributes.md)
-   [資料流程描述元屬性](stream-descriptor-attributes.md)

其中一個屬性值得特別注明： [ [**MF \_ PD \_ duration**](mf-pd-duration-attribute.md) ] 屬性包含來源的總持續時間。 如果您事先知道持續時間，請設定此屬性;例如，視檔案格式而定，可能會在檔案標頭中指定持續時間。 應用程式可能會顯示此值，或使用它來設定進度列或搜尋列。

## <a name="streaming-states"></a>串流狀態

媒體來源會定義下列狀態：



| 州    | 描述                                                                                                     |
|----------|-----------------------------------------------------------------------------------------------------------------|
| 已開始  | 來源接受並處理範例要求。                                                               |
| 已暫停   | 來源接受範例要求，但不會處理它們。 要求會排入佇列，直到來源啟動為止。 |
| 已停止。 | 來源會拒絕範例要求。                                                                             |



 

### <a name="start"></a>開始

[**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)方法會啟動媒體來源。 它需要以下參數：

-   展示描述項。
-   時間格式 GUID。
-   開始位置。

應用程式必須藉由在來源上呼叫 [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) 來取得簡報描述項。 沒有任何已定義的機制可驗證簡報描述項。 如果應用程式指定錯誤的表示描述項，則會產生未定義的結果。

時間格式 GUID 會指定如何解讀開始位置。 標準格式為 100-納 (ns) 單位，以 GUID Null 表示 \_ 。 每個媒體來源都必須支援 100-ns 單位。 （選擇性）來源可支援其他時間單位，例如框架數或時間代碼。 不過，沒有標準的方式可以查詢媒體來源，以取得它所支援的時間格式清單。

開始位置會以 **PROPVARIANT** 的形式提供，根據時間格式允許不同的資料類型。 若為 100-ns， **PROPVARIANT** 類型為 **Vt \_ I8** 或 **vt \_ 空白**。 如果 **VT \_ I8**， **PROPVARIANT** 就會包含 100-ns 單位中的開始位置。 **VT \_ 空白** 值具有「從目前位置開始」的特殊意義。

依照下列方式執行 [**啟動**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 方法：

1.  驗證參數和狀態：
    -   檢查是否有 **Null** 參數。
    -   檢查時間格式 GUID。 如果值無效，則傳回 **MF \_ E \_ 不支援的 \_ 時間 \_ 格式**。
    -   檢查保存開始位置的 **PROPVARIANT** 資料類型。
    -   驗證開始位置。 如果無效，則傳回 **MF \_ E \_ INVALIDREQUEST**。
    -   如果來源已關閉，則傳回 **MF \_ E \_ 關機**。
2.  如果步驟1中未發生任何錯誤，請將非同步作業排入佇列。 此步驟之後的所有專案都會在工作佇列執行緒上發生。
3.  針對每個資料流程：
    1.  檢查資料流程是否已從先前的 [**啟動要求開始**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 作用中。
    2.  呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) ，以檢查應用程式是否已選取或取消選取資料流程。
    3.  如果先前選取的資料流程現在已取消選取，請清除該資料流程的任何未傳遞範例。
    4.  如果資料流程為使用中，則媒體來源 (不是資料流程) 傳送下列其中一個事件：
        -   如果資料流程先前為使用中，則會傳送 [MEUpdatedStream](meupdatedstream.md) 。
        -   否則，它會傳送 [MENewStream](menewstream.md)。

        針對這兩個事件，事件資料是資料流程的 [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) 指標。
    5.  如果來源從暫停狀態重新開機，可能會有擱置範例要求。 如果是，請立即傳遞。
    6.  如果來源正在搜尋新的位置，每個資料流程物件都會傳送 [MEStreamSeeked](mestreamseeked.md) 事件。 否則，每個資料流程都會傳送 [MEStreamStarted](mestreamstarted.md) 事件。
4.  如果來源正在搜尋新的位置，則媒體來源會傳送 [MESourceSeeked](mesourceseeked.md) 事件。 否則，它會傳送 [MESourceStarted](mesourcestarted.md) 事件。

如果在步驟2之後的任何時間發生錯誤，來源就會傳送含有錯誤碼的 [MESourceStarted](mesourcestarted.md) 事件。 這會對應用程式發出 [**啟動**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 方法非同步失敗的警示。

下列程式碼顯示步驟 1-2：


```C++
HRESULT MPEG1Source::Start(
        IMFPresentationDescriptor* pPresentationDescriptor,
        const GUID* pguidTimeFormat,
        const PROPVARIANT* pvarStartPos
    )
{

    HRESULT hr = S_OK;
    SourceOp *pAsyncOp = NULL;

    // Check parameters.

    // Start position and presentation descriptor cannot be NULL.
    if (pvarStartPos == NULL || pPresentationDescriptor == NULL)
    {
        return E_INVALIDARG;
    }

    // Check the time format.
    if ((pguidTimeFormat != NULL) && (*pguidTimeFormat != GUID_NULL))
    {
        // Unrecognized time format GUID.
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    // Check the data type of the start position.
    if ((pvarStartPos->vt != VT_I8) && (pvarStartPos->vt != VT_EMPTY))
    {
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    EnterCriticalSection(&m_critSec);

    // Check if this is a seek request. This sample does not support seeking.

    if (pvarStartPos->vt == VT_I8)
    {
        // If the current state is STOPPED, then position 0 is valid.
        // Otherwise, the start position must be VT_EMPTY (current position).

        if ((m_state != STATE_STOPPED) || (pvarStartPos->hVal.QuadPart != 0))
        {
            hr = MF_E_INVALIDREQUEST;
            goto done;
        }
    }

    // Fail if the source is shut down.
    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Fail if the source was not initialized yet.
    hr = IsInitialized();
    if (FAILED(hr))
    {
        goto done;
    }

    // Perform a basic check on the caller's presentation descriptor.
    hr = ValidatePresentationDescriptor(pPresentationDescriptor);
    if (FAILED(hr))
    {
        goto done;
    }

    // The operation looks OK. Complete the operation asynchronously.
    hr = SourceOp::CreateStartOp(pPresentationDescriptor, &pAsyncOp);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAsyncOp->SetData(*pvarStartPos);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = QueueOperation(pAsyncOp);

done:
    SafeRelease(&pAsyncOp);
    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



其餘步驟會顯示在下一個範例中：


```C++
HRESULT MPEG1Source::DoStart(StartOp *pOp)
{
    assert(pOp->Op() == SourceOp::OP_START);

    IMFPresentationDescriptor *pPD = NULL;
    IMFMediaEvent  *pEvent = NULL;

    HRESULT     hr = S_OK;
    LONGLONG    llStartOffset = 0;
    BOOL        bRestartFromCurrentPosition = FALSE;
    BOOL        bSentEvents = FALSE;

    hr = BeginAsyncOp(pOp);

    // Get the presentation descriptor from the SourceOp object.
    // This is the PD that the caller passed into the Start() method.
    // The PD has already been validated.
    if (SUCCEEDED(hr))
    {
        hr = pOp->GetPresentationDescriptor(&pPD);
    }

    // Because this sample does not support seeking, the start
    // position must be 0 (from stopped) or "current position."

    // If the sample supported seeking, we would need to get the
    // start position from the PROPVARIANT data contained in pOp.

    if (SUCCEEDED(hr))
    {
        // Select/deselect streams, based on what the caller set in the PD.
        // This method also sends the MENewStream/MEUpdatedStream events.
        hr = SelectStreams(pPD, pOp->Data());
    }

    if (SUCCEEDED(hr))
    {
        m_state = STATE_STARTED;

        // Queue the "started" event. The event data is the start position.
        hr = m_pEventQueue->QueueEventParamVar(
            MESourceStarted,
            GUID_NULL,
            S_OK,
            &pOp->Data()
            );
    }

    if (FAILED(hr))
    {
        // Failure. Send the error code to the application.

        // Note: It's possible that QueueEvent itself failed, in which case it
        // is likely to fail again. But there is no good way to recover in
        // that case.

        (void)m_pEventQueue->QueueEventParamVar(
            MESourceStarted, GUID_NULL, hr, NULL);
    }

    CompleteAsyncOp(pOp);

    SafeRelease(&pEvent);
    SafeRelease(&pPD);
    return hr;
}
```



### <a name="pause"></a>暫停

[**IMFMediaSource：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)方法會暫停媒體來源。 依照下列方式執行此方法：

1.  將非同步作業排在佇列中。
2.  每個作用中的資料流程都會傳送 [MEStreamPaused](mestreampaused.md) 事件。
3.  媒體來源會傳送 [MESourcePaused](mesourcepaused.md) 事件。

暫停時，來源會將要求排在佇列中，而不需要處理它們。  (查看 [範例要求](#sample-requests)。 ) 

### <a name="stop"></a>停止

[**IMFMediaSource：： Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop)方法會停止媒體來源。 依照下列方式執行此方法：

1.  將非同步作業排在佇列中。
2.  每個作用中的資料流程都會傳送 [MEStreamStopped](mestreamstopped.md) 事件。
3.  清除所有已排入佇列的範例和範例要求。
4.  媒體來源會傳送 [MESourceStopped](mesourcestopped.md) 事件。

當停止時，來源會拒絕範例的所有要求。

如果來源是在 i/o 要求進行時停止，則 i/o 要求可能會在來源進入 [已停止] 狀態之後完成。 在這種情況下，來源應該捨棄該 i/o 要求的結果。

## <a name="sample-requests"></a>範例要求

媒體基礎使用 *提取* 模型，在此模型中，管線會從媒體來源要求範例。 這不同于 DirectShow 所使用的模型，其中來源會「推送」範例。

若要要求新的範例，媒體基礎管線會呼叫 [**IMFMediaStream：： RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)。 這個方法會採用表示 *權杖* 物件的 **IUnknown** 指標。 Token 物件的實作為呼叫端;它只會提供一種方法讓呼叫端追蹤範例要求。 Token 參數也可以是 **Null**。

假設來源使用非同步 i/o 要求來讀取資料，則產生的範例不會與範例要求同步處理。 若要同步處理範例要求和產生範例，媒體來源會執行下列動作：

1.  要求權杖會放置在佇列中。
2.  當產生樣本時，會將它們放在第二個佇列上。
3.  媒體來源會從第一個佇列提取要求權杖，並從第二個佇列提取一個範例，以完成範例要求。
4.  媒體來源會傳送 MEMediaSample 事件。 此事件包含範例的指標，且範例包含權杖的指標。

下圖顯示 [MEMediaSample](memediasample.md) 事件、範例與要求權杖之間的關聯性。

![顯示 memediasample 和指向 imfsample 的範例佇列的圖表;imfsample 和要求佇列點至 iunknown](images/mediasourceimpl01.png)

範例 MPEG-2 來源會依照下列方式來執行此程式：

1.  [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)方法會將要求放在 FIFO 佇列上。
2.  當 i/o 要求完成時，媒體來源會建立新的範例，並將它們放在第二個 FIFO 佇列上。  (此佇列的大小上限，以防止來源讀取太遠的進度。 ) 
3.  只要兩個佇列都至少有一個專案 (一個要求和一個範例) ，媒體來源就會從範例佇列中送出第一個範例，以完成要求佇列中的第一個要求。
4.  為了傳遞範例，資料流程物件 (不是) 傳送 [MEMediaSample](memediasample.md) 事件的來源物件。
    -   事件資料是範例 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面的指標。
    -   如果要求包含權杖，請在範例上設定 [**MFSampleExtension \_ token**](mfsampleextension-token-attribute.md) 屬性，以將權杖附加至範例。

目前有三種可能性：

-   範例佇列中有另一個範例，但沒有相符的要求。
-   有一個要求，但沒有範例。
-   這兩個佇列都是空的;沒有任何範例和要求。

如果範例佇列是空的，則來源會檢查資料流程的結尾 (查看資料流程) 的 [結尾](#end-of-stream) 。 否則，它會啟動資料的另一個 i/o 要求。 如果在此程式期間發生任何錯誤，資料流程將會傳送 [MEError](meerror.md) 事件。

下列程式碼會實行 [**IMFMediaStream：： RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) 方法：


```C++
HRESULT MPEG1Stream::RequestSample(IUnknown* pToken)
{
    HRESULT hr = S_OK;
    IMFMediaSource *pSource = NULL;

    // Hold the media source object's critical section.
    SourceLock lock(m_pSource);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_state == STATE_STOPPED)
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (!m_bActive)
    {
        // If the stream is not active, it should not get sample requests.
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (m_bEOS && m_Samples.IsEmpty())
    {
        // This stream has already reached the end of the stream, and the
        // sample queue is empty.
        hr = MF_E_END_OF_STREAM;
        goto done;
    }

    hr = m_Requests.InsertBack(pToken);
    if (FAILED(hr))
    {
        goto done;
    }

    // Dispatch the request.
    hr = DispatchSamples();
    if (FAILED(hr))
    {
        goto done;
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        hr = m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }
    return hr;
}
```



`DispatchSamples`方法會從範例佇列提取範例、將它們與擱置的範例要求比對，以及佇列[MEMediaSample](memediasample.md)事件：


```C++
HRESULT MPEG1Stream::DispatchSamples()
{
    HRESULT hr = S_OK;
    BOOL bNeedData = FALSE;
    BOOL bEOS = FALSE;

    SourceLock lock(m_pSource);

    // An I/O request can complete after the source is paused, stopped, or
    // shut down. Do not deliver samples unless the source is running.
    if (m_state != STATE_STARTED)
    {
        return S_OK;
    }

    IMFSample *pSample = NULL;
    IUnknown  *pToken = NULL;

    // Deliver as many samples as we can.
    while (!m_Samples.IsEmpty() && !m_Requests.IsEmpty())
    {
        // Pull the next sample from the queue.
        hr = m_Samples.RemoveFront(&pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Pull the next request token from the queue. Tokens can be NULL.
        hr = m_Requests.RemoveFront(&pToken);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pToken)
        {
            // Set the token on the sample.
            hr = pSample->SetUnknown(MFSampleExtension_Token, pToken);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Send an MEMediaSample event with the sample.
        hr = m_pEventQueue->QueueEventParamUnk(
            MEMediaSample, GUID_NULL, S_OK, pSample);

        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pSample);
        SafeRelease(&pToken);
    }

    if (m_Samples.IsEmpty() && m_bEOS)
    {
        // The sample queue is empty AND we have reached the end of the source
        // stream. Notify the pipeline by sending the end-of-stream event.

        hr = m_pEventQueue->QueueEventParamVar(
            MEEndOfStream, GUID_NULL, S_OK, NULL);

        if (FAILED(hr))
        {
            goto done;
        }

        // Notify the source. It will send the end-of-presentation event.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_END_OF_STREAM);
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (NeedsData())
    {
        // The sample queue is empty; the request queue is not empty; and we
        // have not reached the end of the stream. Ask for more data.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_REQUEST_DATA);
        if (FAILED(hr))
        {
            goto done;
        }
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }

    SafeRelease(&pSample);
    SafeRelease(&pToken);
    return S_OK;
}
```



在 `DispatchSamples` 下列情況下，會呼叫方法：

-   在 [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) 方法內。
-   當媒體來源從暫停狀態重新開機時。
-   當 i/o 要求完成時。

## <a name="end-of-stream"></a>資料流程結尾

當資料流程沒有其他資料，而且已傳遞該資料流程的所有範例時，資料流程物件就會傳送 [MEEndOfStream](meendofstream.md) 事件。

當所有作用中資料流程完成時，媒體來源會傳送 [MEEndOfPresentation](meendofpresentation.md) 事件。

## <a name="asynchronous-operations"></a>非同步作業

撰寫媒體來源最困難的部分是瞭解媒體基礎的非同步模型。

媒體來源上控制串流的所有方法都是非同步。 在每個案例中，方法會執行一些初始驗證，例如檢查參數。 然後，來源會將其餘的工作分派至工作佇列。 作業完成之後，媒體來源會透過媒體來源的 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面，將事件傳回給呼叫者。 因此，瞭解工作佇列是很重要的。

若要將專案放在工作佇列中，您可以呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) 或 [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex)。 MPEG-2 來源是使用 **MFPutWorkItem**，但這兩個函式會執行相同的動作。 **MFPutWorkItem** 函式會使用下列參數：

-   識別工作佇列的 **DWORD** 值。 您可以建立私用工作佇列，或使用 **MFASYNC \_ 回呼 \_ 佇列 \_ 標準**。
-   [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)介面的指標。 叫用此回呼介面來執行工作。
-   選用的狀態物件，必須執行 **IUnknown**。

工作佇列是由一或多個背景工作執行緒所提供，這些執行緒會持續從佇列提取下一個工作專案，並叫用回呼介面的 [**IMFAsyncCallback：： invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法。

不保證會以您將工作專案放在佇列上的相同順序來執行工作專案。 請記住，有一個以上的執行緒可以服務相同的工作佇列 [**，因此叫**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 用呼叫可以依順序重迭或發生。 因此，以正確的順序提交工作佇列專案，可由媒體來源維持正確的內部狀態。 只有當先前的作業完成時，來源才會開始下一項作業。

為了表示暫止的作業，MPEG 1 來源定義了名為的類別 `SourceOp` ：


```C++
// Represents a request for an asynchronous operation.

class SourceOp : public IUnknown
{
public:

    enum Operation
    {
        OP_START,
        OP_PAUSE,
        OP_STOP,
        OP_REQUEST_DATA,
        OP_END_OF_STREAM
    };

    static HRESULT CreateOp(Operation op, SourceOp **ppOp);
    static HRESULT CreateStartOp(IMFPresentationDescriptor *pPD, SourceOp **ppOp);

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    SourceOp(Operation op);
    virtual ~SourceOp();

    HRESULT SetData(const PROPVARIANT& var);

    Operation Op() const { return m_op; }
    const PROPVARIANT& Data() { return m_data;}

protected:
    long        m_cRef;     // Reference count.
    Operation   m_op;
    PROPVARIANT m_data;     // Data for the operation.
};
```



`Operation`列舉會識別正在暫止的作業。 類別也包含 **PROPVARIANT** ，以傳達作業的任何其他資料。

### <a name="operation-queue"></a>作業佇列

為了序列化作業，媒體來源會維護物件的佇列 `SourceOp` 。 它會使用 helper 類別來管理佇列：


```C++
template <class OP_TYPE>
class OpQueue : public IUnknown
{
public:

    typedef ComPtrList<OP_TYPE>   OpList;

    HRESULT QueueOperation(OP_TYPE *pOp);

protected:

    HRESULT ProcessQueue();
    HRESULT ProcessQueueAsync(IMFAsyncResult *pResult);

    virtual HRESULT DispatchOperation(OP_TYPE *pOp) = 0;
    virtual HRESULT ValidateOperation(OP_TYPE *pOp) = 0;

    OpQueue(CRITICAL_SECTION& critsec)
        : m_OnProcessQueue(this, &OpQueue::ProcessQueueAsync),
          m_critsec(critsec)
    {
    }

    virtual ~OpQueue()
    {
    }

protected:
    OpList                  m_OpQueue;         // Queue of operations.
    CRITICAL_SECTION&       m_critsec;         // Protects the queue state.
    AsyncCallback<OpQueue>  m_OnProcessQueue;  // ProcessQueueAsync callback.
};
```



`OpQueue`類別的設計是要由執行非同步工作專案的元件所繼承。 *Op \_ 型* 別範本參數是用來表示佇列中之工作專案的物件類型，在此案例中， *op \_ 類型* 會是 `SourceOp` 。 `OpQueue`類別會執行下列方法：

-   `QueueOperation` 將新專案放在佇列上。
-   `ProcessQueue` 從佇列分派下一次作業。 這個方法是非同步方法。
-   `ProcessQueueAsync` 完成非同步 `ProcessQueue` 方法。

另兩個方法必須由衍生類別來執行：

-   `ValidateOperation` 在指定媒體來源的目前狀態時，檢查是否有效，以執行指定的作業。
-   `DispatchOperation` 執行非同步工作專案。

作業佇列的使用方式如下：

1.  媒體基礎管線會呼叫媒體來源上的非同步方法，例如 [**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)。
2.  非同步方法會呼叫 `QueueOperation` ，這會將 [**開始**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 作業放在佇列上，並 `ProcessQueue` 以物件) 的形式呼叫 (`SourceOp` 。
3.  `ProcessQueue` 呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem)。
4.  工作佇列執行緒會呼叫 `ProcessQueueAsync` 。
5.  `ProcessQueueAsync`方法會呼叫 `ValidateOperation` 和 `DispatchOperation` 。

下列程式碼會將 MPEG-2 來源上的新作業排入佇列：


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::QueueOperation(OP_TYPE *pOp)
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_critsec);

    hr = m_OpQueue.InsertBack(pOp);
    if (SUCCEEDED(hr))
    {
        hr = ProcessQueue();
    }

    LeaveCriticalSection(&m_critsec);
    return hr;
}
```



下列程式碼會處理佇列：


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::ProcessQueue()
{
    HRESULT hr = S_OK;
    if (m_OpQueue.GetCount() > 0)
    {
        hr = MFPutWorkItem(
            MFASYNC_CALLBACK_QUEUE_STANDARD,    // Use the standard work queue.
            &m_OnProcessQueue,                  // Callback method.
            NULL                                // State object.
            );
    }
    return hr;
}
```



`ValidateOperation`方法會檢查 mpeg-2 來源是否可以分派佇列中的下一項作業。 如果另一個作業正在進行中，則會傳回 `ValidateOperation` **MF \_ E \_ NOTACCEPTING**。 這可確保 `DispatchOperation` 當另一個作業暫止時，不會呼叫。


```C++
HRESULT MPEG1Source::ValidateOperation(SourceOp *pOp)
{
    if (m_pCurrentOp != NULL)
    {
        return MF_E_NOTACCEPTING;
    }
    return S_OK;
}
```



DispatchOperation 方法會在作業類型上切換：


```C++
//-------------------------------------------------------------------
// DispatchOperation
//
// Performs the asynchronous operation indicated by pOp.
//
// NOTE:
// This method implements the pure-virtual OpQueue::DispatchOperation
// method. It is always called from a work-queue thread.
//-------------------------------------------------------------------

HRESULT MPEG1Source::DispatchOperation(SourceOp *pOp)
{
    EnterCriticalSection(&m_critSec);

    HRESULT hr = S_OK;

    if (m_state == STATE_SHUTDOWN)
    {
        LeaveCriticalSection(&m_critSec);

        return S_OK; // Already shut down, ignore the request.
    }

    switch (pOp->Op())
    {

    // IMFMediaSource methods:

    case SourceOp::OP_START:
        hr = DoStart((StartOp*)pOp);
        break;

    case SourceOp::OP_STOP:
        hr = DoStop(pOp);
        break;

    case SourceOp::OP_PAUSE:
        hr = DoPause(pOp);
        break;

    // Operations requested by the streams:

    case SourceOp::OP_REQUEST_DATA:
        hr = OnStreamRequestSample(pOp);
        break;

    case SourceOp::OP_END_OF_STREAM:
        hr = OnEndOfStream(pOp);
        break;

    default:
        hr = E_UNEXPECTED;
    }

    if (FAILED(hr))
    {
        StreamingError(hr);
    }

    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



總括來說：

1.  管線會呼叫非同步方法，例如 [**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)。
2.  非同步方法會呼叫 `OpQueue::QueueOperation` ，將指標傳入 `SourceOp` 物件。
3.  方法會將作業 `QueueOperation` 放在 *m \_ OpQueue* 佇列上，並呼叫 `OpQueue::ProcessQueue` 。
4.  `ProcessQueue`方法會呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem)。 從此時開始，所有專案都會在媒體基礎的工作佇列執行緒上發生。 非同步方法會傳回給呼叫端。
5.  工作佇列執行緒會呼叫 `OpQueue::ProcessQueueAsync` 方法。
6.  `ProcessQueueAsync`方法會呼叫 `MPEG1Source:ValidateOperation` 以驗證作業。
7.  `ProcessQueueAsync`方法會呼叫 `MPEG1Source::DispatchOperation` 以處理作業。

此設計有幾個優點：

-   方法是非同步，因此不會封鎖呼叫應用程式的執行緒。
-   作業會分派在媒體基礎的工作佇列執行緒上，其會在管線元件之間共用。 因此，媒體來源不會建立自己的執行緒，而會減少所建立的執行緒總數。
-   等候作業完成時，媒體來源不會封鎖。 這樣可減少媒體來源意外造成鎖死的機率，並有助於減少內容切換。
-   媒體來源可以使用非同步 i/o，藉由呼叫 [**IMFByteStream：： BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)) 來讀取原始程式檔 (。 在等候 i/o 常式完成時，不需要封鎖媒體來源。

如果您遵循 SDK 範例所示的模式，您可以將焦點放在媒體來源的特定詳細資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體來源](media-sources.md)
</dt> <dt>

[撰寫自訂媒體來源](writing-a-custom-media-source.md)
</dt> </dl>

 

 



