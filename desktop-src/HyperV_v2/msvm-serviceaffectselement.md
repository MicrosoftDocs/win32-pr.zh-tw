---
description: 將虛擬機器實例與控制其狀態的管理服務產生關聯。
ms.assetid: 12EB3951-74D4-477F-8B55-69FAA3B14631
title: Msvm_ServiceAffectsElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceAffectsElement
- Msvm_ServiceAffectsElement.AffectedElement
- Msvm_ServiceAffectsElement.AffectingElement
- Msvm_ServiceAffectsElement.ElementEffects
- Msvm_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: db9ab0ff0aa3eab6f0268f7e85cb5f4efd0e7d2624c7e97a95abb3dd3b414ab2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582278"
---
# <a name="msvm_serviceaffectselement-class"></a>Msvm \_ ServiceAffectsElement 類別

將虛擬機器實例與控制其狀態的管理服務產生關聯。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceAffectsElement : CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[] = 5;
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>成員

**Msvm \_ ServiceAffectsElement** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ ServiceAffectsElement** 類別具有這些屬性。

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器的參考。 這個屬性繼承自 [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))。

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

控制虛擬機器的服務參考。 這個屬性繼承自 [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))。

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定關聯表示的控制項類型。 這個屬性繼承自 [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))，而且一律設定為下列值。



| 值                                                                        | 意義            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>5</dt> </dl> | 管理<br/> |



 

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**ElementAffects** 屬性陣列中對應陣列位置的關聯類型詳細資料。 如果 **ElementAffects** 設定為 1 (其他) ，則需要這項資訊。 這個屬性繼承自 [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))，而且一律設定為 **Null**。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ ServiceAffectsElement** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ ServiceAffectsElement**](cim-serviceaffectselement.md)
</dt> <dt>

[**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))
</dt> </dl>

 

