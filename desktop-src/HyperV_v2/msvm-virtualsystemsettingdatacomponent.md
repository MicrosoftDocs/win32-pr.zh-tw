---
description: 泛型關聯，用來建立一個 CIM \_ VirtualSystemSettingData 實例與一或多個 cim ResourceAllocationSettingData 實例之間的關聯性部分 \_ 。
ms.assetid: 936B41E7-1B3B-4A7B-86F0-E2F4497CE610
title: Msvm_VirtualSystemSettingDataComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingDataComponent
- Msvm_VirtualSystemSettingDataComponent.GroupComponent
- Msvm_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfff3981d6fdb9fdb0368fa887c559026fc10af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971355"
---
# <a name="msvm_virtualsystemsettingdatacomponent-class"></a>Msvm \_ VirtualSystemSettingDataComponent 類別

泛型關聯，用來建立一個 [**cim \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) 實例與一或多個 [**cim \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)實例之間的「部分」關聯性。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingDataComponent : CIM_VirtualSystemSettingDataComponent
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualSystemSettingDataComponent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VirtualSystemSettingDataComponent** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 **寫**、 **最小** (1) 、 **最大** (1) 
</dt> </dl>

關聯中的父元素。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85))。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

關聯中的子項目。 這個屬性繼承自 [**CIM \_ VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85))。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ VirtualSystemSettingDataComponent** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ VirtualSystemSettingDataComponent**](cim-virtualsystemsettingdatacomponent.md)
</dt> <dt>

[**CIM \_ VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85))
</dt> <dt>

[虛擬系統類別](virtual-system-classes.md)
</dt> </dl>

 

