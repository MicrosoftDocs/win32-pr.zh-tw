---
description: Win32 \_ ProgramGroupContents 關聯 WMI 類別會關聯程式群組順序，以及其中包含的個別程式群組或專案。
ms.assetid: 687794d1-acc1-498a-9886-0c9ac762ebf4
ms.tgt_platform: multiple
title: Win32_ProgramGroupContents 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProgramGroupContents
- Win32_ProgramGroupContents.GroupComponent
- Win32_ProgramGroupContents.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f77a61052357f7c67009ee7a89da018abeadda8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025850"
---
# <a name="win32_programgroupcontents-class"></a>Win32 \_ ProgramGroupContents 類別

**Win32 \_ ProgramGroupContents** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會關聯程式群組順序，以及其中包含的個別程式群組或專案。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{86E30E83-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_ProgramGroupContents : CIM_Component
{
  Win32_LogicalProgramGroup REF GroupComponent;
  Win32_ProgramGroupOrItem  REF PartComponent;
};
```

## <a name="members"></a>成員

**Win32 \_ ProgramGroupContents** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ ProgramGroupContents** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ LogicalProgramGroup**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "GroupComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ LogicalProgramGroup" ) 
</dt> </dl>

代表此關聯之邏輯程式群組的實例參考。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ ProgramGroupOrItem**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "PartComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ ProgramGroupOrItem" ) 
</dt> </dl>

代表此關聯之 [ **開始** ] 功能表群組或專案之實例的參考。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ ProgramGroupContents** 類別衍生自 [**CIM \_ 元件**](cim-component.md)。

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

[**CIM \_ 元件**](cim-component.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> </dl>

 

 
