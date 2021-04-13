---
title: WFP 錯誤碼 (Winerror.h)
description: " (WFP) 特定錯誤碼。"
ms.assetid: 11f3085a-f044-4a78-b47a-59b9086562bf
topic_type:
- apiref
api_name:
- FWP_E_CALLOUT_NOT_FOUND
- FWP_E_CONDITION_NOT_FOUND
- FWP_E_FILTER_NOT_FOUND
- FWP_E_LAYER_NOT_FOUND
- FWP_E_PROVIDER_NOT_FOUND
- FWP_E_PROVIDER_CONTEXT_NOT_FOUND
- FWP_E_SUBLAYER_NOT_FOUND
- FWP_E_NOT_FOUND
- FWP_E_ALREADY_EXISTS
- FWP_E_IN_USE
- FWP_E_DYNAMIC_SESSION_IN_PROGRESS
- FWP_E_WRONG_SESSION
- FWP_E_NO_TXN_IN_PROGRESS
- FWP_E_TXN_IN_PROGRESS
- FWP_E_TXN_ABORTED
- FWP_E_SESSION_ABORTED
- FWP_E_INCOMPATIBLE_TXN
- FWP_E_TIMEOUT
- FWP_E_NET_EVENTS_DISABLED
- FWP_E_INCOMPATIBLE_LAYER
- FWP_E_KM_CLIENTS_ONLY
- FWP_E_LIFETIME_MISMATCH
- FWP_E_BUILTIN_OBJECT
- FWP_E_TOO_MANY_CALLOUTS
- FWP_E_NOTIFICATION_DROPPED
- FWP_E_TRAFFIC_MISMATCH
- FWP_E_INCOMPATIBLE_SA_STATE
- FWP_E_NULL_POINTER
- FWP_E_INVALID_ENUMERATOR
- FWP_E_INVALID_FLAGS
- FWP_E_INVALID_NET_MASK
- FWP_E_INVALID_RANGE
- FWP_E_INVALID_INTERVAL
- FWP_E_ZERO_LENGTH_ARRAY
- FWP_E_NULL_DISPLAY_NAME
- FWP_E_INVALID_ACTION_TYPE
- FWP_E_INVALID_WEIGHT
- FWP_E_MATCH_TYPE_MISMATCH
- FWP_E_TYPE_MISMATCH
- FWP_E_OUT_OF_BOUNDS
- FWP_E_RESERVED
- FWP_E_DUPLICATE_CONDITION
- FWP_E_DUPLICATE_KEYMOD
- FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER
- FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT
- FWP_E_INCOMPATIBLE_AUTH_METHOD
- FWP_E_INCOMPATIBLE_DH_GROUP
- FWP_E_EM_NOT_SUPPORTED
- FWP_E_NEVER_MATCH
- FWP_E_PROVIDER_CONTEXT_MISMATCH
- FWP_E_INVALID_PARAMETER
- FWP_E_TOO_MANY_SUBLAYERS
- FWP_E_CALLOUT_NOTIFICATION_FAILED
- FWP_E_INVALID_AUTH_TRANSFORM
- FWP_E_INVALID_CIPHER_TRANSFORM
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a0e7ee1ab0364a31f136f0c0cdbf87f459225b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466053"
---
# <a name="wfp-error-codes"></a>WFP 錯誤碼

Windows 篩選平台 (WFP) 特定錯誤碼如下所示。

<dl> <dt>

<span id="FWP_E_CALLOUT_NOT_FOUND"></span><span id="fwp_e_callout_not_found"></span>**\_ \_ \_ \_ 找不到 .FWP E 標注**
</dt> <dd> <dl> <dt>

0x80320001
</dt> <dt>



標注不存在。


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONDITION_NOT_FOUND"></span><span id="fwp_e_condition_not_found"></span>**\_ \_ \_ \_ 找不到 .FWP E 條件**
</dt> <dd> <dl> <dt>

0x80320002
</dt> <dt>



篩選準則不存在。


</dt> </dl> </dd> <dt>

<span id="FWP_E_FILTER_NOT_FOUND"></span><span id="fwp_e_filter_not_found"></span>**\_ \_ \_ \_ 找不到 .FWP E 篩選**
</dt> <dd> <dl> <dt>

0x80320003
</dt> <dt>



篩選不存在。


</dt> </dl> </dd> <dt>

<span id="FWP_E_LAYER_NOT_FOUND"></span><span id="fwp_e_layer_not_found"></span>**\_ \_ \_ 找不到 .FWP E 圖層 \_**
</dt> <dd> <dl> <dt>

