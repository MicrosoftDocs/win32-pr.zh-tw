---
description: 表示度量的實例值。
ms.assetid: 6b272ae8-7684-45bb-bff8-6559680cc8b6
title: CIM_BaseMetricValue 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricValue
- CIM_BaseMetricValue.InstanceID
- CIM_BaseMetricValue.MetricDefinitionId
- CIM_BaseMetricValue.MeasuredElementName
- CIM_BaseMetricValue.TimeStamp
- CIM_BaseMetricValue.Duration
- CIM_BaseMetricValue.MetricValue
- CIM_BaseMetricValue.BreakdownDimension
- CIM_BaseMetricValue.BreakdownValue
- CIM_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 107dc3721ee32ca7f51efd563cdd6af14af483a69a5990e0b107a153b79b9351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014696"
---
# <a name="cim_basemetricvalue-class"></a>CIM \_ BaseMetricValue 類別

表示度量的實例值。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricValue : CIM_ManagedElement
{
  string   InstanceID;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
};
```

## <a name="members"></a>成員

**CIM \_ BaseMetricValue** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ BaseMetricValue** 類別具有這些屬性。

<dl> <dt>

**BreakdownDimension**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

根據相關聯之 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md)物件的 **BreakdownDimensions** 屬性，將這組度量值細分為的維度。

</dd> <dt>

**BreakdownValue**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

針對這個實例值所定義之 **BreakdownDimension** 屬性的值。 例如，如果 **BreakdownDimension** 包含 "TransactionName"，則此屬性可以命名套用此特定度量值的實際交易。

</dd> <dt>

**有效期間**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**"，"**CIM \_ BaseMetricValue**.**TimeStamp**") 
</dt> </dl>

此度量值有效的持續時間。 這個屬性不應該存在於只適用于某個時間點的時間戳記，但應針對在特定時間週期內視為有效的值來定義 (例如， 取樣) 。 如果 **Duration** 屬性存在且為非 Null，則 **時間戳記** 值應為間隔的結尾。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "InstanceID" ) 
</dt> </dl>

在包含的命名空間範圍內唯一識別此類別的實例。

> [!IMPORTANT]
>
> 為了確保命名空間中的唯一性， **InstanceID** 屬性的值應該以下列模式來建立： *OrgID*：*LocalID*
>
> *OrgID* 必須包含受著作權、商標或其他唯一名稱（由定義 **InstanceID** 的商務實體所擁有），或是由可辨識的全域授權單位所指派的註冊識別碼。 此模式類似于架構類別名稱的結構。 此外，若要確保唯一性， **InstanceID** 中的第一個冒號必須介於 *OrgID* 和 *LocalID* 之間。 因此， *OrgID* 不能包含冒號 ( '： ' ) 。
>
> *LocalID* 是由商務實體所選擇，不應重新使用以識別不同的基礎現實世界元素。
>
> 如果未使用上述模式，則定義實體必須確保產生的 **instanceid** 值不會重複用於這個提供者所產生之任何 **instanceid** 屬性或這個命名空間的其他提供者。
>
> 若為分散式管理工作強制 (DMTF) 定義的實例，則必須搭配 *OrgID* 設定為 CIM 使用模式。

 

</dd> <dt>

**MeasuredElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

度量測量之元素的描述性名稱。

如果計量定義未與 [**CIM \_ ManagedElement**](cim-managedelement.md) 物件相關聯，而且可在其他情況下用來提供補充資訊，則需要這個屬性。 這可讓您獨立于任何 **CIM \_ ManagedElement** 物件之外捕獲計量。

如果有多個 [**CIM \_ ManagedElement**](cim-managedelement.md) 物件與計量值相關聯，您可以選擇其中一個受控元素來建立度量的補充資訊。 屬性並非用來做為用來查詢測量元素的外鍵。 相反地，應該使用與 **CIM \_ ManagedElement** 的關聯。

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**識別碼**") 
</dt> </dl>

與這個實例值相關聯之 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 實例的索引鍵。

</dd> <dt>

**MetricValue**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**必要**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

度量值的字串表示。 度量值的原始資料類型會在相關聯的 [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) 物件中指定。

</dd> <dt>

**時間 戳**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**"，"**CIM \_ BaseMetricValue**.**Duration**") 
</dt> </dl>

計算度量實例值的時間。 這與建立實例的時間不同。 如果 **Volatile** 屬性為 true，則會在每次建立新的度量快照時變更此值。

管理應用程式可以藉由抓取 **CIM \_ BaseMetricValue** 的實例，並根據其 **時間戳記** 值進行排序，來建立計量資料的時間序列。

</dd> <dt>

**揮發 性**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果每次計量實例的值變更時， **時間戳記** 值變更，則為 True。 如果這個物件必須保持不變，並為新的 **時間戳記** 值建立新的物件，則為 False。

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

 

