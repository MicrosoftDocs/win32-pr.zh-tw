---
description: Demux 時鐘行為
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Demux 時鐘行為
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9065e6da51acb5387ca06bf921d5cdc91c567843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025731"
---
# <a name="demux-clock-behavior"></a><span data-ttu-id="0c2a5-103">Demux 時鐘行為</span><span class="sxs-lookup"><span data-stu-id="0c2a5-103">Demux Clock Behavior</span></span>

<span data-ttu-id="0c2a5-104">在 push 模式中，MPEG-2 信號 (demux) 會公開 [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) 介面。</span><span class="sxs-lookup"><span data-stu-id="0c2a5-104">In push mode, the MPEG-2 Demultiplexer (demux) exposes the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span> <span data-ttu-id="0c2a5-105">它會做為即時來源，因此預設會將其選擇為圖形參考時鐘;如需詳細資訊，請參閱 [即時來源](live-sources.md) 。</span><span class="sxs-lookup"><span data-stu-id="0c2a5-105">It acts as a live source, so it will be chosen as the graph reference clock by default; see [Live Sources](live-sources.md) for more information.</span></span>

-   <span data-ttu-id="0c2a5-106">針對傳輸資料流程，demux 會將其時鐘同步至對應至應用程式最近所對應之音訊或影片串流的 PCR 串流。</span><span class="sxs-lookup"><span data-stu-id="0c2a5-106">For transport streams, the demux synchronizes its clock to the PCR stream that corresponds to the audio or video stream most recently mapped by the application.</span></span> <span data-ttu-id="0c2a5-107">就內部而言，demux 會追蹤 PAT 和 PMT 資料表。</span><span class="sxs-lookup"><span data-stu-id="0c2a5-107">Internally, the demux tracks the PAT and PMT tables.</span></span> <span data-ttu-id="0c2a5-108">當應用程式將基本資料流程 PID 對應到輸出圖釘時，demux 會查閱該 PID 的 PCR 串流，並使用該 PCR 串流。</span><span class="sxs-lookup"><span data-stu-id="0c2a5-108">When the application maps an elementary stream PID to an output pin, the demux looks up the PCR stream for that PID and uses that PCR stream.</span></span> <span data-ttu-id="0c2a5-109"> (目前沒有方法可讓應用程式直接指定 PCR PID。 ) </span><span class="sxs-lookup"><span data-stu-id="0c2a5-109">(Currently, there is not way for the application to specify the PCR PID directly.)</span></span>
-   <span data-ttu-id="0c2a5-110">針對程式資料流程，demux 會將其時鐘同步處理到 SCR 資料流程。</span><span class="sxs-lookup"><span data-stu-id="0c2a5-110">For program streams, the demux synchronizes its clock to the SCR stream.</span></span>

<span data-ttu-id="0c2a5-111">將篩選時鐘同步至 PCR 或 SCR 資料流程可防止資料溢位或下溢，這可能會導致圖形時鐘與資料流程時鐘不同的結果。</span><span class="sxs-lookup"><span data-stu-id="0c2a5-111">Synchronizing the filter clock to the PCR or SCR stream prevents data overflow or underflow, which could result if the graph clock varied from the stream clock.</span></span> <span data-ttu-id="0c2a5-112">Demux 也會將 PE 值的值轉譯成 DirectShow 參考時間，並使用這些值來為媒體範例加蓋時間戳記。</span><span class="sxs-lookup"><span data-stu-id="0c2a5-112">The demux also translates PES PTS values into DirectShow reference times, and uses these values to time stamp the media samples.</span></span> <span data-ttu-id="0c2a5-113">時間戳記適用于下一個畫面格界限;不保證框架界限會與媒體範例的開頭一致。</span><span class="sxs-lookup"><span data-stu-id="0c2a5-113">The time stamps apply to the next frame boundary; there is no guarantee that the frame boundary will align with the start of the media sample.</span></span>

<span data-ttu-id="0c2a5-114">Demux 可保證時間戳記會以單純的時間增加。</span><span class="sxs-lookup"><span data-stu-id="0c2a5-114">The demux guarantees that the time stamps increase monotonically.</span></span> <span data-ttu-id="0c2a5-115">這表示，如果傳輸資料流程所包含的區段（例如商業）是使用與主要程式不同的時鐘所建立的，則 demux 會調整呈現時間戳記，以隱藏下游篩選準則的不連續時間。</span><span class="sxs-lookup"><span data-stu-id="0c2a5-115">This means, for example, that if a transport stream includes a segment such as a commercial that was created with a different clock than the main program, the demux will adjust the presentation time stamps to hide the time discontinuity from downstream filters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c2a5-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="0c2a5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c2a5-117">使用 MPEG-2 信號信號</span><span class="sxs-lookup"><span data-stu-id="0c2a5-117">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