0x80320004
</dt> <dt>



圖層不存在。


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_NOT_FOUND"></span><span id="fwp_e_provider_not_found"></span>**\_ \_ \_ 找不到 .FWP E 提供者 \_**
</dt> <dd> <dl> <dt>

0x80320005
</dt> <dt>



提供者不存在。


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_NOT_FOUND"></span><span id="fwp_e_provider_context_not_found"></span>**\_ \_ \_ \_ \_ 找不到 .FWP E 提供者內容**
</dt> <dd> <dl> <dt>

0x80320006
</dt> <dt>



提供者內容不存在。


</dt> </dl> </dd> <dt>

<span id="FWP_E_SUBLAYER_NOT_FOUND"></span><span id="fwp_e_sublayer_not_found"></span>**\_ \_ \_ \_ 找不到 .FWP E 子層**
</dt> <dd> <dl> <dt>

0x80320007
</dt> <dt>



子層不存在。


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOT_FOUND"></span><span id="fwp_e_not_found"></span>**\_ \_ 找不到 .FWP E \_**
</dt> <dd> <dl> <dt>

0x80320008
</dt> <dt>



物件不存在。

如果找不到 SA 內容識別碼， [IPsecSaCoNtext \* ](fwp-ipsec-functions.md)函數會傳回此錯誤。


</dt> </dl> </dd> <dt>

<span id="FWP_E_ALREADY_EXISTS"></span><span id="fwp_e_already_exists"></span>**\_ \_ 已有 .FWP \_ E**
</dt> <dd> <dl> <dt>

0x80320009
</dt> <dt>



具有 GUID 或 LUID 的物件已經存在。


</dt> </dl> </dd> <dt>

<span id="FWP_E_IN_USE"></span><span id="fwp_e_in_use"></span>**\_ \_ 使用中的 .FWP 電子 \_**
</dt> <dd> <dl> <dt>

0x8032000A
</dt> <dt>



物件是由其他物件所參考，所以無法刪除。


</dt> </dl> </dd> <dt>

<span id="FWP_E_DYNAMIC_SESSION_IN_PROGRESS"></span><span id="fwp_e_dynamic_session_in_progress"></span>**\_ \_ \_ \_ 正在進行的 .FWP 電子動態會話 \_**
</dt> <dd> <dl> <dt>

0x8032000B
</dt> <dt>



不允許從動態會話內呼叫。


</dt> </dl> </dd> <dt>

<span id="FWP_E_WRONG_SESSION"></span><span id="fwp_e_wrong_session"></span>**.FWP 的 \_ 電子 \_ 錯誤 \_ 會話**
</dt> <dd> <dl> <dt>

0x8032000C
</dt> <dt>



從錯誤的會話進行呼叫，因此無法完成。


</dt> </dl> </dd> <dt>

<span id="FWP_E_NO_TXN_IN_PROGRESS"></span><span id="fwp_e_no_txn_in_progress"></span>**\_ \_ 未 \_ \_ \_ 進行的 .FWP E TXN**
</dt> <dd> <dl> <dt>

0x8032000D
</dt> <dt>



呼叫必須從明確交易內進行。


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_IN_PROGRESS"></span><span id="fwp_e_txn_in_progress"></span>**\_ \_ \_ 正在進行的 .FWP 電子 TXN \_**
</dt> <dd> <dl> <dt>

0x8032000E
</dt> <dt>



不允許從明確交易內呼叫。


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_ABORTED"></span><span id="fwp_e_txn_aborted"></span>**已 \_ 中止 .FWP E \_ TXN \_**
</dt> <dd> <dl> <dt>

0x8032000F
</dt> <dt>



明確的交易已強制取消。


</dt> </dl> </dd> <dt>

<span id="FWP_E_SESSION_ABORTED"></span><span id="fwp_e_session_aborted"></span>**已 \_ 中止 .FWP E \_ 會話 \_**
</dt> <dd> <dl> <dt>

0x80320010
</dt> <dt>



會話已取消。

會話控制碼必須藉由呼叫 [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0)來關閉，即使它已不再有效也是一樣。否則，用戶端狀態將會流失。 您應呼叫 [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)來建立新的會話。


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_TXN"></span><span id="fwp_e_incompatible_txn"></span>**.FWP 的 \_ 電子 \_ 不相容 \_ TXN**
</dt> <dd> <dl> <dt>

0x80320011
</dt> <dt>



不允許在唯讀交易內進行呼叫。


</dt> </dl> </dd> <dt>

