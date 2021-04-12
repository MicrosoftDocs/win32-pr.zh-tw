---
description: Pin 連接
ms.assetid: 1406ade4-77d8-49a7-8f36-cc49ff007a26
title: Pin 連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b509abddf4a915b65dfd322f76b4afb132a7f835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385648"
---
# <a name="pin-connections"></a><span data-ttu-id="81c77-103">Pin 連接</span><span class="sxs-lookup"><span data-stu-id="81c77-103">Pin Connections</span></span>

<span data-ttu-id="81c77-104">篩選器會透過 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面，在其針腳上連接。</span><span class="sxs-lookup"><span data-stu-id="81c77-104">Filters connect at their pins, through the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="81c77-105">輸出連接會連線至輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="81c77-105">Output pins connect to input pins.</span></span> <span data-ttu-id="81c77-106">每個 pin 連線都有媒體類型，由 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構所描述。</span><span class="sxs-lookup"><span data-stu-id="81c77-106">Each pin connection has a media type, described by the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="81c77-107">應用程式會藉由呼叫篩選圖形管理員上的方法來連接篩選，而不會藉由呼叫篩選或釘選上的方法。</span><span class="sxs-lookup"><span data-stu-id="81c77-107">An application connects filters by calling methods on the Filter Graph Manager, never by calling methods on the filters or pins themselves.</span></span> <span data-ttu-id="81c77-108">應用程式可以藉由呼叫 [**IFilterGraph：： ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) 或 [**IGraphBuilder：： connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) 方法，直接指定要連接的篩選準則;或者，它可以使用圖表建立方法（例如 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)）間接連接篩選。</span><span class="sxs-lookup"><span data-stu-id="81c77-108">The application can directly specify which filters to connect, by calling the [**IFilterGraph::ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) or [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) method; or it can connect filters indirectly, using a graph-building method such as [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).</span></span>

<span data-ttu-id="81c77-109">若要讓連接成功，這兩個篩選準則必須在篩選圖形中。</span><span class="sxs-lookup"><span data-stu-id="81c77-109">For the connection to succeed, both filters must be in the filter graph.</span></span> <span data-ttu-id="81c77-110">應用程式可以藉由呼叫 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 方法，將篩選新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="81c77-110">The application can add a filter to the graph by calling the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method.</span></span> <span data-ttu-id="81c77-111">篩選圖形管理員也可以將篩選新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="81c77-111">The Filter Graph Manager may add filters to the graph, as well.</span></span> <span data-ttu-id="81c77-112">加入篩選準則時，篩選圖形管理員會呼叫篩選器的 [**IBaseFilter：： JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) 方法來通知篩選。</span><span class="sxs-lookup"><span data-stu-id="81c77-112">When a filter is added, the Filter Graph Manager calls the filter's [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method to notify the filter.</span></span>

<span data-ttu-id="81c77-113">連接程式的一般大綱如下所示：</span><span class="sxs-lookup"><span data-stu-id="81c77-113">The general outline of the connection process is the following:</span></span>

1.  <span data-ttu-id="81c77-114">篩選圖形管理員會在輸出釘選上呼叫 [**IPin：： Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) ，並將指標傳遞至輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="81c77-114">The Filter Graph Manager calls [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) on the output pin, passing a pointer to the input pin.</span></span>
2.  <span data-ttu-id="81c77-115">如果輸出 pin 接受連接，則會在輸入 pin 上呼叫 [**IPin：： ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) 。</span><span class="sxs-lookup"><span data-stu-id="81c77-115">If the output pin accepts the connection, it calls [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) on the input pin.</span></span>
3.  <span data-ttu-id="81c77-116">如果輸入釘選也接受連接，連接嘗試就會成功，而且會連線到 pin。</span><span class="sxs-lookup"><span data-stu-id="81c77-116">If the input pin also accepts the connection, the connection attempt succeeds and the pins are connected.</span></span>

<span data-ttu-id="81c77-117">當篩選準則為作用中時，某些 pin 可以中斷連接並重新連接。</span><span class="sxs-lookup"><span data-stu-id="81c77-117">Some pins can be disconnected and reconnected while the filter is active.</span></span> <span data-ttu-id="81c77-118">這種類型的重新連接稱為 *動態* 重新連接。</span><span class="sxs-lookup"><span data-stu-id="81c77-118">This type of reconnection is called a *dynamic* reconnection.</span></span> <span data-ttu-id="81c77-119">如需詳細資訊，請參閱 [動態圖形建築物](dynamic-graph-building.md)。</span><span class="sxs-lookup"><span data-stu-id="81c77-119">For more information, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span> <span data-ttu-id="81c77-120">不過，大部分的篩選器都不支援動態重新連接。</span><span class="sxs-lookup"><span data-stu-id="81c77-120">However, most filters do not support dynamic reconnection.</span></span>

<span data-ttu-id="81c77-121">篩選通常會以下游順序連接，換句話說，篩選器的輸入接點會在其輸出圖釘之前連線。</span><span class="sxs-lookup"><span data-stu-id="81c77-121">Filters are usually connected in downstream order—in other words, the filter's input pins are connected before its output pins.</span></span> <span data-ttu-id="81c77-122">篩選準則應該一律支援此連接順序。</span><span class="sxs-lookup"><span data-stu-id="81c77-122">A filter should always support this order of connection.</span></span> <span data-ttu-id="81c77-123">某些篩選準則也會以相反的順序支援連接—輸出釘選，後面接著輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="81c77-123">Some filters also support connections in the opposite order—output pins first, followed by input pins.</span></span> <span data-ttu-id="81c77-124">例如，在連接 MUX 篩選器的輸入圖釘之前，可能可以將 MUX 篩選器的輸出圖釘連接至檔案寫入器篩選器。</span><span class="sxs-lookup"><span data-stu-id="81c77-124">For example, it might be possible to connect a MUX filter's output pin to the file-writer filter, before connecting the MUX filter's input pins.</span></span>

<span data-ttu-id="81c77-125">當呼叫 pin 的 **Connect** 或 **ReceiveConnection** 方法時，pin 必須確認它可以支援連接。</span><span class="sxs-lookup"><span data-stu-id="81c77-125">When a pin's **Connect** or **ReceiveConnection** method is called, the pin must verify that it can support the connection.</span></span> <span data-ttu-id="81c77-126">詳細資料取決於特定的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="81c77-126">The details depend on the particular filter.</span></span> <span data-ttu-id="81c77-127">最常見的工作包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="81c77-127">The most common tasks include the following:</span></span>

-   <span data-ttu-id="81c77-128">檢查媒體類型是否可接受</span><span class="sxs-lookup"><span data-stu-id="81c77-128">Check that the media type is acceptable</span></span>
-   <span data-ttu-id="81c77-129">協調配置器</span><span class="sxs-lookup"><span data-stu-id="81c77-129">Negotiate an allocator</span></span>
-   <span data-ttu-id="81c77-130">查詢其他 pin 以取得必要的介面。</span><span class="sxs-lookup"><span data-stu-id="81c77-130">Query the other pin for required interfaces.</span></span>

 

 



