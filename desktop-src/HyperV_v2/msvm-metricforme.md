---
description: 此關聯會將 managed 元素連結至為其維護的度量值。
ms.assetid: 89b43736-90ae-49e0-a0ed-7918ddec8558
title: Msvm_MetricForME 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricForME
- Msvm_MetricForME.Antecedent
- Msvm_MetricForME.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c483cc5ab6c2b3a9fea572a9de100dccd692334500c9851e735496edcdbdf6ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117811526"
---
# <a name="msvm_metricforme-class"></a>Msvm \_ MetricForME 類別

此關聯會將 managed 元素連結至為其維護的度量值。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricForME : CIM_MetricForME
{
  CIM_ManagedElement  REF Antecedent;
  CIM_BaseMetricValue REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm \_ MetricForME** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ MetricForME** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

[**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)類別之實例的參考，該類別表示具有由 **相依** 維護的計量所定義之計量的 managed 元素。 這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： * * * * CIM \_ BaseMetricValue * * * *
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**CIM \_ BaseMetricValue** 類別實例的參考，表示之前為它 **收集的度量**。 這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

