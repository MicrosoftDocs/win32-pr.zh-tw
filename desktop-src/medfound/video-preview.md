---
description: 本主題說明如何使用 MFPlay 來預覽攝影機的影片。
ms.assetid: ecf6113f-1d8e-4680-87ab-bfd45a9663e4
title: 影片預覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d458568a18f598e5aa4ee7e8fb21059e503362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974158"
---
# <a name="video-preview"></a><span data-ttu-id="88f83-103">影片預覽</span><span class="sxs-lookup"><span data-stu-id="88f83-103">Video Preview</span></span>

<span data-ttu-id="88f83-104">\[MFPlay 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="88f83-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="88f83-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="88f83-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="88f83-106">\]</span><span class="sxs-lookup"><span data-stu-id="88f83-106">\]</span></span>

<span data-ttu-id="88f83-107">本主題說明如何使用 MFPlay 來預覽攝影機的影片。</span><span class="sxs-lookup"><span data-stu-id="88f83-107">This topic describes how to use MFPlay to preview video from a video camera.</span></span>

<span data-ttu-id="88f83-108">MFPlay 提供最簡單的方式，讓您從「捕獲裝置」 Microsoft 媒體基礎預覽影片。</span><span class="sxs-lookup"><span data-stu-id="88f83-108">MFPlay provides the simplest way in Microsoft Media Foundation to preview video from a capture device.</span></span> <span data-ttu-id="88f83-109">如果下列條件都成立，則應該使用 MFPlay：</span><span class="sxs-lookup"><span data-stu-id="88f83-109">You should use MFPlay if the following conditions are all true:</span></span>

-   <span data-ttu-id="88f83-110">您不需要將影片捕獲到檔案。</span><span class="sxs-lookup"><span data-stu-id="88f83-110">You do not need to capture the video to a file.</span></span>
-   <span data-ttu-id="88f83-111">您不需要對影片的呈現方式進行細微的控制。</span><span class="sxs-lookup"><span data-stu-id="88f83-111">You do not need fine-grained control over how the video is rendered.</span></span> <span data-ttu-id="88f83-112"> (例如，您不需要控制建立 Direct3D 裝置。 ) </span><span class="sxs-lookup"><span data-stu-id="88f83-112">(For example, you do not need to control the creation of the Direct3D device.)</span></span>
-   <span data-ttu-id="88f83-113">在轉譯之前，您不需要處理相機的影片資料。</span><span class="sxs-lookup"><span data-stu-id="88f83-113">You do not need to process the video data from the camera prior to rendering.</span></span>

<span data-ttu-id="88f83-114">否則， [來源讀取器](source-reader.md) 可能會是更好的選項。</span><span class="sxs-lookup"><span data-stu-id="88f83-114">Otherwise, the [Source Reader](source-reader.md) may be a better option.</span></span>

<span data-ttu-id="88f83-115">若要使用 MFPlay 搭配影片捕獲裝置，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="88f83-115">To use MFPlay with a video capture device, perform the following steps:</span></span>

1.  <span data-ttu-id="88f83-116">建立 capture 裝置的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="88f83-116">Create a media source for the capture device.</span></span> <span data-ttu-id="88f83-117">請參閱 [列舉影片捕獲裝置](enumerating-video-capture-devices.md)。</span><span class="sxs-lookup"><span data-stu-id="88f83-117">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="88f83-118">呼叫 [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) 來建立 player 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="88f83-118">Call [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) to create an instance of the player object.</span></span>
3.  <span data-ttu-id="88f83-119">呼叫 [**IMFPMediaPlayer：： CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) 方法。</span><span class="sxs-lookup"><span data-stu-id="88f83-119">Call the [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) method.</span></span> <span data-ttu-id="88f83-120">將指標傳入媒體來源的 IMFMediaSource 介面。</span><span class="sxs-lookup"><span data-stu-id="88f83-120">Pass in a pointer to the IMFMediaSource interface of the media source.</span></span> <span data-ttu-id="88f83-121">方法會接收指向 [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="88f83-121">The method receives a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface.</span></span>
4.  <span data-ttu-id="88f83-122">呼叫 [**IMFPMediaPlayer：： SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem)。</span><span class="sxs-lookup"><span data-stu-id="88f83-122">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).</span></span>
5.  <span data-ttu-id="88f83-123">呼叫 [**IMFPMediaPlayer：:P 版面**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) 配置以開始預覽。</span><span class="sxs-lookup"><span data-stu-id="88f83-123">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to begin previewing.</span></span>

<span data-ttu-id="88f83-124">下列程式碼顯示這些步驟：</span><span class="sxs-lookup"><span data-stu-id="88f83-124">The following code shows these steps:</span></span>


```C++
    IMFPMediaItem *pItem = NULL;

    if (SUCCEEDED(hr))
    {
        hr = MFPCreateMediaPlayer(
            NULL,       // URL.
            FALSE,      // Do not start playback yet.
            0,          // Option flags.
            NULL,       // Callback interface.
            hwnd,
            &g_pPlayer
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromObject(
            g_pSource,
            TRUE,       // Blocking call.
            0,          // User data.
            &pItem
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->Play();
    }

    SafeRelease(&pItem);
```



<span data-ttu-id="88f83-125">在一般應用程式中，您會在 [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) 函式中提供回呼介面的指標，並使用回呼介面從播放程式取得事件。</span><span class="sxs-lookup"><span data-stu-id="88f83-125">In a typical application, you would provide a pointer to a callback interface in the [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) function, and use the callback interface to get events from the player.</span></span> <span data-ttu-id="88f83-126">為了簡單起見，此處所示的程式碼會略過這些步驟。</span><span class="sxs-lookup"><span data-stu-id="88f83-126">For simplicity, the code shown here skips these steps.</span></span> <span data-ttu-id="88f83-127">如需詳細資訊，請參閱 [使用 MFPlay 開始使用](getting-started-with-mfplay.md)。</span><span class="sxs-lookup"><span data-stu-id="88f83-127">For more information, see [Getting Started with MFPlay](getting-started-with-mfplay.md).</span></span>

### <a name="shutting-down"></a><span data-ttu-id="88f83-128">關閉</span><span class="sxs-lookup"><span data-stu-id="88f83-128">Shutting Down</span></span>

<span data-ttu-id="88f83-129">在應用程式結束之前，請關閉媒體來源和 player 物件，如下所示：</span><span class="sxs-lookup"><span data-stu-id="88f83-129">Before the application exits, shut down the media source and the player object as follows:</span></span>

1.  <span data-ttu-id="88f83-130">呼叫媒體來源上的 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) 。</span><span class="sxs-lookup"><span data-stu-id="88f83-130">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span>
2.  <span data-ttu-id="88f83-131">呼叫 player 物件上的 [**IMFPMediaPlayer：： Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) 。</span><span class="sxs-lookup"><span data-stu-id="88f83-131">Call [**IMFPMediaPlayer::Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) on the player object.</span></span>


```C++
    if (g_pSource)
    {
        g_pSource->Shutdown();
        g_pSource->Release();
        g_pSource = NULL;
    }

    if (g_pPlayer)
    {
        g_pPlayer->Shutdown();
        g_pPlayer->Release();
        g_pPlayer = NULL;
    }
```



## <a name="requirements"></a><span data-ttu-id="88f83-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="88f83-132">Requirements</span></span>

<span data-ttu-id="88f83-133">MFPlay 需要 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="88f83-133">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88f83-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="88f83-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88f83-135">MFPlay</span><span class="sxs-lookup"><span data-stu-id="88f83-135">MFPlay</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="88f83-136">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="88f83-136">Video Capture</span></span>](audio-video-capture.md)
</dt> </dl>

 

 



