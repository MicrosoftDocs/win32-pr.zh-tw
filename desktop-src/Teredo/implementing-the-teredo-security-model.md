---
title: 執行 Teredo 安全性模型
description: Teredo 安全性模型是以 windows Vista 內建的 Windows 篩選平台 (WFP) 技術為基礎。 因此，建議協力廠商防火牆使用 WFP 來強制執行 Teredo 安全性模型。
ms.assetid: ee81e5f1-e3e0-440e-a53f-2accced476bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a39668f8e1c86e0cd5b12056df5eb9a5fd9cd3ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682795"
---
# <a name="implementing-the-teredo-security-model"></a><span data-ttu-id="41245-104">執行 Teredo 安全性模型</span><span class="sxs-lookup"><span data-stu-id="41245-104">Implementing the Teredo Security Model</span></span>

<span data-ttu-id="41245-105">Teredo 安全性模型是以 windows Vista 內建的 [Windows 篩選平台](/windows/desktop/FWP/windows-filtering-platform-start-page) (WFP) 技術為基礎。</span><span class="sxs-lookup"><span data-stu-id="41245-105">The Teredo security model is based on the [Windows Filtering Platform](/windows/desktop/FWP/windows-filtering-platform-start-page) (WFP) technology built into Windows Vista.</span></span> <span data-ttu-id="41245-106">因此，建議協力廠商防火牆使用 WFP 來強制執行 [Teredo](about-teredo.md) 安全性模型。</span><span class="sxs-lookup"><span data-stu-id="41245-106">As a result, it is recommended that third-party firewalls use WFP to enforce the [Teredo](about-teredo.md) security model.</span></span>

<span data-ttu-id="41245-107">[Teredo 安全性模型](the-teredo-security-model.md)的一般執行需要下列各項：</span><span class="sxs-lookup"><span data-stu-id="41245-107">The general implementation of the [Teredo Security Model](the-teredo-security-model.md) requires the following:</span></span>

-   <span data-ttu-id="41245-108">具備 IPv6 功能的主機防火牆必須向電腦上的 Windows 安全性 Center (WSC) 註冊。</span><span class="sxs-lookup"><span data-stu-id="41245-108">An IPv6-capable host firewall must be registered with Windows Security Center (WSC) on the machine.</span></span> <span data-ttu-id="41245-109">如果沒有以主機為基礎的防火牆或 WSC 本身，Teredo 介面將無法供使用。</span><span class="sxs-lookup"><span data-stu-id="41245-109">In the absence of a host-based firewall, or WSC itself, the Teredo interface will not be available for use.</span></span> <span data-ttu-id="41245-110">這是透過 Teredo 介面接收來自網際網路之要求流量的唯一需求。</span><span class="sxs-lookup"><span data-stu-id="41245-110">This is the only requirement to receive solicited traffic from the Internet over the Teredo interface.</span></span>
-   <span data-ttu-id="41245-111">任何透過 Teredo 介面接收來自網際網路之未經要求流量的應用程式，都必須先向具備 IPv6 功能的防火牆註冊，例如 [Windows 防火牆](/previous-versions/windows/desktop/ics/windows-firewall-start-page)，才能接收未受要求的流量。</span><span class="sxs-lookup"><span data-stu-id="41245-111">Any application that receives unsolicited traffic from the Internet over the Teredo interface must register with an IPv6-capable firewall, like [Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page), before receiving the unsolicited traffic.</span></span>

<span data-ttu-id="41245-112">如果未在 Teredo 介面上傳送或接收流量超過一小時，且符合未要求流量所需安全性準則的應用程式未執行或未開啟接聽通訊端，Teredo 位址將會變成休眠狀態。</span><span class="sxs-lookup"><span data-stu-id="41245-112">A Teredo address will become dormant if traffic has not been sent or received over the Teredo interface for one hour and if applications that meet the required security criteria for unsolicited traffic are not running or do not have listening sockets open.</span></span>

<span data-ttu-id="41245-113">在機器重新開機之後，或如果 Teredo 位址失去其資格，Windows Vista 會自動限定該位址，並在應用程式系結至具備 IPv6 功能的通訊端時，讓它可以立即使用。</span><span class="sxs-lookup"><span data-stu-id="41245-113">After the reboot of a machine, or if the Teredo address loses its qualifications, Windows Vista will automatically qualify the address and makes it available for use as soon as an application binds to IPv6-capable sockets.</span></span> <span data-ttu-id="41245-114">務必要注意的是，應用程式所設定的 Windows 防火牆「Edge 遍歷」選項，允許透過 Teredo 的未經要求流量在重新開機時持續存在。</span><span class="sxs-lookup"><span data-stu-id="41245-114">It is important to note that the Windows Firewall "Edge Traversal" option set by an application to allow unsolicited traffic via Teredo is persistent across reboots.</span></span>

## <a name="firewall-requirements-for-teredo"></a><span data-ttu-id="41245-115">Teredo 的防火牆需求</span><span class="sxs-lookup"><span data-stu-id="41245-115">Firewall Requirements for Teredo</span></span>

