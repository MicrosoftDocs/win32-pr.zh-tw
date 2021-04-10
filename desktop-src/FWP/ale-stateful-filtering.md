---
title: ALE 具狀態篩選
description: 在應用層強制安裝的篩選 (Windows 篩選平台的 ALE) 層 (WFP) 執行具狀態網路篩選。
ms.assetid: d5a3fcad-d55e-4a07-af21-cb40e5e9a9ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cc1b4a5830efd0fef6dc28c88db85cd9c88cca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023473"
---
# <a name="ale-stateful-filtering"></a><span data-ttu-id="5bb77-103">ALE 具狀態篩選</span><span class="sxs-lookup"><span data-stu-id="5bb77-103">ALE Stateful Filtering</span></span>

<span data-ttu-id="5bb77-104">在應用層強制安裝的篩選 (Windows 篩選平台的 ALE) 層 (WFP) 執行具狀態網路篩選。</span><span class="sxs-lookup"><span data-stu-id="5bb77-104">Filters installed at the Application Layer Enforcement (ALE) layers of the Windows Filtering Platform (WFP) perform stateful network filtering.</span></span> <span data-ttu-id="5bb77-105">*Ale 流程* 是用來做為 ale 可設定狀態的篩選基礎。</span><span class="sxs-lookup"><span data-stu-id="5bb77-105">An *ALE flow* is used as the basis for ALE stateful filtering.</span></span>

<span data-ttu-id="5bb77-106">ALE 流程是根據來源 IP 位址、目的地 IP 位址、來源埠、目的地埠和通訊協定，將網路流量分組的方式。</span><span class="sxs-lookup"><span data-stu-id="5bb77-106">An ALE flow is a way of classifying network traffic by grouping it based on a Source IP Address, a Destination IP Address, a Source Port, a Destination Port, and a Protocol.</span></span> <span data-ttu-id="5bb77-107">ALE 流程可以是泛型，也就是一或多個描述項可能符合 (或萬用字元) 的所有專案 \* 。</span><span class="sxs-lookup"><span data-stu-id="5bb77-107">An ALE flow could be generic, that is one or more of the descriptors could be matching everything (or wildcard \*).</span></span> <span data-ttu-id="5bb77-108">例如，一般的 UDP ALE 流程將會描述為來源 IP 位址 = \* 、目的地 Ip 位址 = \* 、來源埠 = \* 、目的地埠 = \* 和通訊協定 = UDP。</span><span class="sxs-lookup"><span data-stu-id="5bb77-108">For example, a generic UDP ALE flow would be described as Source IP Address = \*, Destination IP Address = \*, Source Port = \*, Destination Port = \*, and Protocol = UDP.</span></span>

<span data-ttu-id="5bb77-109">授權連線之後 (輸入連線會在 [**FWPM \_ 層 \_ ale \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 層以及 **FWPM \_ 層 \_ ale \_ auth auth \_ CONNECT \_ v {4 \| 6}** 層) 的輸出連線，就會建立一個 ale 流程，如此一來，就會自動允許屬於相同 ale 流程的所有封包、輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="5bb77-109">Once a connection is authorized (inbound connections are authorized at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer and outbound connections at the **FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}** layer), an ALE flow is created such that, barring a policy change, all packets, inbound and outbound, that belong to the same ALE flow are permitted automatically.</span></span> <span data-ttu-id="5bb77-110">由於原則變更可能需要封鎖先前允許的連線，因此在發生原則變更時，必須 [重新授權](ale-re-authorization.md) ALE 流程。</span><span class="sxs-lookup"><span data-stu-id="5bb77-110">Because a policy change might require blocking previously allowed connections, ALE flows need to be [reauthorized](ale-re-authorization.md) when a policy change occurs.</span></span>

<span data-ttu-id="5bb77-111">ALE 具狀態篩選只會將屬於 ALE 流程的第一個封包分類，以大幅減少所需分類的數目。</span><span class="sxs-lookup"><span data-stu-id="5bb77-111">ALE stateful filtering reduces drastically the number of required classifications by classifying only the first packet that belongs to an ALE flow.</span></span> <span data-ttu-id="5bb77-112">相較之下，非具狀態的篩選需要分類流經網路的每個封包。</span><span class="sxs-lookup"><span data-stu-id="5bb77-112">By comparison, non-stateful filtering requires classification of every packet that traverse the network.</span></span>

