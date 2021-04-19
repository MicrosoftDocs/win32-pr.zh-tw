---
description: 表示度量的定義方面。
ms.assetid: 861a69f6-a3bf-4e18-a9c2-931632e3cccc
title: Msvm_BaseMetricDefinition 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricDefinition
- Msvm_BaseMetricDefinition.InstanceID
- Msvm_BaseMetricDefinition.Caption
- Msvm_BaseMetricDefinition.Description
- Msvm_BaseMetricDefinition.ElementName
- Msvm_BaseMetricDefinition.Id
- Msvm_BaseMetricDefinition.Name
- Msvm_BaseMetricDefinition.DataType
- Msvm_BaseMetricDefinition.Calculable
- Msvm_BaseMetricDefinition.Units
- Msvm_BaseMetricDefinition.BreakdownDimensions
- Msvm_BaseMetricDefinition.IsContinuous
- Msvm_BaseMetricDefinition.ChangeType
- Msvm_BaseMetricDefinition.TimeScope
- Msvm_BaseMetricDefinition.GatheringType
- Msvm_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d1edbd722e3bf87631371b5650576917a7cfb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986402"
---
# <a name="msvm_basemetricdefinition-class"></a>Msvm \_ BaseMetricDefinition 類別

表示度量的定義方面。 **Msvm \_ BaseMetricDefinition** 類別應該與它所套用的 [**CIM \_ ManagedElements**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)相關聯。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricDefinition : CIM_BaseMetricDefinition
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  string  Id;
  string  Name;
  uint16  DataType;
  uint16  Calculable;
  string  Units;
  string  BreakdownDimensions[];
  boolean IsContinuous;
  uint16  ChangeType;
  uint16  TimeScope;
  uint16  GatheringType;
  string  ProgrammaticUnits;
};
```

## <a name="members"></a>成員

**Msvm \_ BaseMetricDefinition** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ BaseMetricDefinition** 類別具有這些屬性。

<dl> <dt>

**BreakdownDimensions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

定義一個或多個字串，可用來針對特定維度上的度量值， (細分) 查詢。 其中一個範例是交易名稱，允許將所有交易的總值細分為一組值，每個交易名稱各一個值。 其他範例可能是應用程式系統或使用者組名。 這些字串是免費格式，對計量資料的使用者而言應該有意義。 這些字串表示基礎檢測針對此計量定義支援哪些細分維度。 這個屬性繼承自 **CIM \_ BaseMetricDefinition**。

</dd> <dt>

**計算**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述用於執行計算之度量的特性。 這個屬性繼承自 **CIM \_ BaseMetricDefinition**。 這可能是 **Null** 或下列其中一個值。



| 值                                                                                                                                                                                                                                                   | 意義                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <dt>**非可計算**</dt> <dt>1</dt> </dl> | 無法計算此值。 例如，字串。<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <dt>**Summable**</dt> <dt>2</dt> </dl>                         | 此值可以加總許多實例。 例如，如果每個備份作業都是工作單位，而且每個作業平均備份27000檔案，則100備份作業會處理2700000檔案。<br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <dt>**非 summable**</dt> <dt>3</dt> </dl>    | 此值不能加總在許多實例上。 其中一個範例是在作業抵達伺服器時測量佇列長度的度量。 如果每個作業都是工作單位，而且每個作業抵達時的平均佇列長度為33，則表示100作業的佇列長度為3300並不合理。 假設 mean 為33，是合理的。<br/> |



 

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示計量值如何變更，以典型的細部屬性組合（例如方向變更、最小和最大值和最大值），以及換行語義的形式呈現。 這個屬性繼承自 **CIM \_ BaseMetricDefinition**。



| 值                                                                                                                                                                                                                                                                       | 意義                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**未知**</dt>的 <dt>0</dt> </dl>                                                 | 度量設計師未限定 **ChangeType。**<br/>                                                                                                                              |
| <span id="N_A"></span><span id="n_a"></span><dl> <dt>**N/A**</dt> <dt>2</dt> </dl>                                                                                       | 如果 **IsContinuous** 屬性為 "false"， **ChangeType** 就沒有意義，且必須設定為 "N/A"。<br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <dt>**計數器**</dt> <dt>3</dt> </dl>                                                 | 度量是計數器度量。 這些都有非負整數值，在達到可表示的最大值，然後換行並開始從0增加時，才會增加。<br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <dt></dt>量測計<dt>4</dt> </dl>                                                         | 計量是量測計度量。 這些值具有可任意增加和減少的整數或浮點值。<br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF 保留**</dt> <dt>5. 32767</dt> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt>**廠商保留**</dt> <dt>32768. 65535</dt> </dl> | 廠商可以擴充廠商保留範圍中的 **ChangeType** 屬性。<br/>                                                                                                          |



 

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

度量的資料類型。 這個屬性繼承自 **CIM \_ BaseMetricDefinition**。

<dl> <dt>

<span id="boolean"></span><span id="BOOLEAN"></span>**布林值** (1) 
</dt> <dt>

<span id="char16"></span><span id="CHAR16"></span>**char16** (2) 
</dt> <dt>

<span id="datetime"></span><span id="DATETIME"></span>**datetime** (3) 
</dt> <dt>

<span id="real32"></span><span id="REAL32"></span>**real32** (4) 
</dt> <dt>

<span id="real64"></span><span id="REAL64"></span>**real64** (5) 
</dt> <dt>

<span id="sint16"></span><span id="SINT16"></span>**sint16** (6) 
</dt> <dt>

<span id="sint32"></span><span id="SINT32"></span>**sint32** (7) 
</dt> <dt>

<span id="sint64"></span><span id="SINT64"></span>**sint64** (8) 
</dt> <dt>

<span id="sint8"></span><span id="SINT8"></span>**sint8** (9) 
</dt> <dt>

<span id="string"></span><span id="STRING"></span>**字串** (10) 
</dt> <dt>

<span id="uint16"></span><span id="UINT16"></span>**uint16** (11) 
</dt> <dt>

<span id="uint32"></span><span id="UINT32"></span>**uint32** (12) 
</dt> <dt>

<span id="uint64"></span><span id="UINT64"></span>**uint64** (13) 
</dt> <dt>

<span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14 ) 
</dt> </dl>

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**GatheringType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出基礎檢測如何收集度量值。 這可讓用戶端應用程式選擇正確的度量以供用途。 這個屬性繼承自 **CIM \_ BaseMetricDefinition**。 這可能是 **Null** 或下列其中一個值。



| 值                                                                                                                                                                                                                                                                       | 意義                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**未知**</dt>的 <dt>0</dt> </dl>                                                 | 收集類型未知。<br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <dt>**OnChange**</dt> <dt>2</dt> </dl>                                             | 當測量的資源內的值變更時，就會立即更新度量值。<br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <dt>**週期**</dt> <dt>3</dt> </dl>                                             | 度量值會定期更新。 比方說，在用戶端應用程式中，套用至目前時間的度量值在每個收集間隔期間都會出現常數，然後在每個收集間隔結束時跳到新值。<br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <dt>**OnRequest**</dt> <dt>4</dt> </dl>                                         | 每次用戶端應用程式讀取時，就會決定度量值。<br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF 保留**</dt> <dt>5. 32767</dt> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt>**廠商保留**</dt> <dt>32768. 65535</dt> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

**識別碼**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

可唯一識別度量定義的字串。 這個屬性繼承自 **CIM \_ BaseMetricDefinition**。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

可唯一識別這個類別之實例的字串。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**IsContinuous**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出度量值為連續或純量。 效能計量是連續度量的範例。 純量計量的範例包括錯誤碼或操作狀態。 您可以使用「大於」關聯來比較連續計量。 這個屬性繼承自 **CIM \_ BaseMetricDefinition**。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

計量的名稱。 這個屬性繼承自 **CIM \_ BaseMetricDefinition**。

</dd> <dt>

**ProgrammaticUnits**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別值的特定單位。 這個屬性的值將會是程式設計單位辨識符號的合法值，如 [DSP0004 2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) 或更新版本的附錄 C. 1 中所定義。 這個屬性繼承自 **CIM \_ BaseMetricDefinition**。

</dd> <dt>

**TimeScope**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

表示套用度量值的時間範圍。 這個屬性繼承自 **CIM \_ BaseMetricDefinition**。



| 值                                                                                                                                                                                                                                                                       | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**未知**</dt>的 <dt>0</dt> </dl>                                                 | 時間範圍未由計量設計師限定，或對提供者而言是未知的。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <dt>**點**</dt> <dt>2</dt> </dl>                                                         | 度量會套用至某個時間點。 在對應的 [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) 實例上， **TimeStamp** 屬性會指定時間點，而 **Duration** 屬性一律為0。<br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <dt>**間隔**</dt> <dt>3</dt> </dl>                                             | 度量會套用至時間間隔。 在對應的 [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) 實例上， **TimeStamp** 屬性會指定時間間隔的結尾，而 **duration** 屬性則會指定其持續時間。<br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <dt>**StartupInterval**</dt> <dt>4</dt> </dl>                 | 計量適用于啟動測量資源 (的時間間隔，也就是 MetricDefForMe) 相關聯的 ManagedElement。 在對應的 [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) 實例上， **TimeStamp** 屬性會指定時間間隔的結尾。 如果 **Duration** 屬性是0，這表示測量的資源的啟動時間是未知的。 否則， **duration** 會指定資源和 **時間戳記** 啟動之間的持續時間。<br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF 保留**</dt> <dt>5. 32767</dt> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt>**廠商保留**</dt> <dt>32768. 65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**單位**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別值的特定單位，例如「mb」。 這個屬性繼承自 **CIM \_ BaseMetricDefinition**。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

