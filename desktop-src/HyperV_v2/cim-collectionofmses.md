---
description: 子類別的抽象類別，代表 CIM \_ ManagedSystemElement 物件的集合。 這些集合允許將 managed 系統專案分組以進行識別，以及簡化設定和設定的關聯。
ms.assetid: f47bf1d6-6d89-4d9f-82d1-99a7343481bc
title: 'CIM_CollectionOfMSEs 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.CollectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e467e775c78364718f25cc732d6689d9fb2b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848793"
---
# <a name="cim_collectionofmses-class-hyper-v-management"></a>CIM_CollectionOfMSEs 類別 (Hyper-v 管理) 

子類別的抽象類別，代表 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) 物件的集合。 這些集合允許將 managed 系統專案分組以進行識別，以及簡化設定和設定的關聯。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectionOfMSEs : CIM_Collection
{
  string CollectionID;
};
```

## <a name="members"></a>成員

**CIM \_ CollectionOfMSEs** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ CollectionOfMSEs** 類別具有這些屬性。

<dl> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

集合物件的識別。 子類別化時， **CollectionID** 屬性可以覆寫為索引鍵屬性。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 集合**](cim-collection.md)
</dt> </dl>

 

