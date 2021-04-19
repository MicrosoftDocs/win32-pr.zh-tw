---
description: 新區段
ms.assetid: 6c470b38-481f-4e52-93b8-eb6b343dcefc
title: 新區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5438cb3b457ed8ea0f77bd2ac1dcc5d6d2c72698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973734"
---
# <a name="new-segments"></a><span data-ttu-id="d40ae-103">新區段</span><span class="sxs-lookup"><span data-stu-id="d40ae-103">New Segments</span></span>

<span data-ttu-id="d40ae-104">*區段* 是一組共用一般開始時間、停止時間和播放速率的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="d40ae-104">A *segment* is a group of media samples that share a common start time, stop time, and playback rate.</span></span> <span data-ttu-id="d40ae-105">[**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)方法會為新區段的開頭髮出信號。</span><span class="sxs-lookup"><span data-stu-id="d40ae-105">The [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method signals the start of a new segment.</span></span> <span data-ttu-id="d40ae-106">它提供一種方法讓來源篩選準則通知下游篩選準則，指出時間和費率資訊已變更。</span><span class="sxs-lookup"><span data-stu-id="d40ae-106">It provides a way for a source filter to inform downstream filters that the time and rate information has changed.</span></span> <span data-ttu-id="d40ae-107">例如，如果來源篩選搜尋到資料流程中的新點，則會以新的開始時間來呼叫 **NewSegment** 。</span><span class="sxs-lookup"><span data-stu-id="d40ae-107">For example, if the source filter seeks to a new point in the stream, it calls **NewSegment** with the new start time.</span></span>

<span data-ttu-id="d40ae-108">某些下游篩選器會在處理範例時使用區段資訊。</span><span class="sxs-lookup"><span data-stu-id="d40ae-108">Some downstream filters use the segment information when they process samples.</span></span> <span data-ttu-id="d40ae-109">例如，使用幀壓縮的格式，如果停止時間落在差異框架上，來源篩選可能需要在停止時間之後傳送額外的範例。</span><span class="sxs-lookup"><span data-stu-id="d40ae-109">For example, in a format that uses interframe compression, if the stop time falls on a delta frame, the source filter may need to send additional samples after the stop time.</span></span> <span data-ttu-id="d40ae-110">這可讓解碼器解碼最終的 delta frame。</span><span class="sxs-lookup"><span data-stu-id="d40ae-110">This enables the decoder to decode the final delta frame.</span></span> <span data-ttu-id="d40ae-111">為了判斷正確的最後框架，此解碼器會參考區段停止時間。</span><span class="sxs-lookup"><span data-stu-id="d40ae-111">To determine the correct final frame, the decoder refers to the segment stop time.</span></span> <span data-ttu-id="d40ae-112">另一個範例是，音訊轉譯器會使用區段速率以及音訊取樣率，以產生正確的音訊輸出。</span><span class="sxs-lookup"><span data-stu-id="d40ae-112">As another example, audio renderers use the segment rate along with the audio sampling rate to generate the correct audio output.</span></span>

<span data-ttu-id="d40ae-113">在推送模型中，來源篩選準則會起始 **NewSegment** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="d40ae-113">In the push model, the source filter initiates the **NewSegment** call.</span></span> <span data-ttu-id="d40ae-114">在提取模型中，這是由剖析器篩選所完成。</span><span class="sxs-lookup"><span data-stu-id="d40ae-114">In the pull model, this is done by the parser filter.</span></span> <span data-ttu-id="d40ae-115">無論是哪一種情況，篩選準則都會呼叫下游輸入 pin 的 **NewSegment** ，這會將呼叫傳播至下一個篩選器，直到呼叫到達轉譯器為止。</span><span class="sxs-lookup"><span data-stu-id="d40ae-115">In either case, the filter calls **NewSegment** on the downstream input pin, which propagates the call to the next filter, until the call reaches the renderer.</span></span> <span data-ttu-id="d40ae-116">篩選準則必須將 **NewSegment** 呼叫與其他串流呼叫序列化，例如 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)。</span><span class="sxs-lookup"><span data-stu-id="d40ae-116">Filters must serialize **NewSegment** calls with other streaming calls, such as [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).</span></span>

<span data-ttu-id="d40ae-117">資料流程時間會在每個新區段之後重設為零。</span><span class="sxs-lookup"><span data-stu-id="d40ae-117">Stream time resets to zero after each new segment.</span></span> <span data-ttu-id="d40ae-118">區段從零開始之後所傳遞樣本的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="d40ae-118">Time stamps on samples delivered after the segment start from zero.</span></span>

 

 



