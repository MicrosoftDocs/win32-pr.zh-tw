---
title: 停止伺服器應用程式
description: 伺服器應用程式可以藉由呼叫 RpcMgmtStopServerListening 和 RpcServerUnregisterIf，或直接結束主機進程，來停止接聽用戶端。
ms.assetid: 9d310cfb-72ad-448f-a66a-db6ac2478824
keywords:
- 遠端程序呼叫 RPC、工作、停止伺服器應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83f0a96732b1c862cf3e00d25cc2d2d9caf27ae5d764a9edab00c78aaf18682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925138"
---
# <a name="stopping-the-server-application"></a>停止伺服器應用程式

伺服器應用程式可以藉由呼叫 [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) 和 [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)，或直接結束主機進程，來停止接聽用戶端。 這兩種方法都是可接受的。 如果伺服器採用第一種方法，則應該執行下列步驟：

在發生例外狀況或呼叫 [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)之前，伺服器函數 [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten)不會傳回呼叫程式。 依預設，只有另一個伺服器執行緒可以使用 **RpcMgmtStopServerListening** 來中止 RPC 伺服器。 嘗試停止伺服器的用戶端將會收到錯誤的「 \_ RPC \_ 拒絕存取」錯誤 \_ 。 不過，您可以設定 RPC 允許部分或所有用戶端停止伺服器。 如需詳細資訊，請參閱 **RpcMgmtStopServerListening** 。

您也可以讓用戶端應用程式對伺服器上的 shutdown 常式進行遠端程序呼叫。 Shutdown 常式會呼叫 [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) 和 [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)。 本教學課程範例程式應用程式會使用這種方法，方法是將新的遠端函式（ **Shutdown**）新增至 Hellop 檔案。

在 **Shutdown** 函式中， [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) 的單一 null 參數表示本機應用程式應該停止接聽遠端程序呼叫。 要 [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) 的兩個 null 參數是萬用字元，表示所有介面都應該取消註冊。 **FALSE** 參數表示應該立即從登錄中移除介面，而不是等候暫止的呼叫完成。


```C++
/* add this function to hellop.c */
void Shutdown(void)
{
    RPC_STATUS status;
 
    status = RpcMgmtStopServerListening(NULL);
 
    if (status) 
    {
       exit(status);
    }
 
    status = RpcServerUnregisterIf(NULL, NULL, FALSE);
 
    if (status) 
    {
       exit(status);
    }
} //end Shutdown
```



 

 




