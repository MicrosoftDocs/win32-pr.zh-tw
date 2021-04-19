---
description: 為了充分利用已啟用 IPv6 的函式，IT 系統管理員必須在其 WPAD 腳本內定義，此函式稱為 FindProxyForURLEx (url，主機) ，其將取代舊版 FindProxyForUrl (url、host) 函數。
ms.assetid: e531a66d-5c50-4065-a12a-783fd4d1d310
title: IPv6-Aware Proxy 協助程式 API 定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b1ff5a0c287327593e65e29a0b03cfb59269f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988966"
---
# <a name="ipv6-aware-proxy-helper-api-definitions"></a><span data-ttu-id="c7fef-103">IPv6-Aware Proxy 協助程式 API 定義</span><span class="sxs-lookup"><span data-stu-id="c7fef-103">IPv6-Aware Proxy Helper API Definitions</span></span>

<span data-ttu-id="c7fef-104">為了充分利用已啟用 IPv6 的函式，IT 系統管理員必須在其 WPAD 腳本內定義，此函式稱為 FindProxyForURLEx (url，主機) ，其將取代舊版 FindProxyForUrl (url、host) 函數。</span><span class="sxs-lookup"><span data-stu-id="c7fef-104">In order to take advantage of the IPv6 enabled functions, IT administrators must define within their WPAD script, a function called FindProxyForURLEx (url, host) which will replace the legacy FindProxyForUrl (url, host) function.</span></span> <span data-ttu-id="c7fef-105">只有在新的 FindProxyForURLEx 函式中，系統管理員才能執行新的功能。</span><span class="sxs-lookup"><span data-stu-id="c7fef-105">Only from the new FindProxyForURLEx function will administrators be able to execute the new functions.</span></span>

<span data-ttu-id="c7fef-106">我們也嘗試簡化開發人員的工作，方法是讓我們的函式以與其他網路元件相同的喜好設定順序傳回不同類型的 IP 位址，特別是 IPv6 位址，後面接著 IPv4 位址 (亦即 Winsock getaddrinfo ( 的目前行為。) 函式) 。</span><span class="sxs-lookup"><span data-stu-id="c7fef-106">We also attempted to simplify work for developers, by aligning our functions to return different types of IP addresses in the same order of preference as other networking components, specifically IPv6 addresses followed by IPv4 addresses (i.e. current behavior for Winsock’s getaddrinfo(..) function).</span></span>

<span data-ttu-id="c7fef-107">下列函式是導覽 [器 Proxy 自動設定 (PAC) 檔案格式規格](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) 的擴充功能，可讓 WPAD 腳本處理具備 IPv6 功能的網路。</span><span class="sxs-lookup"><span data-stu-id="c7fef-107">The following functions are extensions to the [Navigator Proxy Auto-Config (PAC) File Format specification](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) to enable WPAD scripts to handle IPv6 capable networks.</span></span>

## <a name="predefined-functions-and-environment-for-the-javascript-function-findproxyforurlex"></a><span data-ttu-id="c7fef-108">JavaScript 函式 FindProxyforURLEx 的預先定義函數和環境</span><span class="sxs-lookup"><span data-stu-id="c7fef-108">Predefined Functions and Environment for the JavaScript Function FindProxyforURLEx</span></span>

<span data-ttu-id="c7fef-109">以主機名稱為基礎的條件</span><span class="sxs-lookup"><span data-stu-id="c7fef-109">Hostname based conditions</span></span>

<dl> <dt>

[<span data-ttu-id="c7fef-110">**isResolvableEx**</span><span class="sxs-lookup"><span data-stu-id="c7fef-110">**isResolvableEx**</span></span>](isresolvableex.md)
</dt> <dd>

<span data-ttu-id="c7fef-111">判斷指定的主機字串是否可解析為 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c7fef-111">Determines if a given host string can resolve to an IP address.</span></span>

</dd> <dt>

[<span data-ttu-id="c7fef-112">**isInNetEx**</span><span class="sxs-lookup"><span data-stu-id="c7fef-112">**isInNetEx**</span></span>](isinnetex.md)
</dt> <dd>

<span data-ttu-id="c7fef-113">判斷 IP 位址是否在特定子網中。</span><span class="sxs-lookup"><span data-stu-id="c7fef-113">Determines if an IP address is in a specific subnet.</span></span>

</dd> </dl>

<span data-ttu-id="c7fef-114">相關公用程式函式</span><span class="sxs-lookup"><span data-stu-id="c7fef-114">Related utility functions</span></span>

<dl> <dt>

[<span data-ttu-id="c7fef-115">**dnsResolveEx**</span><span class="sxs-lookup"><span data-stu-id="c7fef-115">**dnsResolveEx**</span></span>](dnsresolveex.md)
</dt> <dd>

<span data-ttu-id="c7fef-116">將主機字串解析為其 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c7fef-116">Resolve a host string to its IP address.</span></span>

</dd> <dt>

[<span data-ttu-id="c7fef-117">**myIPAddressEx**</span><span class="sxs-lookup"><span data-stu-id="c7fef-117">**myIPAddressEx**</span></span>](myipaddressex.md)
</dt> <dd>

<span data-ttu-id="c7fef-118">尋找 localhost 的所有 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c7fef-118">Finds all the IP addresses for localhost.</span></span>

</dd> <dt>

[<span data-ttu-id="c7fef-119">**sortIpAddressList**</span><span class="sxs-lookup"><span data-stu-id="c7fef-119">**sortIpAddressList**</span></span>](sortipaddresslist.md)
</dt> <dd>

<span data-ttu-id="c7fef-120">排序 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="c7fef-120">Sorts a list of IP addresses.</span></span>

</dd> <dt>

[<span data-ttu-id="c7fef-121">**getClientVersion**</span><span class="sxs-lookup"><span data-stu-id="c7fef-121">**getClientVersion**</span></span>](getclientversion.md)
</dt> <dd>

<span data-ttu-id="c7fef-122">取得 WPAD 處理引擎的版本。</span><span class="sxs-lookup"><span data-stu-id="c7fef-122">Gets the version of the WPAD processing engine.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="c7fef-123">這種功能需要 Windows Internet Explorer 7 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="c7fef-123">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



