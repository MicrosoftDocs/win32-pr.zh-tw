---
title: 管理 DNS 伺服器
description: 瞭解如何管理 DNS 伺服器。 DNS 伺服器是在 DNS 中完成名稱解析程式的電腦。
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d797e05bc326b35e48173082d9b36a2b334fd9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010771"
---
# <a name="managing-dns-servers"></a><span data-ttu-id="a12a2-104">管理 DNS 伺服器</span><span class="sxs-lookup"><span data-stu-id="a12a2-104">Managing DNS Servers</span></span>

<span data-ttu-id="a12a2-105">DNS 伺服器是在 DNS 中完成名稱解析程式的電腦。</span><span class="sxs-lookup"><span data-stu-id="a12a2-105">A DNS Server is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="a12a2-106">DNS 伺服器包含稱為 *區域* 檔案的檔案，可讓他們解析 IP 位址的名稱 (或反之亦然) 。</span><span class="sxs-lookup"><span data-stu-id="a12a2-106">DNS Servers contain files, called *zone files*, that enable them to resolve names to IP addresses (or vice versa).</span></span> <span data-ttu-id="a12a2-107">在查詢時，DNS 伺服器會以下列三種方式之一回應：</span><span class="sxs-lookup"><span data-stu-id="a12a2-107">When queried, a DNS Server responds in one of three ways:</span></span>

-   <span data-ttu-id="a12a2-108">伺服器會傳回要求的名稱解析或 IP 解析資訊。</span><span class="sxs-lookup"><span data-stu-id="a12a2-108">The server returns the requested name-resolution or IP-resolution information.</span></span>
-   <span data-ttu-id="a12a2-109">伺服器會將指標傳回給另一部可服務要求的 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="a12a2-109">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="a12a2-110">伺服器表示它沒有所要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="a12a2-110">The server indicates that it does not have the requested information.</span></span>

<span data-ttu-id="a12a2-111">DNS 伺服器可能會在準備傳回所要求的解析資訊時，查詢其他 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="a12a2-111">DNS Servers might, during the course of preparing to return the requested resolution information, query other DNS Servers.</span></span> <span data-ttu-id="a12a2-112">但除此之外，DNS 伺服器不會執行上述清單中所述的任何作業。</span><span class="sxs-lookup"><span data-stu-id="a12a2-112">But beyond that, DNS Servers do not perform any operations other than those mentioned in the previous list.</span></span>

<span data-ttu-id="a12a2-113">有三種主要的 DNS 伺服器：主伺服器、次要伺服器和快取伺服器。</span><span class="sxs-lookup"><span data-stu-id="a12a2-113">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span> <span data-ttu-id="a12a2-114">如需這些 DNS 伺服器的詳細資訊，請參閱 [Dns 伺服器](dns-servers.md) 。</span><span class="sxs-lookup"><span data-stu-id="a12a2-114">See [DNS Servers](dns-servers.md) for more information on these DNS Servers.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="a12a2-115">管理步驟</span><span class="sxs-lookup"><span data-stu-id="a12a2-115">Administration Steps</span></span>

<span data-ttu-id="a12a2-116">DNS WMI 提供者可讓您從伺服器本身或從遠端主機管理 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="a12a2-116">The DNS WMI Provider enables the administration of DNS Servers from the server itself, or from remote hosts.</span></span> <span data-ttu-id="a12a2-117">使用 DNS WMI 提供者管理 DNS 伺服器所需的一般步驟如下：</span><span class="sxs-lookup"><span data-stu-id="a12a2-117">The general steps necessary to administer a DNS Server using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="a12a2-118">連接到 DNS WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="a12a2-118">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="a12a2-119">取得伺服器實例</span><span class="sxs-lookup"><span data-stu-id="a12a2-119">Getting a server instance</span></span>
-   <span data-ttu-id="a12a2-120">列出或修改伺服器屬性，或使用方法</span><span class="sxs-lookup"><span data-stu-id="a12a2-120">Listing or modifying a server property, or using a method</span></span>

<span data-ttu-id="a12a2-121">為了說明如何實行這些管理步驟，我們提供了範例。</span><span class="sxs-lookup"><span data-stu-id="a12a2-121">To illustrate how to implement those administration steps, examples are provided.</span></span> <span data-ttu-id="a12a2-122">下列工作會連結到其相關聯的腳本範例。</span><span class="sxs-lookup"><span data-stu-id="a12a2-122">The following tasks are linked to their associated scripting samples.</span></span>

-   [<span data-ttu-id="a12a2-123">停止 DNS 伺服器</span><span class="sxs-lookup"><span data-stu-id="a12a2-123">Stopping a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="a12a2-124">啟動 DNS 伺服器</span><span class="sxs-lookup"><span data-stu-id="a12a2-124">Starting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="a12a2-125">重新開機 DNS 伺服器</span><span class="sxs-lookup"><span data-stu-id="a12a2-125">Restarting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="a12a2-126">新增 IP 位址</span><span class="sxs-lookup"><span data-stu-id="a12a2-126">Adding an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="a12a2-127">移除 IP 位址</span><span class="sxs-lookup"><span data-stu-id="a12a2-127">Removing an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="a12a2-128">列出 DNS 伺服器屬性</span><span class="sxs-lookup"><span data-stu-id="a12a2-128">Listing DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="a12a2-129">顯示 DNS 伺服器屬性類型</span><span class="sxs-lookup"><span data-stu-id="a12a2-129">Displaying DNS Server Property Types</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="a12a2-130">修改 DNS 伺服器屬性</span><span class="sxs-lookup"><span data-stu-id="a12a2-130">Modifying DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