<span id="FWP_E_TIMEOUT"></span><span id="fwp_e_timeout"></span>**.FWP \_ E \_ TIMEOUT**
</dt> <dd> <dl> <dt>

0x80320012
</dt> <dt>



呼叫會在等候取得交易鎖定的時候超時。


</dt> </dl> </dd> <dt>

<span id="FWP_E_NET_EVENTS_DISABLED"></span><span id="fwp_e_net_events_disabled"></span>**\_ \_ \_ \_ 已停用 .FWP 的電子網路**
</dt> <dd> <dl> <dt>

0x80320013
</dt> <dt>



已停用網路診斷事件的收集。


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_LAYER"></span><span id="fwp_e_incompatible_layer"></span>**.FWP \_ E \_ 不相容的 \_ 圖層**
</dt> <dd> <dl> <dt>

0x80320014
</dt> <dt>



指定的層級不支援此作業。


</dt> </dl> </dd> <dt>

<span id="FWP_E_KM_CLIENTS_ONLY"></span><span id="fwp_e_km_clients_only"></span>**\_僅限 .FWP 的 E \_ KM \_ 用戶端 \_**
</dt> <dd> <dl> <dt>

0x80320015
</dt> <dt>



只有核心模式呼叫端可以呼叫。


</dt> </dl> </dd> <dt>

<span id="FWP_E_LIFETIME_MISMATCH"></span><span id="fwp_e_lifetime_mismatch"></span>**.FWP \_ E \_ 存留期 \_ 不符**
</dt> <dd> <dl> <dt>

0x80320016
</dt> <dt>



呼叫嘗試將兩個物件與不相容的存留期產生關聯。

如需物件存留期和物件關聯的詳細資訊，請參閱 [物件管理](object-management.md) 。


</dt> </dl> </dd> <dt>

<span id="FWP_E_BUILTIN_OBJECT"></span><span id="fwp_e_builtin_object"></span>**.FWP \_ E 內 \_ 建 \_ 物件**
</dt> <dd> <dl> <dt>

0x80320017
</dt> <dt>



物件是內建的，因此無法刪除。


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_CALLOUTS"></span><span id="fwp_e_too_many_callouts"></span>**.FWP 的 \_ 電子 \_ 太 \_ 多 \_ 標注**
</dt> <dd> <dl> <dt>

0x80320018
</dt> <dt>



已達到最大的標注數目。

最多可以同時註冊100000個標注。


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOTIFICATION_DROPPED"></span><span id="fwp_e_notification_dropped"></span>**已捨棄的 .FWP \_ E \_ 通知 \_**
</dt> <dd> <dl> <dt>

0x80320019
</dt> <dt>



因為訊息佇列的最大容量，所以無法傳遞通知。


</dt> </dl> </dd> <dt>

<span id="FWP_E_TRAFFIC_MISMATCH"></span><span id="fwp_e_traffic_mismatch"></span>**.FWP 的 \_ 電子 \_ 流量 \_ 不符**
</dt> <dd> <dl> <dt>

0x8032001A
</dt> <dt>



網路流量參數不符合安全性關聯內容的參數。

您可以多次呼叫 [**IPsecSaCoNtextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) ，但呼叫端必須每次都指定相同的 [**IPSEC \_ TRAFFIC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) 。 如果後續的呼叫提供不同的 **IPSEC \_ TRAFFIC0**，則會傳回此錯誤。


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_SA_STATE"></span><span id="fwp_e_incompatible_sa_state"></span>**.FWP \_ E \_ 不相容的 \_ SA \_ 狀態**
</dt> <dd> <dl> <dt>

0x8032001B
</dt> <dt>



 (SA) 狀態的目前安全性關聯不允許此呼叫。

SA 內容函式必須以特定順序呼叫：

-   [**IPsecSaCoNtextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)
-   [**IPsecSaCoNtextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)
-   [**IPsecSaCoNtextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)
-   [**IPsecSaCoNtextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)

如果以順序呼叫此錯誤，就會傳回此錯誤。


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_POINTER"></span><span id="fwp_e_null_pointer"></span>**.FWP \_ E \_ Null \_ 指標**
</dt> <dd> <dl> <dt>

0x8032001C
</dt> <dt>



必要的指標為 null。


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ENUMERATOR"></span><span id="fwp_e_invalid_enumerator"></span>**.FWP \_ E \_ 不正確 \_ 枚舉器**
</dt> <dd> <dl> <dt>

0x8032001D
</dt> <dt>



