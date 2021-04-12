---
title: IP 版本6支援
description: 從 IE7 和更新版本開始，WinINet 支援主機名稱中的 IPv6 常值，以及 URI 的授權單位部分。
ms.assetid: cbbb9f93-15b0-4017-ac39-8a396203532e
keywords:
- IP 版本6支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed0857d9a0968bcd3e6c18e54623fb0c7d86cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382474"
---
# <a name="ip-version-6-support"></a><span data-ttu-id="79fd0-104">IP 版本6支援</span><span class="sxs-lookup"><span data-stu-id="79fd0-104">IP Version 6 Support</span></span>

<span data-ttu-id="79fd0-105">從 IE7 和更新版本開始，WinINet 支援主機名稱中的 IPv6 常值，以及 URI 的授權單位部分。</span><span class="sxs-lookup"><span data-stu-id="79fd0-105">Starting with IE7 and above, WinINet supports IPv6 literals in the hostname, and the authority component of the URI.</span></span> <span data-ttu-id="79fd0-106">WinINet 也支援在 HTTP 通訊協定的相關部分（例如，在 Location 標頭中）使用 IPv6 常值。</span><span class="sxs-lookup"><span data-stu-id="79fd0-106">WinINet also supports the use of IPv6 literals in relevant portions of the HTTP protocol, such as in the Location header.</span></span>

## <a name="hostname-ipv6-literals-and-uri-components"></a><span data-ttu-id="79fd0-107">主機名稱 IPv6 常值和 URI 元件</span><span class="sxs-lookup"><span data-stu-id="79fd0-107">Hostname IPv6 Literals and URI Components</span></span>

<span data-ttu-id="79fd0-108">WinINet 會根據 RFC 3513 中的規格來實行 IPv6 常值。</span><span class="sxs-lookup"><span data-stu-id="79fd0-108">WinINet implements IPv6 literals according to the specifications in RFC 3513.</span></span> <span data-ttu-id="79fd0-109">如這個 RFC 所指定，URI 中的 IPv6 常值必須以括弧括住。</span><span class="sxs-lookup"><span data-stu-id="79fd0-109">As specified in this RFC, IPv6 literals in a URI must be enclosed in brackets.</span></span> <span data-ttu-id="79fd0-110">例如，HTTPs:// \[ ：： 1 \] /是有效的 IPv6 URI; 不含括弧 (的格式無效 https://::1/) 。</span><span class="sxs-lookup"><span data-stu-id="79fd0-110">For example, https://\[::1\]/ is a valid IPv6 URI; the form without brackets (https://::1/) is not valid.</span></span> <span data-ttu-id="79fd0-111">不過，主機名稱 IPv6 常值不是 URI 的一部分，因此不需要用括弧括住;WinINet 可以接受兩種形式。</span><span class="sxs-lookup"><span data-stu-id="79fd0-111">Hostname IPv6 literals that are not part of the URI, however, do not need to be enclosed in the brackets; either form is acceptable to WinINet.</span></span> <span data-ttu-id="79fd0-112">例如，"：： 1" 和 " \[ ：： 1 \] " 是 IPv6 主機名稱常值的可接受形式。</span><span class="sxs-lookup"><span data-stu-id="79fd0-112">For example, both "::1" and "\[::1\]" are acceptable forms of IPv6 hostname literals.</span></span> <span data-ttu-id="79fd0-113">其他 Api （例如 WinSock API）也會接受這兩種形式。</span><span class="sxs-lookup"><span data-stu-id="79fd0-113">Other APIs, such as the WinSock API, will also accept both forms.</span></span> <span data-ttu-id="79fd0-114">因此，應用程式應該準備好處理這兩種形式的 IPv6 主機名稱常值。</span><span class="sxs-lookup"><span data-stu-id="79fd0-114">Thus applications should be prepared to handle both forms of IPv6 hostname literals.</span></span>

## <a name="scope-id"></a><span data-ttu-id="79fd0-115">範圍識別碼</span><span class="sxs-lookup"><span data-stu-id="79fd0-115">Scope ID</span></span>

