---
description: 表示計量值物件與其度量定義之間的關聯。
ms.assetid: 98ad9390-78b4-4c18-b068-d05efa2f1866
title: Msvm_MetricInstance 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricInstance
- Msvm_MetricInstance.Antecedent
- Msvm_MetricInstance.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18a15ff6479caa690a8645e89d9b68f4a15f523bd7cee56fedb6957e20373214
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521538"
---
# <a name="msvm_metricinstance-class"></a>Msvm \_ MetricInstance 類別

表示計量值物件與其度量定義之間的關聯。 此關聯會將 [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) 的實例系結至其 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md)。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricInstance : CIM_MetricInstance
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm \_ MetricInstance** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ MetricInstance** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： * * * * CIM \_ ManagedElement * * * *
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

代表度量定義之 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) 類別實例的參考。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： * * * * CIM \_ ManagedElement * * * *
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

[**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md)類別實例的參考，代表相依于前 **一個的度量。**

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




