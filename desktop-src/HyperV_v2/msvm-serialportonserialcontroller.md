---
description: 將序列埠與序列控制器產生關聯。
ms.assetid: A07DE787-2600-4C40-9CE2-7D96D6A58E53
title: Msvm_SerialPortOnSerialController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortOnSerialController
- Msvm_SerialPortOnSerialController.Antecedent
- Msvm_SerialPortOnSerialController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ddc5a5c006b92945178f89cf5f4df585f96ed3eaef692b04326878cb0d16520
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107438"
---
# <a name="msvm_serialportonserialcontroller-class"></a>Msvm \_ SerialPortOnSerialController 類別

將序列埠與序列控制器產生關聯。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortOnSerialController : CIM_PortOnDevice
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm \_ SerialPortOnSerialController** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ SerialPortOnSerialController** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

埠所連接的序列控制器。 這個屬性繼承自 [**CIM \_ PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

序列控制器的通訊埠。 這個屬性繼承自 [**CIM \_ PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ SerialPortOnSerialController** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**CIM \_ PortOnDevice**](cim-portondevice.md)
</dt> <dt>

[**CIM \_ PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)
</dt> <dt>

[序列裝置類別](serial-devices-classes.md)
</dt> </dl>

 

