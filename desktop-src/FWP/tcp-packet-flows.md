---
title: TCP 封包流程
description: 在一般的 TCP 會話期間，Windows 篩選平台 (WFP) 篩選引擎層級的順序。
ms.assetid: 75319c91-f77b-4dec-b94f-36772f1f1d53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2203ccb4b2793983bd5b1052d53c2700d3033a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932385"
---
# <a name="tcp-packet-flows"></a><span data-ttu-id="08e2b-103">TCP 封包流程</span><span class="sxs-lookup"><span data-stu-id="08e2b-103">TCP Packet Flows</span></span>

<span data-ttu-id="08e2b-104">本節說明在一般 TCP 會話期間，Windows 篩選平台 (WFP) 篩選引擎的各層的順序。</span><span class="sxs-lookup"><span data-stu-id="08e2b-104">This section describes the order in which the layers of the Windows Filtering Platform (WFP) filter engine are traversed during a typical TCP session.</span></span>

> [!Note]  
> <span data-ttu-id="08e2b-105">IPv6 的 TCP 封包流程遵循與 IPv4 相同的模式。</span><span class="sxs-lookup"><span data-stu-id="08e2b-105">TCP packet flows for IPv6 follow the same pattern as for IPv4.</span></span>

 

> [!Note]  
> <span data-ttu-id="08e2b-106">非 TCP 封包流程遵循的模式與 [UDP 封包流程](udp-packet-flows.md)相同。</span><span class="sxs-lookup"><span data-stu-id="08e2b-106">Non-TCP packet flows follow the same pattern as [UDP packet flows](udp-packet-flows.md).</span></span>

 

## <a name="tcp-connection-establishment"></a><span data-ttu-id="08e2b-107">TCP 連接建立</span><span class="sxs-lookup"><span data-stu-id="08e2b-107">TCP Connection Establishment</span></span>

<dl> <span data-ttu-id="08e2b-108">伺服器 (接收者) 執行被動開啟</span><span class="sxs-lookup"><span data-stu-id="08e2b-108">Server (receiver) performs Passive Open</span></span>

-   <span data-ttu-id="08e2b-109">系結： FWPM LAYER ALE 系結重新 \_ \_ \_ \_ 導向 \_ V4 (僅限 windows 7/Windows Server 2008 R2) </span><span class="sxs-lookup"><span data-stu-id="08e2b-109">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="08e2b-110">bind： FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-110">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="08e2b-111">接聽： FWPM \_ LAYER \_ ALE \_ AUTH \_ 接聽 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-111">listen: FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V4</span></span>

  
<span data-ttu-id="08e2b-112">用戶端 (傳送者) 執行 Active Open</span><span class="sxs-lookup"><span data-stu-id="08e2b-112">Client (sender) performs Active Open</span></span>

-   <span data-ttu-id="08e2b-113">系結： FWPM LAYER ALE 系結重新 \_ \_ \_ \_ 導向 \_ V4 (僅限 windows 7/Windows Server 2008 R2) </span><span class="sxs-lookup"><span data-stu-id="08e2b-113">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="08e2b-114">bind： FWPM \_ LAYER \_ ALE \_ 資源 \_ 指派 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-114">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="08e2b-115">connect： FWPM \_ LAYER \_ ALE \_ CONNECT 重新 \_ 導向 \_ V4 (僅限 windows 7/Windows Server 2008 R2) </span><span class="sxs-lookup"><span data-stu-id="08e2b-115">connect: FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="08e2b-116">connect： FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-116">connect: FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V4</span></span>
-   <span data-ttu-id="08e2b-117">SYN： FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-117">SYN: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="08e2b-118">SYN： FWPM \_ LAYER \_ 輸出 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-118">SYN: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="08e2b-119">伺服器</span><span class="sxs-lookup"><span data-stu-id="08e2b-119">Server</span></span>

-   <span data-ttu-id="08e2b-120">SYN： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-120">SYN: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="08e2b-121">SYN： FWPM \_ LAYER \_ 輸入 \_ 傳輸 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-121">SYN: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="08e2b-122">SYN： FWPM \_ LAYER \_ ALE \_ AUTH \_ 接收 \_ 接受 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-122">SYN: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="08e2b-123">SYN-ACK： FWPM \_ LAYER \_ 輸出 \_ 傳輸 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-123">SYN-ACK: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="08e2b-124">SYN-ACK： FWPM \_ LAYER \_ 輸出 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-124">SYN-ACK: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="08e2b-125">用戶端</span><span class="sxs-lookup"><span data-stu-id="08e2b-125">Client</span></span>

