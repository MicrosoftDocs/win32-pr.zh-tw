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
# <a name="how-to-create-a-playlist"></a><span data-ttu-id="1072a-103">如何建立播放清單</span><span class="sxs-lookup"><span data-stu-id="1072a-103">How to Create a Playlist</span></span>

<span data-ttu-id="1072a-104">本主題說明如何使用順序來源來播放一連串的檔案。</span><span class="sxs-lookup"><span data-stu-id="1072a-104">This topic describes how to use the Sequence Source to play a sequence of files.</span></span>

## <a name="overview"></a><span data-ttu-id="1072a-105">概觀</span><span class="sxs-lookup"><span data-stu-id="1072a-105">Overview</span></span>

<span data-ttu-id="1072a-106">若要在序列中播放媒體檔案，應用程式必須以順序新增拓撲以建立播放清單，並在媒體會話上將這些拓撲排入佇列以供播放。</span><span class="sxs-lookup"><span data-stu-id="1072a-106">To play media files in a sequence, the application must add topologies in a sequence to create a playlist, and queue these topologies on the Media Session for playback.</span></span>

<span data-ttu-id="1072a-107">Sequencer 來源會在媒體會話開始播放目前的拓撲之前，初始化和載入下一個拓撲，以確保無縫播放。</span><span class="sxs-lookup"><span data-stu-id="1072a-107">The sequencer source ensures seamless playback by initializing and loading the next topology before the Media Session starts playing the current topology.</span></span> <span data-ttu-id="1072a-108">這可讓應用程式在需要時快速啟動下一個拓撲。</span><span class="sxs-lookup"><span data-stu-id="1072a-108">This enables the application to start the next topology quickly whenever it is required.</span></span>

<span data-ttu-id="1072a-109">媒體會話負責將資料摘要至接收，並在順序來源中播放拓撲。</span><span class="sxs-lookup"><span data-stu-id="1072a-109">The Media Session is responsible for feeding data to the sinks and playing the topologies in the sequence source.</span></span> <span data-ttu-id="1072a-110">此外，媒體會話也會管理區段的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="1072a-110">In addition, the Media Session manages the presentation time for the segments.</span></span>

<span data-ttu-id="1072a-111">如需有關 sequencer 來源如何管理拓撲的詳細資訊，請參閱 [關於 Sequencer 來源](about-the-sequencer-source.md)。</span><span class="sxs-lookup"><span data-stu-id="1072a-111">For more information about how the sequencer source manages topologies, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="1072a-112">本逐步解說包含下列步驟：</span><span class="sxs-lookup"><span data-stu-id="1072a-112">This walk-through contains the following steps:</span></span>

