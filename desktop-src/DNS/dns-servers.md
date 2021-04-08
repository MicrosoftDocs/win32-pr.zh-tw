---
title: DNS 伺服器
description: DNS 伺服器是在 DNS 中完成名稱解析程式的電腦。
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- DNS 伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 509ceeb811f221560540ae60f269c6ee1b05444f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674360"
---
# <a name="dns-servers"></a><span data-ttu-id="f4e21-104">DNS 伺服器</span><span class="sxs-lookup"><span data-stu-id="f4e21-104">DNS Servers</span></span>

<span data-ttu-id="f4e21-105">*Dns 伺服器* 是在 dns 中完成名稱解析程式的電腦。</span><span class="sxs-lookup"><span data-stu-id="f4e21-105">A *DNS Server* is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="f4e21-106">DNS 伺服器包含 [*區域*](z-gly.md) 檔案，可讓他們將 ip 位址和 ip 位址的名稱解析為名稱。</span><span class="sxs-lookup"><span data-stu-id="f4e21-106">DNS Servers contain [*zone files*](z-gly.md) that enable them to resolve names to IP addresses and IP addresses to names.</span></span> <span data-ttu-id="f4e21-107">當查詢時，DNS 伺服器會以下列三種方式之一回應：</span><span class="sxs-lookup"><span data-stu-id="f4e21-107">When queried, a DNS Server will respond in one of three ways:</span></span>

-   <span data-ttu-id="f4e21-108">伺服器會傳回要求的名稱解析或 IP 解析資料。</span><span class="sxs-lookup"><span data-stu-id="f4e21-108">The server returns the requested name-resolution or IP-resolution data.</span></span>
-   <span data-ttu-id="f4e21-109">伺服器會將指標傳回給另一部可服務要求的 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="f4e21-109">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="f4e21-110">伺服器表示它沒有所要求的資料。</span><span class="sxs-lookup"><span data-stu-id="f4e21-110">The server indicates that it does not have the requested data.</span></span>

<span data-ttu-id="f4e21-111">DNS 伺服器可能在準備傳回所要求的解析資料、查詢其他 DNS 伺服器，但除此之外，DNS 伺服器不會執行任何其他作業。</span><span class="sxs-lookup"><span data-stu-id="f4e21-111">DNS Servers might, during the course of preparing to return the requested resolution data, query other DNS Servers, but beyond that, DNS Servers do not perform any other operations.</span></span>

<span data-ttu-id="f4e21-112">有三種主要的 DNS 伺服器：主伺服器、次要伺服器和快取伺服器。</span><span class="sxs-lookup"><span data-stu-id="f4e21-112">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span>

## <a name="primary-server"></a><span data-ttu-id="f4e21-113">主要伺服器</span><span class="sxs-lookup"><span data-stu-id="f4e21-113">Primary Server</span></span>

<span data-ttu-id="f4e21-114">*主伺服器* 是區域的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="f4e21-114">The *primary server* is the authoritative server for the zone.</span></span> <span data-ttu-id="f4e21-115">與區域相關聯的所有管理工作 (例如在區域內建立子域，或其他類似的系統管理工作) 必須在主伺服器上執行。</span><span class="sxs-lookup"><span data-stu-id="f4e21-115">All administrative tasks associated with the zone (such as creating subdomains within the zone, or other similar administrative tasks) must be performed on the primary server.</span></span> <span data-ttu-id="f4e21-116">此外，在主伺服器上，您必須在主伺服器上建立與區域相關聯的任何變更，或區域檔案中任何對 Rr 的修改或新增專案。</span><span class="sxs-lookup"><span data-stu-id="f4e21-116">In addition, any changes associated with the zone or any modifications or additions to RRs in the zone files must be made on the primary server.</span></span> <span data-ttu-id="f4e21-117">針對任何指定的區域，只有一部主伺服器，但在整合 Active Directory services 與 Microsoft DNS 伺服器時除外。</span><span class="sxs-lookup"><span data-stu-id="f4e21-117">For any given zone, there is one primary server, except when you integrate Active Directory services and Microsoft DNS Server.</span></span>

