---
description: Win32 \_ SystemProcesses 關聯 WMI 類別會將電腦系統和在該系統上執行的處理常式產生關聯。
ms.assetid: 0d8c3ec6-265e-4486-8e94-f5acd2845cf5
ms.tgt_platform: multiple
title: Win32_SystemProcesses 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProcesses
- Win32_SystemProcesses.GroupComponent
- Win32_SystemProcesses.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b963aea5d9c651e27dc4380200e40dd3dcb9a77
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025927"
---
# <a name="win32_systemprocesses-class"></a>Win32 \_ SystemProcesses 類別

**Win32 \_ SystemProcesses** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將電腦系統和在該系統上執行的處理常式產生關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProcesses : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_Process        REF PartComponent;
};
```

## <a name="members"></a>成員

**Win32 \_ SystemProcesses** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ SystemProcesses** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_** 未執行
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "GroupComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ " ) 
</dt> </dl>

代表執行進程之電腦系統的實例參考。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ 進程**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "PartComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ Process" ) 
</dt> </dl>

代表電腦系統上執行之進程的實例參考。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ SystemProcesses** 類別衍生自 [**CIM \_ SystemComponent**](cim-systemcomponent.md)。

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

[**CIM \_ SystemComponent**](cim-systemcomponent.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> </dl>

 

 
