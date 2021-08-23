---
description: 定義 Msvm \_ BaseMetricDefinition 與 CIM ManagedElement 之間的關聯， \_ 以定義後者的度量。 計量定義是由 ManagedElement 提供的內容，這就是定義相依于元素的原因。
ms.assetid: 528d9b1a-089d-48ae-b5a6-40bc9d09191c
title: Msvm_MetricDefForME 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricDefForME
- Msvm_MetricDefForME.Antecedent
- Msvm_MetricDefForME.Dependent
- Msvm_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c6da093c5f902657c51285e124593e0bf44a9be0bf32ed87a55d3349cbfba92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521598"
---
# <a name="msvm_metricdefforme-class"></a>Msvm \_ MetricDefForME 類別

定義 [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) 與 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) 之間的關聯，以定義後者的度量。 計量定義是由 ManagedElement 提供的內容，這就是定義相依于元素的原因。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricDefForME : CIM_MetricDefForME
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a>成員

**Msvm \_ MetricDefForME** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ MetricDefForME** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

[**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)類別之實例的參考，該類別代表可以套用 **相依的相依** 型別度量的 managed 元素。 這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

[**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)類別實例的參考，該類別代表前 **一個可套用到它的度量** 定義。 這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。

</dd> <dt>

**MetricCollectionEnabled**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否正在為 **Antecedent** 收集 **相依** 的度量。 這會是下列其中一個值。



| 值                                                                                                                                                                                                                                                               | 意義                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**已啟用**</dt> <dt>2</dt> </dl>                                         | 正在收集度量。<br/>                                |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**停用**</dt> <dt>3</dt> </dl>                                     | 未收集度量。<br/>                            |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <dt>**保留**</dt> <dt>4</dt> </dl>                                     |                                                                          |
| <span id="PartiallyEnabled"></span><span id="partiallyenabled"></span><span id="PARTIALLYENABLED"></span><dl> <dt>**PartiallyEnabled**</dt> <dt>32768</dt> </dl> | 系統會針對部分（而非全部）裝置收集度量。<br/> |



 

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