<span data-ttu-id="5bb77-113">ALE 流程具有相關聯的方向，也就是流程第一個封包的方向。</span><span class="sxs-lookup"><span data-stu-id="5bb77-113">An ALE flow has an associated direction, which is the direction of the first packet of the flow.</span></span> <span data-ttu-id="5bb77-114">藉由允許輸入起始的連接與輸出起始的連接具有不同的原則，即可提供更有彈性的原則。</span><span class="sxs-lookup"><span data-stu-id="5bb77-114">This allows for more flexible policies, by permitting inbound initiated connections to have different policies from outbound initiated connections.</span></span>

## <a name="tcp-ale-flow"></a><span data-ttu-id="5bb77-115">TCP ALE 流程</span><span class="sxs-lookup"><span data-stu-id="5bb77-115">TCP ALE Flow</span></span>

<span data-ttu-id="5bb77-116">TCP 流量的 ALE 流程是由 TCP/IP (來源 IP 位址、目的地 IP 位址、來源埠、目的地埠和通訊協定) 的五個元組所識別。</span><span class="sxs-lookup"><span data-stu-id="5bb77-116">An ALE flow for TCP traffic is identified by the five-tuple of TCP/IP (Source IP Address, Destination IP Address, Source Port, Destination Port, and Protocol).</span></span>

<span data-ttu-id="5bb77-117">TCP ALE 流程與連線的 TCP 通訊端具有相同的存留期。</span><span class="sxs-lookup"><span data-stu-id="5bb77-117">A TCP ALE flow has the same lifetime as a connected TCP socket.</span></span> <span data-ttu-id="5bb77-118">連接的 TCP 通訊端可以是使用 [**connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) 建立的通訊端，或是 [**接受 ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) 呼叫所建立的通訊端。</span><span class="sxs-lookup"><span data-stu-id="5bb77-118">A connected TCP socket could be either a socket created using [**connect()**](/windows/desktop/api/winsock2/nf-winsock2-connect) or a socket created as a result of an [**accept()**](/windows/desktop/api/winsock2/nf-winsock2-accept) call.</span></span>

<span data-ttu-id="5bb77-119">ALE 會維護 TCP ALE 流程與 TCP 控制區塊之間的一對一關聯性， (TCB) 。</span><span class="sxs-lookup"><span data-stu-id="5bb77-119">ALE maintains a one-to-one relationship between a TCP ALE flow and a TCP Control Block (TCB).</span></span>

## <a name="udp-ale-flow"></a><span data-ttu-id="5bb77-120">UDP ALE 流程</span><span class="sxs-lookup"><span data-stu-id="5bb77-120">UDP ALE Flow</span></span>

> [!Note]  
> <span data-ttu-id="5bb77-121">非 TCP 或 ICMP 的通訊協定會視為 UDP。</span><span class="sxs-lookup"><span data-stu-id="5bb77-121">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="5bb77-122">UDP 流量的 ALE 流程是由 TCP/IP (來源 IP 位址、目的地 IP 位址、來源埠、目的地埠和通訊協定) 的五個元組所識別。</span><span class="sxs-lookup"><span data-stu-id="5bb77-122">An ALE flow for UDP traffic is identified by the five-tuple of TCP/IP (Source IP Address, Destination IP Address, Source Port, Destination Port, and Protocol).</span></span>

<span data-ttu-id="5bb77-123">UDP ALE 流程是根據 UDP 通訊端建立，它代表應用程式正在通訊的遠端對等。</span><span class="sxs-lookup"><span data-stu-id="5bb77-123">A UDP ALE flow is created based on a UDP socket and it represents the remote peer that the application is communicating with.</span></span> <span data-ttu-id="5bb77-124">遠端對等是由 (目的地 IP 位址和目的地埠) 元組所識別。</span><span class="sxs-lookup"><span data-stu-id="5bb77-124">A remote peer is identified by a (Destination IP Address and Destination Port) tuple.</span></span>

<span data-ttu-id="5bb77-125">UDP 通訊端和與其交談的遠端對等之間，有一對多關聯性。</span><span class="sxs-lookup"><span data-stu-id="5bb77-125">There is a one-to-many relationship between a UDP socket and the remote peers that it talks to.</span></span>

<span data-ttu-id="5bb77-126">當本機 UDP 通訊端關閉時，將會刪除與其相關聯的所有 ALE 流程。</span><span class="sxs-lookup"><span data-stu-id="5bb77-126">When the local UDP socket is closed, all the ALE flows associated with it will be deleted.</span></span>

