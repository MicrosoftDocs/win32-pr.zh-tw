---
description: 表示作業與受管理元素之間的關聯，這些專案可能會受其執行影響。
ms.assetid: 81849DE4-9039-426F-B7B1-45BB31A9132C
title: Msvm_AffectedStorageJobElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedStorageJobElement
- Msvm_AffectedStorageJobElement.AffectedElement
- Msvm_AffectedStorageJobElement.AffectingElement
- Msvm_AffectedStorageJobElement.ElementEffects
- Msvm_AffectedStorageJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d900f42e5022301a08ebeee0036400be3a2f1bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970948"
---
# <a name="msvm_affectedstoragejobelement-class"></a>Msvm \_ AffectedStorageJobElement 類別

表示作業與受管理元素之間的關聯，這些專案可能會受其執行影響。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedStorageJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_StorageJob    REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>成員

**Msvm \_ AffectedStorageJobElement** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ AffectedStorageJobElement** 類別具有這些屬性。

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

受管理的元素受工作的執行影響。 這個屬性繼承自 [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))。

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ get-storagejob**](msvm-storagejob.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**OVERRIDE**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ AffectedJobElement. AffectingElement" ) 
</dt> </dl>

影響受影響元素的作業。 這個屬性繼承自 [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))。

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述 managed 元素效果的列舉。 這個陣列對應于 **OtherElementEffectsDescriptions** 屬性陣列，後者會提供與這個屬性所列舉之高階效果相關的詳細資料。 如果 **ElementEffects** 屬性陣列包含值1， (其他) ，則需要額外的詳細資料。 這個屬性繼承自 [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))。

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**專屬用途** (2) 
</dt> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**效能影響** (3) 
</dt> <dt>

<span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**元素完整性** (4 ) 
</dt> </dl>

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在 **ElementEffects** 屬性陣列中的對應陣列位置提供效果的詳細資料。 只要 **ElementEffects** 屬性陣列中的對應元素包含值 1 (其他) ，就需要這項資訊。 這個屬性繼承自 [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ AffectedStorageJobElement** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[儲存類別](storage-classes.md)
</dt> </dl>

 

