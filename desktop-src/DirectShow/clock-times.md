---
description: 時鐘時間
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: 時鐘時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0639fd2b38e312f30f932fcf508427cd71c054
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385597"
---
# <a name="clock-times"></a><span data-ttu-id="2ff7a-103">時鐘時間</span><span class="sxs-lookup"><span data-stu-id="2ff7a-103">Clock Times</span></span>

<span data-ttu-id="2ff7a-104">DirectShow 定義了兩個相關的時鐘時間：參考時間和資料流程時間。</span><span class="sxs-lookup"><span data-stu-id="2ff7a-104">DirectShow defines two related clock times: reference time and stream time.</span></span>

-   <span data-ttu-id="2ff7a-105">*參考時間* 是參考時鐘所傳回的絕對時間。</span><span class="sxs-lookup"><span data-stu-id="2ff7a-105">*Reference time* is the absolute time returned by the reference clock.</span></span> <span data-ttu-id="2ff7a-106"> (參閱 [參考時鐘](reference-clocks.md). ) </span><span class="sxs-lookup"><span data-stu-id="2ff7a-106">(See [Reference Clocks](reference-clocks.md).)</span></span>
-   <span data-ttu-id="2ff7a-107">*資料流程時間* 的定義是相對於圖形上次開始執行的時間。</span><span class="sxs-lookup"><span data-stu-id="2ff7a-107">*Stream time* is defined relative to when the graph last started running.</span></span>
    -   <span data-ttu-id="2ff7a-108">當圖形正在執行時，資料流程時間等於參考時間減去開始時間。</span><span class="sxs-lookup"><span data-stu-id="2ff7a-108">While the graph is running, stream time equals reference time minus start time.</span></span>
    -   <span data-ttu-id="2ff7a-109">當圖形暫停時，資料流程時間會在資料流程時間保持暫停狀態。</span><span class="sxs-lookup"><span data-stu-id="2ff7a-109">While the graph is paused, stream time remains at the stream time when it was paused.</span></span>
    -   <span data-ttu-id="2ff7a-110">在搜尋作業之後，資料流程時間會重設為零。</span><span class="sxs-lookup"><span data-stu-id="2ff7a-110">After a seek operation, stream time resets to zero.</span></span>
    -   <span data-ttu-id="2ff7a-111">當圖形停止時，資料流程時間是未定義的。</span><span class="sxs-lookup"><span data-stu-id="2ff7a-111">While the graph is stopped, stream time is undefined.</span></span>

<span data-ttu-id="2ff7a-112">當媒體範例有時間戳記 *t* 時，即表示範例應該在資料流程時間 *t* 轉譯。</span><span class="sxs-lookup"><span data-stu-id="2ff7a-112">When a media sample has a time stamp *t*, it means the sample should be rendered at stream time *t*.</span></span> <span data-ttu-id="2ff7a-113">基於這個理由，資料流程時間也稱為 *呈現時間*。</span><span class="sxs-lookup"><span data-stu-id="2ff7a-113">For this reason, stream time is also called *presentation time*.</span></span>

<span data-ttu-id="2ff7a-114">當應用程式呼叫 [**IMediaControl：： run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) 來執行篩選圖形時，篩選圖形管理員會在每個篩選器上呼叫 [**IMediaFilter：： run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) 。</span><span class="sxs-lookup"><span data-stu-id="2ff7a-114">When an application calls [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the filter graph, the Filter Graph Manager calls [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) on each filter.</span></span> <span data-ttu-id="2ff7a-115">為了補償篩選器開始執行所需的時間，篩選圖形管理員會指定未來的開始時間。</span><span class="sxs-lookup"><span data-stu-id="2ff7a-115">To compensate for the slight amount of time it takes for the filters to start running, the Filter Graph Manager specifies a start time slightly in the future.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ff7a-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="2ff7a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ff7a-117">DirectShow 中的時間和時鐘</span><span class="sxs-lookup"><span data-stu-id="2ff7a-117">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="2ff7a-118">時間戳記</span><span class="sxs-lookup"><span data-stu-id="2ff7a-118">Time Stamps</span></span>](time-stamps.md)
</dt> </dl>

 

 



