---
description: 本主題說明如何藉由設定播放的開始和停止時間，在 MFPlay 中播放媒體檔案的區段。
ms.assetid: cd761a4a-42ad-4994-b1b8-0946d29c3d8b
title: 如何播放檔案剪輯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744db96c6dc384f2473f6c6d3361b24950a8881d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848377"
---
# <a name="how-to-play-a-file-clip"></a><span data-ttu-id="caeea-103">如何播放檔案剪輯</span><span class="sxs-lookup"><span data-stu-id="caeea-103">How to Play a File Clip</span></span>

<span data-ttu-id="caeea-104">\[MFPlay 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="caeea-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="caeea-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="caeea-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="caeea-106">\]</span><span class="sxs-lookup"><span data-stu-id="caeea-106">\]</span></span>

<span data-ttu-id="caeea-107">本主題說明如何藉由設定播放的開始和停止時間，在 MFPlay 中播放媒體檔案的區段。</span><span class="sxs-lookup"><span data-stu-id="caeea-107">This topic describes how to play a segment of a media file in MFPlay, by setting the start and stop times for playback.</span></span>

<span data-ttu-id="caeea-108">**播放檔案剪輯**</span><span class="sxs-lookup"><span data-stu-id="caeea-108">**To Play a File Clip**</span></span>

1.  <span data-ttu-id="caeea-109">呼叫 [**IMFPMediaPlayer：： CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) 或 [**IMFPMediaPlayer：： CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) 來建立檔案的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="caeea-109">Call [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) or [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) to create a media item for the file.</span></span>
2.  <span data-ttu-id="caeea-110">（選擇性）取得檔案的總持續時間，如 [如何取得播放持續時間](how-to-get-the-playback-duration.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="caeea-110">Optionally, get the total duration of the file, as described in [How to Get the Playback Duration](how-to-get-the-playback-duration.md).</span></span>
3.  <span data-ttu-id="caeea-111">呼叫 [**IMFPMediaItem：： SetStartStopPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) 來設定開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="caeea-111">Call [**IMFPMediaItem::SetStartStopPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) to set the start and stop times.</span></span> <span data-ttu-id="caeea-112">停止時間不得超過檔案持續時間。</span><span class="sxs-lookup"><span data-stu-id="caeea-112">The stop time must not exceed the file duration.</span></span>
4.  <span data-ttu-id="caeea-113">呼叫 [**IMFPMediaPlayer：： SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) 以開始播放。</span><span class="sxs-lookup"><span data-stu-id="caeea-113">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) to start playback.</span></span>

<span data-ttu-id="caeea-114">下列範例會使用 [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)的封鎖版本。</span><span class="sxs-lookup"><span data-stu-id="caeea-114">The following example uses the blocking version of [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl).</span></span> <span data-ttu-id="caeea-115">如果使用非封鎖版本，則在 **CreateMediaItemFromURL** 之後出現的程式碼應該放在 **\_ \_ \_ MEDIAITEM \_ 建立** 事件的處理常式中。</span><span class="sxs-lookup"><span data-stu-id="caeea-115">If the non-blocking version is used, the code that appears after **CreateMediaItemFromURL** should be placed in the handler for the **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event.</span></span> <span data-ttu-id="caeea-116">如需有關 MFPlay 中事件的詳細資訊，請參閱 [從播放程式接收事件](getting-started-with-mfplay.md)。</span><span class="sxs-lookup"><span data-stu-id="caeea-116">For more information about events in MFPlay, see [Receiving Events From the Player](getting-started-with-mfplay.md).</span></span>

<span data-ttu-id="caeea-117">為了取得檔案持續時間，此範例會呼叫 `GetPlaybackDuration` 主題中顯示 [如何取得播放持續時間](how-to-get-the-playback-duration.md)的函式。</span><span class="sxs-lookup"><span data-stu-id="caeea-117">To get the file duration, this example calls the `GetPlaybackDuration` function shown in the topic [How to Get the Playback Duration](how-to-get-the-playback-duration.md).</span></span>


```C++
HRESULT PlayMediaClip(
    IMFPMediaPlayer *pPlayer,
    PCWSTR pszURL,
    LONGLONG    hnsStart,
    LONGLONG    hnsEnd
    )
{
    IMFPMediaItem *pItem = NULL;
    PROPVARIANT varStart, varEnd;

    ULONGLONG hnsDuration = 0;

    HRESULT hr = pPlayer->CreateMediaItemFromURL(pszURL, TRUE, 0, &pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetPlaybackDuration(pItem, &hnsDuration);
    if (FAILED(hr))
    {
        goto done;
    }

    if ((ULONGLONG)hnsEnd > hnsDuration)
    {
        hnsEnd = hnsDuration;
    }

    hr = InitPropVariantFromInt64(hnsStart, &varStart);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitPropVariantFromInt64(hnsEnd, &varEnd);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pItem->SetStartStopPosition(
        &MFP_POSITIONTYPE_100NS,
        &varStart,
        &MFP_POSITIONTYPE_100NS,
        &varEnd
        );
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPlayer->SetMediaItem(pItem);

done:
    SafeRelease(&pItem);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="caeea-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="caeea-118">Requirements</span></span>

<span data-ttu-id="caeea-119">MFPlay 需要 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="caeea-119">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="caeea-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="caeea-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caeea-121">使用 MFPlay 進行音訊/影片播放</span><span class="sxs-lookup"><span data-stu-id="caeea-121">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



