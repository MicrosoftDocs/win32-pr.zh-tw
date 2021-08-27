---
title: 非同步撥號狀態
description: 此頁面描述 RPC 呼叫的非同步撥號狀態。
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7ab00104b305ac87fa87883031d2425f229ce5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478624"
---
# <a name="asynchronous-call-state"></a>非同步撥號狀態

此頁面描述 RPC 呼叫的非同步撥號狀態。

## <a name="client-behavior"></a>用戶端行為




| 狀態 | 狀態名稱 | 動作 | 
|-------|------------|--------|
| C | 進行呼叫 | 讓 RPC<ul><li>成功時移至狀態 WComp</li><li>發生例外狀況時移至結尾</li></ul>失敗：前往 [可以]<br /> | 
| 可以 | 取消呼叫 | 呼叫 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>前往 WComp<br /> | 
| WComp | 等候完成 | 等候 notificationCall-應會收到完整通知<br /> 移至 [複合]<br /> | 
| Comp | Completion | 問題 <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>移至結尾<br /> | 
| 結束 | 




 

## <a name="server-behavior"></a>伺服器行為



| 狀態 | 狀態名稱     | 動作                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D     | 分派       | 呼叫是由 RPC runtimeProcess 分派<br/> 移至 [複合]<br/> 若要在 RPC 執行緒上執行時失敗嚴重 () ：引發例外狀況;移至結尾<br/> 若要正常地失敗：請移至<br/> |
| A     | 中止呼叫 | 呼叫 [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)Go to End<br/>                                                                                                                                             |
| Comp  | Completion     | 問題 [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)移至結尾<br/>                                                                                                                                      |
| 結束   |                |                                                                                                                                                                                                                     |



 

 

 





