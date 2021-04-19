---
description: 設定播放速率
ms.assetid: 74ae45d3-4fea-491c-af1f-46768df41c5f
title: 設定播放速率
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8a3297ca376b0cc55e4df4884b22d1cb2df81b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972295"
---
# <a name="setting-the-playback-rate"></a><span data-ttu-id="4b0b0-103">設定播放速率</span><span class="sxs-lookup"><span data-stu-id="4b0b0-103">Setting the Playback Rate</span></span>

<span data-ttu-id="4b0b0-104">若要變更播放速率，請呼叫 [**IMediaSeeking：： SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) 方法。</span><span class="sxs-lookup"><span data-stu-id="4b0b0-104">To change the playback rate, call the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span> <span data-ttu-id="4b0b0-105">以原始費率的分數指定新的速率。</span><span class="sxs-lookup"><span data-stu-id="4b0b0-105">Specify the new rate as a fraction of the original rate.</span></span> <span data-ttu-id="4b0b0-106">例如，若要以兩倍的一般速度播放，請使用下列程式：</span><span class="sxs-lookup"><span data-stu-id="4b0b0-106">For example, to play at twice-normal speed, use the following:</span></span>


```C++
pSeek->SetRate(2.0)
```



<span data-ttu-id="4b0b0-107">大於1的速率比平常更快。</span><span class="sxs-lookup"><span data-stu-id="4b0b0-107">Rates greater than one are faster than normal.</span></span> <span data-ttu-id="4b0b0-108">介於零和1之間的速率低於一般。</span><span class="sxs-lookup"><span data-stu-id="4b0b0-108">Rates between zero and one are slower than normal.</span></span> <span data-ttu-id="4b0b0-109">負數會定義為回溯播放，但實際上大部分的篩選都不支援。</span><span class="sxs-lookup"><span data-stu-id="4b0b0-109">Negative rates are defined as backward playback, but in practice most filters do not support it.</span></span> <span data-ttu-id="4b0b0-110">目前沒有任何標準的 DirectShow 篩選支援反向播放。</span><span class="sxs-lookup"><span data-stu-id="4b0b0-110">Currently none of the standard DirectShow filters support reverse playback.</span></span>

<span data-ttu-id="4b0b0-111">無論播放速率為何，目前的位置和停止位置一律會相對於原始來源來表示。</span><span class="sxs-lookup"><span data-stu-id="4b0b0-111">Regardless of the playback rate, the current position and the stop position are always expressed relative to the original source.</span></span> <span data-ttu-id="4b0b0-112">例如，如果原始程式檔的長度為20秒，且正常播放速率為10秒，則將目前的位置設為10秒將會搜尋到檔案的中間。</span><span class="sxs-lookup"><span data-stu-id="4b0b0-112">For example, if a source file is 20 seconds long at normal playback rate, setting the current position to 10 seconds will seek to the middle of the file.</span></span> <span data-ttu-id="4b0b0-113">如果播放速率為2.0，則停止位置為20秒，而您要搜尋10秒的位置，該檔案將會播放5秒的即時：10秒鐘的時間，這兩倍的正常播放速度。</span><span class="sxs-lookup"><span data-stu-id="4b0b0-113">If the playback rate is 2.0, the stop position is 20 seconds, and you seek to the 10-second position, the file will play for 5 seconds of real time: 10 seconds' worth, at twice the normal playback speed.</span></span> <span data-ttu-id="4b0b0-114">在2.0 的播放速率中，目前的位置會以參考時鐘的速率倍增加。</span><span class="sxs-lookup"><span data-stu-id="4b0b0-114">At a playback rate of 2.0, the current position increases at twice the rate of the reference clock.</span></span>

 

 



