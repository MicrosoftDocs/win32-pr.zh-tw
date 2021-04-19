---
description: 如果泛型主機和用戶端可以在網路上看到彼此，但是實際的主機和用戶端無法，則可能是問題是在網路上端點之間傳送的訊息中。
ms.assetid: 1b0943fb-076e-4feb-9a4f-36a06bdd19ae
title: 使用 WSD Debug 用戶端來驗證多播流量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a814ac97512ef4b0691c22d3238d151372023a7
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380662"
---
# <a name="using-wsd-debug-client-to-verify-multicast-traffic"></a><span data-ttu-id="453b4-103">使用 WSD Debug 用戶端來驗證多播流量</span><span class="sxs-lookup"><span data-stu-id="453b4-103">Using WSD Debug Client to Verify Multicast Traffic</span></span>

<span data-ttu-id="453b4-104">如果泛型主機和用戶端可以在網路上看到彼此，但是實際的主機和用戶端無法，則可能是問題是在網路上端點之間傳送的訊息中。</span><span class="sxs-lookup"><span data-stu-id="453b4-104">If the generic host and client can see each other on the network but the actual host and client cannot, it is likely that the problem is in the messages sent between the endpoints over the network.</span></span> <span data-ttu-id="453b4-105">如需泛型主機和用戶端的詳細資訊，請參閱 [使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="453b4-105">For more information about the generic host and client, see [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span> <span data-ttu-id="453b4-106">因為完整的網路追蹤可能很難收集、篩選和讀取，所以可以使用 WSD Debug 用戶端工具來列印 WS-Discovery 訊息的多播邊。</span><span class="sxs-lookup"><span data-stu-id="453b4-106">Because full network traces can be difficult to collect, filter, and read, the WSD Debug Client tool can be used to print the multicast sides of WS-Discovery messages.</span></span>

<span data-ttu-id="453b4-107">多播模式中的 WSD Debug 用戶端只能檢查一半的訊息，因為用戶端無法列印單播訊息。</span><span class="sxs-lookup"><span data-stu-id="453b4-107">The WSD Debug Client in multicast mode can only inspect half of the messages, since the client cannot print unicast messages.</span></span> <span data-ttu-id="453b4-108">如果您有興趣的單播流量，請直接跳到 [檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="453b4-108">If unicast traffic is of interest, skip directly to [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="453b4-109">此程式會顯示一個方法，顯示網路上的所有多播流量。</span><span class="sxs-lookup"><span data-stu-id="453b4-109">This procedure shows a method that will display all multicast traffic on the network.</span></span> <span data-ttu-id="453b4-110">若只要顯示進出裝置的多播流量，請參閱下面的「 [篩選 WSD Debug 用戶端結果](#filtering-wsd-debug-client-results) 」一節。</span><span class="sxs-lookup"><span data-stu-id="453b4-110">To display only multicast traffic to and from the device, see the [Filtering WSD Debug Client Results](#filtering-wsd-debug-client-results) section below.</span></span>

<span data-ttu-id="453b4-111">**使用 WSD Debug 用戶端來驗證多播流量**</span><span class="sxs-lookup"><span data-stu-id="453b4-111">**To use the WSD Debug Client to verify multicast traffic**</span></span>

1.  <span data-ttu-id="453b4-112">將主機和用戶端設定為在網路上執行 (也就是確定主機和用戶端會在) 的不同電腦上運作。</span><span class="sxs-lookup"><span data-stu-id="453b4-112">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="453b4-113">開啟命令提示字元，然後執行下列命令： **WSDDebug \_client.exe/mode 多播**</span><span class="sxs-lookup"><span data-stu-id="453b4-113">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast**</span></span>
3.  <span data-ttu-id="453b4-114">啟動主機和用戶端，或在網路總管中按 F5，以重現失敗。</span><span class="sxs-lookup"><span data-stu-id="453b4-114">Reproduce the failure by starting the host and client or by pressing F5 in the Network Explorer.</span></span>
4.  <span data-ttu-id="453b4-115">確認訊息正在進行多播。</span><span class="sxs-lookup"><span data-stu-id="453b4-115">Verify that messages are being multicast.</span></span>

<span data-ttu-id="453b4-116">如果所需的訊息顯示在 WSD Debug 用戶端輸出中，則應用程式失敗可能會位於多播訊息內容中，或是對應單播回應訊息的存在或內容中。</span><span class="sxs-lookup"><span data-stu-id="453b4-116">If the required messages are displayed in the WSD Debug Client output, then the application failure may be in the multicast message content, or in the existence or content of the corresponding unicast response messages.</span></span> <span data-ttu-id="453b4-117">遵循 [檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md)中的指示，繼續進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="453b4-117">Continue troubleshooting by following the instructions in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="453b4-118">如果在 WSD Debug 用戶端輸出中顯示必要的訊息，則可能已識別出應用程式問題的來源。</span><span class="sxs-lookup"><span data-stu-id="453b4-118">If the required messages are displayed in the WSD Debug Client output, then it is likely that the source of the application problem has been identified.</span></span> <span data-ttu-id="453b4-119">網路上可能不會傳輸多播流量。</span><span class="sxs-lookup"><span data-stu-id="453b4-119">It is likely that the multicast traffic is not being transmitted on the network.</span></span> <span data-ttu-id="453b4-120">當應用程式未正確列舉多播介面卡時，就會發生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="453b4-120">This failure can happen when the application does not enumerate multicast adapters correctly.</span></span> <span data-ttu-id="453b4-121">應用程式必須在所有網路介面上明確地傳送多播流量;否則，可能不會針對回送介面或其他介面產生封包。</span><span class="sxs-lookup"><span data-stu-id="453b4-121">Applications must explicitly send multicast traffic over all network interfaces; otherwise, packets may not be generated for the loopback interface or for other interfaces.</span></span> <span data-ttu-id="453b4-122">若要確認封包未出現在網路上，請遵循 [檢查網路追蹤中的 UDP ws-management](inspecting-network-traces-for-udp-ws-discovery.md) 的指示，並尋找遺失的多播訊息的辨識項。</span><span class="sxs-lookup"><span data-stu-id="453b4-122">To verify that the packets are not appearing on the network, follow the instructions in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) and look for evidence of missing multicast messages.</span></span>

## <a name="verifying-that-messages-are-being-multicast"></a><span data-ttu-id="453b4-123">確認訊息正在多播</span><span class="sxs-lookup"><span data-stu-id="453b4-123">Verifying that messages are being multicast</span></span>

<span data-ttu-id="453b4-124">一律確認 [探查](probe-message.md) 訊息是多播。</span><span class="sxs-lookup"><span data-stu-id="453b4-124">Always verify that [Probe](probe-message.md) messages are being multicast.</span></span> <span data-ttu-id="453b4-125">（選擇性）確認 [Hello](hello-message.md) 和 [Resolve](resolve-message.md) 訊息是多播。</span><span class="sxs-lookup"><span data-stu-id="453b4-125">Optionally, verify that [Hello](hello-message.md) and [Resolve](resolve-message.md) messages are being multicast.</span></span> <span data-ttu-id="453b4-126">請注意，並非所有應用程式都使用解析訊息。</span><span class="sxs-lookup"><span data-stu-id="453b4-126">Note that not all applications use Resolve messages.</span></span> <span data-ttu-id="453b4-127">如需用戶端和主機使用之訊息模式的詳細資訊，請參閱 [探索和中繼資料交換訊息模式](discovery-and-metadata-exchange-message-patterns.md) ，以及 [使用 WSDAPI 疑難排解的開始使用](getting-started-with-wsdapi-troubleshooting.md)。</span><span class="sxs-lookup"><span data-stu-id="453b4-127">For more information about message patterns used by clients and hosts, see [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md) and [Getting Started with WSDAPI Troubleshooting](getting-started-with-wsdapi-troubleshooting.md).</span></span>

<span data-ttu-id="453b4-128">必須觸發訊息，才能依照上述步驟3所述的方式傳送訊息。</span><span class="sxs-lookup"><span data-stu-id="453b4-128">Messages must be triggered in order to be sent as described in step 3 above.</span></span> <span data-ttu-id="453b4-129">WSD Debug 用戶端會將原始的 SOAP 訊息顯示為輸出。</span><span class="sxs-lookup"><span data-stu-id="453b4-129">The WSD Debug Client displays the raw SOAP message as output.</span></span> <span data-ttu-id="453b4-130">因為所有在多播模式中由 WSD Debug 用戶端列印的訊息都會透過多播通訊端接收，所以不會顯示訊息目的地位址。</span><span class="sxs-lookup"><span data-stu-id="453b4-130">Because all messages printed by WSD Debug Client in multicast mode are received over a multicast socket, the message destination address is not displayed.</span></span>

<span data-ttu-id="453b4-131">下列範例 WSD Debug 用戶端輸出會顯示探查訊息。</span><span class="sxs-lookup"><span data-stu-id="453b4-131">The following sample WSD Debug Client output shows a Probe message.</span></span> <span data-ttu-id="453b4-132">元素會將 \<wsa:Action> 訊息識別為探查訊息。</span><span class="sxs-lookup"><span data-stu-id="453b4-132">The \<wsa:Action> element identifies the message as a Probe message.</span></span> <span data-ttu-id="453b4-133">檢查 \<wsa:Action> 欄位，確認接收的訊息是探查訊息。</span><span class="sxs-lookup"><span data-stu-id="453b4-133">Inspect the \<wsa:Action> field to verify that the received message was a Probe message.</span></span>

``` syntax
UDP message at 05/08/07 10:06:55 from soap.udp://[127.0.0.1:49334]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe</wsa:Action>
<wsa:MessageID>urn:uuid:256ad815-1576-4e59-8efc-4c1e0f15fdd2</wsa:MessageID></so
ap:Header><soap:Body><wsd:Probe><wsd:Types>wsdp:Device</wsd:Types></wsd:Probe></
soap:Body></soap:Envelope>
```

<span data-ttu-id="453b4-134">下列範例 WSD Debug 用戶端輸出會顯示 Hello 訊息。</span><span class="sxs-lookup"><span data-stu-id="453b4-134">The following sample WSD Debug Client output shows a Hello message.</span></span> <span data-ttu-id="453b4-135">元素會將 \<wsa:Action> 訊息識別為 Hello 訊息。</span><span class="sxs-lookup"><span data-stu-id="453b4-135">The \<wsa:Action> element identifies the message as a Hello message.</span></span>

``` syntax
UDP message at 05/08/07 10:10:49 from soap.udp://[[::1]:49343]
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="h
ttp://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsd="https://schemas.xmlso
ap.org/ws/2005/04/discovery" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/d
evprof"><soap:Header><wsa:To>urn:schemas-xmlsoap-org:ws:2005:04:discovery</wsa:T
o><wsa:Action>https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello</wsa:Action>
<wsa:MessageID>urn:uuid:8999e29a-b056-4345-9e13-f42dbedab28a</wsa:MessageID><wsd
:AppSequence InstanceId="1" SequenceId="urn:uuid:abb0a2a1-6efc-4242-b8e7-c02484a
6eea2" MessageNumber="1"></wsd:AppSequence></soap:Header><soap:Body><wsd:Hello><
wsa:EndpointReference><wsa:Address>urn:uuid:02a76d74-82d0-43e6-ab09-16f54ab81ac6
</wsa:Address></wsa:EndpointReference><wsd:Types>wsdp:Device</wsd:Types><wsd:Met
adataVersion>1</wsd:MetadataVersion></wsd:Hello></soap:Body></soap:Envelope>
```

## <a name="filtering-wsd-debug-client-results"></a><span data-ttu-id="453b4-136">篩選 WSD Debug 用戶端結果</span><span class="sxs-lookup"><span data-stu-id="453b4-136">Filtering WSD Debug Client Results</span></span>

<span data-ttu-id="453b4-137">篩選 WSD Debug 用戶端結果有助於識別牽涉到裝置的事件流量。</span><span class="sxs-lookup"><span data-stu-id="453b4-137">Filtering the WSD Debug Client results can help identify incident traffic involving the device.</span></span> <span data-ttu-id="453b4-138">只有在雜訊的網路上才需要篩選。</span><span class="sxs-lookup"><span data-stu-id="453b4-138">Filtering is only necessary on noisy networks.</span></span>

<span data-ttu-id="453b4-139">有兩種方式可以篩選結果。</span><span class="sxs-lookup"><span data-stu-id="453b4-139">There are two ways to filter results.</span></span> <span data-ttu-id="453b4-140">啟動 WSD Debug 用戶端時，可以明確識別要篩選的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="453b4-140">The IP addresses to filter can be explicitly identified when starting the WSD Debug Client.</span></span> <span data-ttu-id="453b4-141">或者，您可以在用戶端啟動之後指定 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="453b4-141">Alternatively, the IP addresses can be specified after the client has started.</span></span> <span data-ttu-id="453b4-142">本節將說明這兩種方法。</span><span class="sxs-lookup"><span data-stu-id="453b4-142">This section describes both methods.</span></span>

<span data-ttu-id="453b4-143">**若要在啟動 WSD Debug 用戶端時指定要篩選的 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="453b4-143">**To specify IP addresses to filter when starting WSD Debug Client**</span></span>

1.  <span data-ttu-id="453b4-144">將主機和用戶端設定為在網路上執行 (也就是確定主機和用戶端會在) 的不同電腦上運作。</span><span class="sxs-lookup"><span data-stu-id="453b4-144">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="453b4-145">收集裝置 (es) 的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="453b4-145">Collect the IP address(es) of the device.</span></span> <span data-ttu-id="453b4-146">如果裝置有多個位址 (例如，它同時具有 IPv4 和 IPv6 位址) 必須收集所有位址。</span><span class="sxs-lookup"><span data-stu-id="453b4-146">If the device has multiple addresses (for example, it has both IPv4 and IPv6 addresses) all addresses must be collected.</span></span>
3.  <span data-ttu-id="453b4-147">開啟命令提示字元，然後執行下列命令： \**WSDDebug \_client.exe/mode 多播/ip add\*\*\*<device IP>*</span><span class="sxs-lookup"><span data-stu-id="453b4-147">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast /ip add** *<device IP>*</span></span>

<span data-ttu-id="453b4-148">*<device IP>* 是 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="453b4-148">*<device IP>* is an IP address.</span></span> <span data-ttu-id="453b4-149">下列清單顯示此 IP 位址的一些範例格式。</span><span class="sxs-lookup"><span data-stu-id="453b4-149">The following list shows some sample formats for this IP address.</span></span>

-   <span data-ttu-id="453b4-150">192.168.0.1</span><span class="sxs-lookup"><span data-stu-id="453b4-150">192.168.0.1</span></span>
-   <span data-ttu-id="453b4-151">：：1</span><span class="sxs-lookup"><span data-stu-id="453b4-151">::1</span></span>
-   <span data-ttu-id="453b4-152">mydevice.contoso.com</span><span class="sxs-lookup"><span data-stu-id="453b4-152">mydevice.contoso.com</span></span>

<span data-ttu-id="453b4-153">WSD Debug 用戶端會自動解析在命令提示字元中提供的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="453b4-153">The WSD Debug Client automatically resolves hostnames supplied at the command prompt.</span></span>

<span data-ttu-id="453b4-154">**若要在啟動 WSD Debug 用戶端之後篩選結果**</span><span class="sxs-lookup"><span data-stu-id="453b4-154">**To filter results after starting WSD Debug Client**</span></span>

1.  <span data-ttu-id="453b4-155">將主機和用戶端設定為在網路上執行 (也就是確定主機和用戶端會在) 的不同電腦上運作。</span><span class="sxs-lookup"><span data-stu-id="453b4-155">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="453b4-156">收集裝置 (es) 的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="453b4-156">Collect the IP address(es) of the device.</span></span> <span data-ttu-id="453b4-157">如果裝置有多個位址 (例如，它同時具有 IPv4 和 IPv6 位址) 必須收集所有位址。</span><span class="sxs-lookup"><span data-stu-id="453b4-157">If the device has multiple addresses (for example, it has both IPv4 and IPv6 addresses) all addresses must be collected.</span></span>
3.  <span data-ttu-id="453b4-158">開啟命令提示字元，然後執行下列命令： **WSDDebug \_client.exe/mode 多播**</span><span class="sxs-lookup"><span data-stu-id="453b4-158">Open a command prompt and run the following command: **WSDDebug\_client.exe /mode multicast**</span></span>
4.  <span data-ttu-id="453b4-159">在 WSD Debug 用戶端命令提示字元中，執行下列命令： \**ip add\*\*\*<device IP>*</span><span class="sxs-lookup"><span data-stu-id="453b4-159">At the WSD Debug Client command prompt, run the following command: **ip add** *<device IP>*</span></span>
5.  <span data-ttu-id="453b4-160">重複步驟4，直到新增所有裝置 IP 位址為止。</span><span class="sxs-lookup"><span data-stu-id="453b4-160">Repeat step 4 until all device IP addresses have been added.</span></span>

<span data-ttu-id="453b4-161">下列程式假設已啟動 WSD Debug 用戶端，並依 IP 位址進行篩選。</span><span class="sxs-lookup"><span data-stu-id="453b4-161">The following procedure assumes that the WSD Debug Client has been started and filtering by IP address is occurring.</span></span>

<span data-ttu-id="453b4-162">**確認正在篩選正確的 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="453b4-162">**To verify that the correct IP addresses are being filtered**</span></span>

-   <span data-ttu-id="453b4-163">在 WSD Debug 用戶端命令提示字元中，執行下列命令： **ip 列印**</span><span class="sxs-lookup"><span data-stu-id="453b4-163">At the WSD Debug Client command prompt, run the following command: **ip print**</span></span>

    <span data-ttu-id="453b4-164">要篩選的 IP 位址清單隨即出現。</span><span class="sxs-lookup"><span data-stu-id="453b4-164">The list of IP addresses being filtered appears.</span></span>

<span data-ttu-id="453b4-165">下列程式假設已啟動 WSD Debug 用戶端，並依 IP 位址進行篩選。</span><span class="sxs-lookup"><span data-stu-id="453b4-165">The following procedure assumes that the WSD Debug Client has been started and filtering by IP address is occurring.</span></span>

<span data-ttu-id="453b4-166">**若要停用篩選**</span><span class="sxs-lookup"><span data-stu-id="453b4-166">**To disable filtering**</span></span>

-   <span data-ttu-id="453b4-167">在 WSD Debug 用戶端命令提示字元中，執行下列命令： **ip clear**</span><span class="sxs-lookup"><span data-stu-id="453b4-167">At the WSD Debug Client command prompt, run the following command: **ip clear**</span></span>

    <span data-ttu-id="453b4-168">所有多播流量現在都會顯示在調試輸出中。</span><span class="sxs-lookup"><span data-stu-id="453b4-168">All multicast traffic will now be shown in the debug output.</span></span>

## <a name="related-topics"></a><span data-ttu-id="453b4-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="453b4-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="453b4-170">WSDAPI 診斷程式</span><span class="sxs-lookup"><span data-stu-id="453b4-170">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="453b4-171">使用 WSDAPI 進行疑難排解的開始使用</span><span class="sxs-lookup"><span data-stu-id="453b4-171">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



