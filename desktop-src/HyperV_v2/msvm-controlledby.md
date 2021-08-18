---
description: 將存放裝置與擁有裝置的儲存控制器產生關聯。
ms.assetid: 3DE05EDC-C54A-4C3C-9057-4418246037D5
title: Msvm_ControlledBy 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ControlledBy
- Msvm_ControlledBy.NegotiatedSpeed
- Msvm_ControlledBy.NegotiatedDataWidth
- Msvm_ControlledBy.Antecedent
- Msvm_ControlledBy.Dependent
- Msvm_ControlledBy.AccessState
- Msvm_ControlledBy.TimeOfDeviceReset
- Msvm_ControlledBy.NumberOfHardResets
- Msvm_ControlledBy.NumberOfSoftResets
- Msvm_ControlledBy.DeviceNumber
- Msvm_ControlledBy.AccessMode
- Msvm_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b08cf97c54363009e839ea78fe139c6c8a1bdd81cac07182d019d3d00857dee4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130598"
---
# <a name="msvm_controlledby-class"></a>Msvm \_ ControlledBy 類別

將存放裝置與擁有裝置的儲存控制器產生關聯。 此關聯會與 IDE 和磁碟控制卡一起使用。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ControlledBy : CIM_ControlledBy
{
  uint64                NegotiatedSpeed = 0;
  uint32                NegotiatedDataWidth = 0;
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState = 1;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode = 2;
  uint16                AccessPriority = 0;
};
```

## <a name="members"></a>成員

**Msvm \_ ControlledBy** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ ControlledBy** 類別具有這些屬性。

<dl> <dt>

**AccessMode**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

透過前一個控制器存取裝置的功能。 這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)，而且一律設定為 2 (讀取/寫入) 。

</dd> <dt>

**AccessPriority**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

透過此控制器存取裝置所提供的優先權。 最高優先順序的路徑會有最小值。 這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)，而且一律設定為0。

</dd> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出控制器是否正在主動命令或存取裝置。 這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)，而且一律設定為 1 (作用中) 。

</dd> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ 控制器**](/windows/desktop/CIMWin32Prov/cim-controller)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

控制器的參考。 這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

受控制裝置的參考。 這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)。

</dd> <dt>

**DeviceNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

前一個控制器內容中相關聯裝置的位址。 這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)。

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)，而且一律設定為0。

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)，而且一律設定為0。

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)，但不會使用它。

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)，但不會使用它。

</dd> <dt>

**TimeOfDeviceReset**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)，但不會使用它。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ ControlledBy** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dt>

[**CIM \_ ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby)
</dt> <dt>

[儲存體類](storage-classes.md)
</dt> </dl>

 

