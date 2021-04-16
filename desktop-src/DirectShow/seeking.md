---
description: 尋求
ms.assetid: ceccb657-f1e1-4d59-920a-477a95b8a1a4
title: 尋求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef7e82009198a790d5c0f7818599aa13905ce82
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104570845"
---
# <a name="seeking"></a><span data-ttu-id="2c3b9-103">尋求</span><span class="sxs-lookup"><span data-stu-id="2c3b9-103">Seeking</span></span>

<span data-ttu-id="2c3b9-104">篩選準則支援搜尋 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面。</span><span class="sxs-lookup"><span data-stu-id="2c3b9-104">Filters support seeking through the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="2c3b9-105">應用程式會查詢篩選圖形管理員以取得 **IMediaSeeking** ，並使用它來發出搜尋命令。</span><span class="sxs-lookup"><span data-stu-id="2c3b9-105">The application queries the Filter Graph Manager for **IMediaSeeking** and uses it to issue seek commands.</span></span> <span data-ttu-id="2c3b9-106">篩選圖形管理員會將每個搜尋命令分散到圖形中的所有轉譯器篩選。</span><span class="sxs-lookup"><span data-stu-id="2c3b9-106">The Filter Graph Manager distributes each seek command to all of the renderer filters in the graph.</span></span> <span data-ttu-id="2c3b9-107">每個轉譯器都會透過上游篩選的輸出圖釘，將命令傳遞給上游，直到到達可執行搜尋的篩選準則為止。</span><span class="sxs-lookup"><span data-stu-id="2c3b9-107">Each renderer passes the command upstream, through the output pins of the upstream filters, until it reaches a filter that can execute the seek.</span></span> <span data-ttu-id="2c3b9-108">通常來源篩選器或剖析器篩選器（例如 [AVI 分隔](avi-splitter-filter.md)器）會執行搜尋作業。</span><span class="sxs-lookup"><span data-stu-id="2c3b9-108">Typically a source filter or parser filter, such as the [AVI Splitter](avi-splitter-filter.md), carries out the seek operation.</span></span>

<span data-ttu-id="2c3b9-109">當篩選準則執行搜尋作業時，它會清除任何暫止的資料。</span><span class="sxs-lookup"><span data-stu-id="2c3b9-109">When a filter performs a seek operation, it flushes any pending data.</span></span> <span data-ttu-id="2c3b9-110">結果是將搜尋命令的延遲降至最低，因為現有的資料會從圖表中清除。</span><span class="sxs-lookup"><span data-stu-id="2c3b9-110">The result is to minimize the latency of seek commands, because existing data is flushed from the graph.</span></span> <span data-ttu-id="2c3b9-111">在 seek 命令之後，資料流程時間會重設為零。</span><span class="sxs-lookup"><span data-stu-id="2c3b9-111">After a seek command, stream time resets to zero.</span></span>

<span data-ttu-id="2c3b9-112">下圖說明事件的順序。</span><span class="sxs-lookup"><span data-stu-id="2c3b9-112">The following diagram illustrates the sequence of events.</span></span>

![事件的順序](images/seeking.png)

<span data-ttu-id="2c3b9-114">如果剖析器篩選器有多個輸出釘選，通常會指定其中一個來接受搜尋命令。</span><span class="sxs-lookup"><span data-stu-id="2c3b9-114">If a parser filter has more than one output pin, it typically designates one of them to accept seek commands.</span></span> <span data-ttu-id="2c3b9-115">其他 pin 會拒絕或忽略它們所收到的任何搜尋命令。</span><span class="sxs-lookup"><span data-stu-id="2c3b9-115">The other pins reject or ignore any seek commands they receive.</span></span> <span data-ttu-id="2c3b9-116">如此一來，剖析器就會將其所有資料流程保持同步。</span><span class="sxs-lookup"><span data-stu-id="2c3b9-116">In this way, the parser keeps all of its streams synchronized.</span></span> <span data-ttu-id="2c3b9-117">不過，所有輸出圖釘都應該執行 [**IMediaSeeking：： GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) 和 [**IMediaSeeking：： CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) ，以傳回篩選準則的搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="2c3b9-117">However, all output pins should implement [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) and [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) to return the filter's seeking capabilities.</span></span> <span data-ttu-id="2c3b9-118">這可確保篩選圖形管理員會將正確的值傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="2c3b9-118">This ensures that the Filter Graph Manager returns the correct value to the application.</span></span>

<span data-ttu-id="2c3b9-119">篩選器的 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 介面已被取代。</span><span class="sxs-lookup"><span data-stu-id="2c3b9-119">The [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface has been deprecated for filters.</span></span> <span data-ttu-id="2c3b9-120">Automation 用戶端仍然需要在篩選圖形管理員上使用這個介面，因為 **IMediaSeeking** 不是自動化相容，但是篩選圖形管理員會將所有 **IMediaPosition** 呼叫轉譯為 **IMediaSeeking** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="2c3b9-120">Automation clients still need to use this interface on the Filter Graph Manager, because **IMediaSeeking** is not Automation-compatible, but the Filter Graph Manager translates all **IMediaPosition** calls into **IMediaSeeking** calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c3b9-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="2c3b9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c3b9-122">沖洗</span><span class="sxs-lookup"><span data-stu-id="2c3b9-122">Flushing</span></span>](flushing.md)
</dt> <dt>

[<span data-ttu-id="2c3b9-123">DirectShow 中的時間和時鐘</span><span class="sxs-lookup"><span data-stu-id="2c3b9-123">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



