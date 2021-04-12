---
description: 任何可顯示原始封包的網路封包分析器都可以用來檢查 UDP WS-Discovery 封包。 建議使用 Microsoft 網路監視器 3 (Netmon) 。 如需 Netmon 的詳細資訊，請參閱下載 Netmon 和範例 DPWS 篩選器。
ms.assetid: f12f9847-b87f-4d5f-bee3-4d219f9ad898
title: 檢查 UDP WS-Discovery 的網路追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85f4acd79588ef48c7f8e1ace2a44c9a3458475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193056"
---
# <a name="inspecting-network-traces-for-udp-ws-discovery"></a><span data-ttu-id="c2dff-105">檢查 UDP WS-Discovery 的網路追蹤</span><span class="sxs-lookup"><span data-stu-id="c2dff-105">Inspecting Network Traces for UDP WS-Discovery</span></span>

<span data-ttu-id="c2dff-106">任何可顯示原始封包的網路封包分析器都可以用來檢查 UDP WS-Discovery 封包。</span><span class="sxs-lookup"><span data-stu-id="c2dff-106">Any network packet analyzer that can display raw packets can be used to inspect UDP WS-Discovery packets.</span></span> <span data-ttu-id="c2dff-107">建議使用 Microsoft 網路監視器 3 (Netmon) 。</span><span class="sxs-lookup"><span data-stu-id="c2dff-107">Microsoft Network Monitor 3 (Netmon) is recommended.</span></span> <span data-ttu-id="c2dff-108">如需 Netmon 的詳細資訊，請參閱 [下載 netmon 和範例 DPWS 篩選器](downloading-netmon-and-sample-dpws-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="c2dff-108">For more information about Netmon, see [Downloading Netmon and Sample DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span></span>

<span data-ttu-id="c2dff-109">**檢查 UDP WS-探索的網路追蹤**</span><span class="sxs-lookup"><span data-stu-id="c2dff-109">**To inspect network traces for UDP WS-Discovery**</span></span>

1.  <span data-ttu-id="c2dff-110">將主機和用戶端設定為在網路上執行 (也就是確定主機和用戶端會在) 的不同電腦上運作。</span><span class="sxs-lookup"><span data-stu-id="c2dff-110">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="c2dff-111">在用戶端或主機上安裝封包分析器 (Netmon) 。</span><span class="sxs-lookup"><span data-stu-id="c2dff-111">Install the packet analyzer (Netmon) on either the client or the host.</span></span>
3.  <span data-ttu-id="c2dff-112">設定封包分析器，以在連接主機和用戶端的網路介面卡上捕獲流量。</span><span class="sxs-lookup"><span data-stu-id="c2dff-112">Configure the packet analyzer to capture traffic on the network adapter connecting the host and the client.</span></span>
4.  <span data-ttu-id="c2dff-113">啟動主機和用戶端，或在網路總管中按 F5，以重現失敗。</span><span class="sxs-lookup"><span data-stu-id="c2dff-113">Reproduce the failure by starting the host and client or by pressing F5 in the Network Explorer.</span></span>
5.  <span data-ttu-id="c2dff-114">篩選結果以隔離 WS-Discovery 流量。</span><span class="sxs-lookup"><span data-stu-id="c2dff-114">Filter the results to isolate WS-Discovery traffic.</span></span> <span data-ttu-id="c2dff-115">若要查看範例 Netmon 篩選器，請參閱 [下載 netmon 和範例 DPWS 篩選器](downloading-netmon-and-sample-dpws-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="c2dff-115">To view sample Netmon filters, see [Downloading Netmon and Sample DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="c2dff-116">此為選用步驟。</span><span class="sxs-lookup"><span data-stu-id="c2dff-116">This step is optional.</span></span>

     

6.  <span data-ttu-id="c2dff-117">確認用戶端與主機之間傳送的訊息符合基本流量需求。</span><span class="sxs-lookup"><span data-stu-id="c2dff-117">Verify that messages sent between client and host meet basic traffic requirements.</span></span>

## <a name="verifying-that-messages-meet-traffic-requirements"></a><span data-ttu-id="c2dff-118">確認訊息符合流量需求</span><span class="sxs-lookup"><span data-stu-id="c2dff-118">Verifying that messages meet traffic requirements</span></span>

<span data-ttu-id="c2dff-119">WSDAPI 用戶端和主機必須傳送符合下列準則的訊息。</span><span class="sxs-lookup"><span data-stu-id="c2dff-119">WSDAPI clients and hosts must send messages that conform to the following criteria.</span></span> <span data-ttu-id="c2dff-120">如需訊息模式的一般資訊，請參閱 [探索和中繼資料交換訊息模式](discovery-and-metadata-exchange-message-patterns.md)。</span><span class="sxs-lookup"><span data-stu-id="c2dff-120">For general information about message patterns, see [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md).</span></span>

-   <span data-ttu-id="c2dff-121">[探查](probe-message.md) 訊息必須由 UDP 多播傳送到埠3702。</span><span class="sxs-lookup"><span data-stu-id="c2dff-121">[Probe](probe-message.md) messages must be sent by UDP multicast to port 3702.</span></span>
-   <span data-ttu-id="c2dff-122">[探查](probe-message.md)訊息的 **Types** 元素必須存在，而且不可以是空的。</span><span class="sxs-lookup"><span data-stu-id="c2dff-122">The **Types** element of a [Probe](probe-message.md) message must be present and must not be empty.</span></span> <span data-ttu-id="c2dff-123">它必須包含主機將回應的類型。</span><span class="sxs-lookup"><span data-stu-id="c2dff-123">It must contain the types to which a host will respond.</span></span>
-   <span data-ttu-id="c2dff-124">[ProbeMatches](probematches-message.md)訊息必須傳送給傳送[探查](probe-message.md)的 UDP 通訊埠。</span><span class="sxs-lookup"><span data-stu-id="c2dff-124">A [ProbeMatches](probematches-message.md) message must be sent unicast to the UDP port from which the [Probe](probe-message.md) was sent.</span></span>
-   <span data-ttu-id="c2dff-125">[ProbeMatches](probematches-message.md)訊息的 **RelatesTo** 元素必須存在，且不得為空白。</span><span class="sxs-lookup"><span data-stu-id="c2dff-125">The **RelatesTo** element of a [ProbeMatches](probematches-message.md) message must be present and must not be empty.</span></span> <span data-ttu-id="c2dff-126">其值必須符合對應 [探查](probe-message.md)訊息中 **MessageId** 元素的值。</span><span class="sxs-lookup"><span data-stu-id="c2dff-126">Its value must match the value of the **MessageId** element from the corresponding [Probe](probe-message.md) message.</span></span>
-   <span data-ttu-id="c2dff-127">如果 [ProbeMatches](probematches-message.md)訊息中包含了 **XAddrs** 元素，則必須驗證提供的傳輸位址。</span><span class="sxs-lookup"><span data-stu-id="c2dff-127">If an **XAddrs** element was included in the [ProbeMatches](probematches-message.md) message, the supplied transport addresses must be validated.</span></span> <span data-ttu-id="c2dff-128">如需詳細資訊，請參閱 [XAddr 驗證規則](xaddr-validation-rules.md)。</span><span class="sxs-lookup"><span data-stu-id="c2dff-128">For more information, see [XAddr Validation Rules](xaddr-validation-rules.md).</span></span>
-   <span data-ttu-id="c2dff-129">[ProbeMatches](probematches-message.md)訊息必須在對應[探查](probe-message.md)訊息的4秒內傳送。</span><span class="sxs-lookup"><span data-stu-id="c2dff-129">A [ProbeMatches](probematches-message.md) message must be sent within 4 seconds of the corresponding [Probe](probe-message.md) message.</span></span> <span data-ttu-id="c2dff-130">Windows 防火牆可能會捨棄在探查訊息之後傳送超過4秒的 ProbeMatches 訊息。</span><span class="sxs-lookup"><span data-stu-id="c2dff-130">The Windows Firewall may drop a ProbeMatches message sent more than 4 seconds after a Probe message.</span></span>
-   <span data-ttu-id="c2dff-131">如果 [ProbeMatches](probematches-message.md)訊息中未包含任何 **XAddrs** 元素，且用戶端或主機會傳送 HTTP 訊息 (例如 [取得](get--metadata-exchange--http-request-and-message.md)中繼資料交換要求或) 的服務訊息，則用戶端或主機必須透過 UDP 多播將 [解析](resolve-message.md)訊息傳送到埠3702。</span><span class="sxs-lookup"><span data-stu-id="c2dff-131">If no **XAddrs** element was included in the [ProbeMatches](probematches-message.md) message, and the client or host will send an HTTP message (such as a [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange request or a service message), then the client or host must send a [Resolve](resolve-message.md) message by UDP multicast to port 3702.</span></span>
-   <span data-ttu-id="c2dff-132">如果傳送了 [解析](resolve-message.md) 訊息，則必須將 [ResolveMatches](resolvematches-message.md) 訊息傳送至傳送解析訊息的 UDP 通訊埠。</span><span class="sxs-lookup"><span data-stu-id="c2dff-132">If a [Resolve](resolve-message.md) message is sent, then a [ResolveMatches](resolvematches-message.md) message must be sent unicast to the UDP port from which the Resolve message was sent.</span></span>
-   <span data-ttu-id="c2dff-133">[ResolveMatches](resolvematches-message.md)訊息必須在對應的[解析](resolve-message.md)訊息的4秒內傳送。</span><span class="sxs-lookup"><span data-stu-id="c2dff-133">A [ResolveMatches](resolvematches-message.md) message must be sent within 4 seconds of the corresponding [Resolve](resolve-message.md) message.</span></span> <span data-ttu-id="c2dff-134">在解析訊息之後，Windows 防火牆可能會捨棄超過4秒的 ResolveMatchesmessage 傳送。</span><span class="sxs-lookup"><span data-stu-id="c2dff-134">The Windows Firewall may drop a ResolveMatchesmessage sent more than 4 seconds after a Resolve message.</span></span>

<span data-ttu-id="c2dff-135">如果程式所傳送的訊息不符合這些訊息需求，則會成功識別出問題的原因，而不需要進行進一步的疑難排解步驟。</span><span class="sxs-lookup"><span data-stu-id="c2dff-135">If the messages sent by the program do not conform to these message requirements, the cause of the problem has been successfully identified and no further troubleshooting steps are necessary.</span></span> <span data-ttu-id="c2dff-136">重寫程式，使其產生符合標準的訊息，並重新測試程式。</span><span class="sxs-lookup"><span data-stu-id="c2dff-136">Rewrite the program so that it generates conformant messages and retest the program.</span></span>

<span data-ttu-id="c2dff-137">如果仍然無法識別問題的來源，請洽詢 Microsoft 支援服務尋求協助。</span><span class="sxs-lookup"><span data-stu-id="c2dff-137">If the source of the problem still cannot be identified, contact Microsoft support for assistance.</span></span> <span data-ttu-id="c2dff-138">在聯繫支援之前，請收集適當的記錄檔，以協助找出問題的根本原因。</span><span class="sxs-lookup"><span data-stu-id="c2dff-138">Before contacting support, collect the appropriate log files to help identify the root cause of the problem.</span></span> <span data-ttu-id="c2dff-139">如需詳細資訊，請參閱 [啟用 WSDAPI 追蹤](enabling-wsdapi-tracing.md)。</span><span class="sxs-lookup"><span data-stu-id="c2dff-139">For more information, see [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2dff-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="c2dff-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2dff-141">WSDAPI 診斷程式</span><span class="sxs-lookup"><span data-stu-id="c2dff-141">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="c2dff-142">使用 WSDAPI 進行疑難排解的開始使用</span><span class="sxs-lookup"><span data-stu-id="c2dff-142">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="c2dff-143">下載 Netmon 和範例 DPWS 篩選器</span><span class="sxs-lookup"><span data-stu-id="c2dff-143">Downloading Netmon and Sample DPWS Filters</span></span>](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



