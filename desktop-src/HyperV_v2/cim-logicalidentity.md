---
description: 表示兩個 managed 專案之間的泛型關聯，這些元素代表相同基礎實體的不同層面。
ms.assetid: 28d153de-ce9c-4cd3-8995-0d959846be4d
title: 'CIM_LogicalIdentity 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SystemElement
- CIM_LogicalIdentity.SameElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 71382910dc195c0fa6ef2456e1811d66d90a41e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970754"
---
# <a name="cim_logicalidentity-class-hyper-v-management"></a>CIM_LogicalIdentity 類別 (Hyper-v 管理) 

表示兩個 managed 專案之間的泛型關聯，這些元素代表相同基礎實體的不同層面。

## <a name="syntax"></a>語法

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_LogicalIdentity
{
  CIM_ManagedElement REF SystemElement;
  CIM_ManagedElement REF SameElement;
};
```

## <a name="members"></a>成員

**CIM \_ LogicalIdentity** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ LogicalIdentity** 類別具有這些屬性。

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedElement**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

關聯中的第二個方面。

</dd> <dt>

**SystemElement**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedElement**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

關聯中的第一個方面。 在屬性名稱中使用系統不會限制關聯的範圍。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

