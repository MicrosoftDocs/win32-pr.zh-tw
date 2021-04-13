---
description: 與 Windows 通訊端1.1 搭配使用的原始 include 檔是 Winsock. h 標頭檔。
ms.assetid: 0536abcc-4277-4bd8-927c-3bf429bc65bb
title: 包含檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf7a4edcd70e6a6280b26f7b6ab9f0f1dab674e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318376"
---
# <a name="include-files"></a><span data-ttu-id="bf279-103">包含檔案</span><span class="sxs-lookup"><span data-stu-id="bf279-103">Include Files</span></span>

<span data-ttu-id="bf279-104">與 Windows 通訊端1.1 搭配使用的原始 include 檔是 *Winsock. h* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="bf279-104">The original include file for use with Windows Sockets 1.1 was the *Winsock.h* header file.</span></span> <span data-ttu-id="bf279-105">為了讓您能夠輕鬆地根據 Berkeley UNIX 通訊端將現有的原始程式碼移植到 Windows sockets，我們鼓勵使用 Winsock 1.1 的 Windows 通訊端開發工具組，以與標準 UNIX (include 檔案相同的名稱，在 *sys/socket. h* 和 arpa/inet .h 標頭檔中提供，例如) 。</span><span class="sxs-lookup"><span data-stu-id="bf279-105">To ease porting existing source code based on Berkeley UNIX sockets to Windows sockets, Windows Sockets development kits for Winsock 1.1 were encouraged to be supplied with several include files with the same names as standard UNIX include files (the *sys/socket.h* and arpa/inet.h header files, for example).</span></span> <span data-ttu-id="bf279-106">不過，這些類似名稱的 Winsock 標頭檔只會包含指示詞，以包含 *Winsock2* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="bf279-106">However, these similarly-name Winsock header files merely contained a directive to include the *Winsock2.h* header file.</span></span>

<span data-ttu-id="bf279-107">當 Windows 通訊端2發行時，與 Windows 通訊端搭配使用的主要 include 檔案已重新命名為 *Winsock2. h*。</span><span class="sxs-lookup"><span data-stu-id="bf279-107">When Windows Sockets 2 was released, the primary include file for use with Windows Sockets was renamed to *Winsock2.h*.</span></span> <span data-ttu-id="bf279-108">Winsock 1.1 舊的原始 *winsock. h* 標頭檔也會保留，以與繼承應用程式相容。</span><span class="sxs-lookup"><span data-stu-id="bf279-108">The older original *Winsock.h* header file for Winsock 1.1 was also retained for compatibility with older applications.</span></span> <span data-ttu-id="bf279-109">從 Windows 2000 發行之後，已淘汰 Winsock 1.1 相容應用程式的開發。</span><span class="sxs-lookup"><span data-stu-id="bf279-109">The development of Winsock 1.1 compatible applications has been deprecated since Windows 2000 was released.</span></span> <span data-ttu-id="bf279-110">所有應用程式現在都應該使用 Winsock 應用程式原始程式檔中的 [include *Winsock2 .h* ] 指示詞。</span><span class="sxs-lookup"><span data-stu-id="bf279-110">All applications should now use use the include *Winsock2.h* directive in Winsock application source files.</span></span>

<span data-ttu-id="bf279-111">*Winsock2* 標頭檔包含大部分的 Winsock 函數、結構和定義。</span><span class="sxs-lookup"><span data-stu-id="bf279-111">The *Winsock2.h* header file contains most of the Winsock functions, structures, and definitions.</span></span> <span data-ttu-id="bf279-112">*Ws2tcpip .h* 標頭檔包含 WinSock 2 Protocol-Specific 附錄檔中針對 tcp/ip 所引進的定義，其中包含用來抓取 IP 位址的較新函數和結構。</span><span class="sxs-lookup"><span data-stu-id="bf279-112">The *Ws2tcpip.h* header file contains definitions introduced in the WinSock 2 Protocol-Specific Annex document for TCP/IP that includes newer functions and structures used to retrieve IP addresses.</span></span> <span data-ttu-id="bf279-113">這些包含 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 和 [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) 系列的函式，可為 IPv4 或 IPv6 位址提供名稱解析。</span><span class="sxs-lookup"><span data-stu-id="bf279-113">These include the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) family of functions that provide name resolution for both IPv4 or IPv6 addresses.</span></span> <span data-ttu-id="bf279-114">只有當應用程式需要這些 IP 中立的命名函式時，才需要 *Ws2tcpip .h* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="bf279-114">The *Ws2tcpip.h* header file is only needed if these IP-agnostic naming functions are required by the application.</span></span>

<span data-ttu-id="bf279-115">*Mswsock* 標頭檔包含 Windows 通訊端 2 ([**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile)、 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)和 [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)的 Microsoft 特定擴充功能的定義，例如) 。</span><span class="sxs-lookup"><span data-stu-id="bf279-115">The *Mswsock.h* header file contains definitions for Microsoft-specific extensions to the Windows Sockets 2 ([**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), and [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), for example).</span></span> <span data-ttu-id="bf279-116">除非應用程式使用這些 Microsoft 專屬的延伸模組，否則通常不需要 *Mswsock .h* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="bf279-116">The *Mswsock.h* header file is not normally needed unless these Microsoft-specific extensions are used by the application.</span></span>

<span data-ttu-id="bf279-117">*Winsock2. h* 標頭檔內部包含來自 *Windows .h* 標頭檔的核心元素，因此 \# Winsock 應用程式中的 *Windows .h* 標頭檔通常不會有包含行。</span><span class="sxs-lookup"><span data-stu-id="bf279-117">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for the *Windows.h* header file in Winsock applications.</span></span> <span data-ttu-id="bf279-118">如果 \# *Windows .h* 標頭檔需要包含行，則前面應該有 \# 定義 WIN32 的「精簡」和「MEAN」 \_ \_ \_ 宏。</span><span class="sxs-lookup"><span data-stu-id="bf279-118">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="bf279-119">基於歷史原因， *windows .h* 標頭預設為包含 Windows 通訊端1.1 的 *Winsock* 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="bf279-119">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="bf279-120">*Winsock* 標頭檔中的宣告會與 Windows 通訊端2所需的 *Winsock2* 標頭檔中的宣告相衝突。</span><span class="sxs-lookup"><span data-stu-id="bf279-120">The declarations in the *Winsock.h* header file will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.</span></span> <span data-ttu-id="bf279-121">WIN32 的「 \_ 精簡」和「MEAN」 \_ \_ 宏可防止在 *Windows .h* 標頭中包含 *Winsock. h。*</span><span class="sxs-lookup"><span data-stu-id="bf279-121">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* from being included by the *Windows.h* header.</span></span> <span data-ttu-id="bf279-122">以下顯示說明這種情況的範例。</span><span class="sxs-lookup"><span data-stu-id="bf279-122">An example illustrating this is shown below.</span></span>


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="bf279-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="bf279-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf279-124">建立基本 Winsock 應用程式</span><span class="sxs-lookup"><span data-stu-id="bf279-124">Creating a Basic Winsock Application</span></span>](creating-a-basic-winsock-application.md)
</dt> <dt>

[<span data-ttu-id="bf279-125">使用 Winsock 開始使用</span><span class="sxs-lookup"><span data-stu-id="bf279-125">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="bf279-126">將通訊端應用程式移植到 Winsock</span><span class="sxs-lookup"><span data-stu-id="bf279-126">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="bf279-127">Winsock 程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="bf279-127">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 
