---
description: 本主題說明如何搭配 MFPlay 使用音訊/影片效果。
ms.assetid: 90f34bf3-899f-46e0-80c8-af83caa4835d
title: 如何新增音訊或影片效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d2b02453ce4561ead7fee0d272a07e694e8388
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983453"
---
# <a name="how-to-add-audio-or-video-effects"></a><span data-ttu-id="32d51-103">如何新增音訊或影片效果</span><span class="sxs-lookup"><span data-stu-id="32d51-103">How to Add Audio or Video Effects</span></span>

<span data-ttu-id="32d51-104">\[MFPlay 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="32d51-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="32d51-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="32d51-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="32d51-106">\]</span><span class="sxs-lookup"><span data-stu-id="32d51-106">\]</span></span>

<span data-ttu-id="32d51-107">本主題說明如何搭配 MFPlay 使用音訊/影片效果。</span><span class="sxs-lookup"><span data-stu-id="32d51-107">This topic describes how to use audio/video effects with MFPlay.</span></span>

<span data-ttu-id="32d51-108">若要搭配 MFPlay 使用效果，必須將效果實作為媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="32d51-108">To use an effect with MFPlay, the effect must be implemented as a Media Foundation transform (MFT).</span></span> <span data-ttu-id="32d51-109">如需詳細資訊，請參閱 [媒體基礎轉換](media-foundation-transforms.md)。</span><span class="sxs-lookup"><span data-stu-id="32d51-109">For more information, see [Media Foundation Transforms](media-foundation-transforms.md).</span></span>

<span data-ttu-id="32d51-110">**新增音訊或影片效果**</span><span class="sxs-lookup"><span data-stu-id="32d51-110">**To Add an Audio or Video Effect**</span></span>

1.  <span data-ttu-id="32d51-111">建立可執行效果的 MFT 實例。</span><span class="sxs-lookup"><span data-stu-id="32d51-111">Create an instance of the MFT that implements the effect.</span></span>
2.  <span data-ttu-id="32d51-112">呼叫 [**IMFPMediaPlayer：： InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect)。</span><span class="sxs-lookup"><span data-stu-id="32d51-112">Call [**IMFPMediaPlayer::InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect).</span></span>

<span data-ttu-id="32d51-113">開啟媒體檔案來播放之前，請先呼叫 [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) 。</span><span class="sxs-lookup"><span data-stu-id="32d51-113">Call [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) before you open the media file for playback.</span></span> <span data-ttu-id="32d51-114">MFPlay 會自動判斷效果是影片效果或音訊效果。</span><span class="sxs-lookup"><span data-stu-id="32d51-114">MFPlay automatically determines whether the effect is a video effect or audio effect.</span></span>

<span data-ttu-id="32d51-115">[**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect)方法也會採用布林值參數，指定效果是選擇性或必要的。</span><span class="sxs-lookup"><span data-stu-id="32d51-115">The [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) method also takes a Boolean parameter that specifies whether the effect is optional or required.</span></span> <span data-ttu-id="32d51-116">如果 MFPlay 無法新增必要的效果 (例如，因為資料流程格式與) 不相容，所以會發生播放錯誤。</span><span class="sxs-lookup"><span data-stu-id="32d51-116">If MFPlay cannot add a required effect (for example, because the stream format is incompatible), a playback error occurs.</span></span> <span data-ttu-id="32d51-117">在大部分的情況下，最好將效果設定為選擇性。</span><span class="sxs-lookup"><span data-stu-id="32d51-117">In most cases, it is better to set an effect as optional.</span></span>

<span data-ttu-id="32d51-118">MFPlay 會繼續使用所有後續播放的效果。</span><span class="sxs-lookup"><span data-stu-id="32d51-118">MFPlay continues to use the effect for all subsequent playback.</span></span> <span data-ttu-id="32d51-119">若要移除效果，請呼叫 [**IMFPMediaPlayer：： RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) 或 [**IMFPMediaPlayer：： RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects)。</span><span class="sxs-lookup"><span data-stu-id="32d51-119">To remove the effect, call [**IMFPMediaPlayer::RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) or [**IMFPMediaPlayer::RemoveAllEffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects).</span></span>


```C++
HRESULT AddPlaybackEffect(REFGUID clsid, IMFPMediaPlayer *pPlayer)
{
    IMFTransform *pMFT = NULL;

    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pMFT));

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->InsertEffect(pMFT, TRUE); // Set as optional.
    }

    SafeRelease(&pMFT);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="32d51-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="32d51-120">Requirements</span></span>

<span data-ttu-id="32d51-121">MFPlay 需要 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="32d51-121">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32d51-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="32d51-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32d51-123">使用 MFPlay 進行音訊/影片播放</span><span class="sxs-lookup"><span data-stu-id="32d51-123">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



