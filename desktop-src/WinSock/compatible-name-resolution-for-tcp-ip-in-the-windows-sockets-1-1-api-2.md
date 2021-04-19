---
description: 請注意，名稱解析的所有 Windows 通訊端1.1 函式都是 IPv4 TCP/IP 網路專用的。
ms.assetid: 5a2a37f3-85c5-4b27-9ce3-f5b707b1564a
title: Windows 通訊端 1.1 API 中 TCP/IP 的相容名稱解析
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2447590b25861abc80bd0a89be173272fb809814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973463"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-api"></a><span data-ttu-id="5d6e3-103">Windows 通訊端 1.1 API 中 TCP/IP 的相容名稱解析</span><span class="sxs-lookup"><span data-stu-id="5d6e3-103">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>

> [!Note]  
> <span data-ttu-id="5d6e3-104">所有適用于名稱解析的 Windows 通訊端1.1 函式都是 IPv4 TCP/IP 網路專用的功能。</span><span class="sxs-lookup"><span data-stu-id="5d6e3-104">All of the Windows Sockets 1.1 functions for name resolution are specific to IPv4 TCP/IP networks.</span></span> <span data-ttu-id="5d6e3-105">應用程式開發人員強烈建議您繼續使用這些僅支援 IPv4 的傳輸特定功能。</span><span class="sxs-lookup"><span data-stu-id="5d6e3-105">Application developers are strongly discouraged from continuing to utilize these transport-specific functions that only support IPv4.</span></span>

 

<span data-ttu-id="5d6e3-106">應用程式開發人員應該使用與通訊協定無關的下列功能，並同時支援 IPv6 和 IPv4 名稱解析。</span><span class="sxs-lookup"><span data-stu-id="5d6e3-106">Application developers should be using the following functions that are protocol-independent and support both IPv6 and IPv4 name resolution.</span></span>

