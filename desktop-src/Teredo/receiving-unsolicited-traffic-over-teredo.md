---
title: 透過 Teredo 接收未經要求的流量
description: Teredo 使用 IPv6 和 NAT 的遍歷功能提供全球連線能力。
ms.assetid: 0c03d1bb-15f8-4e77-9a96-e182b1d190ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5c7ffe7b84cfa325b3ecd8c0858ad96445e629
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682793"
---
# <a name="receiving-unsolicited-traffic-over-teredo"></a><span data-ttu-id="442bc-103">透過 Teredo 接收未經要求的流量</span><span class="sxs-lookup"><span data-stu-id="442bc-103">Receiving Unsolicited Traffic Over Teredo</span></span>

<span data-ttu-id="442bc-104">[Teredo](about-teredo.md) 使用 IPV6 和 NAT 的遍歷功能提供全球連線能力。</span><span class="sxs-lookup"><span data-stu-id="442bc-104">[Teredo](about-teredo.md) provides global connectivity using IPv6 and NAT traversal capabilities.</span></span> <span data-ttu-id="442bc-105">不過，許多應用程式（包括對等）將需要 Teredo 才能從網際網路接收未經要求的流量。</span><span class="sxs-lookup"><span data-stu-id="442bc-105">However, many applications, including peer-to-peer, will require Teredo to receive unsolicited traffic from the Internet.</span></span> <span data-ttu-id="442bc-106">應用程式可透過單一 IPv6 介面或所有支援 IPv6 的介面，以程式設計的方式接收流量。</span><span class="sxs-lookup"><span data-stu-id="442bc-106">An application can be programmed to receive traffic over a single IPv6 interface or all IPv6-capable interfaces.</span></span> <span data-ttu-id="442bc-107">本檔說明使用 Teredo 介面接收未經要求之 IPv6 流量的應用程式需求。</span><span class="sxs-lookup"><span data-stu-id="442bc-107">This documentation describes the requirements for applications that use the Teredo interface to receive unsolicited IPv6 traffic.</span></span>

<span data-ttu-id="442bc-108">只有當應用程式已向 [Windows 防火牆](/previous-versions/windows/desktop/ics/windows-firewall-start-page)註冊時，應用程式才會透過 Teredo 介面接收未經要求的流量。</span><span class="sxs-lookup"><span data-stu-id="442bc-108">An application will receive unsolicited traffic over the Teredo interface only if the application is registered with [Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page).</span></span> <span data-ttu-id="442bc-109">為了接收未經要求的流量，必須進行下列動作：</span><span class="sxs-lookup"><span data-stu-id="442bc-109">In order to receive unsolicited traffic the following must occur:</span></span>

-   <span data-ttu-id="442bc-110">必須指示使用者使用 Microsoft Management Console (MMC) 來啟用應用程式的「Edge 遍歷」選項。</span><span class="sxs-lookup"><span data-stu-id="442bc-110">Users must be instructed to use of the Microsoft Management Console (MMC) to enable the "Edge Traversal" option for an application.</span></span> <span data-ttu-id="442bc-111">此選項可在 [Windows 防火牆] Snap-In--> <application name> --> [Advanced] 索引標籤下取得。必須針對每個應用程式個別啟用「Edge 遍歷」選項。</span><span class="sxs-lookup"><span data-stu-id="442bc-111">This option is available under Windows Firewall Snap-In --> <application name> --> "Advanced" tab. The "Edge Traversal" option must be enabled individually for each application.</span></span>

-   <span data-ttu-id="442bc-112">應用程式會啟用 [Edge 遍歷] 選項。</span><span class="sxs-lookup"><span data-stu-id="442bc-112">The "Edge Traversal" option is enabled by the application.</span></span> <span data-ttu-id="442bc-113">能夠接收未要求流量的應用程式可能會向 Windows 防火牆註冊以進行「邊緣遍歷」，並透過 Teredo 介面接收未經要求的流量。</span><span class="sxs-lookup"><span data-stu-id="442bc-113">It is possible for applications capable of receiving unsolicited traffic to register with Windows Firewall for "Edge Traversal" and receive unsolicited traffic over the Teredo interface.</span></span> <span data-ttu-id="442bc-114">若要這樣做，應用程式必須呼叫 [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) API，並將「Edge 遍歷」選項設定為 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="442bc-114">To do this an application must call the [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) API with the "Edge Traversal" option set to VARIANT\_TRUE.</span></span> <span data-ttu-id="442bc-115">允許應用程式接聽流量之前，此 API 呼叫需要使用者同意。</span><span class="sxs-lookup"><span data-stu-id="442bc-115">User consent is required for this API call before an application is permitted to listen for the traffic.</span></span>

-   <span data-ttu-id="442bc-116">應用程式會透過 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)將 Winsock [IPV6 \_ 保護 \_ 等級](/windows/desktop/WinSock/ipv6-protection-level)通訊端選項設定為 **\_ \_ 無限制的保護層級**。</span><span class="sxs-lookup"><span data-stu-id="442bc-116">The application sets the Winsock [IPV6\_PROTECTION\_LEVEL](/windows/desktop/WinSock/ipv6-protection-level) socket option to **PROTECTION\_LEVEL\_UNRESTRICTED** via [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span></span> <span data-ttu-id="442bc-117">這可讓應用程式接收 Edge 遍歷流量。</span><span class="sxs-lookup"><span data-stu-id="442bc-117">This will allow the application to receive Edge Traversal traffic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="442bc-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="442bc-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="442bc-119">透過 Teredo 接收請求的流量</span><span class="sxs-lookup"><span data-stu-id="442bc-119">Receiving Solicited Traffic Over Teredo</span></span>](receiving-solicited-traffic-over-teredo.md)
</dt> </dl>

 

 