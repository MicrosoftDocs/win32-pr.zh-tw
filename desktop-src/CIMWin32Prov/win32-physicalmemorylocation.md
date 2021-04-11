---
description: Win32 \_ PhysicalMemoryLocation 關聯 WMI 類別會將實體記憶體和其實體記憶體的陣列產生關聯。
ms.assetid: 40252428-77ca-4dfb-8048-c05096a114d8
ms.tgt_platform: multiple
title: Win32_PhysicalMemoryLocation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryLocation
- Win32_PhysicalMemoryLocation.LocationWithinContainer
- Win32_PhysicalMemoryLocation.PartComponent
- Win32_PhysicalMemoryLocation.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: daa6d47b13cb5caa74a10f28ab5fcd6e66e1524f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936515"
---
# <a name="win32_physicalmemorylocation-class"></a>Win32 \_ PhysicalMemoryLocation 類別

**Win32 \_ PhysicalMemoryLocation** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將實體記憶體和其實體記憶體的陣列產生關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF562-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_PhysicalMemoryLocation : CIM_PackagedComponent
{
  string                        LocationWithinContainer;
  Win32_PhysicalMemory      REF PartComponent;
  Win32_PhysicalMemoryArray REF GroupComponent;
};
```

## <a name="members"></a>成員

**Win32 \_ PhysicalMemoryLocation** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ PhysicalMemoryLocation** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ PhysicalMemoryArray**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "GroupComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ PhysicalMemoryArray" ) 
</dt> </dl>

[**Win32 \_ PhysicalMemoryArray**](win32-physicalmemoryarray.md) ，代表包含實體記憶體的實體記憶體陣列。

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

自由格式的字串，表示實體元素在實體封裝內的位置。 與容器中的固定元素相關的資訊 (例如：「來自頂端的第二個磁片磁碟機槽」 ) 、角度、高度和其他資料都可以記錄在這個屬性中。 此字串可以補充或用來取代將 [**CIM \_ 位置**](cim-location.md) 物件具現化。

這個屬性繼承自 [**CIM \_ 容器**](cim-container.md)。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ PhysicalMemory**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "PartComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ PhysicalMemory" ) 
</dt> </dl>

[**Win32 \_ PhysicalMemory**](win32-physicalmemory.md) ，代表包含在實體記憶體陣列中的實體記憶體。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ PhysicalMemoryLocation** 類別衍生自 [**CIM \_ PackagedComponent**](cim-packagedcomponent.md)。

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

[**CIM \_ PackagedComponent**](cim-packagedcomponent.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

 
