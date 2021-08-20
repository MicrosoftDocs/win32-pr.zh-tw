---
description: 建立 &\# 0034;&\# 0034 的一部分; 系統與其組成之任何 managed 系統專案之間的關聯性。
ms.assetid: 6BF72E36-9B6C-4853-A553-DDAF65991C86
title: Msvm_SystemComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemComponent
- Msvm_SystemComponent.GroupComponent
- Msvm_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 538deaff8e0edf3d1467c4447a3d25ced18987e4f81bc8d14a056848313c8526
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949680"
---
# <a name="msvm_systemcomponent-class"></a>Msvm \_ SystemComponent 類別

建立系統與其組成之任何 managed 系統專案之間的「部分」關聯性。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), Association, Aggregation]
class Msvm_SystemComponent : CIM_SystemComponent
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>成員

**Msvm \_ SystemComponent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ SystemComponent** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ 系統**](/windows/desktop/CIMWin32Prov/cim-system)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

關聯中的父元素。 這個屬性繼承自 [**CIM \_ SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent)。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

關聯中的子項目。 這個屬性繼承自 [**CIM \_ SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

