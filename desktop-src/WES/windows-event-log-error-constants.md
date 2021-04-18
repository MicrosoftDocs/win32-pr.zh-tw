---
title: 'Windows 事件記錄檔錯誤常數 (Winerror.h .h) '
description: 以下是 Windows 事件記錄檔所定義的錯誤碼。
ms.assetid: 889ea4ae-dede-45d5-9293-cec85d81f010
topic_type:
- apiref
api_name:
- ERROR_EVT_INVALID_CHANNEL_PATH
- ERROR_EVT_INVALID_QUERY
- ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND
- ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND
- ERROR_EVT_INVALID_PUBLISHER_NAME
- ERROR_EVT_INVALID_EVENT_DATA
- ERROR_EVT_CHANNEL_NOT_FOUND
- ERROR_EVT_MALFORMED_XML_TEXT
- ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL
- ERROR_EVT_CONFIGURATION_ERROR
- ERROR_EVT_QUERY_RESULT_STALE
- ERROR_EVT_QUERY_RESULT_INVALID_POSITION
- ERROR_EVT_NON_VALIDATING_MSXML
- ERROR_EVT_FILTER_ALREADYSCOPED
- ERROR_EVT_FILTER_NOTELTSET
- ERROR_EVT_FILTER_INVARG
- ERROR_EVT_FILTER_INVTEST
- ERROR_EVT_FILTER_INVTYPE
- ERROR_EVT_FILTER_PARSEERR
- ERROR_EVT_FILTER_UNSUPPORTEDOP
- ERROR_EVT_FILTER_UNEXPECTEDTOKEN
- ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL
- ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE
- ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE
- ERROR_EVT_CHANNEL_CANNOT_ACTIVATE
- ERROR_EVT_FILTER_TOO_COMPLEX
- ERROR_EVT_MESSAGE_NOT_FOUND
- ERROR_EVT_MESSAGE_ID_NOT_FOUND
- ERROR_EVT_UNRESOLVED_VALUE_INSERT
- ERROR_EVT_UNRESOLVED_PARAMETER_INSERT
- ERROR_EVT_MAX_INSERTS_REACHED
- ERROR_EVT_EVENT_DEFINITION_NOT_FOUND
- ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND
- ERROR_EVT_VERSION_TOO_OLD
- ERROR_EVT_VERSION_TOO_NEW
- ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY
- ERROR_EVT_PUBLISHER_DISABLED
- ERROR_EVT_FILTER_OUT_OF_RANGE
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa5443d98c53d6abedbe3a0027e8e2e524ae9df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965529"
---
# <a name="windows-event-log-error-constants"></a>Windows 事件記錄檔錯誤常數

以下是 Windows 事件記錄檔所定義的錯誤碼。

<dl> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**錯誤 \_ .EVT \_ 不正確 \_ 通道 \_ 路徑**
</dt> <dd> <dl> <dt>

15000
</dt> <dt>



指定的通道路徑無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**錯誤 \_ .EVT \_ 不正確 \_ 查詢**
</dt> <dd> <dl> <dt>

15001
</dt> <dt>



指定的查詢無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**\_ \_ \_ \_ 找不到簽發者中繼資料 \_ 的錯誤**
</dt> <dd> <dl> <dt>

15002
</dt> <dt>



在資源中找不到提供者中繼資料。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤 .EVT 事件範本**
</dt> <dd> <dl> <dt>

15003
</dt> <dt>



資源中找不到事件定義的範本。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**錯誤 \_ .EVT \_ 不正確 \_ 發行者 \_ 名稱**
</dt> <dd> <dl> <dt>

15004
</dt> <dt>



指定的提供者名稱無效。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**錯誤 \_ .EVT \_ 不正確 \_ 事件 \_ 資料**
</dt> <dd> <dl> <dt>

15005
</dt> <dt>



提供者所引發的事件資料與提供者資訊清單中的事件範本定義不相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 .EVT 頻道**
</dt> <dd> <dl> <dt>

15007
</dt> <dt>



找不到指定的通道。 檢查通道設定。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**錯誤 \_ .EVT \_ 格式不正確的 \_ XML \_ 文字**
</dt> <dd> <dl> <dt>

15008
</dt> <dt>



指定的 XML 文字格式不正確。 如需詳細資訊，請呼叫 [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) 函數。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**\_ \_ \_ 對 \_ 直接 \_ 通道的錯誤 .EVT 訂用帳戶**
</dt> <dd> <dl> <dt>

15009
</dt> <dt>



您無法訂閱分析或 Debug 通道;分析或 Debug 通道的事件會直接移至記錄檔，而且無法訂閱。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**錯誤 \_ .EVT \_ 設定 \_ 錯誤**
</dt> <dd> <dl> <dt>

15010
</dt> <dt>



發生設定錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**錯誤 \_ .EVT \_ 查詢 \_ 結果 \_ 過時**
</dt> <dd> <dl> <dt>

15011
</dt> <dt>



查詢結果無效。 這可能是因為在建立查詢結果之後清除或變換記錄所致。 釋放查詢結果物件並重新發出查詢。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**錯誤 \_ .EVT \_ 查詢 \_ 結果 \_ 不正確 \_ 位置**
</dt> <dd> <dl> <dt>

15012
</dt> <dt>



查詢結果的游標未指向有效的位置。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**錯誤 \_ .EVT \_ 非 \_ 驗證 \_ MSXML**
</dt> <dd> <dl> <dt>

15013
</dt> <dt>



註冊的 MSXML 剖析器不支援驗證。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**錯誤 \_ .EVT \_ 篩選 \_ ALREADYSCOPED**
</dt> <dd> <dl> <dt>

