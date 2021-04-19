---
description: 傳輸
ms.assetid: 63c5ff5b-293d-4a80-92e8-3ece41321095
title: 傳輸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3d87ffacc871fc45ef1e8e645849afc956fb1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979200"
---
# <a name="transports"></a><span data-ttu-id="fddbc-103">傳輸</span><span class="sxs-lookup"><span data-stu-id="fddbc-103">Transports</span></span>

<span data-ttu-id="fddbc-104">為了透過篩選圖形來移動媒體資料，DirectShow 濾波器必須支援數個可能的通訊協定之一。</span><span class="sxs-lookup"><span data-stu-id="fddbc-104">In order to move media data through the filter graph, a DirectShow filter must support one of several possible protocols.</span></span> <span data-ttu-id="fddbc-105">這些通訊協定稱為「傳輸」。</span><span class="sxs-lookup"><span data-stu-id="fddbc-105">These protocols are called transports.</span></span> <span data-ttu-id="fddbc-106">當兩個篩選準則連接時，它們必須支援相同的傳輸;否則無法交換媒體資料。</span><span class="sxs-lookup"><span data-stu-id="fddbc-106">When two filters connect, they must support the same transport; otherwise they cannot exchange media data.</span></span> <span data-ttu-id="fddbc-107">一般而言，傳輸需要其中一個 pin 支援特定的介面。</span><span class="sxs-lookup"><span data-stu-id="fddbc-107">Typically, a transport requires that one of the pins support a particular interface.</span></span> <span data-ttu-id="fddbc-108">當篩選準則連線時，其中一個 pin 會查詢該介面的另一個。</span><span class="sxs-lookup"><span data-stu-id="fddbc-108">When the filters connect, one pin queries the other for the interface.</span></span>

<span data-ttu-id="fddbc-109">大部分的 DirectShow 篩選器會在主要記憶體中保存媒體資料，並將其傳遞至不同的 pin 連線篩選。</span><span class="sxs-lookup"><span data-stu-id="fddbc-109">Most DirectShow filters hold media data in main memory, and deliver it to other filters across pin connections.</span></span> <span data-ttu-id="fddbc-110">這種類型的傳輸稱為本機記憶體傳輸。</span><span class="sxs-lookup"><span data-stu-id="fddbc-110">This type of transport is called local memory transport.</span></span> <span data-ttu-id="fddbc-111">雖然本機記憶體傳輸是 DirectShow 中最常見的傳輸，但是並非所有篩選都使用它。</span><span class="sxs-lookup"><span data-stu-id="fddbc-111">Although local memory transport is the most common transport in DirectShow, not all filters use it.</span></span> <span data-ttu-id="fddbc-112">例如，某些篩選器會沿著硬體路徑傳送媒體資料，並只使用 pin 來提供控制資訊。</span><span class="sxs-lookup"><span data-stu-id="fddbc-112">For example, some filters send media data along a hardware path, and use pins only to deliver control information.</span></span> <span data-ttu-id="fddbc-113">例如，請參閱 [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) 介面。</span><span class="sxs-lookup"><span data-stu-id="fddbc-113">For example, see the [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) interface.</span></span>

<span data-ttu-id="fddbc-114">DirectShow 定義了兩種機制來進行本機記憶體傳輸、推播模型和提取模型。</span><span class="sxs-lookup"><span data-stu-id="fddbc-114">DirectShow defines two mechanisms for local memory transport, the push model and the pull model.</span></span> <span data-ttu-id="fddbc-115">在推送模型中，來源篩選會產生資料，並將它傳遞給下一個篩選器下游。</span><span class="sxs-lookup"><span data-stu-id="fddbc-115">In the push model, a source filter generates data and delivers it to the next filter downstream.</span></span> <span data-ttu-id="fddbc-116">該篩選會被動接收資料、處理資料，並進一步將它傳送給下游。</span><span class="sxs-lookup"><span data-stu-id="fddbc-116">That filter passively receives the data, processes it, and sends it further downstream.</span></span> <span data-ttu-id="fddbc-117">在提取模型中，來源篩選會連接到剖析器篩選器。</span><span class="sxs-lookup"><span data-stu-id="fddbc-117">In the pull model, the source filter is connected to a parser filter.</span></span> <span data-ttu-id="fddbc-118">剖析器篩選器會從來源篩選要求資料。</span><span class="sxs-lookup"><span data-stu-id="fddbc-118">The parser filter requests data from the source filter.</span></span> <span data-ttu-id="fddbc-119">來源篩選器會藉由傳遞資料來回應要求。</span><span class="sxs-lookup"><span data-stu-id="fddbc-119">The source filter responds to the requests by delivering data.</span></span> <span data-ttu-id="fddbc-120">推送模型使用 [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) 介面，而提取模型則使用 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 介面。</span><span class="sxs-lookup"><span data-stu-id="fddbc-120">The push model uses the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, and the pull model uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

<span data-ttu-id="fddbc-121">推送模型比提取模型更常見。</span><span class="sxs-lookup"><span data-stu-id="fddbc-121">The push model is more common than the pull model.</span></span> <span data-ttu-id="fddbc-122">因此，接下來的文章會採用推送模型。</span><span class="sxs-lookup"><span data-stu-id="fddbc-122">Therefore, the articles that follow assume a push model.</span></span> <span data-ttu-id="fddbc-123">此區段中的最後一篇文章（ [提取模型](pull-model.md)）描述 **IAsyncReader** 介面與 **IMemInputPin** 有何不同。</span><span class="sxs-lookup"><span data-stu-id="fddbc-123">The last article in this section, [Pull Model](pull-model.md), describes how the **IAsyncReader** interface differs from **IMemInputPin**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fddbc-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="fddbc-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fddbc-125">篩選圖形中的資料流程</span><span class="sxs-lookup"><span data-stu-id="fddbc-125">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



