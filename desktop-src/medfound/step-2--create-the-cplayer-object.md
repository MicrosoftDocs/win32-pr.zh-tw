---
description: 本主題是教學課程的步驟2，說明如何使用媒體基礎來播放媒體檔案。
ms.assetid: b489312f-ab8c-4ec6-8070-f5848034087e
title: 步驟2：建立 CPlayer 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021ffa383506c0ab1be8d6c1ca327f67ed8f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985619"
---
# <a name="step-2-create-the-cplayer-object"></a><span data-ttu-id="57ccb-103">步驟2：建立 CPlayer 物件</span><span class="sxs-lookup"><span data-stu-id="57ccb-103">Step 2: Create the CPlayer Object</span></span>

<span data-ttu-id="57ccb-104">本主題是教學課程的步驟2， [說明如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="57ccb-104">This topic is step 2 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="57ccb-105">完整的程式碼會顯示在「 [媒體會話播放」範例](media-session-playback-example.md)中。</span><span class="sxs-lookup"><span data-stu-id="57ccb-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="57ccb-106">若要建立類別的實例 `CPlayer` ，應用程式會呼叫靜態 `CPlayer::CreateInstance` 方法。</span><span class="sxs-lookup"><span data-stu-id="57ccb-106">To create an instance of the `CPlayer` class, the application calls the static `CPlayer::CreateInstance` method.</span></span> <span data-ttu-id="57ccb-107">這個方法會採用下列參數：</span><span class="sxs-lookup"><span data-stu-id="57ccb-107">This method takes the following parameters:</span></span>

-   <span data-ttu-id="57ccb-108">*hVideo* 會指定要顯示影片的視窗。</span><span class="sxs-lookup"><span data-stu-id="57ccb-108">*hVideo* specifies the window to display video.</span></span>
-   <span data-ttu-id="57ccb-109">*hEvent* 指定要接收事件的視窗。</span><span class="sxs-lookup"><span data-stu-id="57ccb-109">*hEvent* specifies a window to receive events.</span></span> <span data-ttu-id="57ccb-110">將相同的控制碼傳遞給兩個視窗控制碼是有效的。</span><span class="sxs-lookup"><span data-stu-id="57ccb-110">It is valid to pass the same handle for both window handles.</span></span>
-   <span data-ttu-id="57ccb-111">*ppPlayer* 會接收新實例的指標 `CPlayer` 。</span><span class="sxs-lookup"><span data-stu-id="57ccb-111">*ppPlayer* receives a pointer to a new `CPlayer` instance.</span></span>

<span data-ttu-id="57ccb-112">下列程式碼顯示 `CreateInstance` 方法：</span><span class="sxs-lookup"><span data-stu-id="57ccb-112">The following code shows the `CreateInstance` method:</span></span>


```C++
//  Static class method to create the CPlayer object.

HRESULT CPlayer::CreateInstance(
    HWND hVideo,                  // Video window.
    HWND hEvent,                  // Window to receive notifications.
    CPlayer **ppPlayer)           // Receives a pointer to the CPlayer object.
{
    if (ppPlayer == NULL)
    {
        return E_POINTER;
    }

    CPlayer *pPlayer = new (std::nothrow) CPlayer(hVideo, hEvent);
    if (pPlayer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pPlayer->Initialize();
    if (SUCCEEDED(hr))
    {
        *ppPlayer = pPlayer;
    }
    else
    {
        pPlayer->Release();
    }
    return hr;
}

HRESULT CPlayer::Initialize()
{
    // Start up Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        m_hCloseEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
        if (m_hCloseEvent == NULL)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }
    return hr;
}
```



<span data-ttu-id="57ccb-113">下列程式碼顯示此函式 `CPlayer` ：</span><span class="sxs-lookup"><span data-stu-id="57ccb-113">The following code shows the `CPlayer` constructor:</span></span>


```C++
CPlayer::CPlayer(HWND hVideo, HWND hEvent) : 
    m_pSession(NULL),
    m_pSource(NULL),
    m_pVideoDisplay(NULL),
    m_hwndVideo(hVideo),
    m_hwndEvent(hEvent),
    m_state(Closed),
    m_hCloseEvent(NULL),
    m_nRefCount(1)
{
}
```



<span data-ttu-id="57ccb-114">此函式會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="57ccb-114">The constructor does the following:</span></span>

1.  <span data-ttu-id="57ccb-115">呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 以初始化媒體基礎平臺。</span><span class="sxs-lookup"><span data-stu-id="57ccb-115">Calls [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize the Media Foundation platform.</span></span>
2.  <span data-ttu-id="57ccb-116">建立自動重設事件。</span><span class="sxs-lookup"><span data-stu-id="57ccb-116">Creates an auto-reset event.</span></span> <span data-ttu-id="57ccb-117">關閉媒體會話時，會使用此事件;請參閱 [步驟7：關機媒體會話](step-7--shut-down-the-media-session.md)。</span><span class="sxs-lookup"><span data-stu-id="57ccb-117">This event is used when closing the Media Session; see [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md).</span></span>

<span data-ttu-id="57ccb-118">此函式會關閉媒體會話，如 [步驟7：關機媒體會話](step-7--shut-down-the-media-session.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="57ccb-118">The destructor shuts down the Media Session, as described in [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md).</span></span>


```C++
CPlayer::~CPlayer()
{
    assert(m_pSession == NULL);  
    // If FALSE, the app did not call Shutdown().

    // When CPlayer calls IMediaEventGenerator::BeginGetEvent on the
    // media session, it causes the media session to hold a reference 
    // count on the CPlayer. 
    
    // This creates a circular reference count between CPlayer and the 
    // media session. Calling Shutdown breaks the circular reference 
    // count.

    // If CreateInstance fails, the application will not call 
    // Shutdown. To handle that case, call Shutdown in the destructor. 

    Shutdown();
}
```



<span data-ttu-id="57ccb-119">請注意，函式和函式都是受保護的類別方法。</span><span class="sxs-lookup"><span data-stu-id="57ccb-119">Note that the constructor and destructor are both protected class methods.</span></span> <span data-ttu-id="57ccb-120">應用程式會使用靜態方法來建立物件 `CreateInstance` 。</span><span class="sxs-lookup"><span data-stu-id="57ccb-120">The application creates the object using the static `CreateInstance` method.</span></span> <span data-ttu-id="57ccb-121">它會藉由呼叫 **IUnknown：： Release** 來終結物件，而不是明確地使用 **delete**。</span><span class="sxs-lookup"><span data-stu-id="57ccb-121">It destroys the object by calling **IUnknown::Release**, rather than explicitly using **delete**.</span></span>

<span data-ttu-id="57ccb-122">下一[步：步驟3：開啟媒體](step-3--open-a-media-file.md)檔案</span><span class="sxs-lookup"><span data-stu-id="57ccb-122">Next: [Step 3: Open a Media File](step-3--open-a-media-file.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="57ccb-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="57ccb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57ccb-124">音訊/視訊播放</span><span class="sxs-lookup"><span data-stu-id="57ccb-124">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="57ccb-125">如何使用媒體基礎播放媒體檔案</span><span class="sxs-lookup"><span data-stu-id="57ccb-125">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



