---
description: 在 Winsock 應用程式中，會使用 WSAGetLastError 函式來抓取錯誤碼，Windows 通訊端取代 Windows GetLastError 函數。
ms.assetid: cb73fc92-74bd-4c8b-a1c0-6daf4d298aa1
title: 錯誤碼-errno、h_errno 和 WSAGetLastError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2e9c4372bd479ee4b94bd3226128737dae3d5637be94046eb013716590ac285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132631"
---
# <a name="error-codes---errno-h_errno-and-wsagetlasterror"></a>錯誤碼-errno、h \_ errno 和 WSAGetLastError

在 Winsock 應用程式中，會使用 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)函式來抓取錯誤碼，Windows 通訊端取代 Windows [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)函數。 Windows 通訊端所傳回的錯誤碼類似于 UNIX 通訊端錯誤碼常數，但常數前面都加上 WSA。 因此在 Winsock 應用程式中，會傳回 WSAEWOULDBLOCK 錯誤碼，而在 UNIX 的應用程式中，將會傳回 EWOULDBLOCK 錯誤碼。

Windows 通訊端所設定的錯誤碼無法透過 *errno* 變數使用。 此外，針對函式的 **getXbyY** 類別，不會透過 *h \_ errno* 變數提供錯誤碼。 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)函式旨在提供可靠的方式，讓多執行緒進程中的執行緒取得每個執行緒的錯誤資訊。

為了與 Berkeley UNIX (BSD) ，Windows (Windows 通訊端2更新和 Windows 98 的早期版本 Windows 95) ，例如 Windows 重新定義 Berkeley 的一般錯誤常數通常會在 BSD 上的 *errno* 中，做為相等的通訊端 WSA 錯誤。 例如，ECONNREFUSED 在 *Winsock* 標頭檔中定義為 **WSAECONNREFUSED** 。 在後續版本的 Windows 中 (Windows NT 3.1 和更新版本) 這些定義已標記為批註，以避免與 Microsoft c/c + + 和 Visual Studio 所使用的 *errno* 發生衝突。

Microsoft Windows 軟體開發套件 (SDK 隨附的 *Winsock2* 標頭檔) 、平臺軟體發展工具組 (SDK) 和 Visual Studio 仍包含在 ifdef 0 和 endif 區塊中的已標記批註區塊， \# 其中定義了與 \# WSA 錯誤常數相同的 BSD 通訊端錯誤碼。 這些可以用來提供 UNIX、BSD 和 Linux 通訊端程式設計的一些相容性。 為了與 BSD 相容，應用程式可能會選擇變更 *Winsock2* ，並取消批註此區塊。 不過，強烈建議應用程式開發人員不要取消批註此區塊，因為在大部分的應用程式中，與 *errno* 之間的衝突是不可避免的。 此外，bsd 通訊端錯誤的定義與 UNIX、BSD 和 Linux 程式中使用的值非常不同。 應用程式開發人員強烈建議使用通訊端應用程式中的 WSA 錯誤常數。

在 \# ifdef 0 和 \# Endif 區塊內的 Winsock2. h 標頭中，這些定義仍會以批註方式出現。 如果應用程式開發人員堅持使用 BSD 錯誤碼以提供相容性，則應用程式可能會選擇包含表單的行：


```C++
#include <windows.h>

#define errno WSAGetLastError()
```



這可讓所撰寫的網路程式碼使用全域 *errno* ，以便在單一執行緒環境中正確運作。 有一些極嚴重的缺點。 如果原始程式檔包含檢查通訊端和非通訊端函式 *errno* 的程式碼，則無法使用此機制。 此外，應用程式也不可能指派新值給 *errno*。  (在 Windows 通訊端中，函數 [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror)可用於此用途。 ) 

典型的 BSD 樣式


```C++
r = recv(...);
if (r == -1
    && errno == EWOULDBLOCK)
    {...}
```



慣用樣式


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == EWOULDBLOCK)
    {...}
```



雖然提供與 Berkeley 通訊端4.3 一致的錯誤常數，但基於相容性的目的，我們強烈建議您使用應用程式來使用 WSA 錯誤碼定義。 這是因為某些 Windows 通訊端函式所傳回的錯誤碼會落在 Microsoft C ©所定義之錯誤碼的標準範圍中。 因此，上述原始碼片段的較佳版本為：


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == WSAEWOULDBLOCK)
    {...}
```



1995中定義的原始 Winsock 1.1 規格建議一組錯誤碼，並列出可能會因每個函式而傳回的錯誤。 Windows通訊端2新增了函數和功能，除了原始 Winsock 規格中所列的以外，還會傳回其他 Windows 通訊端錯誤碼。 在一段時間內已新增額外的函式，以增強 Winsock 以供開發人員使用。 例如，新的名稱服務函式 ([**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)和 [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)，例如，在 Windows XP 和更新版本上同時支援 IPv6 和 IPv4 的) 。 某些較舊的 IPv4 名稱服務函式 (函式的 **getXbyY** 類別，例如) 已被取代。

[Windows 通訊端錯誤碼](windows-sockets-error-codes-2.md)的一節中提供 Windows 通訊端函式所傳回之可能錯誤碼的完整清單。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[處理 Winsock 錯誤](handling-winsock-errors.md)
</dt> <dt>

[將通訊端應用程式移植到 Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Windows通訊端錯誤碼](windows-sockets-error-codes-2.md)
</dt> <dt>

[Winsock 程式設計考慮](winsock-programming-considerations.md)
</dt> </dl>

 

 
