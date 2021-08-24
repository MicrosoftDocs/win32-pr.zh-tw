---
description: CIM \_ 錯誤類別包含 cim 作業失敗的相關資訊。
ms.assetid: 35acecbd-b972-45b4-9616-2047bba8fd41
title: CIM_Error 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Error
- CIM_Error.ErrorType
- CIM_Error.OtherErrorType
- CIM_Error.OwningEntity
- CIM_Error.MessageID
- CIM_Error.Message
- CIM_Error.MessageArguments
- CIM_Error.PerceivedSeverity
- CIM_Error.ProbableCause
- CIM_Error.ProbableCauseDescription
- CIM_Error.RecommendedActions
- CIM_Error.ErrorSource
- CIM_Error.ErrorSourceFormat
- CIM_Error.OtherErrorSourceFormat
- CIM_Error.CIMStatusCode
- CIM_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1c7e7fba10cb507e1288344637c944bb56d62dc4c9eaaf909a980ceaf3250440
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695968"
---
# <a name="cim_error-class"></a>CIM \_ 錯誤類別

**Cim \_ 錯誤** 類別包含 cim 作業失敗的相關資訊。

## <a name="syntax"></a>語法

``` syntax
[Indication, Abstract, Version("2.22.1"), Exception, UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_Error
{
  uint16 ErrorType;
  string OtherErrorType;
  string OwningEntity;
  string MessageID;
  string Message;
  string MessageArguments[];
  uint16 PerceivedSeverity;
  uint16 ProbableCause;
  string ProbableCauseDescription;
  string RecommendedActions[];
  string ErrorSource;
  uint16 ErrorSourceFormat = 0;
  string OtherErrorSourceFormat;
  uint32 CIMStatusCode;
  string CIMStatusCodeDescription;
};
```

## <a name="members"></a>成員

**CIM \_ 錯誤** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ 錯誤** 類別具有這些屬性。

<dl> <dt>

**CIMStatusCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "DSP0201。DMTF \| 錯誤。代碼 \| 2.3 "，" DSP0200。DMTF \| CIMError \| 1.3 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ 錯誤**。**CIMStatusCodeDescription**") 
</dt> </dl>

此實例的特性的 CIM 狀態碼。 這個屬性會定義 CIM 伺服器或接聽程式可以傳回的狀態碼。

<dt>

<span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>

<span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>**CIM \_錯誤 \_ 失敗** (1) 


</dt> <dd>

發生的一般錯誤未涵蓋于更明確的錯誤碼。

</dd> <dt>

<span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>

<span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>**CIM \_錯誤 \_ \_ 拒絕存取** (2) 


</dt> <dd>

用戶端無法使用 CIM 資源的存取權。

</dd> <dt>

<span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>

<span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>**CIM \_錯誤 \_ 不正確 \_ 命名空間** (3) 


</dt> <dd>

目標命名空間不存在。

</dd> <dt>

<span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>

<span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>**CIM \_錯誤 \_ 不正確 \_ 參數** (4) 


</dt> <dd>

傳遞給方法的一或多個參數值無效。

</dd> <dt>

<span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>

<span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>**CIM \_錯誤 \_ 不正確 \_ 類別** (5) 


</dt> <dd>

指定的類別不存在。

</dd> <dt>

<span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>

<span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>**CIM \_ (6) \_ \_ 找不到錯誤**


</dt> <dd>

找不到要求的物件。

</dd> <dt>

<span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>

<span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>**CIM \_ (7) \_ 不 \_ 支援的錯誤**


</dt> <dd>

不支援要求的作業。

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>

<span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>**CIM \_ERR \_ 類別 \_ 具有 \_ 子** 系 (8) 


</dt> <dd>

無法在這個類別上執行操作，因為它有實例。

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>

<span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>**CIM \_ERR \_ 類別 \_ 具有 \_ 實例** (9) 


</dt> <dd>

無法在這個類別上執行操作，因為它有實例。

</dd> <dt>

<span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>

<span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>**CIM \_錯誤 \_ 不正確 \_ 超類** (10) 


</dt> <dd>

因為指定的超類別不存在，所以無法執行操作。

</dd> <dt>

<span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>

<span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>**CIM \_錯誤 \_ 已經 \_ 存在** (11) 


</dt> <dd>

無法執行操作，因為物件已經存在。

</dd> <dt>

<span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>

<span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>**CIM \_錯誤 (12) 不會有 \_ \_ 此 \_ 屬性**


</dt> <dd>

指定的屬性不存在。

</dd> <dt>

<span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>

<span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>**CIM \_錯誤 \_ 類型 \_ 不符** (13) 


</dt> <dd>

提供的值與類型不相容。

</dd> <dt>

<span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>

<span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>**CIM \_\_ \_ \_ 不 \_ 支援** (14) 的 ERR 查詢語言


