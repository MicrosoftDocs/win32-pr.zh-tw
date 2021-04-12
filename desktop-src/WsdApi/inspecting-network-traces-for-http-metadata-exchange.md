---
description: 任何可顯示原始封包的網路封包分析器，都可以用來檢查 HTTP 中繼資料交換要求。 建議使用 Microsoft 網路監視器 3 (Netmon) 。 如需 Netmon 的詳細資訊，請參閱下載 Netmon 和範例 DPWS 篩選器。
ms.assetid: b3b6c4d1-5fa3-41fb-ae1d-067638e385b0
title: 檢查 HTTP 中繼資料交換的網路追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9993c542789b7f11eb35344dd6b0b03bfbafc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192173"
---
# <a name="inspecting-network-traces-for-http-metadata-exchange"></a><span data-ttu-id="952b7-105">檢查 HTTP 中繼資料交換的網路追蹤</span><span class="sxs-lookup"><span data-stu-id="952b7-105">Inspecting Network Traces for HTTP Metadata Exchange</span></span>

<span data-ttu-id="952b7-106">任何可顯示原始封包的網路封包分析器，都可以用來檢查 HTTP 中繼資料交換要求。</span><span class="sxs-lookup"><span data-stu-id="952b7-106">Any network packet analyzer that can display raw packets can be used to inspect HTTP metadata exchange requests.</span></span> <span data-ttu-id="952b7-107">建議使用 Microsoft 網路監視器 3 (Netmon) 。</span><span class="sxs-lookup"><span data-stu-id="952b7-107">Microsoft Network Monitor 3 (Netmon) is recommended.</span></span> <span data-ttu-id="952b7-108">如需 Netmon 的詳細資訊，請參閱 [下載 netmon 和範例 DPWS 篩選器](downloading-netmon-and-sample-dpws-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="952b7-108">For more information about Netmon, see [Downloading Netmon and Sample DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span></span>

<span data-ttu-id="952b7-109">針對使用安全通道進行通訊的用戶端和主機，此診斷程式可能不會很有用，因為訊息內容已加密。</span><span class="sxs-lookup"><span data-stu-id="952b7-109">This diagnostic procedure may not be as useful for clients and hosts using a secure channel for communications because the message contents are encrypted.</span></span>

<span data-ttu-id="952b7-110">**檢查 HTTP 中繼資料交換的網路追蹤**</span><span class="sxs-lookup"><span data-stu-id="952b7-110">**To inspect network traces for HTTP metadata exchange**</span></span>

1.  <span data-ttu-id="952b7-111">將主機和用戶端設定為在網路上執行 (也就是確定主機和用戶端會在) 的不同電腦上運作。</span><span class="sxs-lookup"><span data-stu-id="952b7-111">Configure the host and client to run across the network (that is, make sure that the host and client will operate on different machines).</span></span>
2.  <span data-ttu-id="952b7-112">在用戶端或主機上安裝封包分析器 (Netmon) 。</span><span class="sxs-lookup"><span data-stu-id="952b7-112">Install the packet analyzer (Netmon) on either the client or the host.</span></span>
3.  <span data-ttu-id="952b7-113">設定封包分析器，以在連接主機和用戶端的網路介面卡上捕獲流量。</span><span class="sxs-lookup"><span data-stu-id="952b7-113">Configure the packet analyzer to capture traffic on the network adapter connecting the host and the client.</span></span>
4.  <span data-ttu-id="952b7-114">啟動主機和用戶端，或在網路總管中按 F5，以重現失敗。</span><span class="sxs-lookup"><span data-stu-id="952b7-114">Reproduce the failure by starting the host and client or by pressing F5 in the Network Explorer.</span></span>
5.  <span data-ttu-id="952b7-115">篩選結果，以隔離 WS-Discovery 和中繼資料交換流量。</span><span class="sxs-lookup"><span data-stu-id="952b7-115">Filter the results to isolate WS-Discovery and metadata exchange traffic.</span></span> <span data-ttu-id="952b7-116">若要查看範例 Netmon 篩選器，請參閱 [下載 netmon 和範例 DPWS 篩選器](downloading-netmon-and-sample-dpws-filters.md)。</span><span class="sxs-lookup"><span data-stu-id="952b7-116">To view sample Netmon filters, see [Downloading Netmon and Sample DPWS Filters](downloading-netmon-and-sample-dpws-filters.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="952b7-117">此為選用步驟。</span><span class="sxs-lookup"><span data-stu-id="952b7-117">This step is optional.</span></span>

     

6.  <span data-ttu-id="952b7-118">確認用戶端與主機之間傳送的訊息符合基本流量需求。</span><span class="sxs-lookup"><span data-stu-id="952b7-118">Verify that messages sent between client and host meet basic traffic requirements.</span></span>

## <a name="verifying-that-messages-meet-traffic-requirements"></a><span data-ttu-id="952b7-119">確認訊息符合流量需求</span><span class="sxs-lookup"><span data-stu-id="952b7-119">Verifying that messages meet traffic requirements</span></span>

<span data-ttu-id="952b7-120">WSDAPI 用戶端和主機必須傳送符合下列準則的訊息。</span><span class="sxs-lookup"><span data-stu-id="952b7-120">WSDAPI clients and hosts must send messages that conform to the following criteria.</span></span> <span data-ttu-id="952b7-121">如需訊息模式的一般資訊，請參閱 [探索和中繼資料交換訊息模式](discovery-and-metadata-exchange-message-patterns.md)。</span><span class="sxs-lookup"><span data-stu-id="952b7-121">For general information about message patterns, see [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md).</span></span>

-   <span data-ttu-id="952b7-122">訊息必須符合 [檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md)主題中提供的流量需求，除非絕對確定 WS-Discovery 不會用於中繼資料交換。</span><span class="sxs-lookup"><span data-stu-id="952b7-122">Messages must meet the traffic requirements provided in the topic [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md), unless it is absolutely certain that WS-Discovery is not being used for metadata exchange.</span></span>
-   <span data-ttu-id="952b7-123">必須在用戶端與 [ProbeMatches](probematches-message.md)或 [ResolveMatches](resolvematches-message.md)訊息的 **XAddrs** 元素中提供的第一個傳輸位址之間建立 TCP 連接。</span><span class="sxs-lookup"><span data-stu-id="952b7-123">A TCP connection must be established between the client and the first transport address provided in the **XAddrs** element of a [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message.</span></span> <span data-ttu-id="952b7-124">下列清單顯示用來建立 TCP 連接的一般封包交換。</span><span class="sxs-lookup"><span data-stu-id="952b7-124">The following list shows a typical packet exchange used to establish a TCP connection.</span></span>
    -   <span data-ttu-id="952b7-125">用戶端會將 TCP SYN 封包傳送至指定埠上的主機。</span><span class="sxs-lookup"><span data-stu-id="952b7-125">The client sends a TCP SYN packet to the host at a specified port.</span></span>
    -   <span data-ttu-id="952b7-126">主機會將 TCP SYN/ACK 封包傳送給用戶端。</span><span class="sxs-lookup"><span data-stu-id="952b7-126">The host sends a TCP SYN/ACK packet to the client.</span></span>
    -   <span data-ttu-id="952b7-127">用戶端會將 TCP ACK 封包傳送至指定埠上的主機。</span><span class="sxs-lookup"><span data-stu-id="952b7-127">The client sends a TCP ACK packet to the host at a specified port.</span></span>

    <span data-ttu-id="952b7-128">一旦用戶端傳送 TCP ACK 封包，就會建立 TCP 連接。</span><span class="sxs-lookup"><span data-stu-id="952b7-128">Once the client has sent a TCP ACK packet, the TCP connection is established.</span></span> <span data-ttu-id="952b7-129">請注意，如果先前已建立 TCP 連接，則不會發生此訊息交換。</span><span class="sxs-lookup"><span data-stu-id="952b7-129">Note that this message exchange will not occur if a TCP connection has previously been established.</span></span>
-   <span data-ttu-id="952b7-130">用戶端必須傳送有效的 [Get](get--metadata-exchange--http-request-and-message.md) HTTP 要求和訊息。</span><span class="sxs-lookup"><span data-stu-id="952b7-130">The client must send a valid [Get](get--metadata-exchange--http-request-and-message.md) HTTP request and message.</span></span>
-   <span data-ttu-id="952b7-131">主機必須接聽 [Get](get--metadata-exchange--http-request-and-message.md) HTTP 要求中所指定的 URL 路徑。</span><span class="sxs-lookup"><span data-stu-id="952b7-131">The host must be listening on the URL path specified in the [Get](get--metadata-exchange--http-request-and-message.md) HTTP request.</span></span>
-   <span data-ttu-id="952b7-132">[取得](get--metadata-exchange--http-request-and-message.md)中繼資料訊息的 **To** 專案必須存在，而且不是空的。</span><span class="sxs-lookup"><span data-stu-id="952b7-132">The **To** element of a [Get](get--metadata-exchange--http-request-and-message.md) metadata message must be present and not empty.</span></span> <span data-ttu-id="952b7-133">**To** 元素的值必須符合其中一個主機端點位址。</span><span class="sxs-lookup"><span data-stu-id="952b7-133">The value of the **To** element must match one of the host's endpoint addresses.</span></span> <span data-ttu-id="952b7-134">主機的端點位址通常會在 [ProbeMatches](probematches-message.md) 或 [ResolveMatches](resolvematches-message.md) 訊息中公告。</span><span class="sxs-lookup"><span data-stu-id="952b7-134">A host's endpoint address is typically advertised in a [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message.</span></span>
-   <span data-ttu-id="952b7-135">主機必須傳送有效的 HTTP 回應標頭。</span><span class="sxs-lookup"><span data-stu-id="952b7-135">The host must send a valid HTTP response header.</span></span> <span data-ttu-id="952b7-136">如果初始要求成功，回應標頭應包含 HTTP/1.1 200 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="952b7-136">If the initial request was successful, the response header should contain the HTTP/1.1 200 status code.</span></span>
-   <span data-ttu-id="952b7-137">主機必須傳送有效的 [GetResponse](getresponse--metadata-exchange--message.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="952b7-137">The host must send a valid [GetResponse](getresponse--metadata-exchange--message.md) message.</span></span>
-   <span data-ttu-id="952b7-138">[GetResponse](getresponse--metadata-exchange--message.md)訊息的 **RelatesTo** 元素必須存在，且不得為空白。</span><span class="sxs-lookup"><span data-stu-id="952b7-138">The **RelatesTo** element of a [GetResponse](getresponse--metadata-exchange--message.md) message must be present and must not be empty.</span></span> <span data-ttu-id="952b7-139">其值必須符合對應的 [Get](get--metadata-exchange--http-request-and-message.md)訊息中 **MessageId** 元素的值。</span><span class="sxs-lookup"><span data-stu-id="952b7-139">Its value must match the value of the **MessageId** element from the corresponding [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span>

<span data-ttu-id="952b7-140">如果由程式傳送的 HTTP 要求或中繼資料交換訊息不符合這些流量需求，則會成功識別出問題的原因，而不需要進行進一步的疑難排解步驟。</span><span class="sxs-lookup"><span data-stu-id="952b7-140">If the HTTP requests or metadata exchange messages sent by the program do not conform to these traffic requirements, the cause of the problem has been successfully identified and no further troubleshooting steps are necessary.</span></span> <span data-ttu-id="952b7-141">重寫程式，使其產生符合標準的訊息和要求，並重新測試程式。</span><span class="sxs-lookup"><span data-stu-id="952b7-141">Rewrite the program so that it generates conformant messages and requests and retest the program.</span></span>

<span data-ttu-id="952b7-142">如果仍然無法識別問題的來源，請洽詢 Microsoft 支援服務尋求協助。</span><span class="sxs-lookup"><span data-stu-id="952b7-142">If the source of the problem still cannot be identified, contact Microsoft support for assistance.</span></span> <span data-ttu-id="952b7-143">在聯繫支援之前，請收集適當的記錄檔，以協助找出問題的根本原因。</span><span class="sxs-lookup"><span data-stu-id="952b7-143">Before contacting support, collect the appropriate log files to help identify the root cause of the problem.</span></span> <span data-ttu-id="952b7-144">如需詳細資訊，請參閱 [啟用 WSDAPI 追蹤](enabling-wsdapi-tracing.md)。</span><span class="sxs-lookup"><span data-stu-id="952b7-144">For more information, see [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="952b7-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="952b7-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="952b7-146">WSDAPI 診斷程式</span><span class="sxs-lookup"><span data-stu-id="952b7-146">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="952b7-147">使用 WSDAPI 進行疑難排解的開始使用</span><span class="sxs-lookup"><span data-stu-id="952b7-147">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="952b7-148">下載 Netmon 和範例 DPWS 篩選器</span><span class="sxs-lookup"><span data-stu-id="952b7-148">Downloading Netmon and Sample DPWS Filters</span></span>](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



