---
description: 本主題是教學課程的步驟3，說明如何使用媒體基礎來播放媒體檔案。
ms.assetid: cc0d2b60-64d7-49f3-844f-97487cab8466
title: 步驟3：開啟媒體檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b50f036b84806f96e4349f77a3f06e02e08764
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104027670"
---
# <a name="step-3-open-a-media-file"></a><span data-ttu-id="9f56f-103">步驟3：開啟媒體檔案</span><span class="sxs-lookup"><span data-stu-id="9f56f-103">Step 3: Open a Media File</span></span>

<span data-ttu-id="9f56f-104">本主題是教學課程的步驟3， [說明如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="9f56f-104">This topic is step 3 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="9f56f-105">完整的程式碼會顯示在「 [媒體會話播放」範例](media-session-playback-example.md)中。</span><span class="sxs-lookup"><span data-stu-id="9f56f-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="9f56f-106">`CPlayer::OpenURL`方法會從 URL 開啟媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="9f56f-106">The `CPlayer::OpenURL` method opens a media file from a URL.</span></span>


```C++
//  Open a URL for playback.
HRESULT CPlayer::OpenURL(const WCHAR *sURL)
{
    // 1. Create a new media session.
    // 2. Create the media source.
    // 3. Create the topology.
    // 4. Queue the topology [asynchronous]
    // 5. Start playback [asynchronous - does not happen in this method.]

    IMFTopology *pTopology = NULL;
    IMFPresentationDescriptor* pSourcePD = NULL;

    // Create the media session.
    HRESULT hr = CreateSession();
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the media source.
    hr = CreateMediaSource(sURL, &m_pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the presentation descriptor for the media source.
    hr = m_pSource->CreatePresentationDescriptor(&pSourcePD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pSourcePD, m_hwndVideo, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the topology on the media session.
    hr = m_pSession->SetTopology(0, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = OpenPending;

    // If SetTopology succeeds, the media session will queue an 
    // MESessionTopologySet event.

done:
    if (FAILED(hr))
    {
        m_state = Closed;
    }

    SafeRelease(&pSourcePD);
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="9f56f-107">這個方法會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="9f56f-107">This method performs the following steps:</span></span>

1.  <span data-ttu-id="9f56f-108">呼叫 **CPlayer：： CreateSession** 來建立媒體會話的新實例。</span><span class="sxs-lookup"><span data-stu-id="9f56f-108">Calls **CPlayer::CreateSession** to create a new instance of the Media Session.</span></span> <span data-ttu-id="9f56f-109">請參閱 [步驟4：建立媒體會話](step-4--create-the-media-session.md)。</span><span class="sxs-lookup"><span data-stu-id="9f56f-109">See [Step 4: Create the Media Session](step-4--create-the-media-session.md).</span></span>
2.  <span data-ttu-id="9f56f-110">從 URL 建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="9f56f-110">Creates a media source from the URL.</span></span> <span data-ttu-id="9f56f-111">此步驟的完整程式碼會顯示在 [使用來源解析程式](using-the-source-resolver.md)的主題中。</span><span class="sxs-lookup"><span data-stu-id="9f56f-111">The complete code for this step is shown in the topic [Using the Source Resolver](using-the-source-resolver.md).</span></span>
3.  <span data-ttu-id="9f56f-112">呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) 來取得媒體來源的展示描述項。</span><span class="sxs-lookup"><span data-stu-id="9f56f-112">Calls [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to get the media source's presentation descriptor.</span></span> <span data-ttu-id="9f56f-113">展示描述項描述來源檔案中的每個資料流程。</span><span class="sxs-lookup"><span data-stu-id="9f56f-113">The presentation descriptor describes each streams in the source file.</span></span>
4.  <span data-ttu-id="9f56f-114">建立播放拓撲。</span><span class="sxs-lookup"><span data-stu-id="9f56f-114">Creates the playback topology.</span></span> <span data-ttu-id="9f56f-115">此步驟的程式碼會顯示在 [建立播放拓撲](creating-playback-topologies.md)的主題中。</span><span class="sxs-lookup"><span data-stu-id="9f56f-115">Code for this step is shown in the topic [Creating Playback Topologies](creating-playback-topologies.md).</span></span>
5.  <span data-ttu-id="9f56f-116">呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) 來設定媒體會話上的拓撲。</span><span class="sxs-lookup"><span data-stu-id="9f56f-116">Calls [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>

<span data-ttu-id="9f56f-117">[**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)方法會以非同步方式完成。</span><span class="sxs-lookup"><span data-stu-id="9f56f-117">The [**SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method completes asynchronously.</span></span> <span data-ttu-id="9f56f-118">完成時，會呼叫 CPlayer 物件的 [**IMFAsyncCallback：： Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法;請參閱 [步驟5：處理媒體會話事件](step-5--handle-media-session-events.md)。</span><span class="sxs-lookup"><span data-stu-id="9f56f-118">When it completes, the CPlayer object's [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method is called; see [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>

<span data-ttu-id="9f56f-119">下一 [步：步驟4：建立媒體會話](step-4--create-the-media-session.md)</span><span class="sxs-lookup"><span data-stu-id="9f56f-119">Next: [Step 4: Create the Media Session](step-4--create-the-media-session.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f56f-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="9f56f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f56f-121">音訊/視訊播放</span><span class="sxs-lookup"><span data-stu-id="9f56f-121">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="9f56f-122">如何使用媒體基礎播放媒體檔案</span><span class="sxs-lookup"><span data-stu-id="9f56f-122">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



