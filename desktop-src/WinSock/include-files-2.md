---
description: 與 Windows 通訊端1.1 搭配使用的原始 include 檔是 Winsock. h 標頭檔。
ms.assetid: 0536abcc-4277-4bd8-927c-3bf429bc65bb
title: 包含檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 740bde9fae96aa3088a4317c66479bcc75176ee3b9ca9f5e390365c5ef481109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051526"
---
# <a name="include-files"></a>包含檔案

與 Windows 通訊端1.1 搭配使用的原始 include 檔是 *Winsock. h* 標頭檔。 為了讓您可以輕鬆地根據 Berkeley UNIX 通訊端將現有的原始程式碼移植到 Windows sockets，我們鼓勵使用 Winsock 1.1 的 Windows 通訊端開發工具組，以標準 UNIX 包含檔案的相同名稱來提供，例如 (*sys/socket. h* 和 arpa/inet .h 標頭檔。 不過，這些類似名稱的 Winsock 標頭檔只會包含指示詞，以包含 *Winsock2* 標頭檔。

釋放 Windows 通訊端2時，與 Windows 通訊端搭配使用的主要 include 檔案已重新命名為 *Winsock2. h*。 Winsock 1.1 舊的原始 *winsock. h* 標頭檔也會保留，以與繼承應用程式相容。 從 Windows 2000 發行之後，已淘汰 Winsock 1.1 相容應用程式的開發。 所有應用程式現在都應該使用 Winsock 應用程式原始程式檔中的 [include *Winsock2 .h* ] 指示詞。

*Winsock2* 標頭檔包含大部分的 Winsock 函數、結構和定義。 *Ws2tcpip .h* 標頭檔包含 WinSock 2 Protocol-Specific 附錄檔中針對 tcp/ip 所引進的定義，其中包含用來抓取 IP 位址的較新函數和結構。 這些包含 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 和 [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) 系列的函式，可為 IPv4 或 IPv6 位址提供名稱解析。 只有當應用程式需要這些 IP 中立的命名函式時，才需要 *Ws2tcpip .h* 標頭檔。

*Mswsock 的 .h* 標頭檔包含 Windows 通訊端 2 ([**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile)、 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)和 [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)的 Microsoft 特定擴充功能的定義，例如) 。 除非應用程式使用這些 Microsoft 專屬的延伸模組，否則通常不需要 *Mswsock .h* 標頭檔。

*Winsock2. h* 標頭檔集中包含 *Windows .h* 標頭檔中的核心元素，因此 \# Winsock 應用程式中的 *Windows .h* 標頭檔通常不會有包含的行。 如果 \# *Windows .h* 標頭檔需要包含行，則前面應該有 \# 定義 WIN32 的「精簡」和「MEAN」 \_ \_ \_ 宏。 基於歷史原因， *Windows .h* 標頭預設為包含 Windows 通訊端1.1 的 *Winsock. h* 標頭檔。 *Winsock* 標頭檔中的宣告會與 Windows 通訊端2所要求的 *Winsock2* 標頭檔中的宣告相衝突。 WIN32 的「 \_ 精簡」和「MEAN」 \_ \_ 宏可防止 *Windows .h* 標頭包含 *Winsock. h* 。 以下顯示說明這種情況的範例。


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立基本 Winsock 應用程式](creating-a-basic-winsock-application.md)
</dt> <dt>

[使用 Winsock 開始使用](getting-started-with-winsock.md)
</dt> <dt>

[將通訊端應用程式移植到 Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Winsock 程式設計考慮](winsock-programming-considerations.md)
</dt> </dl>

 

 