結構中的列舉值超出範圍。


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_FLAGS"></span><span id="fwp_e_invalid_flags"></span>**.FWP \_ E \_ 不正確 \_ 旗標**
</dt> <dd> <dl> <dt>

0x8032001E
</dt> <dt>



[旗標] 欄位包含不正確值。


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_NET_MASK"></span><span id="fwp_e_invalid_net_mask"></span>**.FWP \_ E \_ 不正確 \_ 淨 \_ 遮罩**
</dt> <dd> <dl> <dt>

0x8032001F
</dt> <dt>



網路遮罩無效。


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_RANGE"></span><span id="fwp_e_invalid_range"></span>**.FWP \_ E \_ 無效 \_ 範圍**
</dt> <dd> <dl> <dt>

0x80320020
</dt> <dt>



[**.Fwp \_ RANGE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0)結構無效。


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_INTERVAL"></span><span id="fwp_e_invalid_interval"></span>**.FWP \_ E \_ 無效 \_ 間隔**
</dt> <dd> <dl> <dt>

0x80320021
</dt> <dt>



時間間隔無效。


</dt> </dl> </dd> <dt>

<span id="FWP_E_ZERO_LENGTH_ARRAY"></span><span id="fwp_e_zero_length_array"></span>**.FWP \_ E \_ 零 \_ 長度 \_ 陣列**
</dt> <dd> <dl> <dt>

0x80320022
</dt> <dt>



必須包含至少一個元素的陣列長度為零。


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_DISPLAY_NAME"></span><span id="fwp_e_null_display_name"></span>**.FWP \_ E \_ Null \_ 顯示 \_ 名稱**
</dt> <dd> <dl> <dt>

0x80320023
</dt> <dt>



**DisplayData.name** 欄位不可以是 null。


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ACTION_TYPE"></span><span id="fwp_e_invalid_action_type"></span>**.FWP \_ E \_ 不正確 \_ 動作 \_ 類型**
</dt> <dd> <dl> <dt>

0x80320024
</dt> <dt>



動作類型不是篩選準則的其中一個允許動作類型。


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_WEIGHT"></span><span id="fwp_e_invalid_weight"></span>**.FWP \_ E \_ 不正確 \_ 權數**
</dt> <dd> <dl> <dt>

0x80320025
</dt> <dt>



篩選權數無效。

如需詳細資訊，請參閱 [篩選權數指派](filter-weight-assignment.md) 。


</dt> </dl> </dd> <dt>

<span id="FWP_E_MATCH_TYPE_MISMATCH"></span><span id="fwp_e_match_type_mismatch"></span>**.FWP \_ E \_ 符合 \_ 類型 \_ 不符**
</dt> <dd> <dl> <dt>

0x80320026
</dt> <dt>



篩選準則包含與運算元不相容的比對類型。

如需詳細資訊，請參閱 [**.Fwp \_ 相符 \_ 類型**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) 。


</dt> </dl> </dd> <dt>

<span id="FWP_E_TYPE_MISMATCH"></span><span id="fwp_e_type_mismatch"></span>**.FWP \_ E \_ 類型 \_ 不符**
</dt> <dd> <dl> <dt>

0x80320027
</dt> <dt>



[**.Fwp \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0)結構或 [**FWPM \_ 條件 \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0)結構的型別錯誤。


</dt> </dl> </dd> <dt>

<span id="FWP_E_OUT_OF_BOUNDS"></span><span id="fwp_e_out_of_bounds"></span>**已 \_ \_ 超出 \_ 範圍的 \_ .FWP E**
</dt> <dd> <dl> <dt>

0x80320028
</dt> <dt>



整數值超出允許的範圍。


</dt> </dl> </dd> <dt>

<span id="FWP_E_RESERVED"></span><span id="fwp_e_reserved"></span>**.FWP \_ E \_ 保留**
</dt> <dd> <dl> <dt>

0x80320029
</dt> <dt>



保留的欄位不是零。


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_CONDITION"></span><span id="fwp_e_duplicate_condition"></span>**.FWP \_ E \_ 重複 \_ 條件**
</dt> <dd> <dl> <dt>

0x8032002A
</dt> <dt>



篩選準則不能包含多個在單一欄位上運作的條件。


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_KEYMOD"></span><span id="fwp_e_duplicate_keymod"></span>**.FWP \_ E \_ 重複的 \_ KEYMOD**
</dt> <dd> <dl> <dt>

0x8032002B
</dt> <dt>



原則不能包含相同的加密模組一次以上。


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_action_incompatible_with_layer"></span>**\_ \_ \_ \_ 與圖層不相容的 \_ .FWP E 動作**
</dt> <dd> <dl> <dt>

