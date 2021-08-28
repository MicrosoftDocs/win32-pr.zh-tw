---
description: 將 Msvm \_ BootSourceSettingData 與整體 Msvm VirtualSystemSettingData 建立關聯 \_ 。
ms.assetid: DB2E66F1-CC2C-49FC-96CE-D9DE441AA809
title: Msvm_BootSourceComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceComponent
- Msvm_BootSourceComponent.GroupComponent
- Msvm_BootSourceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44b4b1bb6908a304ddef67d4988069c6fa018235c2d0488179d87e332f6d45e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252958"
---
# <a name="msvm_bootsourcecomponent-class"></a>Msvm \_ BootSourceComponent 類別

將 [**Msvm \_ BootSourceSettingData**](msvm-bootsourcesettingdata.md) 與整體 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)建立關聯。 此類別衍生自 [**CIM \_ 元件**](/windows/desktop/CIMWin32Prov/cim-component)。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceComponent : CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>成員

**Msvm \_ BootSourceComponent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ BootSourceComponent** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedSystemElement**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

關聯中父元素的參考。 這個屬性繼承自 [**CIM \_ 元件**](cim-component.md)。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedSystemElement**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

關聯中子項目的參考。 這個屬性繼承自 [**CIM \_ 元件**](cim-component.md)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 元件**](cim-component.md)
</dt> <dt>

[**CIM \_ 元件**](/windows/desktop/CIMWin32Prov/cim-component)
</dt> <dt>

[**Msvm \_ BootSourceSettingData**](msvm-bootsourcesettingdata.md)
</dt> <dt>

[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)
</dt> </dl>

 