<span data-ttu-id="41245-116">防火牆廠商可以輕鬆地在其產品中併入 Teredo 支援，並使用 Windows 篩選平台的功能保護其使用者。</span><span class="sxs-lookup"><span data-stu-id="41245-116">Firewall vendors can easily incorporate Teredo support in their products and protect their users by using the capabilities of the Windows Filtering Platform.</span></span> <span data-ttu-id="41245-117">這可以藉由向 Windows 安全性中心註冊具備 IPv6 功能的防火牆、將適當的規則新增至 WFP Teredo 子層，以及在 Windows 中使用內建 Api 來列舉可能會透過 Teredo 接聽未經要求之流量的應用程式來完成。</span><span class="sxs-lookup"><span data-stu-id="41245-117">This can be accomplished by registering the IPv6-capable firewall with the Windows Security Center, adding appropriate rules into the WFP Teredo sublayer, and using built-in APIs in Windows to enumerate applications that might listen to unsolicited traffic over Teredo.</span></span> <span data-ttu-id="41245-118">在應用程式不需要透過 Teredo 接聽要求流量的情況下，防火牆不需要將其他規則新增至 WFP。</span><span class="sxs-lookup"><span data-stu-id="41245-118">In situations where an application does not need to listen to solicited traffic over Teredo, firewalls do not require additional rules added to the WFP.</span></span> <span data-ttu-id="41245-119">不過，具備 Windows 安全性中心的 IPv6 可用防火牆註冊，仍然需要讓 Teredo 位址可供使用。</span><span class="sxs-lookup"><span data-stu-id="41245-119">However an IPv6 capable firewall registration with Windows Security Center is still a requirement to make the Teredo address to available for use.</span></span>

<span data-ttu-id="41245-120">為了支援此案例，防火牆必須具備 IPv6 功能，並向 Windows 安全性中心註冊。</span><span class="sxs-lookup"><span data-stu-id="41245-120">In order to support this scenario, the firewall must be IPv6-capable and registered with the Windows Security Center.</span></span> <span data-ttu-id="41245-121">此外，防火牆不能變更 Windows 安全性 Center 服務 (wscsvc) 的執行中或啟動狀態，因為 Teredo 相依于透過 WSC Api 提供的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="41245-121">Additionally, the firewall must not change the running or startup state of the Windows Security Center service (wscsvc), as Teredo is dependent on the state information provided through the WSC APIs.</span></span>

<span data-ttu-id="41245-122">用來向 WSC 註冊防火牆的 API 可透過與 Microsoft 聯絡來取得 wscisv@microsoft.com 。</span><span class="sxs-lookup"><span data-stu-id="41245-122">The API utilized to register a firewall with the WSC can be obtained by contacting Microsoft at wscisv@microsoft.com.</span></span> <span data-ttu-id="41245-123">基於安全性考慮，必須有 (NDA) 的保密合約，才能洩漏此 API。</span><span class="sxs-lookup"><span data-stu-id="41245-123">A Non-Disclosure Agreement (NDA) is required for the disclosure of this API due to security concerns.</span></span>

<span data-ttu-id="41245-124">下列檔詳細說明使用的篩選準則和例外狀況，以確保與 Teredo 的最佳相容性：</span><span class="sxs-lookup"><span data-stu-id="41245-124">The following documentation details the filters and exceptions utilized to ensure optimal compatibility with Teredo:</span></span>

-   [<span data-ttu-id="41245-125">執行 Teredo 的防火牆篩選器</span><span class="sxs-lookup"><span data-stu-id="41245-125">Implementing Firewall Filters for Teredo</span></span>](implementing-firewall-filters-for-teredo.md)
-   [<span data-ttu-id="41245-126">Teredo 的必要防火牆例外</span><span class="sxs-lookup"><span data-stu-id="41245-126">Required Firewall Exceptions for Teredo</span></span>](required-firewall-exceptions-for-teredo.md)
-   [<span data-ttu-id="41245-127">Teredo 需要的 Windows 篩選平台例外狀況</span><span class="sxs-lookup"><span data-stu-id="41245-127">Required Windows Filtering Platform Exceptions for Teredo</span></span>](required-windows-filtering-platform-exceptions-for-teredo.md)

## <a name="firewall-requirements-for-other-ipv6-transition-technologies"></a><span data-ttu-id="41245-128">其他 IPv6 轉換技術的防火牆需求</span><span class="sxs-lookup"><span data-stu-id="41245-128">Firewall Requirements for Other IPv6 Transition Technologies</span></span>

<span data-ttu-id="41245-129">為了支援其他 IPv6 轉換技術 (例如6to4 和 ISATAP) ，主機防火牆產品必須能夠處理 IPv6 流量。</span><span class="sxs-lookup"><span data-stu-id="41245-129">In order to support other IPv6 transition technologies (such as 6to4 and ISATAP), the host firewall product must be capable of processing IPv6 traffic.</span></span> <span data-ttu-id="41245-130">IP 通訊協定41表示 IPv6 標頭在 IPv4 標頭之後。</span><span class="sxs-lookup"><span data-stu-id="41245-130">The IP Protocol 41 indicates when an IPv6 header follows an IPv4 header.</span></span> <span data-ttu-id="41245-131">當主機防火牆遇到通訊協定41時，必須辨識封包是 IPv6 封裝的封包，因此必須適當地處理封包，並根據其原則中的 IPv6 規則進行接受/拒絕決策。</span><span class="sxs-lookup"><span data-stu-id="41245-131">When a host firewall encounters protocol 41, it must recognize that the packet is an IPv6-encapsulated packet and as a result must process the packet appropriately and make the accept/deny decisions based on the IPv6 rules in its policy.</span></span>

 

 