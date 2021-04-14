---
description: 本主題是教學課程的步驟7，說明如何使用媒體基礎來播放媒體檔案。
ms.assetid: c31444df-8717-4ca8-a9ec-72cbb0ee4125
title: 步驟7：關機媒體會話
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9fd11cde51b06d932b212f4effabf315deecb7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104116072"
---
# <a name="step-7-shut-down-the-media-session"></a><span data-ttu-id="f4cdb-103">步驟7：關機媒體會話</span><span class="sxs-lookup"><span data-stu-id="f4cdb-103">Step 7: Shut Down the Media Session</span></span>

<span data-ttu-id="f4cdb-104">本主題是教學課程的步驟7， [說明如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="f4cdb-104">This topic is step 7 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="f4cdb-105">完整的程式碼會顯示在「 [媒體會話播放」範例](media-session-playback-example.md)中。</span><span class="sxs-lookup"><span data-stu-id="f4cdb-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="f4cdb-106">若要關閉 [媒體會話](media-session.md)，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="f4cdb-106">To shut down the [Media Session](media-session.md), perform the following steps:</span></span>

1.  <span data-ttu-id="f4cdb-107">呼叫 [**IMFMediaSession：： close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) 以關閉目前的簡報。</span><span class="sxs-lookup"><span data-stu-id="f4cdb-107">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the current presentation.</span></span>
2.  <span data-ttu-id="f4cdb-108">等候 [MESessionClosed](mesessionclosed.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="f4cdb-108">Wait for the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="f4cdb-109">此事件保證是媒體會話中的最後一個事件。</span><span class="sxs-lookup"><span data-stu-id="f4cdb-109">This event is guaranteed to be the last event from the Media Session.</span></span>
3.  <span data-ttu-id="f4cdb-110">呼叫 [**IMFMediaSession：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)。</span><span class="sxs-lookup"><span data-stu-id="f4cdb-110">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="f4cdb-111">這個方法會讓媒體會話釋放資源。</span><span class="sxs-lookup"><span data-stu-id="f4cdb-111">This method causes the Media Sessions to release resources.</span></span>
4.  <span data-ttu-id="f4cdb-112">在目前的媒體來源上呼叫 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) 。</span><span class="sxs-lookup"><span data-stu-id="f4cdb-112">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the current media source.</span></span>

<span data-ttu-id="f4cdb-113">下列方法會關閉媒體會話。</span><span class="sxs-lookup"><span data-stu-id="f4cdb-113">The following method shuts down the Media Session.</span></span> <span data-ttu-id="f4cdb-114">它會使用事件控制碼 (*m \_ hCloseEvent*) 等候 [MESessionClosed](mesessionclosed.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="f4cdb-114">It uses an event handle (*m\_hCloseEvent*) to wait for the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="f4cdb-115">請參閱 [步驟5：處理媒體會話事件](step-5--handle-media-session-events.md)。</span><span class="sxs-lookup"><span data-stu-id="f4cdb-115">See [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>


```C++
//  Close the media session. 
HRESULT CPlayer::CloseSession()
{
    //  The IMFMediaSession::Close method is asynchronous, but the 
    //  CPlayer::CloseSession method waits on the MESessionClosed event.
    //  
    //  MESessionClosed is guaranteed to be the last event that the 
    //  media session fires.

    HRESULT hr = S_OK;

    SafeRelease(&m_pVideoDisplay);

    // First close the media session.
    if (m_pSession)
    {
        DWORD dwWaitResult = 0;

        m_state = Closing;
           
        hr = m_pSession->Close();
        // Wait for the close operation to complete
        if (SUCCEEDED(hr))
        {
            dwWaitResult = WaitForSingleObject(m_hCloseEvent, 5000);
            if (dwWaitResult == WAIT_TIMEOUT)
            {
                assert(FALSE);
            }
            // Now there will be no more events from this session.
        }
    }

    // Complete shutdown operations.
    if (SUCCEEDED(hr))
    {
        // Shut down the media source. (Synchronous operation, no events.)
        if (m_pSource)
        {
            (void)m_pSource->Shutdown();
        }
        // Shut down the media session. (Synchronous operation, no events.)
        if (m_pSession)
        {
            (void)m_pSession->Shutdown();
        }
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pSession);
    m_state = Closed;
    return hr;
}
```



<span data-ttu-id="f4cdb-116">在應用程式結束之前，關閉媒體會話，然後呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) 來關閉 Microsoft 媒體基礎平臺。</span><span class="sxs-lookup"><span data-stu-id="f4cdb-116">Before the application exits, shut down the Media Session, and then call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Microsoft Media Foundation platform.</span></span>


```C++
//  Release all resources held by this object.
HRESULT CPlayer::Shutdown()
{
    // Close the session
    HRESULT hr = CloseSession();

    // Shutdown the Media Foundation platform
    MFShutdown();

    if (m_hCloseEvent)
    {
        CloseHandle(m_hCloseEvent);
        m_hCloseEvent = NULL;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="f4cdb-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="f4cdb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4cdb-118">音訊/視訊播放</span><span class="sxs-lookup"><span data-stu-id="f4cdb-118">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="f4cdb-119">如何使用媒體基礎播放媒體檔案</span><span class="sxs-lookup"><span data-stu-id="f4cdb-119">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



