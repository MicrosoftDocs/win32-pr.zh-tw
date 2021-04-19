---
description: CIM 警示通知的具體超類別。
ms.assetid: ec4cf41d-decd-4f21-b805-90db4a61376d
title: CIM_AlertIndication 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlertIndication
- CIM_AlertIndication.Description
- CIM_AlertIndication.AlertingManagedElement
- CIM_AlertIndication.AlertingElementFormat
- CIM_AlertIndication.OtherAlertingElementFormat
- CIM_AlertIndication.AlertType
- CIM_AlertIndication.OtherAlertType
- CIM_AlertIndication.PerceivedSeverity
- CIM_AlertIndication.ProbableCause
- CIM_AlertIndication.ProbableCauseDescription
- CIM_AlertIndication.Trending
- CIM_AlertIndication.RecommendedActions
- CIM_AlertIndication.EventID
- CIM_AlertIndication.EventTime
- CIM_AlertIndication.SystemCreationClassName
- CIM_AlertIndication.SystemName
- CIM_AlertIndication.ProviderName
- CIM_AlertIndication.Message
- CIM_AlertIndication.MessageArguments
- CIM_AlertIndication.MessageID
- CIM_AlertIndication.OwningEntity
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1916705ee696c949dba2a557f7077ade8db7ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970755"
---
# <a name="cim_alertindication-class"></a>CIM \_ AlertIndication 類別

CIM 警示通知的具體超類別。 **CIM \_AlertIndication** 是 **CIM \_ 指示** 類別的特製化類型，其中包含有關「真實世界」事件的嚴重性、原因、建議動作和其他資料的資訊。 此事件和其資料可能不會在 CIM 類別階層中建立模型。

## <a name="syntax"></a>語法

``` syntax
[Indication, Version("2.22.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_AlertIndication : CIM_ProcessIndication
{
  string   Description;
  string   AlertingManagedElement;
  uint16   AlertingElementFormat = 0;
  string   OtherAlertingElementFormat;
  uint16   AlertType;
  string   OtherAlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  uint16   Trending;
  string   RecommendedActions[];
  string   EventID;
  datetime EventTime;
  string   SystemCreationClassName;
  string   SystemName;
  string   ProviderName;
  string   Message;
  string   MessageArguments[];
  string   MessageID;
  string   OwningEntity;
};
```

## <a name="members"></a>成員

**CIM \_ AlertIndication** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ AlertIndication** 類別具有這些屬性。

<dl> <dt>

**AlertingElementFormat**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**AlertingManagedElement**"，"**CIM \_ AlertIndication**.**OtherAlertingElementFormat**") 
</dt> </dl>

**AlertingManagedElement** 屬性的格式。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd>

CIM 用戶端應用程式可解譯的格式不明或不具意義。

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd>

格式是由 OtherAlertingElementFormat 屬性的值所定義。

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2) 


</dt> <dd>

格式為 CIMObjectPath，指定 CIM 架構中的實例。

</dd> </dl>

</dd> <dt>

**AlertingManagedElement**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**AlertingElementFormat**") 
</dt> </dl>

實體 (的識別資訊，即產生此指示的實例) 。 屬性包含實例的路徑，編碼為字串參數-如果實例在 CIM 架構中建立模型。 如果不是 CIM 實例，屬性會包含一些識別字串來為產生警示的實體命名。 路徑或識別字串會根據 AlertingElementFormat 屬性格式化。

</dd> <dt>

**AlertType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。事件種類 ") 
</dt> </dl>

指示的主要分類。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd>

\- 其他。 指示的 OtherAlertType 屬性會傳達其分類。 列舉中的「其他」使用是標準的 CIM 慣例。 這表示目前的指示不符合此列舉所描述的類別。

</dd> <dt>

<span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>

<span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>**通訊警示** (2) 


</dt> <dd>

這種類型的指示主要是與將資訊從某個點傳送到另一個點所需的程式和/或程式相關聯。

</dd> <dt>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**服務品質警示** (3) 


</dt> <dd>

這種類型的表示主要與實體的效能或功能中的效能或錯誤相關。

</dd> <dt>

<span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>

<span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>**處理錯誤** (4) 


</dt> <dd>

這種類型的表示主要與軟體或處理錯誤相關。

</dd> <dt>

<span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>

<span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>**裝置警示** (5) 


</dt> <dd>

這種類型的表示主要與設備或硬體錯誤相關。

</dd> <dt>

<span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>

<span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>**環境警示** (6) 


</dt> <dd>

環境警示。 這種類型的指示主要是與硬體所在主機殼相關的條件相關聯，或其他環境考慮。

</dd> <dt>

<span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>

<span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>**模型變更** (7) 


</dt> <dd>

指示會解決資訊模型中的變更。 例如，它可能會內嵌生命週期指示，以傳達要警示的特定模型變更。

</dd> <dt>

<span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>

<span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>**安全性警示** (8) 


</dt> <dd>

. 這種類型的指示會相關聯。

