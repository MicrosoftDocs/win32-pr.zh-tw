---
title: Proxy
description: Proxy 位於呼叫進程的位址空間中，並作為遠端物件的代理。
ms.assetid: 6c82f655-ac46-4ed9-992b-0387b324a8f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11257dd060f51bef118a4afc0cc35acf995c111
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "106976616"
---
# <a name="proxy"></a><span data-ttu-id="8483a-103">Proxy</span><span class="sxs-lookup"><span data-stu-id="8483a-103">Proxy</span></span>

<span data-ttu-id="8483a-104">Proxy 位於呼叫進程的位址空間中，並作為遠端物件的代理。</span><span class="sxs-lookup"><span data-stu-id="8483a-104">A proxy resides in the address space of the calling process and acts as a surrogate for the remote object.</span></span> <span data-ttu-id="8483a-105">從呼叫物件的觀點來看，proxy 就是物件。</span><span class="sxs-lookup"><span data-stu-id="8483a-105">From the perspective of the calling object, the proxy is the object.</span></span> <span data-ttu-id="8483a-106">一般而言，proxy 的角色是封裝介面參數，以呼叫其物件介面中的方法。</span><span class="sxs-lookup"><span data-stu-id="8483a-106">Typically, the proxy's role is to package the interface parameters for calls to methods in its object interfaces.</span></span> <span data-ttu-id="8483a-107">Proxy 會將參數封裝至訊息緩衝區，並將緩衝區傳遞至通道，以處理處理常式之間的傳輸。</span><span class="sxs-lookup"><span data-stu-id="8483a-107">The proxy packages the parameters into a message buffer and passes the buffer onto the channel, which handles the transport between processes.</span></span> <span data-ttu-id="8483a-108">Proxy 會實作為匯總或複合的物件。</span><span class="sxs-lookup"><span data-stu-id="8483a-108">The proxy is implemented as an aggregate, or composite, object.</span></span> <span data-ttu-id="8483a-109">它包含系統提供的管理員元件，稱為 proxy 管理員以及一或多個介面特定的元件，稱為 interface proxy。</span><span class="sxs-lookup"><span data-stu-id="8483a-109">It contains a system-provided, manager piece called the proxy manager and one or more interface-specific components called interface proxies.</span></span> <span data-ttu-id="8483a-110">介面 proxy 的數目等於已公開給該特定用戶端的物件介面數目。</span><span class="sxs-lookup"><span data-stu-id="8483a-110">The number of interface proxies equals the number of object interfaces that have been exposed to that particular client.</span></span> <span data-ttu-id="8483a-111">用戶端若要遵守元件物件模型，proxy 就會顯示為真正的物件。</span><span class="sxs-lookup"><span data-stu-id="8483a-111">To the client complying with the component object model, the proxy appears to be the real object.</span></span>

> [!Note]  
> <span data-ttu-id="8483a-112">使用自訂封送處理時，您可以類似的方式執行 proxy，也可以直接與物件進行通訊，而不需要使用存根。</span><span class="sxs-lookup"><span data-stu-id="8483a-112">With custom marshaling, the proxy can be implemented similarly or it can communicate directly with the object without using a stub.</span></span>

 

<span data-ttu-id="8483a-113">每個介面 proxy 都是元件物件，可針對其中一個物件的介面來執行封送處理常式代碼。</span><span class="sxs-lookup"><span data-stu-id="8483a-113">Each interface proxy is a component object that implements the marshaling code for one of the object's interfaces.</span></span> <span data-ttu-id="8483a-114">Proxy 代表提供封送處理常式代碼的物件。</span><span class="sxs-lookup"><span data-stu-id="8483a-114">The proxy represents the object for which it provides marshaling code.</span></span> <span data-ttu-id="8483a-115">每個 proxy 也會實 [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) 介面。</span><span class="sxs-lookup"><span data-stu-id="8483a-115">Each proxy also implements the [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) interface.</span></span> <span data-ttu-id="8483a-116">雖然 proxy 表示的物件介面是公用的，但 **IRpcProxyBuffer** 實作為私用，並且在 proxy 內部使用。</span><span class="sxs-lookup"><span data-stu-id="8483a-116">Although the object interface represented by the proxy is public, the **IRpcProxyBuffer** implementation is private and is used internally within the proxy.</span></span> <span data-ttu-id="8483a-117">Proxy 管理員會持續追蹤介面 proxy，也會包含針對匯總控制 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面的公用執行。</span><span class="sxs-lookup"><span data-stu-id="8483a-117">The proxy manager keeps track of the interface proxies and also contains the public implementation of the controlling [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface for the aggregate.</span></span> <span data-ttu-id="8483a-118">每個介面 proxy 都可以存在於不同的 DLL 中，當它所支援的介面具體化至用戶端時，就會載入該 DLL。</span><span class="sxs-lookup"><span data-stu-id="8483a-118">Each interface proxy can exist in a separate DLL that is loaded when the interface it supports is materialized to the client.</span></span>

## <a name="structure-of-the-proxy"></a><span data-ttu-id="8483a-119">Proxy 的結構</span><span class="sxs-lookup"><span data-stu-id="8483a-119">Structure of the Proxy</span></span>

<span data-ttu-id="8483a-120">下圖顯示的 proxy 結構支援屬於兩個介面的標準封送處理參數： IA1 和 IA2。</span><span class="sxs-lookup"><span data-stu-id="8483a-120">The following diagram shows the structure of a proxy that supports the standard marshaling of parameters belonging to two interfaces: IA1 and IA2.</span></span> <span data-ttu-id="8483a-121">每個介面 proxy 都會針對匯總片段之間的內部通訊來執行 [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) 。</span><span class="sxs-lookup"><span data-stu-id="8483a-121">Each interface proxy implements [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer) for internal communication between the aggregate pieces.</span></span> <span data-ttu-id="8483a-122">當 proxy 準備將其封送處理的參數傳遞至整個進程界限時，它會呼叫 [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) 介面中的方法，該介面是由通道所執行。</span><span class="sxs-lookup"><span data-stu-id="8483a-122">When the proxy is ready to pass its marshaled parameters across the process boundary, it calls methods in the [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) interface, which is implemented by the channel.</span></span> <span data-ttu-id="8483a-123">通道接著會將呼叫轉送至 RPC 執行時間程式庫，讓它可以在物件中到達其目的地。</span><span class="sxs-lookup"><span data-stu-id="8483a-123">The channel in turn forwards the call to the RPC run-time library so that it can reach its destination in the object.</span></span>

![顯示 proxy 結構的圖表。](images/4432d8d3-dfab-4635-90f8-408aecf70134.png)

## <a name="related-topics"></a><span data-ttu-id="8483a-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="8483a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8483a-126">通道</span><span class="sxs-lookup"><span data-stu-id="8483a-126">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="8483a-127">物件間通訊</span><span class="sxs-lookup"><span data-stu-id="8483a-127">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="8483a-128">封送處理詳細資料</span><span class="sxs-lookup"><span data-stu-id="8483a-128">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="8483a-129">Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="8483a-129">Microsoft RPC</span></span>](microsoft-rpc.md)
</dt> <dt>

[<span data-ttu-id="8483a-130">存根</span><span class="sxs-lookup"><span data-stu-id="8483a-130">Stub</span></span>](stub.md)
</dt> </dl>

 

 