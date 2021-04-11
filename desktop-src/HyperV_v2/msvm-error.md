---
description: 包含嚴重性、原因、建議動作，以及與 CIM 作業失敗相關之其他資料的相關資訊。
ms.assetid: 128B9ECE-D26C-4A7D-BFB7-69CD986B0DBA
title: Msvm_Error 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Error
- Msvm_Error.ErrorType
- Msvm_Error.OtherErrorType
- Msvm_Error.OwningEntity
- Msvm_Error.MessageID
- Msvm_Error.Message
- Msvm_Error.MessageArguments
- Msvm_Error.PerceivedSeverity
- Msvm_Error.ProbableCause
- Msvm_Error.ProbableCauseDescription
- Msvm_Error.RecommendedActions
- Msvm_Error.ErrorSource
- Msvm_Error.ErrorSourceFormat
- Msvm_Error.OtherErrorSourceFormat
- Msvm_Error.CIMStatusCode
- Msvm_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56b3b30f1d64146db2554d097b11104df09ba018
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026817"
---
# <a name="msvm_error-class"></a>Msvm \_ Error 類別

特製化類別，其中包含有關「嚴重性」、「原因」、「建議的動作」和「CIM」作業失敗的其他資料的相關資訊。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Error : CIM_Error
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

**Msvm \_ Error** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ 錯誤** 類別具有這些屬性。

<dl> <dt>

**CIMStatusCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此實例的特性的 CIM 狀態碼。 這個屬性會定義符合的 CIM 伺服器或接聽程式可能傳回的狀態碼。 並非所有狀態碼都對每項作業都有效。 每項作業的規格都應該定義該作業可能傳回的狀態碼。 系統會定義 CIM 狀態碼的下列值。 這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。



| 值                                                                                                                                                                                                                                                                                          | 意義                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span><dl> <dt>**CIM \_錯誤 \_ 失敗**</dt> <dt>1</dt> </dl>                                                                       | 發生的一般錯誤未涵蓋于更明確的錯誤碼。<br/>    |
| <span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span><dl> <dt>**CIM \_錯誤 \_ \_ 拒絕存取**</dt> <dt>2</dt> </dl>                                                 | 用戶端無法使用 CIM 資源的存取權。<br/>                      |
| <span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span><dl> <dt>**CIM \_錯誤 \_ 不正確 \_ 命名空間**</dt> <dt>3</dt> </dl>                                     | 目標命名空間不存在。<br/>                                           |
| <span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span><dl> <dt>**CIM \_錯誤 \_ 不正確 \_ 參數**</dt> <dt>4</dt> </dl>                                     | 傳遞給方法的一或多個參數值無效。<br/>                |
| <span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span><dl> <dt>**CIM \_錯誤 \_ \_ 類別**</dt> <dt>5</dt>無效 </dl>                                                 | 指定的類別不存在。<br/>                                            |
| <span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span><dl> <dt>**CIM \_\_找不 \_ 到錯誤**</dt> <dt>6</dt> </dl>                                                             | 找不到要求的物件。<br/>                                       |
| <span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span><dl> <dt>**CIM \_錯誤 \_ 不 \_ 支援**</dt> <dt>7</dt> </dl>                                                 | 不支援要求的作業。<br/>                                      |
| <span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span><dl> <dt>**CIM \_ERR \_ 類別 \_ 有 \_ 子**</dt>系 <dt>8</dt> </dl>                                 | 無法在這個類別上執行操作，因為它有實例。<br/>        |
| <span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span><dl> <dt>**CIM \_ERR \_ 類別 \_ 具有 \_ 實例**</dt> <dt>9</dt> </dl>                              | 無法在這個類別上執行操作，因為它有實例。<br/>          |
| <span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span><dl> <dt>**CIM \_錯誤 \_ 不正確 \_ 超類別**</dt> <dt>10</dt> </dl>                                 | 因為指定的超類別不存在，所以無法執行操作。<br/> |
| <span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span><dl> <dt>**CIM \_錯誤 \_ 已經 \_ 存在**</dt> <dt>11</dt> </dl>                                             | 無法執行操作，因為物件已經存在。<br/>              |
| <span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span><dl> <dt>**CIM \_錯誤 \_ 沒有 \_ 這類的 \_ 屬性**</dt> <dt>12</dt> </dl>                                      | 指定的屬性不存在。<br/>                                         |
| <span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span><dl> <dt>**CIM \_錯誤 \_ 類型 \_ 不符**</dt> <dt>13</dt> </dl>                                                | 提供的值與類型不相容。<br/>                              |
| <span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span><dl> <dt>**CIM \_\_ \_ \_ 不 \_ 支援的 ERR 查詢語言**</dt> <dt>14</dt> </dl> | 無法辨識或支援查詢語言。<br/>                             |
| <span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span><dl> <dt>**CIM \_錯誤 \_ 不正確 \_ 查詢**</dt> <dt>15</dt> </dl>                                                | 查詢對指定的查詢語言無效。<br/>                       |
| <span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span><dl> <dt>**CIM \_ERR \_ 方法 \_ 不可 \_ 用**</dt> <dt>16</dt> </dl>                          | 無法執行外部方法。<br/>                                    |
| <span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span><dl> <dt>**CIM \_\_ \_ \_ 找不到錯誤的方法**</dt> <dt>17</dt> </dl>                                      | 指定的外部方法不存在。<br/>                                 |
| <span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span><dl> <dt>**CIM \_錯誤的未 \_ 預期 \_ 回應**</dt> <dt>18</dt> </dl>                              | 對非同步作業所傳回的回應不是預期的。<br/>          |
| <span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span><dl> <dt>**CIM \_錯誤 \_ 不正確 \_ 回應 \_ 目的地**</dt> <dt>19</dt> </dl>  | 非同步回應的指定目的地無效。<br/>          |
| <span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span><dl> <dt>**CIM \_ERR \_ 命名空間 \_ 不是 \_ 空**</dt>的 <dt>20</dt> </dl>                             | 指定的命名空間不是空的。<br/>                                          |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <dt>已 **保留 DMTF**</dt><dt>21 =*值*</dt> </dl>                            | 保留值。<br/>                                                               |



 

