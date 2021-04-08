---
description: 描述相關聯 Msvm \_ MetricService 實例的功能。
ms.assetid: 4E24D675-8265-4B5E-9551-550510B138FE
title: Msvm_MetricServiceCapabilities 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceCapabilities
- Msvm_MetricServiceCapabilities.InstanceID
- Msvm_MetricServiceCapabilities.Caption
- Msvm_MetricServiceCapabilities.Description
- Msvm_MetricServiceCapabilities.ElementName
- Msvm_MetricServiceCapabilities.ElementNameEditSupported
- Msvm_MetricServiceCapabilities.MaxElementNameLen
- Msvm_MetricServiceCapabilities.RequestedStatesSupported
- Msvm_MetricServiceCapabilities.ElementNameMask
- Msvm_MetricServiceCapabilities.ControllableMetrics
- Msvm_MetricServiceCapabilities.MetricsControlTypes
- Msvm_MetricServiceCapabilities.ControllableManagedElements
- Msvm_MetricServiceCapabilities.ManagedElementControlTypes
- Msvm_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 635e153d3184e74ea581a045e3d6d54a5fea199f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852384"
---
# <a name="msvm_metricservicecapabilities-class"></a>Msvm \_ MetricServiceCapabilities 類別

描述相關聯 [**Msvm \_ MetricService**](msvm-metricservice.md) 實例的功能。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceCapabilities : CIM_MetricServiceCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Metric Service Capabilities";
  string  Description = "Defines Hyper-V Metric Service Capabilities";
  string  ElementName = "Hyper-V Metric Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  ControllableMetrics[];
  uint16  MetricsControlTypes[];
  string  ControllableManagedElements[];
  uint16  ManagedElementControlTypes[];
  uint16  SupportedMethods[];
};
```

## <a name="members"></a>成員

**Msvm \_ MetricServiceCapabilities** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ MetricServiceCapabilities** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 計量服務功能」。

</dd> <dt>

**ControllableManagedElements**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **ArrayType** ( 「已編制索引」 ) 
</dt> </dl>

識別可由相關聯的 **cim \_ MetricService** 實例控制的 [**cim \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)實例。 如果此屬性為 **Null**，則可以控制所有元素。 這個屬性繼承自 **CIM \_ MetricServiceCapabilities**。

</dd> <dt>

**ControllableMetrics**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **ArrayType** ( 「已編制索引」 ) 
</dt> </dl>

識別可由相關聯的 **cim \_ MetricService** 實例控制的 **cim \_ BaseMetricDefinition** 實例。 如果此屬性為 **Null**，則可以控制所有計量。 這個屬性繼承自 **CIM \_ MetricServiceCapabilities**。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「定義 Hyper-v 計量服務功能」。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 計量服務功能」。

</dd> <dt>

**ElementNameEditSupported**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否可以修改 **ElementName** 屬性。 這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。

</dd> <dt>

**ElementNameMask**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定 **ElementName** 的限制，以正則運算式表示。 這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

唯一識別此類別的實例。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**ManagedElementControlTypes**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **ArrayType** ( 「已編制索引」 ) 
</dt> </dl>

針對 **ControllableManagedElements** 屬性中位於相同陣列索引的值所識別的 [**cim \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)物件，識別相關聯的 **cim \_ MetricService** 實例所支援的控制項類型。 如果此屬性為 **Null**，則支援所有控制項類型。 這個屬性繼承自 **CIM \_ MetricServiceCapabilities**。



| 值                                                                                   | 意義                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Unknown<br/>         |
| <dl> <dt>2</dt> </dl>            | Discrete<br/>        |
| <dl> <dt>3</dt> </dl>            | 大量<br/>            |
| <dl> <dt>4</dt> </dl>            | 兩者<br/>            |
| <dl> <dt>5. 32767</dt> </dl>     | 已保留 DMTF<br/>   |
| <dl> <dt>32768. 65535</dt> </dl> | 特定廠商<br/> |



 

</dd> <dt>

**MaxElementNameLen**
</dt> <dd> <dl> <dt>

資料類型： **unit16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **int32.maxvalue** (256) 
</dt> </dl>

指定 **ElementName** 屬性支援的最大長度。 這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。

</dd> <dt>

**MetricsControlTypes**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **ArrayType** ( 「已編制索引」 ) 
</dt> </dl>

識別 **ControllableMetrics** 屬性中相同陣列索引的值所識別之 **cim \_ BaseMetricDefinition** 的相關 **cim \_ MetricService** 實例所支援的控制項類型。 如果此屬性為 **Null**，則支援所有控制項類型。 這個屬性繼承自 **CIM \_ MetricServiceCapabilities**。



| 值                                                                                   | 意義                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Unknown<br/>         |
| <dl> <dt>2</dt> </dl>            | Discrete<br/>        |
| <dl> <dt>3</dt> </dl>            | 大量<br/>            |
| <dl> <dt>4</dt> </dl>            | 兩者<br/>            |
| <dl> <dt>5. 32767</dt> </dl>     | 已保留 DMTF<br/>   |
| <dl> <dt>32768. 65535</dt> </dl> | 特定廠商<br/> |



 

</dd> <dt>

**RequestedStatesSupported**
</dt> <dd> <dl> <dt>

資料類型： **unit16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出在啟用的邏輯元素上使用 **RequestStateChange** 方法時，可以要求的可能狀態。 這個屬性繼承自 **CIM \_ EnabledLogicalElementCapabilities**。



| 值                                                                         | 意義              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <dt>2</dt> </dl>  | 已啟用<br/>   |
| <dl> <dt>3</dt> </dl>  | 禁用<br/>  |
| <dl> <dt>4</dt> </dl>  | 關閉<br/> |
| <dl> <dt>6</dt> </dl>  | 離線<br/>   |
| <dl> <dt>7</dt> </dl>  | 測試<br/>      |
| <dl> <dt>8</dt> </dl>  | 推遲<br/>     |
| <dl> <dt>9</dt> </dl>  | 靜止<br/>   |
| <dl> <dt>10</dt> </dl> | 重新啟動<br/>    |
| <dl> <dt>11</dt> </dl> | 重設<br/>     |



 

</dd> <dt>

**>supportedmethods**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定度量服務所支援的方法。 這個屬性繼承自 **CIM \_ MetricServiceCapabilities**。



| 值                                                                                   | 意義                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>2</dt> </dl>            | 支援 [**ControlMetrics**](controlmetrics-msvm-metricservice.md) 方法。<br/> |
| <dl> <dt>3</dt> </dl>            | 支援 **ControlMetricsByClass** 方法。<br/>                                   |
| <dl> <dt>4</dt> </dl>            | 支援 **ShowMetrics** 方法。<br/>                                             |
| <dl> <dt>5</dt> </dl>            | 支援 **ShowMetricsByClass** 方法。<br/>                                      |
| <dl> <dt>6</dt> </dl>            | 支援 **GetMetricValues** 方法。<br/>                                         |
| <dl> <dt>7</dt> </dl>            | 支援 **ControlSampleTimes** 方法。<br/>                                      |
| <dl> <dt>8. 32767</dt> </dl>     | 已保留 DMTF<br/>                                                                        |
| <dl> <dt>32768. 65535</dt> </dl> | 特定廠商<br/>                                                                      |



 

</dd> </dl>

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

[**CIM \_ MetricServiceCapabilities**](cim-metricservicecapabilities.md)
</dt> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

