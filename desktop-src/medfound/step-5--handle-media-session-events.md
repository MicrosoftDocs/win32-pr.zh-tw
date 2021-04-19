---
description: 本主題是教學課程的步驟5，說明如何使用媒體基礎來播放媒體檔案。
ms.assetid: db9b896f-6f56-47b1-b129-331c984e0b16
title: 步驟5：處理媒體會話事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ea3092189644f800a5cb27d2e8b07744f5d90c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106992116"
---
# <a name="step-5-handle-media-session-events"></a>步驟5：處理媒體會話事件

本主題是教學課程的步驟5， [說明如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案。 完整的程式碼會顯示在「 [媒體會話播放」範例](media-session-playback-example.md)中。

如需本主題的背景資訊，請參閱 [媒體事件](media-event-generators.md)產生器。 本主題包含下列幾節：

-   [取得會話事件](#getting-session-events)
-   [MESessionTopologyStatus](#mesessiontopologystatus)
-   [MEEndOfPresentation](#meendofpresentation)
-   [MENewPresentation](#menewpresentation)
-   [相關主題](#related-topics)

## <a name="getting-session-events"></a>取得會話事件

為了從媒體會話取得事件，CPlayer 物件會呼叫 [**IMFMediaEventGenerator：： BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) 方法，如 [步驟4：建立媒體會話](step-4--create-the-media-session.md)所示。 這個方法是非同步，這表示它會立即返回呼叫端。 當下一個會話事件發生時，媒體會話會呼叫 CPlayer 物件的 [**IMFAsyncCallback：： Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法。

請務必 [**記住，叫**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 用會從背景工作執行緒呼叫，而不是從應用程式執行緒呼叫。 因此，叫用必須是多執行緒 **安全的。** 其中一個方法是使用重要區段保護成員資料。 不過，此 `CPlayer` 類別會顯示替代方法：

1.  在 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法中，CPlayer 物件會將 **WM 應用 \_ 程式 \_ 播放機 \_ 事件** 訊息張貼至應用程式。 Message 參數是 [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) 指標。
2.  應用程式會收到 **WM \_ 應用程式 \_ 播放機 \_ 事件** 訊息。
3.  應用程式會呼叫 `CPlayer::HandleEvent` 方法，並傳入 [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) 指標。
4.  `HandleEvent`方法會回應事件。

下列程式碼顯示 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法：


```C++
//  Callback for the asynchronous BeginGetEvent method.

HRESULT CPlayer::Invoke(IMFAsyncResult *pResult)
{
    MediaEventType meType = MEUnknown;  // Event type

    IMFMediaEvent *pEvent = NULL;

    // Get the event from the event queue.
    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the event type. 
    hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (meType == MESessionClosed)
    {
        // The session was closed. 
        // The application is waiting on the m_hCloseEvent event handle. 
        SetEvent(m_hCloseEvent);
    }
    else
    {
        // For all other events, get the next event in the queue.
        hr = m_pSession->BeginGetEvent(this, NULL);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Check the application state. 
        
    // If a call to IMFMediaSession::Close is pending, it means the 
    // application is waiting on the m_hCloseEvent event and
    // the application's message loop is blocked. 

    // Otherwise, post a private window message to the application. 

    if (m_state != Closing)
    {
        // Leave a reference count on the event.
        pEvent->AddRef();

        PostMessage(m_hwndEvent, WM_APP_PLAYER_EVENT, 
            (WPARAM)pEvent, (LPARAM)meType);
    }

done:
    SafeRelease(&pEvent);
    return S_OK;
}
```



[**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)方法會執行下列步驟：

1.  呼叫 [**IMFMediaEventGenerator：： EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) 以取得事件。 這個方法會傳回 [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) 介面的指標。
2.  呼叫 [**IMFMediaEvent：： GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) 以取得事件代碼。
3.  如果事件程式碼是 [MESessionClosed](mesessionclosed.md)，請呼叫 SetEvent 來設定 *m \_ hCloseEvent* 事件。 此步驟的原因會在 [步驟7：關機媒體會話](step-7--shut-down-the-media-session.md)，也會在程式碼批註中說明。
4.  若為所有其他事件碼，請呼叫 [**IMFMediaEventGenerator：： BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) 來要求下一個事件。
5.  將 **WM \_ 應用程式 \_ 播放機 \_ 事件** 訊息張貼至視窗。

下列程式碼顯示 HandleEvent 方法，此方法會在應用程式收到 WM 的 **\_ 應用程式 \_ 播放機 \_ 事件** 訊息時呼叫：


```C++
HRESULT CPlayer::HandleEvent(UINT_PTR pEventPtr)
{
    HRESULT hrStatus = S_OK;            
    MediaEventType meType = MEUnknown;  

    IMFMediaEvent *pEvent = (IMFMediaEvent*)pEventPtr;

    if (pEvent == NULL)
    {
        return E_POINTER;
    }

    // Get the event type.
    HRESULT hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the event status. If the operation that triggered the event 
    // did not succeed, the status is a failure code.
    hr = pEvent->GetStatus(&hrStatus);

    // Check if the async operation succeeded.
    if (SUCCEEDED(hr) && FAILED(hrStatus)) 
    {
        hr = hrStatus;
    }
    if (FAILED(hr))
    {
        goto done;
    }

    switch(meType)
    {
    case MESessionTopologyStatus:
        hr = OnTopologyStatus(pEvent);
        break;

    case MEEndOfPresentation:
        hr = OnPresentationEnded(pEvent);
        break;

    case MENewPresentation:
        hr = OnNewPresentation(pEvent);
        break;

    default:
        hr = OnSessionEvent(pEvent, meType);
        break;
    }

done:
    SafeRelease(&pEvent);
    return hr;
}
```



這個方法會呼叫 [**IMFMediaEvent：： GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) 來取得事件種類和 [**IMFMediaEvent：： GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) ，以取得與事件相關聯之失敗碼的成功。 下一個採取的動作取決於事件代碼。

## <a name="mesessiontopologystatus"></a>MESessionTopologyStatus

[MESessionTopologyStatus](mesessiontopologystatus.md)事件會通知拓撲狀態的變更。 事件物件的 [ [**MF \_ 事件 \_ 拓撲 \_ 狀態**](mf-event-topology-status-attribute.md) ] 屬性包含狀態。 在此範例中，唯一感興趣的值是 **MF \_ TOPOSTATUS \_ ready**，表示播放已準備好開始。


```C++
HRESULT CPlayer::OnTopologyStatus(IMFMediaEvent *pEvent)
{
    UINT32 status; 

    HRESULT hr = pEvent->GetUINT32(MF_EVENT_TOPOLOGY_STATUS, &status);
    if (SUCCEEDED(hr) && (status == MF_TOPOSTATUS_READY))
    {
        SafeRelease(&m_pVideoDisplay);

        // Get the IMFVideoDisplayControl interface from EVR. This call is
        // expected to fail if the media file does not have a video stream.

        (void)MFGetService(m_pSession, MR_VIDEO_RENDER_SERVICE, 
            IID_PPV_ARGS(&m_pVideoDisplay));

        hr = StartPlayback();
    }
    return hr;
}
```



`CPlayer::StartPlayback`方法會顯示在[步驟6：控制項播放](step-6--control-playback.md)中。

此範例也會呼叫 [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) ，以從 [增強的影片](enhanced-video-renderer.md)轉譯器取得 [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)介面 (EVR) 。 需要此介面，才能處理重新繪製和調整影片視窗的大小，也會顯示在 [步驟6：控制項播放](step-6--control-playback.md)中。

## <a name="meendofpresentation"></a>MEEndOfPresentation

[MEEndOfPresentation](meendofpresentation.md)事件表示播放已到達檔案結尾。 媒體會話會自動切換回 [已停止] 狀態。


```C++
//  Handler for MEEndOfPresentation event.
HRESULT CPlayer::OnPresentationEnded(IMFMediaEvent *pEvent)
{
    // The session puts itself into the stopped state automatically.
    m_state = Stopped;
    return S_OK;
}
```



## <a name="menewpresentation"></a>MENewPresentation

[MENewPresentation](menewpresentation.md)事件會對新簡報的開頭髮出信號。 事件資料是新簡報的 [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) 指標。

在許多情況下，您完全不會收到此事件。 如果您這樣做，請使用 [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) 指標來建立新的播放拓撲，如 [步驟3：開啟媒體](step-3--open-a-media-file.md)檔案所示。 然後將新拓撲排入媒體會話。


```C++
//  Handler for MENewPresentation event.
//
//  This event is sent if the media source has a new presentation, which 
//  requires a new topology. 

HRESULT CPlayer::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFTopology *pTopology = NULL;

    // Get the presentation descriptor from the event.
    HRESULT hr = GetEventObject(pEvent, &pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pPD,  m_hwndVideo,&pTopology);
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

done:
    SafeRelease(&pTopology);
    SafeRelease(&pPD);
    return S_OK;
}
```



下一 [步：步驟6：控制播放](step-6--control-playback.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊/視訊播放](audio-video-playback.md)
</dt> <dt>

[如何使用媒體基礎播放媒體檔案](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



