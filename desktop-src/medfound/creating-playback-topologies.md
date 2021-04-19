---
description: 本主題說明如何建立音訊或影片播放的拓朴。
ms.assetid: 9c536c4e-fbf8-4c16-932f-e5863b7652fe
title: 建立播放拓撲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6d34e9237278766ccb1ee174ba6c09bf953933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970745"
---
# <a name="creating-playback-topologies"></a><span data-ttu-id="1fda5-103">建立播放拓撲</span><span class="sxs-lookup"><span data-stu-id="1fda5-103">Creating Playback Topologies</span></span>

<span data-ttu-id="1fda5-104">本主題說明如何建立音訊或影片播放的拓朴。</span><span class="sxs-lookup"><span data-stu-id="1fda5-104">This topic describes how to create a topology for audio or video playback.</span></span> <span data-ttu-id="1fda5-105">針對基本播放，您可以建立部分拓撲，其中來源節點會直接連接至輸出節點。</span><span class="sxs-lookup"><span data-stu-id="1fda5-105">For basic playback, you can create a partial topology, in which the source nodes are connected directly to the output nodes.</span></span> <span data-ttu-id="1fda5-106">您不需要為中繼轉換（例如，「解碼器」或「色彩轉換器」）插入任何節點。</span><span class="sxs-lookup"><span data-stu-id="1fda5-106">You do not need to insert any nodes for the intermediate transforms, such as decoders or color converters.</span></span> <span data-ttu-id="1fda5-107">媒體會話將使用拓撲載入器來解析拓撲，而拓撲載入器會插入所需的轉換。</span><span class="sxs-lookup"><span data-stu-id="1fda5-107">The Media Session will use the topology loader to resolve the topology, and the topology loader will insert the transforms that are required.</span></span>