## <a name="secondary-servers"></a><span data-ttu-id="f4e21-118">次要伺服器</span><span class="sxs-lookup"><span data-stu-id="f4e21-118">Secondary Servers</span></span>

<span data-ttu-id="f4e21-119">*次要伺服器* 是備份 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="f4e21-119">*Secondary servers* are backup DNS Servers.</span></span> <span data-ttu-id="f4e21-120">次要伺服器會從區域轉送中的主伺服器區域檔案接收所有的區域檔案。</span><span class="sxs-lookup"><span data-stu-id="f4e21-120">Secondary servers receive all of their zone files from the primary server zone files in a zone transfer.</span></span> <span data-ttu-id="f4e21-121">任何指定區域都可以有多個次要伺服器（視需要提供 [*負載平衡*](l-gly.md)、 [*容錯*](f-gly.md)和流量降低）。</span><span class="sxs-lookup"><span data-stu-id="f4e21-121">Multiple secondary servers can exist for any given zone — as many as necessary to provide [*load balancing*](l-gly.md), [*fault tolerance*](f-gly.md), and traffic reduction.</span></span> <span data-ttu-id="f4e21-122">此外，任何指定的 DNS 伺服器可以是多個區域的次要伺服器。</span><span class="sxs-lookup"><span data-stu-id="f4e21-122">Additionally, any given DNS Server can be a secondary server for multiple zones.</span></span>

<span data-ttu-id="f4e21-123">除了主要和次要 DNS 伺服器之外，當這類伺服器適用于 DNS 基礎結構時，也可以使用額外的 DNS 伺服器角色。</span><span class="sxs-lookup"><span data-stu-id="f4e21-123">In addition to primary and secondary DNS Servers, additional DNS Server roles can be used when such servers are appropriate for a DNS infrastructure.</span></span> <span data-ttu-id="f4e21-124">這些額外的伺服器是快取 [*伺服器和轉寄*](f-gly.md)站。</span><span class="sxs-lookup"><span data-stu-id="f4e21-124">These additional servers are caching servers and [*forwarders*](f-gly.md).</span></span>

## <a name="caching-servers"></a><span data-ttu-id="f4e21-125">快取伺服器</span><span class="sxs-lookup"><span data-stu-id="f4e21-125">Caching Servers</span></span>

<span data-ttu-id="f4e21-126">快取 [*伺服器*](c-gly.md)（也稱為僅限快取伺服器）的執行方式如其名稱所示;它們只針對 DNS 回應提供快取查詢服務。</span><span class="sxs-lookup"><span data-stu-id="f4e21-126">[*Caching servers*](c-gly.md), also known as caching-only servers, perform as their name suggests; they provide only cached-query service for DNS responses.</span></span> <span data-ttu-id="f4e21-127">快取 DNS 伺服器會執行查詢、快取答案，然後將結果傳回給查詢用戶端，而不是像其他次要伺服器一樣維護區域檔案。</span><span class="sxs-lookup"><span data-stu-id="f4e21-127">Rather than maintaining zone files like other secondary servers do, caching DNS Servers perform queries, cache the answers, and return the results to the querying client.</span></span> <span data-ttu-id="f4e21-128">快取伺服器和其他次要伺服器之間的主要差異在於，其他次要伺服器會在適當的情況下 (維護區域檔案，並在適當時進列區域轉送，進而產生與傳輸) 相關聯的網路流量，而快取伺服器則否。</span><span class="sxs-lookup"><span data-stu-id="f4e21-128">The primary difference between caching servers and other secondary servers is that other secondary servers maintain zone files (and do zone transfers when appropriate, thereby generating network traffic associated with the transfer), caching servers do not.</span></span>

 

 




