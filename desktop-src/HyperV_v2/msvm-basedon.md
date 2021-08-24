---
description: 描述如何從較低層級範圍組合儲存區範圍的關聯。
ms.assetid: 8be9bb2c-ef46-454b-bfc3-0398c64d17b7
title: Msvm_BasedOn 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BasedOn
- Msvm_BasedOn.Antecedent
- Msvm_BasedOn.Dependent
- Msvm_BasedOn.StartingAddress
- Msvm_BasedOn.EndingAddress
- Msvm_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f3f8138fcc06d5e2d100f38b0333dcbfc5e76c61366da686b313a70d40ffa120
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790248"
---
# <a name="msvm_basedon-class"></a>Msvm \_ BasedOn 類別

描述如何從較低層級範圍組合儲存區範圍的關聯。 例如，ProtectedSpaceExtents 是 PhysicalExtents 的一部分，而 VolumeSets 則是從一個或多個實體或 ProtectedSpaceExtents 來組合。 另一個範例是，CacheMemory 可以獨立定義並在 PhysicalElement 中實現，也可以根據 Volatile 或 NonVolatileStorageExtents。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BasedOn : CIM_BasedOn
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a>成員

**Msvm \_ BasedOn** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ BasedOn** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

較低層級的儲存區。 這個屬性繼承自 [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

較高層級的儲存區。 這個屬性繼承自 [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)。

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

結束位址，在較低層級的儲存體中，較高層級的範圍結束。 當將非連續的範圍對應至較高層級的群組時，這個屬性會很有用。 這個屬性繼承自 [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)。

</dd> <dt>

**OrderIndex**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果根據描述如何組合較高層級儲存區的關聯來產生訂單， **OrderIndex** 屬性就會指出這一點。 當訂單存在時，具有相同 **相依** 值 (相同較高層級範圍的實例) 應該會在 **OrderIndex** 屬性中放置唯一值。 最小值表示較低層級範圍集合的第一個成員，而增加值則表示集合的後續成員。 如果沒有已排序的關聯性，則應該指定零值。 使用這個屬性的範例是定義三個磁片的 RAID 0 等量陣列。 結果 RAID 陣列是一個儲存範圍，相依于描述三個磁片的每個磁片區。 從磁片區到 RAID 陣列的每個關聯的 **OrderIndex** ，都可以指定為1、2和3，以指出磁片區用來存取 RAID 資料的順序。 這個屬性繼承自 [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)。

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

從較低層級的儲存體開始，較高層級的範圍開始的起始位址。 這個屬性繼承自 [**CIM \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

