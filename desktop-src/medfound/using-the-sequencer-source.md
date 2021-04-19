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
# <a name="using-the-sequencer-source"></a><span data-ttu-id="6e44d-103">使用 Sequencer 來源</span><span class="sxs-lookup"><span data-stu-id="6e44d-103">Using the Sequencer Source</span></span>

<span data-ttu-id="6e44d-104">本主題說明如何使用 [Sequencer 來源](sequencer-source.md)。</span><span class="sxs-lookup"><span data-stu-id="6e44d-104">This topic describes how to use the [Sequencer Source](sequencer-source.md).</span></span> <span data-ttu-id="6e44d-105">它包含下列區段：</span><span class="sxs-lookup"><span data-stu-id="6e44d-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="6e44d-106">概觀</span><span class="sxs-lookup"><span data-stu-id="6e44d-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="6e44d-107">新增拓撲</span><span class="sxs-lookup"><span data-stu-id="6e44d-107">Adding Topologies</span></span>](#adding-topologies)
-   [<span data-ttu-id="6e44d-108">刪除拓撲</span><span class="sxs-lookup"><span data-stu-id="6e44d-108">Deleting Topologies</span></span>](#deleting-topologies)
-   [<span data-ttu-id="6e44d-109">跳到區段</span><span class="sxs-lookup"><span data-stu-id="6e44d-109">Skipping to a Segment</span></span>](#skipping-to-a-segment)
-   [<span data-ttu-id="6e44d-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e44d-110">Related topics</span></span>](#related-topics)

<span data-ttu-id="6e44d-111">如需 sequencer 來源的一般總覽，請參閱 [關於 Sequencer 來源](about-the-sequencer-source.md)。</span><span class="sxs-lookup"><span data-stu-id="6e44d-111">For a general overview of the sequencer source, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

## <a name="overview"></a><span data-ttu-id="6e44d-112">概觀</span><span class="sxs-lookup"><span data-stu-id="6e44d-112">Overview</span></span>

<span data-ttu-id="6e44d-113">Sequencer 來源會公開下列介面。</span><span class="sxs-lookup"><span data-stu-id="6e44d-113">The sequencer source exposes the following interfaces.</span></span>



| <span data-ttu-id="6e44d-114">介面</span><span class="sxs-lookup"><span data-stu-id="6e44d-114">Interface</span></span>                                                                        | <span data-ttu-id="6e44d-115">描述</span><span class="sxs-lookup"><span data-stu-id="6e44d-115">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e44d-116">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="6e44d-116">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                         | <span data-ttu-id="6e44d-117">公開一般媒體來源功能。</span><span class="sxs-lookup"><span data-stu-id="6e44d-117">Exposes generic media source functionality.</span></span>                                        |
| [<span data-ttu-id="6e44d-118">**IMFSequencerSource**</span><span class="sxs-lookup"><span data-stu-id="6e44d-118">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)                                 | <span data-ttu-id="6e44d-119">可讓應用程式新增或移除拓撲。</span><span class="sxs-lookup"><span data-stu-id="6e44d-119">Enables the application to add or remove topologies.</span></span>                               |
| [<span data-ttu-id="6e44d-120">**IMFMediaSourceTopologyProvider**</span><span class="sxs-lookup"><span data-stu-id="6e44d-120">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)         | <span data-ttu-id="6e44d-121">在媒體會話上抓取下一個要排入佇列的拓撲。</span><span class="sxs-lookup"><span data-stu-id="6e44d-121">Retrieves the next topology to queue on the Media Session.</span></span>                         |
| [<span data-ttu-id="6e44d-122">**IMFMediaSourcePresentationProvider**</span><span class="sxs-lookup"><span data-stu-id="6e44d-122">**IMFMediaSourcePresentationProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider) | <span data-ttu-id="6e44d-123">媒體會話用來結束區段。</span><span class="sxs-lookup"><span data-stu-id="6e44d-123">Used by the Media Session to end segments.</span></span> <span data-ttu-id="6e44d-124">應用程式不會使用此介面。</span><span class="sxs-lookup"><span data-stu-id="6e44d-124">Applications do not use this interface.</span></span> |
| [<span data-ttu-id="6e44d-125">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="6e44d-125">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                           | <span data-ttu-id="6e44d-126">查詢 [服務介面](service-interfaces.md)的 sequencer 來源。</span><span class="sxs-lookup"><span data-stu-id="6e44d-126">Queries the sequencer source for [Service Interfaces](service-interfaces.md).</span></span>     |



 

<span data-ttu-id="6e44d-127">若要播放媒體來源序列，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="6e44d-127">To play a sequence of media sources, perform the following steps:</span></span>

1.  <span data-ttu-id="6e44d-128">若要建立 sequencer 來源，請呼叫 [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) 函數。</span><span class="sxs-lookup"><span data-stu-id="6e44d-128">To create the sequencer source, call the [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) function.</span></span>
2.  <span data-ttu-id="6e44d-129">針對每個區段建立播放拓撲，如 [建立播放拓撲](creating-playback-topologies.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="6e44d-129">For each segment, create a playback topology, as described in [Creating Playback Topologies](creating-playback-topologies.md).</span></span> <span data-ttu-id="6e44d-130">若要將拓撲新增至展示檔，請呼叫 [**IMFSequencerSource：： AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology)。</span><span class="sxs-lookup"><span data-stu-id="6e44d-130">To add the topology to the presentation, call [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span></span>
3.  <span data-ttu-id="6e44d-131">開始播放之前，請在 sequencer 來源上呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) 。</span><span class="sxs-lookup"><span data-stu-id="6e44d-131">Before starting playback, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the sequencer source.</span></span> <span data-ttu-id="6e44d-132">這個方法會傳回第一個區段的表示描述項指標。</span><span class="sxs-lookup"><span data-stu-id="6e44d-132">This method returns a pointer to a presentation descriptor for the first segment.</span></span> <span data-ttu-id="6e44d-133">若要取得與此區段相關聯的拓撲，請針對 [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)介面呼叫 sequencer 來源上的 **QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="6e44d-133">To get the topology associated with this segment, call **QueryInterface** on the sequencer source for the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface.</span></span> <span data-ttu-id="6e44d-134">將表示描述項傳遞給 [**IMFMediaSourceTopologyProvider：： GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) 方法。</span><span class="sxs-lookup"><span data-stu-id="6e44d-134">Pass the presentation descriptor to the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span> <span data-ttu-id="6e44d-135">這個方法會傳回拓撲的指標。</span><span class="sxs-lookup"><span data-stu-id="6e44d-135">This method returns a pointer to the topology.</span></span>
4.  <span data-ttu-id="6e44d-136">藉由呼叫媒體會話的 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) 方法，將第一個區段的拓撲傳遞給媒體會話。</span><span class="sxs-lookup"><span data-stu-id="6e44d-136">Pass the topology for the first segment to the Media Session, by calling the Media Session's [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method.</span></span>
5.  <span data-ttu-id="6e44d-137">藉由呼叫 [**IMFMediaSession：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)來開始播放。</span><span class="sxs-lookup"><span data-stu-id="6e44d-137">Start playback by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>
6.  <span data-ttu-id="6e44d-138">當 sequencer 來源準備好可預先產生下一個區段時，它會傳送 [MENewPresentation](menewpresentation.md) 事件，其事件資料是 [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="6e44d-138">When the sequencer source is ready to preroll the next segment, it sends an [MENewPresentation](menewpresentation.md) event whose event data is an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface pointer.</span></span> <span data-ttu-id="6e44d-139">同樣地，在 sequencer 來源上呼叫 [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) 來取得區段的拓撲，然後藉由呼叫 [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)，在媒體會話上設定拓撲。</span><span class="sxs-lookup"><span data-stu-id="6e44d-139">Again, get the topology for the segment by calling [**GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) on the sequencer source, and set the topology on the Media Session by calling [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="6e44d-140">不需要重新開機媒體來源;它會自動播放到下一個區段。</span><span class="sxs-lookup"><span data-stu-id="6e44d-140">It is not necessary to re-start the media source; it will automatically play through to the next segment.</span></span>
7.  <span data-ttu-id="6e44d-141">在應用程式結束之前，藉由呼叫 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)關閉 sequencer 來源。</span><span class="sxs-lookup"><span data-stu-id="6e44d-141">Before the application quits, shut down the sequencer source by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>

<span data-ttu-id="6e44d-142">下列程式碼示範如何取得拓撲，並在媒體會話上設定它：</span><span class="sxs-lookup"><span data-stu-id="6e44d-142">The following code shows how to get the topology and set it on the Media Session:</span></span>


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



<span data-ttu-id="6e44d-143">如需完整的程式碼範例，請參閱 [Sequencer 來源範例程式碼](sequencer-source-example-code.md)。</span><span class="sxs-lookup"><span data-stu-id="6e44d-143">For a complete code example, see [Sequencer Source Example Code](sequencer-source-example-code.md).</span></span>

## <a name="adding-topologies"></a><span data-ttu-id="6e44d-144">新增拓撲</span><span class="sxs-lookup"><span data-stu-id="6e44d-144">Adding Topologies</span></span>

<span data-ttu-id="6e44d-145">Sequencer 來源會維護兩個拓撲清單： *輸入清單* 和預先執行 *清單*。</span><span class="sxs-lookup"><span data-stu-id="6e44d-145">The sequencer source maintains two lists of topologies: the *input list* and the *preroll list*.</span></span>

<span data-ttu-id="6e44d-146">輸入清單是對應至播放清單區段的拓撲集合，其順序是由應用程式透過呼叫 [**IMFSequencerSource：： AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology)來新增。</span><span class="sxs-lookup"><span data-stu-id="6e44d-146">The input list is a collection of topologies corresponding to playlist segments, in the order that they were added by the application by calling [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology).</span></span> <span data-ttu-id="6e44d-147">這個方法會將 **MFSequencerElementId** 型別的唯一 *區段識別碼* 指派給每個拓撲。</span><span class="sxs-lookup"><span data-stu-id="6e44d-147">This method assigns each topology a unique *segment identifier* of the type **MFSequencerElementId**.</span></span> <span data-ttu-id="6e44d-148">區段識別碼會設定為所有來源拓撲節點的屬性。</span><span class="sxs-lookup"><span data-stu-id="6e44d-148">The segment identifier is set as an attribute for all source topology nodes.</span></span> <span data-ttu-id="6e44d-149">應用程式可以使用 [MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID](mf-toponode-sequence-elementid-attribute.md) 屬性，從來源節點取得區段識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e44d-149">An application can get the segment identifier from a source node by using the [MF\_TOPONODE\_SEQUENCE\_ELEMENTID](mf-toponode-sequence-elementid-attribute.md) attribute.</span></span> <span data-ttu-id="6e44d-150">如果應用程式在相同拓撲上呼叫 **AppendTopology** 超過一次，則輸入清單可以有重複的拓撲;不過，它們是由其唯一區段識別碼來識別。</span><span class="sxs-lookup"><span data-stu-id="6e44d-150">The input list can have duplicate topologies if the application called **AppendTopology** on the same topology more than once; however, they are identified by their unique segment identifiers.</span></span>

<span data-ttu-id="6e44d-151">預先集清單是輸入清單拓撲的集合，已初始化以準備播放。</span><span class="sxs-lookup"><span data-stu-id="6e44d-151">The preroll list is a collection of input list topologies that have been initialized in preparation for playback.</span></span> <span data-ttu-id="6e44d-152">這可讓媒體會話在使用中拓撲結束時，順暢地轉換到下一個拓撲。</span><span class="sxs-lookup"><span data-stu-id="6e44d-152">This enables the Media Session to transition to the next topology seamlessly when the active topology ends.</span></span> <span data-ttu-id="6e44d-153">應用程式無法直接在預先載入清單中新增或移除拓撲;當選取輸入清單中的拓撲以進行播放時，它是由 sequencer 來源所產生。</span><span class="sxs-lookup"><span data-stu-id="6e44d-153">The application cannot directly add or remove topologies from the preroll list; it is generated by the sequencer source when a topology from the input list is selected for playback.</span></span> <span data-ttu-id="6e44d-154">這會導致 sequencer 來源將下一個拓撲從輸入清單新增到預先產生的清單。</span><span class="sxs-lookup"><span data-stu-id="6e44d-154">This causes the sequencer source to add the next topology from the input list to the preroll list.</span></span> <span data-ttu-id="6e44d-155">在這麼做之後，sequencer 來源會以非同步方式引發 [MENewPresentation](menewpresentation.md) 事件，並將預先產生拓撲的呈現描述項傳遞為事件資料。</span><span class="sxs-lookup"><span data-stu-id="6e44d-155">After doing so, the sequencer source asynchronously raises the [MENewPresentation](menewpresentation.md) event and passes the presentation descriptor for the preroll topology as event data.</span></span> <span data-ttu-id="6e44d-156">應用程式必須使用媒體會話的 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) 介面來接聽此事件，並藉由呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)，將媒體會話上的預先執行拓撲排入佇列。</span><span class="sxs-lookup"><span data-stu-id="6e44d-156">The application must listen for this event by using the Media Session's [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface and queue the preroll topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="6e44d-157">這必須在媒體會話完成作用中拓撲的播放之前完成。</span><span class="sxs-lookup"><span data-stu-id="6e44d-157">This must be done before the Media Session completes playback of the active topology.</span></span> <span data-ttu-id="6e44d-158">**SetTopology** 會通知媒體會話關於下一個拓撲的播放，在作用中拓朴播放之後必須播放該拓撲。</span><span class="sxs-lookup"><span data-stu-id="6e44d-158">**SetTopology** informs the Media Session about the next topology that it must play after playback of the active topology has ended.</span></span> <span data-ttu-id="6e44d-159">為了確保無縫 treansition，應用程式必須在媒體會話完成播放先前的拓撲之前呼叫 **SetTopology** 。</span><span class="sxs-lookup"><span data-stu-id="6e44d-159">To ensure a seamless treansition, the application must call **SetTopology** before the Media Session completes playing the previous topology.</span></span> <span data-ttu-id="6e44d-160">否則區段之間會有間距。</span><span class="sxs-lookup"><span data-stu-id="6e44d-160">Otherwise, there will be a gap between the segments.</span></span>

<span data-ttu-id="6e44d-161">只要作用中拓撲之後有拓撲，就會引發 [MENewPresentation](menewpresentation.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="6e44d-161">The [MENewPresentation](menewpresentation.md) event is raised as long as there is a topology following the active topology.</span></span> <span data-ttu-id="6e44d-162">因此，如果輸入清單只包含一個拓撲，或是使用中拓撲是輸入清單中的最後一個拓撲，就不會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="6e44d-162">Consequently, if the input list contains only one topology, or if the active topology is the last one in the input list, this event is not raised.</span></span>

<span data-ttu-id="6e44d-163">預先處理清單會與輸入清單同步處理，並在每次在輸入清單中新增或刪除拓撲時重新整理。</span><span class="sxs-lookup"><span data-stu-id="6e44d-163">The preroll list is synchronized with the input list and is refreshed each time a topology is added to or deleted from the input list.</span></span>

## <a name="deleting-topologies"></a><span data-ttu-id="6e44d-164">刪除拓撲</span><span class="sxs-lookup"><span data-stu-id="6e44d-164">Deleting Topologies</span></span>

<span data-ttu-id="6e44d-165">若要從 sequencer 來源移除拓撲，應用程式必須呼叫 [**IMFSequencerSource：:D eletetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) 方法，並指定區段識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e44d-165">To remove a topology from the sequencer source, an application must call the [**IMFSequencerSource::DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology) method and specify the segment identifier.</span></span>

<span data-ttu-id="6e44d-166">在呼叫 [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology)之前，應用程式必須確定媒體會話未使用應用程式要刪除的拓撲。</span><span class="sxs-lookup"><span data-stu-id="6e44d-166">Before calling [**DeleteTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-deletetopology), the application must make sure that Media Session is not using the topology that the application wants to delete.</span></span> <span data-ttu-id="6e44d-167">若要這樣做，應用程式呼叫 **DeleteTopology** 之前，必須執行下列兩項作業：</span><span class="sxs-lookup"><span data-stu-id="6e44d-167">To do this, both of the following must occur before the application calls **DeleteTopology**:</span></span>

-   <span data-ttu-id="6e44d-168">[](mesessiontopologystatus.md)已 \_ 針對拓撲收到 MESessionTopologyStatus 的 TOPOSTATUS 事件， \_ 以確保媒體會話已完成播放。</span><span class="sxs-lookup"><span data-stu-id="6e44d-168">[MESessionTopologyStatus](mesessiontopologystatus.md) event with MF\_TOPOSTATUS\_ENDED is received for the topology to ensure that Media Session has completed playback.</span></span>

-   <span data-ttu-id="6e44d-169">[](mesessiontopologystatus.md) \_ \_ \_ 針對下一個拓撲，會收到 MESessionTopologyStatus with MF TOPOSTATUS 已啟動來源，以確保媒體會話已開始播放下一個拓撲，並收到[MESessionEnded](mesessionended.md)事件，以確保媒體會話是使用 sequencer 來源中的最後一個拓撲進行。</span><span class="sxs-lookup"><span data-stu-id="6e44d-169">[MESessionTopologyStatus](mesessiontopologystatus.md) with MF\_TOPOSTATUS\_STARTED\_SOURCE is received for the next topology to ensure that the Media Session has started playing the next topology, [MESessionEnded](mesessionended.md) event is received to ensure that Media Session is done with the last topology in the sequencer source.</span></span>

<span data-ttu-id="6e44d-170">如果要刪除的區段是使用中的拓撲，播放會停止，且 sequencer 來源會引發 [MEEndOfPresentationSegment](meendofpresentationsegment.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="6e44d-170">If the segment being deleted is the active topology, playback is stopped and the sequencer source raises the [MEEndOfPresentationSegment](meendofpresentationsegment.md) event.</span></span> <span data-ttu-id="6e44d-171">如果作用中拓撲也是最後一個拓撲，則會引發 [MEEndOfPresentation](meendofpresentation.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="6e44d-171">If the active topology is also the last topology, the [MEEndOfPresentation](meendofpresentation.md) event is raised.</span></span>

## <a name="skipping-to-a-segment"></a><span data-ttu-id="6e44d-172">跳到區段</span><span class="sxs-lookup"><span data-stu-id="6e44d-172">Skipping to a Segment</span></span>

<span data-ttu-id="6e44d-173">應用程式可以使用區段位移來啟動 [媒體會話](media-session.md) ，以跳到序列中的特定區段，如下所示：</span><span class="sxs-lookup"><span data-stu-id="6e44d-173">An application can skip to a particular segment in the sequence by starting the [Media Session](media-session.md) with a segment offset, as follows:</span></span>

1.  <span data-ttu-id="6e44d-174">呼叫 [**MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) 函數，以建立區段位移。</span><span class="sxs-lookup"><span data-stu-id="6e44d-174">Call the [**MFCreateSequencerSegmentOffset**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersegmentoffset) function to create the segment offset.</span></span> <span data-ttu-id="6e44d-175">在 *dwId* 參數中指定區段的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6e44d-175">Specify the identifier of the segment in the *dwId* parameter.</span></span> <span data-ttu-id="6e44d-176"> (當您第一次將拓撲加入至 sequencer 來源時， [**IMFSequencerSource：： AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) 方法所傳回的識別碼。 ) *hnsOffset* 參數會指定相對於區段開頭的時間位移。</span><span class="sxs-lookup"><span data-stu-id="6e44d-176">(The identifier was returned by the [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) method when you first added the topology to the sequencer source.) The *hnsOffset* parameter specifies a time offset, relative to the start of the segment.</span></span> <span data-ttu-id="6e44d-177">現在將會開始播放。</span><span class="sxs-lookup"><span data-stu-id="6e44d-177">Playback will start at this time.</span></span> <span data-ttu-id="6e44d-178">針對 *pvarSegmentOffset* 參數，傳入空白 **PROPVARIANT** 的位址。</span><span class="sxs-lookup"><span data-stu-id="6e44d-178">For the *pvarSegmentOffset* parameter, pass in the address of an empty **PROPVARIANT**.</span></span> <span data-ttu-id="6e44d-179">當函數傳回時，此 **PROPVARIANT** 會包含區段位移。</span><span class="sxs-lookup"><span data-stu-id="6e44d-179">When the function returns, this **PROPVARIANT** contains the segment offset.</span></span>

2.  <span data-ttu-id="6e44d-180">呼叫媒體會話上的 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) 方法。</span><span class="sxs-lookup"><span data-stu-id="6e44d-180">Call the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method on the Media Session.</span></span> <span data-ttu-id="6e44d-181">針對 *pguidTimeFormat* 參數，請使用 GUID 值 MF \_ 時間 \_ 格式 \_ 區段 \_ 位移。</span><span class="sxs-lookup"><span data-stu-id="6e44d-181">For the *pguidTimeFormat* parameter, use the GUID value MF\_TIME\_FORMAT\_SEGMENT\_OFFSET.</span></span> <span data-ttu-id="6e44d-182">這個值表示依區段位移搜尋。</span><span class="sxs-lookup"><span data-stu-id="6e44d-182">This value indicates seeking by segment offset.</span></span> <span data-ttu-id="6e44d-183">針對 *pvarStartPosition* 參數，傳遞在上一個步驟中建立之 **PROPVARIANT** 的位址。</span><span class="sxs-lookup"><span data-stu-id="6e44d-183">For the *pvarStartPosition* parameter, pass the address of the **PROPVARIANT** created in the previous step.</span></span>

<span data-ttu-id="6e44d-184">下列程式碼範例示範如何跳到序列中指定區段的開頭。</span><span class="sxs-lookup"><span data-stu-id="6e44d-184">The following code example shows how to skip to the start of a specified segment in a sequence.</span></span>


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



<span data-ttu-id="6e44d-185">當應用程式跨區段搜尋時，應用程式會收到數個事件，因為 sequencer 來源會結束目前的區段，並準備好播放新的區段。</span><span class="sxs-lookup"><span data-stu-id="6e44d-185">When the application seeks across segments, the application receives several events as the sequencer source ends the current segment and prepares to play the new segment.</span></span> <span data-ttu-id="6e44d-186">因為這些事件是以非同步方式接收，所以很難預測確切的事件順序。</span><span class="sxs-lookup"><span data-stu-id="6e44d-186">Because these events are received asynchronously, it is difficult to predict the exact sequence of events.</span></span> <span data-ttu-id="6e44d-187">這些事件如下所示：</span><span class="sxs-lookup"><span data-stu-id="6e44d-187">These events are as follows:</span></span>

-   <span data-ttu-id="6e44d-188">Sequencer 來源會針對即將略過媒體會話的新區段傳送 [MENewPresentation](menewpresentation.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="6e44d-188">The sequencer source sends an [MENewPresentation](menewpresentation.md) event for the new segment to which the Media Session is skipping.</span></span>

-   <span data-ttu-id="6e44d-189">當 sequencer 來源結束使用中區段時，它會傳送 [MEEndOfPresentationSegment](meendofpresentationsegment.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="6e44d-189">When the sequencer source ends the active segment, it sends the [MEEndOfPresentationSegment](meendofpresentationsegment.md) event.</span></span>
-   <span data-ttu-id="6e44d-190">Sequencer 來源接著會取消預先進行的拓撲。</span><span class="sxs-lookup"><span data-stu-id="6e44d-190">The sequencer source then cancels the preroll topology.</span></span> <span data-ttu-id="6e44d-191">這會產生已取消拓撲的下列事件：</span><span class="sxs-lookup"><span data-stu-id="6e44d-191">This results in the following events for the canceled topology:</span></span>

    -   <span data-ttu-id="6e44d-192">[](mesessiontopologystatus.md)具有 MF \_ TOPOSTATUS READY 旗標的 MESessionTopologyStatus 事件 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6e44d-192">[MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag.</span></span>
    -   <span data-ttu-id="6e44d-193">[](mesessiontopologystatus.md)具有 MF \_ TOPOSTATUS \_ 啟動 \_ 來源旗標的 MESessionTopologyStatus 事件。</span><span class="sxs-lookup"><span data-stu-id="6e44d-193">[MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_STARTED\_SOURCE flag.</span></span>
    -   <span data-ttu-id="6e44d-194">具有 [ [MF \_ 事件 \_ 來源 \_ 拓撲 \_ 已取消](mf-event-source-topology-canceled-attribute.md)] 屬性的[MEEndOfPresentationSegment](meendofpresentationsegment.md)事件，表示拓撲已由 sequencer 來源取消。</span><span class="sxs-lookup"><span data-stu-id="6e44d-194">[MEEndOfPresentationSegment](meendofpresentationsegment.md) event with the [MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED](mf-event-source-topology-canceled-attribute.md) attribute to indicate that the topology was canceled by the sequencer source.</span></span>

-   <span data-ttu-id="6e44d-195">接著，sequencer 來源會傳送新區段的事件，包括各種 [MESessionTopologyStatus](mesessiontopologystatus.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="6e44d-195">Next, the sequencer source sends events for the new segment, including various [MESessionTopologyStatus](mesessiontopologystatus.md) events.</span></span>
-   <span data-ttu-id="6e44d-196">如果新區段不是清單中的最後一個區段，sequencer 來源就會重新整理預先產生的清單，並針對新的預先產生拓撲引發另一個 [MENewPresentation](menewpresentation.md) 。</span><span class="sxs-lookup"><span data-stu-id="6e44d-196">If the new segment is not the last on the list, the sequencer source refreshes the preroll list and raises another [MENewPresentation](menewpresentation.md) for the new preroll topology.</span></span> <span data-ttu-id="6e44d-197">如需有關預先排程清單中拓撲的詳細資訊，請參閱 [關於 Sequencer 來源](about-the-sequencer-source.md)。</span><span class="sxs-lookup"><span data-stu-id="6e44d-197">For information about topologies in the preroll list, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="6e44d-198">有關 sequencer 來源所傳送之事件的更多詳細資料，可在「 [Sequencer 來源事件](sequencer-source-events.md)」主題中找到。</span><span class="sxs-lookup"><span data-stu-id="6e44d-198">More details about the events sent by the sequencer source can be found in the topic [Sequencer Source Events](sequencer-source-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e44d-199">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e44d-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e44d-200">如何建立播放清單</span><span class="sxs-lookup"><span data-stu-id="6e44d-200">How to Create a Playlist</span></span>](how-to-create-a-playlist.md)
</dt> <dt>

[<span data-ttu-id="6e44d-201">Sequencer 來源</span><span class="sxs-lookup"><span data-stu-id="6e44d-201">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



