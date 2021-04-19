---
description: Msvm \_ VirtualSystemSettingData 實例與 Msvm VirtualSystemSettingData 實例之間的關聯 \_ ，代表這個物件所依據的最新快照集。
ms.assetid: F779775B-9AB3-4495-B6FF-9985FCDF63E4
title: Msvm_ParentChildSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentChildSettingData
- Msvm_ParentChildSettingData.Antecedent
- Msvm_ParentChildSettingData.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 083de5f5d162f32fc9499a67b2ec991c6d3b398a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000186"
---
# <a name="msvm_parentchildsettingdata-class"></a>Msvm \_ ParentChildSettingData 類別

[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)實例與 **Msvm \_ VirtualSystemSettingData** 實例之間的關聯，代表這個物件所依據的最新快照集。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentChildSettingData : CIM_Dependency
{
  Msvm_VirtualSystemSettingData REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm \_ ParentChildSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ ParentChildSettingData** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性 \_ 。前面」 ) 
</dt> </dl>

子設定資料所依據的快照集設定資料。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性依存」 \_ ) 
</dt> </dl>

虛擬機器的設定資料，代表父系的子系。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ ParentChildSettingData** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**CIM \_ 相依性**](cim-dependency.md)
</dt> <dt>

[**CIM \_ 相依性**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> <dt>

[虛擬系統類別](virtual-system-classes.md)
</dt> </dl>

 

