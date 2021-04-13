---
title: ALE 層
description: 應用層強制 (ALE) 是由數個篩選層和許多相符的捨棄層所組成。
ms.assetid: 3ac71787-2350-4a60-b0bf-b00b52d30b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a96e3b2ae5092bf8cca014eb3603eea5efe8f71
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314722"
---
# <a name="ale-layers"></a><span data-ttu-id="56dd0-103">ALE 層</span><span class="sxs-lookup"><span data-stu-id="56dd0-103">ALE Layers</span></span>

<span data-ttu-id="56dd0-104">應用層強制 (ALE) 是由數個篩選層和許多相符的捨棄層所組成。</span><span class="sxs-lookup"><span data-stu-id="56dd0-104">The Application Layer Enforcement (ALE) consists of several filtering layers and many matching discard layers.</span></span> <span data-ttu-id="56dd0-105">所有的 Windows 篩選平台 (WFP) 篩選引擎層級（包括 ALE）都會在 [**篩選層識別碼**](management-filtering-layer-identifiers-.md)中描述。</span><span class="sxs-lookup"><span data-stu-id="56dd0-105">All the Windows Filtering Platform (WFP) filtering engine layers, including ALE, are described in [**Filtering Layer Identifiers**](management-filtering-layer-identifiers-.md).</span></span> <span data-ttu-id="56dd0-106">本主題包含屬於 ALE 之篩選層的詳細描述。</span><span class="sxs-lookup"><span data-stu-id="56dd0-106">This topic contains a more detailed description of the filtering layers that are part of ALE.</span></span>

## <a name="resource_assignment"></a><span data-ttu-id="56dd0-107">資源 \_ 指派</span><span class="sxs-lookup"><span data-stu-id="56dd0-107">RESOURCE\_ASSIGNMENT</span></span>

