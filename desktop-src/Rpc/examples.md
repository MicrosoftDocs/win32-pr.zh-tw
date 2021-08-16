---
title: RPC)  (範例
description: 示範遠端程序呼叫 (RPC) 概念的範例。
ms.assetid: d5db3085-6df0-4539-a605-d60055f4f4ec
keywords:
- 遠端程序呼叫 RPC，範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e75dca3866e325a4f10eb446d209b834b62ff0407e7edd19f92ec70ac700df85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930047"
---
# <a name="examples-rpc"></a>RPC)  (範例

平臺軟體發展工具組 (SDK) 包含的範例會示範各種不同的遠端程序呼叫， (RPC) 概念，如下所示：

-   ASYNCRPC 說明使用非同步遠端程序呼叫的 RPC 應用程式結構。 它也會示範呼叫完成的各種通知方法。
-   CLUUID 示範如何使用用戶端物件 UUID，讓用戶端從遠端程式的多個執行中進行選取。
-   資料目錄包含四個程式： DUNION 說明區分 (nonencapsulated) 等位的差異;INOUT 示範[ \[ in \] ](../midl/in.md)、 [ \[ out \] ](../midl/out-idl.md)參數;REPAS 示範[代表 \_ as](/windows/desktop/Midl/represent-as)屬性;XMIT 示範[傳輸 \_ 為](/windows/desktop/Midl/transmit-as)屬性。
-   DYNEPT 示範用戶端應用程式透過動態端點管理其與伺服器的連線。
-   FILEREP 目錄包含四個範例，說明開發人員如何撰寫簡單的檔案複寫服務、多重使用者檔案複寫服務、支援安全性功能的服務，以及使用 RPC 非同步管道的服務。
-   控制碼目錄包含三個程式： AUTO、CXHNDL、USRDEF，分別示範 [自動 \_ 處理](/windows/desktop/Midl/auto-handle)、 \[ 內容 \_ 控制碼 \] 和泛型 (使用者定義的) 控制碼。
-   HELLO 是 "Hello，world" 的用戶端/伺服器執行。
-   PICKLE 目錄包含兩個程式： PICKLP 示範資料程式序列化;PICKLT 示範資料類型序列化;這兩個程式都使用[ \[ 編碼 \] ](../midl/encode.md)和[ \[ \] 解碼](../midl/decode.md)屬性。
-   管道示範如何使用管道類型的函式。
-   RPCSVC 示範如何使用 RPC 來執行服務。
-   STROUT 示範如何在伺服器上為 () 指標陣列的二維物件配置記憶體，並將其以 out 參數的形式傳遞回用戶端 \[ \] 。 然後，用戶端就會釋出記憶體。 這項技術可讓存根呼叫伺服器，而不需事先知道將傳回多少資料。

    此程式也可讓使用者針對 UNICODE 或 ANSI 進行編譯。

這些程式的所有原始程式檔和 makefile 都位於 Platform SDK 中。

如需基本的 RPC 應用程式開發和更簡單的範例，請參閱 [教學](tutorial.md) 課程主題。

 

 
