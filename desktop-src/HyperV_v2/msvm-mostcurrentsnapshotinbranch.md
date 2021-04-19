---
description: 將代表虛擬系統之 Msvm 系統的實例 \_ 或 Msvm \_ PlannedComputerSystem 類別的實例，與 \_ 代表相依快照集中最新快照集之虛擬系統快照集的 Msvm VirtualSystemSettingData 類別的實例產生關聯。
ms.assetid: EEB9D2C1-C463-4EFE-862F-95E8AD8E1753
title: Msvm_MostCurrentSnapshotInBranch 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MostCurrentSnapshotInBranch
- Msvm_MostCurrentSnapshotInBranch.Antecedent
- Msvm_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3ed0824fd68670245e2c8d09b73733ff23be16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994539"
---
# <a name="msvm_mostcurrentsnapshotinbranch-class"></a>Msvm \_ MostCurrentSnapshotInBranch 類別

將代表虛擬系統之 [**Msvm \_**](msvm-computersystem.md) 系統的實例或 [**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) 類別的實例，與代表相依快照集中最新快照集之虛擬系統快照集的 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 類別的實例產生關聯。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Experimental, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MostCurrentSnapshotInBranch : CIM_MostCurrentSnapshotInBranch
{
  CIM_ComputerSystem            REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm \_ MostCurrentSnapshotInBranch** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ MostCurrentSnapshotInBranch** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_** 未執行](/windows/desktop/CIMWin32Prov/cim-computersystem)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 
</dt> </dl>

代表虛擬系統的 [**Msvm \_**](msvm-computersystem.md) 系統實例或 [**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) 類別之實例的參考。 這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**最小**](/windows/desktop/WmiSdk/standard-qualifiers) (0) 、 [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 
</dt> </dl>

[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)類別之實例的參考，代表在相依快照集中分支中最新快照集的虛擬系統快照。 這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