<span data-ttu-id="56dd0-108">針對網路系結作業（明確或隱含），會比對 [**FWPM \_ layer \_ ALE \_ 資源 \_ 指派 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 層的篩選。</span><span class="sxs-lookup"><span data-stu-id="56dd0-108">A filter at the [**FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for network bind operations, explicit or implicit.</span></span>

<span data-ttu-id="56dd0-109">如果此層級的篩選準則符合以授權原始通訊端建立，則會設定 [ [**.Fwp \_ 條件 \_ 旗標 \_ 為 \_ 原始 \_ 端點**](filtering-condition-flags-.md) 旗標]。</span><span class="sxs-lookup"><span data-stu-id="56dd0-109">If a filter at this layer is matched to authorize raw socket creation, the [**FWP\_CONDITION\_FLAG\_IS\_RAW\_ENDPOINT**](filtering-condition-flags-.md) flag will be set.</span></span>

<span data-ttu-id="56dd0-110">如果此層級的篩選準則符合以授權混合模式接收，則 [ [**.Fwp \_ 條件 \_ ALE \_ 混合 \_ 模式]**](filtering-condition-identifiers-.md) 欄位將設定為 [SIO RCVALL] \_ 。</span><span class="sxs-lookup"><span data-stu-id="56dd0-110">If a filter at this layer is matched to authorize promiscuous mode receiving, the [**FWP\_CONDITION\_ALE\_PROMISCUOUS\_MODE**](filtering-condition-identifiers-.md) field will be set to SIO\_RCVALL.</span></span> <span data-ttu-id="56dd0-111">如需 SIO RCVALL 的說明 \_ ，請參閱 [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)。</span><span class="sxs-lookup"><span data-stu-id="56dd0-111">For a description of SIO\_RCVALL, see [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).</span></span>

> [!Note]  
> <span data-ttu-id="56dd0-112">這是唯一可篩選混合模式的層級。</span><span class="sxs-lookup"><span data-stu-id="56dd0-112">This is the only layer where promiscuous mode can be filtered.</span></span>

 

<span data-ttu-id="56dd0-113">如果系結 **()** 期間未指定埠，也就是埠設定為 0 (零) ，則 tcp/ip 堆疊會從動態埠範圍選取埠 (19152 – 65535) 。</span><span class="sxs-lookup"><span data-stu-id="56dd0-113">If no port is specified during **bind()**, that is, port is set to 0 (zero), then the TCP/IP stack will select a port from the dynamic port range (19152–65535).</span></span> <span data-ttu-id="56dd0-114">選取的埠會在此層級進行分類，而 [ [**.Fwp \_ 條件] 旗標為 [ \_ \_ \_ 萬用字元 \_**](filtering-condition-flags-.md) 系結旗標]。</span><span class="sxs-lookup"><span data-stu-id="56dd0-114">The selected port will be classified at this layer along with the [**FWP\_CONDITION\_FLAG\_IS\_WILDCARD\_BIND**](filtering-condition-flags-.md) flag.</span></span>

<span data-ttu-id="56dd0-115">如果未在 [**bind ()**](/windows/desktop/api/winsock/nf-winsock-bind) 呼叫中指定本機位址，則 [本機位址] 欄位會設定為 [ [**.fwp \_ 空白**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)]。</span><span class="sxs-lookup"><span data-stu-id="56dd0-115">If the local address is not specified in the [**bind()**](/windows/desktop/api/winsock/nf-winsock-bind) call, the local address field is set to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span>

## <a name="auth_listen"></a><span data-ttu-id="56dd0-116">驗證 \_ 接聽</span><span class="sxs-lookup"><span data-stu-id="56dd0-116">AUTH\_LISTEN</span></span>

<span data-ttu-id="56dd0-117">[**FWPM \_ layer \_ ALE \_ AUTH AUTH \_ 接聽 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md)層的篩選器會與 TCP [**接聽 ()**](/windows/desktop/api/winsock2/nf-winsock2-listen)呼叫進行比對。</span><span class="sxs-lookup"><span data-stu-id="56dd0-117">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**listen()**](/windows/desktop/api/winsock2/nf-winsock2-listen) calls.</span></span>

## <a name="auth_recv_accept"></a><span data-ttu-id="56dd0-118">驗證 \_ 接收 \_ 接受</span><span class="sxs-lookup"><span data-stu-id="56dd0-118">AUTH\_RECV\_ACCEPT</span></span>

<span data-ttu-id="56dd0-119">[**FWPM \_ 圖層 \_ ALE \_ 驗證 \_ 接收 \_ 接受 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md)層的篩選準則符合 TCP [**接受 ()**](/windows/desktop/api/winsock2/nf-winsock2-accept)呼叫、第一個 UDP 封包 (來自唯一遠端位址/埠元組的單點傳送) ，以及針對第一個輸入的非錯誤 ICMP 訊息 (具有唯一 ICMP 類型、代碼和識別碼的單點傳送) 。</span><span class="sxs-lookup"><span data-stu-id="56dd0-119">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**accept()**](/windows/desktop/api/winsock2/nf-winsock2-accept) calls, for first UDP packets (unicast) from a unique remote address/port tuple, and for first inbound non-error ICMP messages (unicast) with a unique ICMP type, code, and ID.</span></span>

> [!Note]  
> <span data-ttu-id="56dd0-120">非 TCP 或 ICMP 的通訊協定會視為 UDP。</span><span class="sxs-lookup"><span data-stu-id="56dd0-120">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="56dd0-121">原始通訊端接收的 TCP 封包會以類似 UDP 流量的方式處理。</span><span class="sxs-lookup"><span data-stu-id="56dd0-121">TCP packets received by raw sockets are handled similarly to UDP traffic.</span></span> <span data-ttu-id="56dd0-122">也就是說，只會篩選第一個 TCP [**傳送 ()**](/windows/desktop/api/winsock2/nf-winsock2-send) 以及透過原始通訊端的第一個 tcp [**接收 ()**](/windows/desktop/api/winsock/nf-winsock-recv) 。</span><span class="sxs-lookup"><span data-stu-id="56dd0-122">That is, only the first TCP [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) and the first TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) over raw sockets will be filtered.</span></span>

## <a name="auth_connect"></a><span data-ttu-id="56dd0-123">驗證 \_ 連接</span><span class="sxs-lookup"><span data-stu-id="56dd0-123">AUTH\_CONNECT</span></span>

<span data-ttu-id="56dd0-124">[**FWPM \_ layer \_ ALE \_ AUTH AUTH \_ CONNECT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md)層的篩選準則會比對 TCP [**CONNECT ()**](/windows/desktop/api/winsock2/nf-winsock2-connect)呼叫、傳送給唯一遠端位址和埠元組的第一封 UDP 封包，以及具有唯一 ICMP 類型、代碼和識別碼的第一個輸出非錯誤 ICMP 訊息。</span><span class="sxs-lookup"><span data-stu-id="56dd0-124">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**connect()**](/windows/desktop/api/winsock2/nf-winsock2-connect) calls, for first UDP packets sent to a unique remote address and port tuple, and for first outbound non-error ICMP messages with a unique ICMP type, code, and ID.</span></span>

