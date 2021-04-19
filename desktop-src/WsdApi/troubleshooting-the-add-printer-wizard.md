---
description: 列出針對 [新增印表機嚮導] 進行疑難排解時要使用的診斷程式。
ms.assetid: 3ffee09b-e980-4a14-97ad-270444457dd7
title: 針對新增印表機嚮導進行疑難排解
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b0054758e3ec721598ad279a073a32862af368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979079"
---
# <a name="troubleshooting-the-add-printer-wizard"></a><span data-ttu-id="bc56b-103">針對新增印表機嚮導進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="bc56b-103">Troubleshooting the Add Printer Wizard</span></span>

<span data-ttu-id="bc56b-104">[新增印表機] 嚮導：</span><span class="sxs-lookup"><span data-stu-id="bc56b-104">The Add Printer Wizard:</span></span>

-   <span data-ttu-id="bc56b-105">一律使用 UDP WS-Discovery 進行裝置探索</span><span class="sxs-lookup"><span data-stu-id="bc56b-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="bc56b-106">一律起始中繼資料交換的 HTTP 或 HTTPS 連接</span><span class="sxs-lookup"><span data-stu-id="bc56b-106">Always initiates a HTTP or HTTPS connection for metadata exchange</span></span>
-   <span data-ttu-id="bc56b-107">有時會使用導向的探索</span><span class="sxs-lookup"><span data-stu-id="bc56b-107">Sometimes uses directed discovery</span></span>
-   <span data-ttu-id="bc56b-108">有時會使用安全通道 (HTTPS) 進行中繼資料交換</span><span class="sxs-lookup"><span data-stu-id="bc56b-108">Sometimes uses a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="bc56b-109">下列診斷程式應依序 (使用，) 協助您找出 [新增印表機嚮導] 的問題。</span><span class="sxs-lookup"><span data-stu-id="bc56b-109">The following diagnostic procedures should be used (in order) to help identify problems with the Add Printer Wizard.</span></span>

<span data-ttu-id="bc56b-110">**若要針對新增印表機嚮導進行疑難排解**</span><span class="sxs-lookup"><span data-stu-id="bc56b-110">**To troubleshoot the Add Printer Wizard**</span></span>

1.  <span data-ttu-id="bc56b-111">如果使用導向探索，請 [針對導向探索進行疑難排解](troubleshooting-applications-using-directed-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="bc56b-111">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="bc56b-112">[檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="bc56b-112">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="bc56b-113">[使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="bc56b-113">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="bc56b-114">[使用 WSD Debug 用戶端來驗證多播流量](using-wsddebug-client-to-verify-multicast-traffic.md)。</span><span class="sxs-lookup"><span data-stu-id="bc56b-114">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="bc56b-115">[檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="bc56b-115">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="bc56b-116">[使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="bc56b-116">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="bc56b-117">[使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)。</span><span class="sxs-lookup"><span data-stu-id="bc56b-117">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="bc56b-118">[檢查 HTTP 中繼資料交換的網路追蹤](inspecting-network-traces-for-http-metadata-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="bc56b-118">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="bc56b-119">如果無法使用上述診斷程式來識別問題的來源，請遵循 [啟用 WSDAPI 追蹤](enabling-wsdapi-tracing.md) 並聯絡 Microsoft 支援服務的指示。</span><span class="sxs-lookup"><span data-stu-id="bc56b-119">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc56b-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="bc56b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc56b-121">使用 WSDAPI 進行疑難排解的開始使用</span><span class="sxs-lookup"><span data-stu-id="bc56b-121">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="bc56b-122">使用導向探索針對應用程式進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="bc56b-122">Troubleshooting Applications Using Directed Discovery</span></span>](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 



