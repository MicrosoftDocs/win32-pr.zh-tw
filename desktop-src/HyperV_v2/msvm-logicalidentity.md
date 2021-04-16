---
description: 將兩個代表相同基礎實體不同層面的 managed 專案產生關聯。
ms.assetid: 107A2B15-09F2-490A-8AB2-F9FE5F6FEE60
title: Msvm_LogicalIdentity 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalIdentity
- Msvm_LogicalIdentity.SameElement
- Msvm_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2f8d2ee522fde3769c08bcbb78611b99eed8e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513360"
---
# <a name="msvm_logicalidentity-class"></a>Msvm \_ LogicalIdentity 類別

將兩個代表相同基礎實體不同層面的 managed 專案產生關聯。 此類別衍生自 [**CIM \_ LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity)。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalIdentity : CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a>成員

**Msvm \_ LogicalIdentity** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ LogicalIdentity** 類別具有這些屬性。

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ LogicalElement**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

系統實體替代層面的參考。

</dd> <dt>

**SystemElement**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ LogicalElement**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

邏輯元素的一個層面參考。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ LogicalIdentity**](cim-logicalidentity.md)
</dt> <dt>

[**CIM \_ LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity)
</dt> </dl>

 

