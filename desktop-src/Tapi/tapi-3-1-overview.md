---
description: TAPI 3.1 版是以 COM 為基礎的 API，可合併傳統和 IP 電話語音。 可能的應用程式範圍從使用公用交換器電話網絡的簡單語音通話 (PSTN) 到具有服務品質 (QOS) 的多播多媒體 IP 會議。
ms.assetid: 1f7ccef8-5aad-48e7-90e9-a378dd83a870
title: TAPI 3.1 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30b70ccdc1c4a0985107d2bd2fc36bfbe4e3fca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983487"
---
# <a name="tapi-31-overview"></a><span data-ttu-id="68ac1-104">TAPI 3.1 總覽</span><span class="sxs-lookup"><span data-stu-id="68ac1-104">TAPI 3.1 Overview</span></span>

<span data-ttu-id="68ac1-105">TAPI 3.1 版是以 COM 為基礎的 API，可合併傳統和 IP 電話語音。</span><span class="sxs-lookup"><span data-stu-id="68ac1-105">TAPI version 3.1 is a COM-based API that merges classic and IP telephony.</span></span> <span data-ttu-id="68ac1-106">可能的應用程式範圍從使用公用交換器電話網絡的簡單語音通話 (PSTN) 到具有服務品質 (QOS) 的多播多媒體 IP 會議。</span><span class="sxs-lookup"><span data-stu-id="68ac1-106">Possible applications range from simple voice calls over the Public Switched Telephone Network (PSTN) to multicast multimedia IP conferencing with quality of service (QOS).</span></span>

<span data-ttu-id="68ac1-107">如需有關 TAPI 3.1 IP 電話語音功能的詳細資訊，請參閱 Microsoft 網站上的「使用 TAPI 3 的 IP 電話語音」白皮書。</span><span class="sxs-lookup"><span data-stu-id="68ac1-107">For additional information on TAPI 3.1 IP Telephony capabilities, please consult the "IP Telephony with TAPI 3" white paper, which can be found on the Microsoft web site.</span></span>

<span data-ttu-id="68ac1-108">TAPI 3.1 有四個主要元件：</span><span class="sxs-lookup"><span data-stu-id="68ac1-108">There are four major components to TAPI 3.1:</span></span>

-   <span data-ttu-id="68ac1-109">COM API</span><span class="sxs-lookup"><span data-stu-id="68ac1-109">COM API</span></span>
-   <span data-ttu-id="68ac1-110">TAPI 伺服器</span><span class="sxs-lookup"><span data-stu-id="68ac1-110">TAPI Server</span></span>
-   <span data-ttu-id="68ac1-111">電話語音服務提供者 (Tsp) </span><span class="sxs-lookup"><span data-stu-id="68ac1-111">Telephony Service Providers (TSPs)</span></span>
-   <span data-ttu-id="68ac1-112">媒體串流提供者 (Msp) </span><span class="sxs-lookup"><span data-stu-id="68ac1-112">Media Stream Providers (MSPs)</span></span>

<span data-ttu-id="68ac1-113">下圖說明 TAPI 3.1 架構：</span><span class="sxs-lookup"><span data-stu-id="68ac1-113">The following diagram illustrates the TAPI 3.1 architecture:</span></span>

![tapi 3 架構](images/callarc-gif-1.png)

<span data-ttu-id="68ac1-115">API 會實作為元件物件模型的套件， (COM) 物件。</span><span class="sxs-lookup"><span data-stu-id="68ac1-115">The API is implemented as a suite of Component Object Model (COM) objects.</span></span> <span data-ttu-id="68ac1-116">將 TAPI 移至物件導向 COM 模型，可讓開發人員以許多語言撰寫啟用 TAPI 的應用程式，例如 JAVA、Visual Basic 或 C/c + +。</span><span class="sxs-lookup"><span data-stu-id="68ac1-116">Moving TAPI to the object-oriented COM model allows developers to write TAPI-enabled applications in many languages, such as Java, Visual Basic, or C/C++.</span></span> <span data-ttu-id="68ac1-117">使用 COM 可讓元件升級 TAPI 功能。</span><span class="sxs-lookup"><span data-stu-id="68ac1-117">Use of COM enables component upgrades of TAPI features.</span></span>

