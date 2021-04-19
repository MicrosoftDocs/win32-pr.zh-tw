---
description: Microsoft Internet Explorer 支援使用 IPv6 來連線及存取已啟用 IPv6 的網站 (網頁伺服器和 FTP 伺服器，例如在符合下列情況時) ：執行 Internet Explorer 的主機電腦必須安裝並啟用 IPv6。連接到位於本機子網上的主機時，提供連線的介面必須已指派可路由傳送的 IPv6 位址。連線至 IPv6 回送位址 (：： 1) 或連結-本機目的地時，不需要可路由傳送的 IPv6 位址。如果要求的 URL 包含名稱 (www.contoso.com，例如) ，則網域名稱系統 (DNS) 查詢該名稱必須傳回一或多個 IPv6 位址。如果要求的 URL 包含 IPv6 位址 (：：1（例如) ），則 IPv6 位址必須以方括弧括住 (HTTPs:// \[ ：： 1 \]) 。 範圍識別碼（有時稱為「區域索引」）支援為 IPv6 位址的一部分。 範圍識別碼是用來決定在具有多個網路介面的電腦上傳送要求時，所要使用的網路介面。 在主要 IPv6 位址 (fe80：： 1% 11 之後，使用 '% ' 字元指定範圍識別碼，例如) 。 不過，'% ' 字元必須在與 Internet Explorer 搭配使用的 URL 中進行換用。 例如，使用 Internet Explorer 時，連結-本機位址的範圍識別碼11會指定為 HTTPs:// \[ fe80：： 1% 2511 \] 。 Internet Explorer 7 和更新版本支援在 URL 中使用 IPv6 位址的功能。
ms.assetid: c3a8303a-50d6-4deb-a371-171ac0a7c5a9
title: 使用 Internet Explorer 來存取 IPv6 網站
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d11e7b207de132441d2152a4e0593b20bc00d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984233"
---
# <a name="using-internet-explorer-to-access-ipv6-websites"></a><span data-ttu-id="5e789-109">使用 Internet Explorer 來存取 IPv6 網站</span><span class="sxs-lookup"><span data-stu-id="5e789-109">Using Internet Explorer to Access IPv6 Websites</span></span>

<span data-ttu-id="5e789-110">Microsoft Internet Explorer 支援使用 IPv6 來連接及存取已啟用 IPv6 的網站 (網頁伺服器和 FTP 伺服器，例如在符合下列情況時) ：</span><span class="sxs-lookup"><span data-stu-id="5e789-110">Microsoft Internet Explorer supports using IPv6 to connect and access IPv6-enabled sites (web servers and FTP servers, for example) when the following circumstances are met:</span></span>

-   <span data-ttu-id="5e789-111">執行 Internet Explorer 的主機電腦必須安裝並啟用 IPv6。</span><span class="sxs-lookup"><span data-stu-id="5e789-111">The host machine running Internet Explorer must have IPv6 installed and enabled.</span></span>
    -   <span data-ttu-id="5e789-112">連接到位於本機子網上的主機時，提供連線的介面必須已指派可路由傳送的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="5e789-112">When connecting to a host that is outside of the local subnet, the interface that provides the connectivity must have a routable IPv6 address assigned.</span></span>
    -   <span data-ttu-id="5e789-113">連線至 IPv6 回送位址 (：： 1) 或連結-本機目的地時，不需要可路由傳送的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="5e789-113">When connecting to the IPv6 loopback address (::1) or to a link-local destination, a routable IPv6 address is not required.</span></span>
-   <span data-ttu-id="5e789-114">如果要求的 URL 包含名稱 (www.contoso.com，例如) ，則網域名稱系統 (DNS) 查詢該名稱必須傳回一或多個 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="5e789-114">If the requested URL contains a name (www.contoso.com, for example), the Domain Name System (DNS) query for that name must return one or more IPv6 addresses.</span></span>
-   <span data-ttu-id="5e789-115">如果要求的 URL 包含 IPv6 位址 (：：1（例如) ），則 IPv6 位址必須以方括弧括住 (HTTPs:// \[ ：： 1 \]) 。</span><span class="sxs-lookup"><span data-stu-id="5e789-115">If the requested URL contains an IPv6 address (::1, for example), the IPv6 address must be surrounded by square brackets (https://\[::1\]).</span></span> <span data-ttu-id="5e789-116">範圍識別碼（有時稱為「區域索引」）支援為 IPv6 位址的一部分。</span><span class="sxs-lookup"><span data-stu-id="5e789-116">Scope IDs, sometimes called zone indexes, are supported as part of the IPv6 address.</span></span> <span data-ttu-id="5e789-117">範圍識別碼是用來決定在具有多個網路介面的電腦上傳送要求時，所要使用的網路介面。</span><span class="sxs-lookup"><span data-stu-id="5e789-117">The scope ID is used to determine which network interface to use when sending the request on computers with multiple network interfaces.</span></span> <span data-ttu-id="5e789-118">在主要 IPv6 位址 (fe80：： 1% 11 之後，使用 '% ' 字元指定範圍識別碼，例如) 。</span><span class="sxs-lookup"><span data-stu-id="5e789-118">The scope ID is specified using the '%' character after the main IPv6 address (fe80::1%11, for example).</span></span> <span data-ttu-id="5e789-119">不過，'% ' 字元必須在與 Internet Explorer 搭配使用的 URL 中進行換用。</span><span class="sxs-lookup"><span data-stu-id="5e789-119">However, the '%' character must be escaped in the URL used with Internet Explorer.</span></span> <span data-ttu-id="5e789-120">例如，使用 Internet Explorer 時，連結-本機位址的範圍識別碼11會指定為 HTTPs:// \[ fe80：： 1% 2511 \] 。</span><span class="sxs-lookup"><span data-stu-id="5e789-120">For example, scope ID 11 on a link-local address would be specified as https://\[fe80::1%2511\] when using Internet Explorer.</span></span> <span data-ttu-id="5e789-121">Internet Explorer 7 和更新版本支援在 URL 中使用 IPv6 位址的功能。</span><span class="sxs-lookup"><span data-stu-id="5e789-121">This ability to use IPv6 addresses in a URL is supported on Internet Explorer 7 and later.</span></span>

> [!Note]  
> <span data-ttu-id="5e789-122">如果 Internet Explorer 設定為使用 proxy 伺服器，則 proxy 伺服器必須已指派 IPv6 位址，且 proxy 伺服器必須能夠 proxy 處理 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="5e789-122">If Internet Explorer is configured to use a proxy server, the proxy server must have an IPv6 address assigned and the proxy server must able to proxy IPv6 addresses.</span></span> <span data-ttu-id="5e789-123">Proxy 伺服器將用來連接到使用 IPv6 的外部主機。</span><span class="sxs-lookup"><span data-stu-id="5e789-123">The proxy server would be used to connect to an external host using IPv6.</span></span> <span data-ttu-id="5e789-124">通常會略過 IPv6 回送位址和 IPv6 連結-本機位址的 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="5e789-124">The proxy server would normally be bypassed for the IPv6 loopback address and IPv6 link-local addresses.</span></span>

 

 

 



