---
title: 管理 DNS 區域
description: DNS 區域是對應至 DNS 階層式命名空間一部分之 RR 專案的資料庫。 DNS 區域是用來界定哪些 DNS 伺服器有權解析 DNS 階層中指定區段的名稱解析查詢。
ms.assetid: d4aa94e0-36f7-4b97-8a0a-c677c8a826a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c4cc991821f88076d3c3e9b2bfcbddc3ab662d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674483"
---
# <a name="managing-dns-zones"></a><span data-ttu-id="bc188-104">管理 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="bc188-104">Managing DNS Zones</span></span>

<span data-ttu-id="bc188-105">DNS 區域是對應至 DNS 階層式命名空間一部分之 RR 專案的資料庫。</span><span class="sxs-lookup"><span data-stu-id="bc188-105">A DNS zone is a database of RR entries that corresponds to part of the DNS hierarchical name space.</span></span> <span data-ttu-id="bc188-106">DNS 區域是用來界定哪些 DNS 伺服器有權解析 DNS 階層中指定區段的名稱解析查詢。</span><span class="sxs-lookup"><span data-stu-id="bc188-106">DNS zones are used to delineate which DNS Servers are authoritative for resolving name-resolution queries for a given section of the DNS hierarchy.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="bc188-107">管理步驟</span><span class="sxs-lookup"><span data-stu-id="bc188-107">Administration Steps</span></span>

<span data-ttu-id="bc188-108">DNS WMI 提供者可從授權 DNS 伺服器本身或從遠端主機管理 DNS 區域。</span><span class="sxs-lookup"><span data-stu-id="bc188-108">The DNS WMI Provider enables the administration of DNS zones from the authoritative DNS Server itself, or from remote hosts.</span></span> <span data-ttu-id="bc188-109">使用 DNS WMI 提供者管理區域所需的一般步驟如下：</span><span class="sxs-lookup"><span data-stu-id="bc188-109">The general steps necessary to administer a zone using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="bc188-110">連接到 DNS WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="bc188-110">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="bc188-111">取得區域實例</span><span class="sxs-lookup"><span data-stu-id="bc188-111">Getting a zone instance</span></span>
-   <span data-ttu-id="bc188-112">列出或修改區域屬性，或使用方法</span><span class="sxs-lookup"><span data-stu-id="bc188-112">Listing or modifying a zone property, or using a method</span></span>

<span data-ttu-id="bc188-113">下列工作會連結到其相關聯的腳本範例：</span><span class="sxs-lookup"><span data-stu-id="bc188-113">The following tasks are linked to their associated scripting samples:</span></span>

-   [<span data-ttu-id="bc188-114">建立 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="bc188-114">Creating a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="bc188-115">修改 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="bc188-115">Modifying a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="bc188-116">刪除 DNS 區域</span><span class="sxs-lookup"><span data-stu-id="bc188-116">Deleting a DNS Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="bc188-117">新增區域 IP 位址</span><span class="sxs-lookup"><span data-stu-id="bc188-117">Adding a Zone IP Address</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="bc188-118">刪除區域 IP 位址</span><span class="sxs-lookup"><span data-stu-id="bc188-118">Deleting a Zone IP Address</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="bc188-119">暫停區域</span><span class="sxs-lookup"><span data-stu-id="bc188-119">Pausing a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="bc188-120">繼續區域</span><span class="sxs-lookup"><span data-stu-id="bc188-120">Resuming a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="bc188-121">更新區域</span><span class="sxs-lookup"><span data-stu-id="bc188-121">Updating a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="bc188-122">重載區域</span><span class="sxs-lookup"><span data-stu-id="bc188-122">Reloading a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)
-   [<span data-ttu-id="bc188-123">重新整理區域</span><span class="sxs-lookup"><span data-stu-id="bc188-123">Refreshing a Zone</span></span>](dns-wmi-provider-samples-managing-dns-zones.md)

 

 




