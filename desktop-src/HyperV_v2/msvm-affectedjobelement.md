---
description: 表示作業與受管理元素之間的關聯，可能會受到其執行影響。
ms.assetid: 125A4976-A4E3-4D7A-A43B-86045C3B00AE
title: Msvm_AffectedJobElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedJobElement
- Msvm_AffectedJobElement.AffectedElement
- Msvm_AffectedJobElement.AffectingElement
- Msvm_AffectedJobElement.ElementEffects
- Msvm_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bef667872a7afa4c726ee1b2c77a36c29649114d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001412"
---
# <a name="msvm_affectedjobelement-class"></a>Msvm \_ AffectedJobElement 類別

表示作業與受管理元素之間的關聯，可能會受到其執行影響。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_ConcreteJob   REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>成員

**Msvm \_ AffectedJobElement** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ AffectedJobElement** 類別具有這些屬性。

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

受管理的元素受工作的執行影響。 這個屬性繼承自 [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))。

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ ConcreteJob**](msvm-concretejob.md)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

影響受管理元素的作業。 這個屬性繼承自 [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))。

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述 managed 元素效果的列舉。 這個屬性繼承自 [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))。

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供 **ElementEffects** 中對應陣列位置的效果詳細資料。 這個屬性繼承自 [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ AffectedJobElement** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**CIM \_ AffectedJobElement**](cim-affectedjobelement.md)
</dt> <dt>

[**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))
</dt> <dt>

[虛擬系統管理類別](virtual-system-management-classes.md)
</dt> </dl>

 