</dt> <dd>

無法辨識或支援查詢語言。

</dd> <dt>

<span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>

<span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>**CIM \_錯誤 \_ 不正確 \_ 查詢** (15) 


</dt> <dd>

查詢對指定的查詢語言無效。

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>

<span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>**CIM \_ (16) \_ \_ 無法 \_ 使用 ERR 方法**


</dt> <dd>

無法執行外部方法。

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>

<span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>**CIM \_\_ \_ \_ 找不到** (17) 的 ERR 方法


</dt> <dd>

指定的外部方法不存在。

</dd> <dt>

<span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>

<span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>**CIM \_錯誤的非 \_ 預期 \_ 回應** (18) 


</dt> <dd>

對非同步作業所傳回的回應不是預期的。

</dd> <dt>

<span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>

<span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>**CIM \_錯誤 \_ 不正確 \_ 回應 \_ 目的地** (19) 


</dt> <dd>

非同步回應的指定目的地無效。

</dd> <dt>

<span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>

<span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>**CIM \_錯誤 \_ 命名空間 \_ 不是 \_ 空** 的 (20) 


</dt> <dd>

指定的命名空間不是空的。

</dd> <dt>

<span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>

<span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>**CIM \_錯誤 \_ 不正確 \_ 列舉 \_ 內容** (21) 


</dt> <dd>

提供的列舉內容無效。

</dd> <dt>

<span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>

<span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>**CIM \_錯誤 \_ 無效 \_ \_** 的作業超時 (22) 


</dt> <dd>

指定的命名空間不是空的。

</dd> <dt>

<span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>

<span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>**CIM \_\_ \_ \_ 已 \_ 放棄 (23) 的錯誤提取**


</dt> <dd>

指定的命名空間不是空的。

</dd> <dt>

<span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>

<span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>**CIM \_\_ \_ 無法 \_ \_ 放棄** (24) 的錯誤提取


</dt> <dd>

嘗試放棄提取作業失敗。

</dd> <dt>

<span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>

<span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>**CIM \_ (25) \_ \_ \_ 不 \_ 支援錯誤篩選的列舉**


</dt> <dd>

不支援篩選的 Enumeratrions。

</dd> <dt>

<span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>

<span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>**CIM \_\_ \_ \_ 錯誤 \_ 不 \_ 支援錯誤接續** (26) 


</dt> <dd>

不支援發生錯誤時仍繼續。

</dd> <dt>

<span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>

<span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>**CIM \_ (27) \_ \_ \_ 超過 ERR 伺服器限制**


</dt> <dd>

已超過 WBEM 伺服器限制 (例如記憶體、連線 ... ) 。

</dd> <dt>

<span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>

<span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>**CIM \_ERR \_ 伺服器 \_ 正在 \_ 關閉 \_** (28) 


</dt> <dd>

WBEM 伺服器正在關閉。

</dd> <dt>

<span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>

<span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>**CIM \_\_ \_ \_ 不 \_ 支援** (29) 的 ERR 查詢功能


</dt> <dd>

不支援指定的查詢功能。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**CIMStatusCodeDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "DSP0201。DMTF \| 錯誤。描述 \| 2.3 "，" DSP0200。DMTF \| CIMError \| 1.3 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ 錯誤**。**CIMStatusCode**") 
</dt> </dl>

自由格式的字串，其中包含人類可讀取的 **CIMStatusCode** 屬性值描述。

> [!Note]  
> 這項描述可能會延伸，但必須與 **CIMStatusCode** 的定義一致。

 

</dd> <dt>

**ErrorSource**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 錯誤**」。**ErrorSourceFormat**") 
</dt> </dl>

識別產生錯誤之實體的資訊。 如果實體是由 CIM 架構模型化，則這個屬性會包含編碼為字串參數之實例的路徑。 否則，屬性會包含一個字串，該字串會為產生錯誤的實體命名。 這個屬性的格式是由 **ErrorSourceFormat** 屬性所指定。

</dd> <dt>

**ErrorSourceFormat**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 錯誤**」。**ErrorSource**"，"**CIM \_ 錯誤**。**OtherErrorSourceFormat**") 
</dt> </dl>

**ErrorSource** 屬性的格式。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd>

CIM 用戶端應用程式可解譯的格式不明或不具意義。

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd>

格式是由 **OtherErrorSourceFormat** 屬性的值所定義。

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2) 


</dt> <dd>

Cim 基礎結構規格中定義的 CIM 物件路徑。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 錯誤**」。**OtherErrorType**") 
</dt> </dl>

主要錯誤類型。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>

<span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>**通訊錯誤** (2) 


</dt> <dd>

此類型的錯誤主要與將資訊從某個點傳送到另一個點所需的程式和/或程式相關聯。

</dd> <dt>

<span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>

<span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>**服務品質錯誤** (3) 