0x8032002C
</dt> <dt>



動作類型與圖層不相容。


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER"></span><span id="fwp_e_action_incompatible_with_sublayer"></span>**\_ \_ \_ \_ 具有子層的 .FWP E 動作不相容 \_**
</dt> <dd> <dl> <dt>

0x8032002D
</dt> <dt>



動作類型與子層不相容。


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_context_incompatible_with_layer"></span>**.FWP \_ E \_ 內容 \_ \_ 與 \_ 圖層不相容**
</dt> <dd> <dl> <dt>

0x8032002E
</dt> <dt>



原始內容或提供者內容與圖層不相容。


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT"></span><span id="fwp_e_context_incompatible_with_callout"></span>**.FWP \_ E \_ 內容 \_ \_ 與 \_ 標注不相容**
</dt> <dd> <dl> <dt>

0x8032002F
</dt> <dt>



原始內容或提供者內容與標注不相容。


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_AUTH_METHOD"></span><span id="fwp_e_incompatible_auth_method"></span>**.FWP 的 \_ 電子 \_ 不相容 \_ AUTH \_ 方法**
</dt> <dd> <dl> <dt>

0x80320030
</dt> <dt>



驗證方法與原則類型不相容。


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_DH_GROUP"></span><span id="fwp_e_incompatible_dh_group"></span>**.FWP 的 \_ 電子 \_ 不相容 \_ DH \_ 群組**
</dt> <dd> <dl> <dt>

0x80320031L
</dt> <dt>



Diffie-Hellman 群組與原則類型不相容。


</dt> </dl> </dd> <dt>

<span id="FWP_E_EM_NOT_SUPPORTED"></span><span id="fwp_e_em_not_supported"></span>**\_ \_ \_ 不支援 .FWP E \_ EM**
</dt> <dd> <dl> <dt>

0x80320032
</dt> <dt>



IKE 原則不能包含擴充模式原則。


</dt> </dl> </dd> <dt>

<span id="FWP_E_NEVER_MATCH"></span><span id="fwp_e_never_match"></span>**.FWP \_ E \_ 永不 \_ 相符**
</dt> <dd> <dl> <dt>

0x80320033
</dt> <dt>



列舉範本或訂閱永遠不會與任何物件相符。


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_MISMATCH"></span><span id="fwp_e_provider_context_mismatch"></span>**.FWP \_ E \_ 提供者 \_ 內容 \_ 不符**
</dt> <dd> <dl> <dt>

0x80320034
</dt> <dt>



提供者內容的類型錯誤。


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_PARAMETER"></span><span id="fwp_e_invalid_parameter"></span>**.FWP \_ E \_ 不正確 \_ 參數**
</dt> <dd> <dl> <dt>

0x80320035
</dt> <dt>



參數錯誤。

此錯誤的可能原因：

-   呼叫 [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)時，不需將旗標 **FWPM 通道旗標指向 [ \_ \_ \_ \_ \_ 點**] 和 [本機/遠端位址以外的條件]。
-   不正確 Unicode 字串，或包含不可列印字元的 Unicode 字串。


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_SUBLAYERS"></span><span id="fwp_e_too_many_sublayers"></span>**.FWP 的 \_ 電子郵件 \_ 太 \_ 多 \_ 子層**
</dt> <dd> <dl> <dt>

0x80320036
</dt> <dt>



已達到子層的最大數目。

WFP 最多可支援 2 6 個子層。


</dt> </dl> </dd> <dt>

<span id="FWP_E_CALLOUT_NOTIFICATION_FAILED"></span><span id="fwp_e_callout_notification_failed"></span>**.FWP \_ E \_ 標注 \_ 通知 \_ 失敗**
</dt> <dd> <dl> <dt>

0x80320037
</dt> <dt>



標注的通知函數傳回錯誤。


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_AUTH_TRANSFORM"></span><span id="fwp_e_invalid_auth_transform"></span>**.FWP \_ 電子 \_ 不正確 \_ 驗證 \_ 轉換**
</dt> <dd> <dl> <dt>

0x80320038
</dt> <dt>



IPsec 驗證轉換無效。


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_CIPHER_TRANSFORM"></span><span id="fwp_e_invalid_cipher_transform"></span>**.FWP \_ E \_ 不正確 \_ 密碼 \_ 轉換**
</dt> <dd> <dl> <dt>

0x80320039
</dt> <dt>



IPsec 加密轉換無效。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Winerror.h。h</dt> </dl> |



 

 





