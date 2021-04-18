---
description: 有關媒體封包大小的主題中所討論的媒體封包大小問題，會影響不同的 PF \_ IPX 通訊協定。
ms.assetid: 7f0643b8-6bb2-4dbb-b306-d9b2e0d0e03c
title: 封包大小如何影響通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c778ee6c75cd558d19cdf1cbb76052065e03c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318379"
---
# <a name="how-packet-size-affects-protocols"></a><span data-ttu-id="dbc23-103">封包大小如何影響通訊協定</span><span class="sxs-lookup"><span data-stu-id="dbc23-103">How Packet Size Affects Protocols</span></span>

<span data-ttu-id="dbc23-104">[有關媒體封包大小](about-media-packet-size-2.md)的主題中所討論的媒體封包大小問題，會影響不同的 PF \_ IPX 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="dbc23-104">Media packet size issues discussed in the topic, [About Media Packet Size](about-media-packet-size-2.md), affect the various PF\_IPX protocols differently.</span></span> <span data-ttu-id="dbc23-105">處理各種路由器和媒體大小限制的常見策略，是在遠端工作站的網路編號符合本機工作站時使用完整媒體大小，否則會改回最小的封包大小。</span><span class="sxs-lookup"><span data-stu-id="dbc23-105">A common strategy for handling various router and media size constraints is to use the full media size when the remote station's network number matches the local station, and fall back to the minimum packet size otherwise.</span></span>

## <a name="parameters"></a><span data-ttu-id="dbc23-106">參數</span><span class="sxs-lookup"><span data-stu-id="dbc23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbc23-107"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>NSPROTO \_ IPX</span><span class="sxs-lookup"><span data-stu-id="dbc23-107"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>NSPROTO\_IPX</span></span>
</dt> <dd>

<span data-ttu-id="dbc23-108">提供資料包服務;每個資料包都必須位於封包大小上限內。</span><span class="sxs-lookup"><span data-stu-id="dbc23-108">Provides a datagram service; each datagram must reside within the maximum packet size.</span></span> <span data-ttu-id="dbc23-109">Winsock 將最大的資料包封包大小設定為本機媒體封包大小，減去 IPX 標頭。</span><span class="sxs-lookup"><span data-stu-id="dbc23-109">Winsock sets the maximum datagram packet size to the local media packet size minus the IPX header.</span></span> <span data-ttu-id="dbc23-110">不過請記住，如果封包是路由傳送的，則可能會達到路由器限制（路由）。</span><span class="sxs-lookup"><span data-stu-id="dbc23-110">Keep in mind, however, that if the packet is routed, it may hit router restrictions en route.</span></span> <span data-ttu-id="dbc23-111">請確定您的應用程式可以切換回546位元組的資料包。</span><span class="sxs-lookup"><span data-stu-id="dbc23-111">Make sure your application can fall back to 546-byte datagrams.</span></span>

</dd> <dt>

<span data-ttu-id="dbc23-112"><span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO \_ SPX</span><span class="sxs-lookup"><span data-stu-id="dbc23-112"><span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO\_SPX</span></span>
</dt> <dd>

