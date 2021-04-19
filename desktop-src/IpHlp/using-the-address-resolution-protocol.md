---
description: 您可以使用 IP 協助程式來執行本機電腦 (ARP) 作業的位址解析通訊協定。 使用下列函式來取出和修改 ARP 資料表。
ms.assetid: 2c5dc1f8-590f-4b41-b6bb-f82ab093252f
title: 使用位址解析通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deec57c3b028f8f90135567bb07dbc00bda89036
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984732"
---
# <a name="using-the-address-resolution-protocol"></a><span data-ttu-id="bd1a1-104">使用位址解析通訊協定</span><span class="sxs-lookup"><span data-stu-id="bd1a1-104">Using the Address Resolution Protocol</span></span>

<span data-ttu-id="bd1a1-105">您可以使用 IP 協助程式來執行本機電腦 (ARP) 作業的位址解析通訊協定。</span><span class="sxs-lookup"><span data-stu-id="bd1a1-105">You can use IP Helper to perform Address Resolution Protocol (ARP) operations for the local computer.</span></span> <span data-ttu-id="bd1a1-106">使用下列函式來取出和修改 ARP 資料表。</span><span class="sxs-lookup"><span data-stu-id="bd1a1-106">Use the following functions to retrieve and modify the ARP table.</span></span>

<span data-ttu-id="bd1a1-107">[**GetIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable)會捕獲 ARP 資料表。</span><span class="sxs-lookup"><span data-stu-id="bd1a1-107">The [**GetIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipnettable) retrieves the ARP table.</span></span> <span data-ttu-id="bd1a1-108">ARP 表格包含 IP 位址與實體位址的對應。</span><span class="sxs-lookup"><span data-stu-id="bd1a1-108">The ARP table contains the mapping of IP addresses to physical addresses.</span></span> <span data-ttu-id="bd1a1-109">實體位址有時稱為媒體存取控制器 (MAC) 位址。</span><span class="sxs-lookup"><span data-stu-id="bd1a1-109">Physical addresses are sometimes referred to as Media Access Controller (MAC) addresses.</span></span>

<span data-ttu-id="bd1a1-110">使用 [**CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) 和 [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) 函數，在資料表中新增或移除特定的 ARP 專案。</span><span class="sxs-lookup"><span data-stu-id="bd1a1-110">Use the [**CreateIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipnetentry) and [**DeleteIpNetEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipnetentry) functions to add or remove particular ARP entries to or from the table.</span></span> <span data-ttu-id="bd1a1-111">[**FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable)函數會刪除資料表中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="bd1a1-111">The [**FlushIpNetTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-flushipnettable) function deletes all entries from the table.</span></span>

<span data-ttu-id="bd1a1-112">若要建立或刪除 proxy ARP 專案，請使用 [**CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) 和 [**DeleteProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) 函數。</span><span class="sxs-lookup"><span data-stu-id="bd1a1-112">To create or delete proxy ARP entries, use the [**CreateProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createproxyarpentry) and [**DeleteProxyArpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteproxyarpentry) functions.</span></span>

<span data-ttu-id="bd1a1-113">[**SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp)函式會將 ARP 要求傳送到區域網路。</span><span class="sxs-lookup"><span data-stu-id="bd1a1-113">The [**SendARP**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-sendarp) function sends an ARP request to the local network.</span></span>

 

 



