---
description: 表示包含 CIM MetricInstance 物件中繼資料的度量定義 \_ 。
ms.assetid: 6abfb0dc-e80b-4ca6-89d9-2e43283d0abe
title: CIM_BaseMetricDefinition 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricDefinition
- CIM_BaseMetricDefinition.Id
- CIM_BaseMetricDefinition.Name
- CIM_BaseMetricDefinition.DataType
- CIM_BaseMetricDefinition.Calculable
- CIM_BaseMetricDefinition.Units
- CIM_BaseMetricDefinition.BreakdownDimensions
- CIM_BaseMetricDefinition.IsContinuous
- CIM_BaseMetricDefinition.ChangeType
- CIM_BaseMetricDefinition.TimeScope
- CIM_BaseMetricDefinition.GatheringType
- CIM_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cac965ed1eae59f1c269d897a12e9aa116183eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001455"
---
# <a name="cim_basemetricdefinition-class"></a>CIM \_ BaseMetricDefinition 類別

表示包含 **CIM \_ MetricInstance** 物件中繼資料的度量定義。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricDefinition : CIM_ManagedElement
{
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

**CIM \_ BaseMetricDefinition** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ BaseMetricDefinition** 類別具有這些屬性。

<dl> <dt>

**BreakdownDimensions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

陣列，其中包含可用來將 [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md) 物件的查詢沿著特定維度細分的自由格式字串。 這些字串對計量資料的終端使用者應該有意義。 此外，這些字串應該會指出基礎檢測針對計量定義支援哪些細分維度。

例如，允許將所有交易的總值細分為一組值的交易名稱，每個交易名稱各有一個值。 其他範例包括應用程式系統或使用者組名。

</dd> <dt>

**計算**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用來執行計算的度量特性。

<dt>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**非可計算** (1) 


</dt> <dd>

字串。 算術沒有任何意義。

</dd> <dt>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Summable** (2) 


</dt> <dd>

將此值與許多實例（例如 UnitOfWork）加總，例如在備份作業中處理的檔案數目，是合理的。 例如，如果每個備份作業都是 UnitOfWork，而且每個作業都會平均備份27000檔案，則應該假設100備份作業已處理2700000檔案。

</dd> <dt>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**非 summable** (3) 


</dt> <dd>

在 UnitOfWork 的許多實例加總此值並不合理。 其中一個範例是在作業抵達伺服器時測量佇列長度的度量。 如果每個作業都是 UnitOfWork，而且每個作業抵達時的平均佇列長度為33，則表示100作業的佇列長度為3300並不合理。 假設 mean 為33，是合理的。

</dd> </dl>

</dd> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ BaseMetricDefinition**.**IsContinuous**") 
</dt> </dl>

使用一般屬性（例如方向變更、最小值和最大值和包裝語義）來表示計量值的變更方式。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd>

度量設計師未限定 ChangeType。

</dd> <dt>

<span id="N_A"></span><span id="n_a"></span>

<span id="N_A"></span><span id="n_a"></span>**N/A** (2) 


</dt> <dd>

如果 "IsContinuous" 屬性為 "false"，ChangeType 就沒有意義，且必須設定為 "N/A"。

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**計數器** (3) 


</dt> <dd>

度量是計數器度量。 這些都有非負整數值，會在到達可表示的最大值時單純增加，然後換行並開始從0增加。 這類計數器（也稱為變換計數器）可以用來計算網路錯誤的數目或處理的交易數目。 用戶端應用程式追蹤換行程式的唯一方法，是以適當的短間隔取出計數器的值。

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>量測 **計 (4**) 


</dt> <dd>

計量是量測計度量。 這些值具有可任意增加和減少的整數或浮點值。 量測計在達到可表示的最小值或最大值時不能換行，而是在該數位的值 "棒"。 可代表值範圍內的最小值或最大值，而不一定會定義度量值 "棒"。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** (5. 32767) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) 


</dt> <dd></dd> </dl>

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

度量的資料類型。

<dt>

<span id="boolean"></span><span id="BOOLEAN"></span>

**布林值** (1) 


</dt> <dd></dd> <dt>

<span id="char16"></span><span id="CHAR16"></span>

**char16** (2) 


</dt> <dd></dd> <dt>

<span id="datetime"></span><span id="DATETIME"></span>

**datetime** (3) 


</dt> <dd></dd> <dt>

<span id="real32"></span><span id="REAL32"></span>

