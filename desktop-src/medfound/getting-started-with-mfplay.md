---
description: MFPlay 是在 c + + 中建立媒體播放應用程式的 API。
ms.assetid: 55612f49-5995-4bdf-aa12-8a853e5a2b24
title: 使用 MFPlay 開始使用
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2afb0b20189501530116c252a4d11a9b3e2d8d0dff07482b1998b73400071e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118063489"
---
# <a name="getting-started-with-mfplay"></a>使用 MFPlay 開始使用

\[MFPlay 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 \]

MFPlay 是在 c + + 中建立媒體播放應用程式的 API。

本主題包含下列幾節：

-   [需求](#requirements)
-   [關於 MFPlay](#about-mfplay)
-   [播放媒體檔案](#playing-a-media-file)
-   [控制播放](#controlling-playback)
-   [從播放玩家接收事件](#receiving-events-from-the-player)
-   [取得媒體檔案的相關資訊](#getting-information-about-a-media-file)
-   [管理影片播放](#managing-video-playback)
-   [MFPlay 的限制](#limitations-of-mfplay)
-   [相關主題](#related-topics)

## <a name="requirements"></a>規格需求

MFPlay 需要 Windows 7。

## <a name="about-mfplay"></a>關於 MFPlay

MFPlay 具有簡單的程式設計模型，同時提供大部分播放應用程式所需的核心功能集。 應用程式會建立控制播放的 *播放* 程式物件。 為了播放媒體檔案，player 物件會建立 *媒體專案*，可用來取得媒體檔案內容的相關資訊。 應用程式會透過 player 物件之 [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) 介面上的方法來控制播放。 （選擇性）應用程式可以透過回呼介面取得事件通知，下圖說明此程式。

![概念圖：應用程式和播放機會指向彼此，並指向媒體專案，以指向媒體檔案](images/mfplay.png)

## <a name="playing-a-media-file"></a>播放媒體檔案

若要播放媒體檔案，請呼叫 [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) 函式。


```C++
// Global variables
IMFPMediaPlayer *g_pPlayer = NULL;

const WCHAR *sURL = L"C:\\Users\\Public\\Videos\\example.wmv";

HRESULT PlayVideo(HWND hwnd, const WCHAR* sURL)
{
    // Create the player object and play a video file.

    return MFPCreateMediaPlayer(
        sURL,
        TRUE,   // Start playback automatically?
        0,      // Flags.
        NULL,   // Callback pointer.
        hwnd,
        &g_pPlayer
        );
}
```



[**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer)函式會建立 MFPlay player 物件的新實例。 函數會採用下列參數：

-   第一個參數是要開啟之檔案的 URL。 這可以是本機檔案或媒體伺服器上的檔案。
-   第二個參數指定播放是否自動啟動。 藉由將此參數設為 **TRUE**，檔案會在 MFPlay 載入時立即播放。
-   第三個參數會設定各種選項。 若為預設選項，請傳遞零 (0) 。
-   第四個參數是選擇性回呼介面的指標。 這個參數可以是 **Null**，如下所示。 回呼會在 [從播放程式接收事件](#receiving-events-from-the-player)的區段中描述。
-   第五個參數是應用程式視窗的控制碼。 如果媒體檔案包含影片串流，影片將會出現在此視窗的工作區中。 針對僅限音訊播放，此參數可以是 **Null**。

最後一個參數會接收 player 物件之 [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) 介面的指標。

在應用程式關閉之前，請務必釋放 [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) 指標。 您可以在 **WM \_ 關閉** 訊息處理常式中完成這項作業。


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



> [!Note]  
> 此範例會使用 [SafeRelease](saferelease.md) 函式來釋放介面指標。

 

針對簡單的影片播放，這就是您所需的所有程式碼。 本教學課程的其餘部分將說明如何新增更多功能，從如何控制播放開始。

## <a name="controlling-playback"></a>控制播放

上一節所顯示的程式碼將會播放媒體檔案，直到到達檔案結尾為止。 您可以在 [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) 介面上呼叫下列方法，以停止並開始播放：

-   [**IMFPMediaPlayer：:P ause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) 會暫停播放。 播放暫停時，會顯示最新的影片畫面，且音訊為無訊息。
-   [**IMFPMediaPlayer：： Stop**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) 停止播放。 不會顯示任何影片，而且播放位置會重設為檔案的開頭。
-   [**IMFPMediaPlayer：:P**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) 配置在停止或暫停之後繼續播放。

當您按下 **空格鍵** 時，下列程式碼會暫停或繼續播放。


```C++
//-------------------------------------------------------------------
// OnKeyDown
//
// Handles the WM_KEYDOWN message.
//-------------------------------------------------------------------

void OnKeyDown(HWND hwnd, UINT vk, BOOL fDown, int cRepeat, UINT flags)
{
    HRESULT hr = S_OK;

    switch (vk)
    {
    case VK_SPACE:

        // Toggle between playback and paused/stopped.
        if (g_pPlayer)
        {
            MFP_MEDIAPLAYER_STATE state = MFP_MEDIAPLAYER_STATE_EMPTY;
            
            g_pPlayer->GetState(&state);

            if (state == MFP_MEDIAPLAYER_STATE_PAUSED ||  
                state == MFP_MEDIAPLAYER_STATE_STOPPED)
            {
                g_pPlayer->Play();
            }
            else if (state == MFP_MEDIAPLAYER_STATE_PLAYING)
            {
                g_pPlayer->Pause();
            }
        }
        break;
    }
}
```



此範例會呼叫 [**IMFPMediaPlayer：： >getstate**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) 方法，以取得目前的播放狀態 (暫停、停止或播放) ，並據以暫停或繼續。

## <a name="receiving-events-from-the-player"></a>從播放玩家接收事件

MFPlay 使用回呼介面將事件傳送至您的應用程式。 此回呼有兩個原因：

-   播放會在個別的執行緒上執行。 在播放期間，某些事件可能會發生，例如到達檔案結尾。 MFPlay 使用回呼來通知您應用程式的事件。
-   許多 [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) 方法都是非同步，這表示它們會在作業完成之前傳回。 非同步方法可讓您從 UI 執行緒啟動作業，此作業可能需要很長的時間才能完成，而不會造成 UI 封鎖。 作業完成之後，MFPlay 會發出回呼的信號。

若要接收回呼通知，請執行 [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) 介面。 此介面會繼承 **IUnknown** 並定義單一方法 [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent)。 若要設定回呼，請在 [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer)函式的 *pCallback* 參數中傳遞 **IMFPMediaPlayerCallback** 執行的指標。

以下是本教學課程中的第一個範例，修改為包含回呼。


```
// Global variables.
IMFPMediaPlayer *g_pPlayer = NULL;
IMFPMediaPlayerCallback *g_pCallback = NULL;

// Call an application-defined function to create the callback object.
hr = CreateMyCallback(&g_pCallback);

// Create the player object and play a video file.

const WCHAR *sURL = L"C:\\Users\\Public\\Videos\\example.wmv";

if (SUCCEEDED(hr))
{
    hr = MFPCreateMediaPlayer(
        sURL,
        TRUE,        // Start playback automatically?
        0,           // Flags.
        g_pCallback, // Callback pointer.
        hwnd,
        &g_pPlayer
        );
}
```



[**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent)方法具有單一參數，也就是 [**MFP \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header)結構的指標。 此結構的 **eEventType** 成員會告知您發生了哪些事件。 例如，當播放開始時，MFPlay 會傳送「 **MFP \_ 事件種類」 \_ \_ 播放** 事件。

每個事件種類都有對應的資料結構，其中包含該事件的資訊。 這些結構都會以 [**MFP \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 結構作為開頭。 在您的回呼中，將 [ **MFP] \_ 事件 \_ 標頭** 指標轉換為事件特定的資料結構。 例如，如果事件種類是「 **mfp \_ play」 \_ 事件**，資料結構就是「 [**mfp 播放」 \_ \_ 事件**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event)。 下列程式碼顯示如何在回呼中處理這個事件。


```
void STDMETHODCALLTYPE MediaPlayerCallback::OnMediaPlayerEvent(
    MFP_EVENT_HEADER *pEventHeader
    )
{
    switch (pEventHeader->eEventType)
    {
    case MFP_EVENT_TYPE_PLAY:
        OnPlay(MFP_GET_PLAY_EVENT(pEventHeader));
        break;

    // Other event types (not shown).

    }
}

// Function to handle the event.
void OnPlay(MFP_PLAY_EVENT *pEvent)
{
    if (FAILED(pEvent->header.hrEvent))
    {  
        // Error occurred during playback.
    }  
}
```



此範例會使用「 [**mfp \_ 取得 \_ play \_ 事件**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) 」事件，將 *pEventHeader* 指標轉型為 [**MFP \_ PLAY \_ 事件**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) 結構。 觸發事件之作業的 **HRESULT** 會儲存在結構的 **hrEvent** 欄位中。

如需所有事件種類和對應資料結構的清單，請參閱 [**MFP \_ 事件 \_ 類型**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type)。

有關執行緒的附注：根據預設，MFPlay 會從呼叫 [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer)的相同執行緒叫用回呼。 此執行緒必須有訊息迴圈。 或者，您可以在 **MFPCreateMediaPlayer** 的 *creationOptions* 參數中傳遞 **MFP \_ 選項 \_ 自由 \_ 執行緒 \_ 回呼** 旗標。 此旗標會使 MFPlay 叫用來自不同執行緒的回呼。 任一個選項對您的應用程式都有影響。 預設選項表示您的回呼無法執行任何動作，因為它會封鎖您的視窗程式，而不會等候您的訊息迴圈，例如等待 UI 動作。 無限制執行緒選項表示您需要使用重要區段來保護您在回呼中存取的任何資料。 在大部分的情況下，預設選項是最簡單的。

## <a name="getting-information-about-a-media-file"></a>取得媒體檔案的相關資訊

當您在 MFPlay 中開啟媒體檔案時，播放程式會建立一個稱為 *媒體專案* 的物件，代表媒體檔案。 此物件會公開 [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) 介面，可讓您用來取得媒體檔案的相關資訊。 許多 MFPlay 事件結構都包含指向目前媒體專案的指標。 您也可以在播放程式上呼叫 [**IMFPMediaPlayer：： GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) ，以取得目前的媒體專案。

有兩個特別有用的方法是 [**IMFPMediaItem：： HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) 和 [**IMFPMediaItem：： HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio)。 這些方法會查詢媒體來源是否包含影片或音訊。

例如，下列程式碼會測試目前的媒體檔案是否包含影片串流。


```
IMFPMediaItem *pItem;
BOOL bHasVideo = FALSE;
BOOL bIsSelected = FALSE;

hr = g_pPlayer->GetMediaItem(TRUE, &pItem);
if (SUCCEEDED(hr))
{
    hr = pItem->HasVideo(&bHasVideo, &bIsSelected);
    pItem->Release();
}
```



如果來源檔案包含已選取要播放的影片資料流程， *bHasVideo* 和 *bIsSelected* 都設為 **TRUE**。

## <a name="managing-video-playback"></a>管理影片播放

當 MFPlay 播放影片檔案時，它會在您于 [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) 函式中指定的視窗內繪製影片。 這會發生在 Microsoft 媒體基礎播放管線所擁有的另一個執行緒上。 在大部分的情況下，您的應用程式不需要管理此進程。 不過，在兩種情況下，應用程式必須通知 MFPlay 更新影片。

-   如果播放暫停或停止，MFPlay 必須在應用程式的影片視窗收到 WM 油漆訊息時收到通知 \_ 。 這可讓 MFPlay 重新繪製視窗。
-   如果調整視窗的大小，則必須通知 MFPlay，讓它可以調整影片以符合新的視窗大小。

[**IMFPMediaPlayer：： UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo)方法會處理這兩種情況。 在適用于影片視窗的 WM \_ 油漆和 wm \_ 大小訊息處理常式內，呼叫這個方法。

> [!IMPORTANT]
> 呼叫 GDI **BeginPaint** 函式之前，請先呼叫 [**UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo)。

 


```
IMFPMediaPlayer *g_pPlayer;   // MFPlay player object

void OnSize(HWND hwnd, UINT state, int cx, int cy)
{
    HDC hdc;
    PAINTSTRUCT ps;

    if (g_pPlayer && (state == SIZE_RESTORED))
    {
        hdc = BeginPaint(hwnd, &ps);
        g_pPlayer->UpdateVideo();
         EndPaint(hwnd, &ps);
    }
}

void OnPaint(HWND hwnd)
{
    HDC hdc;
    PAINTSTRUCT ps;

    hdc = BeginPaint(hwnd, &ps);
    if (g_pPlayer)
    {
        g_pPlayer->UpdateVideo();
    }
      EndPaint(hwnd, &ps);
}
```



除非您另外指定，否則 MFPlay 會使用上下黑邊縮（如有需要）顯示正確的外觀比例的影片。 如果您不想要保留長寬比，請使用 **MFVideoARMode \_ None** 旗標來呼叫 [**IMFPMediaPlayer：： SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) 。 這會導致 MFPlay 延展影片以填滿整個矩形，而不會上下黑邊縮。 一般來說，您應該使用預設設定，讓 MFPlay 黑邊影片。 預設黑邊色彩為黑色，但您可以藉由呼叫 [**IMFPMediaPlayer：： SetBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor)來變更。

## <a name="limitations-of-mfplay"></a>MFPlay 的限制

目前的 MFPlay 版本具有下列限制：

-   MFPlay 不支援受 DRM 保護的內容。
-   根據預設，MFPlay 不支援網路串流通訊協定。 如需詳細資訊，請參閱 [**IMFPMediaPlayer：： CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)。
-   MFPlay 不支援伺服器端播放清單， (SSPLs) 或其他播放多個區段的來源類型。 在技術方面，MFPlay 會在第一次簡報之後停止播放，並忽略媒體來源中的任何 [MENewPresentation](menewpresentation.md) 事件。
-   MFPlay 不支援媒體來源之間的無縫轉換。
-   MFPlay 不支援混合多個影片串流。
-   MFPlay 只支援在媒體基礎中以原生方式支援的媒體格式。  (包括可能安裝在系統上的協力廠商媒體基礎元件 ) 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 MFPlay 進行音訊/影片播放](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



