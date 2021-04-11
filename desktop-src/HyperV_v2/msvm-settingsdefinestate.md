---
description: 將虛擬機器及其裝置與 CIM SettingData 的實例產生關聯 \_ ，以代表適用于這些物件的目前設定。
ms.assetid: 991FE773-1F87-4D5E-89E6-CB1A33989B1A
title: Msvm_SettingsDefineState 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineState
- Msvm_SettingsDefineState.ManagedElement
- Msvm_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f104943be80df696b58c9d5d6eaad4c430362338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193508"
---
# <a name="msvm_settingsdefinestate-class"></a>Msvm \_ SettingsDefineState 類別

將虛擬機器及其裝置與 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) 的實例產生關聯，以代表適用于這些物件的目前設定。 更明確地說，它會將 Msvm 的程式設計與 [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)的實例產生關聯，並將 **Msvm \_ \** _ 衍生的 [_ *cim \_ LogicalDevice* *](/windows/desktop/CIMWin32Prov/cim-logicaldevice)與 **Msvm \_ \** _ 衍生的 [_ *cim \_ ResourceAllocationSettingData* *](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)產生關聯。 [**\_**](msvm-computersystem.md)

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_SettingsDefineState : CIM_SettingsDefineState
{
  Msvm_ComputerSystem           REF ManagedElement;
  Msvm_VirtualSystemSettingData REF SettingData;
};
```

## <a name="members"></a>成員

**Msvm \_ SettingsDefineState** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ SettingsDefineState** 類別具有這些屬性。

<dl> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_**](msvm-computersystem.md)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器的參考。

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬機器目前使用中設定的參考。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ SettingsDefineState** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**CIM \_ SettingsDefineState**](cim-settingsdefinestate.md)
</dt> <dt>

[**CIM \_ SettingsDefineState**](/previous-versions/windows/desktop/clushyperv/cim-settingsdefinestate)
</dt> <dt>

[虛擬系統管理類別](virtual-system-management-classes.md)
</dt> </dl>

 

