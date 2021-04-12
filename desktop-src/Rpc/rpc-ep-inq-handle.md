---
title: 'RPC_EP_INQ_HANDLE (Rpcasync) '
description: RPC \_ EP \_ INQ \_ 控制碼資料類型會宣告查詢內容的控制碼。 RPC 應用程式會使用它來查看端點對應中儲存的伺服器位址資訊。
ms.assetid: e18ce800-0110-4450-9a1b-a3f777d00f2d
keywords:
- RPC_EP_INQ_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c34c64b5601b31485808924fc57dbe3412b6009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385134"
---
# <a name="rpc_ep_inq_handle"></a>RPC \_ EP \_ INQ \_ 控制碼

**RPC \_ EP \_ INQ \_ 控制碼** 資料類型會宣告查詢內容的控制碼。 RPC 應用程式會使用它來查看端點對應中儲存的伺服器位址資訊。


```C++
typedef I_RPC_HANDLE* RPC_EP_INQ_HANDLE;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>Rpcasync (包含 Rpc) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RpcMgmtEpEltInqBegin**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)
</dt> <dt>

[**RpcMgmtEpEltInqNext**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)
</dt> <dt>

[**RpcMgmtEpEltInqDone**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone)
</dt> </dl>

 

 