</dt> <dd>

這種類型的錯誤主要與導致功能或效能降低的失敗有關。

</dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**軟體錯誤** (4) 


</dt> <dd>

此類型的錯誤主要與軟體或處理錯誤相關。

</dd> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**硬體錯誤** (5) 


</dt> <dd>

此類型的錯誤主要與設備或硬體故障相關聯。

</dd> <dt>

<span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>

<span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>**環境錯誤** (6) 


</dt> <dd>

其他環境考慮。

</dd> <dt>

<span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>

<span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>**安全性錯誤** (7) 


</dt> <dd>

此類型的錯誤與安全性違規、病毒偵測和類似問題相關聯。

</dd> <dt>

<span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>

<span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>**過度訂閱錯誤** (8) 


</dt> <dd>

此類型的錯誤主要與失敗相關，無法配置足夠的資源來完成作業。

</dd> <dt>

<span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>

<span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>**無法使用資源錯誤** (9) 


</dt> <dd>

此類型的錯誤主要與無法存取所需資源的相關聯。

</dd> <dt>

<span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>

<span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span> (10) **不支援** 的作業錯誤


</dt> <dd>

此類型的錯誤主要與不支援的要求相關聯。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**訊息**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 錯誤**」。**MessageID**"，"**CIM \_ 錯誤**。**MessageArguments**") 
</dt> </dl>

格式化的訊息。

> [!Note]  
> 這則訊息是藉由將 **MessageArguments** 屬性的動態元素與 **MessageID** 屬性的靜態元素結合，然後將它們新增至與 **OwningEntity** 相關聯的訊息登錄或目錄來建立。

 

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 錯誤**」。**MessageID**"，"**CIM \_ 錯誤**。**訊息**「) 
</dt> </dl>

陣列，其中包含訊息的動態內容。

</dd> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ Error**.**Message**"，"**CIM \_ 錯誤**。**MessageArguments**") 
</dt> </dl>

在 OwningEntity 範圍內唯一識別的不透明字串，這是訊息的格式。

</dd> <dt>

**OtherErrorSourceFormat**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 錯誤**」。**ErrorSourceFormat**") 
</dt> </dl>

當 **ErrorSourceFormat** 設定為 "1" (其他) 時，定義 **ErrorSourceFormat** 值的字串。

</dd> <dt>

**OtherErrorType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 錯誤**」。**ErrorType**") 
</dt> </dl>

描述 **ErrorType** 值的自由格式字串，其設定為 "1" (其他) 。

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

擁有此實例所描述的訊息格式之實體的唯一識別碼。

> [!Note]  
> 這個屬性必須包含受著作權、商標或唯一的名稱，該名稱是由定義訊息格式的商務實體或標準主體所擁有。

 

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。察覺嚴重性」 ) 
</dt> </dl>

從傳送錯誤訊息之元素的觀點來看，錯誤嚴重性的描述。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd>

已知的指示嚴重性不明或不定。

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd>

表示可以在 **OtherSeverity** 屬性中找到嚴重性的值。

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**資訊** (2) 


</dt> <dd>

提供資訊性回應時應使用資訊。

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**降級/警告** (3) 


</dt> <dd>

如果適合讓使用者決定是否需要採取動作，則應該使用。

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**次要** (4) 


</dt> <dd>

需要採取動作，但這次的情況並不嚴重。

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**主要** (5) 


</dt> <dd>

現在需要採取動作。

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (6) 


</dt> <dd>

現在需要採取動作，而範圍很廣泛 (可能會導致重要資源的即將中斷) 。

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**嚴重/** 無法恢復 (7) 


</dt> <dd>

發生錯誤，但太晚採取補救動作。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ProbableCause**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。可能的原因 "，" \| M3100. probableCause "，" itu-IANA-鬧鐘-TC ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ 錯誤**。**ProbableCauseDescription**") 
</dt> </dl>

錯誤可能原因的描述。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

**介面卡/卡片錯誤** (2) 


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

**應用程式子系統失敗** (3) 


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

**頻寬減少** (4) 


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

**連接建立錯誤** (5) 


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

**通訊協定錯誤** (6) 


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

**通訊子系統失敗** (7) 


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

設定 **/自訂錯誤** (8) 


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

**擁塞** (9) 


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

**已** 損毀的資料 (10) 


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

**CPU 週期限制超過** (11) 


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

**資料集/數據機錯誤** (12) 


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

**降級的信號** (13) 


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

**DTE-DCE 介面錯誤** (14) 


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

**主機殼門開啟** (15) 


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

**設備故障** (16) 


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

**過度震動** (17) 


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

**檔案格式錯誤** (18) 


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

**引發偵測到** (19) 


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

偵測 **到大量** (20) 


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

**框架錯誤** (21) 


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

**HVAC 問題** (22) 


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

