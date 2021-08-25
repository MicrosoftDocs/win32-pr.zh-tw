---
title: '系結選項常數 (Rpcdce .h) '
description: 應用程式會設定系結選項常數，以控制 RPC 執行時間程式庫處理遠端程序呼叫的方式。 下表列出每個系結屬性，以及系結屬性的相關常數值。
ms.assetid: ff88e05d-b9f3-42ef-a44f-fee9261832c8
topic_type:
- apiref
api_name:
- RPC_C_OPT_BINDING_NONCAUSAL
- RPC_C_OPT_MAX_OPTIONS
- RPC_C_DONT_FAIL
- RPC_C_OPT_SESSION_ID
- RPC_C_OPT_COOKIE_AUTH
- RPC_C_OPT_RESOURCE_TYPE_UUID
- RPC_C_OPT_DONT_LINGER
- RPC_C_OPT_UNIQUE_BINDING
api_location:
- Rpcdce.h
- Rpcdcep.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 147d36cf66bb3a45add61b8639ccd3fada31856e72fce8c1f96d7a021e1d5e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023118"
---
# <a name="binding-option-constants"></a>系結選項常數

應用程式會設定系結選項常數，以控制 RPC 執行時間程式庫處理遠端程序呼叫的方式。 下表列出每個系結屬性，以及系結屬性的相關常數值。

> [!Note]  
> 下表中 (MQ) 的所有訊息佇列選項僅適用于 Windows 2000。 WindowsXP 和更新版本不支援訊息佇列。 開發人員不建議使用訊息佇列。

 



| 常數/值                                                                                                                                                                                                                                                        | 描述                                                                                                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_OPT_BINDING_NONCAUSAL"></span><span id="rpc_c_opt_binding_noncausal"></span><dl> <dt>**RPC \_C \_ OPT \_ \_**</dt>系結 NONCAUSAL <dt>9</dt> </dl>     | 預設值。 如果 **為 FALSE**，則為因果呼叫順序。 RPC 呼叫會以嚴格的提交順序來執行。 請參閱＜備註＞。<br/> 若 **為 TRUE**，則 noncausal 呼叫順序。 RPC 呼叫會獨立執行。 請參閱＜備註＞。<br/>                                                                        |
| <span id="RPC_C_OPT_MAX_OPTIONS"></span><span id="rpc_c_opt_max_options"></span><dl> <dt>**RPC \_C \_ OPT \_ 最大 \_ 選項**</dt> <dt>17</dt> </dl>                      | 應用程式不需要。 由 Microsoft 在內部使用。<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_DONT_FAIL"></span><span id="rpc_c_dont_fail"></span><dl> <dt>**RPC \_C \_ 不 \_ 會失敗**</dt> <dt>4</dt> </dl>                                          | 應用程式不需要。 由 Microsoft 在內部使用。<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_SESSION_ID"></span><span id="rpc_c_opt_session_id"></span><dl> <dt>**RPC \_C \_ OPT \_ 會話 \_ 識別碼**</dt> <dt>6</dt> </dl>                          | 若 **為 TRUE**，則會為每個連接產生會話識別碼。<br/>                                                                                                                                                                                                                                |
| <span id="RPC_C_OPT_COOKIE_AUTH"></span><span id="rpc_c_opt_cookie_auth"></span><dl> <dt>**RPC \_C \_ OPT \_ COOKIE \_ 驗證**</dt> <dt>7</dt> </dl>                       | 若為 **TRUE**，則會使用以用戶端 cookie 為基礎的驗證來進行連接。 [**RPC \_ C \_ OPT \_ COOKIE \_ 驗證 \_ 描述**](/windows/desktop/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor)元結構的指標會在 [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)中做為 *OptionValue* 參數傳遞。<br/> |
| <span id="RPC_C_OPT_RESOURCE_TYPE_UUID"></span><span id="rpc_c_opt_resource_type_uuid"></span><dl> <dt>**RPC \_C \_ OPT \_ 資源 \_ 類型 \_ UUID**</dt> <dt>8</dt> </dl> | 應用程式不需要。 由 Microsoft 在內部使用。<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_DONT_LINGER"></span><span id="rpc_c_opt_dont_linger"></span><dl> <dt>**RPC \_C \_ OPT \_ \_**</dt>不會逗留 <dt>13</dt> </dl>                      | 若 **為 TRUE**，則會在釋放關聯的最後一個系結控制碼/內容控制碼之後，強制關閉該關聯。<br/>                                                                                                                                                                                |
| <span id="RPC_C_OPT_UNIQUE_BINDING"></span><span id="rpc_c_opt_unique_binding"></span><dl> <dt>**RPC \_C \_ OPT \_ 唯一 \_**</dt>系結 <dt>11</dt> </dl>             | 當設為 **true** 時，RPC 不會重複使用現有的連接。 針對每個連接開啟唯一的系結控制碼，並為每個唯一的系結控制碼維護狀態。<br/>                                                                                                               |



## <a name="remarks"></a>備註

根據預設，RPC 執行時間程式庫會以嚴格的提交順序，從應用程式的每個執行緒在給定的系結控制碼上執行呼叫。 這並不保證會序列化相同系結控制碼上不同執行緒的呼叫。 多執行緒應用程式必須序列化其 RPC 呼叫。 如果此行為過於嚴格，您可以啟用 noncausal 順序。 當您這樣做時，RPC 執行時間程式庫會獨立執行呼叫。 它不會在提交時進行排序。

可能會發現 noncausal 順序的應用程式範例之一，就是執行緒在相同系結控制碼上進行呼叫的多執行緒程式。 同樣地，在系結控制碼上使用多個非同步呼叫的程式，會發現 noncausal 順序是一個方便的選項。 另一個範例可能是使用單一線程處理數個用戶端要求的網際網路 proxy 程式。 在上述每一種情況下，嘗試序列化遠端程序呼叫是非常嚴格的。

您只能在使用 **ncalrpc** 或 **\_ \* ncacn* _ 通訊協定序列的系結控制碼上設定「 **RPC \_ C \_ OPT 未 \_ \_ 逗留**」選項。 它不能用在 _*ncadg \_ \**_ 通訊協定序列上。 具有此選項的 [_ *RpcBindingSetOption* *](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)函式必須在至少進行一個 RPC 呼叫的系結控制碼上呼叫。 如果未在系結控制碼上進行 RPC 呼叫，則會從 **RpcBindingSetOption** 函式呼叫傳回 **rpc \_ S \_ 錯誤 \_ \_ 的 \_** 系結類型。 不論附加至關聯的系結控制碼有多少，此選項都會對整個關聯生效。 由於在關聯終結之前會先進行檢查，因此可以在系結控制碼關閉之前隨時進行設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                 |
| 標頭<br/>                   | <dl> <dt>Rpcdce .h;</dt><dt>Rpcdcep .h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[**RpcBindingInqOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[管理 (關聯) 的網路連接集 ](managing-network-connection-sets-associations-.md)
</dt> </dl>

 

 





