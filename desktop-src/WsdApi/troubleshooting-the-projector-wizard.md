---
description: 列出針對投影機 Wizard 進行疑難排解時要使用的診斷程式。
ms.assetid: 54efc88c-0b8e-4652-8655-817a288863d1
title: 針對投影機 Wizard 進行疑難排解
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3776e86d3a156fa86873900aa9e804df9830ec64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972405"
---
# <a name="troubleshooting-the-projector-wizard"></a><span data-ttu-id="28183-103">針對投影機 Wizard 進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="28183-103">Troubleshooting the Projector Wizard</span></span>

<span data-ttu-id="28183-104">投影機 Wizard：</span><span class="sxs-lookup"><span data-stu-id="28183-104">The Projector Wizard:</span></span>

-   <span data-ttu-id="28183-105">一律使用 UDP WS-Discovery 進行裝置探索</span><span class="sxs-lookup"><span data-stu-id="28183-105">Always uses UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="28183-106">一律使用 HTTP 進行中繼資料交換</span><span class="sxs-lookup"><span data-stu-id="28183-106">Always uses HTTP for metadata exchange</span></span>
-   <span data-ttu-id="28183-107">有時會使用導向的探索</span><span class="sxs-lookup"><span data-stu-id="28183-107">Sometimes uses directed discovery</span></span>

<span data-ttu-id="28183-108">下列診斷程式應依序 (使用，) 協助您找出投影機 Wizard 的問題。</span><span class="sxs-lookup"><span data-stu-id="28183-108">The following diagnostic procedures should be used (in order) to help identify problems with the Projector Wizard.</span></span>

<span data-ttu-id="28183-109">**針對投影機 Wizard 進行疑難排解**</span><span class="sxs-lookup"><span data-stu-id="28183-109">**To troubleshoot the Projector Wizard**</span></span>

1.  <span data-ttu-id="28183-110">如果使用導向探索，請 [針對導向探索進行疑難排解](troubleshooting-applications-using-directed-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="28183-110">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="28183-111">[檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="28183-111">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="28183-112">[使用泛型主機和用戶端進行 UDP WS 探索](using-a-generic-host-and-client-for-udp-ws-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="28183-112">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="28183-113">[使用 WSD Debug 用戶端來驗證多播流量](using-wsddebug-client-to-verify-multicast-traffic.md)。</span><span class="sxs-lookup"><span data-stu-id="28183-113">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="28183-114">[檢查 UDP WS-探索的網路追蹤](inspecting-network-traces-for-udp-ws-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="28183-114">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="28183-115">[使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="28183-115">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="28183-116">[使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)。</span><span class="sxs-lookup"><span data-stu-id="28183-116">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="28183-117">[檢查 HTTP 中繼資料交換的網路追蹤](inspecting-network-traces-for-http-metadata-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="28183-117">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="28183-118">如果無法使用上述診斷程式來識別問題的來源，請遵循 [啟用 WSDAPI 追蹤](enabling-wsdapi-tracing.md) 並聯絡 Microsoft 支援服務的指示。</span><span class="sxs-lookup"><span data-stu-id="28183-118">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28183-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="28183-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28183-120">使用 WSDAPI 進行疑難排解的開始使用</span><span class="sxs-lookup"><span data-stu-id="28183-120">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



