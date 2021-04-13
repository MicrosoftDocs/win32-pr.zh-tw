---
description: 資料流程結束通知
ms.assetid: cf2b13bc-5b54-4ac7-8a33-7434126fdf31
title: 資料流程結束通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53fcdfef1225aa5b93b56aeaa0d8ae9d0a8550c9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187541"
---
# <a name="end-of-stream-notifications"></a><span data-ttu-id="07784-103">資料流程結束通知</span><span class="sxs-lookup"><span data-stu-id="07784-103">End-of-Stream Notifications</span></span>

<span data-ttu-id="07784-104">當來源篩選完成傳送資料時，它會在下游輸入 pin 上呼叫 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 方法。</span><span class="sxs-lookup"><span data-stu-id="07784-104">When a source filter is done sending data, it calls the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method on the downstream input pin.</span></span> <span data-ttu-id="07784-105">下游篩選器會將呼叫傳播至下一個篩選器，依此類推。</span><span class="sxs-lookup"><span data-stu-id="07784-105">The downstream filter propagates the call to the next filter, and so on.</span></span> <span data-ttu-id="07784-106">當 **EndOfStream** 呼叫到達轉譯器時，轉譯器會將 [**EC \_ 完成**](ec-complete.md) 事件傳送至篩選圖形管理員。</span><span class="sxs-lookup"><span data-stu-id="07784-106">When the **EndOfStream** call reaches the renderer, the renderer sends an [**EC\_COMPLETE**](ec-complete.md) event to the Filter Graph Manager.</span></span> <span data-ttu-id="07784-107">如果轉譯器有多個輸入圖釘，則會 \_ 在每個輸入 pin 收到「資料流程結束」通知之後，傳遞 EC COMPLETE 事件。</span><span class="sxs-lookup"><span data-stu-id="07784-107">If the renderer has multiple input pins, it delivers the EC\_COMPLETE event after every input pin has received the end-of-stream notification.</span></span>

<span data-ttu-id="07784-108">篩選準則必須將 [**EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 呼叫與其他串流呼叫（例如 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)）進行序列化。</span><span class="sxs-lookup"><span data-stu-id="07784-108">A filter must serialize [**EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) calls with other streaming calls, such as [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).</span></span> <span data-ttu-id="07784-109"> (換句話說，下游篩選準則一律必須以正確的順序接收呼叫。 ) </span><span class="sxs-lookup"><span data-stu-id="07784-109">(In other words, the downstream filter must always receive the calls in the correct order.)</span></span>

<span data-ttu-id="07784-110">在某些情況下，下游篩選器可能會在來源篩選器之前偵測到資料流程的結尾。</span><span class="sxs-lookup"><span data-stu-id="07784-110">In some cases, a downstream filter might detect the end of the stream before the source filter does.</span></span> <span data-ttu-id="07784-111"> (例如，下游篩選可能正在剖析資料流程 ) 。在這種情況下，下游篩選器可以傳送資料流程結束通知，在這種情況下，它應該會傳回 FALSE， \_ 從 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 直到圖形停止或排清為止。</span><span class="sxs-lookup"><span data-stu-id="07784-111">(For example, the downstream filter might be parsing the stream.) In that case, the downstream filter can send the end-of-stream notification, in which case it should return S\_FALSE from [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) until the graph stops or flushes.</span></span> <span data-ttu-id="07784-112">FALSE 傳回 \_ 值會通知來源篩選停止傳送資料。</span><span class="sxs-lookup"><span data-stu-id="07784-112">The S\_FALSE return value informs the source filter to stop sending data.</span></span>

### <a name="default-handling-of-ec_complete"></a><span data-ttu-id="07784-113">EC 完成的預設處理 \_</span><span class="sxs-lookup"><span data-stu-id="07784-113">Default Handling of EC\_COMPLETE</span></span>

<span data-ttu-id="07784-114">篩選圖形管理員預設不會將每個 EC \_ 完成事件轉寄至應用程式。</span><span class="sxs-lookup"><span data-stu-id="07784-114">By default, the Filter Graph Manager does not forward every EC\_COMPLETE event to the application.</span></span> <span data-ttu-id="07784-115">相反地，它會等到所有串流都已 \_ 完成通知 EC，然後傳送單一的 EC \_ 完成事件。</span><span class="sxs-lookup"><span data-stu-id="07784-115">Instead, it waits until all streams have signaled EC\_COMPLETE and then sends a single EC\_COMPLETE event.</span></span> <span data-ttu-id="07784-116">因此，應用程式會在每個資料流程完成之後接收事件。</span><span class="sxs-lookup"><span data-stu-id="07784-116">Thus, the application receives the event after every stream has completed.</span></span>

<span data-ttu-id="07784-117">若要判斷資料流程的數目，篩選圖形管理員會計算支援透過 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 或) [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 搜尋 (的篩選器數目，並 *具有轉譯的輸入圖釘* ，其定義為沒有對應輸出的輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="07784-117">To determine the number of streams, the Filter Graph Manager counts the number of filters that support seeking (through [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) or [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)) and have a *rendered* input pin, which is defined as an input pin with no corresponding outputs.</span></span> <span data-ttu-id="07784-118">篩選圖形管理員會以下列兩種方式之一來判斷是否轉譯 pin：</span><span class="sxs-lookup"><span data-stu-id="07784-118">The Filter Graph Manager determines whether a pin is rendered in one of two ways:</span></span>

-   <span data-ttu-id="07784-119">Pin 的 [**IPin：： QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) 方法會在 *nPin* 參數中傳回零。</span><span class="sxs-lookup"><span data-stu-id="07784-119">The pin's [**IPin::QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) method returns zero in the *nPin* parameter.</span></span>
-   <span data-ttu-id="07784-120">篩選會公開 [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) 介面，並傳回 AM \_ 篩選器 \_ \_ 的其他旗標為轉譯器 \_ 旗標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="07784-120">The filter exposes the [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) interface and returns the AM\_FILTER\_MISC\_FLAGS\_IS\_RENDERER flag.</span></span>

### <a name="end-of-stream-notifications-in-pull-mode"></a><span data-ttu-id="07784-121">提取模式中的資料流程結束通知</span><span class="sxs-lookup"><span data-stu-id="07784-121">End-of-Stream Notifications in Pull Mode</span></span>

<span data-ttu-id="07784-122">在 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 連接中，來源篩選不會傳送資料流程結束通知。</span><span class="sxs-lookup"><span data-stu-id="07784-122">In an [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) connection, the source filter does not send an end-of-stream notification.</span></span> <span data-ttu-id="07784-123">Instread，這是由下游篩選器（通常是剖析器篩選器）來完成。</span><span class="sxs-lookup"><span data-stu-id="07784-123">Instread, this is done by the downstream filter, which is typically a parser filter.</span></span> <span data-ttu-id="07784-124">剖析器會將 [**EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 呼叫傳送給下游。</span><span class="sxs-lookup"><span data-stu-id="07784-124">The parser sends the [**EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) call downstream.</span></span> <span data-ttu-id="07784-125">它不會傳送一個上游給來源篩選。</span><span class="sxs-lookup"><span data-stu-id="07784-125">It does not send one upstream to the source filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07784-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="07784-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07784-127">傳遞資料流程結尾</span><span class="sxs-lookup"><span data-stu-id="07784-127">Delivering the End of Stream</span></span>](delivering-the-end-of-stream.md)
</dt> </dl>

 

 



