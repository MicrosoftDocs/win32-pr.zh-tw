---
title: 接聽遠端程序呼叫
description: 當伺服器程式註冊其系結資訊，並在名稱服務資料庫中通告其存在時，就可以開始接聽遠端程序呼叫的端點。
ms.assetid: 1c116e44-03a4-4b86-ae37-0b9187981e53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d9463e0591279377502394541190be685cccd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020734"
---
# <a name="listening-for-remote-procedure-calls"></a>接聽遠端程序呼叫

當伺服器程式註冊其系結資訊，並在名稱服務資料庫中通告其存在時，就可以開始接聽遠端程序呼叫的端點。 伺服器程式會呼叫 [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) 函數，以監視遠端程式的用戶端調用的端點。

[**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten)的 DCE 規格指出，在伺服器程式中的函式呼叫 [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)之前，不應傳回。 Microsoft RPC 的 **RpcServerListen** 執行會使用兩個未出現在 DCE 規格中的參數： *DontWait* 和 *MinimumCallThreads*。 您的伺服器程式可以傳遞非零值給 *DontWait* 參數。 如果有的話， **RpcServerListen** 函式將會立即傳回。 使用 [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) 常式來執行通常與 **RpcServerListen** 相關聯的等候作業。

 

 