</dd> <dt>

**CIMStatusCodeDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

字串，包含使用者可讀取的 **CIMStatusCode** 屬性描述。 這項描述可延伸，但必須與 **CIMStatusCode** 定義一致。 這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。

</dd> <dt>

**ErrorSource**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

 (實例) 產生錯誤之實體的識別資訊。 如果此實體在 CIM 架構中建立模型，這個屬性會包含編碼為字串參數之實例的路徑。 如果未建立模型，屬性會包含一些識別字串來為產生錯誤的實體命名。 路徑或識別字串會根據 **ErrorSourceFormat** 屬性格式化。 這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。

</dd> <dt>

**ErrorSourceFormat**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**ErrorSource** 屬性的格式會根據此屬性的值可解譯。 這個屬性是從 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))繼承而來，而且一律設定為0。



| 值                                                                                                                                                                                                                                                        | 意義                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**未知**</dt>的 <dt>0</dt> </dl>                                  | CIM 用戶端應用程式可解譯的格式不明或不具意義。<br/>                                         |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**其他**</dt> <dt>1</dt> </dl>                                          | 格式是由 **OtherErrorSourceFormat** 屬性的值所定義。<br/>                                               |
| <span id="CIMObjectHandle"></span><span id="cimobjecthandle"></span><span id="CIMOBJECTHANDLE"></span><dl> <dt>**CIMObjectHandle**</dt> <dt>2</dt> </dl> | 使用針對 objectHandle 非終端機定義之 MOF 語法編碼的 CIM 物件控制碼，會用來識別實體。<br/> |



 

</dd> <dt>

**ErrorType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

錯誤的主要分類。 以下是定義的值。 這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。



| 值                                                                                                                                                                                                                                                                                                         | 意義                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**未知**</dt>的 <dt>0</dt> </dl>                                                                                   |                                                                                                                                                          |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**其他**</dt> <dt>1</dt> </dl>                                                                                           |                                                                                                                                                          |
| <span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span><dl> <dt>**通訊錯誤**</dt> <dt>2</dt> </dl>                               | 此類型的錯誤主要與將資訊從某個點傳送到另一個點所需的程式和/或程式相關聯。<br/> |
| <span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span><dl> <dt>**服務品質錯誤**</dt> <dt>3</dt> </dl>               | 這種類型的錯誤主要與導致功能或效能降低的失敗有關。<br/>                             |
| <span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span><dl> <dt>**軟體錯誤**</dt> <dt>4</dt> </dl>                                                       | 此類型的錯誤主要與軟體或處理錯誤相關。<br/>                                                            |
| <span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span><dl> <dt>**硬體錯誤**</dt> <dt>5</dt> </dl>                                                       | 此類型的錯誤主要與設備或硬體故障相關聯。<br/>                                                         |
| <span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span><dl> <dt>**環境錯誤**</dt> <dt>6</dt> </dl>                                   | 此類型的錯誤主要與設備相關的失敗狀況或其他環境考慮相關。<br/>      |
| <span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span><dl> <dt>**安全性錯誤**</dt> <dt>7</dt> </dl>                                                       | 此類型的錯誤與安全性違規、病毒偵測和類似問題相關聯。<br/>                                        |
| <span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span><dl> <dt>**過度訂閱錯誤**</dt> <dt>8</dt> </dl>                       | 此類型的錯誤主要與失敗相關，無法配置足夠的資源來完成作業。<br/>                   |
| <span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span><dl> <dt>**無法使用的資源錯誤**</dt> <dt>9</dt> </dl>       | 此類型的錯誤主要與無法存取所需資源的相關聯。<br/>                                                |
| <span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span><dl> <dt>**不支援的操作錯誤**</dt> <dt>10</dt> </dl> | 此類型的錯誤主要與不支援的要求相關聯。<br/>                                                          |



 

