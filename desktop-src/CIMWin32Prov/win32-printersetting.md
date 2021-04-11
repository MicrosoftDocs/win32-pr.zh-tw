---
description: Win32 \_ PrinterSetting 關聯 WMI 類別會建立印表機與其設定的關聯性。
ms.assetid: 5d0f0724-0583-449b-a6da-336e7c8e526e
ms.tgt_platform: multiple
title: Win32_PrinterSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterSetting
- Win32_PrinterSetting.Setting
- Win32_PrinterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90a77678e61b755550ebb1818c34ccdc3159a88c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187729"
---
# <a name="win32_printersetting-class"></a>Win32 \_ PrinterSetting 類別

**Win32 \_ PrinterSetting** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會建立印表機與其設定的關聯性。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class Win32_PrinterSetting : Win32_DeviceSettings
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a>成員

**Win32 \_ PrinterSetting** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ PrinterSetting** 類別具有這些屬性。

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ LogicalDevice**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "cim \| cim \_ LogicalDevice" ) 
</dt> </dl>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，代表可套用設定的邏輯裝置屬性。

這個屬性繼承自 [**Win32 \_ DeviceSettings**](win32-devicesettings.md)。

</dd> <dt>

**設定**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ 設定**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "cim \| cim \_ 設定" ) 
</dt> </dl>

[**CIM \_ 設定**](cim-setting.md)，代表可以套用至邏輯裝置的設定。

這個屬性繼承自 [**Win32 \_ DeviceSettings**](win32-devicesettings.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ PrinterSetting** 類別衍生自 [**win32 \_ DeviceSettings**](win32-devicesettings.md)。

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

[**Win32 \_ DeviceSettings**](win32-devicesettings.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

 
