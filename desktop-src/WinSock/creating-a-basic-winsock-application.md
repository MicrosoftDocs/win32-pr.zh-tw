---
description: 如何建立基本 Windows 通訊端 (Winsock) 應用程式。
ms.assetid: 56af2e95-ea82-49e4-b335-86dcf4c38780
title: 建立基本 Winsock 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67b13acc0ae80242fb747415d457e6809895c38cd81878224cad2ffe130b2536
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860948"
---
# <a name="creating-a-basic-winsock-application"></a>建立基本 Winsock 應用程式

**若要建立基本 Winsock 應用程式**

1.  建立新的空白專案。
2.  將空的 c + + 原始程式檔加入至專案。
3.  確定組建環境是指 Microsoft Windows 軟體開發套件 (SDK) 或舊版平臺軟體發展工具組 (SDK) 的包含、Lib 和 Src 目錄。
4.  確定組建環境會連結到 Winsock 程式庫檔案 Ws2 \_ 32..。 使用 Winsock 的應用程式必須與 Ws2 \_ 32 .lib 程式庫檔案連結。 \#Pragma 批註指出需要 *Ws2 \_ 32 .lib* 檔案的連結器。
5.  開始程式設計 Winsock 應用程式。 包含 Winsock 2 標頭檔，以使用 Winsock API。 *Winsock2* 標頭檔包含大部分的 Winsock 函數、結構和定義。 *Ws2tcpip .h* 標頭檔包含 WinSock 2 Protocol-Specific 附錄檔中針對 tcp/ip 所引進的定義，其中包含用來抓取 IP 位址的較新函數和結構。
    > [!Note]  
    > Stdio.h 會用於標準輸入和輸出，特別是 **printf ()** 函式。

     


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



> [!Note]
>
> 如果應用程式使用 IP 協助程式 Api，則需要 *Iphlpapi .h* 標頭檔。 需要 *Iphlpapi .h* 標頭檔時，必須在 \#  \# *Iphlpapi .h* 標頭檔的包含行之前放置 Winsock2 標頭檔的 include 行。
>
> *Winsock2. h* 標頭檔集中包含 *Windows .h* 標頭檔中的核心元素，因此 \# Winsock 應用程式中的 *Windows .h* 標頭檔通常不會有包含的行。 如果 \# *Windows .h* 標頭檔需要包含行，則前面應該有 \# 定義 WIN32 的「精簡」和「MEAN」 \_ \_ \_ 宏。 基於歷史原因， *Windows .h* 標頭預設為包含 Windows 通訊端1.1 的 *Winsock. h* 標頭檔。 *Winsock* 標頭檔中的宣告會與 Windows 通訊端2.0 所需的 *Winsock2* 標頭檔中的宣告相衝突。 WIN32 的「 \_ 精簡」和「MEAN」 \_ \_ 宏可防止 *Windows .h* 標頭包含 *Winsock. h* 。 以下顯示說明這種情況的範例。

 


```C++
#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <iphlpapi.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



下一步： [初始化 Winsock](initializing-winsock.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Winsock 開始使用](getting-started-with-winsock.md)
</dt> <dt>

[關於伺服器和用戶端](about-clients-and-servers.md)
</dt> </dl>

 

 



