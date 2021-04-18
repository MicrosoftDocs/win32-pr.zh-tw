---
description: IP Helper 提供管理網路介面卡的功能。 指定電腦上的介面和介面卡之間有一對一的對應關係。 介面是一個 IP 層級的抽象概念，而介面卡是一個交叉連結層級的抽象概念。
ms.assetid: fbb32941-2add-4f74-90c4-1dc1bfebd64c
title: 管理網路介面卡
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa8f42cf1499ee7873d13334d0edbc9f954794f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511256"
---
# <a name="managing-network-adapters"></a><span data-ttu-id="93b29-105">管理網路介面卡</span><span class="sxs-lookup"><span data-stu-id="93b29-105">Managing Network Adapters</span></span>

<span data-ttu-id="93b29-106">IP Helper 提供管理網路介面卡的功能。</span><span class="sxs-lookup"><span data-stu-id="93b29-106">IP Helper provides capabilities for managing network adapters.</span></span> <span data-ttu-id="93b29-107">指定電腦上的介面和介面卡之間有一對一的對應關係。</span><span class="sxs-lookup"><span data-stu-id="93b29-107">There is a one-to-one correspondence between the interfaces and adapters on a given computer.</span></span> <span data-ttu-id="93b29-108">介面是一個 IP 層級的抽象概念，而介面卡是一個交叉連結層級的抽象概念。</span><span class="sxs-lookup"><span data-stu-id="93b29-108">An interface is an IP-level abstraction, whereas an adapter is a datalink-level abstraction.</span></span>

<span data-ttu-id="93b29-109">您可以使用下列段落中所述的函式，來取得本機電腦上網路介面卡的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="93b29-109">Use the functions described in the following paragraphs to retrieve information about the network adapters in the local computer.</span></span>

<span data-ttu-id="93b29-110">[**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo)函式會傳回 [**IP \_ 介面卡 \_ 資訊**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info)結構的陣列，本機電腦中的每個介面卡都有一個陣列。</span><span class="sxs-lookup"><span data-stu-id="93b29-110">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function returns an array of [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) structures, one for each adapter in the local computer.</span></span> <span data-ttu-id="93b29-111">[**GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo)函數會傳回特定介面卡的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="93b29-111">The [**GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) function returns additional information about a specific adapter.</span></span> <span data-ttu-id="93b29-112">**GetPerAdapterInfo** 函式需要呼叫者指定介面卡的索引。</span><span class="sxs-lookup"><span data-stu-id="93b29-112">The **GetPerAdapterInfo** function requires the caller to specify the index of the adapter.</span></span> <span data-ttu-id="93b29-113">若要從介面卡名稱取得介面卡索引，請使用 [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) 函數。</span><span class="sxs-lookup"><span data-stu-id="93b29-113">To obtain the adapter index from the adapter name, use the [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) function.</span></span>

<span data-ttu-id="93b29-114">有些應用程式會使用接收資料包的介面卡，但無法傳輸。</span><span class="sxs-lookup"><span data-stu-id="93b29-114">Some applications use adapters that receive datagrams, but cannot transmit them.</span></span> <span data-ttu-id="93b29-115">若要取得這些介面卡的相關資訊，請使用 [**GetUniDirectionalAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="93b29-115">To obtain information about these adapters, use the [**GetUniDirectionalAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) function.</span></span>

<span data-ttu-id="93b29-116">[**GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses)函數可讓您取得與特定介面卡相關聯的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="93b29-116">The [**GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) function enables you to retrieve the IP addresses associated with a particular adapter.</span></span> <span data-ttu-id="93b29-117">此函式支援 IPv4 和 IPv6 定址。</span><span class="sxs-lookup"><span data-stu-id="93b29-117">This function supports both IPv4 and IPv6 addressing.</span></span>

-   <span data-ttu-id="93b29-118">如需涉及 [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) 的程式碼範例，請參閱 [使用 GetAdaptersInfo 管理網路介面卡](managing-network-adapters-using-getadaptersinfo.md)。</span><span class="sxs-lookup"><span data-stu-id="93b29-118">For code samples involving [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) see [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span></span>

 

 



