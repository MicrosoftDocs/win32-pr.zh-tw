---
description: IP Helper 提供管理網路路由的功能。 使用下列功能管理 IP 路由表，以及取得其他路由資訊。
ms.assetid: 879b90e3-aecc-492e-9b22-9ebbf505a610
title: 管理路由
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ec199de19b4c8d724fbe6a2e77c3fac7dc19b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847950"
---
# <a name="managing-routing"></a><span data-ttu-id="8f66b-104">管理路由</span><span class="sxs-lookup"><span data-stu-id="8f66b-104">Managing Routing</span></span>

<span data-ttu-id="8f66b-105">IP Helper 提供管理網路路由的功能。</span><span class="sxs-lookup"><span data-stu-id="8f66b-105">IP Helper provides features to manage network routing.</span></span> <span data-ttu-id="8f66b-106">使用下列功能管理 IP 路由表，以及取得其他路由資訊。</span><span class="sxs-lookup"><span data-stu-id="8f66b-106">Use the following functions to manage the IP routing table, and to obtain other routing information.</span></span>

<span data-ttu-id="8f66b-107">藉由呼叫 [**GetIpForwardTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) 函數來取出 IP 路由表的內容。</span><span class="sxs-lookup"><span data-stu-id="8f66b-107">Retrieve the contents of the IP routing table by making a call to the [**GetIpForwardTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) function.</span></span> <span data-ttu-id="8f66b-108">使用 [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry)、 [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)和 [**SetIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) 函數來操作 IP 路由表中的特定專案。</span><span class="sxs-lookup"><span data-stu-id="8f66b-108">Manipulate specific entries in the IP routing table using the [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry), and [**SetIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) functions.</span></span> <span data-ttu-id="8f66b-109">使用 **CreateIpForwardEntry** 函式來加入新的路由表專案。</span><span class="sxs-lookup"><span data-stu-id="8f66b-109">Use the **CreateIpForwardEntry** function to add a new routing table entry.</span></span> <span data-ttu-id="8f66b-110">使用 **DeleteIpForwardEntry** 函數來移除現有的專案。</span><span class="sxs-lookup"><span data-stu-id="8f66b-110">Use the **DeleteIpForwardEntry** function to remove an existing entry.</span></span> <span data-ttu-id="8f66b-111">**SetIpForwardEntry** 函式會修改現有的專案。</span><span class="sxs-lookup"><span data-stu-id="8f66b-111">The **SetIpForwardEntry** function modifies an existing entry.</span></span>

<span data-ttu-id="8f66b-112">IP 協助程式的路由器管理功能可以用來取得有關如何透過網路路由傳送資料包的資訊。</span><span class="sxs-lookup"><span data-stu-id="8f66b-112">The router management capabilities of IP Helper can be used to retrieve information about how datagrams are routed over the network.</span></span> <span data-ttu-id="8f66b-113">[**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute)函式會取得指定之目的地位址的最佳路由。</span><span class="sxs-lookup"><span data-stu-id="8f66b-113">The [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) function retrieves the best route to a specified destination address.</span></span> <span data-ttu-id="8f66b-114">[**GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface)函式會將最佳路由所使用的介面索引，捕獲到指定的目的地位址。</span><span class="sxs-lookup"><span data-stu-id="8f66b-114">The [**GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) function retrieves the index of the interface used by the best route to a specified destination address.</span></span> <span data-ttu-id="8f66b-115">最後， [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) 函式會 (RTT) 和躍點數目，以指定的目的地位址抓取來回時間。</span><span class="sxs-lookup"><span data-stu-id="8f66b-115">Lastly, the [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) function retrieves the round-trip time (RTT) and number of hops to a specified destination address.</span></span>

 

 



