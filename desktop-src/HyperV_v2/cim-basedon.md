---
description: 代表較高層級 CIM \_ StorageExtent 物件與較低層級 cim StorageExtent 物件之間的關聯 \_ 。 例如，CIM \_ ProtectedSpaceExtent 物件是 cim \_ PhysicalExtent 物件的一部分。
ms.assetid: 40a88927-981b-4fc4-af5f-be91d9933284
title: 'CIM_BasedOn 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Antecedent
- CIM_BasedOn.Dependent
- CIM_BasedOn.StartingAddress
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47d2e44d1106eba57f4c46c0957662c348c9ca1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847964"
---
# <a name="cim_basedon-class-hyper-v-management"></a>CIM_BasedOn 類別 (Hyper-v 管理) 

代表較高層級 **cim \_ StorageExtent** 物件與較低層級 **cim \_ StorageExtent** 物件之間的關聯。 例如， [**cim \_ ProtectedSpaceExtent**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) 物件是 [**cim \_ PhysicalExtent**](/windows/desktop/CIMWin32Prov/cim-physicalextent) 物件的一部分。

## <a name="syntax"></a>語法

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a>成員

**CIM \_ BasedOn** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ BasedOn** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ StorageExtent**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

較低層級的 **CIM \_ StorageExtent** 物件。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ StorageExtent**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

較高層級的 **CIM \_ StorageExtent** 物件。

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出較低層級儲存體中之位置的位址，較高層級的 **CIM \_ StorageExtent** 物件會結束。 當將非連續的 **CIM \_ StorageExtent** 物件對應至較高層級的群組時，這個屬性會很有用。

</dd> <dt>

**OrderIndex**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用來指定集合中 **CIM \_ BasedOn** 關聯順序的索引，否則為 "0" 表示沒有順序。 **CIM \_** 具有相同相依值的 BasedOn 實例應該在 **OrderIndex** 屬性中放置唯一值。 最小的 **OrderIndex** 值會指定集合的第一個成員。

使用這個屬性的範例是定義3個磁片的 RAID 0 等量陣列。 結果 RAID 陣列是儲存區，相依于描述3個磁片的每個磁片區的儲存區。 從磁片區至 RAID 陣列的每個 **CIM \_ BasedOn** 關聯的 **OrderIndex** 值可以指定為1、2和3，以指出磁片區用來存取 RAID 資料的順序。

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出較低層級儲存體中之位置的位址，會開始較高層級的 **CIM \_ StorageExtent** 物件。

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

 

