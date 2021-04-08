---
description: 當虛擬機器在 VM 電腦系統上執行時， (VM)  (的相容性資訊，) 或在主機電腦系統上執行 (時的主機) 。
ms.assetid: A3DB75BF-91C8-444E-B273-25DF8A5BFA7B
title: Msvm_CompatibilityVector 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CompatibilityVector
- Msvm_CompatibilityVector.VectorId
- Msvm_CompatibilityVector.CompareOperation
- Msvm_CompatibilityVector.CompatibilityInfo
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66eba92daf420fb4bd332d3f7d537b7936618ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850296"
---
# <a name="msvm_compatibilityvector-class"></a>Msvm \_ CompatibilityVector 類別

當虛擬機器在 VM 電腦系統上執行時， (VM)  (的相容性資訊，) 或在主機電腦系統上執行 (時的主機) 。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CompatibilityVector
{
  uint32 VectorId;
  uint32 CompareOperation;
  uint64 CompatibilityInfo;
};
```

## <a name="members"></a>成員

**Msvm \_ CompatibilityVector** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ CompatibilityVector** 類別具有這些屬性。

<dl> <dt>

**CompareOperation**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別只有當兩個向量相容時，才會傳回 true 的比較運算。 VM 的資料位於比較的左側，而該主機的資料位於右邊的位置。

<dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>

**等於** (0) 


</dt> <dd></dd> <dt>

<span id="Superset"></span><span id="superset"></span><span id="SUPERSET"></span>

**超集合** (1) 


</dt> <dd></dd> <dt>

<span id="Subset"></span><span id="subset"></span><span id="SUBSET"></span>

**子集** (2) 


</dt> <dd></dd> <dt>

<span id="Disjoint"></span><span id="disjoint"></span><span id="DISJOINT"></span>

無 **交集** 的 (3) 


</dt> <dd></dd> <dt>

<span id="GreaterThan"></span><span id="greaterthan"></span><span id="GREATERTHAN"></span>

**GreaterThan** (4) 


</dt> <dd></dd> <dt>

<span id="GreaterThanOrEqual"></span><span id="greaterthanorequal"></span><span id="GREATERTHANOREQUAL"></span>

**GreaterThanOrEqual** (5) 


</dt> <dd></dd> <dt>

<span id="LessThan"></span><span id="lessthan"></span><span id="LESSTHAN"></span>

**LessThan** (6) 


</dt> <dd></dd> <dt>

<span id="LessThanOrEqual"></span><span id="lessthanorequal"></span><span id="LESSTHANOREQUAL"></span>

**LessThanOrEqual** (7) 


</dt> <dd></dd> <dt>

<span id="Multiple"></span><span id="multiple"></span><span id="MULTIPLE"></span>

**多** (8) 


</dt> <dd></dd> <dt>

<span id="Divisible"></span><span id="divisible"></span><span id="DIVISIBLE"></span>

 (9) **整除**


</dt> <dd></dd> </dl>

</dd> <dt>

**CompatibilityInfo**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用於比較的實際相容性屬性資料。

</dd> <dt>

**VectorId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別表示特定屬性的相容性向量。 這個屬性是用來比對主機和 VM 之間的對應向量。

</dd> </dl>

## <a name="remarks"></a>備註

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)類別的 [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)方法會傳回主機 (的 **Msvm \_ CompatibilityVector** 實例陣列，如果在主機) 上執行，或在 vm) 上執行，則為 vm (。 清單中的每個 **Msvm \_ CompatibilityVector** 專案都會描述相容性屬性向量。 若要讓 VM 與主機相容，其所有相容性屬性都必須與主機的屬性相容。

每個 **Msvm \_ CompatibilityVector** 專案都有下列屬性：

<dl> <dt>

**VectorId**
</dt> <dd>

唯一識別相容性向量。 這是用來比對向量，以在主機和 VM 之間進行比較。

</dd> <dt>

**CompareOperation**
</dt> <dd>

識別判斷向量是否相容的比較運算。

</dd> <dt>

**CompatibilityInfo**
</dt> <dd>

包含實際的相容性屬性;這實際上是屬性承載 (例如處理器功能遮罩、快取行排清大小等等 ) 

</dd> </dl>

針對 **CompareOperation** 所定義的作業集合只涉及基本的整數比較和位邏輯。 這可讓 **CompatibilityInfo** 的實際內容保持不變。 作業集包括：



| CompareOperation | Description                                      | 虛擬虛擬的比較                |
|------------------|--------------------------------------------------|--------------------------------------|
| VmCcEqual        | VmAttr 必須等於 HostAttr                       | 如果 (VmAttr = = HostAttr)               |
| VmCcSuperSet     | VmAttr 必須是 HostAttr 的超集合            | 如果 ( (VmAttr & HostAttr) = = HostAttr)  |
| VmCcSubSet       | VmAttr 必須是 HostAttr 的子集              | 如果 ( (VmAttr & HostAttr) = = VmAttr)    |
| VmCcDisjointSet  | VmAttr 必須是 HostAttr 中的斷續集合      | 如果 ( (VmAttr & HostAttr) = = 0)         |
| VmCcGreater      | VmAttr 必須大於 HostAttr             | 如果 (VmAttr > HostAttr)             |
| VmCcGreaterEqual | VmAttr 必須大於或等於 HostAttr | 如果 (VmAttr >= HostAttr)            |
| VmCcLess         | VmAttr 必須小於 HostAttr                | 如果 (VmAttr < HostAttr)             |
| VmCcLessEqual    | VmAttr 必須小於或等於 HostAttr    | 如果 (VmAttr <= HostAttr)            |
| VmCcMultiple     | VmAttr 必須是 HostAttr 的倍數            | 如果 ( (VmAttr% HostAttr) = = 0)         |
| VmCcDivisor      | VmAttr 必須是 HostAttr 的除數             | 如果 ( (HostAttr% VmAttr) = = 0)         |



 

SCVMM 必須執行下列步驟，以判斷 VM 是否與主機相容。

**判斷 VM 是否與主機相容**

1.  逐一查看 VM 的所有 **Msvm \_ CompatibilityVector** 元素。
2.  針對每個 **Msvm \_ CompatibilityVector** 專案，使用在 **CompareOperation** 中指定的相容性作業，將 VM 的硬體相容性向量與主機的對應相容性向量進行比較。
3.  如果 VM 中的所有 **Msvm \_ CompatibilityVector** 元素都被視為相容，則 vm 與主機 (相容) 的處理器功能觀點。

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

[**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