<span data-ttu-id="5bb77-127">在沒有通訊端關閉的情況下，UDP 單播 ALE 流程具有 [可](ale-flow-customization.md) 設定的閒置 timeout，預設為60秒。</span><span class="sxs-lookup"><span data-stu-id="5bb77-127">In the absence of socket closures, UDP unicast ALE flows have a [configurable](ale-flow-customization.md) idle timeout that defaults to 60 seconds.</span></span> <span data-ttu-id="5bb77-128">如果在此視窗內沒有傳送或接收任何封包，則會刪除 ALE 流程。</span><span class="sxs-lookup"><span data-stu-id="5bb77-128">If no packets are sent or received within this window, the ALE flow will be deleted.</span></span> <span data-ttu-id="5bb77-129">當整個系統的 ALE 流程數目達到特定閾值時，此預設的超時時間會逐漸縮短。</span><span class="sxs-lookup"><span data-stu-id="5bb77-129">This default timeout is progressively shortened when the number of ALE flows system-wide reaches a certain threshold.</span></span>

## <a name="icmp-ale-flow"></a><span data-ttu-id="5bb77-130">ICMP ALE 流程</span><span class="sxs-lookup"><span data-stu-id="5bb77-130">ICMP ALE Flow</span></span>

<span data-ttu-id="5bb77-131">ICMP 流量的 ALE 流程是由六個元組所識別 (來源 IP 位址、目的地 IP 位址、ICMP 類型、ICMP 代碼、通訊協定和 ICMP 識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="5bb77-131">An ALE flow for ICMP traffic is identified by the six-tuple (Source IP Address, Destination IP Address, ICMP type, ICMP code, Protocol, and ICMP ID).</span></span> <span data-ttu-id="5bb77-132">ICMP 識別碼只是針對 ICMP echo/回復流量的 ALE 流程的一部分。</span><span class="sxs-lookup"><span data-stu-id="5bb77-132">The ICMP ID is part of the ALE flow only for ICMP echo/reply traffic.</span></span>

<span data-ttu-id="5bb77-133">在沒有通訊端關閉的情況下，ICMP 單播 ALE 流程具有 [可](ale-flow-customization.md) 設定的閒置 timeout，預設為60秒。</span><span class="sxs-lookup"><span data-stu-id="5bb77-133">In the absence of socket closures, ICMP unicast ALE flows have a [configurable](ale-flow-customization.md) idle timeout that defaults to 60 seconds.</span></span> <span data-ttu-id="5bb77-134">如果在此視窗內沒有傳送或接收任何封包，則會刪除 ALE 流程。</span><span class="sxs-lookup"><span data-stu-id="5bb77-134">If no packets are sent or received within this window, the ALE flow will be deleted.</span></span> <span data-ttu-id="5bb77-135">當整個系統的 ALE 流程數目達到特定閾值時，此預設的超時時間會逐漸縮短。</span><span class="sxs-lookup"><span data-stu-id="5bb77-135">This default timeout is progressively shortened when the number of ALE flows system-wide reaches a certain threshold.</span></span>

<span data-ttu-id="5bb77-136">只有 ICMP 非錯誤訊息會指出至 ALE 層。</span><span class="sxs-lookup"><span data-stu-id="5bb77-136">Only ICMP non-error messages are indicated to ALE layers.</span></span> <span data-ttu-id="5bb77-137">Icmp 錯誤訊息可以在 ICMP 錯誤層級進行檢查 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5bb77-137">ICMP error messages can be inspected at ICMP\_ERROR layers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5bb77-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="5bb77-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bb77-139">應用層強制 (ALE) </span><span class="sxs-lookup"><span data-stu-id="5bb77-139">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="5bb77-140">ALE 層</span><span class="sxs-lookup"><span data-stu-id="5bb77-140">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="5bb77-141">ALE 多播/廣播流量</span><span class="sxs-lookup"><span data-stu-id="5bb77-141">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="5bb77-142">ALE 重新授權</span><span class="sxs-lookup"><span data-stu-id="5bb77-142">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="5bb77-143">ALE 流程自訂</span><span class="sxs-lookup"><span data-stu-id="5bb77-143">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> <dt>

[<span data-ttu-id="5bb77-144">TCP 封包流程</span><span class="sxs-lookup"><span data-stu-id="5bb77-144">TCP Packet Flows</span></span>](tcp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="5bb77-145">UDP 封包流程</span><span class="sxs-lookup"><span data-stu-id="5bb77-145">UDP Packet Flows</span></span>](udp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="5bb77-146">Winsock 函數</span><span class="sxs-lookup"><span data-stu-id="5bb77-146">Winsock Functions</span></span>](/windows/desktop/WinSock/winsock-functions)
</dt> </dl>

 

 