-   [<span data-ttu-id="5d6e3-107">**getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-107">**getaddrinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
-   [<span data-ttu-id="5d6e3-108">**GetAddrInfoEx**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-108">**GetAddrInfoEx**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
-   [<span data-ttu-id="5d6e3-109">**GetAddrInfoW**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-109">**GetAddrInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
-   [<span data-ttu-id="5d6e3-110">**getnameinfo**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-110">**getnameinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
-   [<span data-ttu-id="5d6e3-111">**GetNameInfoW**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-111">**GetNameInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)

<span data-ttu-id="5d6e3-112">Windows 通訊端1.1 定義了數個用來搭配 TCP/IP (IP 第4版) 網路進行名稱解析的常式。</span><span class="sxs-lookup"><span data-stu-id="5d6e3-112">Windows Sockets 1.1 defined a number of routines used for name resolution with TCP/IP (IP version 4) networks.</span></span> <span data-ttu-id="5d6e3-113">這些有時稱為 **getXbyY** 函式，並包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="5d6e3-113">These are sometimes called the **getXbyY** functions and include the following:</span></span>

<dl>

[<span data-ttu-id="5d6e3-114">**gethostname**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-114">**gethostname**</span></span>](/windows/desktop/api/winsock/nf-winsock-gethostname)  
[<span data-ttu-id="5d6e3-115">**gethostbyaddr**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-115">**gethostbyaddr**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)  
[<span data-ttu-id="5d6e3-116">**gethostbyname**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-116">**gethostbyname**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)  
[<span data-ttu-id="5d6e3-117">**getprotobyname**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-117">**getprotobyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobyname)  
[<span data-ttu-id="5d6e3-118">**getprotobynumber**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-118">**getprotobynumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)  
[<span data-ttu-id="5d6e3-119">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-119">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)  
[<span data-ttu-id="5d6e3-120">**getservbyport**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-120">**getservbyport**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyport)  
</dl>

<span data-ttu-id="5d6e3-121">這些函數的非同步版本也已定義。</span><span class="sxs-lookup"><span data-stu-id="5d6e3-121">Asynchronous versions of these functions were also defined.</span></span>

<dl>

[<span data-ttu-id="5d6e3-122">**WSAAsyncGetHostByAddr**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-122">**WSAAsyncGetHostByAddr**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)  
[<span data-ttu-id="5d6e3-123">**WSAAsyncGetHostByName**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-123">**WSAAsyncGetHostByName**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)  
[<span data-ttu-id="5d6e3-124">**WSAAsyncGetProtoByName**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-124">**WSAAsyncGetProtoByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)  
[<span data-ttu-id="5d6e3-125">**WSAAsyncGetProtoByNumber**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-125">**WSAAsyncGetProtoByNumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)  
[<span data-ttu-id="5d6e3-126">**WSAAsyncGetServByName**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-126">**WSAAsyncGetServByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)  
[<span data-ttu-id="5d6e3-127">**WSAAsyncGetServByPort**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-127">**WSAAsyncGetServByPort**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)  
</dl>

<span data-ttu-id="5d6e3-128">另外還有兩個函式（現在會在 Winsock2.dll 中執行），分別用來將類似的 Ipv4 位址標記法轉換成字串和二進位標記法。</span><span class="sxs-lookup"><span data-stu-id="5d6e3-128">There are also two functions, now implemented in the Winsock2.dll, used to convert dotted Ipv4 address notation to and from string and binary representations, respectively.</span></span>

<dl>

[<span data-ttu-id="5d6e3-129">**inet \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-129">**inet\_addr**</span></span>](/windows/win32/api/winsock2/nf-winsock2-inet_addr)  
[<span data-ttu-id="5d6e3-130">**inet \_ ntoa**</span><span class="sxs-lookup"><span data-stu-id="5d6e3-130">**inet\_ntoa**</span></span>](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)  
</dl>

<span data-ttu-id="5d6e3-131">為了保持與 Windows 通訊端1.1 的嚴格回溯相容性，只要至少有一個命名空間提供者支援 AF INET 位址系列，就會繼續支援所有舊的 IPv4 函式 (這些函式與 \_ IP 版本6（以 AF INET6) 表示）無關 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5d6e3-131">In order to retain strict backward compatibility with Windows Sockets 1.1, all of the older IPv4-only functions continue to be supported as long as at least one namespace provider is present that supports the AF\_INET address family (these functions are not relevant to IP version 6, denoted by AF\_INET6).</span></span>

<span data-ttu-id="5d6e3-132">Ws2 \_32.dll 會使用適當的 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) / **下一個** / **End** 函數呼叫順序，來實作為新的通訊協定獨立名稱解析設備的相容性功能。</span><span class="sxs-lookup"><span data-stu-id="5d6e3-132">The Ws2\_32.dll implements these compatibility functions in terms of the new, protocol-independent name resolution facilities using an appropriate sequence of [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)/**Next**/**End** function calls.</span></span> <span data-ttu-id="5d6e3-133">以下提供 **getXbyY** 函式如何對應至名稱解析函式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5d6e3-133">The details of how the **getXbyY** functions are mapped to name resolution functions are provided below.</span></span> <span data-ttu-id="5d6e3-134">WSs2 \_32.dll 會處理 **getXbyY** 函數的非同步和同步版本之間的差異，因此只會討論同步 **getXbyY** 函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="5d6e3-134">The WSs2\_32.dll handles the differences between the asynchronous and synchronous versions of the **getXbyY** functions, so only the implementation of the synchronous **getXbyY** functions are discussed.</span></span>

<span data-ttu-id="5d6e3-135">本節說明 Windows 通訊端 1.1 API 中 TCP/IP 的相容名稱解析。</span><span class="sxs-lookup"><span data-stu-id="5d6e3-135">This section describes compatible name resolution for TCP/IP in the Windows Sockets 1.1 API.</span></span> <span data-ttu-id="5d6e3-136">下列清單說明本節中的主題：</span><span class="sxs-lookup"><span data-stu-id="5d6e3-136">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="5d6e3-137">API 中的 GetXbyY 基本方法</span><span class="sxs-lookup"><span data-stu-id="5d6e3-137">Basic Approach for GetXbyY in the API</span></span>](basic-approach-for-getxbyy-in-the-api-2.md)
-   [<span data-ttu-id="5d6e3-138">API 中的 getprotobyname 和 getprotobynumber 函式</span><span class="sxs-lookup"><span data-stu-id="5d6e3-138">getprotobyname and getprotobynumber Functions in the API</span></span>](getprotobyname-and-getprotobynumber-functions-in-the-api-2.md)
-   [<span data-ttu-id="5d6e3-139">API 中的 getservbyname 和 getservbyport 函式</span><span class="sxs-lookup"><span data-stu-id="5d6e3-139">getservbyname and getservbyport Functions in the API</span></span>](getservbyname-and-getservbyport-functions-in-the-api-2.md)
-   [<span data-ttu-id="5d6e3-140">API 中的 gethostbyname 函式</span><span class="sxs-lookup"><span data-stu-id="5d6e3-140">gethostbyname Function in the API</span></span>](gethostbyname-function-in-the-api-2.md)
-   [<span data-ttu-id="5d6e3-141">API 中的 gethostbyaddr 函式</span><span class="sxs-lookup"><span data-stu-id="5d6e3-141">gethostbyaddr Function in the API</span></span>](gethostbyaddr-function-in-the-api-2.md)
-   [<span data-ttu-id="5d6e3-142">API 中的 gethostname 函式</span><span class="sxs-lookup"><span data-stu-id="5d6e3-142">gethostname Function in the API</span></span>](gethostname-function-in-the-api-2.md)

## <a name="related-topics"></a><span data-ttu-id="5d6e3-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="5d6e3-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d6e3-144">通訊協定獨立名稱解析</span><span class="sxs-lookup"><span data-stu-id="5d6e3-144">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="5d6e3-145">註冊和名稱解析</span><span class="sxs-lookup"><span data-stu-id="5d6e3-145">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
