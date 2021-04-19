---
description: 新增 IPv6 支援時，您必須確定您的應用程式會定義大小正確的資料結構。
ms.assetid: 2bf353e2-38d5-462c-9e6c-65886b617215
title: 變更 IPv6 Winsock Html5 應用程式的資料結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c91e19ed733d111bd4e12d824da6ee1a988e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973062"
---
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a><span data-ttu-id="4bc87-103">變更 IPv6 Winsock Html5 應用程式的資料結構</span><span class="sxs-lookup"><span data-stu-id="4bc87-103">Changing Data Structures for IPv6 Winsock Appications</span></span>

<span data-ttu-id="4bc87-104">新增 IPv6 支援時，您必須確定您的應用程式會定義大小正確的資料結構。</span><span class="sxs-lookup"><span data-stu-id="4bc87-104">When adding support for IPv6, you must ensure that your application defines properly sized data structures.</span></span> <span data-ttu-id="4bc87-105">IPv6 位址的大小遠超過 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="4bc87-105">The size of an IPv6 address is much larger than an IPv4 address.</span></span> <span data-ttu-id="4bc87-106">當儲存 IP 位址時，以硬式編碼來處理 IPv4 位址大小的結構，將會導致您的應用程式發生問題，且必須加以修改。</span><span class="sxs-lookup"><span data-stu-id="4bc87-106">Structures that are hard-coded to handle the size of an IPv4 address when storing an IP address will cause problems in your application, and must be modified.</span></span>

<span data-ttu-id="4bc87-107">最佳做法</span><span class="sxs-lookup"><span data-stu-id="4bc87-107">Best Practice</span></span>

