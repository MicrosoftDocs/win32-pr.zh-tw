---
description: 本主題說明如何使用 MFPlay 取得媒體檔案的播放持續時間。
ms.assetid: b1ea4f21-55d1-47b0-b6d3-8951dce79f7c
title: 如何取得播放持續時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21dd98a916109c8fb3d0ad3311643b1ffdc0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974559"
---
# <a name="how-to-get-the-playback-duration"></a><span data-ttu-id="f138e-103">如何取得播放持續時間</span><span class="sxs-lookup"><span data-stu-id="f138e-103">How to Get the Playback Duration</span></span>

<span data-ttu-id="f138e-104">\[MFPlay 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="f138e-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f138e-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="f138e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="f138e-106">\]</span><span class="sxs-lookup"><span data-stu-id="f138e-106">\]</span></span>

<span data-ttu-id="f138e-107">本主題說明如何使用 MFPlay 取得媒體檔案的播放持續時間。</span><span class="sxs-lookup"><span data-stu-id="f138e-107">This topic describes how to get the playback duration of a media file using MFPlay.</span></span>

<span data-ttu-id="f138e-108">**取得播放持續時間**</span><span class="sxs-lookup"><span data-stu-id="f138e-108">**To Get the Playback Duration**</span></span>

1.  <span data-ttu-id="f138e-109">呼叫 [**IMFPMediaPlayer：： CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) 或 [**IMFPMediaPlayer：： CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) 來建立檔案的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="f138e-109">Call [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) or [**IMFPMediaPlayer::CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) to create a media item for the file.</span></span>
2.  <span data-ttu-id="f138e-110">呼叫 [**IMFPMediaItem：： GetDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration)。</span><span class="sxs-lookup"><span data-stu-id="f138e-110">Call [**IMFPMediaItem::GetDuration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration).</span></span> <span data-ttu-id="f138e-111">指定第一個參數的 **MFP \_ positiontype] \_ 100ns** 。</span><span class="sxs-lookup"><span data-stu-id="f138e-111">Specify **MFP\_POSITIONTYPE\_100NS** for the first parameter.</span></span> <span data-ttu-id="f138e-112">持續時間會以包含 **大型 \_ 整數** 值的 **PROPVARIANT** 傳回。</span><span class="sxs-lookup"><span data-stu-id="f138e-112">The duration is returned as a **PROPVARIANT** that contains a **LARGE\_INTEGER** value.</span></span> <span data-ttu-id="f138e-113">持續時間會以 100-毫微秒單位提供。</span><span class="sxs-lookup"><span data-stu-id="f138e-113">The duration is given in 100-nanosecond units.</span></span>

<span data-ttu-id="f138e-114">下列範例顯示步驟2：</span><span class="sxs-lookup"><span data-stu-id="f138e-114">The following example shows step 2:</span></span>


```C++
#include <propvarutil.h>

HRESULT GetPlaybackDuration(IMFPMediaItem *pItem, ULONGLONG *phnsDuration)
{
    PROPVARIANT var;

    HRESULT hr = pItem->GetDuration(MFP_POSITIONTYPE_100NS, &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt64(var, phnsDuration);
        PropVariantClear(&var);
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="f138e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f138e-115">Requirements</span></span>

<span data-ttu-id="f138e-116">MFPlay 需要 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="f138e-116">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f138e-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="f138e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f138e-118">使用 MFPlay 進行音訊/影片播放</span><span class="sxs-lookup"><span data-stu-id="f138e-118">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



