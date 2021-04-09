---
description: 列出針對函數探索用戶端進行疑難排解時要使用的診斷程式。
ms.assetid: e488882a-fadd-4150-89ef-b958c3df34c6
title: 針對函數探索用戶端進行疑難排解
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a44c17b269a604efa1f5f999dff22211cee24f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691511"
---
# <a name="troubleshooting-function-discovery-clients"></a><span data-ttu-id="bfa88-103">針對函數探索用戶端進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="bfa88-103">Troubleshooting Function Discovery Clients</span></span>

<span data-ttu-id="bfa88-104">函數探索用戶端：</span><span class="sxs-lookup"><span data-stu-id="bfa88-104">Function Discovery clients:</span></span>

-   <span data-ttu-id="bfa88-105">一律使用 UDP WS-Discovery 進行裝置探索</span><span class="sxs-lookup"><span data-stu-id="bfa88-105">Always use UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="bfa88-106">一律起始中繼資料交換的 HTTP 或 HTTPS 連接</span><span class="sxs-lookup"><span data-stu-id="bfa88-106">Always initiate HTTP or HTTPS connections for metadata exchange</span></span>
-   <span data-ttu-id="bfa88-107">有時使用導向探索</span><span class="sxs-lookup"><span data-stu-id="bfa88-107">Sometimes use directed discovery</span></span>
-   <span data-ttu-id="bfa88-108">有時使用安全通道 (HTTPS) 進行中繼資料交換</span><span class="sxs-lookup"><span data-stu-id="bfa88-108">Sometimes use a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="bfa88-109">下列清單顯示功能探索用戶端傳送和接收的一般訊息順序。</span><span class="sxs-lookup"><span data-stu-id="bfa88-109">The following list shows the typical sequence of messages sent and received by Function Discovery clients.</span></span> <span data-ttu-id="bfa88-110">並非所有的訊息都是強制性的。</span><span class="sxs-lookup"><span data-stu-id="bfa88-110">Not all messages are mandatory.</span></span>

1.  <span data-ttu-id="bfa88-111">用戶端會傳送 [探查](probe-message.md) 訊息以探索裝置和服務。</span><span class="sxs-lookup"><span data-stu-id="bfa88-111">The client sends a [Probe](probe-message.md) message to discover devices and services.</span></span> <span data-ttu-id="bfa88-112">如果用戶端使用導向探索，則會透過 HTTP 或 HTTPS 傳送此訊息;否則，UDP 多播會將訊息傳送到埠3702。</span><span class="sxs-lookup"><span data-stu-id="bfa88-112">If the client is using directed discovery then this message is sent over HTTP or HTTPS; otherwise, the message is sent by UDP multicast to port 3702.</span></span>
2.  <span data-ttu-id="bfa88-113">用戶端會接收來自相符裝置或服務的 [ProbeMatches](probematches-message.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="bfa88-113">The client receives [ProbeMatches](probematches-message.md) messages from matching devices or services.</span></span> <span data-ttu-id="bfa88-114">導向的探索訊息會透過 HTTP 或 HTTPS 傳送;否則，這些訊息會由 UDP 單播傳送，並源自埠3702。</span><span class="sxs-lookup"><span data-stu-id="bfa88-114">Directed discovery messages are sent over HTTP or HTTPS; otherwise, these messages are sent by UDP unicast and originate from port 3702.</span></span>
3.  <span data-ttu-id="bfa88-115">如果 ProbeMatches 訊息中未包含任何 XAddrs，則用戶端會透過 UDP 多播將 [解析](resolve-message.md) 訊息傳送到埠3702。</span><span class="sxs-lookup"><span data-stu-id="bfa88-115">If no XAddrs were included in the ProbeMatches message, then the client will send a [Resolve](resolve-message.md) message by UDP multicast to port 3702.</span></span>
4.  <span data-ttu-id="bfa88-116">如果傳送了 [解析](resolve-message.md) 訊息，則用戶端會收到相符服務的 [ResolveMatches](resolvematches-message.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="bfa88-116">If a [Resolve](resolve-message.md) message was sent, then the client receives a [ResolveMatches](resolvematches-message.md) message from matching services.</span></span> <span data-ttu-id="bfa88-117">此訊息是由 UDP 單播從埠3702傳送到解析訊息來源的埠。</span><span class="sxs-lookup"><span data-stu-id="bfa88-117">This message is sent by UDP unicast from port 3702 to the port where the Resolve message originated.</span></span>
5.  <span data-ttu-id="bfa88-118">用戶端會傳送 [Get](get--metadata-exchange--http-request-and-message.md) 訊息，以從裝置或服務要求中繼資料。</span><span class="sxs-lookup"><span data-stu-id="bfa88-118">The client sends a [Get](get--metadata-exchange--http-request-and-message.md) message to request metadata from the device or service.</span></span> <span data-ttu-id="bfa88-119">此訊息是由 HTTP 或 HTTPS 傳送。</span><span class="sxs-lookup"><span data-stu-id="bfa88-119">This message is sent by HTTP or HTTPS.</span></span>
6.  <span data-ttu-id="bfa88-120">用戶端會收到具有裝置或服務中繼資料的 [GetResponse](getresponse--metadata-exchange--message.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="bfa88-120">The client receives a [GetResponse](getresponse--metadata-exchange--message.md) message with the device or service metadata.</span></span> <span data-ttu-id="bfa88-121">此訊息是由 HTTP 或 HTTPS 傳送。</span><span class="sxs-lookup"><span data-stu-id="bfa88-121">This message is sent by HTTP or HTTPS.</span></span>

<span data-ttu-id="bfa88-122">下列診斷程式應依序 (使用) ，以協助找出函式探索用戶端的問題。</span><span class="sxs-lookup"><span data-stu-id="bfa88-122">The following diagnostic procedures should be used (in order) to help identify problems with a Function Discovery client.</span></span>

<span data-ttu-id="bfa88-123">**針對函數探索用戶端進行疑難排解**</span><span class="sxs-lookup"><span data-stu-id="bfa88-123">**To troubleshoot a Function Discovery client**</span></span>

1.  <span data-ttu-id="bfa88-124">如果使用導向探索，請 [針對導向探索進行疑難排解](troubleshooting-applications-using-directed-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="bfa88-124">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="bfa88-125">[檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="bfa88-125">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="bfa88-126">[使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="bfa88-126">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="bfa88-127">[使用 WSD Debug 用戶端來驗證多播流量](using-wsddebug-client-to-verify-multicast-traffic.md)。</span><span class="sxs-lookup"><span data-stu-id="bfa88-127">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="bfa88-128">[檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="bfa88-128">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="bfa88-129">[使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="bfa88-129">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="bfa88-130">[使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)。</span><span class="sxs-lookup"><span data-stu-id="bfa88-130">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="bfa88-131">[檢查 HTTP 中繼資料交換的網路追蹤](inspecting-network-traces-for-http-metadata-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="bfa88-131">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="bfa88-132">如果無法使用上述診斷程式來識別問題的來源，請遵循 [啟用 WSDAPI 追蹤](enabling-wsdapi-tracing.md) 並聯絡 Microsoft 支援服務的指示。</span><span class="sxs-lookup"><span data-stu-id="bfa88-132">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfa88-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="bfa88-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfa88-134">使用 WSDAPI 進行疑難排解的開始使用</span><span class="sxs-lookup"><span data-stu-id="bfa88-134">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



