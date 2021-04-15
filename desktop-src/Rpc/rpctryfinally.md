---
title: 'RpcTryFinally (的 Rpc .h) '
description: RpcTryFinally 語句提供結構化終止處理。
ms.assetid: e9ed748a-db15-4c91-b8a4-b510f99042d8
keywords:
- RpcTryFinally RPC
topic_type:
- apiref
api_name:
- RpcTryFinally
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 909d65013fb3fb83ffb926fea6a6b3f30980a3b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465833"
---
# <a name="rpctryfinally"></a>RpcTryFinally

**RpcTryFinally** 語句提供結構化終止處理。 例外狀況發生在與 **RpcTryFinally** 語句相關聯之程式碼區塊的執行語句期間，會執行與 [**RpcFinally**](/previous-versions/aa375699(v=vs.80)) 語句相關聯之程式碼區塊中的語句。 所有 **RpcTryFinally** 語句都必須由 [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) 語句終止。

如需詳細資訊，請參閱 [**RpcFinally**](/previous-versions/aa375699(v=vs.80))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Rpc。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RpcFinally**](/previous-versions/aa375699(v=vs.80))
</dt> <dt>

[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))
</dt> </dl>

 

