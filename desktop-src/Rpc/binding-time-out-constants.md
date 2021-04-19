---
title: '系結超時常數 (Rpcdce .h) '
description: RPC 程式庫會使用系結超時常數來指定在放棄之前，建立伺服器系結所需花費的相對時間量。
ms.assetid: bf5f3f08-ab29-4732-9ce3-d6d7ad699369
topic_type:
- apiref
api_name:
- RPC_C_BINDING_INFINITE_TIMEOUT
- RPC_C_BINDING_MIN_TIMEOUT
- RPC_C_BINDING_DEFAULT_TIMEOUT
- RPC_C_BINDING_MAX_TIMEOUT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096fd320e1341f9affc35ae6ff1d355fcf12d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106993743"
---
# <a name="binding-time-out-constants"></a>系結超時常數

RPC 程式庫會使用系結超時常數來指定在放棄之前，建立伺服器系結所需花費的相對時間量。 您可以透過呼叫 [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) 函式來啟用超時。 下列清單包含有效的超時值。



| 常數/值                                                                                                                                                                                                                                                                | Description                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_BINDING_INFINITE_TIMEOUT"></span><span id="rpc_c_binding_infinite_timeout"></span><dl> <dt>**RPC \_C 系結 \_ \_ 無限 \_ 超時時間**</dt> <dt> 10</dt> </dl> | 繼續嘗試永遠建立通訊。<br/>                                                                                                                                                             |
| <span id="RPC_C_BINDING_MIN_TIMEOUT"></span><span id="rpc_c_binding_min_timeout"></span><dl> <dt>**RPC \_C 系結 \_ \_ 最小 \_ 超時**</dt> <dt>0</dt> </dl>                   | 嘗試使用網路通訊協定的最小時間量。 此值會在判斷伺服器是否正在執行時，優先于正確的回應時間。<br/>                                          |
| <span id="RPC_C_BINDING_DEFAULT_TIMEOUT"></span><span id="rpc_c_binding_default_timeout"></span><dl> <dt>**RPC \_C 系結 \_ \_ 預設 \_ 超時**</dt> <dt>5</dt> </dl>       | 嘗試使用網路通訊協定的平均時間量。 此值可讓您判斷伺服器是否正在執行，並提供回應時間的相等加權。 這是預設值。<br/> |
| <span id="RPC_C_BINDING_MAX_TIMEOUT"></span><span id="rpc_c_binding_max_timeout"></span><dl> <dt>**RPC \_C 系結 \_ \_ 最大 \_ 超時**</dt> <dt>9</dt> </dl>                   | 嘗試使用網路通訊協定的最長時間量。 此值會在判斷伺服器是否正在回應時間執行時，優先于判斷是否正確。<br/>                                            |



## <a name="remarks"></a>備註

上表中的值不是以秒為單位。 這些值代表以零到10之小數位數的相對時間量。 如需避免通訊延遲的詳細資訊，請參閱防止用戶端停止回應。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Rpcdce。h</dt> </dl> |



 

 





