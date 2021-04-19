---
description: 本主題說明如何使用 Sequencer 來源。
ms.assetid: 7ce8dc67-02b1-4fd4-9e4d-6614fdb40620
title: 使用 Sequencer 來源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba99202838fbdc8be86f2f1d8931e5aa99ae9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977802"
---
# <a name="using-the-sequencer-source"></a>使用 Sequencer 來源

本主題說明如何使用 [Sequencer 來源](sequencer-source.md)。 它包含下列區段：

-   [概觀](#overview)
-   [新增拓撲](#adding-topologies)
-   [刪除拓撲](#deleting-topologies)
-   [跳到區段](#skipping-to-a-segment)
-   [相關主題](#related-topics)

如需 sequencer 來源的一般總覽，請參閱 [關於 Sequencer 來源](about-the-sequencer-source.md)。

## <a name="overview"></a>概觀

Sequencer 來源會公開下列介面。



| 介面                                                                        | 描述                                                                        |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                         | 公開一般媒體來源功能。                                        |
| [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)                                 | 可讓應用程式新增或移除拓撲。                               |
| [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)         | 在媒體會話上抓取下一個要排入佇列的拓撲。                         |
| [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider) | 媒體會話用來結束區段。 應用程式不會使用此介面。 |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                           | 查詢 [服務介面](service-interfaces.md)的 sequencer 來源。     |



 

若要播放媒體來源序列，請執行下列步驟：

1.  若要建立 sequencer 來源，請呼叫 [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) 函數。
2.  針對每個區段建立播放拓撲，如 [建立播放拓撲](creating-playback-topologies.md)中所述。 若要將拓撲新增至展示檔，請呼叫 [**IMFSequencerSource：： AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology)。
3.  開始播放之前，請在 sequencer 來源上呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) 。 這個方法會傳回第一個區段的表示描述項指標。 若要取得與此區段相關聯的拓撲，請針對 [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)介面呼叫 sequencer 來源上的 **QueryInterface** 。 將表示描述項傳遞給 [**IMFMediaSourceTopologyProvider：： GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) 方法。 這個方法會傳回拓撲的指標。
4.  藉由呼叫媒體會話的 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) 方法，將第一個區段的拓撲傳遞給媒體會話。
5.  藉由呼叫 [**IMFMediaSession：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)來開始播放。
6.  當 sequencer 來源準備好可預先產生下一個區段時，它會傳送 [MENewPresentation](menewpresentation.md) 事件，其事件資料是 [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) 介面指標。 同樣地，在 sequencer 來源上呼叫 [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) 來取得區段的拓撲，然後藉由呼叫 [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)，在媒體會話上設定拓撲。 不需要重新開機媒體來源;它會自動播放到下一個區段。
7.  在應用程式結束之前，藉由呼叫 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)關閉 sequencer 來源。

下列程式碼示範如何取得拓撲，並在媒體會話上設定它：


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



如需完整的程式碼範例，請參閱 [Sequencer 來源範例程式碼](sequencer-source-example-code.md)。

## <a name="adding-topologies"></a>新增拓撲

Sequencer 來源會維護兩個拓撲清單： *輸入清單* 和預先執行 *清單*。

輸入清單是對應至播放清單區段的拓撲集合，其順序是由應用程式透過呼叫 [**IMFSequencerSource：： AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology)來新增。 這個方法會將 **MFSequencerElementId** 型別的唯一 *區段識別碼* 指派給每個拓撲。 區段識別碼會設定為所有來源拓撲節點的屬性。 應用程式可以使用 [MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID](mf-toponode-sequence-elementid-attribute.md) 屬性，從來源節點取得區段識別碼。 如果應用程式在相同拓撲上呼叫 **AppendTopology** 超過一次，則輸入清單可以有重複的拓撲;不過，它們是由其唯一區段識別碼來識別。

預先集清單是輸入清單拓撲的集合，已初始化以準備播放。 這可讓媒體會話在使用中拓撲結束時，順暢地轉換到下一個拓撲。 應用程式無法直接在預先載入清單中新增或移除拓撲;當選取輸入清單中的拓撲以進行播放時，它是由 sequencer 來源所產生。 這會導致 sequencer 來源將下一個拓撲從輸入清單新增到預先產生的清單。 在這麼做之後，sequencer 來源會以非同步方式引發 [MENewPresentation](menewpresentation.md) 事件，並將預先產生拓撲的呈現描述項傳遞為事件資料。 應用程式必須使用媒體會話的 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面來接聽此事件，並藉由呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)，將媒體會話上的預先執行拓撲排入佇列。 這必須在媒體會話完成作用中拓撲的播放之前完成。 **SetTopology** 會通知媒體會話關於下一個拓撲的播放，在作用中拓朴播放之後必須播放該拓撲。 為了確保無縫 treansition，應用程式必須在媒體會話完成播放先前的拓撲之前呼叫 **SetTopology** 。 否則區段之間會有間距。

只要作用中拓撲之後有拓撲，就會引發 [MENewPresentation](menewpresentation.md) 事件。 因此，如果輸入清單只包含一個拓撲，或是使用中拓撲是輸入清單中的最後一個拓撲，就不會引發此事件。

預先處理清單會與輸入清單同步處理，並在每次在輸入清單中新增或刪除拓撲時重新整理。

## <a name="deleting-topologies"></a>刪除拓撲

若要從 sequencer 來源移除拓撲，應用程式必須呼叫 [**IMFSequencerSource：:D eletetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) 方法，並指定區段識別碼。

在呼叫 [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology)之前，應用程式必須確定媒體會話未使用應用程式要刪除的拓撲。 若要這樣做，應用程式呼叫 **DeleteTopology** 之前，必須執行下列兩項作業：

-   [](mesessiontopologystatus.md)已 \_ 針對拓撲收到 MESessionTopologyStatus 的 TOPOSTATUS 事件， \_ 以確保媒體會話已完成播放。

-   [](mesessiontopologystatus.md) \_ \_ \_ 針對下一個拓撲，會收到 MESessionTopologyStatus with MF TOPOSTATUS 已啟動來源，以確保媒體會話已開始播放下一個拓撲，並收到[MESessionEnded](mesessionended.md)事件，以確保媒體會話是使用 sequencer 來源中的最後一個拓撲進行。

如果要刪除的區段是使用中的拓撲，播放會停止，且 sequencer 來源會引發 [MEEndOfPresentationSegment](meendofpresentationsegment.md) 事件。 如果作用中拓撲也是最後一個拓撲，則會引發 [MEEndOfPresentation](meendofpresentation.md) 事件。

## <a name="skipping-to-a-segment"></a>跳到區段

應用程式可以使用區段位移來啟動 [媒體會話](media-session.md) ，以跳到序列中的特定區段，如下所示：

1.  呼叫 [**MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) 函數，以建立區段位移。 在 *dwId* 參數中指定區段的識別碼。  (當您第一次將拓撲加入至 sequencer 來源時， [**IMFSequencerSource：： AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) 方法所傳回的識別碼。 ) *hnsOffset* 參數會指定相對於區段開頭的時間位移。 現在將會開始播放。 針對 *pvarSegmentOffset* 參數，傳入空白 **PROPVARIANT** 的位址。 當函數傳回時，此 **PROPVARIANT** 會包含區段位移。

2.  呼叫媒體會話上的 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) 方法。 針對 *pguidTimeFormat* 參數，請使用 GUID 值 MF \_ 時間 \_ 格式 \_ 區段 \_ 位移。 這個值表示依區段位移搜尋。 針對 *pvarStartPosition* 參數，傳遞在上一個步驟中建立之 **PROPVARIANT** 的位址。

