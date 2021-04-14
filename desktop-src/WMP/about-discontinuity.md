---
title: 關於中斷
description: 關於中斷
ms.assetid: 29210758-a1e6-47f2-9428-38f79623fbca
keywords:
- Windows Media Player 外掛程式、音訊 DSP
- 外掛程式、音訊 DSP
- 數位信號處理外掛程式，音訊中斷
- DSP 外掛程式、音訊中斷
- 音訊 DSP 外掛程式，中斷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0448220d4616122b3c99670357bbbd78de11c392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371906"
---
# <a name="about-discontinuity"></a><span data-ttu-id="86d64-108">關於中斷</span><span class="sxs-lookup"><span data-stu-id="86d64-108">About Discontinuity</span></span>

<span data-ttu-id="86d64-109">Windows Media Player 可以在輸入資料流程中的任何時間，藉由呼叫 **IMediaObject：:D iscontinuity** 方法來發出信號。</span><span class="sxs-lookup"><span data-stu-id="86d64-109">At any time, Windows Media Player can signal a break in the input stream by calling the **IMediaObject::Discontinuity** method.</span></span> <span data-ttu-id="86d64-110">這會定期發生于資料流程的開頭和結尾，也會在每次搜尋作業之前，或串流內容因任何原因而中斷時進行。</span><span class="sxs-lookup"><span data-stu-id="86d64-110">This occurs routinely at the start and end of a stream, and also prior to each seek operation or when streaming content is interrupted for any reason.</span></span> <span data-ttu-id="86d64-111">Windows Media Player 外掛程式嚮導所產生的範例 DSP 外掛程式不需要處理不連續，原因如下：</span><span class="sxs-lookup"><span data-stu-id="86d64-111">The sample DSP plug-in that the Windows Media Player Plug-in wizard generates does not need to deal with discontinuities for the following reasons:</span></span>

-   <span data-ttu-id="86d64-112">PCM 範例是不可部分完成的，這表示它們可以在不考慮串流中其他範例的情況下進行處理。</span><span class="sxs-lookup"><span data-stu-id="86d64-112">PCM samples are atomic, meaning they can be processed without regard to the other samples in the stream.</span></span> <span data-ttu-id="86d64-113">某些影片格式包含相依于主要畫面格和壓縮範例的資料。</span><span class="sxs-lookup"><span data-stu-id="86d64-113">Some video formats contain data that depends on key frames and compressed samples.</span></span>
-   <span data-ttu-id="86d64-114">撰寫範例程式碼時，一律會強制用戶端處理所有輸出，然後外掛程式才會接受更多輸入。</span><span class="sxs-lookup"><span data-stu-id="86d64-114">The sample code is written to always force the client to process all output before the plug-in will accept more input.</span></span>

<span data-ttu-id="86d64-115">**IMediaObject：:D iscontinuity** 的預設執行只會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="86d64-115">The default implementation of **IMediaObject::Discontinuity** simply returns S\_OK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86d64-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="86d64-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86d64-117">**執行音訊 DSP 外掛程式**</span><span class="sxs-lookup"><span data-stu-id="86d64-117">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




