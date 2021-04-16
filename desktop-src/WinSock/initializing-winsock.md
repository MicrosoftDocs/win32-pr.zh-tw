---
description: 呼叫 Winsock 函式 (應用程式或 Dll) 的所有進程都必須先初始化 Windows 通訊端 DLL 的使用，再進行其他 Winsock 函式呼叫。 這也可確保系統支援 Winsock。
ms.assetid: 300858d8-bed3-4a3c-abb5-2cecd100e5d7
title: 初始化 Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3d02805c684c677c4358cf79c421d6a577f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511433"
---
# <a name="initializing-winsock"></a>初始化 Winsock

呼叫 Winsock 函式 (應用程式或 Dll) 的所有進程都必須先初始化 Windows 通訊端 DLL 的使用，再進行其他 Winsock 函式呼叫。 這也可確保系統支援 Winsock。

**初始化 Winsock**

1.  建立名為 wsaData 的 [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) 物件。
    ```C++
    WSADATA wsaData;
    ```

    

2.  呼叫 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 並以整數形式傳回其值，並檢查是否有錯誤。
    ```C++
    int iResult;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    ```

    

呼叫 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) 函數，以起始使用 WS2 \_32.dll。

[**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata)結構包含 Windows 通訊端執行的相關資訊。 [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)的 MAKEWORD (2，2) 參數會在系統上提出2.2 版 Winsock 的要求，並將傳遞的版本設定為呼叫端可以使用的最高 Windows 通訊端支援版本。

用戶端的下一個步驟：為 [用戶端建立通訊端](creating-a-socket-for-the-client.md)

伺服器的下一個步驟： [建立伺服器的通訊端](creating-a-socket-for-the-server.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Winsock 開始使用](getting-started-with-winsock.md)
</dt> <dt>

[建立基本 Winsock 應用程式](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



