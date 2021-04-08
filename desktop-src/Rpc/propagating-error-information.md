---
title: 傳播錯誤資訊
description: 傳播延伸的錯誤資訊可讓接收 RPC \_ S 錯誤的伺服器 \_ 或任何其他錯誤碼，讓 rpc 執行時間將所收到的資訊傳播至其呼叫端。
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd20575cee304c0a1693ae4bc6442de4837caa0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840552"
---
# <a name="propagating-error-information"></a>傳播錯誤資訊

傳播延伸的錯誤資訊可讓接收 RPC 錯誤的 \_ 伺服器 \_ \* 或任何其他錯誤碼，讓 rpc 執行時間將其接收的資訊傳播至其呼叫端。 所有伺服器都必須在遇到嚴重錯誤時呼叫 [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) 或 [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) 。 RPC 執行時間會負責連結擴充的錯誤資訊（如果有的話），這會造成嚴重錯誤，以報告嚴重錯誤本身，只要提供給 **RpcRaiseException** 或 **RpcAsyncAbortCall** 的錯誤碼與造成嚴重錯誤的錯誤碼相同即可。

 

 




