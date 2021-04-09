---
title: 資源記錄
description: 資源記錄（通常稱為 RR）是 DNS 區域檔案中的資訊專案單位。Rr 是主機名稱和 IP 資訊的基本組建區塊，可用來解析所有 DNS 查詢。
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05b667b95a8ede32018e1aad7de375e77a890487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674732"
---
# <a name="resource-records"></a><span data-ttu-id="e3237-103">資源記錄</span><span class="sxs-lookup"><span data-stu-id="e3237-103">Resource Records</span></span>

<span data-ttu-id="e3237-104">資源記錄（通常稱為 RR）是 DNS 區域檔案中的資訊專案單位。Rr 是主機名稱和 IP 資訊的基本組建區塊，可用來解析所有 DNS 查詢。</span><span class="sxs-lookup"><span data-stu-id="e3237-104">A resource record, commonly referred to as an RR, is the unit of information entry in DNS zone files; RRs are the basic building blocks of host-name and IP information and are used to resolve all DNS queries.</span></span> <span data-ttu-id="e3237-105">資源記錄有許多類型，可提供延伸的名稱解析服務。</span><span class="sxs-lookup"><span data-stu-id="e3237-105">Resource records exist as many types to provide extended name-resolution services.</span></span>

<span data-ttu-id="e3237-106">不同類型的 Rr 具有不同的格式，因為它們包含不同的資料。</span><span class="sxs-lookup"><span data-stu-id="e3237-106">Different types of RRs have different formats, as they contain different data.</span></span> <span data-ttu-id="e3237-107">不過，一般而言，許多 Rr 共用通用格式，如下列位址資源記錄範例所示。</span><span class="sxs-lookup"><span data-stu-id="e3237-107">In general, however, many RRs share a common format, as the following address resource records example illustrates.</span></span> <span data-ttu-id="e3237-108">下列虛構範例說明在資源記錄中找到的欄位：</span><span class="sxs-lookup"><span data-stu-id="e3237-108">The following fictional example explains the fields found in an A resource record:</span></span>

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   <span data-ttu-id="e3237-109">第一個 (microsoft.com 的欄位) 代表擁有者。</span><span class="sxs-lookup"><span data-stu-id="e3237-109">The first field (microsoft.com) denotes the owner.</span></span>
-   <span data-ttu-id="e3237-110">第二個欄位 (600) 是存留時間 (TTL) 參數（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e3237-110">The second field (600) is the time-to-live (TTL) parameter, in seconds.</span></span>
-   <span data-ttu-id="e3237-111">) 中的第三個欄位 (是代表通訊協定系列的類別欄位，此欄位幾乎都是針對網際網路類別。</span><span class="sxs-lookup"><span data-stu-id="e3237-111">The third field (IN) is the class field that represents the protocol family, which is almost always IN, for Internet class.</span></span>
-   <span data-ttu-id="e3237-112">第四個欄位 () 是 RR 所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="e3237-112">The fourth field (A) is the type of resource the RR is representing.</span></span>
-   <span data-ttu-id="e3237-113">第五個欄位 (150.150.150.1) 為資源資料或 .RDATA。</span><span class="sxs-lookup"><span data-stu-id="e3237-113">The fifth field (150.150.150.1) is the resource data, or RDATA.</span></span> <span data-ttu-id="e3237-114">此欄位是提供資源類型相關資訊的變數類型;在此情況下，它是32位的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e3237-114">This field is a variable type that provides information appropriate for the type of resource; in this case, it's a 32-bit IP address.</span></span>

<span data-ttu-id="e3237-115">DNS 中通常會使用下列資源記錄類型：</span><span class="sxs-lookup"><span data-stu-id="e3237-115">The following resource record types are commonly used in DNS:</span></span>

-   <span data-ttu-id="e3237-116"> (SOA) 的授權單位啟動</span><span class="sxs-lookup"><span data-stu-id="e3237-116">Start of authority (SOA)</span></span>
-   <span data-ttu-id="e3237-117"> (NS) 的名稱伺服器</span><span class="sxs-lookup"><span data-stu-id="e3237-117">Name server (NS)</span></span>
-   <span data-ttu-id="e3237-118">[*指標記錄*](p-gly.md) (PTR) </span><span class="sxs-lookup"><span data-stu-id="e3237-118">[*Pointer record*](p-gly.md) (PTR)</span></span>
-   <span data-ttu-id="e3237-119"> () 的位址</span><span class="sxs-lookup"><span data-stu-id="e3237-119">Address (A)</span></span>
-   <span data-ttu-id="e3237-120">IPv6 位址 (AAAA) </span><span class="sxs-lookup"><span data-stu-id="e3237-120">IPv6 Address (AAAA)</span></span>
-   <span data-ttu-id="e3237-121">郵件交換 (MX) </span><span class="sxs-lookup"><span data-stu-id="e3237-121">Mail exchange (MX)</span></span>
-   <span data-ttu-id="e3237-122">[*標準名稱*](c-gly.md) (CNAME) </span><span class="sxs-lookup"><span data-stu-id="e3237-122">[*Canonical name*](c-gly.md) (CNAME)</span></span>
-   <span data-ttu-id="e3237-123">Windows Internet 命名服務 (WINS) </span><span class="sxs-lookup"><span data-stu-id="e3237-123">Windows Internet Naming Service (WINS)</span></span>
-   <span data-ttu-id="e3237-124">WINS 反向查閱 (WINSR) </span><span class="sxs-lookup"><span data-stu-id="e3237-124">WINS Reverse Look up (WINSR)</span></span>

<span data-ttu-id="e3237-125">DNS 中有許多其他資源記錄類型。</span><span class="sxs-lookup"><span data-stu-id="e3237-125">There are many other resource record types in DNS.</span></span> <span data-ttu-id="e3237-126">如需詳細資訊，請參閱 [DNS WMI 提供者參考](dns-wmi-provider-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="e3237-126">For more information, see [DNS WMI Provider Reference](dns-wmi-provider-reference.md).</span></span>

 

 




