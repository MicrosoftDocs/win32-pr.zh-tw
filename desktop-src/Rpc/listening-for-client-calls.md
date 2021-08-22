---
title: 接聽用戶端呼叫
description: 當您的伺服器應用程式已註冊其介面、建立必要的系結資訊，並註冊其端點之後，就可以開始接聽來自用戶端程式的遠端程序呼叫。
ms.assetid: ca9d24ed-0acc-45de-bbb2-761c56745a58
keywords:
- 遠端程序呼叫 RPC、工作、接聽用戶端呼叫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f94453a3250cfc1adae72aa0af96297a741beb501839f7f7831e3f88a8c218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928603"
---
# <a name="listening-for-client-calls"></a>接聽用戶端呼叫

當您的伺服器應用程式已註冊其介面、建立必要的系結資訊，並註冊其端點之後，就可以開始接聽來自用戶端程式的遠端程序呼叫。

若要接聽遠端程序呼叫，您的伺服器程式必須呼叫 [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten)，如下列程式碼片段所示：


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



RPC 伺服器有一或多個執行緒可挑選用戶端呼叫，並將它們傳遞至已註冊介面中的常式。 [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten)函數的第一個參數是要建立之執行緒的最小數目。 參數只是提示;RPC 執行時間可能會選擇忽略它。

[**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten)的第二個參數是要處理的並行遠端程序呼叫的最大數目。 如果您想要讓應用程式使用預設的最大值，請將 RPC \_ C \_ 接聽 \_ 的最大 \_ 呼叫預設值傳遞 \_ 為此參數的值。

DCE 規格會呼叫 [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) 以繼續執行，直到它收到停止的信號為止。 這個函式有一個 Microsoft 擴充功能，可讓它開始接聽並立即返回。 如果您想要讓應用程式使用預設的 DCE 行為，請將第三個參數設定為零。 如需詳細資訊，請參閱 [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten)、 [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)和 [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) 。

 

 




