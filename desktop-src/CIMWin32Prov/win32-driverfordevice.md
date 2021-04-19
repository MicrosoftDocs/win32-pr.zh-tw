---
description: Win32 \_ DriverForDevice 關聯 WMI 類別會建立印表機實例與印表機驅動程式實例的關聯。
ms.assetid: 56ff74b2-31ba-4d8e-b389-9f962932aa03
ms.tgt_platform: multiple
title: Win32_DriverForDevice 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DriverForDevice
- Win32_DriverForDevice.Antecedent
- Win32_DriverForDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5fb384eed80c6a614af448477c50be3204d3080
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973396"
---
# <a name="win32_driverfordevice-class"></a>Win32 \_ DriverForDevice 類別

**Win32 \_ DriverForDevice** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會建立印表機實例與印表機驅動程式實例的關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class Win32_DriverForDevice : CIM_Dependency
{
  Win32_Printer       REF Antecedent;
  Win32_PrinterDriver REF Dependent;
};
```

## <a name="members"></a>成員

**Win32 \_ DriverForDevice** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ DriverForDevice** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ 印表機**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

參考代表印表機的 [**Win32 \_ 印表機**](win32-printer.md) 實例。

這個屬性繼承自 [**CIM 相依 \_**](cim-dependency.md)性。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ PrinterDriver**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

參考代表印表機印表機驅動程式的 [**Win32 \_ PrinterDriver**](win32-printerdriver.md) 實例。

這個屬性繼承自 [**CIM 相依 \_**](cim-dependency.md)性。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ DriverForDevice** 類別衍生自 CIM 相依 [**性 \_**](cim-dependency.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ 印表機。 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