**real32** (4) 


</dt> <dd></dd> <dt>

<span id="real64"></span><span id="REAL64"></span>

**real64** (5) 


</dt> <dd></dd> <dt>

<span id="sint16"></span><span id="SINT16"></span>

**sint16** (6) 


</dt> <dd></dd> <dt>

<span id="sint32"></span><span id="SINT32"></span>

**sint32** (7) 


</dt> <dd></dd> <dt>

<span id="sint64"></span><span id="SINT64"></span>

**sint64** (8) 


</dt> <dd></dd> <dt>

<span id="sint8"></span><span id="SINT8"></span>

**sint8** (9) 


</dt> <dd></dd> <dt>

<span id="string"></span><span id="STRING"></span>

**字串** (10) 


</dt> <dd></dd> <dt>

<span id="uint16"></span><span id="UINT16"></span>

**uint16** (11) 


</dt> <dd></dd> <dt>

<span id="uint32"></span><span id="UINT32"></span>

**uint32** (12) 


</dt> <dd></dd> <dt>

<span id="uint64"></span><span id="UINT64"></span>

**uint64** (13) 


</dt> <dd></dd> <dt>

<span id="uint8"></span><span id="UINT8"></span>

**uint8** (14) 


</dt> <dd></dd> </dl>

</dd> <dt>

**GatheringType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出基礎檢測如何收集度量值。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd>

指出 GatheringType 是未知的。

</dd> <dt>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2) 


</dt> <dd>

指出當測量的資源內的值變更時，會立即更新 CIM 度量值。 OnChange 計量的值會確實反映資源在任何時間內的目前情況。 例如，當使用者登入和關閉時，會立即更新的已登入使用者數目。

</dd> <dt>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**定期** (3) 


</dt> <dd>

"：表示會定期更新 CIM 度量值。 比方說，在用戶端應用程式中，套用至目前時間的度量值在每個收集間隔中都會顯示為常數，然後在每個收集間隔結束時跳到新值。

</dd> <dt>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4) 


</dt> <dd>

指出每次用戶端應用程式讀取時，都會決定 CIM 度量值。 如果有人要求，OnRequest 計量的值真的會傳回資源內目前的狀況。 不過，它們不會變更 "未觀察到"，因此不建議訂閱 OnRequest 計量的值變更。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** (5. 32767) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) 


</dt> <dd></dd> </dl>

</dd> <dt>

**識別碼**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

度量定義的唯一識別碼。 建議您開啟 Software Foundation (憑證) UUID/Guid。

</dd> <dt>

**IsContinuous**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果度量值是連續的，則為 True;否則為 false。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

計量的名稱。 此名稱不一定要是唯一的，但應該是描述性的，而且可能包含空格。

</dd> <dt>

**ProgrammaticUnits**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

值的特定單位。 這個屬性的值應該是程式設計單位辨識符號的合法值，如 DSP0004 2.4 或更新版本的附錄 C. 1 中所定義。

</dd> <dt>

**TimeScope**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ BaseMetricValue**](cim-basemetricvalue.md).**TimeStamp**"、"**CIM \_ BaseMetricValue**。**Duration**") 
</dt> </dl>

適用于度量設計師的時間範圍。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd>

指出時間範圍未由計量設計師限定，或對提供者而言是未知的。

</dd> <dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>**點** (2) 


</dt> <dd>

指出度量會套用至某個時間點。 在對應的 BaseMetricValue 實例上，TimeStamp 會指定時間點，而持續時間一律為0。

</dd> <dt>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**間隔** (3) 


</dt> <dd>

指出度量會套用至時間間隔。 在對應的 BaseMetricValue 實例上，TimeStamp 會指定時間間隔的結束時間，並指定其持續時間。

</dd> <dt>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4) 


</dt> <dd>

表示計量會套用至開始測量資源 (（也就是 MetricDefForMe) 相關聯的 ManagedElement）啟動的時間間隔。 在對應的 BaseMetricValue 實例上，TimeStamp 會指定時間間隔的結束時間。 如果持續時間為0，這表示測量的資源的啟動時間是未知的。 否則，Duration 會指定資源和時間戳記啟動之間的持續時間。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** (5. 32767) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) 


</dt> <dd></dd> </dl>

</dd> <dt>

**單位**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

度量的單位。 範例包括位元組、封包、作業、檔案、毫秒和安培。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ ManagedElement**](cim-managedelement.md)
</dt> </dl>

 