下列程式碼範例示範如何跳到序列中指定區段的開頭。


```C++
// Skips to the specified segment in the sequencer source

HRESULT CPlaylist::SkipTo(DWORD index)
{
    if (index >= m_count)
    {
        return E_INVALIDARG;
    }

    MFSequencerElementId ID = m_segments[index].SegmentID;

    PROPVARIANT var;

    HRESULT hr = MFCreateSequencerSegmentOffset(ID, NULL, &var);
    
    if (SUCCEEDED(hr))
    {
        hr = m_pSession->Start(&MF_TIME_FORMAT_SEGMENT_OFFSET, &var);
        PropVariantClear(&var);
    }
    return hr;
}
```



當應用程式跨區段搜尋時，應用程式會收到數個事件，因為 sequencer 來源會結束目前的區段，並準備好播放新的區段。 因為這些事件是以非同步方式接收，所以很難預測確切的事件順序。 這些事件如下所示：

-   Sequencer 來源會針對即將略過媒體會話的新區段傳送 [MENewPresentation](menewpresentation.md) 事件。

-   當 sequencer 來源結束使用中區段時，它會傳送 [MEEndOfPresentationSegment](meendofpresentationsegment.md) 事件。
-   Sequencer 來源接著會取消預先進行的拓撲。 這會產生已取消拓撲的下列事件：

    -   [](mesessiontopologystatus.md)具有 MF \_ TOPOSTATUS READY 旗標的 MESessionTopologyStatus 事件 \_ 。
    -   [](mesessiontopologystatus.md)具有 MF \_ TOPOSTATUS \_ 啟動 \_ 來源旗標的 MESessionTopologyStatus 事件。
    -   具有 [ [MF \_ 事件 \_ 來源 \_ 拓撲 \_ 已取消](mf-event-source-topology-canceled-attribute.md)] 屬性的[MEEndOfPresentationSegment](meendofpresentationsegment.md)事件，表示拓撲已由 sequencer 來源取消。

-   接著，sequencer 來源會傳送新區段的事件，包括各種 [MESessionTopologyStatus](mesessiontopologystatus.md) 事件。
-   如果新區段不是清單中的最後一個區段，sequencer 來源就會重新整理預先產生的清單，並針對新的預先產生拓撲引發另一個 [MENewPresentation](menewpresentation.md) 。 如需有關預先排程清單中拓撲的詳細資訊，請參閱 [關於 Sequencer 來源](about-the-sequencer-source.md)。

有關 sequencer 來源所傳送之事件的更多詳細資料，可在「 [Sequencer 來源事件](sequencer-source-events.md)」主題中找到。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何建立播放清單](how-to-create-a-playlist.md)
</dt> <dt>

[Sequencer 來源](sequencer-source.md)
</dt> </dl>

 

 



