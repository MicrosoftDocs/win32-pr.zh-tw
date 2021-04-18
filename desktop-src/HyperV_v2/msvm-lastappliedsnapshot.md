---
description: 代表虛擬系統與最近套用至虛擬系統之快照集的設定資料之間的關聯。
ms.assetid: 9231b441-20c4-468b-905f-5baabc32a8cc
title: Msvm_LastAppliedSnapshot 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LastAppliedSnapshot
- Msvm_LastAppliedSnapshot.Antecedent
- Msvm_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 48854d7b5aaaa6f8026f8dec14745545b0c58806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983486"
---
# <a name="msvm_lastappliedsnapshot-class"></a>Msvm \_ LastAppliedSnapshot 類別

代表虛擬系統與最近套用至虛擬系統之快照集的設定資料之間的關聯。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LastAppliedSnapshot : CIM_LastAppliedSnapshot
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm \_ LastAppliedSnapshot** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ LastAppliedSnapshot** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ VirtualSystemSettingData**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 **寫**、 **最小** ( 0 ) 、 **最大** ( 1 ) 
</dt> </dl>

參考 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) 類別的實例，該類別代表上次套用至虛擬系統的虛擬系統快照。 這個屬性繼承自 **CIM 相依 \_** 性。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_** 未執行
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 **寫**、 **最小** ( 0 ) 、 **最大** ( 1 ) 
</dt> </dl>

參考 [**Msvm \_**](msvm-computersystem.md) 實例類別的實例，此類別代表最近套用了 **先前** 屬性所代表之虛擬系統快照集的虛擬系統。 這個屬性繼承自 **CIM 相依 \_** 性。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