-   [<span data-ttu-id="1fda5-108">建立拓撲</span><span class="sxs-lookup"><span data-stu-id="1fda5-108">Creating the Topology</span></span>](#creating-the-topology)
-   [<span data-ttu-id="1fda5-109">將資料流程連接到媒體接收器</span><span class="sxs-lookup"><span data-stu-id="1fda5-109">Connecting Streams to Media Sinks</span></span>](#connecting-streams-to-media-sinks)
-   [<span data-ttu-id="1fda5-110">建立媒體接收器</span><span class="sxs-lookup"><span data-stu-id="1fda5-110">Creating the Media Sink</span></span>](#creating-the-media-sink)
-   [<span data-ttu-id="1fda5-111">後續步驟</span><span class="sxs-lookup"><span data-stu-id="1fda5-111">Next Steps</span></span>](#next-steps)
-   [<span data-ttu-id="1fda5-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="1fda5-112">Related topics</span></span>](#related-topics)

## <a name="creating-the-topology"></a><span data-ttu-id="1fda5-113">建立拓撲</span><span class="sxs-lookup"><span data-stu-id="1fda5-113">Creating the Topology</span></span>

<span data-ttu-id="1fda5-114">從媒體來源建立部分播放拓撲的整體步驟如下：</span><span class="sxs-lookup"><span data-stu-id="1fda5-114">Here are the overall steps for creating a partial playback topology from a media source:</span></span>

1.  <span data-ttu-id="1fda5-115">建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="1fda5-115">Create the media source.</span></span> <span data-ttu-id="1fda5-116">在大多數情況下，您將使用來源解析程式來建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="1fda5-116">In most cases, you will use the source resolver to create the media source.</span></span> <span data-ttu-id="1fda5-117">如需詳細資訊，請參閱 [來源解析程式](source-resolver.md)。</span><span class="sxs-lookup"><span data-stu-id="1fda5-117">For more information, see [Source Resolver](source-resolver.md).</span></span>
2.  <span data-ttu-id="1fda5-118">取得媒體來源的展示描述項。</span><span class="sxs-lookup"><span data-stu-id="1fda5-118">Get the media source's presentation descriptor.</span></span>
3.  <span data-ttu-id="1fda5-119">建立空的拓撲。</span><span class="sxs-lookup"><span data-stu-id="1fda5-119">Create an empty topology.</span></span>
4.  <span data-ttu-id="1fda5-120">使用展示描述元來列舉資料流程描述項。</span><span class="sxs-lookup"><span data-stu-id="1fda5-120">Use the presentation descriptor to enumerate the stream descriptors.</span></span> <span data-ttu-id="1fda5-121">針對每個資料流程描述元：</span><span class="sxs-lookup"><span data-stu-id="1fda5-121">For each stream descriptor:</span></span>
    1.  <span data-ttu-id="1fda5-122">取得資料流程的主要媒體類型，例如音訊或影片。</span><span class="sxs-lookup"><span data-stu-id="1fda5-122">Get the stream's major media type, such as audio or video.</span></span>
    2.  <span data-ttu-id="1fda5-123">檢查目前是否已選取資料流程。</span><span class="sxs-lookup"><span data-stu-id="1fda5-123">Check if the stream is currently selected.</span></span> <span data-ttu-id="1fda5-124"> (選擇性地，您可以根據媒體類型來選取或取消選取資料流程。 ) </span><span class="sxs-lookup"><span data-stu-id="1fda5-124">(Optionally, you can select or deselect a stream, based on the media type.)</span></span>
    3.  <span data-ttu-id="1fda5-125">如果已選取資料流程，請根據資料流程的媒體類型，建立媒體接收器的啟用物件。</span><span class="sxs-lookup"><span data-stu-id="1fda5-125">If the stream is selected, create an activation object for the media sink, based on the stream's media type.</span></span>
    4.  <span data-ttu-id="1fda5-126">新增資料流程的來源節點和媒體接收器的輸出節點。</span><span class="sxs-lookup"><span data-stu-id="1fda5-126">Add a source node for the stream and an output node for the media sink.</span></span>
    5.  <span data-ttu-id="1fda5-127">將來源節點連接至輸出節點。</span><span class="sxs-lookup"><span data-stu-id="1fda5-127">Connect the source node to the output node.</span></span>

<span data-ttu-id="1fda5-128">為了讓此程式更容易遵循，本主題中的範例程式碼會分成數個函式。</span><span class="sxs-lookup"><span data-stu-id="1fda5-128">To make this process easier to follow, the example code in this topic is organized into several functions.</span></span> <span data-ttu-id="1fda5-129">最上層函數的名稱為 `CreatePlaybackTopology` 。</span><span class="sxs-lookup"><span data-stu-id="1fda5-129">The top-level function is named `CreatePlaybackTopology`.</span></span> <span data-ttu-id="1fda5-130">它會採用三個參數：</span><span class="sxs-lookup"><span data-stu-id="1fda5-130">It takes three parameters:</span></span>

-   <span data-ttu-id="1fda5-131">媒體來源之 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="1fda5-131">A pointer to a [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="1fda5-132">表示描述項之 [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="1fda5-132">A pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor.</span></span> <span data-ttu-id="1fda5-133">藉由呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)來取得此指標。</span><span class="sxs-lookup"><span data-stu-id="1fda5-133">Get this pointer by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="1fda5-134">針對具有多個簡報的來源，後續簡報的呈現描述項會在 [MENewPresentation](menewpresentation.md) 事件中傳遞。</span><span class="sxs-lookup"><span data-stu-id="1fda5-134">For sources with multiple presentations, the presentation descriptors for subsequent presentations are delivered in the [MENewPresentation](menewpresentation.md) event.</span></span>
-   <span data-ttu-id="1fda5-135">應用程式視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1fda5-135">A handle to an application window.</span></span> <span data-ttu-id="1fda5-136">如果來源有影片串流，則影片會顯示在此視窗中。</span><span class="sxs-lookup"><span data-stu-id="1fda5-136">If the source has a video stream, the video will be displayed in this window.</span></span>

<span data-ttu-id="1fda5-137">函數會傳回 *ppTopology* 參數中部分播放拓撲的指標。</span><span class="sxs-lookup"><span data-stu-id="1fda5-137">The function returns a pointer to a partial playback topology in the *ppTopology* parameter.</span></span>


```C++
//  Create a playback topology from a media source.
HRESULT CreatePlaybackTopology(
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    HWND hVideoWnd,                   // Video window.
    IMFTopology **ppTopology)         // Receives a pointer to the topology.
{
    IMFTopology *pTopology = NULL;
    DWORD cSourceStreams = 0;

    // Create a new topology.
    HRESULT hr = MFCreateTopology(&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }




    // Get the number of streams in the media source.
    hr = pPD->GetStreamDescriptorCount(&cSourceStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    // For each stream, create the topology nodes and add them to the topology.
    for (DWORD i = 0; i < cSourceStreams; i++)
    {
        hr = AddBranchToPartialTopology(pTopology, pSource, pPD, i, hVideoWnd);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Return the IMFTopology pointer to the caller.
    *ppTopology = pTopology;
    (*ppTopology)->AddRef();

done:
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="1fda5-138">此函式會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="1fda5-138">This function performs the following steps:</span></span>

1.  <span data-ttu-id="1fda5-139">呼叫 [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) 來建立拓撲。</span><span class="sxs-lookup"><span data-stu-id="1fda5-139">Call [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) to create the topology.</span></span> <span data-ttu-id="1fda5-140">一開始，拓撲不包含任何節點。</span><span class="sxs-lookup"><span data-stu-id="1fda5-140">Initially, the topology does not contain any nodes.</span></span>
2.  <span data-ttu-id="1fda5-141">呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) 來取得簡報中的資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="1fda5-141">Call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) to get the number of streams in the presentation.</span></span>
3.  <span data-ttu-id="1fda5-142">針對每個資料流程，將應用程式定義 `AddBranchToPartialTopology` 函數呼叫至拓撲中的分支。</span><span class="sxs-lookup"><span data-stu-id="1fda5-142">For each stream, call the application-defined `AddBranchToPartialTopology` function to a branch in the topology.</span></span> <span data-ttu-id="1fda5-143">下一節會顯示此函數。</span><span class="sxs-lookup"><span data-stu-id="1fda5-143">This function is shown in the next section.</span></span>

## <a name="connecting-streams-to-media-sinks"></a><span data-ttu-id="1fda5-144">將資料流程連接到媒體接收器</span><span class="sxs-lookup"><span data-stu-id="1fda5-144">Connecting Streams to Media Sinks</span></span>

<span data-ttu-id="1fda5-145">針對每個選取的資料流程，新增來源節點和輸出節點，然後連接這兩個節點。</span><span class="sxs-lookup"><span data-stu-id="1fda5-145">For each selected stream, add a source node and an output node, then connect the two nodes.</span></span> <span data-ttu-id="1fda5-146">來源節點代表資料流程。</span><span class="sxs-lookup"><span data-stu-id="1fda5-146">The source node represents the stream.</span></span> <span data-ttu-id="1fda5-147">輸出節點代表 [增強型影片](enhanced-video-renderer.md) 轉譯器 (EVR) 或 [串流音訊](streaming-audio-renderer.md) 轉譯器 (SAR) 。</span><span class="sxs-lookup"><span data-stu-id="1fda5-147">The output node represents either the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) or the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR).</span></span>

<span data-ttu-id="1fda5-148">`AddBranchToPartialTopology`下一個範例所示的函式會採用下列參數：</span><span class="sxs-lookup"><span data-stu-id="1fda5-148">The `AddBranchToPartialTopology` function, shown in the next example, takes the following parameters:</span></span>

-   <span data-ttu-id="1fda5-149">拓撲之 [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="1fda5-149">A pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the topology.</span></span>
-   <span data-ttu-id="1fda5-150">媒體來源之 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="1fda5-150">A pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="1fda5-151">表示描述項之 [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="1fda5-151">A pointer to the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface of the presentation descriptor.</span></span>
-   <span data-ttu-id="1fda5-152">以零為基底的資料流程索引。</span><span class="sxs-lookup"><span data-stu-id="1fda5-152">The zero-based index of the stream.</span></span>
-   <span data-ttu-id="1fda5-153">影片視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1fda5-153">A handle to the video window.</span></span> <span data-ttu-id="1fda5-154">這個控制碼只適用于影片串流。</span><span class="sxs-lookup"><span data-stu-id="1fda5-154">This handle is used only for the video stream.</span></span>


```C++
//  Add a topology branch for one stream.
//
//  For each stream, this function does the following:
//
//    1. Creates a source node associated with the stream. 
//    2. Creates an output node for the renderer. 
//    3. Connects the two nodes.
//
//  The media session will add any decoders that are needed.

HRESULT AddBranchToPartialTopology(
    IMFTopology *pTopology,         // Topology.
    IMFMediaSource *pSource,        // Media source.
    IMFPresentationDescriptor *pPD, // Presentation descriptor.
    DWORD iStream,                  // Stream index.
    HWND hVideoWnd)                 // Window for video playback.
{
    IMFStreamDescriptor *pSD = NULL;
    IMFActivate         *pSinkActivate = NULL;
    IMFTopologyNode     *pSourceNode = NULL;
    IMFTopologyNode     *pOutputNode = NULL;

    BOOL fSelected = FALSE;

    HRESULT hr = pPD->GetStreamDescriptorByIndex(iStream, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    if (fSelected)
    {
        // Create the media sink activation object.
        hr = CreateMediaSinkActivate(pSD, hVideoWnd, &pSinkActivate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Add a source node for this stream.
        hr = AddSourceNode(pTopology, pSource, pPD, pSD, &pSourceNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Create the output node for the renderer.
        hr = AddOutputNode(pTopology, pSinkActivate, 0, &pOutputNode);
        if (FAILED(hr))
        {
            goto done;
        }

        // Connect the source node to the output node.
        hr = pSourceNode->ConnectOutput(0, pOutputNode, 0);
    }
    // else: If not selected, don't add the branch. 

done:
    SafeRelease(&pSD);
    SafeRelease(&pSinkActivate);
    SafeRelease(&pSourceNode);
    SafeRelease(&pOutputNode);
    return hr;
}
```



<span data-ttu-id="1fda5-155">函數會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="1fda5-155">The function does the following:</span></span>

1.  <span data-ttu-id="1fda5-156">呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) ，並傳入資料流程索引。</span><span class="sxs-lookup"><span data-stu-id="1fda5-156">Calls [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) and passes in the stream index.</span></span> <span data-ttu-id="1fda5-157">這個方法會傳回該資料流程的資料流程描述元指標，以及指出是否已選取資料流程的布林值。</span><span class="sxs-lookup"><span data-stu-id="1fda5-157">This method returns a pointer to the stream descriptor for that stream, along with a Boolean value indicating whether the stream is selected.</span></span>
2.  <span data-ttu-id="1fda5-158">如果未選取資料流程，則函式會結束並傳回 S \_ OK，因為應用程式不需要為數據流建立拓撲分支，除非已選取它。</span><span class="sxs-lookup"><span data-stu-id="1fda5-158">If the stream is not selected, the function exits and returns S\_OK, because the application does not need to create a topology branch for a stream unless it is selected.</span></span>
3.  <span data-ttu-id="1fda5-159">如果選取資料流程，則函式會完成拓撲分支，如下所示：</span><span class="sxs-lookup"><span data-stu-id="1fda5-159">If the stream is selected, the function completes the topology branch as follows:</span></span>
    1.  <span data-ttu-id="1fda5-160">藉由呼叫應用程式定義的 CreateMediaSinkActivate 函式，建立接收的啟用物件。</span><span class="sxs-lookup"><span data-stu-id="1fda5-160">Creates an activation object for the sink, by calling the application-defined CreateMediaSinkActivate function.</span></span> <span data-ttu-id="1fda5-161">下一節會顯示此函數。</span><span class="sxs-lookup"><span data-stu-id="1fda5-161">This function is shown in the next section.</span></span>
    2.  <span data-ttu-id="1fda5-162">將來源節點新增至拓撲。</span><span class="sxs-lookup"><span data-stu-id="1fda5-162">Adds a source node to the topology.</span></span> <span data-ttu-id="1fda5-163">此步驟的程式碼會顯示在 [建立來源節點](creating-source-nodes.md)的主題中。</span><span class="sxs-lookup"><span data-stu-id="1fda5-163">Code for this step is shown in the topic [Creating Source Nodes](creating-source-nodes.md).</span></span>
    3.  <span data-ttu-id="1fda5-164">將輸出節點新增至拓撲。</span><span class="sxs-lookup"><span data-stu-id="1fda5-164">Adds an output node to the topology.</span></span> <span data-ttu-id="1fda5-165">此步驟的程式碼會顯示在 [建立輸出節點](creating-output-nodes.md)的主題中。</span><span class="sxs-lookup"><span data-stu-id="1fda5-165">Code for this step is shown in the topic [Creating Output Nodes](creating-output-nodes.md).</span></span>
    4.  <span data-ttu-id="1fda5-166">藉由在來源節點上呼叫 [**IMFTopologyNode：： ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) 來連接兩個節點。</span><span class="sxs-lookup"><span data-stu-id="1fda5-166">Connects the two nodes by calling [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) on the source node.</span></span> <span data-ttu-id="1fda5-167">藉由連接節點，應用程式會指出上游節點應將資料傳遞至下游節點。</span><span class="sxs-lookup"><span data-stu-id="1fda5-167">By connecting the nodes, the application indicates that the upstream node should deliver data to the downstream node.</span></span> <span data-ttu-id="1fda5-168">來源節點有一個輸出，而輸出節點有一個輸入，因此兩個數據流索引都是零。</span><span class="sxs-lookup"><span data-stu-id="1fda5-168">A source node has one output, and an output node has one input, so both stream indexes are zero.</span></span>

<span data-ttu-id="1fda5-169">更先進的應用程式可以選取或取消選取資料流程，而不是使用來源的預設設定。</span><span class="sxs-lookup"><span data-stu-id="1fda5-169">More advanced applications can select or deselect streams, instead of using the source's default configuration.</span></span> <span data-ttu-id="1fda5-170">來源可能有多個資料流程，預設可能會選取其中任何一個。</span><span class="sxs-lookup"><span data-stu-id="1fda5-170">A source could have multiple streams, and any of them might be selected by default.</span></span> <span data-ttu-id="1fda5-171">媒體來源的簡報描述項具有一組預設的資料流程選取專案。</span><span class="sxs-lookup"><span data-stu-id="1fda5-171">The media source's presentation descriptor has a default set of stream selections.</span></span> <span data-ttu-id="1fda5-172">在具有單一音訊串流和影片串流的簡單影片檔案中，媒體來源預設通常會選取這兩個數據流。</span><span class="sxs-lookup"><span data-stu-id="1fda5-172">In a simple video file with a single audio stream and video stream, the media source will usually select both streams by default.</span></span> <span data-ttu-id="1fda5-173">不過，檔案可能會有不同語言的多個音訊串流，或以不同的位元速率編碼的多個影片串流。</span><span class="sxs-lookup"><span data-stu-id="1fda5-173">However, a file might have multiple audio streams for different languages, or multiple video streams encoded at different bit rates.</span></span> <span data-ttu-id="1fda5-174">在此情況下，部分資料流程預設會取消選取。</span><span class="sxs-lookup"><span data-stu-id="1fda5-174">In that case, some of the streams will be unselected by default.</span></span> <span data-ttu-id="1fda5-175">應用程式可以藉由在展示描述項上呼叫 [**IMFPresentationDescriptor：： SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) 和 [**IMFPresentationDescriptor：:D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) 來變更選取專案。</span><span class="sxs-lookup"><span data-stu-id="1fda5-175">The application can change the selection by calling [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) and [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) on the presentation descriptor.</span></span>

## <a name="creating-the-media-sink"></a><span data-ttu-id="1fda5-176">建立媒體接收器</span><span class="sxs-lookup"><span data-stu-id="1fda5-176">Creating the Media Sink</span></span>

<span data-ttu-id="1fda5-177">下一個函數會建立 EVR 或 SAR 媒體接收器的啟用物件。</span><span class="sxs-lookup"><span data-stu-id="1fda5-177">The next function creates an activation object for the EVR or SAR media sink.</span></span>


```C++
//  Create an activation object for a renderer, based on the stream media type.

HRESULT CreateMediaSinkActivate(
    IMFStreamDescriptor *pSourceSD,     // Pointer to the stream descriptor.
    HWND hVideoWindow,                  // Handle to the video clipping window.
    IMFActivate **ppActivate
)
{
    IMFMediaTypeHandler *pHandler = NULL;
    IMFActivate *pActivate = NULL;

    // Get the media type handler for the stream.
    HRESULT hr = pSourceSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the major media type.
    GUID guidMajorType;
    hr = pHandler->GetMajorType(&guidMajorType);
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Create an IMFActivate object for the renderer, based on the media type.
    if (MFMediaType_Audio == guidMajorType)
    {
        // Create the audio renderer.
        hr = MFCreateAudioRendererActivate(&pActivate);
    }
    else if (MFMediaType_Video == guidMajorType)
    {
        // Create the video renderer.
        hr = MFCreateVideoRendererActivate(hVideoWindow, &pActivate);
    }
    else
    {
        // Unknown stream type. 
        hr = E_FAIL;
        // Optionally, you could deselect this stream instead of failing.
    }
    if (FAILED(hr))
    {
        goto done;
    }
 
    // Return IMFActivate pointer to caller.
    *ppActivate = pActivate;
    (*ppActivate)->AddRef();

done:
    SafeRelease(&pHandler);
    SafeRelease(&pActivate);
    return hr;
}
```



<span data-ttu-id="1fda5-178">此函式會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="1fda5-178">This function performs the following steps:</span></span>

1.  <span data-ttu-id="1fda5-179">在資料流程描述項上呼叫 [**IMFStreamDescriptor：： GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) 。</span><span class="sxs-lookup"><span data-stu-id="1fda5-179">Calls [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span> <span data-ttu-id="1fda5-180">這個方法會傳回 [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="1fda5-180">This method returns an [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface pointer.</span></span>

2.  <span data-ttu-id="1fda5-181">呼叫 [**IMFMediaTypeHandler：： GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype)。</span><span class="sxs-lookup"><span data-stu-id="1fda5-181">Calls [**IMFMediaTypeHandler::GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span></span> <span data-ttu-id="1fda5-182">這個方法會傳回資料流程的主要類型 GUID。</span><span class="sxs-lookup"><span data-stu-id="1fda5-182">This method returns the major type GUID for the stream.</span></span>

3.  <span data-ttu-id="1fda5-183">如果資料流程類型為音訊，則函式會呼叫 [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) 來建立音訊轉譯器啟用物件。</span><span class="sxs-lookup"><span data-stu-id="1fda5-183">If the stream type is audio, the function calls [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) to create the audio renderer activation object.</span></span> <span data-ttu-id="1fda5-184">如果串流類型是 video，則函式會呼叫 [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) 來建立影片轉譯器啟用物件。</span><span class="sxs-lookup"><span data-stu-id="1fda5-184">If the stream type is video, the function calls [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the video renderer activation object.</span></span> <span data-ttu-id="1fda5-185">這兩個函數都會傳回 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="1fda5-185">Both of these functions return a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="1fda5-186">此指標可用來初始化接收的輸出節點，如先前所示。</span><span class="sxs-lookup"><span data-stu-id="1fda5-186">This pointer is used to initialize the output node for the sink, as shown previously.</span></span>

<span data-ttu-id="1fda5-187">針對任何其他資料流程類型，此範例會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1fda5-187">For any other stream type, this example returns an error code.</span></span> <span data-ttu-id="1fda5-188">或者，您也可以直接取消選取資料流程。</span><span class="sxs-lookup"><span data-stu-id="1fda5-188">Alternatively, you could simply deselect the stream.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1fda5-189">後續步驟</span><span class="sxs-lookup"><span data-stu-id="1fda5-189">Next Steps</span></span>

<span data-ttu-id="1fda5-190">若要一次播放一個媒體檔案，請呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)將拓撲排入媒體會話。</span><span class="sxs-lookup"><span data-stu-id="1fda5-190">To play one media file at a time, queue the topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span> <span data-ttu-id="1fda5-191">媒體會話將使用拓撲載入器來解析拓撲。</span><span class="sxs-lookup"><span data-stu-id="1fda5-191">The Media Session will use the topology loader to resolve the topology.</span></span> <span data-ttu-id="1fda5-192">如需完整範例，請參閱 [如何使用媒體基礎播放媒體](how-to-play-unprotected-media-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="1fda5-192">For a complete example, see [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fda5-193">相關主題</span><span class="sxs-lookup"><span data-stu-id="1fda5-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fda5-194">如何播放未受保護的媒體檔案</span><span class="sxs-lookup"><span data-stu-id="1fda5-194">How to Play Unprotected Media Files</span></span>](how-to-play-unprotected-media-files.md)
</dt> <dt>

[<span data-ttu-id="1fda5-195">媒體會話</span><span class="sxs-lookup"><span data-stu-id="1fda5-195">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="1fda5-196">拓撲</span><span class="sxs-lookup"><span data-stu-id="1fda5-196">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



