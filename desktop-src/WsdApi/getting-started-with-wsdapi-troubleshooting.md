---
description: 有兩種方式可以決定要使用的診斷程式。
ms.assetid: d6877063-6cf9-48dc-8208-0f3fc85b6d6b
title: 使用 WSDAPI 進行疑難排解的開始使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12396ea656423772d35dbd4ca237c7c536dcdaf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192175"
---
# <a name="getting-started-with-wsdapi-troubleshooting"></a><span data-ttu-id="7cda1-103">使用 WSDAPI 進行疑難排解的開始使用</span><span class="sxs-lookup"><span data-stu-id="7cda1-103">Getting Started with WSDAPI Troubleshooting</span></span>

<span data-ttu-id="7cda1-104">這份疑難排解指南包含一組 [診斷](wsdapi-diagnostic-procedures.md) 程式，可用來協助找出應用程式問題的原因。</span><span class="sxs-lookup"><span data-stu-id="7cda1-104">This troubleshooting guide contains a set of [diagnostic procedures](wsdapi-diagnostic-procedures.md) that can be used to help identify the cause of application problems.</span></span> <span data-ttu-id="7cda1-105">一旦成功識別出問題的原因，就可以套用診斷程式中的建議解決方案，以便解決問題。</span><span class="sxs-lookup"><span data-stu-id="7cda1-105">Once the cause of the problem has been successfully identified, the suggested solutions in the diagnostic procedure can be applied in order to resolve the problem.</span></span>

<span data-ttu-id="7cda1-106">有兩種方式可以決定要使用的診斷程式。</span><span class="sxs-lookup"><span data-stu-id="7cda1-106">There are two ways to determine the diagnostic procedure to use.</span></span> <span data-ttu-id="7cda1-107">其中一種方式是移至用戶端類型的 [疑難排解] 頁面，以查看用來對用戶端進行疑難排解的診斷程式逐步清單。</span><span class="sxs-lookup"><span data-stu-id="7cda1-107">One way is to go to the troubleshooting page for the type of client to view a step-by-step list of diagnostic procedures to use to troubleshoot the client.</span></span> <span data-ttu-id="7cda1-108">另一種方式是移至下方的疑難排解快速參考，以查看顯示 WSDAPI 應用程式常見問題的摘要資料表，以及用來診斷問題的程式。</span><span class="sxs-lookup"><span data-stu-id="7cda1-108">The other way is to go to the troubleshooting quick reference below to view summary tables that show common problems with WSDAPI applications and the procedures to use to diagnose the problems.</span></span>

## <a name="troubleshooting-by-type-of-client"></a><span data-ttu-id="7cda1-109">依用戶端類型進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="7cda1-109">Troubleshooting by Type of Client</span></span>

<span data-ttu-id="7cda1-110">下列主題依用戶端類型顯示相關的診斷程式。</span><span class="sxs-lookup"><span data-stu-id="7cda1-110">The following topics show the relevant diagnostic procedures by type of client.</span></span> <span data-ttu-id="7cda1-111">這些主題也會顯示與用戶端類型相關聯的訊息模式。</span><span class="sxs-lookup"><span data-stu-id="7cda1-111">These topics also show the message patterns associated with the client type.</span></span>

-   [<span data-ttu-id="7cda1-112">使用導向探索針對 WSDAPI 應用程式進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="7cda1-112">Troubleshooting WSDAPI Applications Using Directed Discovery</span></span>](troubleshooting-applications-using-directed-discovery.md)
-   [<span data-ttu-id="7cda1-113">針對函數探索用戶端進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="7cda1-113">Troubleshooting Function Discovery Clients</span></span>](troubleshooting-function-discovery-clients.md)
-   [<span data-ttu-id="7cda1-114">疑難排解近端分享/會議近端分享</span><span class="sxs-lookup"><span data-stu-id="7cda1-114">Troubleshooting People Near Me/Meetings Near Me</span></span>](troubleshooting-people-near-me-meetings-near-me.md)
-   [<span data-ttu-id="7cda1-115">針對新增印表機嚮導進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="7cda1-115">Troubleshooting the Add Printer Wizard</span></span>](troubleshooting-the-add-printer-wizard.md)
-   [<span data-ttu-id="7cda1-116">疑難排解網路總管</span><span class="sxs-lookup"><span data-stu-id="7cda1-116">Troubleshooting the Network Explorer</span></span>](troubleshooting-the-network-explorer.md)
-   [<span data-ttu-id="7cda1-117">針對投影機 Wizard 進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="7cda1-117">Troubleshooting the Projector Wizard</span></span>](troubleshooting-the-projector-wizard.md)
-   [<span data-ttu-id="7cda1-118">針對其他 WSDAPI 應用程式進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="7cda1-118">Troubleshooting Other WSDAPI Applications</span></span>](troubleshooting-wsdapi-applications.md)

