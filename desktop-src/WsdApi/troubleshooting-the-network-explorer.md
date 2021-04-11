---
description: 列出針對網路總管進行疑難排解時要使用的診斷程式。
ms.assetid: 56052a82-d3a6-4749-9010-6796558dcb17
title: 疑難排解網路總管
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09afe7acbcb20d706c8645d84c68014b0e33d799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943415"
---
# <a name="troubleshooting-the-network-explorer"></a><span data-ttu-id="6da56-103">疑難排解網路總管</span><span class="sxs-lookup"><span data-stu-id="6da56-103">Troubleshooting the Network Explorer</span></span>

<span data-ttu-id="6da56-104">網路總管：</span><span class="sxs-lookup"><span data-stu-id="6da56-104">The Network Explorer:</span></span>

-   <span data-ttu-id="6da56-105">一律使用 UDP WS-Discovery 進行裝置探索</span><span class="sxs-lookup"><span data-stu-id="6da56-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="6da56-106">一律起始中繼資料交換的 HTTP 或 HTTPS 連接</span><span class="sxs-lookup"><span data-stu-id="6da56-106">Always initiates a HTTP or HTTPS connection for metadata exchange</span></span>
-   <span data-ttu-id="6da56-107">有時會使用安全通道 (HTTPS) 進行中繼資料交換</span><span class="sxs-lookup"><span data-stu-id="6da56-107">Sometimes uses a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="6da56-108">下列診斷程式應依序 (使用) ，以協助找出網路總管的問題。</span><span class="sxs-lookup"><span data-stu-id="6da56-108">The following diagnostic procedures should be used (in order) to help identify problems with the Network Explorer.</span></span>

<span data-ttu-id="6da56-109">**若要疑難排解網路總管**</span><span class="sxs-lookup"><span data-stu-id="6da56-109">**To troubleshoot the Network Explorer**</span></span>

1.  <span data-ttu-id="6da56-110">[檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="6da56-110">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
2.  <span data-ttu-id="6da56-111">[使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="6da56-111">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
3.  <span data-ttu-id="6da56-112">[使用 WSD Debug 用戶端來驗證多播流量](using-wsddebug-client-to-verify-multicast-traffic.md)。</span><span class="sxs-lookup"><span data-stu-id="6da56-112">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
4.  <span data-ttu-id="6da56-113">[檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="6da56-113">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
5.  <span data-ttu-id="6da56-114">[使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="6da56-114">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
6.  <span data-ttu-id="6da56-115">[使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)。</span><span class="sxs-lookup"><span data-stu-id="6da56-115">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
7.  <span data-ttu-id="6da56-116">[檢查 HTTP 中繼資料交換的網路追蹤](inspecting-network-traces-for-http-metadata-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="6da56-116">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="6da56-117">網路總管使用 [函數探索](/previous-versions/windows/desktop/fundisc/fd-portal) 來列舉網路裝置。</span><span class="sxs-lookup"><span data-stu-id="6da56-117">The Network Explorer uses [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) to enumerate network devices.</span></span> <span data-ttu-id="6da56-118">如需疑難排解的詳細資訊，請參閱 [疑難排解函數探索用戶端](troubleshooting-function-discovery-clients.md)。</span><span class="sxs-lookup"><span data-stu-id="6da56-118">For more troubleshooting information, see [Troubleshooting Function Discovery Clients](troubleshooting-function-discovery-clients.md).</span></span>

<span data-ttu-id="6da56-119">如果無法使用上述診斷程式來識別問題的來源，請遵循 [啟用 WSDAPI 追蹤](enabling-wsdapi-tracing.md) 並聯絡 Microsoft 支援服務的指示。</span><span class="sxs-lookup"><span data-stu-id="6da56-119">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6da56-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="6da56-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6da56-121">使用 WSDAPI 進行疑難排解的開始使用</span><span class="sxs-lookup"><span data-stu-id="6da56-121">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="6da56-122">針對函數探索用戶端進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="6da56-122">Troubleshooting Function Discovery Clients</span></span>](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 