</dd> <dt>

**訊息**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

格式化的訊息。 此訊息的建立方式是將訊息的動態內容（如 **MessageArguments** 所述）套用至 **OwningEntity** 範圍內唯一識別的格式字串（藉由 **MessageID**）。 這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

陣列，其中包含訊息的動態內容。 這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。

</dd> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在 **OwningEntity** 範圍內唯一識別的不透明字串，這是訊息的格式。 這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。

</dd> <dt>

**OtherErrorSourceFormat**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

為 **ErrorSourceFormat** 定義「其他」值的字串。 當 **ErrorSourceFormat** 設定為 1 (其他) 的值時，此值必須設定為非 Null 值。 對於 **ErrorSourceFormat** 的所有其他值，此字串的值必須設定為 **Null**。 這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。

</dd> <dt>

**OtherErrorType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述當1， (其他) 指定為 **ErrorType** 時，描述 **ErrorType** 的字串。 這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

唯一識別實體的字串，該實體擁有此實例中所描述之訊息格式的定義。 **OwningEntity** 必須包含由商務實體或定義格式的標準內容所擁有的受著作權、商標或其他唯一名稱。 這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

列舉值，描述來自通知者觀點之錯誤的嚴重性： 2-低應用於非嚴重問題，例如不正確參數、不正確的使用方式、不支援的功能。 應該使用 3-Medium 來指出需要採取動作，但目前的情況並不嚴重。 4-High 應該用來指出現在需要採取動作。 5-嚴重應用來指出資料遺失或無法復原的系統或服務失敗。 這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**低** (2) 
</dt> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**中型** (3) 
</dt> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**高** (4) 
</dt> <dt>

<span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>**嚴重** (5 ) 
</dt> </dl>

</dd> <dt>

**ProbableCause**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述錯誤可能原因的列舉值。 這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**介面卡/卡片錯誤** (2) 
</dt> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**應用程式子系統失敗** (3) 
</dt> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**頻寬減少** (4) 
</dt> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**連接建立錯誤** (5) 
</dt> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**通訊協定錯誤** (6) 
</dt> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**通訊子系統失敗** (7) 
</dt> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>設定 **/自訂錯誤** (8) 
</dt> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**擁塞** (9) 
</dt> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>**已** 損毀的資料 (10) 
</dt> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>**CPU 週期限制超過** (11) 
</dt> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**資料集/數據機錯誤** (12) 
</dt> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>**降級的信號** (13) 
</dt> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**DTE-DCE 介面錯誤** (14) 
</dt> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>**主機殼門開啟** (15) 
</dt> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**設備故障** (16) 
</dt> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**過度震動** (17) 
</dt> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**檔案格式錯誤** (18) 
</dt> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>**引發偵測到** (19) 
</dt> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>偵測 **到大量** (20) 
</dt> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**框架錯誤** (21) 
</dt> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**HVAC 問題** (22) 
</dt> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>不 **接受濕度** (23) 
</dt> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>**I/o 裝置錯誤** (24) 
</dt> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**輸入裝置錯誤** (25) 
</dt> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**區域網路錯誤** (26) 
</dt> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>偵測 **到未有毒的** 流失 (27) 
</dt> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**本機節點傳輸錯誤** (28) 
</dt> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**遺失框架** (29) 
</dt> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span> (30) **的信號遺失**
</dt> <dt>

<span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**31** 個數據供應已用盡 (31) 
</dt> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>多工器 **問題** (32) 
</dt> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**記憶體不足** (33) 
</dt> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**輸出裝置錯誤** (34) 
</dt> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>**效能降低** (35) 
</dt> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**電源問題** (36) 
</dt> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**不可接受的壓力** (37) 
</dt> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**處理器問題 (內部電腦錯誤)** (38) 
</dt> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>提取 **失敗** (39) 
</dt> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**佇列大小超過** (40) 
</dt> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**接收失敗** (41) 
</dt> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**接收者失敗** (42) 
</dt> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**遠端節點傳輸錯誤** (43) 
</dt> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**資源或接近容量** (44) 
</dt> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**回應時間過度** (45) 
</dt> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>重新 **傳輸速率過高** (46) 
</dt> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**軟體錯誤** (47) 
</dt> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>**軟體程式異常終止** (48) 
</dt> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**軟體程式錯誤 (不正確的結果)** (49) 
</dt> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**儲存體容量問題** (50) 
</dt> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>無法 **接受的溫度** (51) 
</dt> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**超過** (52) 的閾值
</dt> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**計時問題** (53) 
</dt> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>偵測 **到有毒** 流失 (54) 
</dt> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**傳輸失敗** (55) 
</dt> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>**發送器失敗** (56) 
</dt> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**基礎資源無法使用** (57) 
</dt> <dt>

