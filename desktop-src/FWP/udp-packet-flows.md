---
title: UDP 封包流程
description: 在典型的 UDP 會話期間，會在 Windows 篩選平台 (WFP) 篩選引擎層級的順序。
ms.assetid: ab618c1f-3e7c-4f4b-b4ff-9e396d3258d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790de49e971d5506c1732b9c4d30b88643c7af0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301532"
---
# <a name="udp-packet-flows"></a><span data-ttu-id="4520f-103">UDP 封包流程</span><span class="sxs-lookup"><span data-stu-id="4520f-103">UDP Packet Flows</span></span>

<span data-ttu-id="4520f-104">本節說明在一般的 UDP 會話期間，Windows 篩選平台 (WFP) 篩選引擎層級的順序。</span><span class="sxs-lookup"><span data-stu-id="4520f-104">This section describes the order in which the layers of the Windows Filtering Platform (WFP) filter engine are traversed during a typical UDP session.</span></span>

> [!Note]  
> <span data-ttu-id="4520f-105">IPv6 的 UDP 封包流程遵循與 IPv4 相同的模式。</span><span class="sxs-lookup"><span data-stu-id="4520f-105">UDP packet flows for IPv6 follow the same pattern as for IPv4.</span></span>

 

> [!Note]  
> <span data-ttu-id="4520f-106">所有的非 TCP 封包流程都會遵循與 UDP 封包流程相同的模式。</span><span class="sxs-lookup"><span data-stu-id="4520f-106">All non-TCP packet flows follow the same pattern as UDP packet flows.</span></span>

 

## <a name="udp-connection-establishment"></a><span data-ttu-id="4520f-107">建立 UDP 連接</span><span class="sxs-lookup"><span data-stu-id="4520f-107">UDP Connection Establishment</span></span>

<dl> <span data-ttu-id="4520f-108">伺服器 (接收者) 執行被動開啟</span><span class="sxs-lookup"><span data-stu-id="4520f-108">Server (receiver) performs Passive Open</span></span>

-   <span data-ttu-id="4520f-109">系結： FWPM LAYER ALE 系結重新 \_ \_ \_ \_ 導向 \_ V4 (僅限 windows 7/Windows Server 2008 R2) </span><span class="sxs-lookup"><span data-stu-id="4520f-109">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="4520f-110">bind： FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-110">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>

  
<span data-ttu-id="4520f-111">用戶端 (傳送者) 執行 Active Open</span><span class="sxs-lookup"><span data-stu-id="4520f-111">Client (sender) performs Active Open</span></span>

-   <span data-ttu-id="4520f-112">系結： FWPM LAYER ALE 系結重新 \_ \_ \_ \_ 導向 \_ V4 (僅限 windows 7/Windows Server 2008 R2) </span><span class="sxs-lookup"><span data-stu-id="4520f-112">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="4520f-113">bind： FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-113">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="4520f-114">sendto： FWPM \_ LAYER \_ ALE \_ CONNECT 重新 \_ 導向 \_ V4 (僅限 windows 7/Windows Server 2008 R2) </span><span class="sxs-lookup"><span data-stu-id="4520f-114">sendto: FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="4520f-115">sendto： FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-115">sendto: FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V4</span></span>
-   <span data-ttu-id="4520f-116">FWPM \_ LAYER \_ ALE \_ FLOW 已 \_ 建立 \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-116">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="4520f-117">data： FWPM \_ LAYER \_ \_ 資料包資料 \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-117">data: FWPM\_LAYER\_DATAGRAM\_DATA\_V4</span></span>
-   <span data-ttu-id="4520f-118">UDP 訊息： FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-118">UDP message: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="4520f-119">IP 資料包： FWPM \_ LAYER \_ 輸出 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-119">IP datagrams: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="4520f-120">伺服器</span><span class="sxs-lookup"><span data-stu-id="4520f-120">Server</span></span>

-   <span data-ttu-id="4520f-121">IP 資料包： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-121">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="4520f-122">UDP 訊息： FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-122">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="4520f-123">UDP 訊息： FWPM \_ 層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-123">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="4520f-124">FWPM \_ LAYER \_ ALE \_ FLOW 已 \_ 建立 \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-124">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="4520f-125">data： FWPM \_ LAYER \_ \_ 資料包資料 \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-125">data: FWPM\_LAYER\_DATAGRAM\_DATA\_V4</span></span>

  
</dl>

