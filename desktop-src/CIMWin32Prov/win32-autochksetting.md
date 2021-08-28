---
description: Win32 \_ AUTOCHKSETTING WMI 類別代表磁片之 autocheck 操作的設定。
ms.assetid: 637f4d5d-f2f0-4fe0-bbde-7804156979b7
ms.tgt_platform: multiple
title: Win32_AutochkSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AutochkSetting
- Win32_AutochkSetting.Caption
- Win32_AutochkSetting.Description
- Win32_AutochkSetting.SettingID
- Win32_AutochkSetting.UserInputDelay
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6cccf1877d8812e1fee4816e80189b8404d4090a1ef15f45e840fdd6e58d8ae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020326"
---
# <a name="win32_autochksetting-class"></a>Win32 \_ AutochkSetting 類別

**Win32 \_ AutochkSetting** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表磁片之 autocheck 操作的設定。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, AMENDMENT]
class Win32_AutochkSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 UserInputDelay;
};
```

## <a name="members"></a>成員

**Win32 \_ AutochkSetting** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ AutochkSetting** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

目前物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前物件的文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SettingId" ) ，索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

用來作為目前物件之索引鍵一部分的識別碼。

</dd> <dt>

**UserInputDelay**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKLM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \| AutoChkTimeOut" ) ，[**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "seconds" ) 
</dt> </dl>

Autocheck 的使用者輸入延遲。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ AutochkSetting** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。

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

[**CIM \_ 設定**](cim-setting.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