不 **接受濕度** (23) 


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

**I/o 裝置錯誤** (24) 


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

**輸入裝置錯誤** (25) 


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

**區域網路錯誤** (26) 


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

偵測 **到未有毒的** 流失 (27) 


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

**本機節點傳輸錯誤** (28) 


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

**遺失框架** (29) 


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

 (30) **的信號遺失**


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

**物料供應已用盡** (31) 


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

多工器 **問題** (32) 


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

**記憶體不足** (33) 


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

**輸出裝置錯誤** (34) 


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

**效能降低** (35) 


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

**電源問題** (36) 


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

**不可接受的壓力** (37) 


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

**處理器問題 (內部電腦錯誤)** (38) 


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

提取 **失敗** (39) 


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

**佇列大小超過** (40) 


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

**接收失敗** (41) 


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

**接收者失敗** (42) 


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

**遠端節點傳輸錯誤** (43) 


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

**資源或接近容量** (44) 


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

**回應時間過度** (45) 


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

重新 **傳輸速率過高** (46) 


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

**軟體錯誤** (47) 


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

**軟體程式異常終止** (48) 


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

**軟體程式錯誤 (不正確的結果)** (49) 


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

**儲存體容量問題** (50) 


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

無法 **接受的溫度** (51) 


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

**超過** (52) 的閾值


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

**計時問題** (53) 


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

偵測 **到有毒** 流失 (54) 


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

**傳輸失敗** (55) 


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

**發送器失敗** (56) 


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

**基礎資源無法使用** (57) 


</dt> <dd></dd> <dt>

<span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

**版本不相符** (58) 


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

**先前的警示已清除** (59) 


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

**登入嘗試失敗** (60) 


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

偵測 **到的軟體病毒** (61) 


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

**硬體安全性違反** 了 (62) 


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

偵測 **到拒絕服務** (63) 


</dt> <dd></dd> <dt>

<span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

**安全性認證不符** (64) 


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

**未經授權的存取** (65) 


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

**已收到** (66) 的鬧鐘


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

**遺失指標** (67) 


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

承載 **不符** (68) 


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

**傳輸錯誤** (69) 


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

**過多錯誤率** (70) 


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

**追蹤問題** (71) 


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

**元素無法使用** (72) 


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

**遺漏的元素** (73) 


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

**遺失多框架** (74) 


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

**廣播通道失敗** (75) 


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

**收到的訊息無效** (76) 


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

**路由失敗** (77) 


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

**背板失敗** (78) 


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

**識別碼重複** (79) 


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

**保護路徑失敗** (80) 


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

**同步遺失或** (81) 不相符


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

**終端機問題** (82) 


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

**系統時鐘失敗** (83) 


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

**天線失敗** (84) 


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

**電池充電失敗** (85) 


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

**磁片失敗** (86) 


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

**頻率跳動失敗** (87) 


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

**遺失冗余** (88) 


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

**電源供應器失敗** (89) 


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

**信號品質問題** (90) 


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

**電池放電** (91) 


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

**電池故障** (92) 


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

**商業電源問題** (93) 


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

**風扇故障** (94) 


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

**引擎失敗** (95) 


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

**感應器失敗** (96) 


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

**保險絲故障** (97) 


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

產生器 **失敗** (98) 


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

**電力偏低** (99) 


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

**低燃料** (100) 


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

**低水位** (101) 


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

**爆炸性天然氣** (102) 


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

**高接近尾聲** (103) 


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

**Ice 堆積** (104) 


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

**冒煙** (105) 


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

**記憶體不符** (106) 


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

**CPU 週期** (107) 


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

**軟體環境問題** (108) 


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

**軟體下載失敗** (109) 


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

**元素重新初始化** (110) 


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

**Timeout** (111) 


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

**記錄問題** (112) 


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

偵測到 (113) 的 **洩漏**


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

**保護機制失敗** (114) 


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

**保護資源失敗** (115) 


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

**資料庫不一致** (116) 


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

**驗證失敗** (117) 


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

 (118) **的機密性缺口**


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

**纜線防** (119) 


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

**延遲的資訊** (120) 


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

**重複的資訊** (121) 


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

**遺漏** (122) 的資訊


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

 (123) 的 **資訊修改**


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

**順序中的資訊** (124) 


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

**金鑰已過期** (125) 


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

**不可否認性失敗** (126) 


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

下班 **時間活動** (127) 


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

**服務** (128) 


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

程式 **錯誤** (129) 


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

未 **預期的資訊** (130) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ProbableCauseDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 錯誤**」。**ProbableCause**") 
</dt> </dl>

描述錯誤可能原因的自由格式字串（當 **ProbableCause** 屬性設定為 "1" (其他) 時）。

</dd> <dt>

**RecommendedActions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

自由格式字串的陣列，描述解決錯誤所採取的建議動作。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

