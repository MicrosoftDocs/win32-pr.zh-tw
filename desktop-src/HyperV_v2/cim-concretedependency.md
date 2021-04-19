---
description: 代表 managed 元素相依于另一個的泛型關聯。 CIM \_ ConcreteDependency 子類別 cim 相依性 \_ ，以提供實體類別版本的 cim 相依性 \_ 。
ms.assetid: c0e1527d-d350-410d-9b5f-c9d4dedf7393
title: CIM_ConcreteDependency 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteDependency
- CIM_ConcreteDependency.Antecedent
- CIM_ConcreteDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 253f57b1fd29c3844f0e87d488974ced7bec98bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997852"
---
# <a name="cim_concretedependency-class"></a>CIM \_ ConcreteDependency 類別

代表 managed 元素相依于另一個的泛型關聯。 **CIM \_ConcreteDependency** 子類別 cim 相依性，以提供實體類別版本的 [**\_**](cim-dependency.md) cim 相依性。 **\_**

## <a name="syntax"></a>語法

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a>成員

**CIM \_ ConcreteDependency** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ConcreteDependency** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedElement**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

關聯中的獨立物件。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ManagedElement**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

關聯中的相依物件。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 相依性**](cim-dependency.md)
</dt> </dl>

 

