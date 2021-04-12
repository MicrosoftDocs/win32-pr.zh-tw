---
description: 重新連接釘選
ms.assetid: 34b3e4de-e4eb-48c5-aaef-fc99b63e8691
title: 重新連接釘選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9fc71b4d5a62ee066edaa5f97b4cc3332b2231d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509991"
---
# <a name="reconnecting-pins"></a><span data-ttu-id="6d373-103">重新連接釘選</span><span class="sxs-lookup"><span data-stu-id="6d373-103">Reconnecting Pins</span></span>

<span data-ttu-id="6d373-104">在 pin 連線期間，篩選器可以中斷連接並重新連接其中一個其他 pin，如下所示：</span><span class="sxs-lookup"><span data-stu-id="6d373-104">During a pin connection, a filter can disconnect and reconnect one of its other pins, as follows:</span></span>

1.  <span data-ttu-id="6d373-105">篩選準則會在其他篩選器的 pin 上呼叫 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) ，並指定新的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6d373-105">The filter calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on the other filter's pin, and specifies the new media type.</span></span>
2.  <span data-ttu-id="6d373-106">如果 **QueryAccept** 傳回 S \_ OK，則篩選準則會呼叫 [**IFilterGraph2：： ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) 來重新連接釘選。</span><span class="sxs-lookup"><span data-stu-id="6d373-106">If **QueryAccept** returns S\_OK, the filter calls [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) to reconnect the pins.</span></span>

<span data-ttu-id="6d373-107">以下是篩選可能需要重新連接 pin 的一些範例：</span><span class="sxs-lookup"><span data-stu-id="6d373-107">The following are some examples of when a filter might need to reconnect pins:</span></span>

-   <span data-ttu-id="6d373-108">**T 篩選準則。**</span><span class="sxs-lookup"><span data-stu-id="6d373-108">**Tee filters.**</span></span> <span data-ttu-id="6d373-109">*T 篩選準則* 會將輸入資料流程分割成多個輸出，而不會變更資料流程中的資料。</span><span class="sxs-lookup"><span data-stu-id="6d373-109">A *tee filter* splits an input stream into multiple outputs without changing the data in the stream.</span></span> <span data-ttu-id="6d373-110">指標篩選器可以接受一系列的媒體類型，但類型必須符合所有的釘選連接。</span><span class="sxs-lookup"><span data-stu-id="6d373-110">A tee filter can accept a range of media types, but the types must match across all pin connections.</span></span> <span data-ttu-id="6d373-111">因此，當輸入 pin 連線時，篩選可能需要重新協商輸出針腳上的任何現有連接，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="6d373-111">Therefore, when the input pin connects, the filter might need to renegotiate any existing connections on the output pins, and vice versa.</span></span> <span data-ttu-id="6d373-112">如需範例，請參閱 [InfTee 篩選範例](inftee-filter-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="6d373-112">For an example, see the [InfTee Filter Sample](inftee-filter-sample.md).</span></span>
-   <span data-ttu-id="6d373-113">**就地記錄篩選。**</span><span class="sxs-lookup"><span data-stu-id="6d373-113">**Trans-in-place filters.**</span></span> <span data-ttu-id="6d373-114">*就地* 篩選會修改原始緩衝區中的輸入資料，而不是將資料複製到個別的輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6d373-114">A *trans-in-place* filter modifies the input data in the original buffer instead of copying the data to a separate output buffer.</span></span> <span data-ttu-id="6d373-115">就地篩選必須針對上游和下游連接使用相同的配置器。</span><span class="sxs-lookup"><span data-stu-id="6d373-115">A trans-in-place filter must use the same allocator for both the upstream and the downstream connections.</span></span> <span data-ttu-id="6d373-116">第一個連接 (輸入或輸出的 pin) 會以一般方式協調配置器。</span><span class="sxs-lookup"><span data-stu-id="6d373-116">The first pin to connect (input or output) negotiates an allocator in the usual way.</span></span> <span data-ttu-id="6d373-117">不過，當其他 pin 連線時，可能無法接受第一個配置器。</span><span class="sxs-lookup"><span data-stu-id="6d373-117">When the other pin connects, however, the first allocator might not be acceptable.</span></span> <span data-ttu-id="6d373-118">在這種情況下，第二個 pin 會選擇不同的配置器，而第一個 pin 會使用新的配置器重新連接。</span><span class="sxs-lookup"><span data-stu-id="6d373-118">In that case, the second pin chooses a different allocator, and the first pin reconnects using the new allocator.</span></span> <span data-ttu-id="6d373-119">如需範例執行，請參閱 [**CTransInPlaceFilter**](ctransinplacefilter.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="6d373-119">For an example implementation, see the [**CTransInPlaceFilter**](ctransinplacefilter.md) class.</span></span>

<span data-ttu-id="6d373-120">在 **ReconnectEx** 方法中，篩選圖形管理員會以非同步方式中斷連接並重新連接釘選。</span><span class="sxs-lookup"><span data-stu-id="6d373-120">In the **ReconnectEx** method, the Filter Graph Manager asynchronously disconnects and reconnects the pins.</span></span> <span data-ttu-id="6d373-121">除非 **QueryAccept** 傳回 S OK，否則篩選準則不得嘗試重新連接 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6d373-121">The filter must not attempt the reconnection unless **QueryAccept** returns S\_OK.</span></span> <span data-ttu-id="6d373-122">否則，pin 將會保持中斷連線，而導致圖形錯誤。</span><span class="sxs-lookup"><span data-stu-id="6d373-122">Otherwise, the pin will be left disconnected, causing graph errors.</span></span> <span data-ttu-id="6d373-123">此外，篩選器也應該在相同的執行緒上，從 [**IPin：： Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) 方法內要求重新連接。</span><span class="sxs-lookup"><span data-stu-id="6d373-123">Also, the filter should request the reconnection from inside the [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) method, on the same thread.</span></span> <span data-ttu-id="6d373-124">如果 **連接** 方法在某個執行緒上傳回，而另一個執行緒進行重新連接要求，則篩選圖形管理員可能會在進行重新連接之前執行圖形，進而導致圖形錯誤。</span><span class="sxs-lookup"><span data-stu-id="6d373-124">If the **Connect** method returns on one thread, while another thread makes the reconnection request, the Filter Graph Manager might run the graph before it makes the reconnection, causing graph errors.</span></span>

 

 



