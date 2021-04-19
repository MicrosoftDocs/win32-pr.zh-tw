---
description: 本主題說明如何使用 MFPlay 播放一連串音訊/影片檔案。
ms.assetid: ee16eaa3-0506-4444-b139-f8a8498d6597
title: 如何播放一連串的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dc4d1523be4cc6cc09416096af260c9eae736c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979099"
---
# <a name="how-to-play-a-sequence-of-files"></a><span data-ttu-id="ed585-103">如何播放一連串的檔案</span><span class="sxs-lookup"><span data-stu-id="ed585-103">How to Play a Sequence of Files</span></span>

<span data-ttu-id="ed585-104">\[MFPlay 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="ed585-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ed585-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="ed585-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="ed585-106">\]</span><span class="sxs-lookup"><span data-stu-id="ed585-106">\]</span></span>

<span data-ttu-id="ed585-107">本主題說明如何使用 MFPlay 播放一連串音訊/影片檔案。</span><span class="sxs-lookup"><span data-stu-id="ed585-107">This topic describes how to play a sequence of audio/video files using MFPlay.</span></span>


<span data-ttu-id="ed585-108">[MFPlay 開始使用](getting-started-with-mfplay.md)的主題顯示如何播放單一媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="ed585-108">The topic [Getting Started with MFPlay](getting-started-with-mfplay.md) shows how to play a single media file.</span></span> <span data-ttu-id="ed585-109">您也可以使用 MFPlay 來播放一連串的檔案。</span><span class="sxs-lookup"><span data-stu-id="ed585-109">You can also use MFPlay to play a sequence of files.</span></span>

### <a name="synchronous-blocking-method"></a><span data-ttu-id="ed585-110">同步 (封鎖) 方法</span><span class="sxs-lookup"><span data-stu-id="ed585-110">Synchronous (Blocking) Method</span></span>

1.  <span data-ttu-id="ed585-111">呼叫 [**IMFPMediaPlayer：： CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) 方法。</span><span class="sxs-lookup"><span data-stu-id="ed585-111">Call the [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method.</span></span> <span data-ttu-id="ed585-112">方法會建立一個媒體專案。</span><span class="sxs-lookup"><span data-stu-id="ed585-112">The method creates a media item.</span></span>
2.  <span data-ttu-id="ed585-113">呼叫 [**IMFPMediaPlayer：： SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) ，將媒體專案排入佇列以供播放。</span><span class="sxs-lookup"><span data-stu-id="ed585-113">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) to queue the media item for playback.</span></span>
3.  <span data-ttu-id="ed585-114">呼叫 [**IMFPMediaPlayer：:P**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) 配置以開始播放。</span><span class="sxs-lookup"><span data-stu-id="ed585-114">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to start playback.</span></span>

<span data-ttu-id="ed585-115">下列程式碼顯示這些步驟。</span><span class="sxs-lookup"><span data-stu-id="ed585-115">These steps are shown in the following code.</span></span>


```C++
HRESULT OpenMediaFile(IMFPMediaPlayer *pPlayer, PCWSTR pwszURL)
{
    HRESULT hr = S_OK;
    
    IMFPMediaItem *pItem = NULL;

    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        TRUE,  // Blocking call
        0,     // User data.
        &pItem
        );

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pPlayer->Play();
    }

    if (pItem)
    {
        pItem->Release();
    }
    return hr;
}
```



