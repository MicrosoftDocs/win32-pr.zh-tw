---
description: 本主題是教學課程的步驟2，說明如何使用媒體基礎來播放媒體檔案。
ms.assetid: b489312f-ab8c-4ec6-8070-f5848034087e
title: 步驟2：建立 CPlayer 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df004aa060a8ce8a46adbf0fdae438ca0a0cd1a454e9fc17889ad29eebef21ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847778"
---
# <a name="step-2-create-the-cplayer-object"></a>步驟2：建立 CPlayer 物件

本主題是教學課程的步驟2， [說明如何使用媒體基礎來播放媒體](how-to-play-unprotected-media-files.md)檔案。 完整的程式碼會顯示在「 [媒體會話播放」範例](media-session-playback-example.md)中。

若要建立類別的實例 `CPlayer` ，應用程式會呼叫靜態 `CPlayer::CreateInstance` 方法。 這個方法會採用下列參數：

-   *hVideo* 會指定要顯示影片的視窗。
-   *hEvent* 指定要接收事件的視窗。 將相同的控制碼傳遞給兩個視窗控制碼是有效的。
-   *ppPlayer* 會接收新實例的指標 `CPlayer` 。

下列程式碼顯示 `CreateInstance` 方法：


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



下列程式碼顯示此函式 `CPlayer` ：


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



此函式會執行下列動作：

1.  呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 以初始化媒體基礎平臺。
2.  建立自動重設事件。 關閉媒體會話時，會使用此事件;請參閱 [步驟7：關機媒體會話](step-7--shut-down-the-media-session.md)。

此函式會關閉媒體會話，如 [步驟7：關機媒體會話](step-7--shut-down-the-media-session.md)中所述。


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



請注意，函式和函式都是受保護的類別方法。 應用程式會使用靜態方法來建立物件 `CreateInstance` 。 它會藉由呼叫 **IUnknown：： Release** 來終結物件，而不是明確地使用 **delete**。

下一[步：步驟3：開啟媒體](step-3--open-a-media-file.md)檔案

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊/視訊播放](audio-video-playback.md)
</dt> <dt>

[如何使用媒體基礎播放媒體檔案](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