> [!Note]  
> <span data-ttu-id="56dd0-125">非 TCP 或 ICMP 的通訊協定會視為 UDP。</span><span class="sxs-lookup"><span data-stu-id="56dd0-125">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="56dd0-126">原始通訊端傳送的 TCP 封包會以類似 UDP 流量的方式處理。</span><span class="sxs-lookup"><span data-stu-id="56dd0-126">TCP packets sent by raw sockets are handled similarly to UDP traffic.</span></span> <span data-ttu-id="56dd0-127">也就是說，只會篩選第一個 TCP [**傳送 ()**](/windows/desktop/api/winsock2/nf-winsock2-send) 以及透過原始通訊端的第一個 tcp [**接收 ()**](/windows/desktop/api/winsock/nf-winsock-recv) 。</span><span class="sxs-lookup"><span data-stu-id="56dd0-127">That is, only the first TCP [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) and the first TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) over raw sockets will be filtered.</span></span>

## <a name="flow_established"></a><span data-ttu-id="56dd0-128">流程已 \_ 建立</span><span class="sxs-lookup"><span data-stu-id="56dd0-128">FLOW\_ESTABLISHED</span></span>

<span data-ttu-id="56dd0-129">在 TCP 三向交握成功完成後，會比對 [**FWPM 層的 ALE 流程所建立的篩選準則 \_ \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 層。</span><span class="sxs-lookup"><span data-stu-id="56dd0-129">A filter at the [**FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched after a TCP three-way handshake has successfully completed.</span></span> <span data-ttu-id="56dd0-130">若為非 TCP 流量，篩選準則會在符合 **驗證 \_ 接收 \_ 接受** 或 **驗證 \_ 連接** 層的篩選準則之後立即符合。</span><span class="sxs-lookup"><span data-stu-id="56dd0-130">For non-TCP traffic, the filter is matched immediately after filters from **AUTH\_RECV\_ACCEPT** or **AUTH\_CONNECT** layers are matched.</span></span>

<span data-ttu-id="56dd0-131">這一層的篩選不應傳回區塊或允許。</span><span class="sxs-lookup"><span data-stu-id="56dd0-131">A filter at this layer should not return Block or Permit.</span></span>

<span data-ttu-id="56dd0-132">注標驅動程式會使用此圖層來追蹤連接狀態，如 [Windows 驅動程式套件](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) 檔中的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="56dd0-132">This layer is used by callout drivers to track connection state, described in detail in the [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) documentation.</span></span>

## <a name="resource_release"></a><span data-ttu-id="56dd0-133">資源 \_ 版本</span><span class="sxs-lookup"><span data-stu-id="56dd0-133">RESOURCE\_RELEASE</span></span>

<span data-ttu-id="56dd0-134">[**FWPM \_ 圖層 \_ ALE \_ 資源 \_ 版本 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md)層的篩選準則會在已釋放透過 **資源 \_ 指派** 配置的資源之後進行比對。</span><span class="sxs-lookup"><span data-stu-id="56dd0-134">A filter at the [**FWPM\_LAYER\_ALE\_RESOURCE\_RELEASE\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched after resources that were allocated via **RESOURCE\_ASSIGNMENT** have been freed.</span></span>

## <a name="endpoint_closure"></a><span data-ttu-id="56dd0-135">\_結束端點</span><span class="sxs-lookup"><span data-stu-id="56dd0-135">ENDPOINT\_CLOSURE</span></span>

<span data-ttu-id="56dd0-136">當連接的 TCP 流量或 UDP 通訊端端點關閉時，會比對 [**FWPM \_ 層 \_ ALE \_ 端點 \_ 關閉 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) 層的篩選。</span><span class="sxs-lookup"><span data-stu-id="56dd0-136">A filter at the [**FWPM\_LAYER\_ALE\_ENDPOINT\_CLOSURE\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched when a connected TCP flow or UDP sockets endpoint is closed.</span></span>

## <a name="connect_redirect"></a><span data-ttu-id="56dd0-137">連接重新 \_ 導向</span><span class="sxs-lookup"><span data-stu-id="56dd0-137">CONNECT\_REDIRECT</span></span>

<span data-ttu-id="56dd0-138">[**FWPM \_ layer \_ ALE \_ CONNECT 重新 \_ 導向 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md)層的篩選器可讓您修改遠端位址和埠。</span><span class="sxs-lookup"><span data-stu-id="56dd0-138">A filter at the [**FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer allows for modification of remote addresses and ports.</span></span> <span data-ttu-id="56dd0-139">輸出連線會在該連線的持續時間內重新導向。</span><span class="sxs-lookup"><span data-stu-id="56dd0-139">The outbound connection will be redirected for the duration of that connection.</span></span>

## <a name="bind_redirect"></a><span data-ttu-id="56dd0-140">系結重新 \_ 導向</span><span class="sxs-lookup"><span data-stu-id="56dd0-140">BIND\_REDIRECT</span></span>

<span data-ttu-id="56dd0-141">[**FWPM layer ALE 系結 \_ 重新 \_ \_ \_ 導向 \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md)層的篩選器可讓您修改基礎通訊端的本機位址和埠。</span><span class="sxs-lookup"><span data-stu-id="56dd0-141">A filter at the [**FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer allows for modification of the underlying socket's local address and ports.</span></span> <span data-ttu-id="56dd0-142">在通訊端的存留期內，將會重新導向本機通訊端</span><span class="sxs-lookup"><span data-stu-id="56dd0-142">The local socket will be redirected for the lifetime of the socket</span></span>

## <a name="ale-discard-layers"></a><span data-ttu-id="56dd0-143">ALE 捨棄層</span><span class="sxs-lookup"><span data-stu-id="56dd0-143">ALE DISCARD Layers</span></span>

<span data-ttu-id="56dd0-144">針對上面所述的每個 ALE 層，篩選引擎包含相符的捨棄層。</span><span class="sxs-lookup"><span data-stu-id="56dd0-144">For each of the ALE layers described above the filtering engine contains a matching discard layer.</span></span> <span data-ttu-id="56dd0-145">基於記錄目的，注解會使用 ALE 捨棄層。</span><span class="sxs-lookup"><span data-stu-id="56dd0-145">The ALE discard layers are used by callouts for logging purposes.</span></span> <span data-ttu-id="56dd0-146">在其中一個 ALE 篩選層中捨棄的封包和指示，會以相符的 ALE 捨棄層表示。</span><span class="sxs-lookup"><span data-stu-id="56dd0-146">Packets and indications that have been discarded at one of the ALE filtering layers are indicated to the matching ALE discard layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56dd0-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="56dd0-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56dd0-148">應用層強制 (ALE) </span><span class="sxs-lookup"><span data-stu-id="56dd0-148">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="56dd0-149">ALE 具狀態篩選</span><span class="sxs-lookup"><span data-stu-id="56dd0-149">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="56dd0-150">ALE 多播/廣播流量</span><span class="sxs-lookup"><span data-stu-id="56dd0-150">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="56dd0-151">ALE 重新授權</span><span class="sxs-lookup"><span data-stu-id="56dd0-151">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="56dd0-152">ALE 流程自訂</span><span class="sxs-lookup"><span data-stu-id="56dd0-152">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> <dt>

[<span data-ttu-id="56dd0-153">TCP 封包流程</span><span class="sxs-lookup"><span data-stu-id="56dd0-153">TCP Packet Flows</span></span>](tcp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="56dd0-154">UDP 封包流程</span><span class="sxs-lookup"><span data-stu-id="56dd0-154">UDP Packet Flows</span></span>](udp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="56dd0-155">Winsock 函數</span><span class="sxs-lookup"><span data-stu-id="56dd0-155">Winsock Functions</span></span>](/windows/desktop/WinSock/winsock-functions)
</dt> <dt>

[<span data-ttu-id="56dd0-156">**篩選準則旗標**</span><span class="sxs-lookup"><span data-stu-id="56dd0-156">**Filtering Condition Flags**</span></span>](filtering-condition-flags-.md)
</dt> <dt>

[<span data-ttu-id="56dd0-157">**篩選每個篩選層級的可用條件**</span><span class="sxs-lookup"><span data-stu-id="56dd0-157">**Filtering Conditions Available At Each Filtering Layer**</span></span>](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 