<span data-ttu-id="dbc23-113">提供資料流程和序列封包服務。</span><span class="sxs-lookup"><span data-stu-id="dbc23-113">Provides stream and sequenced-packet services.</span></span> <span data-ttu-id="dbc23-114">Winsock IPX/SPX 可讓資料流程和訊息跨越多個封包，因此封包大小不會限制 [**傳送**](/windows/desktop/api/Winsock2/nf-winsock2-send) 和 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv)所處理的資料量。</span><span class="sxs-lookup"><span data-stu-id="dbc23-114">Winsock IPX/SPX lets data streams and messages span multiple packets, so packet size does not limit the amount of data handled by [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv).</span></span> <span data-ttu-id="dbc23-115">不過，基礎媒體大小必須正確設定，否則第一個大型封包將會無法傳遞，且連接將會重設。</span><span class="sxs-lookup"><span data-stu-id="dbc23-115">However, the underlying media size must be set correctly or the first large packet will be undeliverable and the connection will reset.</span></span> <span data-ttu-id="dbc23-116">如果目標站在區域網路上，Winsock 會將其封包大小設定為媒體封包大小。</span><span class="sxs-lookup"><span data-stu-id="dbc23-116">If the target station is on the local network, Winsock sets its packet size to the media packet size.</span></span> <span data-ttu-id="dbc23-117">否則，它會預設為512個位元組。</span><span class="sxs-lookup"><span data-stu-id="dbc23-117">Otherwise, it defaults to 512 bytes.</span></span> <span data-ttu-id="dbc23-118">您可以在 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) 或 [**接受**](/windows/desktop/api/Winsock2/nf-winsock2-accept) [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)之後立即變更此大小。</span><span class="sxs-lookup"><span data-stu-id="dbc23-118">This size can be changed immediately after [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) or [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) through [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span></span>

</dd> <dt>

<span data-ttu-id="dbc23-119"><span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO \_ SPXII</span><span class="sxs-lookup"><span data-stu-id="dbc23-119"><span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO\_SPXII</span></span>
</dt> <dd>

<span data-ttu-id="dbc23-120">SPXII 具有大型的網際網路封包協商功能，可維持最適合的封包大小，而不需要程式設計人員介入。</span><span class="sxs-lookup"><span data-stu-id="dbc23-120">SPXII features large Internet packet negotiation to maintain a best-fit size for packets and does not require programmer intervention.</span></span> <span data-ttu-id="dbc23-121">但是，如果遠端工作站不支援 SPXII 並協商至標準的 SPX，NSPROTO 的 \_ spx 規則就會生效。</span><span class="sxs-lookup"><span data-stu-id="dbc23-121">However, if the remote station does not support SPXII and negotiates down to standard SPX, the NSPROTO\_SPX rules are in effect.</span></span>



| <span data-ttu-id="dbc23-122">通訊協定</span><span class="sxs-lookup"><span data-stu-id="dbc23-122">Protocol</span></span>     | <span data-ttu-id="dbc23-123">媒體</span><span class="sxs-lookup"><span data-stu-id="dbc23-123">Media</span></span>      | <span data-ttu-id="dbc23-124">類型</span><span class="sxs-lookup"><span data-stu-id="dbc23-124">Type</span></span>        | <span data-ttu-id="dbc23-125">資料封包大小</span><span class="sxs-lookup"><span data-stu-id="dbc23-125">Data packet size</span></span> |
|--------------|------------|-------------|------------------|
| <span data-ttu-id="dbc23-126">NSPROTO \_ IPX</span><span class="sxs-lookup"><span data-stu-id="dbc23-126">NSPROTO\_IPX</span></span> | <span data-ttu-id="dbc23-127">乙太網路</span><span class="sxs-lookup"><span data-stu-id="dbc23-127">Ethernet</span></span>   | <span data-ttu-id="dbc23-128">Ethernet II</span><span class="sxs-lookup"><span data-stu-id="dbc23-128">Ethernet II</span></span> |                  |
|              |            | <span data-ttu-id="dbc23-129">802.3</span><span class="sxs-lookup"><span data-stu-id="dbc23-129">802.3</span></span>       |                  |
|              |            | <span data-ttu-id="dbc23-130">802.2</span><span class="sxs-lookup"><span data-stu-id="dbc23-130">802.2</span></span>       | <span data-ttu-id="dbc23-131">1466</span><span class="sxs-lookup"><span data-stu-id="dbc23-131">1466</span></span>             |
|              |            | <span data-ttu-id="dbc23-132">單元</span><span class="sxs-lookup"><span data-stu-id="dbc23-132">SNAP</span></span>        |                  |
|              | <span data-ttu-id="dbc23-133">Token Ring</span><span class="sxs-lookup"><span data-stu-id="dbc23-133">Token Ring</span></span> | <span data-ttu-id="dbc23-134">4 mb</span><span class="sxs-lookup"><span data-stu-id="dbc23-134">4 megabit</span></span>   |                  |
|              |            | <span data-ttu-id="dbc23-135">16 mb</span><span class="sxs-lookup"><span data-stu-id="dbc23-135">16 megabit</span></span>  |                  |
| <span data-ttu-id="dbc23-136">NSPROTO \_ SPX</span><span class="sxs-lookup"><span data-stu-id="dbc23-136">NSPROTO\_SPX</span></span> | <span data-ttu-id="dbc23-137">乙太網路</span><span class="sxs-lookup"><span data-stu-id="dbc23-137">Ethernet</span></span>   | <span data-ttu-id="dbc23-138">Ethernet II</span><span class="sxs-lookup"><span data-stu-id="dbc23-138">Ethernet II</span></span> |                  |
|              |            | <span data-ttu-id="dbc23-139">802.3</span><span class="sxs-lookup"><span data-stu-id="dbc23-139">802.3</span></span>       |                  |
|              |            | <span data-ttu-id="dbc23-140">802.2</span><span class="sxs-lookup"><span data-stu-id="dbc23-140">802.2</span></span>       | <span data-ttu-id="dbc23-141">1454</span><span class="sxs-lookup"><span data-stu-id="dbc23-141">1454</span></span>             |
|              |            | <span data-ttu-id="dbc23-142">單元</span><span class="sxs-lookup"><span data-stu-id="dbc23-142">SNAP</span></span>        |                  |
|              | <span data-ttu-id="dbc23-143">Token Ring</span><span class="sxs-lookup"><span data-stu-id="dbc23-143">Token Ring</span></span> | <span data-ttu-id="dbc23-144">4 mb</span><span class="sxs-lookup"><span data-stu-id="dbc23-144">4 megabit</span></span>   |                  |
|              |            | <span data-ttu-id="dbc23-145">16 mb</span><span class="sxs-lookup"><span data-stu-id="dbc23-145">16 megabit</span></span>  |                  |



 

</dd> </dl>

 

 



