---
title: 傳播錯誤資訊
description: 傳播延伸的錯誤資訊可讓接收 RPC \_ S 錯誤的伺服器 \_ 或任何其他錯誤碼，讓 rpc 執行時間將所收到的資訊傳播至其呼叫端。
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510ecf011dbac01d2b4c931a463bebb3739a92322059eb3a7a342160c42a9e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927156"
---
# <a name="propagating-error-information"></a>傳播錯誤資訊

傳播延伸的錯誤資訊可讓接收 RPC 錯誤的 \_ 伺服器 \_ \* 或任何其他錯誤碼，讓 rpc 執行時間將其接收的資訊傳播至其呼叫端。 所有伺服器都必須在遇到嚴重錯誤時呼叫 [**RpcRaiseException**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) 或 [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) 。 RPC 執行時間會負責連結擴充的錯誤資訊（如果有的話），這會造成嚴重錯誤，以報告嚴重錯誤本身，只要提供給 **RpcRaiseException** 或 **RpcAsyncAbortCall** 的錯誤碼與造成嚴重錯誤的錯誤碼相同即可。

 

 




