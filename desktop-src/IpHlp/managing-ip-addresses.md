---
description: IP 協助程式可協助管理與本機電腦上的介面相關聯的 IP 位址。 使用下列段落中所述的功能來管理 IP 位址。
ms.assetid: 94da3e53-1898-4721-b5f0-0b7244574c55
title: 管理 IP 位址
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0917050799ea452cf1c6ee3e068cc29793df8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972024"
---
# <a name="managing-ip-addresses"></a><span data-ttu-id="32244-104">管理 IP 位址</span><span class="sxs-lookup"><span data-stu-id="32244-104">Managing IP Addresses</span></span>

<span data-ttu-id="32244-105">IP 協助程式可協助管理與本機電腦上的介面相關聯的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="32244-105">IP Helper can assist in the management of IP addresses associated with interfaces on the local computer.</span></span> <span data-ttu-id="32244-106">使用下列段落中所述的功能來管理 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="32244-106">Use the functions described in the following paragraphs for IP address management.</span></span>

<span data-ttu-id="32244-107">[**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable)函式會抓取包含 IP 位址與介面之對應的資料表。</span><span class="sxs-lookup"><span data-stu-id="32244-107">The [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function retrieves a table that contains the mapping of IP addresses to interfaces.</span></span> <span data-ttu-id="32244-108">有一個以上的 IP 位址可能與相同的介面相關聯。</span><span class="sxs-lookup"><span data-stu-id="32244-108">More than one IP address may be associated with the same interface.</span></span>

<span data-ttu-id="32244-109">使用 [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) 函式，將 IP 位址新增至特定介面。</span><span class="sxs-lookup"><span data-stu-id="32244-109">Use the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function to add an IP address to a particular interface.</span></span> <span data-ttu-id="32244-110">若要移除先前使用 **AddIPAddress** 新增的 IP 位址，請使用 [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) 函數。</span><span class="sxs-lookup"><span data-stu-id="32244-110">To remove IP addresses that were previously added using **AddIPAddress**, use the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function.</span></span>

<span data-ttu-id="32244-111">[**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress)和 [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress)函式需要本機電腦使用動態主機設定通訊協定 (DHCP) 。</span><span class="sxs-lookup"><span data-stu-id="32244-111">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions require the local computer to be using Dynamic Host Configuration Protocol (DHCP).</span></span> <span data-ttu-id="32244-112">**IpReleaseAddress** 函式會釋放先前從 DHCP 取得的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="32244-112">The **IpReleaseAddress** function releases an IP address that was previously obtained from DHCP.</span></span> <span data-ttu-id="32244-113">**IpRenewAddress** 函式會在特定 IP 位址上更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="32244-113">The **IpRenewAddress** function renews a DHCP lease on a particular IP address.</span></span> <span data-ttu-id="32244-114">DHCP 租用可讓電腦在指定的一段時間內使用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="32244-114">A DHCP lease allows a computer to use an IP address for a specified period of time.</span></span>

-   <span data-ttu-id="32244-115">如需涉及 [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) 的程式碼範例，請參閱 [使用 GetIpAddrTable 管理 IP 位址](managing-ip-addresses-using-getipaddrtable.md)。</span><span class="sxs-lookup"><span data-stu-id="32244-115">For code samples involving [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) see [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span></span>

-   <span data-ttu-id="32244-116">如需涉及 [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) 和 [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)的程式碼範例，請參閱 [使用 AddIPAddress 和 DeleteIPAddress 管理 IP 位址](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)。</span><span class="sxs-lookup"><span data-stu-id="32244-116">For code samples involving [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) and [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), see [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md).</span></span>

-   <span data-ttu-id="32244-117">如需涉及 [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) 和 [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) 的程式碼範例，請參閱 [使用 IpReleaseAddress 和 IpRenewAddress 管理 DHCP 租用](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)。</span><span class="sxs-lookup"><span data-stu-id="32244-117">For code samples involving [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) see [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md).</span></span>

 

 