-   <span data-ttu-id="08e2b-126">SYN-ACK： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-126">SYN-ACK: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="08e2b-127">SYN-ACK： FWPM \_ LAYER \_ 輸入 \_ 傳輸 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-127">SYN-ACK: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="08e2b-128">FWPM \_ LAYER \_ ALE \_ FLOW 已 \_ 建立 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-128">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="08e2b-129">ACK： FWPM \_ LAYER \_ 輸出 \_ 傳輸 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-129">ACK: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="08e2b-130">ACK： FWPM \_ LAYER \_ 輸出 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-130">ACK: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="08e2b-131">伺服器</span><span class="sxs-lookup"><span data-stu-id="08e2b-131">Server</span></span>

-   <span data-ttu-id="08e2b-132">ACK： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-132">ACK: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="08e2b-133">ACK： FWPM \_ LAYER \_ 輸入 \_ 傳輸 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-133">ACK: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="08e2b-134">FWPM \_ LAYER \_ ALE \_ FLOW 已 \_ 建立 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-134">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="08e2b-135">接聽完成。</span><span class="sxs-lookup"><span data-stu-id="08e2b-135">Listen completes.</span></span> <span data-ttu-id="08e2b-136">伺服器可以執行接受。</span><span class="sxs-lookup"><span data-stu-id="08e2b-136">Server can perform an accept.</span></span>

  
</dl>

## <a name="tcp-syn-received-with-no-one-listening-on-the-port-or-protocol"></a><span data-ttu-id="08e2b-137">收到的 TCP SYN 未接聽埠或通訊協定</span><span class="sxs-lookup"><span data-stu-id="08e2b-137">TCP SYN Received with No One Listening on the Port or Protocol</span></span>

<span data-ttu-id="08e2b-138">伺服器 (接收者) </span><span class="sxs-lookup"><span data-stu-id="08e2b-138">Server (receiver)</span></span>

-   <span data-ttu-id="08e2b-139">SYN： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-139">SYN: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="08e2b-140">SYN： FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V4 \_ 捨棄</span><span class="sxs-lookup"><span data-stu-id="08e2b-140">SYN: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4\_DISCARD</span></span>
-   <span data-ttu-id="08e2b-141">RST： FWPM \_ LAYER \_ 輸出 \_ 傳輸 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-141">RST: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="08e2b-142">RST： FWPM \_ LAYER \_ 輸出 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-142">RST: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

> [!Note]  
> <span data-ttu-id="08e2b-143">具有特定錯誤狀況的傳輸捨棄時，不會指出 TCP SYN （不含端點）。</span><span class="sxs-lookup"><span data-stu-id="08e2b-143">TCP SYN with no endpoint is indicated at TRANSPORT discard with a specific error condition.</span></span> <span data-ttu-id="08e2b-144">在傳輸捨棄時封鎖此封包，使堆疊不會將對應的事件傳送 (RST) 。</span><span class="sxs-lookup"><span data-stu-id="08e2b-144">Block this packet at TRANSPORT discard to cause the stack not to send the corresponding event (RST).</span></span> <span data-ttu-id="08e2b-145">如需隱形模式篩選的範例，請參閱 [防止埠掃描](preventing-port-scanning.md)。</span><span class="sxs-lookup"><span data-stu-id="08e2b-145">For an example of stealth-mode filtering, see [Preventing Port Scanning](preventing-port-scanning.md).</span></span>

 

## <a name="data-transmitted-over-a-tcp-connection"></a><span data-ttu-id="08e2b-146">透過 TCP 連接傳輸的資料</span><span class="sxs-lookup"><span data-stu-id="08e2b-146">Data Transmitted Over a TCP Connection</span></span>

<dl> <span data-ttu-id="08e2b-147">用戶端 (寄件者) </span><span class="sxs-lookup"><span data-stu-id="08e2b-147">Client (sender)</span></span>

