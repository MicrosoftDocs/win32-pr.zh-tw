---
title: 註冊端點
description: 在伺服器主機電腦的端點對應中註冊伺服器程式，可讓用戶端程式判斷哪個端點 (通常是 TCP/IP 通訊埠，或是伺服器程式正在接聽的具名管道) 。
ms.assetid: d09874f8-2b55-4af2-bfe1-8978301d6692
keywords:
- 遠端程序呼叫 RPC、工作、註冊端點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6674d20eefa9ebd690f618c36f1dfe69f37dcf7743a0830e06cb38bc85ccfd56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926855"
---
# <a name="registering-endpoints"></a>註冊端點

在伺服器主機電腦的端點對應中註冊伺服器程式，可讓用戶端程式判斷哪個端點 (通常是 TCP/IP 通訊埠，或是伺服器程式正在接聽的具名管道) 。 伺服器程式會呼叫 [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) 函式，如下列程式碼片段所示，在伺服器主機系統的端點對應中註冊自己：


```C++
// This example assumes that MyInterface_v1_0_s_ifspec is a valid data
// structure that represents the interface being registered. The 
// variable is a valid pointer to a binding vector.
RPC_STATUS status;
status = RpcEpRegister(
    MyInterface_v1_0_s_ifspec,
    rpcBindingVector,
    NULL,
    NULL);
```



[**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister)的第一個參數是表示介面的結構。 您可以在 MIDL 編譯器從 MIDL 檔案為此分散式應用程式產生的標頭檔中找到它。 請參閱 [開發介面](developing-the-interface.md)。 接下來， **RpcEpRegister** 需要您的應用程式傳遞一組儲存在系結向量中的系結控制碼。

除了註冊介面名稱之外，您的伺服器應用程式也可以在端點對應中註冊物件 Uuid。 在此範例中，沒有任何物件 Uuid 可註冊，因此 [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister) 的第三個參數會設為 **Null**。

最後一個參數是批註字串。 雖然 RPC 執行時間程式庫不會使用此字串，但建議您設定字串，因為它可改善系統的管理性。 系統管理員可以使用此字串來偵測哪些應用程式所使用的埠，然後這些應用程式可以用來判斷防火牆要管理哪些埠。

 

 




