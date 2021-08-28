---
title: 'RPC_BINDING_HANDLE (Rpcdce) '
description: RPC 系結 \_ 控制碼資料類型會宣告一個系結控制碼，其中包含 RPC 執行時間程式庫用來存取系結資訊的資訊。
ms.assetid: 3e07d9e9-04d8-4f94-8104-cd0ee89a9407
keywords:
- RPC_BINDING_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0218f1a7331a070340b7740c83f8464b2286de2698daf67ac1092aa5c057db03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018582"
---
# <a name="rpc_binding_handle"></a>RPC 系結 \_ \_ 控制碼

Rpc 系結 **\_ 控制碼** 資料類型會宣告一個系結控制碼，其中包含 RPC 執行時間程式庫用來存取系結資訊的資訊。


```C++
typedef I_RPC_HANDLE RPC_BINDING_HANDLE;
```



## <a name="remarks"></a>備註

執行時間程式庫會使用系結資訊來建立允許遠端程序呼叫執行的用戶端-伺服器關聯性。 根據建立系結控制碼的內容，它會被視為伺服器系結控制碼或用戶端系結控制碼。

伺服器系結控制碼包含用戶端建立與特定伺服器之關聯性所需的資訊。 任何數目的 RPC API 執行時間常式都會傳回伺服器系結控制碼，可用來進行遠端程序呼叫。

用戶端系結控制碼不能用來進行遠端程序呼叫。 RPC 執行時間程式庫會建立並提供用戶端系結控制碼給被呼叫的伺服器程式， (也稱為伺服器管理員常式) 做為 RPC 系結 \_ \_ 控制碼參數。 用戶端系結控制碼包含呼叫用戶端的相關資訊。

**\*  \*** \_ \_ \_ \_ \_ 當應用程式提供錯誤的系結控制碼類型時，RPCBINDING _ 和 _ RpcNsBinding 函式會傳回狀態碼 RPC S 錯誤的系結類型。

應用程式可以跨多個執行執行緒共用單一系結控制碼。 RPC 執行時間程式庫會管理使用單一系結控制碼的並行遠端程序呼叫。 但是，應用程式負責系結控制碼並行控制，以進行修改系結控制碼的作業。 這些作業包括下列常式：

-   [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)
-   [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)
-   [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
-   [**RpcBindingSetObject**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

例如，如果應用程式在兩個執行執行緒之間共用系結控制碼，並藉由呼叫 [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)在其中一個執行緒中重設系結控制碼端點，則結果為未定義。 另一個執行緒上的系結控制碼也可以重設，或作業可能會失敗，或是進程可能會損毀。 常見的錯誤是在其進行呼叫時釋放系結控制碼;這通常會導致呼叫進程損毀。

如果您不想要平行存取，您可以藉由呼叫 [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy)來設計應用程式，以建立系結控制碼的複本。 在這種情況下，第一個系結控制碼的作業對第二個系結控制碼沒有任何作用。

需要系結控制碼作為參數的常式會顯示 RPC 系 **結 \_ \_ 控制碼** 的資料類型。 系結控制碼參數會以傳值方式傳遞。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                |
| 標頭<br/>                   | <dl> <dt>Rpcdce (包含 Rpc) </dt> </dl> |



 

 