## <a name="udp-message-received-with-no-one-listening-on-the-port-or-protocol"></a><span data-ttu-id="4520f-126">收到的 UDP 訊息沒有接聽埠或通訊協定</span><span class="sxs-lookup"><span data-stu-id="4520f-126">UDP Message Received with No One Listening on the Port or Protocol</span></span>

<span data-ttu-id="4520f-127">伺服器 (接收者) </span><span class="sxs-lookup"><span data-stu-id="4520f-127">Server (receiver)</span></span>

-   <span data-ttu-id="4520f-128">IP 資料包： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-128">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="4520f-129">IP 資料包： FWPM \_ 層 \_ 輸入 \_ IPPACKET \_ V4 \_ 捨棄</span><span class="sxs-lookup"><span data-stu-id="4520f-129">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4\_DISCARD</span></span>
-   <span data-ttu-id="4520f-130">無法連線到 ICMP 目的地： FWPM \_ 層 \_ 輸出 \_ ICMP \_ 錯誤 \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-130">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V4</span></span>
-   <span data-ttu-id="4520f-131">無法連線到 ICMP 目的地： FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-131">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="4520f-132">無法連線到 ICMP 目的地： FWPM \_ 圖層 \_ 輸出 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-132">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

> [!Note]  
> <span data-ttu-id="4520f-133">具有特定錯誤狀況的 IPPACKET 捨棄時，不會指出 UDP 與沒有端點。</span><span class="sxs-lookup"><span data-stu-id="4520f-133">UDP with no endpoint is indicated at IPPACKET discard with a specific error condition.</span></span> <span data-ttu-id="4520f-134">在 IPPACKET 捨棄時封鎖此封包，使堆疊不會將對應的事件傳送 (ICMP 錯誤) 。</span><span class="sxs-lookup"><span data-stu-id="4520f-134">Block this packet at IPPACKET discard to cause the stack not to send the corresponding event (ICMP error).</span></span>

 

## <a name="successful-reauthorization-of-a-udp-packet"></a><span data-ttu-id="4520f-135">成功重新授權 UDP 封包</span><span class="sxs-lookup"><span data-stu-id="4520f-135">Successful Reauthorization of a UDP Packet</span></span>

<span data-ttu-id="4520f-136">伺服器 (接收者) </span><span class="sxs-lookup"><span data-stu-id="4520f-136">Server (receiver)</span></span>

-   <span data-ttu-id="4520f-137">IP 資料包： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-137">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="4520f-138">UDP 訊息： FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-138">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="4520f-139">UDP 訊息： FWPM \_ 層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-139">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="4520f-140">UDP 訊息： FWPM \_ 層 \_ \_ 資料包資料 \_ V4 (輸入) </span><span class="sxs-lookup"><span data-stu-id="4520f-140">UDP message: FWPM\_LAYER\_DATAGRAM\_DATA\_V4(INBOUND)</span></span>

## <a name="failed-reauthorization-of-a-udp-packet"></a><span data-ttu-id="4520f-141">UDP 封包的重新授權失敗</span><span class="sxs-lookup"><span data-stu-id="4520f-141">Failed Reauthorization of a UDP Packet</span></span>

<span data-ttu-id="4520f-142">伺服器 (接收者) </span><span class="sxs-lookup"><span data-stu-id="4520f-142">Server (receiver)</span></span>

-   <span data-ttu-id="4520f-143">IP 資料包： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-143">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="4520f-144">UDP 訊息： FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-144">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="4520f-145">UDP 訊息： FWPM \_ 層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V4</span><span class="sxs-lookup"><span data-stu-id="4520f-145">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="4520f-146">UDP 訊息： FWPM \_ 層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V4 \_ 捨棄</span><span class="sxs-lookup"><span data-stu-id="4520f-146">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4\_DISCARD</span></span>

## <a name="udp-connection-termination"></a><span data-ttu-id="4520f-147">UDP 連接終止</span><span class="sxs-lookup"><span data-stu-id="4520f-147">UDP Connection Termination</span></span>

<span data-ttu-id="4520f-148">任何 WFP 層都不會指出 UDP 連接終止。</span><span class="sxs-lookup"><span data-stu-id="4520f-148">UDP connection termination is not indicated at any WFP layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4520f-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="4520f-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4520f-150">ALE 重新授權</span><span class="sxs-lookup"><span data-stu-id="4520f-150">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="4520f-151">**篩選層識別碼**</span><span class="sxs-lookup"><span data-stu-id="4520f-151">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




