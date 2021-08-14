---
title: 'RpcTryExcept (的 Rpc .h) '
description: RpcTryExcept 語句提供 RPC 應用程式的結構化例外狀況處理。
ms.assetid: 3addb367-4bdc-4c11-bf4d-b5b94da45b26
keywords:
- RpcTryExcept RPC
topic_type:
- apiref
api_name:
- RpcTryExcept
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c7a73ca80eb342b9a23fcaa4b922afe8d19f00e1f22ab82f8c6027ecc43d76d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925965"
---
# <a name="rpctryexcept"></a>RpcTryExcept

**RpcTryExcept** 語句提供 RPC 應用程式的結構化例外狀況處理。 如果 **RpcTryExcept** 中的任何程式語句造成例外狀況，則會執行 [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) 程式碼區塊中的語句。 所有 **RpcTryExcept** 語句都必須由 [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) 語句終止。

如需詳細資訊，請參閱 [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)。

**Windows Vista 和更新版本的 Windows：** 建議對最常見的例外狀況進行結構化例外狀況處理，做為使用 [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)的自訂 [**篩選準則的**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)替代方案。  

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Rpc。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)
</dt> <dt>

[**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)
</dt> <dt>

[**RpcTryFinally**](rpctryfinally.md)
</dt> </dl>

 

