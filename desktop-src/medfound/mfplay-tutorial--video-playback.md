---
description: 本教學課程提供使用 MFPlay 播放影片的完整應用程式。
ms.assetid: f72a7c1f-b059-474c-96f2-8fad3b1f7035
title: MFPlay 教學課程：影片播放
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bbadae22e72799c64a42d09b6eed904b56a60d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692324"
---
# <a name="mfplay-tutorial-video-playback"></a>MFPlay 教學課程：影片播放

\[MFPlay 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 \]

本教學課程提供使用 MFPlay 播放影片的完整應用程式。 它是以 [SimplePlay](simpleplay-sample.md) SDK 範例為基礎。

本教學課程包含下列各節：

-   [需求](#requirements)
-   [標頭檔和程式庫檔案](#header-and-library-files)
-   [全域變數](#global-variables)
-   [宣告回呼類別](#declare-the-callback-class)
-   [宣告 SafeRelease 函式](#declare-the-saferelease-function)
-   [開啟媒體檔案](#open-a-media-file)
-   [視窗訊息處理常式](#window-message-handlers)
-   [執行回呼方法](#implement-the-callback-method)
-   [執行 WinMain](#implement-winmain)
-   [相關主題](#related-topics)

如需 MFPlay API 的更詳細討論，請參閱 [使用 MFPlay 開始使用](getting-started-with-mfplay.md)。

## <a name="requirements"></a>規格需求

MFPlay 需要 Windows 7。

## <a name="header-and-library-files"></a>標頭檔和程式庫檔案

在您的專案中包含下列標頭檔：


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <new>
#include <windows.h>
#include <windowsx.h>
#include <mfplay.h>
#include <mferror.h>
#include <shobjidl.h>   // defines IFileOpenDialog
#include <strsafe.h>
#include <Shlwapi.h>
```



連結至下列程式碼程式庫：

-   mfplay .lib
-   shlwapi .lib

## <a name="global-variables"></a>全域變數

宣告下列全域變數：


```C++
IMFPMediaPlayer         *g_pPlayer = NULL;      // The MFPlay player object.
MediaPlayerCallback     *g_pPlayerCB = NULL;    // Application callback object.

BOOL                    g_bHasVideo = FALSE;
```



這些變數將使用如下所示：

<dl> <dt>

<span id="g_hwnd"></span><span id="G_HWND"></span>*g \_ hwnd*
</dt> <dd>

應用程式視窗的控制碼。

</dd> <dt>

<span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g \_ bVideo*
</dt> <dd>

用來追蹤影片是否現正播放的布林值。

</dd> <dt>

<span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g \_ pPlayer*
</dt> <dd>

[**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)介面的指標。 這個介面是用來控制播放。

</dd> <dt>

<span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g \_ pCallback*
</dt> <dd>

[**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)介面的指標。 應用程式會執行這個回呼介面，以從 player 物件取得通知。

</dd> </dl>

## <a name="declare-the-callback-class"></a>宣告回呼類別

若要從 player 物件取得事件通知，應用程式必須執行 [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) 介面。 下列程式碼會宣告實介面的類別。 唯一的成員變數是 *m \_ cRef*，它會儲存參考計數。

**IUnknown** 方法是以內嵌方式執行。 [**IMFPMediaPlayerCallback：： OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent)方法的執行稍後會顯示;請參閱 [執行回呼方法](#implement-the-callback-method)。


```C++
// Implements the callback interface for MFPlay events.

class MediaPlayerCallback : public IMFPMediaPlayerCallback
{
    long m_cRef; // Reference count

public:

    MediaPlayerCallback() : m_cRef(1)
    {
    }

    IFACEMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(MediaPlayerCallback, IMFPMediaPlayerCallback),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    IFACEMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    IFACEMETHODIMP_(ULONG) Release()
    {
        ULONG count = InterlockedDecrement(&m_cRef);
        if (count == 0)
        {
            delete this;
            return 0;
        }
        return count;
    }

    // IMFPMediaPlayerCallback methods
    IFACEMETHODIMP_(void) OnMediaPlayerEvent(MFP_EVENT_HEADER *pEventHeader);
};
```



## <a name="declare-the-saferelease-function"></a>宣告 SafeRelease 函式

在本教學課程中， [SafeRelease](saferelease.md) 函式是用來釋放介面指標：


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



## <a name="open-a-media-file"></a>開啟媒體檔案

`PlayMediaFile`函數會開啟媒體檔案，如下所示：

1.  如果 *g \_ PPlayer* 為 **Null**，則函式會呼叫 [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) 來建立 media player 物件的新實例。 要 **MFPCreateMediaPlayer** 的輸入參數包含回呼介面的指標，以及影片視窗的控制碼。
2.  為了開啟媒體檔案，此函式會呼叫 [**IMFPMediaPlayer：： CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)，並傳入檔案的 URL。 這個方法會以非同步方式完成。 完成時，會呼叫應用程式的 [**IMFPMediaPlayerCallback：： OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) 方法。


```C++
HRESULT PlayMediaFile(HWND hwnd, PCWSTR pszURL)
{
    HRESULT hr = S_OK;

    // Create the MFPlayer object.
    if (g_pPlayer == NULL)
    {
        g_pPlayerCB = new (std::nothrow) MediaPlayerCallback();

        if (g_pPlayerCB == NULL)
        {
            return E_OUTOFMEMORY;
        }

        hr = MFPCreateMediaPlayer(
            NULL,
            FALSE,          // Start playback automatically?
            0,              // Flags
            g_pPlayerCB,    // Callback pointer
            hwnd,           // Video window
            &g_pPlayer
            );
    }

    // Create a new media item for this URL.

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromURL(pszURL, FALSE, 0, NULL);
    }

    // The CreateMediaItemFromURL method completes asynchronously.
    // The application will receive an MFP_EVENT_TYPE_MEDIAITEM_CREATED
    // event. See MediaPlayerCallback::OnMediaPlayerEvent().

    return hr;
}
```



此函式會 `OnFileOpen` 顯示 [一般檔案] 對話方塊，可讓使用者選取要播放的檔案。 **IFileOpenDialog** 介面是用來顯示 [一般檔案] 對話方塊。 此介面是 Windows Shell Api 的一部分;它是在 Windows Vista 中引進來取代舊版的 **GetOpenFileName** 函式。 當使用者選取檔案後， `OnFileOpen` 就會呼叫 `PlayMediaFile` 以開始播放。


```C++
void OnFileOpen(HWND hwnd)
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;
    PWSTR pwszFilePath = NULL;

    // Create the FileOpenDialog object.
    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL,
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->SetTitle(L"Select a File to Play");
    }

    // Show the file-open dialog.
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(hwnd);
    }

    if (hr == HRESULT_FROM_WIN32(ERROR_CANCELLED))
    {
        // User canceled.
        SafeRelease(&pFileOpen);
        return;
    }

    // Get the file name from the dialog.
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pItem->GetDisplayName(SIGDN_URL, &pwszFilePath);
    }

    // Open the media file.
    if (SUCCEEDED(hr))
    {
        hr = PlayMediaFile(hwnd, pwszFilePath);
    }

    if (FAILED(hr))
    {
        ShowErrorMessage(L"Could not open file.", hr);
    }

    CoTaskMemFree(pwszFilePath);

    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
}
```



## <a name="window-message-handlers"></a>視窗訊息處理常式

接下來，宣告下列視窗訊息的訊息處理常式：

-   **WM \_ 油漆**
-   **WM \_ 大小**
-   **WM \_ 關閉**

針對 **WM \_ 油漆** 訊息，您必須追蹤影片是否現正播放中。 若是如此，請呼叫 [**IMFPMediaPlayer：： UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) 方法。 這個方法會讓 player 物件重繪最近的影片畫面。

如果沒有任何影片，則應用程式會負責繪製視窗。 在本教學課程中，應用程式只會呼叫 GDI **FillRect** 函式來填滿整個工作區。


```C++
void OnPaint(HWND hwnd)
{
    PAINTSTRUCT ps;
    HDC hdc = BeginPaint(hwnd, &ps);

    if (g_pPlayer && g_bHasVideo)
    {
        // Playback has started and there is video.

        // Do not draw the window background, because the video
        // frame fills the entire client area.

        g_pPlayer->UpdateVideo();
    }
    else
    {
        // There is no video stream, or playback has not started.
        // Paint the entire client area.

        FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
    }

    EndPaint(hwnd, &ps);
}
```



若為 **WM \_ 大小** 的訊息，請呼叫 [**IMFPMediaPlayer：： UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo)。 這個方法會使播放程式物件重新調整影片，使其符合目前的視窗大小。 請注意， **UpdateVideo** 會同時用於 **Wm \_ 油漆** 和 **wm \_ 大小**。


```C++
void OnSize(HWND /*hwnd*/, UINT state, int /*cx*/, int /*cy*/)
{
    if (state == SIZE_RESTORED)
    {
        if (g_pPlayer)
        {
            // Resize the video.
            g_pPlayer->UpdateVideo();
        }
    }
}
```



若為 **WM \_ 關閉** 訊息，請釋放 [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) 和 [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) 指標。


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



## <a name="implement-the-callback-method"></a>執行回呼方法

[**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)介面會定義單一方法 [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent)。 每當播放期間發生事件時，這個方法就會通知應用程式。 方法會接受一個參數，也就是一個對 [**MFP \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 結構的指標。 結構的 **eEventType** 成員會指定發生的事件。

[**MFP \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header)結構後面可能接著額外的資料。 針對每個事件種類，會定義將 **MFP \_ 事件 \_ 標頭** 指標轉換成事件特定結構的宏。  (查看 [**MFP \_ 事件 \_ 類型**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type)。 ) 

在本教學課程中，有兩個重要的事件：



| 事件                                    | 描述                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------|
| **已 \_ \_ \_ 建立 MEDIAITEM 的 MFP 事件種類 \_** | [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)完成時傳送。 |
| **\_ \_ \_ MEDIAITEM 設定的 MFP 事件種類 \_**     | [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem)完成時傳送。                         |



 

下列程式碼示範如何將 [**MFP \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 指標轉型為事件特定結構。


```C++
void MediaPlayerCallback::OnMediaPlayerEvent(MFP_EVENT_HEADER * pEventHeader)
{
    if (FAILED(pEventHeader->hrEvent))
    {
        ShowErrorMessage(L"Playback error", pEventHeader->hrEvent);
        return;
    }

    switch (pEventHeader->eEventType)
    {
    case MFP_EVENT_TYPE_MEDIAITEM_CREATED:
        OnMediaItemCreated(MFP_GET_MEDIAITEM_CREATED_EVENT(pEventHeader));
        break;

    case MFP_EVENT_TYPE_MEDIAITEM_SET:
        OnMediaItemSet(MFP_GET_MEDIAITEM_SET_EVENT(pEventHeader));
        break;
    }
}
```



**\_ \_ \_ MEDIAITEM \_ 建立事件的 MFP 事件種類** 會通知應用程式， [**IMFPMediaPlayer：： CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)方法已完成。 事件結構包含 [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) 介面的指標，代表從 URL 建立的媒體專案。 若要將專案排入佇列以進行播放，請將此指標傳遞給 [**IMFPMediaPlayer：： SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) 方法：


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    // The media item was created successfully.

    if (g_pPlayer)
    {
        BOOL    bHasVideo = FALSE;
        BOOL    bIsSelected = FALSE;

        // Check if the media item contains video.
        HRESULT hr = pEvent->pMediaItem->HasVideo(&bHasVideo, &bIsSelected);
        if (SUCCEEDED(hr))
        {
            g_bHasVideo = bHasVideo && bIsSelected;

            // Set the media item on the player. This method completes
            // asynchronously.
            hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
        }

        if (FAILED(hr))
        {
            ShowErrorMessage(L"Error playing this file.", hr);
        }
   }
}
```



[ **MFP \_ 事件 \_ 類型 \_ MEDIAITEM \_ SET** ] 事件會通知應用程式 [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) 已完成。 呼叫 [**IMFPMediaPlayer：:P**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) 配置以開始播放：


```C++
void OnMediaItemSet(MFP_MEDIAITEM_SET_EVENT * /*pEvent*/)
{
    HRESULT hr = g_pPlayer->Play();
    if (FAILED(hr))
    {
        ShowErrorMessage(L"IMFPMediaPlayer::Play failed.", hr);
    }
}
```



## <a name="implement-winmain"></a>執行 WinMain

在本教學課程的其餘部分，沒有媒體基礎 Api 的呼叫。 下列程式碼顯示視窗程式：


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        HANDLE_MSG(hwnd, WM_CLOSE,   OnClose);
        HANDLE_MSG(hwnd, WM_PAINT,   OnPaint);
        HANDLE_MSG(hwnd, WM_COMMAND, OnCommand);
        HANDLE_MSG(hwnd, WM_SIZE,    OnSize);

    case WM_ERASEBKGND:
        return 1;

    default:
        return DefWindowProc(hwnd, uMsg, wParam, lParam);
    }
}
```



`InitializeWindow`函數會註冊應用程式的視窗類別並建立視窗。


```C++
BOOL InitializeWindow(HWND *pHwnd)
{
    const wchar_t CLASS_NAME[]  = L"MFPlay Window Class";
    const wchar_t WINDOW_NAME[] = L"MFPlay Sample Application";

    WNDCLASS wc = {};

    wc.lpfnWndProc   = WindowProc;
    wc.hInstance     = GetModuleHandle(NULL);
    wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wc.lpszClassName = CLASS_NAME;
    wc.lpszMenuName  = MAKEINTRESOURCE(IDR_MENU1);

    RegisterClass(&wc);

    HWND hwnd = CreateWindow(
        CLASS_NAME, WINDOW_NAME, WS_OVERLAPPEDWINDOW,
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,
        NULL, NULL, GetModuleHandle(NULL), NULL);

    if (!hwnd)
    {
        return FALSE;
    }

    ShowWindow(hwnd, SW_SHOWDEFAULT);
    UpdateWindow(hwnd);

    *pHwnd = hwnd;

    return TRUE;
}
```



最後，請執行應用程式進入點：


```C++
int WINAPI wWinMain(HINSTANCE, HINSTANCE, PWSTR, int)
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    HRESULT hr = CoInitializeEx(NULL,
        COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    if (FAILED(hr))
    {
        return 0;
    }

    HWND hwnd = NULL;
    if (InitializeWindow(&hwnd))
    {
        // Message loop
        MSG msg = {};
        while (GetMessage(&msg, NULL, 0, 0))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }

        DestroyWindow(hwnd);
    }
    CoUninitialize();

    return 0;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 MFPlay 進行音訊/影片播放](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



