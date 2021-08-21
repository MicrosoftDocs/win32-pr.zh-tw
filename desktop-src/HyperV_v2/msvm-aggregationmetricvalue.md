---
description: 表示 Msvm AggregationMetricDefinition 類別的實例所定義之度量的實例值 \_ 。
ms.assetid: 6dfcb711-6137-492a-aff4-82facbd11949
title: Msvm_AggregationMetricValue 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricValue
- Msvm_AggregationMetricValue.InstanceID
- Msvm_AggregationMetricValue.Caption
- Msvm_AggregationMetricValue.Description
- Msvm_AggregationMetricValue.ElementName
- Msvm_AggregationMetricValue.MetricDefinitionId
- Msvm_AggregationMetricValue.MeasuredElementName
- Msvm_AggregationMetricValue.TimeStamp
- Msvm_AggregationMetricValue.Duration
- Msvm_AggregationMetricValue.MetricValue
- Msvm_AggregationMetricValue.BreakdownDimension
- Msvm_AggregationMetricValue.BreakdownValue
- Msvm_AggregationMetricValue.Volatile
- Msvm_AggregationMetricValue.AggregationTimeStamp
- Msvm_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 512ed39ea86bad6c1cb89bdf6ace7d528a6605b378a8c026b889be655f5c0a70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149308"
---
# <a name="msvm_aggregationmetricvalue-class"></a>Msvm \_ AggregationMetricValue 類別

表示 [**Msvm \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) 類別的實例所定義之度量的實例值。 繼承自 [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) 的屬性會提供實際的度量值。 這個類別所定義的屬性會提供套用彙總函式的間隔相關資訊。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricValue : CIM_AggregationMetricValue
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a>成員

**Msvm \_ AggregationMetricValue** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ AggregationMetricValue** 類別具有這些屬性。

<dl> <dt>

**AggregationDuration**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

代表計算匯總的持續時間。 套用彙總函式的監視間隔開始時間，是藉由從 **AggregationTimeStamp** 減去 **AggregationDuration** 來決定。 這個屬性繼承自 **CIM \_ AggregationMetricValue**。

</dd> <dt>

**AggregationTimeStamp**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別套用彙總函式以判斷度量實例值的時間。 這與建立實例的時間不同。 針對指定的 **CIM \_ AggregationMetricValue** 實例，每當套用彙總函式來計算值時， **AggregationTimeStamp** 就會變更。 這個屬性繼承自 **CIM \_ AggregationMetricValue**。

</dd> <dt>

**BreakdownDimension**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

從關聯的 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md)中定義的 **BreakdownDimensions** 陣列指定一個細目維度。 這是用來細分這組度量值的維度。 這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**BreakdownValue**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

定義為此度量值實例定義之 **BreakdownDimension** 屬性的值。 例如，如果 **BreakdownDimension** 是 "TransactionName"，則此屬性可以命名套用此特定度量值的實際交易。 這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**有效期間**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定此度量值有效的持續時間。 這個屬性不應該存在於只套用至某個時間點的時間戳記，但應針對在特定 (期間內視為有效的值指定（例如，取樣) ）。 如果 **Duration** 屬性存在，而且不是 **Null**， **TimeStamp** 屬性會指定間隔的結尾。 這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

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

**MeasuredElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

度量值所屬專案的描述性名稱， (已測量的元素) 。 這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此值之 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) 實例的索引鍵。 這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**MetricValue**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

以字串表示的度量值。 這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**時間 戳**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定捕獲或計算度量值的時間。 請注意，這與建立實例的時間不同。 這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**揮發 性**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果下一個時間點的值將使用相同的類別實例，而且只是變更屬性值 (例如 **值** 或 **時間戳記**) ，**則為 True** 。 若 **為 True**，則會重複使用此實例。 如果 **為 False**，則現有的實例會維持不變，並為新的時間點建立新的實例。 這個屬性繼承自 [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