15014
</dt> <dt>



只有當運算式評估為節點集，且不屬於範圍作業的一些其他變更時，運算式才可以接著變更範圍作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**錯誤 \_ .EVT \_ 篩選 \_ NOTELTSET**
</dt> <dd> <dl> <dt>

15015
</dt> <dt>



無法從不代表元素集的詞彙執行步驟運算。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**錯誤 \_ .EVT \_ 篩選 \_ INVARG**
</dt> <dd> <dl> <dt>

15016
</dt> <dt>



二元運算子左邊的引數必須是屬性、節點或變數，且右邊的引數必須是常數。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**錯誤 \_ .EVT \_ 篩選 \_ INVTEST**
</dt> <dd> <dl> <dt>

15017
</dt> <dt>



步驟作業必須牽涉到節點測試，或者，若為述詞，則可評估上一個節點集合所識別之節點集內每個節點的代數運算式。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**錯誤 \_ .EVT \_ 篩選 \_ INVTYPE .。。**
</dt> <dd> <dl> <dt>

15018
</dt> <dt>



不支援此資料類型。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**錯誤 \_ .EVT \_ 篩選 \_ PARSEERR**
</dt> <dd> <dl> <dt>

15019
</dt> <dt>



在指定的位置發生語法錯誤。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**錯誤 \_ .EVT \_ 篩選 \_ UNSUPPORTEDOP**
</dt> <dd> <dl> <dt>

15020
</dt> <dt>



此篩選準則的執行不支援這個運算子。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**錯誤 \_ .EVT \_ 篩選 \_ UNEXPECTEDTOKEN**
</dt> <dd> <dl> <dt>

15021
</dt> <dt>



發現未預期的權杖。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**錯誤 \_ .EVT \_ \_ 啟用的 \_ \_ \_ 直接 \_ 通道上有不正確操作**
</dt> <dd> <dl> <dt>

15022
</dt> <dt>



無法在已啟用的分析或偵測通道上執行要求的作業。 您必須先停用通道，才能執行要求的作業。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**錯誤 \_ .EVT \_ 不正確 \_ 通道 \_ 屬性 \_ 值**
</dt> <dd> <dl> <dt>

15023
</dt> <dt>



通道屬性包含不正確值。 值的類型可能無效、值可能超出範圍，或無法更新此類型的通道或不支援的值。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**錯誤 \_ .EVT \_ 不正確 \_ 發行者 \_ 屬性 \_ 值**
</dt> <dd> <dl> <dt>

15024
</dt> <dt>



Provider 屬性包含不正確值。 值的類型可能無效、值可能超出範圍，或無法更新此值或不支援此類型的提供者。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**錯誤 \_ .EVT \_ 通道 \_ 無法 \_ 啟動**
</dt> <dd> <dl> <dt>

15025
</dt> <dt>



通道無法啟動。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**錯誤 \_ .EVT \_ 篩選 \_ 太 \_ 複雜**
</dt> <dd> <dl> <dt>

15026
</dt> <dt>



XPath 運算式超過支援的複雜度。 簡化運算式或將其分割成兩個或多個簡單運算式。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**\_ \_ \_ \_ 找不到錯誤 .EVT 訊息**
</dt> <dd> <dl> <dt>

15027
</dt> <dt>



訊息資源存在，但在字串或訊息資料表中找不到訊息。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤 .EVT 訊息識別碼**
</dt> <dd> <dl> <dt>

15028
</dt> <dt>



找不到訊息識別碼。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**錯誤 \_ .EVT \_ 無法解析的 \_ 值 \_ 插入**
</dt> <dd> <dl> <dt>

15029
</dt> <dt>



找不到插入索引的替代字串。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**錯誤 \_ .EVT \_ 無法解析的 \_ 參數 \_ 插入**
</dt> <dd> <dl> <dt>

15030
</dt> <dt>



找不到參數參考 (% 1) 的描述字串。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**已 \_ 達到錯誤的 .EVT \_ 最大 \_ 插入 \_ 數**
</dt> <dd> <dl> <dt>

15031
</dt> <dt>



已達到最大取代數目。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤 .EVT 事件定義**
</dt> <dd> <dl> <dt>

15032
</dt> <dt>



找不到事件識別碼的事件定義。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**\_ \_ \_ \_ \_ 找不到錯誤 .EVT 訊息地區設定**
</dt> <dd> <dl> <dt>

15033
</dt> <dt>



所需訊息的地區設定特定資源不存在。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**錯誤的 \_ .EVT \_ 版本 \_ 太 \_ 舊**
</dt> <dd> <dl> <dt>

15034
</dt> <dt>



資源太舊而無法相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**錯誤 \_ .EVT \_ 版本 \_ 太 \_ 新**
</dt> <dd> <dl> <dt>

15035
</dt> <dt>



資源太新，無法相容。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**錯誤 \_ .EVT \_ 無法 \_ 開啟 \_ \_ 查詢通道 \_**
</dt> <dd> <dl> <dt>

15036
</dt> <dt>



無法開啟位於指定之查詢索引的通道。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**錯誤的 \_ .EVT \_ 發行者 \_ 已停用**
</dt> <dd> <dl> <dt>

15037
</dt> <dt>



提供者已停用，且其資源無法使用。 卸載或升級提供者時，就會發生這種情況。


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**錯誤 \_ .EVT \_ 篩選 \_ 超出 \_ \_ 範圍**
</dt> <dd> <dl> <dt>

15038
</dt> <dt>



嘗試建立的數數值型別超出其有效範圍。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Winerror.h。h</dt> </dl> |



 

 





