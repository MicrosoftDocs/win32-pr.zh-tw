---
title: 資源記錄
description: 瞭解資源記錄。 資源記錄是 DNS 區域檔案中的資訊專案單位，用來解析所有 DNS 查詢。
ms.assetid: c64907c2-ebd3-4550-9454-13f51a6d7ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84bd000e2d88884bbb387748eaced1d0d58a324
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010671"
---
# <a name="resource-records"></a><span data-ttu-id="6dea7-104">資源記錄</span><span class="sxs-lookup"><span data-stu-id="6dea7-104">Resource Records</span></span>

<span data-ttu-id="6dea7-105">資源記錄（通常稱為 RR）是 DNS 區域檔案中的資訊專案單位。Rr 是主機名稱和 IP 資訊的基本組建區塊，可用來解析所有 DNS 查詢。</span><span class="sxs-lookup"><span data-stu-id="6dea7-105">A resource record, commonly referred to as an RR, is the unit of information entry in DNS zone files; RRs are the basic building blocks of host-name and IP information and are used to resolve all DNS queries.</span></span> <span data-ttu-id="6dea7-106">資源記錄有許多類型，可提供延伸的名稱解析服務。</span><span class="sxs-lookup"><span data-stu-id="6dea7-106">Resource records exist as many types to provide extended name-resolution services.</span></span>

<span data-ttu-id="6dea7-107">不同類型的 Rr 具有不同的格式，因為它們包含不同的資料。</span><span class="sxs-lookup"><span data-stu-id="6dea7-107">Different types of RRs have different formats, as they contain different data.</span></span> <span data-ttu-id="6dea7-108">不過，一般而言，許多 Rr 共用通用格式，如下列位址資源記錄範例所示。</span><span class="sxs-lookup"><span data-stu-id="6dea7-108">In general, however, many RRs share a common format, as the following address resource records example illustrates.</span></span> <span data-ttu-id="6dea7-109">下列虛構範例說明在資源記錄中找到的欄位：</span><span class="sxs-lookup"><span data-stu-id="6dea7-109">The following fictional example explains the fields found in an A resource record:</span></span>

``` syntax
microsoft.com. 600 IN A 150.150.150.1
```

-   <span data-ttu-id="6dea7-110">第一個 (microsoft.com 的欄位) 代表擁有者。</span><span class="sxs-lookup"><span data-stu-id="6dea7-110">The first field (microsoft.com) denotes the owner.</span></span>
-   <span data-ttu-id="6dea7-111">第二個欄位 (600) 是存留時間 (TTL) 參數（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6dea7-111">The second field (600) is the time-to-live (TTL) parameter, in seconds.</span></span>
-   <span data-ttu-id="6dea7-112">) 中的第三個欄位 (是代表通訊協定系列的類別欄位，此欄位幾乎都是針對網際網路類別。</span><span class="sxs-lookup"><span data-stu-id="6dea7-112">The third field (IN) is the class field that represents the protocol family, which is almost always IN, for Internet class.</span></span>
-   <span data-ttu-id="6dea7-113">第四個欄位 () 是 RR 所代表的資源類型。</span><span class="sxs-lookup"><span data-stu-id="6dea7-113">The fourth field (A) is the type of resource the RR is representing.</span></span>
-   <span data-ttu-id="6dea7-114">第五個欄位 (150.150.150.1) 為資源資料或 .RDATA。</span><span class="sxs-lookup"><span data-stu-id="6dea7-114">The fifth field (150.150.150.1) is the resource data, or RDATA.</span></span> <span data-ttu-id="6dea7-115">此欄位是提供資源類型相關資訊的變數類型;在此情況下，它是32位的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="6dea7-115">This field is a variable type that provides information appropriate for the type of resource; in this case, it's a 32-bit IP address.</span></span>

<span data-ttu-id="6dea7-116">DNS 中通常會使用下列資源記錄類型：</span><span class="sxs-lookup"><span data-stu-id="6dea7-116">The following resource record types are commonly used in DNS:</span></span>

-   <span data-ttu-id="6dea7-117"> (SOA) 的授權單位啟動</span><span class="sxs-lookup"><span data-stu-id="6dea7-117">Start of authority (SOA)</span></span>
-   <span data-ttu-id="6dea7-118"> (NS) 的名稱伺服器</span><span class="sxs-lookup"><span data-stu-id="6dea7-118">Name server (NS)</span></span>
-   <span data-ttu-id="6dea7-119">[*指標記錄*](p-gly.md) (PTR) </span><span class="sxs-lookup"><span data-stu-id="6dea7-119">[*Pointer record*](p-gly.md) (PTR)</span></span>
-   <span data-ttu-id="6dea7-120"> () 的位址</span><span class="sxs-lookup"><span data-stu-id="6dea7-120">Address (A)</span></span>
-   <span data-ttu-id="6dea7-121">IPv6 位址 (AAAA) </span><span class="sxs-lookup"><span data-stu-id="6dea7-121">IPv6 Address (AAAA)</span></span>
-   <span data-ttu-id="6dea7-122">郵件交換 (MX) </span><span class="sxs-lookup"><span data-stu-id="6dea7-122">Mail exchange (MX)</span></span>
-   <span data-ttu-id="6dea7-123">[*標準名稱*](c-gly.md) (CNAME) </span><span class="sxs-lookup"><span data-stu-id="6dea7-123">[*Canonical name*](c-gly.md) (CNAME)</span></span>
-   <span data-ttu-id="6dea7-124">Windows Internet 命名服務 (WINS) </span><span class="sxs-lookup"><span data-stu-id="6dea7-124">Windows Internet Naming Service (WINS)</span></span>
-   <span data-ttu-id="6dea7-125">WINS 反向查閱 (WINSR) </span><span class="sxs-lookup"><span data-stu-id="6dea7-125">WINS Reverse Look up (WINSR)</span></span>

<span data-ttu-id="6dea7-126">DNS 中有許多其他資源記錄類型。</span><span class="sxs-lookup"><span data-stu-id="6dea7-126">There are many other resource record types in DNS.</span></span> <span data-ttu-id="6dea7-127">如需詳細資訊，請參閱 [DNS WMI 提供者參考](dns-wmi-provider-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="6dea7-127">For more information, see [DNS WMI Provider Reference](dns-wmi-provider-reference.md).</span></span>

 

 




