---
description: Win32 \_ SerialPortSetting 關聯 WMI 類別會建立序列埠及其設定的關聯。
ms.assetid: 57856207-abe5-4d93-9a34-acfe30ccd80c
ms.tgt_platform: multiple
title: Win32_SerialPortSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortSetting
- Win32_SerialPortSetting.Setting
- Win32_SerialPortSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 713cdb57b5ed7135529959d3c17f7453924ce1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936107"
---
# <a name="win32_serialportsetting-class"></a>Win32 \_ SerialPortSetting 類別

**Win32 \_ SerialPortSetting** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會建立序列埠及其設定的關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortSetting : Win32_DeviceSettings
{
  Win32_SerialPortConfiguration REF Setting;
  Win32_SerialPort              REF Element;
};
```

## <a name="members"></a>成員

**Win32 \_ SerialPortSetting** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ SerialPortSetting** 類別具有這些屬性。

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ SerialPort**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Element" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ SerialPort" ) 
</dt> </dl>

[**Win32 \_ SerialPort**](win32-serialport.md) ，包含電腦系統上序列埠的屬性。

</dd> <dt>

**設定**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ SerialPortConfiguration**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "設定" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ SerialPortConfiguration" ) 
</dt> </dl>

包含序列埠設定的 [**Win32 \_ SerialPortConfiguration**](win32-serialportconfiguration.md) 。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ SerialPortSetting** 類別衍生自 [**win32 \_ DeviceSettings**](win32-devicesettings.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ DeviceSettings**](win32-devicesettings.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

 
