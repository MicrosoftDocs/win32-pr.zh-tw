---
title: Low-Delay 音訊
description: Low-Delay 音訊
ms.assetid: f93819eb-f38a-45a0-aa1b-4e677e33daf8
keywords:
- Windows Media Format SDK，低延遲音訊
- Windows Media Format SDK，音訊支援
- 編解碼器，低延遲音訊
- 編解碼器、音訊支援
- 低延遲音訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8cedd3a6bb54942f5a517c7133e993cf5b11cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967849"
---
# <a name="low-delay-audio"></a><span data-ttu-id="9842c-108">Low-Delay 音訊</span><span class="sxs-lookup"><span data-stu-id="9842c-108">Low-Delay Audio</span></span>

<span data-ttu-id="9842c-109">「低延遲音訊」是一種編碼模式，會產生比其他模式更小之緩衝區視窗設定的壓縮音訊。</span><span class="sxs-lookup"><span data-stu-id="9842c-109">Low-delay audio is an encoding mode that produces compressed audio with a smaller buffer-window setting than other modes.</span></span> <span data-ttu-id="9842c-110">這適用于需要在播放期間快速切換的資料流程。</span><span class="sxs-lookup"><span data-stu-id="9842c-110">This is useful for streams that need to be switched quickly during playback.</span></span> <span data-ttu-id="9842c-111">這項功能的一般案例是資料流程處理的簡報，其中包含了任意切換內容的能力，例如變更電視的頻道。</span><span class="sxs-lookup"><span data-stu-id="9842c-111">The typical scenario for this feature is a streamed presentation that includes the ability to arbitrarily switch content, like changing the channel of a television.</span></span>

<span data-ttu-id="9842c-112">當您使用低延遲的音訊格式時，相較于其他音訊格式，切換內容的延遲會大幅降低。</span><span class="sxs-lookup"><span data-stu-id="9842c-112">When you use a low-delay audio format, the latency for switching content is drastically reduced compared to other audio formats.</span></span> <span data-ttu-id="9842c-113">當您使用低延遲格式時，即時廣播的延遲也會降低。</span><span class="sxs-lookup"><span data-stu-id="9842c-113">Latency is also reduced for live broadcasts when you use low-delay formats.</span></span>

<span data-ttu-id="9842c-114">Windows Media 音訊9.1 和 Windows Media 音訊 9.1 Professional 編解碼器支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="9842c-114">This feature is supported by the Windows Media Audio 9.1 and Windows Media Audio 9.1 Professional codecs.</span></span> <span data-ttu-id="9842c-115">低延遲格式僅適用于一次傳遞和兩次傳遞)  (的常數位元速率編碼。</span><span class="sxs-lookup"><span data-stu-id="9842c-115">Low-delay formats are available only for constant bit rate encoding (both one-pass and two-pass).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9842c-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="9842c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9842c-117">**編解碼器功能**</span><span class="sxs-lookup"><span data-stu-id="9842c-117">**Codec Features**</span></span>](codec-features.md)
</dt> </dl>

 

 