## <a name="troubleshooting-quick-reference"></a><span data-ttu-id="7cda1-119">疑難排解快速參考</span><span class="sxs-lookup"><span data-stu-id="7cda1-119">Troubleshooting Quick Reference</span></span>

<span data-ttu-id="7cda1-120">下表顯示一些問題，可防止 WSDAPI 用戶端和主機在網路上看到彼此，以及交換裝置中繼資料。</span><span class="sxs-lookup"><span data-stu-id="7cda1-120">The following tables show some problems that can prevent WSDAPI clients and hosts from seeing each other on the network and from exchanging device metadata.</span></span> <span data-ttu-id="7cda1-121">這些表格也會顯示要執行的診斷程式，以及用來評估應用程式是否受到特定問題的準則。</span><span class="sxs-lookup"><span data-stu-id="7cda1-121">The tables also show the diagnostic procedures to run and the criteria to use to evaluate whether the application suffers from a particular problem.</span></span>

### <a name="network-environment-problems"></a><span data-ttu-id="7cda1-122">網路環境問題</span><span class="sxs-lookup"><span data-stu-id="7cda1-122">Network environment problems</span></span>



| <span data-ttu-id="7cda1-123">問題</span><span class="sxs-lookup"><span data-stu-id="7cda1-123">Problem</span></span>                                                                                                                                                                                              | <span data-ttu-id="7cda1-124">診斷程式</span><span class="sxs-lookup"><span data-stu-id="7cda1-124">Diagnostic Procedure</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="7cda1-125">問題識別</span><span class="sxs-lookup"><span data-stu-id="7cda1-125">Problem Identification</span></span>                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cda1-126">防火牆會封鎖網路探索流量。</span><span class="sxs-lookup"><span data-stu-id="7cda1-126">The firewall blocks Network Discovery traffic.</span></span>                                                                                                                                                       | [<span data-ttu-id="7cda1-127">檢查介面卡和防火牆設定</span><span class="sxs-lookup"><span data-stu-id="7cda1-127">Inspecting Adapter and Firewall Settings</span></span>](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | <span data-ttu-id="7cda1-128">啟用防火牆上的網路探索例外可解決問題。</span><span class="sxs-lookup"><span data-stu-id="7cda1-128">Enabling the Network Discovery exception on the firewall solves the problem.</span></span>                                                                                                                      |
| <span data-ttu-id="7cda1-129">應用程式特定的防火牆例外狀況會封鎖訊息。</span><span class="sxs-lookup"><span data-stu-id="7cda1-129">Firewall exceptions specific to the application are blocking messages.</span></span>                                                                                                                               | [<span data-ttu-id="7cda1-130">檢查介面卡和防火牆設定</span><span class="sxs-lookup"><span data-stu-id="7cda1-130">Inspecting Adapter and Firewall Settings</span></span>](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | <span data-ttu-id="7cda1-131">停用防火牆可解決問題。</span><span class="sxs-lookup"><span data-stu-id="7cda1-131">Disabling the firewall solves the problem.</span></span> <span data-ttu-id="7cda1-132">WF 會顯示應用程式特定的防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="7cda1-132">WF.msc shows application-specific firewall rules.</span></span>                                                                                                      |
| <span data-ttu-id="7cda1-133">裝置不會以及時的方式傳送 [ProbeMatches](probematches-message.md) 或 [ResolveMatches](resolvematches-message.md) 訊息， (小於4秒的) 來回應 UDP 要求。</span><span class="sxs-lookup"><span data-stu-id="7cda1-133">The device does not respond to UDP requests by sending a [ProbeMatches](probematches-message.md) or [ResolveMatches](resolvematches-message.md) message in a timely fashion (less than 4 seconds).</span></span> | [<span data-ttu-id="7cda1-134">檢查介面卡和防火牆設定</span><span class="sxs-lookup"><span data-stu-id="7cda1-134">Inspecting Adapter and Firewall Settings</span></span>](inspecting-adapter-and-firewall-settings.md)                                                                                                                                                         | <span data-ttu-id="7cda1-135">停用防火牆可解決此問題，而且在4秒內回應的一般主機會順利運作。</span><span class="sxs-lookup"><span data-stu-id="7cda1-135">Disabling the firewall solves the problem, and a generic host that responds in less than 4 seconds works successfully.</span></span>                                                                            |
| <span data-ttu-id="7cda1-136">應用程式的安全性內容不正確 (亦即，用戶端和主機沒有網路) 的足夠許可權。</span><span class="sxs-lookup"><span data-stu-id="7cda1-136">The security context of the application is incorrect (that is, the client and host do not have adequate permissions on the network).</span></span>                                                                 | <span data-ttu-id="7cda1-137">[使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md) ，或 [使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md)</span><span class="sxs-lookup"><span data-stu-id="7cda1-137">[Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md) or [Using a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md)</span></span> | <span data-ttu-id="7cda1-138">裝置位址不會顯示在 WSD Debug 用戶端輸出中。</span><span class="sxs-lookup"><span data-stu-id="7cda1-138">The device address is not shown in WSD Debug Client output.</span></span> <span data-ttu-id="7cda1-139">以系統管理員身分執行應用程式可解決問題。</span><span class="sxs-lookup"><span data-stu-id="7cda1-139">Running the application as Administrator solves the problem.</span></span>                                                                          |
| <span data-ttu-id="7cda1-140">IPSec 原則正在封鎖訊息。</span><span class="sxs-lookup"><span data-stu-id="7cda1-140">An IPSec policy is blocking messages.</span></span>                                                                                                                                                                | <span data-ttu-id="7cda1-141">[使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md) ，或 [使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md)</span><span class="sxs-lookup"><span data-stu-id="7cda1-141">[Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md) or [Using a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md)</span></span> | <span data-ttu-id="7cda1-142">裝置位址不會顯示在 WSD Debug 用戶端輸出中。</span><span class="sxs-lookup"><span data-stu-id="7cda1-142">The device address is not shown in WSD Debug Client output.</span></span> <span data-ttu-id="7cda1-143">停用防火牆無法解決此問題。</span><span class="sxs-lookup"><span data-stu-id="7cda1-143">The problem is not solved by disabling the firewall.</span></span> <span data-ttu-id="7cda1-144">無法在不受任何 IPSec 原則的電腦上重現問題。</span><span class="sxs-lookup"><span data-stu-id="7cda1-144">The problem cannot be reproduced on a machine not subject to any IPSec policies.</span></span> |



 

### <a name="discovery-traffic-problems"></a><span data-ttu-id="7cda1-145">探索流量問題</span><span class="sxs-lookup"><span data-stu-id="7cda1-145">Discovery traffic problems</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cda1-146">問題</span><span class="sxs-lookup"><span data-stu-id="7cda1-146">Problem</span></span></th>
<th><span data-ttu-id="7cda1-147">診斷程式</span><span class="sxs-lookup"><span data-stu-id="7cda1-147">Diagnostic Procedure</span></span></th>
<th><span data-ttu-id="7cda1-148">問題識別</span><span class="sxs-lookup"><span data-stu-id="7cda1-148">Problem identification</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cda1-149">因為應用程式未正確列舉多播網路介面，所以不會在網路上傳輸<a href="hello-message.md">Hello</a>、<a href="probe-message.md">探查</a>或<a href="resolve-message.md">解析</a>訊息。</span><span class="sxs-lookup"><span data-stu-id="7cda1-149"><a href="hello-message.md">Hello</a>, <a href="probe-message.md">Probe</a>, or <a href="resolve-message.md">Resolve</a> messages are not transmitted on the network because the application does not correctly enumerate the multicast network interfaces.</span></span></td>
<td><span data-ttu-id="7cda1-150"><a href="using-wsddebug-client-to-verify-multicast-traffic.md">使用 WSD Debug 用戶端來驗證多播流量</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-150"><a href="using-wsddebug-client-to-verify-multicast-traffic.md">Using WSD Debug Client to Verify Multicast Traffic</a></span></span></td>
<td><span data-ttu-id="7cda1-151">Hello、探查或解析訊息不會出現在 WSD Debug 用戶端輸出中。</span><span class="sxs-lookup"><span data-stu-id="7cda1-151">The Hello, Probe, or Resolve messages do not appear in WSD Debug Client output.</span></span> <span data-ttu-id="7cda1-152">封包不會出現在網路上。</span><span class="sxs-lookup"><span data-stu-id="7cda1-152">The packets do not appear on the network.</span></span> <span data-ttu-id="7cda1-153">未針對回送介面或其他介面產生封包。</span><span class="sxs-lookup"><span data-stu-id="7cda1-153">Packets are not generated for the loopback interface or for other interfaces.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cda1-154">針對未使用導向探索) 的應用程式，UDP 多播不會將<a href="probe-message.md">探查</a>訊息傳送到埠 3702 (。</span><span class="sxs-lookup"><span data-stu-id="7cda1-154"><a href="probe-message.md">Probe</a> messages are not sent by UDP multicast to port 3702 (for applications not using directed discovery).</span></span></td>
<td><span data-ttu-id="7cda1-155"><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS-探索的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-155"><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecting Network Traces for UDP WS-Discovery</a></span></span></td>
<td><span data-ttu-id="7cda1-156">訊息的檢查顯示其已傳送至錯誤的埠。</span><span class="sxs-lookup"><span data-stu-id="7cda1-156">Inspection of the message shows that it was sent to the wrong port.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cda1-157"><a href="probe-message.md">探查</a>訊息未包含<strong>類型</strong>元素，或<strong>類型</strong>元素是空的。</span><span class="sxs-lookup"><span data-stu-id="7cda1-157">The <a href="probe-message.md">Probe</a> message does not contain a <strong>Types</strong> element, or the <strong>Types</strong> element is empty.</span></span></td>
<td><span data-ttu-id="7cda1-158"><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS 探索的網路追蹤，</a> 或 <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">使用導向探索檢查應用程式的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-158"><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecting Network Traces for UDP WS-Discovery</a> or <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">Inspecting Network Traces for Applications Using Directed Discovery</a></span></span></td>
<td><span data-ttu-id="7cda1-159">訊息的檢查會顯示 <strong>類型</strong> 元素不存在或空白。</span><span class="sxs-lookup"><span data-stu-id="7cda1-159">Inspection of the message shows that the <strong>Types</strong> element is not present or empty.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cda1-160"><a href="probe-message.md">探查</a>訊息的<strong>types</strong>元素不包含主機將回應的類型。</span><span class="sxs-lookup"><span data-stu-id="7cda1-160">The <strong>Types</strong> element of a <a href="probe-message.md">Probe</a> message does not contain the types to which a host will respond.</span></span></td>
<td><span data-ttu-id="7cda1-161"><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS 探索的網路追蹤，</a> 或 <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">使用導向探索檢查應用程式的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-161"><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecting Network Traces for UDP WS-Discovery</a> or <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">Inspecting Network Traces for Applications Using Directed Discovery</a></span></span></td>
<td><span data-ttu-id="7cda1-162">訊息的檢查會顯示 <strong>類型</strong> 元素包含格式錯誤或不正確的值。</span><span class="sxs-lookup"><span data-stu-id="7cda1-162">Inspection of the message shows that the <strong>Types</strong> element contains a malformed or incorrect value.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cda1-163"><a href="probematches-message.md">ProbeMatches</a>訊息未傳送單播給傳送<a href="probe-message.md">探查</a>的 UDP 埠。</span><span class="sxs-lookup"><span data-stu-id="7cda1-163">A <a href="probematches-message.md">ProbeMatches</a> message was not sent unicast to the UDP port from which the <a href="probe-message.md">Probe</a> was sent.</span></span></td>
<td><span data-ttu-id="7cda1-164"><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS 探索的網路追蹤，</a> 或 <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">使用導向探索檢查應用程式的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-164"><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecting Network Traces for UDP WS-Discovery</a> or <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">Inspecting Network Traces for Applications Using Directed Discovery</a></span></span></td>
<td><span data-ttu-id="7cda1-165">檢查輸出會顯示未傳送任何 <a href="probematches-message.md">ProbeMatches</a>) 訊息，或訊息傳送至錯誤的埠。</span><span class="sxs-lookup"><span data-stu-id="7cda1-165">Inspection of the output shows that no <a href="probematches-message.md">ProbeMatches</a>) message was sent or that the message was sent to the wrong port.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7cda1-166">針對使用導向探索的應用程式， <a href="probematches-message.md">ProbeMatches</a> 必須透過 HTTP 或 HTTPS 傳送以回應 <a href="probe-message.md">探查</a> 訊息。</span><span class="sxs-lookup"><span data-stu-id="7cda1-166">For applications using directed discovery, the <a href="probematches-message.md">ProbeMatches</a> must be sent over HTTP or HTTPS in response to the <a href="probe-message.md">Probe</a> message.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cda1-167"><a href="probematches-message.md">ProbeMatches</a>訊息未包含<strong>relatesto</strong>元素，或<strong>relatesto</strong>元素是空的。</span><span class="sxs-lookup"><span data-stu-id="7cda1-167">The <a href="probematches-message.md">ProbeMatches</a> message does not contain a <strong>RelatesTo</strong> element, or the <strong>RelatesTo</strong> element is empty.</span></span></td>
<td><span data-ttu-id="7cda1-168"><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS 探索的網路追蹤，</a> 或 <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">使用導向探索檢查應用程式的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-168"><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecting Network Traces for UDP WS-Discovery</a> or <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">Inspecting Network Traces for Applications Using Directed Discovery</a></span></span></td>
<td><span data-ttu-id="7cda1-169">訊息的檢查會顯示 <strong>RelatesTo</strong> 元素不存在或空白。</span><span class="sxs-lookup"><span data-stu-id="7cda1-169">Inspection of the message shows that the <strong>RelatesTo</strong> element is not present or empty.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cda1-170"><a href="probematches-message.md">ProbeMatches</a>訊息中的<strong>RelatesTo</strong>元素值與對應的<a href="probe-message.md">探查</a>訊息中的<strong>MessageId</strong>元素值不相符。</span><span class="sxs-lookup"><span data-stu-id="7cda1-170">The value of the <strong>RelatesTo</strong> element in a <a href="probematches-message.md">ProbeMatches</a> message does not match the value of the <strong>MessageId</strong> element from the corresponding <a href="probe-message.md">Probe</a> message.</span></span></td>
<td><span data-ttu-id="7cda1-171"><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS 探索的網路追蹤，</a> 或 <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">使用導向探索檢查應用程式的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-171"><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecting Network Traces for UDP WS-Discovery</a> or <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">Inspecting Network Traces for Applications Using Directed Discovery</a></span></span></td>
<td><span data-ttu-id="7cda1-172">訊息的檢查會顯示 <strong>RelatesTo</strong> 元素包含格式錯誤或不正確的值。</span><span class="sxs-lookup"><span data-stu-id="7cda1-172">Inspection of the message shows that the <strong>RelatesTo</strong> element contains a malformed or incorrect value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cda1-173"><a href="probematches-message.md">ProbeMatches</a>訊息中包含的<strong>XAddrs</strong>元素不符合<a href="xaddr-validation-rules.md">XAddr 驗證規則</a>。</span><span class="sxs-lookup"><span data-stu-id="7cda1-173">The <strong>XAddrs</strong> element included in a <a href="probematches-message.md">ProbeMatches</a> message does not conform to the <a href="xaddr-validation-rules.md">XAddr Validation Rules</a>.</span></span></td>
<td><span data-ttu-id="7cda1-174"><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS 探索的網路追蹤，</a> 或 <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">使用導向探索檢查應用程式的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-174"><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecting Network Traces for UDP WS-Discovery</a> or <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">Inspecting Network Traces for Applications Using Directed Discovery</a></span></span></td>
<td><span data-ttu-id="7cda1-175">訊息的檢查會顯示 <strong>XAddrs</strong> 無效。</span><span class="sxs-lookup"><span data-stu-id="7cda1-175">Inspection of the message shows that the <strong>XAddrs</strong> are invalid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cda1-176">針對未使用導向探索) 的應用程式，UDP 多播不會將<a href="resolve-message.md">解決</a>訊息傳送到埠 3702 (。</span><span class="sxs-lookup"><span data-stu-id="7cda1-176"><a href="resolve-message.md">Resolve</a> messages are not sent by UDP multicast to port 3702 (for applications not using directed discovery).</span></span></td>
<td><span data-ttu-id="7cda1-177"><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS 探索的網路追蹤，</a> 或 <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">使用導向探索檢查應用程式的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-177"><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecting Network Traces for UDP WS-Discovery</a> or <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">Inspecting Network Traces for Applications Using Directed Discovery</a></span></span></td>
<td><span data-ttu-id="7cda1-178">檢查輸出會顯示 <a href="resolve-message.md">解析</a> 訊息已傳送至錯誤的埠。</span><span class="sxs-lookup"><span data-stu-id="7cda1-178">Inspection of the output shows that the <a href="resolve-message.md">Resolve</a> message was sent to the wrong port.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cda1-179"><a href="resolvematches-message.md">ResolveMatches</a>訊息未傳送給傳送了<a href="resolve-message.md">解析</a>訊息的 UDP 通訊埠。</span><span class="sxs-lookup"><span data-stu-id="7cda1-179">A <a href="resolvematches-message.md">ResolveMatches</a> message was not sent unicast to the UDP port from which a <a href="resolve-message.md">Resolve</a> message was sent.</span></span></td>
<td><span data-ttu-id="7cda1-180"><a href="inspecting-network-traces-for-udp-ws-discovery.md">檢查 UDP WS 探索的網路追蹤，</a> 或 <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">使用導向探索檢查應用程式的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-180"><a href="inspecting-network-traces-for-udp-ws-discovery.md">Inspecting Network Traces for UDP WS-Discovery</a> or <a href="inspecting-network-traces-for-applications-using-directed-discovery.md">Inspecting Network Traces for Applications Using Directed Discovery</a></span></span></td>
<td><span data-ttu-id="7cda1-181">檢查輸出會顯示未傳送任何 <a href="resolvematches-message.md">ResolveMatches</a> 訊息，或訊息已傳送至錯誤的埠。</span><span class="sxs-lookup"><span data-stu-id="7cda1-181">Inspection of the output shows that no <a href="resolvematches-message.md">ResolveMatches</a> message was sent or that the message was sent to the wrong port.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="metadata-exchange-problems"></a><span data-ttu-id="7cda1-182">中繼資料交換問題</span><span class="sxs-lookup"><span data-stu-id="7cda1-182">Metadata exchange problems</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7cda1-183">問題</span><span class="sxs-lookup"><span data-stu-id="7cda1-183">Problem</span></span></th>
<th><span data-ttu-id="7cda1-184">診斷程式</span><span class="sxs-lookup"><span data-stu-id="7cda1-184">Diagnostic Procedure</span></span></th>
<th><span data-ttu-id="7cda1-185">問題識別</span><span class="sxs-lookup"><span data-stu-id="7cda1-185">Problem identification</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cda1-186">主機所公告的傳輸位址錯誤。</span><span class="sxs-lookup"><span data-stu-id="7cda1-186">The transport address advertised by the host is wrong.</span></span></td>
<td><span data-ttu-id="7cda1-187"><a href="using-a-generic-host-and-client-for-http-metadata-exchange.md">使用泛型主機和用戶端進行 HTTP 中繼資料交換</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-187"><a href="using-a-generic-host-and-client-for-http-metadata-exchange.md">Using a Generic Host and Client for HTTP Metadata Exchange</a></span></span></td>
<td><span data-ttu-id="7cda1-188">在 WSD Debug 用戶端輸出中檢查 XAddrs，會顯示傳輸位址錯誤或格式不正確。</span><span class="sxs-lookup"><span data-stu-id="7cda1-188">Inspection of the XAddrs in the WSD Debug Client output shows that the transport address is wrong or malformed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cda1-189">無法建立中繼資料交換的 TCP 連接。</span><span class="sxs-lookup"><span data-stu-id="7cda1-189">A TCP connection could not be established for metadata exchange.</span></span></td>
<td><span data-ttu-id="7cda1-190"><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-190"><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecting Network Traces for HTTP Metadata Exchange</a></span></span></td>
<td><span data-ttu-id="7cda1-191">封包分析器的輸出不會顯示下列封包交換：</span><span class="sxs-lookup"><span data-stu-id="7cda1-191">The output from the packet analyzer does not show the following packet exchange:</span></span>
<ul>
<li><span data-ttu-id="7cda1-192">從用戶端傳送的 TCP SYN 封包</span><span class="sxs-lookup"><span data-stu-id="7cda1-192">A TCP SYN packet sent from the client</span></span></li>
<li><span data-ttu-id="7cda1-193">從主機傳送的 TCP SYN/ACK 封包</span><span class="sxs-lookup"><span data-stu-id="7cda1-193">A TCP SYN/ACK packet sent from the host</span></span></li>
<li><span data-ttu-id="7cda1-194">從用戶端傳送的 TCP ACK 封包</span><span class="sxs-lookup"><span data-stu-id="7cda1-194">A TCP ACK packet sent from the client</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cda1-195">用戶端未傳送有效的 HTTP GET 要求。</span><span class="sxs-lookup"><span data-stu-id="7cda1-195">The client did not send a valid HTTP GET request.</span></span></td>
<td><span data-ttu-id="7cda1-196"><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-196"><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecting Network Traces for HTTP Metadata Exchange</a></span></span></td>
<td><span data-ttu-id="7cda1-197">封包分析器輸出中沒有 HTTP GET 要求，或要求的格式不正確。</span><span class="sxs-lookup"><span data-stu-id="7cda1-197">There is no HTTP GET request in the packet analyzer output, or the request is malformed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cda1-198">用戶端未傳送有效的 WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">取得</a> 訊息。</span><span class="sxs-lookup"><span data-stu-id="7cda1-198">The client did not send a valid WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> message.</span></span></td>
<td><span data-ttu-id="7cda1-199"><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-199"><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecting Network Traces for HTTP Metadata Exchange</a></span></span></td>
<td><span data-ttu-id="7cda1-200">封包分析器輸出中沒有 WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">取得</a> 訊息，或訊息的格式不正確。</span><span class="sxs-lookup"><span data-stu-id="7cda1-200">There is no WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> message in the packet analyzer output, or the message is malformed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cda1-201">主機未接聽 HTTP GET 要求中指定的 URL 路徑。</span><span class="sxs-lookup"><span data-stu-id="7cda1-201">The host is not listening on the URL path specified in the HTTP GET request.</span></span></td>
<td><span data-ttu-id="7cda1-202"><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-202"><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecting Network Traces for HTTP Metadata Exchange</a></span></span></td>
<td><span data-ttu-id="7cda1-203">封包分析器輸出中沒有 HTTP 回應。</span><span class="sxs-lookup"><span data-stu-id="7cda1-203">There is no HTTP response in the packet analyzer output.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cda1-204">WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> 訊息未包含 <strong>to</strong> 元素，或 <strong>to</strong> 專案是空的。</span><span class="sxs-lookup"><span data-stu-id="7cda1-204">The WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> message does not contain a <strong>To</strong> element, or the <strong>To</strong> element is empty.</span></span></td>
<td><span data-ttu-id="7cda1-205"><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-205"><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecting Network Traces for HTTP Metadata Exchange</a></span></span></td>
<td><span data-ttu-id="7cda1-206">訊息的檢查會顯示 <strong>To</strong> 元素不存在或空白。</span><span class="sxs-lookup"><span data-stu-id="7cda1-206">Inspection of the message shows that the <strong>To</strong> element is not present or empty.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cda1-207">WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a>訊息的<strong>To</strong>元素值不符合其中一個主機端點位址。</span><span class="sxs-lookup"><span data-stu-id="7cda1-207">The value of the <strong>To</strong> element of a WS-Transfer <a href="get--metadata-exchange--http-request-and-message.md">Get</a> message does not match one of the host's endpoint addresses.</span></span></td>
<td><span data-ttu-id="7cda1-208"><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-208"><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecting Network Traces for HTTP Metadata Exchange</a></span></span></td>
<td><span data-ttu-id="7cda1-209">訊息的檢查會顯示 <strong>To</strong> 專案的值不符合主機 <a href="probematches-message.md">ProbeMatches</a> 或 <a href="resolvematches-message.md">ResolveMatches</a> 訊息中通告的其中一個端點位址。</span><span class="sxs-lookup"><span data-stu-id="7cda1-209">Inspection of the message shows that value of the <strong>To</strong> element does not match one of the endpoint addresses advertised in the host's <a href="probematches-message.md">ProbeMatches</a> or <a href="resolvematches-message.md">ResolveMatches</a> message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cda1-210">主機未傳送有效的 HTTP 回應標頭。</span><span class="sxs-lookup"><span data-stu-id="7cda1-210">The host did not send a valid HTTP response header.</span></span></td>
<td><span data-ttu-id="7cda1-211"><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-211"><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecting Network Traces for HTTP Metadata Exchange</a></span></span></td>
<td><span data-ttu-id="7cda1-212">封包分析器輸出中沒有 HTTP 回應，或要求的格式不正確。</span><span class="sxs-lookup"><span data-stu-id="7cda1-212">There is no HTTP response in the packet analyzer output, or the request is malformed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cda1-213">主機傳送的 HTTP 回應標頭表示無法完成要求。</span><span class="sxs-lookup"><span data-stu-id="7cda1-213">The HTTP response header sent by the host indicates that the request cannot be completed.</span></span></td>
<td><span data-ttu-id="7cda1-214"><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-214"><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecting Network Traces for HTTP Metadata Exchange</a></span></span></td>
<td><span data-ttu-id="7cda1-215">回應標頭具有 HTTP/1.1 200 以外的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="7cda1-215">The response header has a status code other than HTTP/1.1 200.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cda1-216">主機未傳送有效的 <a href="getresponse--metadata-exchange--message.md">GetResponse</a> 訊息。</span><span class="sxs-lookup"><span data-stu-id="7cda1-216">The host did not send a valid <a href="getresponse--metadata-exchange--message.md">GetResponse</a> message.</span></span></td>
<td><span data-ttu-id="7cda1-217"><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-217"><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecting Network Traces for HTTP Metadata Exchange</a></span></span></td>
<td><span data-ttu-id="7cda1-218">封包分析器輸出中沒有 <a href="getresponse--metadata-exchange--message.md">GetResponse</a> 訊息，或訊息的格式不正確。</span><span class="sxs-lookup"><span data-stu-id="7cda1-218">There is no <a href="getresponse--metadata-exchange--message.md">GetResponse</a> message in the packet analyzer output, or the message is malformed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cda1-219"><a href="getresponse--metadata-exchange--message.md">GetResponse</a>訊息未包含<strong>relatesto</strong>元素，或<strong>relatesto</strong>元素是空的。</span><span class="sxs-lookup"><span data-stu-id="7cda1-219">The <a href="getresponse--metadata-exchange--message.md">GetResponse</a> message does not contain a <strong>RelatesTo</strong> element, or the <strong>RelatesTo</strong> element is empty.</span></span></td>
<td><span data-ttu-id="7cda1-220"><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-220"><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecting Network Traces for HTTP Metadata Exchange</a></span></span></td>
<td><span data-ttu-id="7cda1-221">訊息的檢查會顯示 <strong>RelatesTo</strong> 元素不存在或空白。</span><span class="sxs-lookup"><span data-stu-id="7cda1-221">Inspection of the message shows that the <strong>RelatesTo</strong> element is not present or empty.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cda1-222"><a href="getresponse--metadata-exchange--message.md">GetResponse</a>訊息中的<strong>RelatesTo</strong>元素值與對應的<a href="get--metadata-exchange--http-request-and-message.md">Get</a>訊息中的<strong>MessageId</strong>元素值不相符。</span><span class="sxs-lookup"><span data-stu-id="7cda1-222">The value of the <strong>RelatesTo</strong> element in a <a href="getresponse--metadata-exchange--message.md">GetResponse</a> message does not match the value of the <strong>MessageId</strong> element from the corresponding <a href="get--metadata-exchange--http-request-and-message.md">Get</a> message.</span></span></td>
<td><span data-ttu-id="7cda1-223"><a href="inspecting-network-traces-for-http-metadata-exchange.md">檢查 HTTP 中繼資料交換的網路追蹤</a></span><span class="sxs-lookup"><span data-stu-id="7cda1-223"><a href="inspecting-network-traces-for-http-metadata-exchange.md">Inspecting Network Traces for HTTP Metadata Exchange</a></span></span></td>
<td><span data-ttu-id="7cda1-224">訊息的檢查會顯示 <strong>RelatesTo</strong> 元素包含格式錯誤或不正確的值。</span><span class="sxs-lookup"><span data-stu-id="7cda1-224">Inspection of the message shows that the <strong>RelatesTo</strong> element contains a malformed or incorrect value.</span></span></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a><span data-ttu-id="7cda1-225">相關主題</span><span class="sxs-lookup"><span data-stu-id="7cda1-225">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cda1-226">WSDAPI 疑難排解指南</span><span class="sxs-lookup"><span data-stu-id="7cda1-226">WSDAPI Troubleshooting Guide</span></span>](wsdapi-troubleshooting-guide.md)
</dt> </dl>
