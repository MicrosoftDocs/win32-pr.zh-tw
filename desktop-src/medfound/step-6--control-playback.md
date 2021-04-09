---
description: 本主題是教學課程的步驟6，說明如何使用媒體基礎來播放媒體檔案。
ms.assetid: e2e3e95b-41b2-45fb-b495-0e700220e5f5
title: 步驟6：控制播放
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdfecea3484ac6b06cc44e23fd3bd1b3235324e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848437"
---
# <a name="step-6-control-playback"></a><span data-ttu-id="1e71f-103">步驟6：控制播放</span><span class="sxs-lookup"><span data-stu-id="1e71f-103">Step 6: Control Playback</span></span>

<span data-ttu-id="1e71f-104">本主題是教學課程的步驟6， [說明如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="1e71f-104">This topic is step 6 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="1e71f-105">完整的程式碼會顯示在「 [媒體會話播放」範例](media-session-playback-example.md)中。</span><span class="sxs-lookup"><span data-stu-id="1e71f-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="1e71f-106">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="1e71f-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="1e71f-107">開始播放</span><span class="sxs-lookup"><span data-stu-id="1e71f-107">Starting Playback</span></span>](#starting-playback)
-   [<span data-ttu-id="1e71f-108">暫停播放</span><span class="sxs-lookup"><span data-stu-id="1e71f-108">Pausing Playback</span></span>](#pausing-playback)
-   [<span data-ttu-id="1e71f-109">停止播放</span><span class="sxs-lookup"><span data-stu-id="1e71f-109">Stopping Playback</span></span>](#stopping-playback)
-   [<span data-ttu-id="1e71f-110">重新繪製影片視窗</span><span class="sxs-lookup"><span data-stu-id="1e71f-110">Repainting the Video Window</span></span>](#repainting-the-video-window)
-   [<span data-ttu-id="1e71f-111">調整影片視窗的大小</span><span class="sxs-lookup"><span data-stu-id="1e71f-111">Resizing the Video Window</span></span>](#resizing-the-video-window)
-   [<span data-ttu-id="1e71f-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="1e71f-112">Related topics</span></span>](#related-topics)

## <a name="starting-playback"></a><span data-ttu-id="1e71f-113">開始播放</span><span class="sxs-lookup"><span data-stu-id="1e71f-113">Starting Playback</span></span>

<span data-ttu-id="1e71f-114">若要開始播放，請呼叫 [**IMFMediaSession：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)。</span><span class="sxs-lookup"><span data-stu-id="1e71f-114">To start playback, call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="1e71f-115">下列程式碼說明如何從目前的播放位置開始。</span><span class="sxs-lookup"><span data-stu-id="1e71f-115">The following code shows how to start from the current playback position.</span></span>


```C++
//  Start playback from the current position. 
HRESULT CPlayer::StartPlayback()
{
    assert(m_pSession != NULL);

    PROPVARIANT varStart;
    PropVariantInit(&varStart);

    HRESULT hr = m_pSession->Start(&GUID_NULL, &varStart);
    if (SUCCEEDED(hr))
    {
        // Note: Start is an asynchronous operation. However, we
        // can treat our state as being already started. If Start
        // fails later, we'll get an MESessionStarted event with
        // an error code, and we will update our state then.
        m_state = Started;
    }
    PropVariantClear(&varStart);
    return hr;
}

//  Start playback from paused or stopped.
HRESULT CPlayer::Play()
{
    if (m_state != Paused && m_state != Stopped)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL || m_pSource == NULL)
    {
        return E_UNEXPECTED;
    }
    return StartPlayback();
}

```



<span data-ttu-id="1e71f-116">[**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)方法也可以指定相對於檔案開頭的起始位置;如需詳細資訊，請參閱 API 參考主題。</span><span class="sxs-lookup"><span data-stu-id="1e71f-116">The [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method can also specify a starting position relative to the start of the file; see the API reference topic for more information.</span></span>

## <a name="pausing-playback"></a><span data-ttu-id="1e71f-117">暫停播放</span><span class="sxs-lookup"><span data-stu-id="1e71f-117">Pausing Playback</span></span>

<span data-ttu-id="1e71f-118">若要暫停播放，請呼叫 [**IMFMediaSession：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)。</span><span class="sxs-lookup"><span data-stu-id="1e71f-118">To pause playback, call [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).</span></span>


```C++
//  Pause playback.
HRESULT CPlayer::Pause()    
{
    if (m_state != Started)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL || m_pSource == NULL)
    {
        return E_UNEXPECTED;
    }

    HRESULT hr = m_pSession->Pause();
    if (SUCCEEDED(hr))
    {
        m_state = Paused;
    }

    return hr;
}
```



## <a name="stopping-playback"></a><span data-ttu-id="1e71f-119">停止播放</span><span class="sxs-lookup"><span data-stu-id="1e71f-119">Stopping Playback</span></span>

<span data-ttu-id="1e71f-120">若要停止播放，請呼叫 [**IMFMediaSession：： stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)。</span><span class="sxs-lookup"><span data-stu-id="1e71f-120">To stop playback, call [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span> <span data-ttu-id="1e71f-121">在停止播放時，會清除影片影像，並根據預設 (黑色的背景色彩繪製影片視窗) 。</span><span class="sxs-lookup"><span data-stu-id="1e71f-121">While playback is stopped, the video image is cleared and the video window is painted with the background color (black by default).</span></span>


```C++
// Stop playback.
HRESULT CPlayer::Stop()
{
    if (m_state != Started && m_state != Paused)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL)
    {
        return E_UNEXPECTED;
    }

    HRESULT hr = m_pSession->Stop();
    if (SUCCEEDED(hr))
    {
        m_state = Stopped;
    }
    return hr;
}
```



## <a name="repainting-the-video-window"></a><span data-ttu-id="1e71f-122">重新繪製影片視窗</span><span class="sxs-lookup"><span data-stu-id="1e71f-122">Repainting the Video Window</span></span>

<span data-ttu-id="1e71f-123">[增強型影片](enhanced-video-renderer.md)轉譯器 (EVR) 會在應用程式所指定的視窗中繪製影片。</span><span class="sxs-lookup"><span data-stu-id="1e71f-123">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) draws the video in the window specified by the application.</span></span> <span data-ttu-id="1e71f-124">這會發生在不同的執行緒上，而大部分的情況下，您的應用程式不需要管理此進程。</span><span class="sxs-lookup"><span data-stu-id="1e71f-124">This occurs on a separate thread, and for the most part, your application does not need to manage this process.</span></span> <span data-ttu-id="1e71f-125">但是，如果播放暫停或停止，則每當影片視窗收到 [**WM \_ 油漆**](../gdi/wm-paint.md) 訊息時，就必須通知 EVR。</span><span class="sxs-lookup"><span data-stu-id="1e71f-125">If playback is paused or stopped, however, the EVR must be notified whenever the video window receives a [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span> <span data-ttu-id="1e71f-126">這可讓 EVR 重新繪製視窗。</span><span class="sxs-lookup"><span data-stu-id="1e71f-126">This allows the EVR to repaint the window.</span></span> <span data-ttu-id="1e71f-127">若要通知 EVR，請呼叫 [**IMFVideoDisplayControl：： RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) 方法：</span><span class="sxs-lookup"><span data-stu-id="1e71f-127">To notify the EVR, call the [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) method:</span></span>


```C++
//  Repaint the video window. Call this method on WM_PAINT.

HRESULT CPlayer::Repaint()
{
    if (m_pVideoDisplay)
    {
        return m_pVideoDisplay->RepaintVideo();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="1e71f-128">下列程式碼顯示了 [**WM \_ 油漆**](../gdi/wm-paint.md) 訊息的處理常式。</span><span class="sxs-lookup"><span data-stu-id="1e71f-128">The following code shows the handler for the [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span> <span data-ttu-id="1e71f-129">您應該從應用程式的訊息迴圈呼叫這個函式。</span><span class="sxs-lookup"><span data-stu-id="1e71f-129">This function should be called from the application's message loop.</span></span>


```C++
//  Handler for WM_PAINT messages.
void OnPaint(HWND hwnd)
{
    PAINTSTRUCT ps;
    HDC hdc = BeginPaint(hwnd, &ps);

    if (g_pPlayer && g_pPlayer->HasVideo())
    {
        // Video is playing. Ask the player to repaint.
        g_pPlayer->Repaint();
    }
    else
    {
        // The video is not playing, so we must paint the application window.
        RECT rc;
        GetClientRect(hwnd, &rc);
        FillRect(hdc, &rc, (HBRUSH) COLOR_WINDOW);
    }
    EndPaint(hwnd, &ps);
}
```



<span data-ttu-id="1e71f-130">`HasVideo`如果 `CPlayer` 物件具有有效的 [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)指標，此方法會傳回 TRUE。</span><span class="sxs-lookup"><span data-stu-id="1e71f-130">The `HasVideo` method returns **TRUE** if the `CPlayer` object has a valid [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) pointer.</span></span> <span data-ttu-id="1e71f-131"> (請參閱 [步驟1：宣告 CPlayer 類別](step-1--declare-the-cplayer-class.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="1e71f-131">(See [Step 1: Declare the CPlayer Class](step-1--declare-the-cplayer-class.md).)</span></span>


```C++
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }
```



## <a name="resizing-the-video-window"></a><span data-ttu-id="1e71f-132">調整影片視窗的大小</span><span class="sxs-lookup"><span data-stu-id="1e71f-132">Resizing the Video Window</span></span>

<span data-ttu-id="1e71f-133">如果您調整影片視窗的大小，請呼叫 [**IMFVideoDisplayControl：： SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) 方法，以更新 EVR 上的目的地矩形：</span><span class="sxs-lookup"><span data-stu-id="1e71f-133">If you resize the video window, update the destination rectangle on the EVR by calling the [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) method:</span></span>


```C++
//  Resize the video rectangle.
//
//  Call this method if the size of the video window changes.

HRESULT CPlayer::ResizeVideo(WORD width, WORD height)
{
    if (m_pVideoDisplay)
    {
        // Set the destination rectangle.
        // Leave the default source rectangle (0,0,1,1).

        RECT rcDest = { 0, 0, width, height };

        return m_pVideoDisplay->SetVideoPosition(NULL, &rcDest);
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="1e71f-134">下一 [步：步驟7：關機媒體會話](step-7--shut-down-the-media-session.md)</span><span class="sxs-lookup"><span data-stu-id="1e71f-134">Next: [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e71f-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="1e71f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e71f-136">音訊/視訊播放</span><span class="sxs-lookup"><span data-stu-id="1e71f-136">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="1e71f-137">如何使用媒體基礎播放媒體檔案</span><span class="sxs-lookup"><span data-stu-id="1e71f-137">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
