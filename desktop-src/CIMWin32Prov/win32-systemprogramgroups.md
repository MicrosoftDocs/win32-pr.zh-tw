---
description: Win32 \_ SystemProgramGroups 關聯 WMI 類別會建立電腦系統和邏輯程式群組的關聯。
ms.assetid: cbf810c8-a967-4d60-889c-e47c43b039ea
ms.tgt_platform: multiple
title: Win32_SystemProgramGroups 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProgramGroups
- Win32_SystemProgramGroups.Element
- Win32_SystemProgramGroups.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1a8ca556c24295e2c4b04ab851610ef35ec9b715
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111480"
---
# <a name="win32_systemprogramgroups-class"></a>Win32 \_ SystemProgramGroups 類別

**Win32 \_ SystemProgramGroups** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會建立電腦系統和邏輯程式群組的關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C505-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProgramGroups : Win32_SystemSetting
{
  Win32_ComputerSystem      REF Element;
  Win32_LogicalProgramGroup REF Setting;
};
```

## <a name="members"></a>成員

**Win32 \_ SystemProgramGroups** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ SystemProgramGroups** 類別具有這些屬性。

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_** 未執行
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Element" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI Win32 \| \_ " ) 
</dt> </dl>

代表包含邏輯程式群組之電腦系統的實例參考。

</dd> <dt>

**設定**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ LogicalProgramGroup**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "設定" ) ， [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ LogicalProgramGroup" ) 
</dt> </dl>

代表電腦系統上的邏輯程式群組之實例的參考。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ SystemProgramGroups** 類別衍生自 [**win32 \_ SystemSetting**](win32-systemsetting.md)。

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

[**Win32 \_ SystemSetting**](win32-systemsetting.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> </dl>

 

 