<span data-ttu-id="4bc87-108">確保您的結構正確大小的最佳方法是使用 [**SOCKADDR \_ 儲存體**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="4bc87-108">The best approach to ensuring that your structures are properly sized is to use the [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure.</span></span> <span data-ttu-id="4bc87-109">**SOCKADDR \_ 儲存體** 結構與 IP 位址版本無關。</span><span class="sxs-lookup"><span data-stu-id="4bc87-109">The **SOCKADDR\_STORAGE** structure is agnostic to IP address version.</span></span> <span data-ttu-id="4bc87-110">使用 **SOCKADDR \_ 儲存體** 結構來儲存 IP 位址時，可以使用一個程式碼基底適當地處理 IPv4 和 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="4bc87-110">When the **SOCKADDR\_STORAGE** structure is used to store IP addresses, IPv4 and IPv6 addresses can be properly handled with one code base.</span></span>

<span data-ttu-id="4bc87-111">下列範例（取自附錄 B 中的 Server .c 檔案的摘錄）會識別 **SOCKADDR \_ 儲存** 結構的適當使用。</span><span class="sxs-lookup"><span data-stu-id="4bc87-111">The following example, which is an excerpt taken from the Server.c file found in Appendix B, identifies an appropriate use of the **SOCKADDR\_STORAGE** structure.</span></span> <span data-ttu-id="4bc87-112">請注意，如下列範例所示，如這個範例所示，此結構可正常地處理 IPv4 或 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="4bc87-112">Notice that the structure, when used properly as this example shows, gracefully handles either an IPv4 or IPv6 address.</span></span>


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

#define BUFFER_SIZE 512
#define DEFAULT_PORT "27015"

int main(int argc, char **argv)
{
    char Buffer[BUFFER_SIZE] = {0};
    char *Hostname;
    int Family = AF_UNSPEC;
    int SocketType = SOCK_STREAM;
    char *Port = DEFAULT_PORT;
    char *Address = NULL;
    int i = 0;
    DWORD dwRetval = 0;
    int iResult = 0;
    int FromLen = 0;
    int AmountRead = 0;

    SOCKADDR_STORAGE From;

    WSADATA wsaData;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;

    // Parse arguments
    if (argc >= 1) {
        Hostname = argv[1];
    }    

   // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }

    From.ss_family = (ADDRESS_FAMILY) Family;
    
    //...
        
        return 0;
}
```



> [!Note]  
> <span data-ttu-id="4bc87-113">[**SOCKADDR \_ 儲存體**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))結構是 Windows XP 的新功能。</span><span class="sxs-lookup"><span data-stu-id="4bc87-113">The [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure is new for Windows XP.</span></span>

 

<span data-ttu-id="4bc87-114">要避免的程式碼</span><span class="sxs-lookup"><span data-stu-id="4bc87-114">Code To Avoid</span></span>

<span data-ttu-id="4bc87-115">一般而言，許多應用程式會使用 [**sockaddr**](sockaddr-2.md) 結構來儲存與通訊協定無關的位址，或 IP 位址的 **sockaddr \_** 結構。</span><span class="sxs-lookup"><span data-stu-id="4bc87-115">Typically, many applications used the [**sockaddr**](sockaddr-2.md) structure to store protocol-independent addresses, or the **sockaddr\_in** structure for IP addresses.</span></span> <span data-ttu-id="4bc87-116">結構中的 sockaddr 結構和 **sockaddr \_** 都夠大，足以容納 ipv6 位址，因此，如果您的應用程式與 ipv6 相容，則兩者都不足夠。</span><span class="sxs-lookup"><span data-stu-id="4bc87-116">Neither the sockaddr structure nor the **sockaddr\_in** structure is large enough to hold IPv6 addresses, and therefore both are insufficient if your application is to be IPv6 compatible.</span></span>

<span data-ttu-id="4bc87-117">程式碼撰寫工作</span><span class="sxs-lookup"><span data-stu-id="4bc87-117">Coding Task</span></span>

<span data-ttu-id="4bc87-118">**從 IPv4 將現有的程式碼基底修改為 IPv4 和 IPv6 互通性**</span><span class="sxs-lookup"><span data-stu-id="4bc87-118">**To modify your existing code base from IPv4 to IPv4- and IPv6-interoperability**</span></span>

1.  <span data-ttu-id="4bc87-119">取得 Checkv4.exe 公用程式。</span><span class="sxs-lookup"><span data-stu-id="4bc87-119">Acquire the Checkv4.exe utility.</span></span> <span data-ttu-id="4bc87-120">此公用程式隨附于 Microsoft Windows 軟體開發套件 (SDK) 可透過 MSDN 訂用帳戶取得，或從 web 下載。</span><span class="sxs-lookup"><span data-stu-id="4bc87-120">The utility is included with the Microsoft Windows Software Development Kit (SDK) which is made available through your MSDN subscription, or from the web as a download.</span></span>
2.  <span data-ttu-id="4bc87-121">針對您的程式碼執行 Checkv4.exe 公用程式。</span><span class="sxs-lookup"><span data-stu-id="4bc87-121">Run the Checkv4.exe utility against your code.</span></span> <span data-ttu-id="4bc87-122">瞭解如何在 [使用 Checkv4.exe 公用程式](using-the-checkv4-exe-utility-2.md)一節中，針對您的檔案執行 Checkv4.exe 公用程式。</span><span class="sxs-lookup"><span data-stu-id="4bc87-122">Learn about how to run the Checkv4.exe utility against your files in the section on [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>
3.  <span data-ttu-id="4bc87-123">此公用程式會警示您 **\_ 在結構中** 使用 **sockaddr** 或 sockaddr，並提供有關如何使用 IPv6 相容結構 [**sockaddr \_ 儲存體**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))來取代任何的建議。</span><span class="sxs-lookup"><span data-stu-id="4bc87-123">The utility alerts you to usage of **sockaddr** or **sockaddr\_in** structures, and provides recommendations on how to replace either with the IPv6 compatible structure [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)).</span></span>
4.  <span data-ttu-id="4bc87-124">請適當地取代任何這類實例和相關聯的程式碼，以使用 **SOCKADDR \_ 儲存體** 結構。</span><span class="sxs-lookup"><span data-stu-id="4bc87-124">Replace any such instances, and associated code as appropriate, to use the **SOCKADDR\_STORAGE** structure.</span></span>

<span data-ttu-id="4bc87-125">或者，您可以 **\_ 在結構中** 搜尋 **sockaddr** 和 sockaddr 實例的程式碼基底，並視需要將所有 (和其他相關聯的程式碼變更為 **sockaddr \_ 儲存體** 結構的) 。</span><span class="sxs-lookup"><span data-stu-id="4bc87-125">Alternatively, you can search your code base for instances of the **sockaddr** and **sockaddr\_in** structures, and change all such usage (and other associated code, as appropriate) to the **SOCKADDR\_STORAGE** structure.</span></span>

> [!Note]  
> <span data-ttu-id="4bc87-126">**Addrinfo** 和 **SOCKADDR \_ 儲存體** 結構分別包含 (**ai \_ 系列** 與 **ss \_ 系列**) 的通訊協定和位址家族成員。</span><span class="sxs-lookup"><span data-stu-id="4bc87-126">The **addrinfo** and **SOCKADDR\_STORAGE** structures include protocol and address family members (**ai\_family** and **ss\_family**), respectively.</span></span> <span data-ttu-id="4bc87-127">RFC 2553 將 [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa)的 **ai \_ 系列** 成員指定為 int，而 **ss \_ 系列** 則指定為簡短; 因此，在這些成員之間的直接複製會導致編譯器錯誤。</span><span class="sxs-lookup"><span data-stu-id="4bc87-127">RFC 2553 specifies the **ai\_family** member of [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) as an int, while **ss\_family** is specified as a short; as such, a direct copy between those members results in a compiler error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4bc87-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="4bc87-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bc87-129">適用于 Windows 通訊端應用程式的 IPv6 指南</span><span class="sxs-lookup"><span data-stu-id="4bc87-129">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="4bc87-130">IPv6 Winsock 應用程式的雙重堆疊通訊端</span><span class="sxs-lookup"><span data-stu-id="4bc87-130">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="4bc87-131">IPv6 Winsock 應用程式的函式呼叫</span><span class="sxs-lookup"><span data-stu-id="4bc87-131">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="4bc87-132">使用硬式編碼的 IPv4 位址</span><span class="sxs-lookup"><span data-stu-id="4bc87-132">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="4bc87-133">IPv6 Winsock 應用程式的消費者介面問題</span><span class="sxs-lookup"><span data-stu-id="4bc87-133">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="4bc87-134">IPv6 Winsock 應用程式的基礎通訊協定</span><span class="sxs-lookup"><span data-stu-id="4bc87-134">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 
