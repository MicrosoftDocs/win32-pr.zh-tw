---
title: 'RPC_NS_HANDLE (Rpcnsi) '
description: RPC \_ NS \_ 控制碼資料類型定義了名稱服務控制碼。
ms.assetid: d9c2a376-4972-4f16-aa8d-f0e43d5ddb8d
keywords:
- RPC_NS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e72ee694e08be1b30a75dc1f5b986619043d592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509203"
---
# <a name="rpc_ns_handle"></a>RPC \_ NS \_ 控制碼

**RPC \_ NS \_ 控制碼** 資料類型定義了名稱服務控制碼。


```C++
typedef void* RPC_NS_HANDLE;
```



## <a name="remarks"></a>備註

名稱服務控制碼是一個不透明的變數，其中包含 RPC 執行時間程式庫用來從名稱-服務資料庫傳回下列 RPC 資料的資訊：

-   伺服器系結控制碼
-   伺服器設定檔成員所提供資源的 Uuid
-   群組成員

名稱服務控制碼的範圍是從「開始」常式到對應的「完成」常式。

應用程式會負責並行控制跨執行緒的名稱服務控制碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>Rpcnsi (包含 Rpc) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone)
</dt> <dt>

[**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)
</dt> <dt>

[**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[**RpcNsBindingLookupDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone)
</dt> <dt>

[**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)
</dt> </dl>

 

 





