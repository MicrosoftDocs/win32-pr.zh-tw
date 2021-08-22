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
ms.openlocfilehash: 12ee48b85ae11b10a24bab35001baa45c8382105158050d110eb7448a8e883e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148361"
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
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ LogicalIdentity**](cim-logicalidentity.md)
</dt> <dt>

[**CIM \_ LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity)
</dt> </dl>

 