-   <span data-ttu-id="08e2b-148">傳送</span><span class="sxs-lookup"><span data-stu-id="08e2b-148">send</span></span>
-   <span data-ttu-id="08e2b-149">資料： FWPM \_ 圖層 \_ 串流 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-149">data: FWPM\_LAYER\_STREAM\_V4</span></span>
-   <span data-ttu-id="08e2b-150">TCP 區段： FWPM \_ 層 \_ 輸出 \_ 傳輸 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-150">TCP segments: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="08e2b-151">IP 資料包： FWPM \_ LAYER \_ 輸出 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-151">IP datagrams: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="08e2b-152">伺服器 (接收者) </span><span class="sxs-lookup"><span data-stu-id="08e2b-152">Server (receiver)</span></span>

-   <span data-ttu-id="08e2b-153">IP 資料包： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-153">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="08e2b-154">TCP 區段： FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-154">TCP segments: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="08e2b-155">資料： FWPM \_ 圖層 \_ 串流 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-155">data: FWPM\_LAYER\_STREAM\_V4</span></span>
-   <span data-ttu-id="08e2b-156">資料可供讀取。</span><span class="sxs-lookup"><span data-stu-id="08e2b-156">Data is available to read.</span></span>

  
</dl>

## <a name="successful-reauthorization-of-a-tcp-packet"></a><span data-ttu-id="08e2b-157">成功重新授權 TCP 封包</span><span class="sxs-lookup"><span data-stu-id="08e2b-157">Successful Reauthorization of a TCP Packet</span></span>

<span data-ttu-id="08e2b-158">伺服器 (接收者) </span><span class="sxs-lookup"><span data-stu-id="08e2b-158">Server (receiver)</span></span>

-   <span data-ttu-id="08e2b-159">IP 資料包： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-159">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="08e2b-160">TCP 區段： FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-160">TCP segment: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="08e2b-161">TCP 區段： FWPM \_ LAYER \_ ALE \_ AUTH \_ 接收 \_ 接受 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-161">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="08e2b-162">data： FWPM \_ LAYER \_ STREAM \_ V4 (輸入) </span><span class="sxs-lookup"><span data-stu-id="08e2b-162">data: FWPM\_LAYER\_STREAM\_V4(INBOUND)</span></span>

## <a name="failed-reauthorization-of-a-tcp-packet"></a><span data-ttu-id="08e2b-163">TCP 封包的重新授權失敗</span><span class="sxs-lookup"><span data-stu-id="08e2b-163">Failed Reauthorization of a TCP Packet</span></span>

<span data-ttu-id="08e2b-164">伺服器 (接收者) </span><span class="sxs-lookup"><span data-stu-id="08e2b-164">Server (receiver)</span></span>

-   <span data-ttu-id="08e2b-165">IP 資料包： FWPM \_ LAYER \_ 輸入 \_ IPPACKET \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-165">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="08e2b-166">TCP 區段： FWPM \_ 層 \_ 輸入 \_ 傳輸 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-166">TCP segment: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="08e2b-167">TCP 區段： FWPM \_ LAYER \_ ALE \_ AUTH \_ 接收 \_ 接受 \_ V4</span><span class="sxs-lookup"><span data-stu-id="08e2b-167">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="08e2b-168">TCP 區段： FWPM \_ LAYER \_ ALE \_ AUTH \_ 接收 \_ ACCEPT \_ V4 \_ 捨棄</span><span class="sxs-lookup"><span data-stu-id="08e2b-168">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4\_DISCARD</span></span>

## <a name="tcp-connection-termination"></a><span data-ttu-id="08e2b-169">TCP 連接終止</span><span class="sxs-lookup"><span data-stu-id="08e2b-169">TCP Connection Termination</span></span>

<span data-ttu-id="08e2b-170">任何 WFP 層都不會指出 TCP 連接終止。</span><span class="sxs-lookup"><span data-stu-id="08e2b-170">TCP connection termination is not indicated at any WFP layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08e2b-171">相關主題</span><span class="sxs-lookup"><span data-stu-id="08e2b-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08e2b-172">ALE 重新授權</span><span class="sxs-lookup"><span data-stu-id="08e2b-172">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="08e2b-173">**篩選層識別碼**</span><span class="sxs-lookup"><span data-stu-id="08e2b-173">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