<span data-ttu-id="79fd0-116">URI 中的 IPv6 常值位址可以包含範圍識別碼。</span><span class="sxs-lookup"><span data-stu-id="79fd0-116">The IPv6 literal address in the URI may include a scope ID.</span></span> <span data-ttu-id="79fd0-117">範圍識別碼可以是介面識別碼，例如 \[ FE80：： 1% 1 \] 。</span><span class="sxs-lookup"><span data-stu-id="79fd0-117">A scope ID can be an interface ID such as \[FE80::1%1\].</span></span> <span data-ttu-id="79fd0-118">URI 標準（記載于 RFC 3986 中）並不會定義範圍識別碼的語法，而在存在範圍識別碼時，URI 會視為非統一。</span><span class="sxs-lookup"><span data-stu-id="79fd0-118">The URI standard, documented in RFC 3986, does not define the syntax for the scope ID, and the URI is considered non-uniform when the scope ID is present.</span></span> <span data-ttu-id="79fd0-119">但是，WinINet 會接受 URI 的授權單位元件和主機名稱 IPv6 常值中的範圍識別碼。</span><span class="sxs-lookup"><span data-stu-id="79fd0-119">However, WinINet accepts a scope ID in the authority component of the URI, and in the hostname IPv6 literal.</span></span>

<span data-ttu-id="79fd0-120">存在於 URI 中時，IPv6 常值位址中的百分比字元 (% ) 必須是轉義百分比。</span><span class="sxs-lookup"><span data-stu-id="79fd0-120">The percent character (%) in the IPv6 literal address must be percent escaped when present in the URI.</span></span> <span data-ttu-id="79fd0-121">例如，範圍識別碼 FE80：： 2% 3 必須以 "HTTPs:// \[ FE80：： 2% 253/" 的 URI 形式出現 \] ，其中 %25 是十六進位編碼百分比字元 (% ) 。</span><span class="sxs-lookup"><span data-stu-id="79fd0-121">For example, the scope ID FE80::2%3, must appear in the URI as "https://\[FE80::2%253\]/", where %25 is the hex encoded percent character (%).</span></span> <span data-ttu-id="79fd0-122">如果應用程式從 Unicode API （例如 Winsock [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) API）抓取 URI，則應用程式必須在 URI 的主機名稱中加入% 字元 (% ) 的轉義版本。</span><span class="sxs-lookup"><span data-stu-id="79fd0-122">If the application retrieves the URI from a Unicode API, such as the Winsock [**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) API, the application must add the escaped version of the percent character (%) in the hostname of the URI.</span></span> <span data-ttu-id="79fd0-123">若要建立 URI 的轉義版本，應用程式會呼叫 [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) ，並將 *dwFlags* 參數設定為 **ICU \_ ESCAPE \_ 授權** 單位，以及在 *lpUrlComponents* 參數中指定的 URL 元件結構中指定的 IPv6 主機名稱。</span><span class="sxs-lookup"><span data-stu-id="79fd0-123">To create the escaped version of the URI, applications call [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) with the *dwFlags* parameter set to **ICU\_ESCAPE\_AUTHORITY**, and the IPv6 hostname specified in the URL components structure specified in the *lpUrlComponents* parameter.</span></span>

<span data-ttu-id="79fd0-124">針對所有通訊端作業，WinINet 會使用範圍識別碼。</span><span class="sxs-lookup"><span data-stu-id="79fd0-124">For all sockets operations, WinINet uses the scope ID.</span></span> <span data-ttu-id="79fd0-125">不過，因為範圍識別碼只有本機主機的重要性，所以不會在要求中做為 HTTP 通訊協定標頭的一部分傳送。</span><span class="sxs-lookup"><span data-stu-id="79fd0-125">However, because the scope ID has only local host significance, it is not sent as part of the HTTP protocol headers in the request.</span></span> <span data-ttu-id="79fd0-126">例如，呼叫 [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) 時，會以 *lpszUrl* 參數中的下列 URL 呼叫。</span><span class="sxs-lookup"><span data-stu-id="79fd0-126">For example, the call to [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) is called with the following URL in the *lpszUrl* parameter.</span></span>

``` syntax
https://[fec0::2%251]:80/path.htm
```

<span data-ttu-id="79fd0-127">傳送此 URL 的 HTTP 要求時，WinINet 會移除 URL 的範圍識別碼部分。</span><span class="sxs-lookup"><span data-stu-id="79fd0-127">The scope ID portion of the URL is removed by WinINet when the HTTP request is sent for this URL.</span></span> <span data-ttu-id="79fd0-128">要求包含下列標頭：</span><span class="sxs-lookup"><span data-stu-id="79fd0-128">The request contains the following headers:</span></span>

``` syntax
GET path.htm HTTP/1.1
Host: [fec0::2]
```

> [!Note]  
> <span data-ttu-id="79fd0-129">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="79fd0-129">WinINet does not support server implementations.</span></span> <span data-ttu-id="79fd0-130">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="79fd0-130">In addition, it should not be used from a service.</span></span> <span data-ttu-id="79fd0-131">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="79fd0-131">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 