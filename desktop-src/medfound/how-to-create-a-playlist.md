---
description: 本主題說明如何使用順序來源來播放一連串的檔案。
ms.assetid: 5a760492-bd52-40b8-a652-8a62646db6ae
title: 如何建立播放清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2e6e19766c3fa569a701fea9bed0f05d11a4324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512453"
---
# <a name="how-to-create-a-playlist"></a>如何建立播放清單

本主題說明如何使用順序來源來播放一連串的檔案。

## <a name="overview"></a>概觀

若要在序列中播放媒體檔案，應用程式必須以順序新增拓撲以建立播放清單，並在媒體會話上將這些拓撲排入佇列以供播放。

Sequencer 來源會在媒體會話開始播放目前的拓撲之前，初始化和載入下一個拓撲，以確保無縫播放。 這可讓應用程式在需要時快速啟動下一個拓撲。

媒體會話負責將資料摘要至接收，並在順序來源中播放拓撲。 此外，媒體會話也會管理區段的呈現時間。

如需有關 sequencer 來源如何管理拓撲的詳細資訊，請參閱 [關於 Sequencer 來源](about-the-sequencer-source.md)。

本逐步解說包含下列步驟：

1.  [先決條件](#prerequisites)
2.  [正在初始化媒體基礎](#initializing-media-foundation)
3.  [建立媒體基礎物件](#creating-media-foundation-objects)
4.  [建立媒體來源](#creating-the-media-source)
5.  [建立部分拓撲](#creating-partial-topologies)
6.  [將拓撲新增至 Sequencer 來源](#adding-topologies-to-the-sequencer-source)
7.  [設定媒體會話的第一個拓撲](#setting-the-first-topology-on-the-media-session)
8.  [排入媒體會話下一個拓撲的佇列](#queuing-the-next-topology-on-the-media-session)
9.  [釋放 Sequencer 來源](#releasing-the-sequencer-source)

本主題所顯示的程式碼範例是主題 [Sequencer 來源範例程式碼](sequencer-source-example-code.md)中的摘錄，其中包含完整的範例程式碼。

## <a name="prerequisites"></a>必要條件

開始本逐步解說之前，請先熟悉下列媒體基礎概念：

-   [媒體會話](media-session.md)
-   [拓撲](topologies.md)
-   [媒體事件產生器](media-event-generators.md)
-   [簡報描述項](presentation-descriptors.md)

此外，請參閱 [如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案，因為這裡的範例程式碼 shwon 展開該主題中的程式碼。

## <a name="initializing-media-foundation"></a>正在初始化媒體基礎

在您可以使用任何媒體基礎介面或方法之前，請先呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 函式來初始化媒體基礎。 如需詳細資訊，請參閱 [初始化媒體基礎](initializing-media-foundation.md)。


```C++
    hr = MFStartup(MF_VERSION);
```



## <a name="creating-media-foundation-objects"></a>建立媒體基礎物件

接下來，建立下列媒體基礎物件：

-   媒體會話。 此物件會公開 [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) 介面，此介面會提供用來播放、暫停和停止目前拓撲的方法。
-   Sequencer 來源。 此物件會公開 [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) 介面，以提供在序列中新增、更新和刪除拓撲的方法。

1.  呼叫 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) 函數來建立媒體會話。
2.  呼叫 [**IMFMediaEventQueue：： BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) ，以要求媒體會話中的第一個事件。
3.  呼叫 [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) 函數，以建立 sequencer 來源。

下列程式碼會建立媒體會話，並要求第一個事件：


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



## <a name="creating-the-media-source"></a>建立媒體來源

接下來，為第一個播放清單區段建立媒體來源。 使用 [來源解析程式](source-resolver.md) ，從 URL 建立媒體來源。 若要這樣做，請呼叫 [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) 函數來建立來源解析程式，然後呼叫 [**IMFSourceResolver：： CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) 方法來建立媒體來源。

如需媒體來源的詳細資訊，請參閱 [媒體來源](media-sources.md)。

## <a name="creating-partial-topologies"></a>建立部分拓撲

Sequencer 來源中的每個區段都有自己的部分拓撲。 接下來，建立媒體來源的部分拓撲。 若為部分拓撲，拓撲來源節點會直接連接至輸出節點，而不會指定任何中繼轉換。 媒體會話會使用拓撲載入器物件來解析拓撲。 解析拓撲之後，會新增必要的解碼器和其他轉換節點。 Sequencer 來源也可以包含完整的拓撲。

若要建立拓撲物件，請使用 [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) 函數，然後使用 [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) 介面來建立資料流程節點。

如需使用這些程式設計項目建立拓撲的完整指示，請參閱 [建立播放拓撲](creating-playback-topologies.md)。

應用程式可以藉由設定來源節點來播放原生來源的選定部分。 若要這樣做，請在 [ **mf \_ 拓撲 \_ SOURCESTREAM \_ 節點** 拓撲] 節點上設定 [ [**mf \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md) ] 屬性和 [ [**mf \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md) ] 屬性。 指定媒體開始時間和媒體停止時間（相對於原生來源作為 **UINT64** 類型的起點）。

## <a name="adding-topologies-to-the-sequencer-source"></a>將拓撲新增至 Sequencer 來源

接下來，將您建立的部分拓撲新增至 sequencer 來源。 每個 sequence 元素（稱為 *區段*）都會被指派一個 **MFSequencerElementId** 識別碼。 如需有關 sequencer 來源如何管理拓撲的詳細資訊，請參閱 [關於 Sequencer 來源](about-the-sequencer-source.md)。

將所有拓撲新增至 sequencer 來源之後，應用程式必須將序列中的最後一個區段標記為管線中的結束播放。 如果沒有這個旗標，sequencer 來源預期會加入更多拓撲。

1.  呼叫 [**IMFSequencerSource：： AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) 方法，將特定拓撲新增至 sequencer 來源。

    ```C++
        hr = m_pSequencerSource->AppendTopology(
            pTopology, 
            SequencerTopologyFlags_Last, 
            &SegmentId
            );
    ```

    

    [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) 會將指定的拓撲新增至順序。 這個方法會傳回 *pdwId* 參數中的區段識別碼。

    如果拓撲是 sequencer 來源中的最後一個拓撲，請 \_ 在 *dwFlags* 參數中最後傳遞 SequencerTopologyFlags。 此值定義于 [**MFSequencerTopologyFlags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) 列舉中。

2.  呼叫 [**IMFSequencerSource：： UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) ，以更新與輸入清單中區段識別碼相關聯之拓撲的旗標。 在此情況下，呼叫會指出指定的區段是 sequencer 中的最後一個區段。  (在 [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) 呼叫中指定最後一個拓撲時，此呼叫是選擇性的。 ) 

    ```C++
        BOOL bFirstSegment = (NumSegments() == 0);

        if (!bFirstSegment)
        {
            // Remove the "last segment" flag from the last segment.
            hr = m_pSequencerSource->UpdateTopologyFlags(LastSegment(), 0);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    ```

    

應用程式可以藉由呼叫 [**IMFSequencerSource：： UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) 並在 *pTopology* 中傳遞新的拓撲，來將區段的拓撲取代為另一個拓撲。 如果新拓撲中有新的原生來源，則會將來源新增至來源快取。 預先整理清單也會重新整理。

## <a name="setting-the-first-topology-on-the-media-session"></a>設定媒體會話的第一個拓撲

接下來，將媒體會話上順序來源中的第一個拓撲排入佇列。 若要從 sequencer 來源取得第一個拓撲，應用程式必須呼叫 [**IMFMediaSourceTopologyProvider：： GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) 方法。 這個方法會傳回由媒體會話解析的部分拓撲。

如需部分拓撲的詳細資訊，請參閱 [關於拓撲](about-topologies.md)。

1.  針對序列來源的第一個拓撲取得原生媒體來源。
2.  藉由呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) 方法，建立媒體來源的簡報描述項。
3.  藉由呼叫 [**IMFMediaSourceTopologyProvider：： GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) 方法，取得簡報的關聯拓撲。
4.  藉由呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)，在媒體會話上設定第一個拓撲。

    呼叫 [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) ，並將 *dwSetTopologyFlags* 參數設定為 **Null**。 這會指示媒體會話在目前的拓撲完成時啟動指定的拓撲。 因為在此情況下，指定的拓撲是第一個拓撲，而且沒有目前的簡報，所以媒體會話會立即啟動新的簡報。

    **Null** 值也表示媒體會話必須解析拓撲，因為拓撲提供者所傳回的拓撲一律為部分拓撲。


```C++
// Queues the next topology on the session.

HRESULT CPlaylist::QueueNextSegment(IMFPresentationDescriptor *pPD)
{
    IMFMediaSourceTopologyProvider *pTopoProvider = NULL;
    IMFTopology *pTopology = NULL;

    //Get the topology for the presentation descriptor
    HRESULT hr = m_pSequencerSource->QueryInterface(IID_PPV_ARGS(&pTopoProvider));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pTopoProvider->GetMediaSourceTopology(pPD, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the topology on the media session
    m_pSession->SetTopology(NULL, pTopology);

done:
    SafeRelease(&pTopoProvider);
    SafeRelease(&pTopology);
    return hr;
}
```



## <a name="queuing-the-next-topology-on-the-media-session"></a>排入媒體會話下一個拓撲的佇列

接下來，應用程式需要處理 [MENewPresentation](menewpresentation.md) 事件。

當媒體會話開始播放有另一個區段之後的區段時，Sequencer 來源會引發 [MENewPresentation](menewpresentation.md) 。 此事件會提供預先集中清單中下一個區段的表示描述項，以通知應用程式有關序列來源中的下一個拓撲。 應用程式必須抓取相關聯的拓撲，方法是使用拓撲提供者，並在媒體會話上將它排入佇列。 Sequencer 來源接著會 prerolls 此拓撲，以確保在簡報之間進行順暢的轉換。

當應用程式跨區段搜尋時，應用程式會收到數個 [MENewPresentation](menewpresentation.md) 事件，因為 sequencer 來源會重新整理預先處理的清單，並設定正確的拓撲。 應用程式必須處理每個事件，並將事件資料中傳回的拓撲排入媒體會話的佇列。 如需跳過區段的詳細資訊，請參閱 [使用 Sequencer 來源](using-the-sequencer-source.md)。

如需取得 sequencer 來源通知的詳細資訊，請參閱 [Sequencer 來源事件](sequencer-source-events.md)。

1.  在 [MENewPresentation](menewpresentation.md) 事件處理常式中，從事件資料中取出下一個區段的呈現描述項。
2.  藉由呼叫 [**IMFMediaSourceTopologyProvider：： GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) 方法，取得簡報的關聯拓撲。
3.  藉由呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) 方法，在媒體會話上設定拓撲。

    當目前的簡報完成時，媒體會話就會啟動新的簡報。


```C++
HRESULT CPlaylist::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = GetEventObject(pEvent, &pPD);

    if (SUCCEEDED(hr))
    {
        // Queue the next segment on the media session
        hr = QueueNextSegment(pPD);
    }

    SafeRelease(&pPD);
    return hr;
}
```



## <a name="releasing-the-sequencer-source"></a>釋放 Sequencer 來源

最後，關閉 sequencer 來源。 若要這樣做，請在 sequencer 來源上呼叫 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) 方法。 此呼叫會關閉 sequencer 來源中的所有基礎原生媒體來源。

釋放 sequencer 來源之後，應用程式應該依序呼叫 [**IMFMediaSession：： close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) 和 [**IMFMediaSession：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)，關閉並關閉媒體會話。

若要避免記憶體流失，當不再需要應用程式時，應用程式必須釋放指向媒體基礎介面的指標。

## <a name="next-steps"></a>後續步驟

本逐步解說說明如何使用 sequencer 來源建立基本播放清單。 建立播放清單之後，您可能會想要新增先進的功能，例如區段略過、變更播放狀態，以及在區段內搜尋。 下列清單提供相關主題的連結：

-   [如何控制呈現狀態](how-to-control-presentation-states.md)： sequencer 來源依賴媒體會話來提供傳輸控制項，例如、播放、暫停和停止。
-   [如何執行](how-to-perform-scrubbing.md) 清除說明在資料流程中搜尋特定位置所需的步驟。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Sequencer 來源](sequencer-source.md)
</dt> </dl>

 

 



