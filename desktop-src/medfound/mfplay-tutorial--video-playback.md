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
# <a name="mfplay-tutorial-video-playback"></a><span data-ttu-id="cbfa5-103">MFPlay 教學課程：影片播放</span><span class="sxs-lookup"><span data-stu-id="cbfa5-103">MFPlay Tutorial: Video Playback</span></span>

<span data-ttu-id="cbfa5-104">\[MFPlay 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cbfa5-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="cbfa5-106">\]</span><span class="sxs-lookup"><span data-stu-id="cbfa5-106">\]</span></span>

<span data-ttu-id="cbfa5-107">本教學課程提供使用 MFPlay 播放影片的完整應用程式。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-107">This tutorial presents a complete application that plays video using MFPlay.</span></span> <span data-ttu-id="cbfa5-108">它是以 [SimplePlay](simpleplay-sample.md) SDK 範例為基礎。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-108">It is based on the [SimplePlay](simpleplay-sample.md) SDK sample.</span></span>

<span data-ttu-id="cbfa5-109">本教學課程包含下列各節：</span><span class="sxs-lookup"><span data-stu-id="cbfa5-109">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="cbfa5-110">需求</span><span class="sxs-lookup"><span data-stu-id="cbfa5-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="cbfa5-111">標頭檔和程式庫檔案</span><span class="sxs-lookup"><span data-stu-id="cbfa5-111">Header and Library Files</span></span>](#header-and-library-files)
-   [<span data-ttu-id="cbfa5-112">全域變數</span><span class="sxs-lookup"><span data-stu-id="cbfa5-112">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="cbfa5-113">宣告回呼類別</span><span class="sxs-lookup"><span data-stu-id="cbfa5-113">Declare the Callback Class</span></span>](#declare-the-callback-class)
-   [<span data-ttu-id="cbfa5-114">宣告 SafeRelease 函式</span><span class="sxs-lookup"><span data-stu-id="cbfa5-114">Declare the SafeRelease Function</span></span>](#declare-the-saferelease-function)
-   [<span data-ttu-id="cbfa5-115">開啟媒體檔案</span><span class="sxs-lookup"><span data-stu-id="cbfa5-115">Open a Media File</span></span>](#open-a-media-file)
-   [<span data-ttu-id="cbfa5-116">視窗訊息處理常式</span><span class="sxs-lookup"><span data-stu-id="cbfa5-116">Window Message Handlers</span></span>](#window-message-handlers)
-   [<span data-ttu-id="cbfa5-117">執行回呼方法</span><span class="sxs-lookup"><span data-stu-id="cbfa5-117">Implement the Callback Method</span></span>](#implement-the-callback-method)
-   [<span data-ttu-id="cbfa5-118">執行 WinMain</span><span class="sxs-lookup"><span data-stu-id="cbfa5-118">Implement WinMain</span></span>](#implement-winmain)
-   [<span data-ttu-id="cbfa5-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="cbfa5-119">Related topics</span></span>](#related-topics)

<span data-ttu-id="cbfa5-120">如需 MFPlay API 的更詳細討論，請參閱 [使用 MFPlay 開始使用](getting-started-with-mfplay.md)。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-120">For a more detailed discussion of the MFPlay API, see [Getting Started with MFPlay](getting-started-with-mfplay.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cbfa5-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbfa5-121">Requirements</span></span>

<span data-ttu-id="cbfa5-122">MFPlay 需要 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-122">MFPlay requires Windows 7.</span></span>

## <a name="header-and-library-files"></a><span data-ttu-id="cbfa5-123">標頭檔和程式庫檔案</span><span class="sxs-lookup"><span data-stu-id="cbfa5-123">Header and Library Files</span></span>

<span data-ttu-id="cbfa5-124">在您的專案中包含下列標頭檔：</span><span class="sxs-lookup"><span data-stu-id="cbfa5-124">Include the following header files in your project:</span></span>


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



<span data-ttu-id="cbfa5-125">連結至下列程式碼程式庫：</span><span class="sxs-lookup"><span data-stu-id="cbfa5-125">Link to the following code libraries:</span></span>

-   <span data-ttu-id="cbfa5-126">mfplay .lib</span><span class="sxs-lookup"><span data-stu-id="cbfa5-126">mfplay.lib</span></span>
-   <span data-ttu-id="cbfa5-127">shlwapi .lib</span><span class="sxs-lookup"><span data-stu-id="cbfa5-127">shlwapi.lib</span></span>

## <a name="global-variables"></a><span data-ttu-id="cbfa5-128">全域變數</span><span class="sxs-lookup"><span data-stu-id="cbfa5-128">Global Variables</span></span>

<span data-ttu-id="cbfa5-129">宣告下列全域變數：</span><span class="sxs-lookup"><span data-stu-id="cbfa5-129">Declare the following global variables:</span></span>


```C++
IMFPMediaPlayer         *g_pPlayer = NULL;      // The MFPlay player object.
MediaPlayerCallback     *g_pPlayerCB = NULL;    // Application callback object.

BOOL                    g_bHasVideo = FALSE;
```



<span data-ttu-id="cbfa5-130">這些變數將使用如下所示：</span><span class="sxs-lookup"><span data-stu-id="cbfa5-130">These variables will be used as follows:</span></span>

<dl> <dt>

<span data-ttu-id="cbfa5-131"><span id="g_hwnd"></span><span id="G_HWND"></span>*g \_ hwnd*</span><span class="sxs-lookup"><span data-stu-id="cbfa5-131"><span id="g_hwnd"></span><span id="G_HWND"></span>*g\_hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="cbfa5-132">應用程式視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-132">A handle to the application window.</span></span>

</dd> <dt>

<span data-ttu-id="cbfa5-133"><span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g \_ bVideo*</span><span class="sxs-lookup"><span data-stu-id="cbfa5-133"><span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g\_bVideo*</span></span>
</dt> <dd>

<span data-ttu-id="cbfa5-134">用來追蹤影片是否現正播放的布林值。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-134">A Boolean value that tracks whether video is playing.</span></span>

</dd> <dt>

<span data-ttu-id="cbfa5-135"><span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g \_ pPlayer*</span><span class="sxs-lookup"><span data-stu-id="cbfa5-135"><span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g\_pPlayer*</span></span>
</dt> <dd>

<span data-ttu-id="cbfa5-136">[**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-136">A pointer to the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span> <span data-ttu-id="cbfa5-137">這個介面是用來控制播放。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-137">This interface is used to control playback.</span></span>

</dd> <dt>

<span data-ttu-id="cbfa5-138"><span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g \_ pCallback*</span><span class="sxs-lookup"><span data-stu-id="cbfa5-138"><span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g\_pCallback*</span></span>
</dt> <dd>

<span data-ttu-id="cbfa5-139">[**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-139">A pointer to the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="cbfa5-140">應用程式會執行這個回呼介面，以從 player 物件取得通知。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-140">The application implements this callback interface to get notifications from the player object.</span></span>

</dd> </dl>

## <a name="declare-the-callback-class"></a><span data-ttu-id="cbfa5-141">宣告回呼類別</span><span class="sxs-lookup"><span data-stu-id="cbfa5-141">Declare the Callback Class</span></span>

<span data-ttu-id="cbfa5-142">若要從 player 物件取得事件通知，應用程式必須執行 [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) 介面。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-142">To get event notifications from the player object, the application must implement the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="cbfa5-143">下列程式碼會宣告實介面的類別。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-143">The following code declares a class that implements the interface.</span></span> <span data-ttu-id="cbfa5-144">唯一的成員變數是 *m \_ cRef*，它會儲存參考計數。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-144">The only member variable is *m\_cRef*, which stores the reference count.</span></span>

<span data-ttu-id="cbfa5-145">**IUnknown** 方法是以內嵌方式執行。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-145">The **IUnknown** methods are implemented inline.</span></span> <span data-ttu-id="cbfa5-146">[**IMFPMediaPlayerCallback：： OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent)方法的執行稍後會顯示;請參閱 [執行回呼方法](#implement-the-callback-method)。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-146">The implementation of the [**IMFPMediaPlayerCallback::OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method is shown later; see [Implement the Callback Method](#implement-the-callback-method).</span></span>


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



## <a name="declare-the-saferelease-function"></a><span data-ttu-id="cbfa5-147">宣告 SafeRelease 函式</span><span class="sxs-lookup"><span data-stu-id="cbfa5-147">Declare the SafeRelease Function</span></span>

<span data-ttu-id="cbfa5-148">在本教學課程中， [SafeRelease](saferelease.md) 函式是用來釋放介面指標：</span><span class="sxs-lookup"><span data-stu-id="cbfa5-148">Throughout this tutorial, the [SafeRelease](saferelease.md) function is used to release interface pointers:</span></span>


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



## <a name="open-a-media-file"></a><span data-ttu-id="cbfa5-149">開啟媒體檔案</span><span class="sxs-lookup"><span data-stu-id="cbfa5-149">Open a Media File</span></span>

<span data-ttu-id="cbfa5-150">`PlayMediaFile`函數會開啟媒體檔案，如下所示：</span><span class="sxs-lookup"><span data-stu-id="cbfa5-150">The `PlayMediaFile` function opens a media file, as follows:</span></span>

1.  <span data-ttu-id="cbfa5-151">如果 *g \_ PPlayer* 為 **Null**，則函式會呼叫 [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) 來建立 media player 物件的新實例。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-151">If *g\_pPlayer* is **NULL**, the function calls [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) to create a new instance of the media player object.</span></span> <span data-ttu-id="cbfa5-152">要 **MFPCreateMediaPlayer** 的輸入參數包含回呼介面的指標，以及影片視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-152">The input parameters to **MFPCreateMediaPlayer** include a pointer to the callback interface and a handle to the video window.</span></span>
2.  <span data-ttu-id="cbfa5-153">為了開啟媒體檔案，此函式會呼叫 [**IMFPMediaPlayer：： CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)，並傳入檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-153">To open the media file, the function calls [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl), passing in the URL of the file.</span></span> <span data-ttu-id="cbfa5-154">這個方法會以非同步方式完成。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-154">This method completes asynchronously.</span></span> <span data-ttu-id="cbfa5-155">完成時，會呼叫應用程式的 [**IMFPMediaPlayerCallback：： OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) 方法。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-155">When it completes, the application's [**IMFPMediaPlayerCallback::OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method is called.</span></span>


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



<span data-ttu-id="cbfa5-156">此函式會 `OnFileOpen` 顯示 [一般檔案] 對話方塊，可讓使用者選取要播放的檔案。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-156">The `OnFileOpen` function displays the common file dialog, which enables the user to select a file for playback.</span></span> <span data-ttu-id="cbfa5-157">**IFileOpenDialog** 介面是用來顯示 [一般檔案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-157">The **IFileOpenDialog** interface is used to display the common file dialog.</span></span> <span data-ttu-id="cbfa5-158">此介面是 Windows Shell Api 的一部分;它是在 Windows Vista 中引進來取代舊版的 **GetOpenFileName** 函式。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-158">This interface is part of the Windows Shell APIs; it was introduced in Windows Vista as a replacement for the older **GetOpenFileName** function.</span></span> <span data-ttu-id="cbfa5-159">當使用者選取檔案後， `OnFileOpen` 就會呼叫 `PlayMediaFile` 以開始播放。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-159">After the user selects a file, `OnFileOpen` calls `PlayMediaFile` to start playback.</span></span>


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



## <a name="window-message-handlers"></a><span data-ttu-id="cbfa5-160">視窗訊息處理常式</span><span class="sxs-lookup"><span data-stu-id="cbfa5-160">Window Message Handlers</span></span>

<span data-ttu-id="cbfa5-161">接下來，宣告下列視窗訊息的訊息處理常式：</span><span class="sxs-lookup"><span data-stu-id="cbfa5-161">Next, declare message handlers for the following window messages:</span></span>

-   <span data-ttu-id="cbfa5-162">**WM \_ 油漆**</span><span class="sxs-lookup"><span data-stu-id="cbfa5-162">**WM\_PAINT**</span></span>
-   <span data-ttu-id="cbfa5-163">**WM \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="cbfa5-163">**WM\_SIZE**</span></span>
-   <span data-ttu-id="cbfa5-164">**WM \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="cbfa5-164">**WM\_CLOSE**</span></span>

<span data-ttu-id="cbfa5-165">針對 **WM \_ 油漆** 訊息，您必須追蹤影片是否現正播放中。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-165">For the **WM\_PAINT** message, you must track whether video is currently playing.</span></span> <span data-ttu-id="cbfa5-166">若是如此，請呼叫 [**IMFPMediaPlayer：： UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) 方法。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-166">If so, call the [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) method.</span></span> <span data-ttu-id="cbfa5-167">這個方法會讓 player 物件重繪最近的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-167">This method causes the player object to redraw the most recent video frame.</span></span>

<span data-ttu-id="cbfa5-168">如果沒有任何影片，則應用程式會負責繪製視窗。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-168">If there is no video, the application is responsible for painting the window.</span></span> <span data-ttu-id="cbfa5-169">在本教學課程中，應用程式只會呼叫 GDI **FillRect** 函式來填滿整個工作區。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-169">For this tutorial, the application simply calls the GDI **FillRect** function to fill the entire client area.</span></span>


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



<span data-ttu-id="cbfa5-170">若為 **WM \_ 大小** 的訊息，請呼叫 [**IMFPMediaPlayer：： UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo)。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-170">For the **WM\_SIZE** message, call [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span></span> <span data-ttu-id="cbfa5-171">這個方法會使播放程式物件重新調整影片，使其符合目前的視窗大小。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-171">This method causes the player object to readjust the video to match the current size of the window.</span></span> <span data-ttu-id="cbfa5-172">請注意， **UpdateVideo** 會同時用於 **Wm \_ 油漆** 和 **wm \_ 大小**。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-172">Note that **UpdateVideo** is used for both **WM\_PAINT** and **WM\_SIZE**.</span></span>


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



<span data-ttu-id="cbfa5-173">若為 **WM \_ 關閉** 訊息，請釋放 [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) 和 [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) 指標。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-173">For the **WM\_CLOSE** message, release the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) and [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) pointers.</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



## <a name="implement-the-callback-method"></a><span data-ttu-id="cbfa5-174">執行回呼方法</span><span class="sxs-lookup"><span data-stu-id="cbfa5-174">Implement the Callback Method</span></span>

<span data-ttu-id="cbfa5-175">[**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)介面會定義單一方法 [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent)。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-175">The [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface defines a single method, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span></span> <span data-ttu-id="cbfa5-176">每當播放期間發生事件時，這個方法就會通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-176">This method notifies the application whenever an event occurs during playback.</span></span> <span data-ttu-id="cbfa5-177">方法會接受一個參數，也就是一個對 [**MFP \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-177">The method takes one parameter, a pointer to an [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="cbfa5-178">結構的 **eEventType** 成員會指定發生的事件。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-178">The **eEventType** member of the structure specifies the event that occurred.</span></span>

<span data-ttu-id="cbfa5-179">[**MFP \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header)結構後面可能接著額外的資料。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-179">The [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure may be followed by additional data.</span></span> <span data-ttu-id="cbfa5-180">針對每個事件種類，會定義將 **MFP \_ 事件 \_ 標頭** 指標轉換成事件特定結構的宏。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-180">For each event type, a macro is defined that casts the **MFP\_EVENT\_HEADER** pointer to an event-specific structure.</span></span> <span data-ttu-id="cbfa5-181"> (查看 [**MFP \_ 事件 \_ 類型**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type)。 ) </span><span class="sxs-lookup"><span data-stu-id="cbfa5-181">(See [**MFP\_EVENT\_TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).)</span></span>

<span data-ttu-id="cbfa5-182">在本教學課程中，有兩個重要的事件：</span><span class="sxs-lookup"><span data-stu-id="cbfa5-182">For this tutorial, two events are significant:</span></span>



| <span data-ttu-id="cbfa5-183">事件</span><span class="sxs-lookup"><span data-stu-id="cbfa5-183">Event</span></span>                                    | <span data-ttu-id="cbfa5-184">描述</span><span class="sxs-lookup"><span data-stu-id="cbfa5-184">Description</span></span>                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbfa5-185">**已 \_ \_ \_ 建立 MEDIAITEM 的 MFP 事件種類 \_**</span><span class="sxs-lookup"><span data-stu-id="cbfa5-185">**MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED**</span></span> | <span data-ttu-id="cbfa5-186">[**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)完成時傳送。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-186">Sent when the [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) completes.</span></span> |
| <span data-ttu-id="cbfa5-187">**\_ \_ \_ MEDIAITEM 設定的 MFP 事件種類 \_**</span><span class="sxs-lookup"><span data-stu-id="cbfa5-187">**MFP\_EVENT\_TYPE\_MEDIAITEM\_SET**</span></span>     | <span data-ttu-id="cbfa5-188">[**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem)完成時傳送。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-188">Sent when [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) completes.</span></span>                         |



 

<span data-ttu-id="cbfa5-189">下列程式碼示範如何將 [**MFP \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 指標轉型為事件特定結構。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-189">The following code shows how to cast the [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) pointer to the event-specific structure.</span></span>


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



<span data-ttu-id="cbfa5-190">**\_ \_ \_ MEDIAITEM \_ 建立事件的 MFP 事件種類** 會通知應用程式， [**IMFPMediaPlayer：： CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)方法已完成。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-190">The **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event notifies the application that the [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method has completed.</span></span> <span data-ttu-id="cbfa5-191">事件結構包含 [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) 介面的指標，代表從 URL 建立的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-191">The event structure contains a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface, which represents the media item created from the URL.</span></span> <span data-ttu-id="cbfa5-192">若要將專案排入佇列以進行播放，請將此指標傳遞給 [**IMFPMediaPlayer：： SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) 方法：</span><span class="sxs-lookup"><span data-stu-id="cbfa5-192">To queue the item for playback, pass this pointer to the [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) method:</span></span>


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



<span data-ttu-id="cbfa5-193">[ **MFP \_ 事件 \_ 類型 \_ MEDIAITEM \_ SET** ] 事件會通知應用程式 [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) 已完成。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-193">The **MFP\_EVENT\_TYPE\_MEDIAITEM\_SET** event notifies the application that [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) has completed.</span></span> <span data-ttu-id="cbfa5-194">呼叫 [**IMFPMediaPlayer：:P**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) 配置以開始播放：</span><span class="sxs-lookup"><span data-stu-id="cbfa5-194">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to start playback:</span></span>


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



## <a name="implement-winmain"></a><span data-ttu-id="cbfa5-195">執行 WinMain</span><span class="sxs-lookup"><span data-stu-id="cbfa5-195">Implement WinMain</span></span>

<span data-ttu-id="cbfa5-196">在本教學課程的其餘部分，沒有媒體基礎 Api 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-196">In the remainder of this tutorial, there are no calls to Media Foundation APIs.</span></span> <span data-ttu-id="cbfa5-197">下列程式碼顯示視窗程式：</span><span class="sxs-lookup"><span data-stu-id="cbfa5-197">The following code shows the window procedure:</span></span>


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



<span data-ttu-id="cbfa5-198">`InitializeWindow`函數會註冊應用程式的視窗類別並建立視窗。</span><span class="sxs-lookup"><span data-stu-id="cbfa5-198">The `InitializeWindow` function registers the application's window class and creates the window.</span></span>


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



<span data-ttu-id="cbfa5-199">最後，請執行應用程式進入點：</span><span class="sxs-lookup"><span data-stu-id="cbfa5-199">Finally, implement the application entry point:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="cbfa5-200">相關主題</span><span class="sxs-lookup"><span data-stu-id="cbfa5-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbfa5-201">使用 MFPlay 進行音訊/影片播放</span><span class="sxs-lookup"><span data-stu-id="cbfa5-201">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



