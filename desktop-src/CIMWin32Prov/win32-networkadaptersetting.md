---
description: Win32 \_ NetworkAdapterSetting 關聯 WMI 類別會建立網路介面卡及其設定的關聯。
ms.assetid: 6fc646c3-05f9-4c92-8598-07ea20fffaca
ms.tgt_platform: multiple
title: Win32_NetworkAdapterSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterSetting
- Win32_NetworkAdapterSetting.Setting
- Win32_NetworkAdapterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c51ef9ed790c902a6a662dc3ebc45df97fa29721
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972147"
---
# <a name="win32_networkadaptersetting-class"></a>Win32 \_ NetworkAdapterSetting 類別

**Win32 \_ NetworkAdapterSetting** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會建立網路介面卡及其設定的關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterSetting : Win32_DeviceSettings
{
  Win32_NetworkAdapterConfiguration REF Setting;
  Win32_NetworkAdapter              REF Element;
};
```

## <a name="members"></a>成員

**Win32 \_ NetworkAdapterSetting** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ NetworkAdapterSetting** 類別具有這些屬性。

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ NetworkAdapter**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Element" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ NetworkAdapter" ) 
</dt> </dl>

[**Win32 \_ NetworkAdapter**](win32-networkadapter.md) ，描述使用特定網路介面卡設定的網路介面卡屬性。

</dd> <dt>

**設定**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ >networkadapterconfiguration**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "設定" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ >networkadapterconfiguration" ) 
</dt> </dl>

[**Win32 \_ >networkadapterconfiguration**](win32-networkadapterconfiguration.md) ，描述網路介面卡上使用的設定。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ NetworkAdapterSetting** 類別衍生自 [**win32 \_ DeviceSettings**](win32-devicesettings.md)。

如需如何使用關聯類別的詳細資訊，請參閱 [語句 associators of](../wmisdk/associators-of-statement.md)。

## <a name="examples"></a>範例

下列 VBScript 範例會使用 **Win32 \_ NetworkAdapterSetting** 來識別區域連接上的 IP 位址。


```VB
strComputer = "."
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colNics = objWMIService.ExecQuery _
    ("Select * From Win32_NetworkAdapter " _
        & "Where NetConnectionID = " & _
        "'Local Area Connection'")
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      ("ASSOCIATORS OF " _
          & "{Win32_NetworkAdapter.DeviceID='" & _
      objNic.DeviceID & "'}" & _
      " WHERE AssocClass=Win32_NetworkAdapterSetting")
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo "IP Address: " &  strIPAddress
        Next
    Next
Next
```



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
</dt> <dt>

[WMI 工作：網路功能](../wmisdk/wmi-tasks--networking.md)
</dt> </dl>

 

 