</dd> </dl>

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。其他文字 ") 
</dt> </dl>

指示的簡短描述。

</dd> <dt>

**EventID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**ProbableCause**") 
</dt> </dl>

檢測或提供者特定的值，用來描述以指示表示的基礎真實世界事件。 具有相同非 Null **EventID** 值的指標會被建立實體考慮，以代表相同的事件。 兩個 **EventID** 值的比較只會針對具有相同、非 Null 值 **SystemCreateClassName**、 **SystemName** 和 **ProviderName** 屬性的警示指示而定義。

</dd> <dt>

**EventTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**ProbableCause**") 
</dt> </dl>

指出第一次偵測到基礎事件的時間和日期。 如果指定了此值，且建立的實體無法提供這項資訊，則此屬性必須設定為 **Null**。 此值是以產生指示之 **CIM \_ ManageSystemElement** 物件的本地日期和時間的概念為基礎。

</dd> <dt>

**訊息**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**MessageID**"，"**CIM \_ AlertIndication**。**MessageArguments**") 
</dt> </dl>

警示指示的格式化訊息。 這則訊息的格式化方式是結合 **MessageArguments** 屬性中指定的一或多個動態元素，以及 **MessageID** 屬性唯一識別的靜態專案。

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**Message**"，"**CIM \_ AlertIndication**。**MessageID**") 
</dt> </dl>

陣列，其中包含警示指示之訊息的動態內容。

</dd> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**Message**"，"**CIM \_ AlertIndication**。**MessageArguments**") 
</dt> </dl>

訊息格式的唯一識別碼，遷移在 **OwningEntity** 中指定之組織的範圍。

</dd> <dt>

**OtherAlertingElementFormat**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**AlertingElementFormat**") 
</dt> </dl>

當 **AlertingElementFormat** 屬性設定為 "1" (其他) 時，定義 **AlertingManagedElement** 屬性的格式;否則，此值必須設定為 **Null**。

</dd> <dt>

**OtherAlertType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**AlertType**") 
</dt> </dl>

當 **AlertType** 屬性設定為 "1" (其他狀態變更) 時，描述 **AlertType** 值的字串。

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

擁有 **Message** 屬性格式定義之組織的唯一識別碼。 **OwningEntity** 必須包含受著作權、商標或唯一的名稱，該名稱是由定義訊息格式的商務實體或標準主體所擁有。

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PerceivedSeverity" ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。察覺嚴重性」 ) 
</dt> </dl>

從引發警示之元素的觀點來指出警示的嚴重性。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd>

遵循常見的使用方式。

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd>

表示可以在 OtherSeverity 屬性中找到嚴重性的值。

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**資訊** (2) 


</dt> <dd>

遵循常見的使用方式。

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**降級/警告** (3) 


</dt> <dd>

如果適合讓使用者決定是否需要採取動作，則應該使用。

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**次要** (4) 


</dt> <dd>

指出需要採取動作，但目前的情況並不嚴重。

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**主要** (5) 


</dt> <dd>

指出現在需要採取動作。

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (6) 


</dt> <dd>

現在需要採取動作，而範圍很廣泛 (可能會導致重要資源的即將中斷) 。

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**嚴重/** 無法恢復 (7) 


</dt> <dd>

指出發生錯誤，但太晚採取補救動作。

</dd> </dl>

</dd> <dt>

**ProbableCause**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。可能的原因 "、" \| M3100. probableCause "、" itu-IANA-鬧鐘-TC ") 、 [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**。**ProbableCauseDescription**"，"**CIM \_ AlertIndication**.**EventID**"，"**CIM \_ AlertIndication**。**EventTime**") 
</dt> </dl>

導致警示指示的情況可能原因。

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

<span id="Version_MisMatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

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

<span id="Security_Credential_MisMatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

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


</dt> <dd></dd> </dl>

</dd> <dt>

**ProbableCauseDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AlertIndication**.**ProbableCause**") 
</dt> </dl>

**ProbableCause** 屬性的其他相關資訊。

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

產生指示的提供者名稱。

</dd> <dt>

**RecommendedActions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。建議的修復動作」 ) 
</dt> </dl>

用於解決通知原因之建議動作的自由形式描述。

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

產生指示之提供者的範圍系統的 **CreationClassName** 值。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

產生指示之提供者的範圍系統名稱。

</dd> <dt>

**趨勢**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。TrendIndication ") 
</dt> </dl>

提供趨勢趨勢-向上、向下或無變更的相關資訊。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**不適用** (1) 


</dt> <dd></dd> <dt>

<span id="Trending_Up"></span><span id="trending_up"></span><span id="TRENDING_UP"></span>

**趨勢向上** (2) 


</dt> <dd></dd> <dt>

<span id="Trending_Down"></span><span id="trending_down"></span><span id="TRENDING_DOWN"></span>

 (3) 的 **趨勢**


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

**沒有變更** (4) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ ProcessIndication**](cim-processindication.md)
</dt> </dl>

 