<span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**版本不相符** (58) 
</dt> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**先前的警示已清除** (59) 
</dt> <dt>

<span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**60 登入嘗試失敗** (60) 
</dt> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>偵測 **到的軟體病毒** (61) 
</dt> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**硬體安全性違反** 了 (62) 
</dt> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>偵測 **到拒絕服務** (63) 
</dt> <dt>

<span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>**安全性認證不符** (64) 
</dt> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>**未經授權的存取** (65) 
</dt> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**已收到** (66) 的鬧鐘
</dt> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**遺失指標** (67) 
</dt> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>承載 **不符** (68) 
</dt> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**傳輸錯誤** (69) 
</dt> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**過多錯誤率** (70) 
</dt> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>**追蹤問題** (71) 
</dt> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**元素無法使用** (72) 
</dt> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>**遺漏的元素** (73) 
</dt> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**遺失多框架** (74) 
</dt> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**廣播通道失敗** (75) 
</dt> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>**收到的訊息無效** (76) 
</dt> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**路由失敗** (77) 
</dt> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**背板失敗** (78) 
</dt> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**識別碼重複** (79) 
</dt> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**保護路徑失敗** (80) 
</dt> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**同步遺失或** (81) 不相符
</dt> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**終端機問題** (82) 
</dt> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**系統時鐘失敗** (83) 
</dt> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**天線失敗** (84) 
</dt> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**電池充電失敗** (85) 
</dt> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>**磁片失敗** (86) 
</dt> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**頻率跳動失敗** (87) 
</dt> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**遺失冗余** (88) 
</dt> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**電源供應器失敗** (89) 
</dt> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**信號品質問題** (90) 
</dt> <dt>

<span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>**91 電池放電** (91) 
</dt> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**電池故障** (92) 
</dt> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**商業電源問題** (93) 
</dt> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**風扇故障** (94) 
</dt> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>**引擎失敗** (95) 
</dt> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**感應器失敗** (96) 
</dt> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**保險絲故障** (97) 
</dt> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>產生器 **失敗** (98) 
</dt> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**電力偏低** (99) 
</dt> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**低燃料** (100) 
</dt> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**低水位** (101) 
</dt> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**爆炸性天然氣** (102) 
</dt> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**高接近尾聲** (103) 
</dt> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**Ice 堆積** (104) 
</dt> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>**冒煙** (105) 
</dt> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>**記憶體不符** (106) 
</dt> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**CPU 週期** (107) 
</dt> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**軟體環境問題** (108) 
</dt> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**軟體下載失敗** (109) 
</dt> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>**元素重新初始化** (110) 
</dt> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Timeout** (111) 
</dt> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**記錄問題** (112) 
</dt> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>偵測到 (113) 的 **洩漏**
</dt> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**保護機制失敗** (114) 
</dt> <dt>

<span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**115 保護資源失敗** (115) 
</dt> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>**資料庫不一致** (116) 
</dt> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**驗證失敗** (117) 
</dt> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span> (118) **的機密性缺口**
</dt> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**纜線防** (119) 
</dt> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**延遲的資訊** (120) 
</dt> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**重複的資訊** (121) 
</dt> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**遺漏** (122) 的資訊
</dt> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span> (123) 的 **資訊修改**
</dt> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**順序中的資訊** (124) 
</dt> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>**金鑰已過期** (125) 
</dt> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**不可否認性失敗** (126) 
</dt> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>下班 **時間活動** (127) 
</dt> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>**服務** (128) 
</dt> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>程式 **錯誤** (129) 
</dt> <dt>

<span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>未 **預期的資訊** (130 ) 
</dt> </dl>

</dd> <dt>

**ProbableCauseDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述錯誤可能原因的字串。 這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。

</dd> <dt>

**RecommendedActions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述要採取以解決錯誤之建議動作的字串。 這個屬性繼承自 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))。

</dd> </dl>

## <a name="remarks"></a>備註

**Msvm \_ 錯誤** 類別的存取權可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 錯誤**](cim-error.md)
</dt> <dt>

[**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85))
</dt> <dt>

[虛擬系統管理類別](virtual-system-management-classes.md)
</dt> </dl>

 

