---
description: 代表 CIM AggregationMetricDefinition 實例所定義之度量的實例值 \_ 。
ms.assetid: 663ef18a-0238-416f-9682-8809b271b4fc
title: CIM_AggregationMetricValue 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricValue
- CIM_AggregationMetricValue.AggregationTimeStamp
- CIM_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0af264b66838e7c039ef3f99a4f365ebab55c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969315"
---
# <a name="cim_aggregationmetricvalue-class"></a>CIM \_ AggregationMetricValue 類別

代表 **CIM \_ AggregationMetricDefinition** 實例所定義之度量的實例值。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricValue : CIM_BaseMetricValue
{
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a>成員

**CIM \_ AggregationMetricValue** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ AggregationMetricValue** 類別具有這些屬性。

<dl> <dt>

**AggregationDuration**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AggregationMetricValue**.**AggregationTimeStamp**") 
</dt> </dl>

代表計算匯總的持續時間。 套用彙總函式的監視間隔開始時間，是從 **AggregationTimestamp** 值減去 **AggregationDuration** 值來決定。

</dd> <dt>

**AggregationTimeStamp**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ AggregationMetricValue**.**Duration**") 
</dt> </dl>

套用彙總函式以判斷度量實例值的時間。 這與建立實例的時間不同。 每當套用彙總函式來計算值時， **AggregationTimeStamp** 值就會變更。

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

[**CIM \_ BaseMetricValue**](cim-basemetricvalue.md)
</dt> </dl>

 

