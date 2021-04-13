---
description: Graph-Building 元件
ms.assetid: d803c56c-6fb1-4937-92e7-9ed2db2afc46
title: Graph-Building 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3ba346356109d8080d887a510cfcb85b6a6c80
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109892"
---
# <a name="graph-building-components"></a><span data-ttu-id="1d85e-103">Graph-Building 元件</span><span class="sxs-lookup"><span data-stu-id="1d85e-103">Graph-Building Components</span></span>

<span data-ttu-id="1d85e-104">DirectShow 提供數個可用於建立篩選圖形的元件。</span><span class="sxs-lookup"><span data-stu-id="1d85e-104">DirectShow provides several components that can be used to build filter graphs.</span></span> <span data-ttu-id="1d85e-105">這些選項包括：</span><span class="sxs-lookup"><span data-stu-id="1d85e-105">These include the following:</span></span>

-   <span data-ttu-id="1d85e-106">[篩選圖形管理員](filter-graph-manager.md)。</span><span class="sxs-lookup"><span data-stu-id="1d85e-106">[Filter Graph Manager](filter-graph-manager.md).</span></span> <span data-ttu-id="1d85e-107">此物件控制篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="1d85e-107">This object controls the filter graph.</span></span> <span data-ttu-id="1d85e-108">它支援 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)、 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)和 [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) 介面，還有其他介面。</span><span class="sxs-lookup"><span data-stu-id="1d85e-108">It supports the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder), [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol), and [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interfaces, among others.</span></span> <span data-ttu-id="1d85e-109">所有的 DirectShow 應用程式在某個時間點都會使用此物件，不過在某些情況下，其他物件會為應用程式建立篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="1d85e-109">All DirectShow applications use this object at some point, although in some cases another object creates the Filter Graph Manager for the application.</span></span>
-   <span data-ttu-id="1d85e-110">[Capture Graph Builder](capture-graph-builder.md)。</span><span class="sxs-lookup"><span data-stu-id="1d85e-110">[Capture Graph Builder](capture-graph-builder.md).</span></span> <span data-ttu-id="1d85e-111">此物件提供建立篩選圖形的其他方法。</span><span class="sxs-lookup"><span data-stu-id="1d85e-111">This object provides additional methods for building filter graphs.</span></span> <span data-ttu-id="1d85e-112">它原本是設計來建立可執行影片捕獲的圖形 (因此，名稱) 但對許多其他類型的自訂篩選圖形都很有用。</span><span class="sxs-lookup"><span data-stu-id="1d85e-112">It was originally designed for building graphs that perform video capture (hence the name) but is useful for many other types of custom filter graph.</span></span> <span data-ttu-id="1d85e-113">它支援 [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) 介面。</span><span class="sxs-lookup"><span data-stu-id="1d85e-113">It supports the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span>
-   <span data-ttu-id="1d85e-114">[篩選](filter-mapper.md) 對應程式和 [系統裝置枚舉](system-device-enumerator.md)器。</span><span class="sxs-lookup"><span data-stu-id="1d85e-114">[Filter Mapper](filter-mapper.md) and [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="1d85e-115">這些物件會尋找在使用者系統上或代表硬體裝置註冊的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="1d85e-115">These objects locate filters that are registered on the user's system, or that represent hardware devices.</span></span>
-   <span data-ttu-id="1d85e-116">[DVD Graph Builder](dvd-graph-builder.md)。</span><span class="sxs-lookup"><span data-stu-id="1d85e-116">[DVD Graph Builder](dvd-graph-builder.md).</span></span> <span data-ttu-id="1d85e-117">這個物件會建立用於 DVD 播放和流覽的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="1d85e-117">This object builds filter graphs for DVD playback and navigation.</span></span> <span data-ttu-id="1d85e-118">它支援 [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) 介面。</span><span class="sxs-lookup"><span data-stu-id="1d85e-118">It supports the [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) interface.</span></span>

### <a name="intelligent-connect"></a><span data-ttu-id="1d85e-119">智慧型連接</span><span class="sxs-lookup"><span data-stu-id="1d85e-119">Intelligent Connect</span></span>

<span data-ttu-id="1d85e-120">「智慧型連接」一詞涵蓋一組演算法，篩選圖形管理員會使用這些演算法來建立全部或部分的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="1d85e-120">The term "Intelligent Connect" covers a set of algorithms that the Filter Graph Manager uses to build all or part of a filter graph.</span></span> <span data-ttu-id="1d85e-121">每當篩選圖形管理員需要額外的篩選才能完成圖形時，大致上會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="1d85e-121">Whenever the Filter Graph Manager requires additional filters to complete the graph, it does roughly the following:</span></span>

1.  <span data-ttu-id="1d85e-122">如果圖形中目前有篩選，而且至少有一個未連接的輸入 pin，則篩選圖形管理員會嘗試使用該篩選準則。</span><span class="sxs-lookup"><span data-stu-id="1d85e-122">If there is a filter currently in the graph, with at least one unconnected input pin, the Filter Graph Manager tries to use that filter.</span></span>
2.  <span data-ttu-id="1d85e-123">否則，篩選圖形管理員會在登錄中尋找可以接受正確媒體類型進行連接的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="1d85e-123">Otherwise, the Filter Graph Manager looks in the registry for filters that can accept the correct media type for the connection.</span></span> <span data-ttu-id="1d85e-124">每個篩選器都有一個稱為「提供」的登錄值，這表示篩選器在完成圖形時大概會有多大的説明。</span><span class="sxs-lookup"><span data-stu-id="1d85e-124">Each filter has a registry value called "Merit," which indicates roughly how likely the filter is to be useful in completing the graph.</span></span> <span data-ttu-id="1d85e-125">篩選圖形管理員會依最高階值的順序來嘗試篩選。</span><span class="sxs-lookup"><span data-stu-id="1d85e-125">The Filter Graph Manager tries filters in order of merit value.</span></span> <span data-ttu-id="1d85e-126">針對每個資料流程類型 (例如音訊、影片或 MIDI) ，預設轉譯器的優點很高。</span><span class="sxs-lookup"><span data-stu-id="1d85e-126">For each stream type (such as audio, video, or MIDI), the default renderer has a high merit.</span></span> <span data-ttu-id="1d85e-127">這些解碼器也有很多優點。</span><span class="sxs-lookup"><span data-stu-id="1d85e-127">Decoders also have high merit.</span></span> <span data-ttu-id="1d85e-128">特殊用途的篩選具有較低的業績。</span><span class="sxs-lookup"><span data-stu-id="1d85e-128">Special-purpose filters have low merit.</span></span>

<span data-ttu-id="1d85e-129">如果篩選圖形管理員停滯，則會返回並嘗試不同的篩選組合。</span><span class="sxs-lookup"><span data-stu-id="1d85e-129">If the Filter Graph Manager gets stuck, it will back out and try a different combination of filters.</span></span> <span data-ttu-id="1d85e-130">您可以在 [智慧型 Connect](intelligent-connect.md)主題中找到確切的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1d85e-130">You can find the exact details in the topic [Intelligent Connect](intelligent-connect.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d85e-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d85e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d85e-132">建立篩選圖形</span><span class="sxs-lookup"><span data-stu-id="1d85e-132">Building the Filter Graph</span></span>](building-the-filter-graph.md)
</dt> </dl>

 

 



