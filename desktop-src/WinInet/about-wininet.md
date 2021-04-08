---
title: 關於 WinINet
description: Windows Internet (WinINet) 應用程式開發介面 (API) 可讓您的應用程式與 FTP 和 HTTP 通訊協定互動以存取網際網路資源。
ms.assetid: 0a06f2af-957a-4dff-a8cc-187370181b5c
keywords:
- 關於 WinINet WinINet
- WinINet WinINet，關於
- WinINet WinINet，起始頁
- Windows 網際網路 WinINet
- 網際網路，Windows 網際網路 WinINet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4513e5c3912a483fd4dbef96f452c5712717c8a5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "103932968"
---
# <a name="about-wininet"></a><span data-ttu-id="6d544-108">關於 WinINet</span><span class="sxs-lookup"><span data-stu-id="6d544-108">About WinINet</span></span>

> [!NOTE]
> <span data-ttu-id="6d544-109">針對應用程式容器，自 Windows 10，版本1709，HTTP/2 (請參閱 [RFC7540](https://tools.ietf.org/html/rfc7540)) 預設為開啟。</span><span class="sxs-lookup"><span data-stu-id="6d544-109">For app containers since Windows 10, version 1709, HTTP/2 (see [RFC7540](https://tools.ietf.org/html/rfc7540)) is on by default.</span></span>

<span data-ttu-id="6d544-110">Windows Internet (WinINet) 應用程式開發介面 (API) 可讓您的應用程式與 FTP 和 HTTP 通訊協定互動以存取網際網路資源。</span><span class="sxs-lookup"><span data-stu-id="6d544-110">The Windows Internet (WinINet) application programming interface (API) enables your application to interact with FTP and HTTP protocols to access Internet resources.</span></span> <span data-ttu-id="6d544-111">當標準演進時，這些函式會處理基礎通訊協定中的變更，讓它們能夠維持一致的行為。</span><span class="sxs-lookup"><span data-stu-id="6d544-111">As standards evolve, these functions handle the changes in underlying protocols, enabling them to maintain consistent behavior.</span></span>

<span data-ttu-id="6d544-112">**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：** 也啟用了與 Gopher 互動的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6d544-112">**Windows XP and Windows Server 2003 R2 and earlier:** Also enabled applications to interact with Gopher.</span></span>

<span data-ttu-id="6d544-113">如需詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="6d544-113">For more information, see:</span></span>

-   [<span data-ttu-id="6d544-114">WinINet 與 WinHTTP</span><span class="sxs-lookup"><span data-stu-id="6d544-114">WinINet vs. WinHTTP</span></span>](wininet-vs-winhttp.md)
-   [<span data-ttu-id="6d544-115">HINTERNET 控制碼</span><span class="sxs-lookup"><span data-stu-id="6d544-115">HINTERNET Handles</span></span>](appendix-a-hinternet-handles.md)
-   [<span data-ttu-id="6d544-116">IP 版本6支援</span><span class="sxs-lookup"><span data-stu-id="6d544-116">IP Version 6 Support</span></span>](ip-version-6-support.md)
-   [<span data-ttu-id="6d544-117">內容 \_ 編碼</span><span class="sxs-lookup"><span data-stu-id="6d544-117">Content\_Encoding</span></span>](content-encoding.md)
-   [<span data-ttu-id="6d544-118">Caching</span><span class="sxs-lookup"><span data-stu-id="6d544-118">Caching</span></span>](caching.md)
-   [<span data-ttu-id="6d544-119">一般函數</span><span class="sxs-lookup"><span data-stu-id="6d544-119">Common Functions</span></span>](common-functions.md)
-   [<span data-ttu-id="6d544-120">FTP 會話</span><span class="sxs-lookup"><span data-stu-id="6d544-120">FTP Sessions</span></span>](ftp-sessions.md)
-   [<span data-ttu-id="6d544-121">HTTP 會話</span><span class="sxs-lookup"><span data-stu-id="6d544-121">HTTP Sessions</span></span>](http-sessions.md)
-   [<span data-ttu-id="6d544-122">HTTP Cookie</span><span class="sxs-lookup"><span data-stu-id="6d544-122">HTTP Cookies</span></span>](http-cookies.md)
-   [<span data-ttu-id="6d544-123">非同步作業</span><span class="sxs-lookup"><span data-stu-id="6d544-123">Asynchronous Operation</span></span>](asynchronous-operation.md)
-   [<span data-ttu-id="6d544-124">處理驗證</span><span class="sxs-lookup"><span data-stu-id="6d544-124">Handling Authentication</span></span>](handling-authentication.md)
-   [<span data-ttu-id="6d544-125">處理統一資源定位器</span><span class="sxs-lookup"><span data-stu-id="6d544-125">Handling Uniform Resource Locators</span></span>](handling-uniform-resource-locators.md)
-   [<span data-ttu-id="6d544-126">安全性 \_ 指導方針</span><span class="sxs-lookup"><span data-stu-id="6d544-126">Security\_Guideline</span></span>](security-guidelines.md)

## <a name="internet-protocols"></a><span data-ttu-id="6d544-127">網際網路通訊協定</span><span class="sxs-lookup"><span data-stu-id="6d544-127">Internet Protocols</span></span>

<span data-ttu-id="6d544-128">這兩個主要的網際網路通訊協定是 FTP 和 HTTP。</span><span class="sxs-lookup"><span data-stu-id="6d544-128">The two primary Internet protocols are FTP and HTTP.</span></span> <span data-ttu-id="6d544-129">如需這些通訊協定的詳細資訊，請參閱適用于 FTP 和 HTTP 的 (RFC) 檔的批註要求：</span><span class="sxs-lookup"><span data-stu-id="6d544-129">For more information about these protocols, see the Request For Comments (RFC) documents for FTP and HTTP:</span></span>

-   <span data-ttu-id="6d544-130">[RFC 959](https://www.ietf.org/rfc/rfc0959.txt)， *檔案傳輸通訊協定 (FTP)*。</span><span class="sxs-lookup"><span data-stu-id="6d544-130">[RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *File Transfer Protocol (FTP)*.</span></span>
-   <span data-ttu-id="6d544-131">[RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt)， *超文字傳輸通訊協定-HTTP/1.0*。</span><span class="sxs-lookup"><span data-stu-id="6d544-131">[RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Hypertext Transfer Protocol - HTTP/1.0*.</span></span>
-   <span data-ttu-id="6d544-132">[RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)， *超文字傳輸通訊協定-HTTP/1.1*。</span><span class="sxs-lookup"><span data-stu-id="6d544-132">[RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Hypertext Transfer Protocol - HTTP/1.1*.</span></span>

> [!NOTE]  
> <span data-ttu-id="6d544-133"> (這些資源可能無法在某些語言及國家/地區使用。 ) </span><span class="sxs-lookup"><span data-stu-id="6d544-133">(These resources may not be available in some languages and countries.)</span></span>

<span data-ttu-id="6d544-134">**WINDOWS XP 和 Windows Server 2003 R2 和更早版本：** 此外也支援 Gopher 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6d544-134">**Windows XP and Windows Server 2003 R2 and earlier:** The Gopher protocol was also supported.</span></span> <span data-ttu-id="6d544-135">請參閱 [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt)（ *網際網路 Gopher 通訊協定*）。</span><span class="sxs-lookup"><span data-stu-id="6d544-135">See [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *The Internet Gopher Protocol*.</span></span>
