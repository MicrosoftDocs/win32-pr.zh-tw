---
description: 使用導向探索的應用程式會透過 HTTP 或 HTTPS 傳送探查訊息以探索裝置。
ms.assetid: 599f5962-da91-4688-b333-a784f06581ed
title: 使用導向探索針對 WSDAPI 應用程式進行疑難排解
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34ebec44c58545c65a4ff04941c5f98c9bc047d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513044"
---
# <a name="troubleshooting-wsdapi-applications-using-directed-discovery"></a><span data-ttu-id="d6f32-103">使用導向探索針對 WSDAPI 應用程式進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="d6f32-103">Troubleshooting WSDAPI Applications Using Directed Discovery</span></span>

<span data-ttu-id="d6f32-104">使用導向探索的應用程式會透過 HTTP 或 HTTPS 傳送 [探查](probe-message.md) 訊息以探索裝置。</span><span class="sxs-lookup"><span data-stu-id="d6f32-104">Applications that use directed discovery send [Probe](probe-message.md) messages over HTTP or HTTPS to discover devices.</span></span> <span data-ttu-id="d6f32-105">在回應中傳送的對應 [ProbeMatches](probematches-message.md) 訊息也會透過 HTTP 或 HTTPS 傳送。</span><span class="sxs-lookup"><span data-stu-id="d6f32-105">The corresponding [ProbeMatches](probematches-message.md) messages sent in response are also sent over HTTP or HTTPS.</span></span> <span data-ttu-id="d6f32-106">[新增印表機嚮導]、[函式探索用戶端] 或 [WSDAPI 應用程式] 可以起始導向探索。</span><span class="sxs-lookup"><span data-stu-id="d6f32-106">Directed discovery can be initiated by the Add Printer Wizard, a Function Discovery client, or a WSDAPI application.</span></span> <span data-ttu-id="d6f32-107">探查和 ProbeMatches 訊息的結構與透過 UDP 傳送的訊息相同。</span><span class="sxs-lookup"><span data-stu-id="d6f32-107">The Probe and ProbeMatches messages are structurally identical to those sent over UDP.</span></span> <span data-ttu-id="d6f32-108">訊息前面會加上適當的 HTTP 或 HTTPS 標頭。</span><span class="sxs-lookup"><span data-stu-id="d6f32-108">The messages are prefixed with the appropriate HTTP or HTTPS headers.</span></span>

<span data-ttu-id="d6f32-109">下列診斷程式應依序 (使用，) 協助您使用導向探索來識別應用程式的問題。</span><span class="sxs-lookup"><span data-stu-id="d6f32-109">The following diagnostic procedures should be used (in order) to help identify problems with an application using directed discovery.</span></span>

<span data-ttu-id="d6f32-110">**使用導向探索針對 WSDAPI 應用程式進行疑難排解**</span><span class="sxs-lookup"><span data-stu-id="d6f32-110">**To troubleshoot a WSDAPI application using directed discovery**</span></span>

1.  <span data-ttu-id="d6f32-111">[檢查介面卡和防火牆設定](inspecting-adapter-and-firewall-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="d6f32-111">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
2.  <span data-ttu-id="d6f32-112">[使用泛型主機和用戶端進行 HTTP 中繼資料交換](using-a-generic-host-and-client-for-http-metadata-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="d6f32-112">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
3.  <span data-ttu-id="d6f32-113">[使用 WinHTTP 記錄來確認取得流量](using-winhttp-logging-to-verify-get-traffic.md)。</span><span class="sxs-lookup"><span data-stu-id="d6f32-113">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
4.  <span data-ttu-id="d6f32-114">[使用導向探索來檢查應用程式的網路追蹤](inspecting-network-traces-for-applications-using-directed-discovery.md)。</span><span class="sxs-lookup"><span data-stu-id="d6f32-114">[Inspect network traces for an application using directed discovery](inspecting-network-traces-for-applications-using-directed-discovery.md).</span></span>

<span data-ttu-id="d6f32-115">如果無法使用上述診斷程式來識別問題的來源，請遵循 [啟用 WSDAPI 追蹤](enabling-wsdapi-tracing.md) 並聯絡 Microsoft 支援服務的指示。</span><span class="sxs-lookup"><span data-stu-id="d6f32-115">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6f32-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="d6f32-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6f32-117">使用 WSDAPI 進行疑難排解的開始使用</span><span class="sxs-lookup"><span data-stu-id="d6f32-117">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="d6f32-118">針對新增印表機嚮導進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="d6f32-118">Troubleshooting the Add Printer Wizard</span></span>](troubleshooting-the-add-printer-wizard.md)
</dt> <dt>

[<span data-ttu-id="d6f32-119">針對 WSDAPI 應用程式進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="d6f32-119">Troubleshooting WSDAPI Applications</span></span>](troubleshooting-wsdapi-applications.md)
</dt> </dl>

 

 



