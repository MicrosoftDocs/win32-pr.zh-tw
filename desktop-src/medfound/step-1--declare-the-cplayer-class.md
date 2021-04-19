---
description: 本主題是教學課程的步驟1，說明如何使用媒體基礎來播放媒體檔案。
ms.assetid: 10767bbf-3b47-4df1-be73-18678397c0ab
title: 步驟1：宣告 CPlayer 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1593842ecece68fcd3c4cca35a7e2e28eac503c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977200"
---
# <a name="step-1-declare-the-cplayer-class"></a>步驟1：宣告 CPlayer 類別

本主題是教學課程的步驟1， [說明如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案。 完整的程式碼會顯示在「 [媒體會話播放」範例](media-session-playback-example.md)中。

在本教學課程中，播放功能會封裝在 `CPlayer` 類別中。 `CPlayer` 類別的宣告方式如下：


```C++
const UINT WM_APP_PLAYER_EVENT = WM_APP + 1;   

    // WPARAM = IMFMediaEvent*, WPARAM = MediaEventType

enum PlayerState
{
    Closed = 0,     // No session.
    Ready,          // Session was created, ready to open a file. 
    OpenPending,    // Session is opening a file.
    Started,        // Session is playing a file.
    Paused,         // Session is paused.
    Stopped,        // Session is stopped (ready to play). 
    Closing         // Application has closed the session, but is waiting for MESessionClosed.
};

class CPlayer : public IMFAsyncCallback
{
public:
    static HRESULT CreateInstance(HWND hVideo, HWND hEvent, CPlayer **ppPlayer);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP  GetParameters(DWORD*, DWORD*)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP  Invoke(IMFAsyncResult* pAsyncResult);

    // Playback
    HRESULT       OpenURL(const WCHAR *sURL);
    HRESULT       Play();
    HRESULT       Pause();
    HRESULT       Stop();
    HRESULT       Shutdown();
    HRESULT       HandleEvent(UINT_PTR pUnkPtr);
    PlayerState   GetState() const { return m_state; }

    // Video functionality
    HRESULT       Repaint();
    HRESULT       ResizeVideo(WORD width, WORD height);
    
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }

protected:
    
    // Constructor is private. Use static CreateInstance method to instantiate.
    CPlayer(HWND hVideo, HWND hEvent);

    // Destructor is private. Caller should call Release.
    virtual ~CPlayer(); 

    HRESULT Initialize();
    HRESULT CreateSession();
    HRESULT CloseSession();
    HRESULT StartPlayback();

    // Media event handlers
    virtual HRESULT OnTopologyStatus(IMFMediaEvent *pEvent);
    virtual HRESULT OnPresentationEnded(IMFMediaEvent *pEvent);
    virtual HRESULT OnNewPresentation(IMFMediaEvent *pEvent);

    // Override to handle additional session events.
    virtual HRESULT OnSessionEvent(IMFMediaEvent*, MediaEventType) 
    { 
        return S_OK; 
    }

protected:
    long                    m_nRefCount;        // Reference count.

    IMFMediaSession         *m_pSession;
    IMFMediaSource          *m_pSource;
    IMFVideoDisplayControl  *m_pVideoDisplay;

    HWND                    m_hwndVideo;        // Video window.
    HWND                    m_hwndEvent;        // App window to receive events.
    PlayerState             m_state;            // Current state of the media session.
    HANDLE                  m_hCloseEvent;      // Event to wait on while closing.
};
```



以下是一些要注意的事項 `CPlayer` ：

-   常數的 **WM \_ 應用程式 \_ 播放機 \_ 事件** 會定義私用視窗訊息。 此訊息是用來通知應用程式有關媒體會話事件。 請參閱 [步驟5：處理媒體會話事件](step-5--handle-media-session-events.md)。
-   `PlayerState`列舉會定義物件的可能狀態 `CPlayer` 。
-   `CPlayer`類別會實 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)介面，用來從媒體會話取得事件通知。
-   此為私用的函式 `CPlayer` 。 應用程式會呼叫靜態 `CreateInstance` 方法來建立類別的實例 `CPlayer` 。
-   此 `CPlayer` 函式也是私用的。 `CPlayer`類別會執行 **IUnknown**，因此物件的存留期會透過其參考計數來控制 (*m \_ nRefCount*) 。 若要終結物件，應用程式會呼叫 **IUnknown：： Release**，而不是 **刪除**。
-   `CPlayer`物件會管理媒體會話和媒體來源。

## <a name="implement-iunknown"></a>執行 IUnknown

`CPlayer`類別會實 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)，它會繼承 **IUnknown**。

此處顯示的程式碼是相當標準的 **IUnknown** 執行。 如果您想要的話，也可以使用 Active Template Library (ATL) 來執行這些方法。 但是，不 `CPlayer` 支援 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 或任何 advanced COM 功能，因此在此使用 ATL 並沒有太好的理由。


```C++
HRESULT CPlayer::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CPlayer, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

ULONG CPlayer::AddRef()
{
    return InterlockedIncrement(&m_nRefCount);
}

ULONG CPlayer::Release()
{
    ULONG uCount = InterlockedDecrement(&m_nRefCount);
    if (uCount == 0)
    {
        delete this;
    }
    return uCount;
}
```



下一 [步：步驟2：建立 CPlayer 物件](step-2--create-the-cplayer-object.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊/視訊播放](audio-video-playback.md)
</dt> <dt>

[如何使用媒體基礎播放媒體檔案](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
