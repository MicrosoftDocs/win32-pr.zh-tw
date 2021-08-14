---
title: 開發 RPC Windows 應用程式
description: 當您安裝 (SDK) 的平臺軟體發展工具組時，會自動安裝下列 RPC 開發環境、執行時間程式庫和工具。
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ddb48a38faadb8235064fa735fa8a75a80a62308990373ab1971d4a6cd9ecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930793"
---
# <a name="developing-rpc-windows-applications"></a>開發 RPC Windows 應用程式

當您安裝 (SDK) 的平臺軟體發展工具組時，會自動安裝下列 RPC 開發環境、執行時間程式庫和工具：

-   C/c + + 語言標頭 (。H) 檔案
-   RPC 匯入程式庫 ( .lib) 檔案
-   範例程式
-   RPC 參考說明檔
-   **Uuidgen.exe** 公用程式

當您安裝 Windows 時，會安裝下列各項：

-   RPC 執行時間 Dll
-   Windows Vista 和更新版本不支援 Microsoft 定位器 () 
-   RPC 端點對應服務

下列 RPC 匯入程式庫。



| 匯入程式庫 | Description                |
|----------------|----------------------------|
| Rpcns4 .lib     | 名稱-服務函數     |
| Rpcrt4 .lib     | Windows 執行時間函數 |



 

> [!Note]  
> Rpcns4 已淘汰，不再支援。

 

下列 RPC 程式庫隨附于下層支援。



| 動態連結程式庫 | 說明                 | 平台                           |
|----------------------|-----------------------------|------------------------------------|
| Rpcltc1.dll          | 用戶端具名管道傳輸 | Windows NT、Windows 98、Windows 95 |
| Rpclts1.dll          | 伺服器具名管道傳輸 | Windows NT、Windows 98、Windows 95 |
| Rpcltc3.dll          | 用戶端 TCP/IP 傳輸     | Windows NT、Windows 98、Windows 95 |
| Rpclts3.dll          | 伺服器 TCP/IP 傳輸     | Windows NT、Windows 98、Windows 95 |
| Rpcltc5.dll          | 用戶端 NetBIOS 傳輸    | Windows NT、Windows 98、Windows 95 |
| Rpclts5.dll          | 伺服器 NetBIOS 傳輸    | Windows NT、Windows 98、Windows 95 |
| Rpcltc6.dll          | 用戶端 SPX 傳輸        | Windows NT、Windows 98、Windows 95 |
| Rpclts6.dll          | 伺服器 SPX 傳輸        | Windows NT、Windows 98、Windows 95 |
| Rpcdgc6.dll          | 用戶端 IPX 傳輸        | Windows NT                         |
| Rpcdgs6.dll          | 伺服器 IPX 傳輸        | Windows NT                         |
| Rpcdgc3.dll          | 用戶端 UDP 傳輸        | Windows NT                         |
| Rpcdgs3.dll          | 伺服器 UDP 傳輸        | Windows NT                         |



 

您也將需要 Microsoft 介面定義語言 (MIDL) 編譯器。 如需詳細資訊，請參閱 [使用 MIDL 編譯器](/windows/desktop/Midl/using-the-midl-compiler-2)。

 

 