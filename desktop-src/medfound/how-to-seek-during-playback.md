---
description: 本主題說明如何使用 MFPlay 在播放期間搜尋。
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: 如何在播放期間搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16d7ad964335db100c84f0a396b7f13de7a270d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993008"
---
# <a name="how-to-seek-during-playback"></a><span data-ttu-id="a1551-103">如何在播放期間搜尋</span><span class="sxs-lookup"><span data-stu-id="a1551-103">How to Seek During Playback</span></span>

<span data-ttu-id="a1551-104">\[MFPlay 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a1551-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a1551-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="a1551-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a1551-106">\]</span><span class="sxs-lookup"><span data-stu-id="a1551-106">\]</span></span>

<span data-ttu-id="a1551-107">本主題說明如何使用 MFPlay 在播放期間搜尋。</span><span class="sxs-lookup"><span data-stu-id="a1551-107">This topic describes how to seek during playback using MFPlay.</span></span>

<span data-ttu-id="a1551-108">**在播放期間搜尋**</span><span class="sxs-lookup"><span data-stu-id="a1551-108">**To Seek During Playback**</span></span>

1.  <span data-ttu-id="a1551-109">將 **PROPVARIANT** 初始化為以 100-毫微秒單位來保存搜尋時間，以 **大 \_ 整數** (**VT \_ I8**) 類型。</span><span class="sxs-lookup"><span data-stu-id="a1551-109">Initialize a **PROPVARIANT** to hold the seek time in 100-nanosecond units, as a **LARGE\_INTEGER** (**VT\_I8**) type.</span></span>
2.  <span data-ttu-id="a1551-110">呼叫 [**IMFPMediaPlayer：： SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition)。</span><span class="sxs-lookup"><span data-stu-id="a1551-110">Call [**IMFPMediaPlayer::SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition).</span></span> <span data-ttu-id="a1551-111">指定第一個參數的 **MFP \_ positiontype] \_ 100ns** ，然後傳入第二個參數的 **PROPVARIANT** 。</span><span class="sxs-lookup"><span data-stu-id="a1551-111">Specify **MFP\_POSITIONTYPE\_100NS** for the first parameter, and pass in the **PROPVARIANT** for the second parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1551-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1551-112">Requirements</span></span>

<span data-ttu-id="a1551-113">MFPlay 需要 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="a1551-113">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1551-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="a1551-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1551-115">使用 MFPlay 進行音訊/影片播放</span><span class="sxs-lookup"><span data-stu-id="a1551-115">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



