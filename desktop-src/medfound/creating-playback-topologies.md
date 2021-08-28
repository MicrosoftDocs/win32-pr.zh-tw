---
description: 本主題說明如何建立音訊或影片播放的拓朴。
ms.assetid: 9c536c4e-fbf8-4c16-932f-e5863b7652fe
title: 建立播放拓撲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563fcef0c9ba8b1a4a33aefc17c5cea744f051470bb04df0ab4699ed4af6fa8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600818"
---
# <a name="creating-playback-topologies"></a>建立播放拓撲

本主題說明如何建立音訊或影片播放的拓朴。 針對基本播放，您可以建立部分拓撲，其中來源節點會直接連接至輸出節點。 您不需要為中繼轉換（例如，「解碼器」或「色彩轉換器」）插入任何節點。 媒體會話將使用拓撲載入器來解析拓撲，而拓撲載入器會插入所需的轉換。

-   [建立拓撲](#creating-the-topology)
-   [將資料流程連接到媒體接收器](#connecting-streams-to-media-sinks)
-   [建立媒體接收器](#creating-the-media-sink)
-   [後續步驟](#next-steps)
-   [相關主題](#related-topics)

## <a name="creating-the-topology"></a>建立拓撲

從媒體來源建立部分播放拓撲的整體步驟如下：

1.  建立媒體來源。 在大多數情況下，您將使用來源解析程式來建立媒體來源。 如需詳細資訊，請參閱 [來源解析程式](source-resolver.md)。
2.  取得媒體來源的展示描述項。
3.  建立空的拓撲。
4.  使用展示描述元來列舉資料流程描述項。 針對每個資料流程描述元：
    1.  取得資料流程的主要媒體類型，例如音訊或影片。
    2.  檢查目前是否已選取資料流程。  (選擇性地，您可以根據媒體類型來選取或取消選取資料流程。 ) 
    3.  如果已選取資料流程，請根據資料流程的媒體類型，建立媒體接收器的啟用物件。
    4.  新增資料流程的來源節點和媒體接收器的輸出節點。
    5.  連線來源節點加入至輸出節點。

為了讓此程式更容易遵循，本主題中的範例程式碼會分成數個函式。 最上層函數的名稱為 `CreatePlaybackTopology` 。 它會採用三個參數：

-   媒體來源之 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面的指標。
-   表示描述項之 [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) 介面的指標。 藉由呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)來取得此指標。 針對具有多個簡報的來源，後續簡報的呈現描述項會在 [MENewPresentation](menewpresentation.md) 事件中傳遞。
-   應用程式視窗的控制碼。 如果來源有影片串流，則影片會顯示在此視窗中。

函數會傳回 *ppTopology* 參數中部分播放拓撲的指標。


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



此函式會執行下列步驟：

1.  呼叫 [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology) 來建立拓撲。 一開始，拓撲不包含任何節點。
2.  呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) 來取得簡報中的資料流程數目。
3.  針對每個資料流程，將應用程式定義 `AddBranchToPartialTopology` 函數呼叫至拓撲中的分支。 下一節會顯示此函數。

## <a name="connecting-streams-to-media-sinks"></a>將資料流程連接到媒體接收器

針對每個選取的資料流程，新增來源節點和輸出節點，然後連接這兩個節點。 來源節點代表資料流程。 輸出節點代表 [增強型影片](enhanced-video-renderer.md) 轉譯器 (EVR) 或 [串流音訊](streaming-audio-renderer.md) 轉譯器 (SAR) 。

`AddBranchToPartialTopology`下一個範例所示的函式會採用下列參數：

-   拓撲之 [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) 介面的指標。
-   媒體來源之 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 介面的指標。
-   表示描述項之 [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) 介面的指標。
-   以零為基底的資料流程索引。
-   影片視窗的控制碼。 這個控制碼只適用于影片串流。


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



函數會執行下列動作：

1.  呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) ，並傳入資料流程索引。 這個方法會傳回該資料流程的資料流程描述元指標，以及指出是否已選取資料流程的布林值。
2.  如果未選取資料流程，則函式會結束並傳回 S \_ OK，因為應用程式不需要為數據流建立拓撲分支，除非已選取它。
3.  如果選取資料流程，則函式會完成拓撲分支，如下所示：
    1.  藉由呼叫應用程式定義的 CreateMediaSinkActivate 函式，建立接收的啟用物件。 下一節會顯示此函數。
    2.  將來源節點新增至拓撲。 此步驟的程式碼會顯示在 [建立來源節點](creating-source-nodes.md)的主題中。
    3.  將輸出節點新增至拓撲。 此步驟的程式碼會顯示在 [建立輸出節點](creating-output-nodes.md)的主題中。
    4.  藉由在來源節點上呼叫 [**IMFTopologyNode：： ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) 來連接兩個節點。 藉由連接節點，應用程式會指出上游節點應將資料傳遞至下游節點。 來源節點有一個輸出，而輸出節點有一個輸入，因此兩個數據流索引都是零。

更先進的應用程式可以選取或取消選取資料流程，而不是使用來源的預設設定。 來源可能有多個資料流程，預設可能會選取其中任何一個。 媒體來源的簡報描述項具有一組預設的資料流程選取專案。 在具有單一音訊串流和影片串流的簡單影片檔案中，媒體來源預設通常會選取這兩個數據流。 不過，檔案可能會有不同語言的多個音訊串流，或以不同的位元速率編碼的多個影片串流。 在此情況下，部分資料流程預設會取消選取。 應用程式可以藉由在展示描述項上呼叫 [**IMFPresentationDescriptor：： SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) 和 [**IMFPresentationDescriptor：:D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) 來變更選取專案。

## <a name="creating-the-media-sink"></a>建立媒體接收器

下一個函數會建立 EVR 或 SAR 媒體接收器的啟用物件。


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



此函式會執行下列步驟：

1.  在資料流程描述項上呼叫 [**IMFStreamDescriptor：： GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) 。 這個方法會傳回 [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) 介面指標。

2.  呼叫 [**IMFMediaTypeHandler：： GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype)。 這個方法會傳回資料流程的主要類型 GUID。

3.  如果資料流程類型為音訊，則函式會呼叫 [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) 來建立音訊轉譯器啟用物件。 如果串流類型是 video，則函式會呼叫 [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) 來建立影片轉譯器啟用物件。 這兩個函數都會傳回 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) 介面的指標。 此指標可用來初始化接收的輸出節點，如先前所示。

針對任何其他資料流程類型，此範例會傳回錯誤碼。 或者，您也可以直接取消選取資料流程。

## <a name="next-steps"></a>後續步驟

若要一次播放一個媒體檔案，請呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)將拓撲排入媒體會話。 媒體會話將使用拓撲載入器來解析拓撲。 如需完整範例，請參閱 [如何使用媒體基礎播放媒體](how-to-play-unprotected-media-files.md)檔案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何播放未受保護的媒體檔案](how-to-play-unprotected-media-files.md)
</dt> <dt>

[媒體會話](media-session.md)
</dt> <dt>

[拓撲](topologies.md)
</dt> </dl>

 

 



