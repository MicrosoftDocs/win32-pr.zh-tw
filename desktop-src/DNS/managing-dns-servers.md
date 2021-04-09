---
title: 管理 DNS 伺服器
description: DNS 伺服器是在 DNS 中完成名稱解析程式的電腦。
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe97e8b8b02e9d2198e49d0574b2d3fb8bc87df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674484"
---
# <a name="managing-dns-servers"></a><span data-ttu-id="265ab-103">管理 DNS 伺服器</span><span class="sxs-lookup"><span data-stu-id="265ab-103">Managing DNS Servers</span></span>

<span data-ttu-id="265ab-104">DNS 伺服器是在 DNS 中完成名稱解析程式的電腦。</span><span class="sxs-lookup"><span data-stu-id="265ab-104">A DNS Server is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="265ab-105">DNS 伺服器包含稱為 *區域* 檔案的檔案，可讓他們解析 IP 位址的名稱 (或反之亦然) 。</span><span class="sxs-lookup"><span data-stu-id="265ab-105">DNS Servers contain files, called *zone files*, that enable them to resolve names to IP addresses (or vice versa).</span></span> <span data-ttu-id="265ab-106">在查詢時，DNS 伺服器會以下列三種方式之一回應：</span><span class="sxs-lookup"><span data-stu-id="265ab-106">When queried, a DNS Server responds in one of three ways:</span></span>

-   <span data-ttu-id="265ab-107">伺服器會傳回要求的名稱解析或 IP 解析資訊。</span><span class="sxs-lookup"><span data-stu-id="265ab-107">The server returns the requested name-resolution or IP-resolution information.</span></span>
-   <span data-ttu-id="265ab-108">伺服器會將指標傳回給另一部可服務要求的 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="265ab-108">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="265ab-109">伺服器表示它沒有所要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="265ab-109">The server indicates that it does not have the requested information.</span></span>

<span data-ttu-id="265ab-110">DNS 伺服器可能會在準備傳回所要求的解析資訊時，查詢其他 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="265ab-110">DNS Servers might, during the course of preparing to return the requested resolution information, query other DNS Servers.</span></span> <span data-ttu-id="265ab-111">但除此之外，DNS 伺服器不會執行上述清單中所述的任何作業。</span><span class="sxs-lookup"><span data-stu-id="265ab-111">But beyond that, DNS Servers do not perform any operations other than those mentioned in the previous list.</span></span>

<span data-ttu-id="265ab-112">有三種主要的 DNS 伺服器：主伺服器、次要伺服器和快取伺服器。</span><span class="sxs-lookup"><span data-stu-id="265ab-112">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span> <span data-ttu-id="265ab-113">如需這些 DNS 伺服器的詳細資訊，請參閱 [Dns 伺服器](dns-servers.md) 。</span><span class="sxs-lookup"><span data-stu-id="265ab-113">See [DNS Servers](dns-servers.md) for more information on these DNS Servers.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="265ab-114">管理步驟</span><span class="sxs-lookup"><span data-stu-id="265ab-114">Administration Steps</span></span>

<span data-ttu-id="265ab-115">DNS WMI 提供者可讓您從伺服器本身或從遠端主機管理 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="265ab-115">The DNS WMI Provider enables the administration of DNS Servers from the server itself, or from remote hosts.</span></span> <span data-ttu-id="265ab-116">使用 DNS WMI 提供者管理 DNS 伺服器所需的一般步驟如下：</span><span class="sxs-lookup"><span data-stu-id="265ab-116">The general steps necessary to administer a DNS Server using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="265ab-117">連接到 DNS WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="265ab-117">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="265ab-118">取得伺服器實例</span><span class="sxs-lookup"><span data-stu-id="265ab-118">Getting a server instance</span></span>
-   <span data-ttu-id="265ab-119">列出或修改伺服器屬性，或使用方法</span><span class="sxs-lookup"><span data-stu-id="265ab-119">Listing or modifying a server property, or using a method</span></span>

<span data-ttu-id="265ab-120">為了說明如何實行這些管理步驟，我們提供了範例。</span><span class="sxs-lookup"><span data-stu-id="265ab-120">To illustrate how to implement those administration steps, examples are provided.</span></span> <span data-ttu-id="265ab-121">下列工作會連結到其相關聯的腳本範例。</span><span class="sxs-lookup"><span data-stu-id="265ab-121">The following tasks are linked to their associated scripting samples.</span></span>

-   [<span data-ttu-id="265ab-122">停止 DNS 伺服器</span><span class="sxs-lookup"><span data-stu-id="265ab-122">Stopping a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="265ab-123">啟動 DNS 伺服器</span><span class="sxs-lookup"><span data-stu-id="265ab-123">Starting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="265ab-124">重新開機 DNS 伺服器</span><span class="sxs-lookup"><span data-stu-id="265ab-124">Restarting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="265ab-125">新增 IP 位址</span><span class="sxs-lookup"><span data-stu-id="265ab-125">Adding an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="265ab-126">移除 IP 位址</span><span class="sxs-lookup"><span data-stu-id="265ab-126">Removing an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="265ab-127">列出 DNS 伺服器屬性</span><span class="sxs-lookup"><span data-stu-id="265ab-127">Listing DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="265ab-128">顯示 DNS 伺服器屬性類型</span><span class="sxs-lookup"><span data-stu-id="265ab-128">Displaying DNS Server Property Types</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="265ab-129">修改 DNS 伺服器屬性</span><span class="sxs-lookup"><span data-stu-id="265ab-129">Modifying DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




