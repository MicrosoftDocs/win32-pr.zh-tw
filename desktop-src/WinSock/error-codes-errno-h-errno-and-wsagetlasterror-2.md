---
description: 在 Winsock 應用程式中，會使用 WSAGetLastError 函式來抓取錯誤碼，Windows 通訊端取代 Windows GetLastError 函數。
ms.assetid: cb73fc92-74bd-4c8b-a1c0-6daf4d298aa1
title: 錯誤碼-errno、h_errno 和 WSAGetLastError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b547e0b580599aaec27a0b77bfad0ffaa8966e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991821"
---
# <a name="error-codes---errno-h_errno-and-wsagetlasterror"></a><span data-ttu-id="32a68-103">錯誤碼-errno、h \_ errno 和 WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="32a68-103">Error Codes - errno, h\_errno and WSAGetLastError</span></span>

<span data-ttu-id="32a68-104">在 Winsock 應用程式中，會使用 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 函式來抓取錯誤碼，Windows 通訊端取代 windows [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數。</span><span class="sxs-lookup"><span data-stu-id="32a68-104">In Winsock applications, error codes are retrieved using the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function, the Windows Sockets substitute for the Windows [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span> <span data-ttu-id="32a68-105">Windows 通訊端所傳回的錯誤碼類似于 UNIX 通訊端錯誤碼常數，但常數前面都加上 WSA。</span><span class="sxs-lookup"><span data-stu-id="32a68-105">The error codes returned by Windows Sockets are similar to UNIX socket error code constants, but the constants are all prefixed with WSA.</span></span> <span data-ttu-id="32a68-106">因此在 Winsock 應用程式中，會傳回 WSAEWOULDBLOCK 錯誤碼，而在 UNIX 應用程式中會傳回 EWOULDBLOCK 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="32a68-106">So in Winsock applications the WSAEWOULDBLOCK error code would be returned, while in UNIX applications the EWOULDBLOCK error code would be returned.</span></span>

<span data-ttu-id="32a68-107">Windows 通訊端所設定的錯誤碼無法透過 *errno* 變數使用。</span><span class="sxs-lookup"><span data-stu-id="32a68-107">Error codes set by Windows Sockets are not made available through the *errno* variable.</span></span> <span data-ttu-id="32a68-108">此外，針對函式的 **getXbyY** 類別，不會透過 *h \_ errno* 變數提供錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="32a68-108">Additionally, for the **getXbyY** class of functions, error codes are not made available through the *h\_errno* variable.</span></span> <span data-ttu-id="32a68-109">[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)函式旨在提供可靠的方式，讓多執行緒進程中的執行緒取得每個執行緒的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="32a68-109">The [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function is intended to provide a reliable way for a thread in a multithreaded process to obtain per-thread error information.</span></span>

<span data-ttu-id="32a68-110">為了與 Berkeley UNIX 相容 (BSD) ，舊版 Windows (Windows 95 （含 Windows 通訊端2更新和 Windows 98），例如) 重新定義 Berkeley 的一般錯誤常數通常會在 BSD 上的 *errno* 中，做為對等的 Windows 通訊端 WSA 錯誤。</span><span class="sxs-lookup"><span data-stu-id="32a68-110">For compatibility with Berkeley UNIX (BSD), early versions of Windows (Windows 95 with the Windows Socket 2 Update and Windows 98, for example) redefined regular Berkeley error constants typically found in *errno.h* on BSD as the equivalent Windows Sockets WSA errors.</span></span> <span data-ttu-id="32a68-111">例如，ECONNREFUSED 在 *Winsock* 標頭檔中定義為 **WSAECONNREFUSED** 。</span><span class="sxs-lookup"><span data-stu-id="32a68-111">So for example, ECONNREFUSED was defined as **WSAECONNREFUSED** in the *Winsock.h* header file.</span></span> <span data-ttu-id="32a68-112">在後續的 Windows (Windows NT 3.1 和更新版本中) 這些定義已標記為批註，以避免與 Microsoft C/c + + 和 Visual Studio 所使用的 *errno* 發生衝突。</span><span class="sxs-lookup"><span data-stu-id="32a68-112">In subsequent versions of Windows (Windows NT 3.1 and later) these defines were commented out to avoid conflicts with *errno.h* used with Microsoft C/C++ and Visual Studio.</span></span>

<span data-ttu-id="32a68-113">Microsoft Windows 軟體開發套件 (SDK 隨附的 *Winsock2* 標頭檔) 、平臺軟體發展工具組 (SDK) 和 Visual Studio 仍包含在 ifdef 0 和 endif 區塊中的已標記批註區塊， \# 其中定義了與 \# WSA 錯誤常數相同的 BSD 通訊端錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="32a68-113">The *Winsock2.h* header file included with the Microsoft Windows Software Development Kit (SDK), Platform Software Development Kit (SDK), and Visual Studio still contains a commented out block of defines within an \#ifdef 0 and \#endif block that define the BSD socket error codes to be the same as the WSA error constants.</span></span> <span data-ttu-id="32a68-114">這些可以用來提供與 UNIX、BSD 和 Linux 通訊端程式設計的一些相容性。</span><span class="sxs-lookup"><span data-stu-id="32a68-114">These can be used to provide some compatibility with UNIX, BSD, and Linux socket programming.</span></span> <span data-ttu-id="32a68-115">為了與 BSD 相容，應用程式可能會選擇變更 *Winsock2* ，並取消批註此區塊。</span><span class="sxs-lookup"><span data-stu-id="32a68-115">For compatibility with BSD, an application may choose to change the *Winsock2.h* and uncomment this block.</span></span> <span data-ttu-id="32a68-116">不過，強烈建議應用程式開發人員不要取消批註此區塊，因為在大部分的應用程式中，與 *errno* 之間的衝突是不可避免的。</span><span class="sxs-lookup"><span data-stu-id="32a68-116">However, application developers are strongly discouraged from uncommenting this block because of inevitable conflicts with *errno.h* in most applications.</span></span> <span data-ttu-id="32a68-117">此外，BSD 通訊端錯誤的定義與 UNIX、BSD 和 Linux 程式中使用的值非常不同。</span><span class="sxs-lookup"><span data-stu-id="32a68-117">Also, the BSD socket errors are defined to very different values than are used in UNIX, BSD, and Linux programs.</span></span> <span data-ttu-id="32a68-118">應用程式開發人員強烈建議使用通訊端應用程式中的 WSA 錯誤常數。</span><span class="sxs-lookup"><span data-stu-id="32a68-118">Application developers are very strongly encouraged to use the WSA error constants in socket applications.</span></span>

<span data-ttu-id="32a68-119">在 \# ifdef 0 和 \# Endif 區塊內的 Winsock2. h 標頭中，這些定義仍會以批註方式出現。</span><span class="sxs-lookup"><span data-stu-id="32a68-119">These defines remain commented out in the *Winsock2.h* header within an \#ifdef 0 and \#endif block.</span></span> <span data-ttu-id="32a68-120">如果應用程式開發人員堅持使用 BSD 錯誤碼以提供相容性，則應用程式可能會選擇包含表單的行：</span><span class="sxs-lookup"><span data-stu-id="32a68-120">If an application developer insists on using the BSD error codes for compatibility, then an application may choose to include a line of the form:</span></span>


```C++
#include <windows.h>

#define errno WSAGetLastError()
```



<span data-ttu-id="32a68-121">這可讓所撰寫的網路程式碼使用全域 *errno* ，以便在單一執行緒環境中正確運作。</span><span class="sxs-lookup"><span data-stu-id="32a68-121">This allows networking code which was written to use the global *errno* to work correctly in a single-threaded environment.</span></span> <span data-ttu-id="32a68-122">有一些極嚴重的缺點。</span><span class="sxs-lookup"><span data-stu-id="32a68-122">There are some very serious drawbacks.</span></span> <span data-ttu-id="32a68-123">如果原始程式檔包含檢查通訊端和非通訊端函式 *errno* 的程式碼，則無法使用此機制。</span><span class="sxs-lookup"><span data-stu-id="32a68-123">If a source file includes code which inspects *errno* for both socket and non-socket functions, this mechanism cannot be used.</span></span> <span data-ttu-id="32a68-124">此外，應用程式也不可能指派新值給 *errno*。</span><span class="sxs-lookup"><span data-stu-id="32a68-124">Furthermore, it is not possible for an application to assign a new value to *errno*.</span></span> <span data-ttu-id="32a68-125"> (在 Windows 通訊端中，函數 [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) 可用於此用途。 ) </span><span class="sxs-lookup"><span data-stu-id="32a68-125">(In Windows Sockets, the function [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) may be used for this purpose.)</span></span>

<span data-ttu-id="32a68-126">典型的 BSD 樣式</span><span class="sxs-lookup"><span data-stu-id="32a68-126">Typical BSD Style</span></span>


```C++
r = recv(...);
if (r == -1
    && errno == EWOULDBLOCK)
    {...}
```



<span data-ttu-id="32a68-127">慣用樣式</span><span class="sxs-lookup"><span data-stu-id="32a68-127">Preferred Style</span></span>


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == EWOULDBLOCK)
    {...}
```



<span data-ttu-id="32a68-128">雖然提供與 Berkeley 通訊端4.3 一致的錯誤常數，但基於相容性的目的，我們強烈建議您使用應用程式來使用 WSA 錯誤碼定義。</span><span class="sxs-lookup"><span data-stu-id="32a68-128">Although error constants consistent with Berkeley Sockets 4.3 are provided for compatibility purposes, applications are strongly encouraged to use the WSA error code definitions.</span></span> <span data-ttu-id="32a68-129">這是因為某些 Windows 通訊端函式所傳回的錯誤碼屬於 Microsoft C ©所定義的標準錯誤碼範圍。</span><span class="sxs-lookup"><span data-stu-id="32a68-129">This is because error codes returned by certain Windows Sockets functions fall into the standard range of error codes as defined by Microsoft C©.</span></span> <span data-ttu-id="32a68-130">因此，上述原始碼片段的較佳版本為：</span><span class="sxs-lookup"><span data-stu-id="32a68-130">Thus, a better version of the preceding source code fragment is:</span></span>


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == WSAEWOULDBLOCK)
    {...}
```



<span data-ttu-id="32a68-131">1995中定義的原始 Winsock 1.1 規格建議一組錯誤碼，並列出可能會因每個函式而傳回的錯誤。</span><span class="sxs-lookup"><span data-stu-id="32a68-131">The original Winsock 1.1 specification defined in 1995 recommended a set of error codes, and listed the possible errors that can be returned as a result of each function.</span></span> <span data-ttu-id="32a68-132">除了原始 Winsock 規格中列出的其他 Windows 通訊端錯誤碼之外，windows 通訊端2還新增了函式和功能。</span><span class="sxs-lookup"><span data-stu-id="32a68-132">Windows Sockets 2 added functions and features with other Windows Sockets error codes returned in addition to those listed in the original Winsock specification.</span></span> <span data-ttu-id="32a68-133">在一段時間內已新增額外的函式，以增強 Winsock 以供開發人員使用。</span><span class="sxs-lookup"><span data-stu-id="32a68-133">Additional functions have been added over time to enhance Winsock for use by developers.</span></span> <span data-ttu-id="32a68-134">例如，新的名稱服務函式 ([**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 和 [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)，例如在 Windows XP 和更新版本上同時支援 IPv6 和 IPv4 的) 。</span><span class="sxs-lookup"><span data-stu-id="32a68-134">For example, new name service functions ([**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo), for example) were added that support both IPv6 and IPv4 on Windows XP and later.</span></span> <span data-ttu-id="32a68-135">某些較舊的 IPv4 名稱服務函式 (函式的 **getXbyY** 類別，例如) 已被取代。</span><span class="sxs-lookup"><span data-stu-id="32a68-135">Some of the older IPv4-only name service functions (the **getXbyY** class of functions, for example) have been deprecated.</span></span>

<span data-ttu-id="32a68-136">有關 windows 通訊端函式所傳回之可能錯誤碼的完整清單，請在 [Windows 通訊端錯誤碼](windows-sockets-error-codes-2.md)的一節中提供。</span><span class="sxs-lookup"><span data-stu-id="32a68-136">A complete list of possible error codes returned by Windows Sockets functions is given in the section on [Windows Sockets Error Codes](windows-sockets-error-codes-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="32a68-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="32a68-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32a68-138">處理 Winsock 錯誤</span><span class="sxs-lookup"><span data-stu-id="32a68-138">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="32a68-139">將通訊端應用程式移植到 Winsock</span><span class="sxs-lookup"><span data-stu-id="32a68-139">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="32a68-140">Windows 通訊端錯誤碼</span><span class="sxs-lookup"><span data-stu-id="32a68-140">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> <dt>

[<span data-ttu-id="32a68-141">Winsock 程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="32a68-141">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 
