---
description: Windows 通訊端1.1 定義了數個常式，用於 TCP/IP 網路的 IPv4 名稱解析。 這些通常稱為 GetXbyY 函式，並包含下列各項。
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: Windows 通訊端 1.1 SPI 中 TCP/IP 的相容名稱解析
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ca58f8868c17c9dad7c67fed083e9460272944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973644"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a><span data-ttu-id="84cbd-104">Windows 通訊端 1.1 SPI 中 TCP/IP 的相容名稱解析</span><span class="sxs-lookup"><span data-stu-id="84cbd-104">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 SPI</span></span>

<span data-ttu-id="84cbd-105">Windows 通訊端1.1 定義了數個常式，用於 TCP/IP 網路的 IPv4 名稱解析。</span><span class="sxs-lookup"><span data-stu-id="84cbd-105">Windows Sockets 1.1 defined a number of routines that were used for IPv4 name resolution with TCP/IP networks.</span></span> <span data-ttu-id="84cbd-106">這些通常稱為 **GetXbyY** 函式，並包含下列各項。</span><span class="sxs-lookup"><span data-stu-id="84cbd-106">These are customarily called the **GetXbyY** functions and include the following.</span></span>

[<span data-ttu-id="84cbd-107">**gethostname**</span><span class="sxs-lookup"><span data-stu-id="84cbd-107">**gethostname**</span></span>](/windows/desktop/api/winsock/nf-winsock-gethostname)

[<span data-ttu-id="84cbd-108">**gethostbyaddr**</span><span class="sxs-lookup"><span data-stu-id="84cbd-108">**gethostbyaddr**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)

[<span data-ttu-id="84cbd-109">**gethostbyname**</span><span class="sxs-lookup"><span data-stu-id="84cbd-109">**gethostbyname**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)

[<span data-ttu-id="84cbd-110">**getprotobyname**</span><span class="sxs-lookup"><span data-stu-id="84cbd-110">**getprotobyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobyname)

[<span data-ttu-id="84cbd-111">**getprotobynumber**</span><span class="sxs-lookup"><span data-stu-id="84cbd-111">**getprotobynumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)

[<span data-ttu-id="84cbd-112">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="84cbd-112">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)

[<span data-ttu-id="84cbd-113">**getservbyport**</span><span class="sxs-lookup"><span data-stu-id="84cbd-113">**getservbyport**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyport)

<span data-ttu-id="84cbd-114">這些函數的非同步版本也已定義。</span><span class="sxs-lookup"><span data-stu-id="84cbd-114">Asynchronous versions of these functions were also defined.</span></span>

[<span data-ttu-id="84cbd-115">**WSAAsyncGetHostByAddr**</span><span class="sxs-lookup"><span data-stu-id="84cbd-115">**WSAAsyncGetHostByAddr**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)

[<span data-ttu-id="84cbd-116">**WSAAsyncGetHostByName**</span><span class="sxs-lookup"><span data-stu-id="84cbd-116">**WSAAsyncGetHostByName**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)

[<span data-ttu-id="84cbd-117">**WSAAsyncGetProtoByName**</span><span class="sxs-lookup"><span data-stu-id="84cbd-117">**WSAAsyncGetProtoByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)

[<span data-ttu-id="84cbd-118">**WSAAsyncGetProtoByNumber**</span><span class="sxs-lookup"><span data-stu-id="84cbd-118">**WSAAsyncGetProtoByNumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)

[<span data-ttu-id="84cbd-119">**WSAAsyncGetServByName**</span><span class="sxs-lookup"><span data-stu-id="84cbd-119">**WSAAsyncGetServByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)

[<span data-ttu-id="84cbd-120">**WSAAsyncGetServByPort**</span><span class="sxs-lookup"><span data-stu-id="84cbd-120">**WSAAsyncGetServByPort**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)

<span data-ttu-id="84cbd-121">這些函式僅適用于 TCP/IP 網路;不建議使用與通訊協定無關的應用程式開發人員繼續使用這些傳輸特有的功能。</span><span class="sxs-lookup"><span data-stu-id="84cbd-121">These functions are specific to TCP/IP networks; developers of protocol-independent applications are discouraged from continuing to utilize these transport-specific functions.</span></span> <span data-ttu-id="84cbd-122">不過，若要保留與 Windows 通訊端1.1 的嚴格回溯相容性，只要至少有一個命名空間提供者支援 AF INET 位址系列，就會繼續支援上述函數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="84cbd-122">However, to retain strict backward compatibility with Windows Sockets 1.1, the preceding functions continue to be supported as long as at least one namespace provider is present that supports the AF\_INET address family.</span></span>

<span data-ttu-id="84cbd-123">*Ws2 \_32.dll* 使用適當的 [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)、 [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)、 [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)函數呼叫順序，來實作為新的通訊協定獨立名稱解析設備的相容性函數。</span><span class="sxs-lookup"><span data-stu-id="84cbd-123">The *Ws2\_32.dll* implements these compatibility functions in terms of the new, protocol-independent name resolution facilities using an appropriate sequence of [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) function calls.</span></span> <span data-ttu-id="84cbd-124">以下提供 **GetXbyY** 函式如何對應至名稱解析函式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="84cbd-124">The details of how the **GetXbyY** functions are mapped to name resolution functions are provided below.</span></span> <span data-ttu-id="84cbd-125">Ws2 \_32.dll 會處理 **GetXbyY** 函數的非同步和同步版本之間的差異，因此只會討論同步 **GetXbyY** 函式的執行。</span><span class="sxs-lookup"><span data-stu-id="84cbd-125">The Ws2\_32.dll handles the differences between the asynchronous and synchronous versions of the **GetXbyY** functions, so that only the implementation of the synchronous **GetXbyY** functions are discussed.</span></span>

 

 
