---
description: 動態格式變更
ms.assetid: ff60de5a-3edc-405d-aa02-8704b96d5e87
title: 動態格式變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49496e0b43d9b120f6daf27007cde98191a7765b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970502"
---
# <a name="dynamic-format-changes"></a><span data-ttu-id="9399a-103">動態格式變更</span><span class="sxs-lookup"><span data-stu-id="9399a-103">Dynamic Format Changes</span></span>

<span data-ttu-id="9399a-104">當兩個篩選準則連線時，它們會同意媒體類型，以描述上游篩選器將傳遞的資料格式。</span><span class="sxs-lookup"><span data-stu-id="9399a-104">When two filters connect, they agree on a media type, which describes the format of the data that the upstream filter will deliver.</span></span> <span data-ttu-id="9399a-105">在大部分的情況下，媒體類型在連線期間都是固定的。</span><span class="sxs-lookup"><span data-stu-id="9399a-105">In most cases, the media type is fixed for the duration of the connection.</span></span> <span data-ttu-id="9399a-106">但是，DirectShow 確實提供篩選器的有限支援來變更媒體類型。</span><span class="sxs-lookup"><span data-stu-id="9399a-106">However, DirectShow does offer limited support for filters to change the media type.</span></span> <span data-ttu-id="9399a-107">當篩選參數切換媒體類型時，它稱為 *動態格式變更*。</span><span class="sxs-lookup"><span data-stu-id="9399a-107">When a filter switches media types, it is called a *dynamic format change*.</span></span> <span data-ttu-id="9399a-108">如果您正在撰寫 DirectShow 篩選器，您應該留意動態格式變更的機制。</span><span class="sxs-lookup"><span data-stu-id="9399a-108">If you are writing a DirectShow filter, you should be aware of the mechanisms for dynamic format changes.</span></span> <span data-ttu-id="9399a-109">即使您的篩選不支援這類變更，如果另一個篩選要求新的格式，則應該會正確地回應。</span><span class="sxs-lookup"><span data-stu-id="9399a-109">Even if your filter does not support such changes, it should respond correctly if another filter requests a new format.</span></span>

<span data-ttu-id="9399a-110">DirectShow 定義了數種不同的動態格式變更機制，視篩選圖形的狀態以及所需的變更類型而定。</span><span class="sxs-lookup"><span data-stu-id="9399a-110">DirectShow defines several distinct mechanisms for dynamic format changes, depending on the state of filter graph and the type of change that is required.</span></span>

-   <span data-ttu-id="9399a-111">如果圖形已停止，則 pin 可以重新連接並重新協商媒體類型。</span><span class="sxs-lookup"><span data-stu-id="9399a-111">If the graph is stopped, the pins can reconnect and renegotiate the media type.</span></span> <span data-ttu-id="9399a-112">如需詳細資訊，請參閱重新 [連接 pin](reconnecting-pins.md)。</span><span class="sxs-lookup"><span data-stu-id="9399a-112">For more information, see [Reconnecting Pins](reconnecting-pins.md).</span></span>
-   <span data-ttu-id="9399a-113">某些篩選器可以重新連接釘選，即使圖形處於作用中狀態 (執行中或已暫停) 。</span><span class="sxs-lookup"><span data-stu-id="9399a-113">Some filters can reconnect pins even while the graph is active (running or paused).</span></span> <span data-ttu-id="9399a-114">如需此機制的詳細資訊，請參閱 [動態重新連接](dynamic-reconnection.md)。</span><span class="sxs-lookup"><span data-stu-id="9399a-114">For more information about this mechanism, see [Dynamic Reconnection](dynamic-reconnection.md).</span></span>

<span data-ttu-id="9399a-115">否則，如果圖形正在使用中，但有問題的篩選器不支援動態 pin 重新連接，則有三種可能的機制可以變更格式：</span><span class="sxs-lookup"><span data-stu-id="9399a-115">Otherwise, if the graph is active, but the filters in question do not support dynamic pin reconnections, there are three possible mechanisms for changing the format:</span></span>

-   <span data-ttu-id="9399a-116">如果輸出圖釘建議將格式變更提供給其下游對等，但只有在新的格式不需要較大的緩衝區時，就會使用[QueryAccept (下游) ](queryaccept--downstream.md) 。</span><span class="sxs-lookup"><span data-stu-id="9399a-116">[QueryAccept (Downstream)](queryaccept--downstream.md) is used when If an output pin proposes a format change to its downstream peer, but only if the new format does not require a larger buffer.</span></span>
-   <span data-ttu-id="9399a-117">[QueryAccept (上游) ](queryaccept--upstream.md) 是在輸入 pin 提議對其上游對等的格式變更時使用。</span><span class="sxs-lookup"><span data-stu-id="9399a-117">[QueryAccept (Upstream)](queryaccept--upstream.md) is used when an input pin proposes a format change to its upstream peer.</span></span> <span data-ttu-id="9399a-118">新格式可以是相同大小，也可以較大。</span><span class="sxs-lookup"><span data-stu-id="9399a-118">The new format can be the same size, or it can be larger.</span></span>
-   <span data-ttu-id="9399a-119">當輸出釘選對其下游對等的格式變更時，會使用[ReceiveConnection](receiveconnection.md) ，而新的格式需要較大的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9399a-119">[ReceiveConnection](receiveconnection.md) is used when an output pin proposes a format change to its downstream peer, and the new format requires a larger buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9399a-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="9399a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9399a-121">處理影片轉譯器的格式變更</span><span class="sxs-lookup"><span data-stu-id="9399a-121">Handling Format Changes from the Video Renderer</span></span>](handling-format-changes-from-the-video-renderer.md)
</dt> </dl>

 

 