<span data-ttu-id="ed585-116">[**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)方法會採用下列參數：</span><span class="sxs-lookup"><span data-stu-id="ed585-116">The [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method takes the following parameters:</span></span>

-   <span data-ttu-id="ed585-117">第一個參數是檔案的 URL。</span><span class="sxs-lookup"><span data-stu-id="ed585-117">The first parameter is the URL of the file.</span></span>
-   <span data-ttu-id="ed585-118">第二個參數會指定方法是否封鎖。</span><span class="sxs-lookup"><span data-stu-id="ed585-118">The second parameter specifies whether the method blocks.</span></span> <span data-ttu-id="ed585-119">如果指定值 **TRUE**（如下所示），則會導致方法封鎖，直到建立媒體專案為止。</span><span class="sxs-lookup"><span data-stu-id="ed585-119">Specifying the value **TRUE**, as shown here, causes the method to block until the media item is created.</span></span>
-   <span data-ttu-id="ed585-120">第三個參數會將任意 **DWORD \_ 指標** 值與媒體專案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="ed585-120">The third parameter associates an arbitrary **DWORD\_PTR** value with the media item.</span></span> <span data-ttu-id="ed585-121">您稍後可以藉由呼叫 [**IMFPMediaItem：： GetUserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata)來取得此值。</span><span class="sxs-lookup"><span data-stu-id="ed585-121">You can get this value later by calling [**IMFPMediaItem::GetUserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).</span></span>
-   <span data-ttu-id="ed585-122">第四個參數會接收媒體專案之 [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="ed585-122">The fourth parameter receives a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface of the media item.</span></span>

### <a name="asynchronous-non-blocking-method"></a><span data-ttu-id="ed585-123">非同步 (非封鎖) 方法</span><span class="sxs-lookup"><span data-stu-id="ed585-123">Asynchronous (Non-Blocking) Method</span></span>

<span data-ttu-id="ed585-124">如果您從 UI 執行緒呼叫 [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) ，請避免封鎖選項，因為它可能需要花費相當長的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="ed585-124">Avoid the blocking option if you call [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) from your UI thread, because it can take a noticeable amount of time to complete.</span></span> <span data-ttu-id="ed585-125">方法通常會開啟檔案或網路連線，並讀取足夠的資料來剖析檔案標頭，這一切都需要一些時間。</span><span class="sxs-lookup"><span data-stu-id="ed585-125">The method typically opens a file or network connection and reads enough data to parse the file headers, all of which can take time.</span></span> <span data-ttu-id="ed585-126">因此，通常最好是將第二個參數設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ed585-126">Therefore, it is generally better to set the second parameter to **FALSE**.</span></span> <span data-ttu-id="ed585-127">此選項會使方法以非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="ed585-127">This option causes the method to perform asynchronously.</span></span> <span data-ttu-id="ed585-128">使用非同步選項時，最後一個參數必須是 **Null**：</span><span class="sxs-lookup"><span data-stu-id="ed585-128">When the asynchronous option is used, the last parameter must be **NULL**:</span></span>


```C++
    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        FALSE,  // Non-blocking call.
        0,      // User data.
        NULL    // Must be NULL for the non-blocking call.
        );
```



<span data-ttu-id="ed585-129">建立媒體專案時，您的應用程式會收到 **\_ \_ \_ MEDIAITEM \_ 建立事件的 MFP 事件種類** 。</span><span class="sxs-lookup"><span data-stu-id="ed585-129">When the media item is created, your application receives an **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event.</span></span> <span data-ttu-id="ed585-130">此事件的資料結構包含媒體專案的指標。</span><span class="sxs-lookup"><span data-stu-id="ed585-130">The data structure for this event contains a pointer to the media item.</span></span> <span data-ttu-id="ed585-131">將此指標傳遞至 [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) 方法，以將專案排入佇列以供播放。</span><span class="sxs-lookup"><span data-stu-id="ed585-131">Pass this pointer to the [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) method to queue the item for playback.</span></span>


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    HRESULT hr = S_OK;
    if (FAILED(pEvent->header.hrEvent))
    {
        // Handle error. (Not shown.)
    }
    else
    {
        hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
    }
}
```



## <a name="requirements"></a><span data-ttu-id="ed585-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed585-132">Requirements</span></span>

<span data-ttu-id="ed585-133">MFPlay 需要 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="ed585-133">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed585-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="ed585-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed585-135">使用 MFPlay 進行音訊/影片播放</span><span class="sxs-lookup"><span data-stu-id="ed585-135">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



