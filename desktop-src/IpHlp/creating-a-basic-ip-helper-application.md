---
description: 如何建立基本 IP 協助程式應用程式。
ms.assetid: b53f1cf5-3659-407e-8279-5c94333f3017
title: 建立基本 IP 協助程式應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baae961f8ffb6aa899e96fd05f0cb9f0c41469ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321083"
---
# <a name="creating-a-basic-ip-helper-application"></a>建立基本 IP 協助程式應用程式

**建立基本 IP 協助程式應用程式**

1.  建立新的空白專案。
2.  將空的 c + + 原始程式檔加入至專案。
3.  請確定組建環境參考平臺軟體發展工具組 (SDK) 的 Include、Lib 和 Src 目錄。
4.  確定組建環境會連結至 IP 協助程式程式庫檔案 Iphlpapi .lib 和 Winsock 程式庫檔案 WS2 \_ 32..。
    > [!Note]  
    > 某些基本的 Winsock 函數是用來傳回 IP 位址值和其他資訊。

     

5.  開始程式設計 IP 協助程式應用程式。 藉由包含 IP Helper 標頭檔來使用 IP 協助程式 API。

    ```C++
    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > 使用 IP Helper 函式的應用程式需要 *Iphlpapi .h* 標頭檔。 *Iphlpapi .h* 標頭檔會自動包含其他標頭檔案，其中包含了 IP Helper 函式所使用的結構和列舉。
    >
    > 在 Windows Vista 和更新版本中引進的新 IP 協助程式函式會定義在 *Netioapi .h* 標頭檔中，該檔案會自動包含在 *Iphlpapi .h* 標頭檔中。 不應直接使用 *Netioapi* 標頭檔。
    >
    > IP Helper 函式所使用的許多結構和列舉都定義于 *Iprtrmib .h*、 *Ipexport .h* 和 *Iptypes .h* 標頭檔中。 這些標頭檔會自動包含在 *Iphlpapi .h* 標頭檔中，而且永遠不會直接使用。
    >
    > 在 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 上，標頭檔的組織已經變更。 部分結構現在定義于 *Ipmib .h*、 *Tcpmib .h* 和 *Udpmib .h* 標頭檔中，而不是 *Iprtrmib .h* 標頭檔中。 *Ipmib .h* 標頭檔會自動包含 *Ifmib .h* 標頭檔。 請注意，這些標頭檔會自動包含在 *Iprtrmib* 中，這會自動包含在 *Iphlpapi .h* 標頭檔中。
    >
    > 大部分使用 IP 協助程式 Api 的應用程式都需要 Windows 通訊端2.0 的 *Winsock2* 標頭檔。 需要 *Winsock2. h* 標頭檔案時，應在 \# \# *Iphlpapi .h* 標頭檔的包含行之前放置此檔案的包含行。
    >
    > *Winsock2. h* 標頭檔內部包含來自 *Windows .h* 標頭檔的核心元素，因此 \# IP 協助程式應用程式中的 *Windows .h* 標頭檔通常不會有內含行。 如果 \# *Windows .h* 標頭檔需要包含行，則前面應該有 \# 定義 WIN32 的「精簡」和「MEAN」 \_ \_ \_ 宏。 基於歷史原因， *windows .h* 標頭預設為包含 Windows 通訊端1.1 的 *Winsock* 標頭檔。 Windows 通訊端1.1 的 *Winsock* 標頭檔中的宣告會與 Windows 通訊端2.0 所需的 *Winsock2* 標頭檔中的宣告相衝突。 WIN32 的「 \_ 精簡」和「MEAN」 \_ \_ 宏可防止 *Windows .H* 標頭檔包含 *Winsock* 標頭檔。 以下顯示說明這種情況的範例。

     

    ```C++
    #ifndef WIN32_LEAN_AND_MEAN
    #define WIN32_LEAN_AND_MEAN
    #endif

    #include <windows.h>

    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > 這個基本 IP 協助程式應用程式只會使用一些 IP 位址資料結構和 IP 位址，從 Windows 通訊端2.0 進行字串轉換函式。 使用這些資源完成時，可以使用這些 Windows 通訊端函式，而不需要呼叫 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 來初始化 Windows 通訊端資源和 [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) 。
    >
    > 在使用非這些 IP 位址的其他 Winsock 函數到字串函式的 IP 協助程式中，必須先呼叫 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 函式來初始化 Windows 通訊端資源，然後再呼叫任何 Windows 通訊端函式，並在應用程式使用 Windows 通訊端資源完成時呼叫 [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) 。

     

    > [!Note]
    >
    > 在此基本 IP 協助程式應用程式中使用各種標準 C 函式時，需要 *stdio.h .h* 標頭檔。

     

    下一步： [使用 GetNetworkParams 來抓取資訊](retrieving-information-using-getnetworkparams.md)

 

 
