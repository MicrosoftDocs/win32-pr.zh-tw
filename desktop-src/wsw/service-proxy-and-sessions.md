---
title: 服務 Proxy 和會話
description: 服務 proxy 具有會話和非會話型通道系結的特殊行為。
ms.assetid: 6dc9de95-b97c-4acc-9d45-d5e6ebb6bd77
keywords:
- 適用于 Windows 的服務 Proxy 和會話 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8477a8cd03579e1d8cbfe4509f89890af8482
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104024347"
---
# <a name="service-proxy-and-sessions"></a><span data-ttu-id="4de63-106">服務 Proxy 和會話</span><span class="sxs-lookup"><span data-stu-id="4de63-106">Service Proxy and Sessions</span></span>

<span data-ttu-id="4de63-107">[服務 proxy](service-proxy.md)具有會話和非會話型通道系結的特殊行為。</span><span class="sxs-lookup"><span data-stu-id="4de63-107">The [service proxy](service-proxy.md) has special behaviors for session and non-session-based channel bindings.</span></span> <span data-ttu-id="4de63-108">如果基礎通道系結是以會話為基礎，服務 proxy 就會提供以會話為基礎的語法。</span><span class="sxs-lookup"><span data-stu-id="4de63-108">The service proxy provides session based semantics if the underlying channel binding is session based.</span></span> <span data-ttu-id="4de63-109">在此情況下，會使用單一通道來服務呼叫。</span><span class="sxs-lookup"><span data-stu-id="4de63-109">In this case a single channel is used to service calls.</span></span> <span data-ttu-id="4de63-110">但是，如果通道系結不是以會話為基礎，服務 proxy 就會為每個呼叫建立個別的通道。</span><span class="sxs-lookup"><span data-stu-id="4de63-110">However, if the channel binding is not session based, the service proxy creates a separate channel for each call.</span></span> <span data-ttu-id="4de63-111">不過請注意，非會話型的通道是集區，而且可能會重複使用。</span><span class="sxs-lookup"><span data-stu-id="4de63-111">Note, though, that non-session-based channels are pooled and maybe reused.</span></span> <span data-ttu-id="4de63-112">在重複使用通道的情況下，如果基礎通道未發生錯誤或通道上的呼叫導致服務 proxy 對通道造成錯誤，服務 proxy 會讓通道保持開啟。</span><span class="sxs-lookup"><span data-stu-id="4de63-112">In reusing a channel, the service proxy keeps the channel open if the underlying channel has not faulted or the call on a channel has resulted in the service proxy's faulting the channel.</span></span> <span data-ttu-id="4de63-113">請注意，</span><span class="sxs-lookup"><span data-stu-id="4de63-113">Note that.</span></span> <span data-ttu-id="4de63-114">除非發生錯誤，否則一旦開啟通道，只要服務 proxy 已開啟，就會保持開啟狀態，而且只有在關閉服務 proxy 時，才會關閉。</span><span class="sxs-lookup"><span data-stu-id="4de63-114">except in the event of a fault, once a channel is opened it is kept open as long as the service proxy is open and is closed only when the service proxy is closed.</span></span>


<span data-ttu-id="4de63-115">如果通道系結是以會話為基礎，而且如果基礎通道發生錯誤，服務 proxy 狀態機器將會轉換為「 [**WS \_ 服務 \_ proxy」 \_ 狀態 \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) 的「錯誤」狀態。</span><span class="sxs-lookup"><span data-stu-id="4de63-115">If the channel binding is session based and if the underlying channel faults, the service proxy state machine will transition into the [**WS\_SERVICE\_PROXY\_STATE\_FAULTED**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) state.</span></span> <span data-ttu-id="4de63-116">在非會話型通道系結的情況下，基礎通道中的錯誤不會導致 proxy 轉換成 **WS \_ 服務 \_ proxy \_ 狀態 \_** 錯誤狀態。</span><span class="sxs-lookup"><span data-stu-id="4de63-116">In the case of non-session based channel binding, a fault in the underlying channel does not cause the proxy to transition into **WS\_SERVICE\_PROXY\_STATE\_FAULTED** state.</span></span>

<span data-ttu-id="4de63-117">如需服務 proxy 及其狀態的相關詳細資訊，請參閱 [服務 proxy](service-proxy.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="4de63-117">For more information on the service proxy and its relation to state, see the [Service Proxy](service-proxy.md) topic.</span></span> <span data-ttu-id="4de63-118">如需不同通道系結的範例，請參閱下列範例：</span><span class="sxs-lookup"><span data-stu-id="4de63-118">For examples of different channel bindings see the following examples:</span></span>

-   <span data-ttu-id="4de63-119">非會話通道系結， [HttpCalculatorClientExample](httpcalculatorclientexample.md)</span><span class="sxs-lookup"><span data-stu-id="4de63-119">non-session channel binding, [HttpCalculatorClientExample](httpcalculatorclientexample.md)</span></span>
-   <span data-ttu-id="4de63-120">以會話為基礎的通道系結， [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)</span><span class="sxs-lookup"><span data-stu-id="4de63-120">session-based channel binding, [SessionfullCalculatorClientExample](sessionfullcalculatorclientexample.md)</span></span>

 

 




