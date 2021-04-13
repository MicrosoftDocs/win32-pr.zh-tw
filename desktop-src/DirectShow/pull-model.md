---
description: 提取模型
ms.assetid: b5246dfe-e6ee-4b91-bfe3-2ec8b8723938
title: 提取模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd4becd54bffb39acf30b6d29fca45e6a117989
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509997"
---
# <a name="pull-model"></a><span data-ttu-id="7ea93-103">提取模型</span><span class="sxs-lookup"><span data-stu-id="7ea93-103">Pull Model</span></span>

<span data-ttu-id="7ea93-104">在 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面中，上游篩選器會決定要傳送的資料，並將資料推送至下游篩選。</span><span class="sxs-lookup"><span data-stu-id="7ea93-104">In the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, the upstream filter determines what data to send, and it pushes the data to the downstream filter.</span></span> <span data-ttu-id="7ea93-105">針對某些篩選， *提取* 模型更適合。</span><span class="sxs-lookup"><span data-stu-id="7ea93-105">For some filters, a *pull* model is more appropriate.</span></span> <span data-ttu-id="7ea93-106">在這裡，下游篩選器會向上游篩選要求資料。</span><span class="sxs-lookup"><span data-stu-id="7ea93-106">Here, the downstream filter requests data from the upstream filter.</span></span> <span data-ttu-id="7ea93-107">範例仍會從輸出釘選到輸入釘選，但下游篩選器會起始資料流程。</span><span class="sxs-lookup"><span data-stu-id="7ea93-107">Samples still travel downstream, from output pin to input pin, but the downstream filter initiates the data flow.</span></span> <span data-ttu-id="7ea93-108">這種類型的連接會使用 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面。</span><span class="sxs-lookup"><span data-stu-id="7ea93-108">This type of connection uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

<span data-ttu-id="7ea93-109">提取模型的一般用途是在檔案播放中。</span><span class="sxs-lookup"><span data-stu-id="7ea93-109">The typical use for the pull model is in file playback.</span></span> <span data-ttu-id="7ea93-110">例如，在 AVI 播放圖形中，非同步檔案 [來源](file-source--async--filter.md) 篩選會執行一般檔案讀取作業，並將資料傳遞為位元組資料流程，且沒有格式資訊。</span><span class="sxs-lookup"><span data-stu-id="7ea93-110">For example, in an AVI playback graph, the [Async File Source](file-source--async--filter.md) filter performs generic file reading operations and delivers the data as a byte stream, with no format information.</span></span> <span data-ttu-id="7ea93-111">[Avi 分隔](avi-splitter-filter.md)器篩選器會讀取 AVI 標頭，並將資料流程剖析成影片和音訊範例。</span><span class="sxs-lookup"><span data-stu-id="7ea93-111">The [AVI Splitter](avi-splitter-filter.md) filter reads the AVI headers and parses the stream into video and audio samples.</span></span> <span data-ttu-id="7ea93-112">AVI 分隔器可判斷所需的資料比非同步檔案來源篩選更好，因此它會使用 **IAsyncReader** 而不是 **IMemInputPin**。</span><span class="sxs-lookup"><span data-stu-id="7ea93-112">The AVI Splitter can determine what data it needs better than the Async File Source filter, and therefore it uses **IAsyncReader** instead of **IMemInputPin**.</span></span>

<span data-ttu-id="7ea93-113">若要從輸出圖釘要求資料，輸入的 pin 會呼叫下列其中一種方法：</span><span class="sxs-lookup"><span data-stu-id="7ea93-113">To request data from the output pin, the input pin calls one of the following methods:</span></span>

-   [<span data-ttu-id="7ea93-114">**IAsyncReader：： Request**</span><span class="sxs-lookup"><span data-stu-id="7ea93-114">**IAsyncReader::Request**</span></span>](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [<span data-ttu-id="7ea93-115">**IAsyncReader::SyncRead**</span><span class="sxs-lookup"><span data-stu-id="7ea93-115">**IAsyncReader::SyncRead**</span></span>](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   <span data-ttu-id="7ea93-116">[**IAsyncReader：： SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)。</span><span class="sxs-lookup"><span data-stu-id="7ea93-116">[**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span></span>

<span data-ttu-id="7ea93-117">第一個方法是非同步，可支援多個重迭讀取。</span><span class="sxs-lookup"><span data-stu-id="7ea93-117">The first method is asynchronous, to support multiple overlapped reads.</span></span> <span data-ttu-id="7ea93-118">其他則為同步。</span><span class="sxs-lookup"><span data-stu-id="7ea93-118">The others are synchronous.</span></span>

<span data-ttu-id="7ea93-119">理論上，任何篩選都可以支援 **IAsyncReader**，但實際上它是針對連接到剖析器篩選器的來源篩選所設計。</span><span class="sxs-lookup"><span data-stu-id="7ea93-119">In theory, any filter can support **IAsyncReader**, but in practice it is designed for source filters that connect to parser filters.</span></span> <span data-ttu-id="7ea93-120">剖析器的運作方式非常類似于推播模型中的來源篩選。</span><span class="sxs-lookup"><span data-stu-id="7ea93-120">The parser acts very much like a source filter in the push model.</span></span> <span data-ttu-id="7ea93-121">當它暫停時，它會建立串流執行緒，從 **IAsyncReader** 連接提取資料並將其推送至下游。</span><span class="sxs-lookup"><span data-stu-id="7ea93-121">When it pauses, it creates a streaming thread that pulls data from the **IAsyncReader** connection and pushes it downstream.</span></span> <span data-ttu-id="7ea93-122">輸出圖釘會使用 **IMemInputPin**，而圖形的其餘部分會使用標準推送模型。</span><span class="sxs-lookup"><span data-stu-id="7ea93-122">The output pins use **IMemInputPin**, and the rest of the graph uses the standard push model.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ea93-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="7ea93-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ea93-124">篩選圖形中的資料流程</span><span class="sxs-lookup"><span data-stu-id="7ea93-124">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



