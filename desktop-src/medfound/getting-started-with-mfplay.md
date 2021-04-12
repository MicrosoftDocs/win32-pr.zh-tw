---
description: MFPlay 是在 c + + 中建立媒體播放應用程式的 API。
ms.assetid: 55612f49-5995-4bdf-aa12-8a853e5a2b24
title: 使用 MFPlay 開始使用
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9e0405d3138a22e0d20e94849d416b29d62945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468617"
---
# <a name="getting-started-with-mfplay"></a><span data-ttu-id="bae60-103">使用 MFPlay 開始使用</span><span class="sxs-lookup"><span data-stu-id="bae60-103">Getting Started with MFPlay</span></span>

<span data-ttu-id="bae60-104">\[MFPlay 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="bae60-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bae60-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="bae60-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="bae60-106">\]</span><span class="sxs-lookup"><span data-stu-id="bae60-106">\]</span></span>

<span data-ttu-id="bae60-107">MFPlay 是在 c + + 中建立媒體播放應用程式的 API。</span><span class="sxs-lookup"><span data-stu-id="bae60-107">MFPlay is an API for creating media playback applications in C++.</span></span>

<span data-ttu-id="bae60-108">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="bae60-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="bae60-109">需求</span><span class="sxs-lookup"><span data-stu-id="bae60-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="bae60-110">關於 MFPlay</span><span class="sxs-lookup"><span data-stu-id="bae60-110">About MFPlay</span></span>](#about-mfplay)
-   [<span data-ttu-id="bae60-111">播放媒體檔案</span><span class="sxs-lookup"><span data-stu-id="bae60-111">Playing a Media File</span></span>](#playing-a-media-file)
-   [<span data-ttu-id="bae60-112">控制播放</span><span class="sxs-lookup"><span data-stu-id="bae60-112">Controlling Playback</span></span>](#controlling-playback)
-   [<span data-ttu-id="bae60-113">從播放玩家接收事件</span><span class="sxs-lookup"><span data-stu-id="bae60-113">Receiving Events From the Player</span></span>](#receiving-events-from-the-player)
-   [<span data-ttu-id="bae60-114">取得媒體檔案的相關資訊</span><span class="sxs-lookup"><span data-stu-id="bae60-114">Getting Information About a Media File</span></span>](#getting-information-about-a-media-file)
-   [<span data-ttu-id="bae60-115">管理影片播放</span><span class="sxs-lookup"><span data-stu-id="bae60-115">Managing Video Playback</span></span>](#managing-video-playback)
-   [<span data-ttu-id="bae60-116">MFPlay 的限制</span><span class="sxs-lookup"><span data-stu-id="bae60-116">Limitations of MFPlay</span></span>](#limitations-of-mfplay)
-   [<span data-ttu-id="bae60-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="bae60-117">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="bae60-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="bae60-118">Requirements</span></span>

<span data-ttu-id="bae60-119">MFPlay 需要 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="bae60-119">MFPlay requires Windows 7.</span></span>

## <a name="about-mfplay"></a><span data-ttu-id="bae60-120">關於 MFPlay</span><span class="sxs-lookup"><span data-stu-id="bae60-120">About MFPlay</span></span>

<span data-ttu-id="bae60-121">MFPlay 具有簡單的程式設計模型，同時提供大部分播放應用程式所需的核心功能集。</span><span class="sxs-lookup"><span data-stu-id="bae60-121">MFPlay has a simple programming model, while providing the core set of features that most playback applications need.</span></span> <span data-ttu-id="bae60-122">應用程式會建立控制播放的 *播放* 程式物件。</span><span class="sxs-lookup"><span data-stu-id="bae60-122">An application creates a *player* object that controls playback.</span></span> <span data-ttu-id="bae60-123">為了播放媒體檔案，player 物件會建立 *媒體專案*，可用來取得媒體檔案內容的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bae60-123">To play a media file, the player object creates a *media item*, which can be used to get information about the contents of the media file.</span></span> <span data-ttu-id="bae60-124">應用程式會透過 player 物件之 [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) 介面上的方法來控制播放。</span><span class="sxs-lookup"><span data-stu-id="bae60-124">The application controls playback through methods on the player object's [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span> <span data-ttu-id="bae60-125">（選擇性）應用程式可以透過回呼介面取得事件通知，下圖說明此程式。</span><span class="sxs-lookup"><span data-stu-id="bae60-125">Optionally, the application can get event notifications through a callback interface The following diagram illustrates this process.</span></span>

![概念圖：應用程式和播放機會指向彼此，並指向媒體專案，以指向媒體檔案](images/mfplay.png)

## <a name="playing-a-media-file"></a><span data-ttu-id="bae60-127">播放媒體檔案</span><span class="sxs-lookup"><span data-stu-id="bae60-127">Playing a Media File</span></span>

<span data-ttu-id="bae60-128">若要播放媒體檔案，請呼叫 [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) 函式。</span><span class="sxs-lookup"><span data-stu-id="bae60-128">To play a media file, call the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span>


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



<span data-ttu-id="bae60-129">[**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer)函式會建立 MFPlay player 物件的新實例。</span><span class="sxs-lookup"><span data-stu-id="bae60-129">The [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function creates a new instance of the MFPlay player object.</span></span> <span data-ttu-id="bae60-130">函數會採用下列參數：</span><span class="sxs-lookup"><span data-stu-id="bae60-130">The function takes the following parameters:</span></span>

-   <span data-ttu-id="bae60-131">第一個參數是要開啟之檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="bae60-131">The first parameter is the URL of the file to open.</span></span> <span data-ttu-id="bae60-132">這可以是本機檔案或媒體伺服器上的檔案。</span><span class="sxs-lookup"><span data-stu-id="bae60-132">This can be a local file or a file on a media server.</span></span>
-   <span data-ttu-id="bae60-133">第二個參數指定播放是否自動啟動。</span><span class="sxs-lookup"><span data-stu-id="bae60-133">The second parameter specifies whether playback starts automatically.</span></span> <span data-ttu-id="bae60-134">藉由將此參數設為 **TRUE**，檔案會在 MFPlay 載入時立即播放。</span><span class="sxs-lookup"><span data-stu-id="bae60-134">By setting this paremeter to **TRUE**, the file will play as soon as MFPlay loads it.</span></span>
-   <span data-ttu-id="bae60-135">第三個參數會設定各種選項。</span><span class="sxs-lookup"><span data-stu-id="bae60-135">The third parameter sets various options.</span></span> <span data-ttu-id="bae60-136">若為預設選項，請傳遞零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="bae60-136">For the default options, pass zero (0).</span></span>
-   <span data-ttu-id="bae60-137">第四個參數是選擇性回呼介面的指標。</span><span class="sxs-lookup"><span data-stu-id="bae60-137">The fourth parameter is a pointer to an optional callback interface.</span></span> <span data-ttu-id="bae60-138">這個參數可以是 **Null**，如下所示。</span><span class="sxs-lookup"><span data-stu-id="bae60-138">This parameter can be **NULL**, as shown.</span></span> <span data-ttu-id="bae60-139">回呼會在 [從播放程式接收事件](#receiving-events-from-the-player)的區段中描述。</span><span class="sxs-lookup"><span data-stu-id="bae60-139">The callback is described in the section [Receiving Events From the Player](#receiving-events-from-the-player).</span></span>
-   <span data-ttu-id="bae60-140">第五個參數是應用程式視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="bae60-140">The fifth parameter is a handle to the application window.</span></span> <span data-ttu-id="bae60-141">如果媒體檔案包含影片串流，影片將會出現在此視窗的工作區中。</span><span class="sxs-lookup"><span data-stu-id="bae60-141">If the media file contains a video stream, the video will appear inside the client area of this window.</span></span> <span data-ttu-id="bae60-142">針對僅限音訊播放，此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bae60-142">For audio-only playback, this parameter can be **NULL**.</span></span>

<span data-ttu-id="bae60-143">最後一個參數會接收 player 物件之 [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="bae60-143">The last parameter receives a pointer to the player object's [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span>

<span data-ttu-id="bae60-144">在應用程式關閉之前，請務必釋放 [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) 指標。</span><span class="sxs-lookup"><span data-stu-id="bae60-144">Before the application shuts down, be sure to release the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) pointer.</span></span> <span data-ttu-id="bae60-145">您可以在 **WM \_ 關閉** 訊息處理常式中完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="bae60-145">You can do this in your **WM\_CLOSE** message handler.</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



> [!Note]  
> <span data-ttu-id="bae60-146">此範例會使用 [SafeRelease](saferelease.md) 函式來釋放介面指標。</span><span class="sxs-lookup"><span data-stu-id="bae60-146">This example uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span>

 

<span data-ttu-id="bae60-147">針對簡單的影片播放，這就是您所需的所有程式碼。</span><span class="sxs-lookup"><span data-stu-id="bae60-147">For simple video playback, that's all the code you need.</span></span> <span data-ttu-id="bae60-148">本教學課程的其餘部分將說明如何新增更多功能，從如何控制播放開始。</span><span class="sxs-lookup"><span data-stu-id="bae60-148">The rest of this tutorial will show how to add more features, starting with how to control playback.</span></span>

## <a name="controlling-playback"></a><span data-ttu-id="bae60-149">控制播放</span><span class="sxs-lookup"><span data-stu-id="bae60-149">Controlling Playback</span></span>

<span data-ttu-id="bae60-150">上一節所顯示的程式碼將會播放媒體檔案，直到到達檔案結尾為止。</span><span class="sxs-lookup"><span data-stu-id="bae60-150">The code shown in the previous section will play the media file until it reaches the end of the file.</span></span> <span data-ttu-id="bae60-151">您可以在 [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) 介面上呼叫下列方法，以停止並開始播放：</span><span class="sxs-lookup"><span data-stu-id="bae60-151">You can stop and start playback by calling the following methods on the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface:</span></span>

-   <span data-ttu-id="bae60-152">[**IMFPMediaPlayer：:P ause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) 會暫停播放。</span><span class="sxs-lookup"><span data-stu-id="bae60-152">[**IMFPMediaPlayer::Pause**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause) pauses playback.</span></span> <span data-ttu-id="bae60-153">播放暫停時，會顯示最新的影片畫面，且音訊為無訊息。</span><span class="sxs-lookup"><span data-stu-id="bae60-153">While playback is paused, the most recent video frame is displayed, and audio is silent.</span></span>
-   <span data-ttu-id="bae60-154">[**IMFPMediaPlayer：： Stop**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) 停止播放。</span><span class="sxs-lookup"><span data-stu-id="bae60-154">[**IMFPMediaPlayer::Stop**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop) stops playback.</span></span> <span data-ttu-id="bae60-155">不會顯示任何影片，而且播放位置會重設為檔案的開頭。</span><span class="sxs-lookup"><span data-stu-id="bae60-155">No video is displayed, and the playback position resets to the start of the file.</span></span>
-   <span data-ttu-id="bae60-156">[**IMFPMediaPlayer：:P**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) 配置在停止或暫停之後繼續播放。</span><span class="sxs-lookup"><span data-stu-id="bae60-156">[**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) resumes playback after stopping or pausing.</span></span>

<span data-ttu-id="bae60-157">當您按下 **空格鍵** 時，下列程式碼會暫停或繼續播放。</span><span class="sxs-lookup"><span data-stu-id="bae60-157">The following code pauses or resumes playback when you press the **SPACEBAR**.</span></span>


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



<span data-ttu-id="bae60-158">此範例會呼叫 [**IMFPMediaPlayer：： >getstate**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) 方法，以取得目前的播放狀態 (暫停、停止或播放) ，並據以暫停或繼續。</span><span class="sxs-lookup"><span data-stu-id="bae60-158">This example calls the [**IMFPMediaPlayer::GetState**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate) method to get the current playback state (paused, stopped, or playing) and pauses or resumes accordingly.</span></span>

## <a name="receiving-events-from-the-player"></a><span data-ttu-id="bae60-159">從播放玩家接收事件</span><span class="sxs-lookup"><span data-stu-id="bae60-159">Receiving Events From the Player</span></span>

<span data-ttu-id="bae60-160">MFPlay 使用回呼介面將事件傳送至您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="bae60-160">MFPlay uses a callback interface to send events to your application.</span></span> <span data-ttu-id="bae60-161">此回呼有兩個原因：</span><span class="sxs-lookup"><span data-stu-id="bae60-161">There are two reasons for this callback:</span></span>

-   <span data-ttu-id="bae60-162">播放會在個別的執行緒上執行。</span><span class="sxs-lookup"><span data-stu-id="bae60-162">Playback occurs on a separate thread.</span></span> <span data-ttu-id="bae60-163">在播放期間，某些事件可能會發生，例如到達檔案結尾。</span><span class="sxs-lookup"><span data-stu-id="bae60-163">During playback, certain events might occur, such as reaching the end of the file.</span></span> <span data-ttu-id="bae60-164">MFPlay 使用回呼來通知您應用程式的事件。</span><span class="sxs-lookup"><span data-stu-id="bae60-164">MFPlay uses the callback to notify your application of the event.</span></span>
-   <span data-ttu-id="bae60-165">許多 [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) 方法都是非同步，這表示它們會在作業完成之前傳回。</span><span class="sxs-lookup"><span data-stu-id="bae60-165">Many of the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) methods are asynchronous, meaning they return before the operation completes.</span></span> <span data-ttu-id="bae60-166">非同步方法可讓您從 UI 執行緒啟動作業，此作業可能需要很長的時間才能完成，而不會造成 UI 封鎖。</span><span class="sxs-lookup"><span data-stu-id="bae60-166">Asynchronous methods let you start an operation from your UI thread that might take a long time to complete, without it causing your UI to block.</span></span> <span data-ttu-id="bae60-167">作業完成之後，MFPlay 會發出回呼的信號。</span><span class="sxs-lookup"><span data-stu-id="bae60-167">After the operation completes, MFPlay signals the callback.</span></span>

<span data-ttu-id="bae60-168">若要接收回呼通知，請執行 [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) 介面。</span><span class="sxs-lookup"><span data-stu-id="bae60-168">To receive callback notifications, implement the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="bae60-169">此介面會繼承 **IUnknown** 並定義單一方法 [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent)。</span><span class="sxs-lookup"><span data-stu-id="bae60-169">This interface inherits **IUnknown** and defines a single method, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span></span> <span data-ttu-id="bae60-170">若要設定回呼，請在 [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer)函式的 *pCallback* 參數中傳遞 **IMFPMediaPlayerCallback** 執行的指標。</span><span class="sxs-lookup"><span data-stu-id="bae60-170">To set up the callback, pass a pointer to your **IMFPMediaPlayerCallback** implementation in the *pCallback* parameter of the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span>

<span data-ttu-id="bae60-171">以下是本教學課程中的第一個範例，修改為包含回呼。</span><span class="sxs-lookup"><span data-stu-id="bae60-171">Here is the first example from this tutorial, modified to include the callback.</span></span>


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



<span data-ttu-id="bae60-172">[**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent)方法具有單一參數，也就是 [**MFP \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="bae60-172">The [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method has a single parameter, which is a pointer to the [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="bae60-173">此結構的 **eEventType** 成員會告知您發生了哪些事件。</span><span class="sxs-lookup"><span data-stu-id="bae60-173">The **eEventType** member of this structure tells you which event occurred.</span></span> <span data-ttu-id="bae60-174">例如，當播放開始時，MFPlay 會傳送「 **MFP \_ 事件種類」 \_ \_ 播放** 事件。</span><span class="sxs-lookup"><span data-stu-id="bae60-174">For example, when playback starts, MFPlay sends the **MFP\_EVENT\_TYPE\_PLAY** event.</span></span>

<span data-ttu-id="bae60-175">每個事件種類都有對應的資料結構，其中包含該事件的資訊。</span><span class="sxs-lookup"><span data-stu-id="bae60-175">Each event type has a corresponding data structure that contains information for that event.</span></span> <span data-ttu-id="bae60-176">這些結構都會以 [**MFP \_ 事件 \_ 標頭**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) 結構作為開頭。</span><span class="sxs-lookup"><span data-stu-id="bae60-176">Each of these structures starts with an [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="bae60-177">在您的回呼中，將 [ **MFP] \_ 事件 \_ 標頭** 指標轉換為事件特定的資料結構。</span><span class="sxs-lookup"><span data-stu-id="bae60-177">In your callback, cast the **MFP\_EVENT\_HEADER** pointer to the event-specific data structure.</span></span> <span data-ttu-id="bae60-178">例如，如果事件種類是「 **mfp \_ play」 \_ 事件**，資料結構就是「 [**mfp 播放」 \_ \_ 事件**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event)。</span><span class="sxs-lookup"><span data-stu-id="bae60-178">For example, if the event type is **MFP\_PLAY\_EVENT**, the data structure is [**MFP\_PLAY\_EVENT**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event).</span></span> <span data-ttu-id="bae60-179">下列程式碼顯示如何在回呼中處理這個事件。</span><span class="sxs-lookup"><span data-stu-id="bae60-179">The following code shows how to handle this event in the callback.</span></span>


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



<span data-ttu-id="bae60-180">此範例會使用「 [**mfp \_ 取得 \_ play \_ 事件**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) 」事件，將 *pEventHeader* 指標轉型為 [**MFP \_ PLAY \_ 事件**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) 結構。</span><span class="sxs-lookup"><span data-stu-id="bae60-180">This example uses the [**MFP\_GET\_PLAY\_EVENT**](/windows/desktop/api/mfplay/nf-mfplay-mfp_get_play_event) event to cast the *pEventHeader* pointer to an [**MFP\_PLAY\_EVENT**](/windows/desktop/api/mfplay/ns-mfplay-mfp_play_event) structure.</span></span> <span data-ttu-id="bae60-181">觸發事件之作業的 **HRESULT** 會儲存在結構的 **hrEvent** 欄位中。</span><span class="sxs-lookup"><span data-stu-id="bae60-181">The **HRESULT** from the operation that triggered the event is stored in the **hrEvent** field of the structure.</span></span>

<span data-ttu-id="bae60-182">如需所有事件種類和對應資料結構的清單，請參閱 [**MFP \_ 事件 \_ 類型**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type)。</span><span class="sxs-lookup"><span data-stu-id="bae60-182">For a list of all the event types and the corresponding data structures, see [**MFP\_EVENT\_TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).</span></span>

<span data-ttu-id="bae60-183">有關執行緒的附注：根據預設，MFPlay 會從呼叫 [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer)的相同執行緒叫用回呼。</span><span class="sxs-lookup"><span data-stu-id="bae60-183">A note about threading: By default, MFPlay invokes the callback from the same thread that called [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer).</span></span> <span data-ttu-id="bae60-184">此執行緒必須有訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="bae60-184">This thread must have a message loop.</span></span> <span data-ttu-id="bae60-185">或者，您可以在 **MFPCreateMediaPlayer** 的 *creationOptions* 參數中傳遞 **MFP \_ 選項 \_ 自由 \_ 執行緒 \_ 回呼** 旗標。</span><span class="sxs-lookup"><span data-stu-id="bae60-185">Alternatively, you can pass the **MFP\_OPTION\_FREE\_THREADED\_CALLBACK** flag in the *creationOptions* parameter of **MFPCreateMediaPlayer**.</span></span> <span data-ttu-id="bae60-186">此旗標會使 MFPlay 叫用來自不同執行緒的回呼。</span><span class="sxs-lookup"><span data-stu-id="bae60-186">This flag causes MFPlay to invoke callbacks from a separate thread.</span></span> <span data-ttu-id="bae60-187">任一個選項對您的應用程式都有影響。</span><span class="sxs-lookup"><span data-stu-id="bae60-187">Either option has implications for your application.</span></span> <span data-ttu-id="bae60-188">預設選項表示您的回呼無法執行任何動作，因為它會封鎖您的視窗程式，而不會等候您的訊息迴圈，例如等待 UI 動作。</span><span class="sxs-lookup"><span data-stu-id="bae60-188">The default option means your callback cannot do anything that waits on your message loop, such as waiting for a UI action, because that will block your window procedure.</span></span> <span data-ttu-id="bae60-189">無限制執行緒選項表示您需要使用重要區段來保護您在回呼中存取的任何資料。</span><span class="sxs-lookup"><span data-stu-id="bae60-189">The free-threaded option means you need to use critical sections to protect any data that you access in your callback.</span></span> <span data-ttu-id="bae60-190">在大部分的情況下，預設選項是最簡單的。</span><span class="sxs-lookup"><span data-stu-id="bae60-190">In most cases, the default option is simplest.</span></span>

## <a name="getting-information-about-a-media-file"></a><span data-ttu-id="bae60-191">取得媒體檔案的相關資訊</span><span class="sxs-lookup"><span data-stu-id="bae60-191">Getting Information About a Media File</span></span>

<span data-ttu-id="bae60-192">當您在 MFPlay 中開啟媒體檔案時，播放程式會建立一個稱為 *媒體專案* 的物件，代表媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="bae60-192">When you open a media file in MFPlay, the player creates an object called a *media item* that represents the media file.</span></span> <span data-ttu-id="bae60-193">此物件會公開 [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) 介面，可讓您用來取得媒體檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bae60-193">This object exposes the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface, which you can use to get information about the media file.</span></span> <span data-ttu-id="bae60-194">許多 MFPlay 事件結構都包含指向目前媒體專案的指標。</span><span class="sxs-lookup"><span data-stu-id="bae60-194">Many of the MFPlay event structures contain a pointer to the current media item.</span></span> <span data-ttu-id="bae60-195">您也可以在播放程式上呼叫 [**IMFPMediaPlayer：： GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) ，以取得目前的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="bae60-195">You can also get the current media item by calling [**IMFPMediaPlayer::GetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem) on the player.</span></span>

<span data-ttu-id="bae60-196">有兩個特別有用的方法是 [**IMFPMediaItem：： HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) 和 [**IMFPMediaItem：： HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio)。</span><span class="sxs-lookup"><span data-stu-id="bae60-196">Two particularly useful methods are [**IMFPMediaItem::HasVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo) and [**IMFPMediaItem::HasAudio**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio).</span></span> <span data-ttu-id="bae60-197">這些方法會查詢媒體來源是否包含影片或音訊。</span><span class="sxs-lookup"><span data-stu-id="bae60-197">These methods query whether the media source contains video or audio.</span></span>

<span data-ttu-id="bae60-198">例如，下列程式碼會測試目前的媒體檔案是否包含影片串流。</span><span class="sxs-lookup"><span data-stu-id="bae60-198">For example, the following code tests whether the current media file contains a video stream.</span></span>


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



<span data-ttu-id="bae60-199">如果來源檔案包含已選取要播放的影片資料流程， *bHasVideo* 和 *bIsSelected* 都設為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="bae60-199">If the source file contains a video stream that is selected for playback, *bHasVideo* and *bIsSelected* are both set to **TRUE**.</span></span>

## <a name="managing-video-playback"></a><span data-ttu-id="bae60-200">管理影片播放</span><span class="sxs-lookup"><span data-stu-id="bae60-200">Managing Video Playback</span></span>

<span data-ttu-id="bae60-201">當 MFPlay 播放影片檔案時，它會在您于 [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) 函式中指定的視窗內繪製影片。</span><span class="sxs-lookup"><span data-stu-id="bae60-201">When MFPlay plays a video file, it draws the video in the window that you specified in the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function.</span></span> <span data-ttu-id="bae60-202">這會發生在 Microsoft 媒體基礎播放管線所擁有的另一個執行緒上。</span><span class="sxs-lookup"><span data-stu-id="bae60-202">This occurs on a separate thread owned by the Microsoft Media Foundation playback pipeline.</span></span> <span data-ttu-id="bae60-203">在大部分的情況下，您的應用程式不需要管理此進程。</span><span class="sxs-lookup"><span data-stu-id="bae60-203">For the most part, your application does not need to manage this process.</span></span> <span data-ttu-id="bae60-204">不過，在兩種情況下，應用程式必須通知 MFPlay 更新影片。</span><span class="sxs-lookup"><span data-stu-id="bae60-204">However, there are two situations where the application must notify MFPlay to update the video.</span></span>

-   <span data-ttu-id="bae60-205">如果播放暫停或停止，MFPlay 必須在應用程式的影片視窗收到 WM 油漆訊息時收到通知 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bae60-205">If playback is paused or stopped, MFPlay must be notified whenever the application's video window receives a WM\_PAINT message.</span></span> <span data-ttu-id="bae60-206">這可讓 MFPlay 重新繪製視窗。</span><span class="sxs-lookup"><span data-stu-id="bae60-206">This allows MFPlay to repaint the window.</span></span>
-   <span data-ttu-id="bae60-207">如果調整視窗的大小，則必須通知 MFPlay，讓它可以調整影片以符合新的視窗大小。</span><span class="sxs-lookup"><span data-stu-id="bae60-207">If the window is resized, MFPlay must be notified so that it can scale the video to match the new window size.</span></span>

<span data-ttu-id="bae60-208">[**IMFPMediaPlayer：： UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo)方法會處理這兩種情況。</span><span class="sxs-lookup"><span data-stu-id="bae60-208">The [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) method handles both cases.</span></span> <span data-ttu-id="bae60-209">在適用于影片視窗的 WM \_ 油漆和 wm \_ 大小訊息處理常式內，呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="bae60-209">Call this method inside both the WM\_PAINT and WM\_SIZE message handlers for the video window.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bae60-210">呼叫 GDI **BeginPaint** 函式之前，請先呼叫 [**UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo)。</span><span class="sxs-lookup"><span data-stu-id="bae60-210">Call the GDI **BeginPaint** function before calling [**UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span></span>

 


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



<span data-ttu-id="bae60-211">除非您另外指定，否則 MFPlay 會使用上下黑邊縮（如有需要）顯示正確的外觀比例的影片。</span><span class="sxs-lookup"><span data-stu-id="bae60-211">Unless you specify otherwise, MFPlay shows the video at the correct aspect ratio, using letterboxing if needed.</span></span> <span data-ttu-id="bae60-212">如果您不想要保留長寬比，請使用 **MFVideoARMode \_ None** 旗標來呼叫 [**IMFPMediaPlayer：： SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) 。</span><span class="sxs-lookup"><span data-stu-id="bae60-212">If you do not want to preserve the aspect ratio, call [**IMFPMediaPlayer::SetAspectRatioMode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode) with the **MFVideoARMode\_None** flag.</span></span> <span data-ttu-id="bae60-213">這會導致 MFPlay 延展影片以填滿整個矩形，而不會上下黑邊縮。</span><span class="sxs-lookup"><span data-stu-id="bae60-213">This will cause MFPlay to stretch the video to fill the entire rectangle, with no letterboxing.</span></span> <span data-ttu-id="bae60-214">一般來說，您應該使用預設設定，讓 MFPlay 黑邊影片。</span><span class="sxs-lookup"><span data-stu-id="bae60-214">Typically you should use the default setting and let MFPlay letterbox the video.</span></span> <span data-ttu-id="bae60-215">預設黑邊色彩為黑色，但您可以藉由呼叫 [**IMFPMediaPlayer：： SetBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor)來變更。</span><span class="sxs-lookup"><span data-stu-id="bae60-215">The default letterbox color is black, but you can change this by calling [**IMFPMediaPlayer::SetBorderColor**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor).</span></span>

## <a name="limitations-of-mfplay"></a><span data-ttu-id="bae60-216">MFPlay 的限制</span><span class="sxs-lookup"><span data-stu-id="bae60-216">Limitations of MFPlay</span></span>

<span data-ttu-id="bae60-217">目前的 MFPlay 版本具有下列限制：</span><span class="sxs-lookup"><span data-stu-id="bae60-217">The current version of MFPlay has the following limitations:</span></span>

-   <span data-ttu-id="bae60-218">MFPlay 不支援受 DRM 保護的內容。</span><span class="sxs-lookup"><span data-stu-id="bae60-218">MFPlay does not support DRM-protected content.</span></span>
-   <span data-ttu-id="bae60-219">根據預設，MFPlay 不支援網路串流通訊協定。</span><span class="sxs-lookup"><span data-stu-id="bae60-219">By default, MFPlay does not support network streaming protocols.</span></span> <span data-ttu-id="bae60-220">如需詳細資訊，請參閱 [**IMFPMediaPlayer：： CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)。</span><span class="sxs-lookup"><span data-stu-id="bae60-220">For more information, see [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span></span>
-   <span data-ttu-id="bae60-221">MFPlay 不支援伺服器端播放清單， (SSPLs) 或其他播放多個區段的來源類型。</span><span class="sxs-lookup"><span data-stu-id="bae60-221">MFPlay does not support server-side playlists (SSPLs) or other types of source that play more than one segment.</span></span> <span data-ttu-id="bae60-222">在技術方面，MFPlay 會在第一次簡報之後停止播放，並忽略媒體來源中的任何 [MENewPresentation](menewpresentation.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="bae60-222">In technical terms, MFPlay stops playback after the first presentation, and ignores any [MENewPresentation](menewpresentation.md) events from the media source.</span></span>
-   <span data-ttu-id="bae60-223">MFPlay 不支援媒體來源之間的無縫轉換。</span><span class="sxs-lookup"><span data-stu-id="bae60-223">MFPlay does not support seamless transitions between media sources.</span></span>
-   <span data-ttu-id="bae60-224">MFPlay 不支援混合多個影片串流。</span><span class="sxs-lookup"><span data-stu-id="bae60-224">MFPlay does not support mixing multiple video streams.</span></span>
-   <span data-ttu-id="bae60-225">MFPlay 只支援在媒體基礎中以原生方式支援的媒體格式。</span><span class="sxs-lookup"><span data-stu-id="bae60-225">Only media formats supported natively in Media Foundation are supported by MFPlay.</span></span> <span data-ttu-id="bae60-226"> (包括可能安裝在系統上的協力廠商媒體基礎元件 ) </span><span class="sxs-lookup"><span data-stu-id="bae60-226">(This includes third-party Media Foundation components that might be installed on the system.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="bae60-227">相關主題</span><span class="sxs-lookup"><span data-stu-id="bae60-227">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bae60-228">使用 MFPlay 進行音訊/影片播放</span><span class="sxs-lookup"><span data-stu-id="bae60-228">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



