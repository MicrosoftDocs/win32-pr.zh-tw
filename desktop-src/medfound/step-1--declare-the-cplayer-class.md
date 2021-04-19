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
# <a name="step-1-declare-the-cplayer-class"></a><span data-ttu-id="48669-103">步驟1：宣告 CPlayer 類別</span><span class="sxs-lookup"><span data-stu-id="48669-103">Step 1: Declare the CPlayer Class</span></span>

<span data-ttu-id="48669-104">本主題是教學課程的步驟1， [說明如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="48669-104">This topic is step 1 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="48669-105">完整的程式碼會顯示在「 [媒體會話播放」範例](media-session-playback-example.md)中。</span><span class="sxs-lookup"><span data-stu-id="48669-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="48669-106">在本教學課程中，播放功能會封裝在 `CPlayer` 類別中。</span><span class="sxs-lookup"><span data-stu-id="48669-106">In this tutorial, playback functionality is encapsulated in the `CPlayer` class.</span></span> <span data-ttu-id="48669-107">`CPlayer` 類別的宣告方式如下：</span><span class="sxs-lookup"><span data-stu-id="48669-107">The `CPlayer` class is declared as follows:</span></span>


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



<span data-ttu-id="48669-108">以下是一些要注意的事項 `CPlayer` ：</span><span class="sxs-lookup"><span data-stu-id="48669-108">Here are some things to note about `CPlayer`:</span></span>

-   <span data-ttu-id="48669-109">常數的 **WM \_ 應用程式 \_ 播放機 \_ 事件** 會定義私用視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="48669-109">The constant **WM\_APP\_PLAYER\_EVENT** defines a private window message.</span></span> <span data-ttu-id="48669-110">此訊息是用來通知應用程式有關媒體會話事件。</span><span class="sxs-lookup"><span data-stu-id="48669-110">This message is used to notify the application about Media Session events.</span></span> <span data-ttu-id="48669-111">請參閱 [步驟5：處理媒體會話事件](step-5--handle-media-session-events.md)。</span><span class="sxs-lookup"><span data-stu-id="48669-111">See [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>
-   <span data-ttu-id="48669-112">`PlayerState`列舉會定義物件的可能狀態 `CPlayer` 。</span><span class="sxs-lookup"><span data-stu-id="48669-112">The `PlayerState` enumeration defines the possible states of the `CPlayer` object.</span></span>
-   <span data-ttu-id="48669-113">`CPlayer`類別會實 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)介面，用來從媒體會話取得事件通知。</span><span class="sxs-lookup"><span data-stu-id="48669-113">The `CPlayer` class implements the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface, which is used to get event notifications from the Media Session.</span></span>
-   <span data-ttu-id="48669-114">此為私用的函式 `CPlayer` 。</span><span class="sxs-lookup"><span data-stu-id="48669-114">The `CPlayer` constructor is private.</span></span> <span data-ttu-id="48669-115">應用程式會呼叫靜態 `CreateInstance` 方法來建立類別的實例 `CPlayer` 。</span><span class="sxs-lookup"><span data-stu-id="48669-115">The application calls the static `CreateInstance` method to create an instance of the `CPlayer` class.</span></span>
-   <span data-ttu-id="48669-116">此 `CPlayer` 函式也是私用的。</span><span class="sxs-lookup"><span data-stu-id="48669-116">The `CPlayer` destructor is also private.</span></span> <span data-ttu-id="48669-117">`CPlayer`類別會執行 **IUnknown**，因此物件的存留期會透過其參考計數來控制 (*m \_ nRefCount*) 。</span><span class="sxs-lookup"><span data-stu-id="48669-117">The `CPlayer` class implements **IUnknown**, so the object's lifetime is controlled through its reference count (*m\_nRefCount*).</span></span> <span data-ttu-id="48669-118">若要終結物件，應用程式會呼叫 **IUnknown：： Release**，而不是 **刪除**。</span><span class="sxs-lookup"><span data-stu-id="48669-118">To destroy the object, the application calls **IUnknown::Release**, not **delete**.</span></span>
-   <span data-ttu-id="48669-119">`CPlayer`物件會管理媒體會話和媒體來源。</span><span class="sxs-lookup"><span data-stu-id="48669-119">The `CPlayer` object manages both the Media Session and the media source.</span></span>

## <a name="implement-iunknown"></a><span data-ttu-id="48669-120">執行 IUnknown</span><span class="sxs-lookup"><span data-stu-id="48669-120">Implement IUnknown</span></span>

<span data-ttu-id="48669-121">`CPlayer`類別會實 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)，它會繼承 **IUnknown**。</span><span class="sxs-lookup"><span data-stu-id="48669-121">The `CPlayer` class implements [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback), which inherits **IUnknown**.</span></span>

<span data-ttu-id="48669-122">此處顯示的程式碼是相當標準的 **IUnknown** 執行。</span><span class="sxs-lookup"><span data-stu-id="48669-122">The code shown here is a fairly standard implementation of **IUnknown**.</span></span> <span data-ttu-id="48669-123">如果您想要的話，也可以使用 Active Template Library (ATL) 來執行這些方法。</span><span class="sxs-lookup"><span data-stu-id="48669-123">If you prefer, you can use the Active Template Library (ATL) to implement these methods.</span></span> <span data-ttu-id="48669-124">但是，不 `CPlayer` 支援 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 或任何 advanced COM 功能，因此在此使用 ATL 並沒有太好的理由。</span><span class="sxs-lookup"><span data-stu-id="48669-124">However, `CPlayer` does not support [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) or any advanced COM features, so there is no overwhelming reason to use ATL here.</span></span>


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



<span data-ttu-id="48669-125">下一 [步：步驟2：建立 CPlayer 物件](step-2--create-the-cplayer-object.md)</span><span class="sxs-lookup"><span data-stu-id="48669-125">Next: [Step 2: Create the CPlayer Object](step-2--create-the-cplayer-object.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="48669-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="48669-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48669-127">音訊/視訊播放</span><span class="sxs-lookup"><span data-stu-id="48669-127">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="48669-128">如何使用媒體基礎播放媒體檔案</span><span class="sxs-lookup"><span data-stu-id="48669-128">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