1.  [<span data-ttu-id="1072a-113">先決條件</span><span class="sxs-lookup"><span data-stu-id="1072a-113">Prerequisites</span></span>](#prerequisites)
2.  [<span data-ttu-id="1072a-114">正在初始化媒體基礎</span><span class="sxs-lookup"><span data-stu-id="1072a-114">Initializing Media Foundation</span></span>](#initializing-media-foundation)
3.  [<span data-ttu-id="1072a-115">建立媒體基礎物件</span><span class="sxs-lookup"><span data-stu-id="1072a-115">Creating Media Foundation Objects</span></span>](#creating-media-foundation-objects)
4.  [<span data-ttu-id="1072a-116">建立媒體來源</span><span class="sxs-lookup"><span data-stu-id="1072a-116">Creating the Media Source</span></span>](#creating-the-media-source)
5.  [<span data-ttu-id="1072a-117">建立部分拓撲</span><span class="sxs-lookup"><span data-stu-id="1072a-117">Creating Partial Topologies</span></span>](#creating-partial-topologies)
6.  [<span data-ttu-id="1072a-118">將拓撲新增至 Sequencer 來源</span><span class="sxs-lookup"><span data-stu-id="1072a-118">Adding Topologies to the Sequencer Source</span></span>](#adding-topologies-to-the-sequencer-source)
7.  [<span data-ttu-id="1072a-119">設定媒體會話的第一個拓撲</span><span class="sxs-lookup"><span data-stu-id="1072a-119">Setting the First Topology on the Media Session</span></span>](#setting-the-first-topology-on-the-media-session)
8.  [<span data-ttu-id="1072a-120">排入媒體會話下一個拓撲的佇列</span><span class="sxs-lookup"><span data-stu-id="1072a-120">Queuing the Next Topology on the Media Session</span></span>](#queuing-the-next-topology-on-the-media-session)
9.  [<span data-ttu-id="1072a-121">釋放 Sequencer 來源</span><span class="sxs-lookup"><span data-stu-id="1072a-121">Releasing the Sequencer Source</span></span>](#releasing-the-sequencer-source)

<span data-ttu-id="1072a-122">本主題所顯示的程式碼範例是主題 [Sequencer 來源範例程式碼](sequencer-source-example-code.md)中的摘錄，其中包含完整的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="1072a-122">The code examples shown this topic are excerpts from the topic [Sequencer Source Example Code](sequencer-source-example-code.md), which contains the complete example code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1072a-123">必要條件</span><span class="sxs-lookup"><span data-stu-id="1072a-123">Prerequisites</span></span>

<span data-ttu-id="1072a-124">開始本逐步解說之前，請先熟悉下列媒體基礎概念：</span><span class="sxs-lookup"><span data-stu-id="1072a-124">Before starting this walk-through, familiarize yourself with the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="1072a-125">媒體會話</span><span class="sxs-lookup"><span data-stu-id="1072a-125">Media Session</span></span>](media-session.md)
-   [<span data-ttu-id="1072a-126">拓撲</span><span class="sxs-lookup"><span data-stu-id="1072a-126">Topologies</span></span>](topologies.md)
-   [<span data-ttu-id="1072a-127">媒體事件產生器</span><span class="sxs-lookup"><span data-stu-id="1072a-127">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="1072a-128">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="1072a-128">Presentation Descriptors</span></span>](presentation-descriptors.md)

<span data-ttu-id="1072a-129">此外，請參閱 [如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案，因為這裡的範例程式碼 shwon 展開該主題中的程式碼。</span><span class="sxs-lookup"><span data-stu-id="1072a-129">Also read [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), because the example code shwon here expands on the code in that topic.</span></span>

## <a name="initializing-media-foundation"></a><span data-ttu-id="1072a-130">正在初始化媒體基礎</span><span class="sxs-lookup"><span data-stu-id="1072a-130">Initializing Media Foundation</span></span>

<span data-ttu-id="1072a-131">在您可以使用任何媒體基礎介面或方法之前，請先呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 函式來初始化媒體基礎。</span><span class="sxs-lookup"><span data-stu-id="1072a-131">Before you can use any Media Foundation interfaces or methods, initialize Media Foundation by calling the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function.</span></span> <span data-ttu-id="1072a-132">如需詳細資訊，請參閱 [初始化媒體基礎](initializing-media-foundation.md)。</span><span class="sxs-lookup"><span data-stu-id="1072a-132">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>


```C++
    hr = MFStartup(MF_VERSION);
```



## <a name="creating-media-foundation-objects"></a><span data-ttu-id="1072a-133">建立媒體基礎物件</span><span class="sxs-lookup"><span data-stu-id="1072a-133">Creating Media Foundation Objects</span></span>

<span data-ttu-id="1072a-134">接下來，建立下列媒體基礎物件：</span><span class="sxs-lookup"><span data-stu-id="1072a-134">Next, create the following Media Foundation objects:</span></span>

-   <span data-ttu-id="1072a-135">媒體會話。</span><span class="sxs-lookup"><span data-stu-id="1072a-135">Media session.</span></span> <span data-ttu-id="1072a-136">此物件會公開 [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) 介面，此介面會提供用來播放、暫停和停止目前拓撲的方法。</span><span class="sxs-lookup"><span data-stu-id="1072a-136">This object exposes the [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface, which provides methods to play, pause, and stop the current topology.</span></span>
-   <span data-ttu-id="1072a-137">Sequencer 來源。</span><span class="sxs-lookup"><span data-stu-id="1072a-137">Sequencer source.</span></span> <span data-ttu-id="1072a-138">此物件會公開 [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) 介面，以提供在序列中新增、更新和刪除拓撲的方法。</span><span class="sxs-lookup"><span data-stu-id="1072a-138">This object exposes the [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) interface, which provides methods to add, update, and delete topologies in a sequence.</span></span>

1.  <span data-ttu-id="1072a-139">呼叫 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) 函數來建立媒體會話。</span><span class="sxs-lookup"><span data-stu-id="1072a-139">Call the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) function to create the Media Session.</span></span>
2.  <span data-ttu-id="1072a-140">呼叫 [**IMFMediaEventQueue：： BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) ，以要求媒體會話中的第一個事件。</span><span class="sxs-lookup"><span data-stu-id="1072a-140">Call [**IMFMediaEventQueue::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-begingetevent) to request the first event from the Media Session.</span></span>
3.  <span data-ttu-id="1072a-141">呼叫 [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) 函數，以建立 sequencer 來源。</span><span class="sxs-lookup"><span data-stu-id="1072a-141">Call the [**MFCreateSequencerSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesequencersource) function to create the sequencer source.</span></span>

<span data-ttu-id="1072a-142">下列程式碼會建立媒體會話，並要求第一個事件：</span><span class="sxs-lookup"><span data-stu-id="1072a-142">The following code creates the Media Session and requests the first event:</span></span>


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



## <a name="creating-the-media-source"></a><span data-ttu-id="1072a-143">建立媒體來源</span><span class="sxs-lookup"><span data-stu-id="1072a-143">Creating the Media Source</span></span>

<span data-ttu-id="1072a-144">接下來，為第一個播放清單區段建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="1072a-144">Next, create a media source for the first playlist segment.</span></span> <span data-ttu-id="1072a-145">使用 [來源解析程式](source-resolver.md) ，從 URL 建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="1072a-145">Use the [Source Resolver](source-resolver.md) to create a media source from a URL.</span></span> <span data-ttu-id="1072a-146">若要這樣做，請呼叫 [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) 函數來建立來源解析程式，然後呼叫 [**IMFSourceResolver：： CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) 方法來建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="1072a-146">To do this, call the [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver) function to create a source resolver and then call the [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) method to create the media source.</span></span>

<span data-ttu-id="1072a-147">如需媒體來源的詳細資訊，請參閱 [媒體來源](media-sources.md)。</span><span class="sxs-lookup"><span data-stu-id="1072a-147">For information about media sources, see [Media Sources](media-sources.md).</span></span>

## <a name="creating-partial-topologies"></a><span data-ttu-id="1072a-148">建立部分拓撲</span><span class="sxs-lookup"><span data-stu-id="1072a-148">Creating Partial Topologies</span></span>

<span data-ttu-id="1072a-149">Sequencer 來源中的每個區段都有自己的部分拓撲。</span><span class="sxs-lookup"><span data-stu-id="1072a-149">Each segment in the sequencer source has its own partial topology.</span></span> <span data-ttu-id="1072a-150">接下來，建立媒體來源的部分拓撲。</span><span class="sxs-lookup"><span data-stu-id="1072a-150">Next, create partial topologies for media sources.</span></span> <span data-ttu-id="1072a-151">若為部分拓撲，拓撲來源節點會直接連接至輸出節點，而不會指定任何中繼轉換。</span><span class="sxs-lookup"><span data-stu-id="1072a-151">For a partial topology, the topology source nodes are connected directly to the output nodes, without specifying any intermediate transforms.</span></span> <span data-ttu-id="1072a-152">媒體會話會使用拓撲載入器物件來解析拓撲。</span><span class="sxs-lookup"><span data-stu-id="1072a-152">The Media Session uses the topology loader object to resolve the topology.</span></span> <span data-ttu-id="1072a-153">解析拓撲之後，會新增必要的解碼器和其他轉換節點。</span><span class="sxs-lookup"><span data-stu-id="1072a-153">After a topology is resolved, the required decoders and other transform nodes are added.</span></span> <span data-ttu-id="1072a-154">Sequencer 來源也可以包含完整的拓撲。</span><span class="sxs-lookup"><span data-stu-id="1072a-154">The sequencer source can also contain full topologies.</span></span>

<span data-ttu-id="1072a-155">若要建立拓撲物件，請使用 [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) 函數，然後使用 [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) 介面來建立資料流程節點。</span><span class="sxs-lookup"><span data-stu-id="1072a-155">To create the topology object, use the [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) function and then use the [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) interface to create stream nodes.</span></span>

<span data-ttu-id="1072a-156">如需使用這些程式設計項目建立拓撲的完整指示，請參閱 [建立播放拓撲](creating-playback-topologies.md)。</span><span class="sxs-lookup"><span data-stu-id="1072a-156">For complete instructions on using these programming elements to create topologies, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

<span data-ttu-id="1072a-157">應用程式可以藉由設定來源節點來播放原生來源的選定部分。</span><span class="sxs-lookup"><span data-stu-id="1072a-157">An application can play a selected portion of the native source by configuring the source node.</span></span> <span data-ttu-id="1072a-158">若要這樣做，請在 [ **mf \_ 拓撲 \_ SOURCESTREAM \_ 節點** 拓撲] 節點上設定 [ [**mf \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md) ] 屬性和 [ [**mf \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="1072a-158">To do this, set the [**MF\_TOPONODE\_MEDIASTART**](mf-toponode-mediastart-attribute.md) attribute and the [**MF\_TOPONODE\_MEDIASTOP**](mf-toponode-mediastop-attribute.md) attribute on **MF\_TOPOLOGY\_SOURCESTREAM\_NODE** topology nodes.</span></span> <span data-ttu-id="1072a-159">指定媒體開始時間和媒體停止時間（相對於原生來源作為 **UINT64** 類型的起點）。</span><span class="sxs-lookup"><span data-stu-id="1072a-159">Specify the media start time and the media stop time relative to the start of the native source as **UINT64** types.</span></span>

## <a name="adding-topologies-to-the-sequencer-source"></a><span data-ttu-id="1072a-160">將拓撲新增至 Sequencer 來源</span><span class="sxs-lookup"><span data-stu-id="1072a-160">Adding Topologies to the Sequencer Source</span></span>

<span data-ttu-id="1072a-161">接下來，將您建立的部分拓撲新增至 sequencer 來源。</span><span class="sxs-lookup"><span data-stu-id="1072a-161">Next, add to the sequencer source the partial topologies that you created.</span></span> <span data-ttu-id="1072a-162">每個 sequence 元素（稱為 *區段*）都會被指派一個 **MFSequencerElementId** 識別碼。</span><span class="sxs-lookup"><span data-stu-id="1072a-162">Each sequence element, called a *segment*, is assigned an **MFSequencerElementId** identifier.</span></span> <span data-ttu-id="1072a-163">如需有關 sequencer 來源如何管理拓撲的詳細資訊，請參閱 [關於 Sequencer 來源](about-the-sequencer-source.md)。</span><span class="sxs-lookup"><span data-stu-id="1072a-163">For more information about how the sequencer source manages topologies, see [About the Sequencer Source](about-the-sequencer-source.md).</span></span>

<span data-ttu-id="1072a-164">將所有拓撲新增至 sequencer 來源之後，應用程式必須將序列中的最後一個區段標記為管線中的結束播放。</span><span class="sxs-lookup"><span data-stu-id="1072a-164">After all of the topologies are added to the sequencer source, the application must flag the last segment in the sequence to end playback in the pipeline.</span></span> <span data-ttu-id="1072a-165">如果沒有這個旗標，sequencer 來源預期會加入更多拓撲。</span><span class="sxs-lookup"><span data-stu-id="1072a-165">Without this flag, the sequencer source expects more topologies to be added.</span></span>

1.  <span data-ttu-id="1072a-166">呼叫 [**IMFSequencerSource：： AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) 方法，將特定拓撲新增至 sequencer 來源。</span><span class="sxs-lookup"><span data-stu-id="1072a-166">Call the [**IMFSequencerSource::AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) method to add a specific topology to the sequencer source.</span></span>

    ```C++
        hr = m_pSequencerSource->AppendTopology(
            pTopology, 
            SequencerTopologyFlags_Last, 
            &SegmentId
            );
    ```

    

    <span data-ttu-id="1072a-167">[**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) 會將指定的拓撲新增至順序。</span><span class="sxs-lookup"><span data-stu-id="1072a-167">[**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) adds the specified topology to the sequence.</span></span> <span data-ttu-id="1072a-168">這個方法會傳回 *pdwId* 參數中的區段識別碼。</span><span class="sxs-lookup"><span data-stu-id="1072a-168">This method returns the segment identifier in the *pdwId* parameter.</span></span>

    <span data-ttu-id="1072a-169">如果拓撲是 sequencer 來源中的最後一個拓撲，請 \_ 在 *dwFlags* 參數中最後傳遞 SequencerTopologyFlags。</span><span class="sxs-lookup"><span data-stu-id="1072a-169">If the topology is the last one in the sequencer source, pass SequencerTopologyFlags\_Last in the *dwFlags* parameter.</span></span> <span data-ttu-id="1072a-170">此值定義于 [**MFSequencerTopologyFlags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) 列舉中。</span><span class="sxs-lookup"><span data-stu-id="1072a-170">This value is defined in the [**MFSequencerTopologyFlags**](/windows/desktop/api/mfidl/ne-mfidl-mfsequencertopologyflags) enumeration.</span></span>

2.  <span data-ttu-id="1072a-171">呼叫 [**IMFSequencerSource：： UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) ，以更新與輸入清單中區段識別碼相關聯之拓撲的旗標。</span><span class="sxs-lookup"><span data-stu-id="1072a-171">Call [**IMFSequencerSource::UpdateTopologyFlags**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopologyflags) to update the flags for the topology associated with the segment identifier in the input list.</span></span> <span data-ttu-id="1072a-172">在此情況下，呼叫會指出指定的區段是 sequencer 中的最後一個區段。</span><span class="sxs-lookup"><span data-stu-id="1072a-172">In this case, the call indicates that the specified segment is the last segment in the sequencer.</span></span> <span data-ttu-id="1072a-173"> (在 [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) 呼叫中指定最後一個拓撲時，此呼叫是選擇性的。 ) </span><span class="sxs-lookup"><span data-stu-id="1072a-173">(This call is optional if the last topology is specified in the [**AppendTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology) call.)</span></span>

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

    

<span data-ttu-id="1072a-174">應用程式可以藉由呼叫 [**IMFSequencerSource：： UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) 並在 *pTopology* 中傳遞新的拓撲，來將區段的拓撲取代為另一個拓撲。</span><span class="sxs-lookup"><span data-stu-id="1072a-174">The application can replace a segment's topology with another topology by calling the [**IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) and passing the new topology in *pTopology*.</span></span> <span data-ttu-id="1072a-175">如果新拓撲中有新的原生來源，則會將來源新增至來源快取。</span><span class="sxs-lookup"><span data-stu-id="1072a-175">If there are new native sources in the new topology, the sources are added to the source cache.</span></span> <span data-ttu-id="1072a-176">預先整理清單也會重新整理。</span><span class="sxs-lookup"><span data-stu-id="1072a-176">The preroll list is also refreshed.</span></span>

## <a name="setting-the-first-topology-on-the-media-session"></a><span data-ttu-id="1072a-177">設定媒體會話的第一個拓撲</span><span class="sxs-lookup"><span data-stu-id="1072a-177">Setting the First Topology on the Media Session</span></span>

<span data-ttu-id="1072a-178">接下來，將媒體會話上順序來源中的第一個拓撲排入佇列。</span><span class="sxs-lookup"><span data-stu-id="1072a-178">Next, queue the first topology in the sequence source on the Media Session.</span></span> <span data-ttu-id="1072a-179">若要從 sequencer 來源取得第一個拓撲，應用程式必須呼叫 [**IMFMediaSourceTopologyProvider：： GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) 方法。</span><span class="sxs-lookup"><span data-stu-id="1072a-179">To get the first topology from the sequencer source, the application must call the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span> <span data-ttu-id="1072a-180">這個方法會傳回由媒體會話解析的部分拓撲。</span><span class="sxs-lookup"><span data-stu-id="1072a-180">This method returns the partial topology, which is resolved by the Media Session.</span></span>

<span data-ttu-id="1072a-181">如需部分拓撲的詳細資訊，請參閱 [關於拓撲](about-topologies.md)。</span><span class="sxs-lookup"><span data-stu-id="1072a-181">For information about partial topologies, see [About Topologies](about-topologies.md).</span></span>

1.  <span data-ttu-id="1072a-182">針對序列來源的第一個拓撲取得原生媒體來源。</span><span class="sxs-lookup"><span data-stu-id="1072a-182">Retrieve the native media source for the first topology of the sequence source.</span></span>
2.  <span data-ttu-id="1072a-183">藉由呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) 方法，建立媒體來源的簡報描述項。</span><span class="sxs-lookup"><span data-stu-id="1072a-183">Create a presentation descriptor for the media source by calling the [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) method.</span></span>
3.  <span data-ttu-id="1072a-184">藉由呼叫 [**IMFMediaSourceTopologyProvider：： GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) 方法，取得簡報的關聯拓撲。</span><span class="sxs-lookup"><span data-stu-id="1072a-184">Retrieve the associated topology for the presentation by calling the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span>
4.  <span data-ttu-id="1072a-185">藉由呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)，在媒體會話上設定第一個拓撲。</span><span class="sxs-lookup"><span data-stu-id="1072a-185">Set the first topology on the Media Session by Calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

    <span data-ttu-id="1072a-186">呼叫 [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) ，並將 *dwSetTopologyFlags* 參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1072a-186">Call [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) with the *dwSetTopologyFlags* parameter set to **NULL**.</span></span> <span data-ttu-id="1072a-187">這會指示媒體會話在目前的拓撲完成時啟動指定的拓撲。</span><span class="sxs-lookup"><span data-stu-id="1072a-187">This instructs the Media Session to start the specified topology when the current topology has been completed.</span></span> <span data-ttu-id="1072a-188">因為在此情況下，指定的拓撲是第一個拓撲，而且沒有目前的簡報，所以媒體會話會立即啟動新的簡報。</span><span class="sxs-lookup"><span data-stu-id="1072a-188">Because in this case, the specified topology is the first topology and there is no current presentation, the Media Session starts the new presentation immediately.</span></span>

    <span data-ttu-id="1072a-189">**Null** 值也表示媒體會話必須解析拓撲，因為拓撲提供者所傳回的拓撲一律為部分拓撲。</span><span class="sxs-lookup"><span data-stu-id="1072a-189">The **NULL** value also indicates that Media Session must resolve the topology because the topology returned by the topology provider is always a partial topology.</span></span>


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



## <a name="queuing-the-next-topology-on-the-media-session"></a><span data-ttu-id="1072a-190">排入媒體會話下一個拓撲的佇列</span><span class="sxs-lookup"><span data-stu-id="1072a-190">Queuing the Next Topology on the Media Session</span></span>

<span data-ttu-id="1072a-191">接下來，應用程式需要處理 [MENewPresentation](menewpresentation.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="1072a-191">Next, the application needs to handle the [MENewPresentation](menewpresentation.md) event.</span></span>

<span data-ttu-id="1072a-192">當媒體會話開始播放有另一個區段之後的區段時，Sequencer 來源會引發 [MENewPresentation](menewpresentation.md) 。</span><span class="sxs-lookup"><span data-stu-id="1072a-192">Sequencer source raises [MENewPresentation](menewpresentation.md) when the Media Session starts playing a segment that has another segment following it.</span></span> <span data-ttu-id="1072a-193">此事件會提供預先集中清單中下一個區段的表示描述項，以通知應用程式有關序列來源中的下一個拓撲。</span><span class="sxs-lookup"><span data-stu-id="1072a-193">This event informs the application about the next topology in the sequence source by providing the presentation descriptor for the next segment in the preroll list.</span></span> <span data-ttu-id="1072a-194">應用程式必須抓取相關聯的拓撲，方法是使用拓撲提供者，並在媒體會話上將它排入佇列。</span><span class="sxs-lookup"><span data-stu-id="1072a-194">The application must retrieve the associated topology, by using the topology provider, and queue it on the Media Session.</span></span> <span data-ttu-id="1072a-195">Sequencer 來源接著會 prerolls 此拓撲，以確保在簡報之間進行順暢的轉換。</span><span class="sxs-lookup"><span data-stu-id="1072a-195">The sequencer source then prerolls this topology, which ensures a seamless transition between presentations.</span></span>

<span data-ttu-id="1072a-196">當應用程式跨區段搜尋時，應用程式會收到數個 [MENewPresentation](menewpresentation.md) 事件，因為 sequencer 來源會重新整理預先處理的清單，並設定正確的拓撲。</span><span class="sxs-lookup"><span data-stu-id="1072a-196">When the application seeks across segments, the application receives several [MENewPresentation](menewpresentation.md) events as the sequencer source refreshes the preroll list and sets up the correct topology.</span></span> <span data-ttu-id="1072a-197">應用程式必須處理每個事件，並將事件資料中傳回的拓撲排入媒體會話的佇列。</span><span class="sxs-lookup"><span data-stu-id="1072a-197">The application must handle each event and queue the topology returned in the event data, on the Media Session.</span></span> <span data-ttu-id="1072a-198">如需跳過區段的詳細資訊，請參閱 [使用 Sequencer 來源](using-the-sequencer-source.md)。</span><span class="sxs-lookup"><span data-stu-id="1072a-198">For information about skipping segments, see [Using the Sequencer Source](using-the-sequencer-source.md).</span></span>

<span data-ttu-id="1072a-199">如需取得 sequencer 來源通知的詳細資訊，請參閱 [Sequencer 來源事件](sequencer-source-events.md)。</span><span class="sxs-lookup"><span data-stu-id="1072a-199">For information about getting sequencer source notifications, see [Sequencer Source Events](sequencer-source-events.md).</span></span>

1.  <span data-ttu-id="1072a-200">在 [MENewPresentation](menewpresentation.md) 事件處理常式中，從事件資料中取出下一個區段的呈現描述項。</span><span class="sxs-lookup"><span data-stu-id="1072a-200">In the [MENewPresentation](menewpresentation.md) event handler, retrieve the presentation descriptor for the next segment from the event data.</span></span>
2.  <span data-ttu-id="1072a-201">藉由呼叫 [**IMFMediaSourceTopologyProvider：： GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) 方法，取得簡報的關聯拓撲。</span><span class="sxs-lookup"><span data-stu-id="1072a-201">Get the associated topology for the presentation by calling the [**IMFMediaSourceTopologyProvider::GetMediaSourceTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) method.</span></span>
3.  <span data-ttu-id="1072a-202">藉由呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) 方法，在媒體會話上設定拓撲。</span><span class="sxs-lookup"><span data-stu-id="1072a-202">Set the topology on the Media Session by calling the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method.</span></span>

    <span data-ttu-id="1072a-203">當目前的簡報完成時，媒體會話就會啟動新的簡報。</span><span class="sxs-lookup"><span data-stu-id="1072a-203">The Media Session starts the new presentation when the current presentation has been completed.</span></span>


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



## <a name="releasing-the-sequencer-source"></a><span data-ttu-id="1072a-204">釋放 Sequencer 來源</span><span class="sxs-lookup"><span data-stu-id="1072a-204">Releasing the Sequencer Source</span></span>

<span data-ttu-id="1072a-205">最後，關閉 sequencer 來源。</span><span class="sxs-lookup"><span data-stu-id="1072a-205">Finally, shut down the sequencer source.</span></span> <span data-ttu-id="1072a-206">若要這樣做，請在 sequencer 來源上呼叫 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) 方法。</span><span class="sxs-lookup"><span data-stu-id="1072a-206">To do so, call the [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) method on the sequencer source.</span></span> <span data-ttu-id="1072a-207">此呼叫會關閉 sequencer 來源中的所有基礎原生媒體來源。</span><span class="sxs-lookup"><span data-stu-id="1072a-207">This call shuts down all of the underlying native media sources in the sequencer source.</span></span>

<span data-ttu-id="1072a-208">釋放 sequencer 來源之後，應用程式應該依序呼叫 [**IMFMediaSession：： close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) 和 [**IMFMediaSession：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)，關閉並關閉媒體會話。</span><span class="sxs-lookup"><span data-stu-id="1072a-208">After releasing the sequencer source, the application should close and shut down the Media Session by calling [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) and [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown), in that order.</span></span>

<span data-ttu-id="1072a-209">若要避免記憶體流失，當不再需要應用程式時，應用程式必須釋放指向媒體基礎介面的指標。</span><span class="sxs-lookup"><span data-stu-id="1072a-209">To avoid memory leaks, the application must release pointers to Media Foundation interfaces when they are no longer needed.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1072a-210">後續步驟</span><span class="sxs-lookup"><span data-stu-id="1072a-210">Next Steps</span></span>

<span data-ttu-id="1072a-211">本逐步解說說明如何使用 sequencer 來源建立基本播放清單。</span><span class="sxs-lookup"><span data-stu-id="1072a-211">This walk-through illustrated how to create a basic playlist by using the sequencer source.</span></span> <span data-ttu-id="1072a-212">建立播放清單之後，您可能會想要新增先進的功能，例如區段略過、變更播放狀態，以及在區段內搜尋。</span><span class="sxs-lookup"><span data-stu-id="1072a-212">After creating the playlist, you might want to add advanced features such as segment skipping, changing the playback state, and seeking within a segment.</span></span> <span data-ttu-id="1072a-213">下列清單提供相關主題的連結：</span><span class="sxs-lookup"><span data-stu-id="1072a-213">The following list provides links to the related topics:</span></span>

-   <span data-ttu-id="1072a-214">[如何控制呈現狀態](how-to-control-presentation-states.md)： sequencer 來源依賴媒體會話來提供傳輸控制項，例如、播放、暫停和停止。</span><span class="sxs-lookup"><span data-stu-id="1072a-214">[How to Control Presentation States](how-to-control-presentation-states.md): The sequencer source relies on the Media Session to provide transport control such as, Play, Pause, and Stop.</span></span>
-   <span data-ttu-id="1072a-215">[如何執行](how-to-perform-scrubbing.md) 清除說明在資料流程中搜尋特定位置所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="1072a-215">[How to Perform Scrubbing](how-to-perform-scrubbing.md) describes the steps required to seek to a specific position in a stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1072a-216">相關主題</span><span class="sxs-lookup"><span data-stu-id="1072a-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1072a-217">Sequencer 來源</span><span class="sxs-lookup"><span data-stu-id="1072a-217">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 



