---
description: 表示作業與負責建立作業的 managed 元素之間的關聯。
ms.assetid: 1a100c7e-7e17-47dd-b730-c05c5e4dccda
title: Msvm_OwningJobElement 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_OwningJobElement
- Msvm_OwningJobElement.OwningElement
- Msvm_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 144a212a98b6f51b731023b5137b01f1e9d77156bddaaae187ce3f6ff2474efb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520978"
---
# <a name="msvm_owningjobelement-class"></a>Msvm \_ OwningJobElement 類別

表示作業與負責建立作業的 managed 元素之間的關聯。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_OwningJobElement : CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  Msvm_ConcreteJob   REF OwnedElement;
};
```

## <a name="members"></a>成員

**Msvm \_ OwningJobElement** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ OwningJobElement** 類別具有這些屬性。

<dl> <dt>

**OwnedElement**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ ConcreteJob**](msvm-concretejob.md)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

Managed 元素所建立的作業。

</dd> <dt>

**OwningElement**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

負責建立作業的 managed 元素。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

