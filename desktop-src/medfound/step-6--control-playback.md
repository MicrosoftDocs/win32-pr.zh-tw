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
# <a name="step-6-control-playback"></a>步驟6：控制播放

本主題是教學課程的步驟6， [說明如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案。 完整的程式碼會顯示在「 [媒體會話播放」範例](media-session-playback-example.md)中。

本主題包含下列幾節：

-   [開始播放](#starting-playback)
-   [暫停播放](#pausing-playback)
-   [停止播放](#stopping-playback)
-   [重新繪製影片視窗](#repainting-the-video-window)
-   [調整影片視窗的大小](#resizing-the-video-window)
-   [相關主題](#related-topics)

## <a name="starting-playback"></a>開始播放

若要開始播放，請呼叫 [**IMFMediaSession：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)。 下列程式碼說明如何從目前的播放位置開始。


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



[**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)方法也可以指定相對於檔案開頭的起始位置;如需詳細資訊，請參閱 API 參考主題。

## <a name="pausing-playback"></a>暫停播放

若要暫停播放，請呼叫 [**IMFMediaSession：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)。


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



## <a name="stopping-playback"></a>停止播放

若要停止播放，請呼叫 [**IMFMediaSession：： stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)。 在停止播放時，會清除影片影像，並根據預設 (黑色的背景色彩繪製影片視窗) 。


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



## <a name="repainting-the-video-window"></a>重新繪製影片視窗

[增強型影片](enhanced-video-renderer.md)轉譯器 (EVR) 會在應用程式所指定的視窗中繪製影片。 這會發生在不同的執行緒上，而大部分的情況下，您的應用程式不需要管理此進程。 但是，如果播放暫停或停止，則每當影片視窗收到 [**WM \_ 油漆**](../gdi/wm-paint.md) 訊息時，就必須通知 EVR。 這可讓 EVR 重新繪製視窗。 若要通知 EVR，請呼叫 [**IMFVideoDisplayControl：： RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) 方法：


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



下列程式碼顯示了 [**WM \_ 油漆**](../gdi/wm-paint.md) 訊息的處理常式。 您應該從應用程式的訊息迴圈呼叫這個函式。


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



`HasVideo`如果 `CPlayer` 物件具有有效的 [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)指標，此方法會傳回 TRUE。  (請參閱 [步驟1：宣告 CPlayer 類別](step-1--declare-the-cplayer-class.md)。 ) 


```C++
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }
```



## <a name="resizing-the-video-window"></a>調整影片視窗的大小

如果您調整影片視窗的大小，請呼叫 [**IMFVideoDisplayControl：： SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) 方法，以更新 EVR 上的目的地矩形：


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



下一 [步：步驟7：關機媒體會話](step-7--shut-down-the-media-session.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊/視訊播放](audio-video-playback.md)
</dt> <dt>

[如何使用媒體基礎播放媒體檔案](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