<span data-ttu-id="68ac1-118">TAPI 伺服器程式 (TAPISRV) 將 TAPI 服務提供者介面從 TAPI 3.x 和 TAPI 2.x (TSPI) ，讓 TAPI 2.x 的電話語音服務提供者可以與 TAPI 3.x 搭配使用，以維護 TAPI 的內部狀態。</span><span class="sxs-lookup"><span data-stu-id="68ac1-118">The TAPI Server process (TAPISRV) abstracts the TAPI Service Provider Interface (TSPI) from TAPI 3.x and TAPI 2.x, allowing TAPI 2.x Telephony Service Providers to be used with TAPI 3.x, maintaining the internal state of TAPI.</span></span> <span data-ttu-id="68ac1-119">TAPISRV 會實作為 SVCHOST 內的服務進程。</span><span class="sxs-lookup"><span data-stu-id="68ac1-119">TAPISRV is implemented as a service process within SVCHOST.</span></span>

<span data-ttu-id="68ac1-120">[服務提供者](./tapi-service-providers.md) 會抽象化提供者特定的媒體傳輸機制。</span><span class="sxs-lookup"><span data-stu-id="68ac1-120">[Service Providers](./tapi-service-providers.md) abstract provider-specific media transport mechanisms.</span></span> <span data-ttu-id="68ac1-121">它們通常會成對存在–電話語音服務提供者 (TSP) 用於通話控制和媒體服務提供者 (適用于媒體控制的 MSP) 。</span><span class="sxs-lookup"><span data-stu-id="68ac1-121">They typically exist in pairs – a Telephony Service Provider (TSP) for call control and a Media Service Provider (MSP) for media control.</span></span>

<span data-ttu-id="68ac1-122">[電話語音服務提供者](./telephony-service-providers-start-page.md) (tsp) 負責將 TAPI 的通訊協定獨立呼叫模型解析為通訊協定特定的呼叫控制機制。</span><span class="sxs-lookup"><span data-stu-id="68ac1-122">[Telephony Service Providers](./telephony-service-providers-start-page.md) (TSPs) are responsible for resolving the protocol-independent call model of TAPI into protocol-specific call control mechanisms.</span></span> <span data-ttu-id="68ac1-123">TAPI 3.1 提供與 TAPI 2.1 Tsp 的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="68ac1-123">TAPI 3.1 provides backward compatibility with TAPI 2.1 TSPs.</span></span> <span data-ttu-id="68ac1-124"> (的兩個 IP 電話語音服務提供者和其相關聯的 Msp) 預設隨附于 TAPI 3.1：-323 TSP 和 IP 多播會議 TSP。</span><span class="sxs-lookup"><span data-stu-id="68ac1-124">Two IP Telephony service providers (and their associated MSPs) ship by default with TAPI 3.1: the H.323 TSP and the IP Multicast Conferencing TSP.</span></span>

<span data-ttu-id="68ac1-125">[媒體服務提供者](media-service-providers-start-page.md) (msp) 提供統一的方式來存取通話中的媒體串流，支援 DirectShow<sup>TM</sup> API 作為主要媒體串流處理常式。</span><span class="sxs-lookup"><span data-stu-id="68ac1-125">[Media Service Providers](media-service-providers-start-page.md) (MSPs) provide a uniform way to access the media streams in a call, supporting the DirectShow<sup>TM</sup> API as the primary media stream handler.</span></span> <span data-ttu-id="68ac1-126">TAPI Msp 會針對特定的 TSP 實行 DirectShow 介面，且所有使用 DirectShow 串流的電話語音服務都需要這些介面。</span><span class="sxs-lookup"><span data-stu-id="68ac1-126">TAPI MSPs implement DirectShow interfaces for a particular TSP and are required for any telephony service that makes use of DirectShow streaming.</span></span> <span data-ttu-id="68ac1-127">一般資料流程是由應用程式處理。</span><span class="sxs-lookup"><span data-stu-id="68ac1-127">Generic streams are handled by the application.</span></span>

 

 
