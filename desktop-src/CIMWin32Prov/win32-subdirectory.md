---
description: Win32 \_ 子目錄關聯 WMI 類別會將目錄 (資料夾) 與其子目錄中的其中一個 () 的子資料夾建立關聯。
ms.assetid: f0565b7b-d593-468b-96b1-3922428c61e1
ms.tgt_platform: multiple
title: Win32_SubDirectory 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubDirectory
- Win32_SubDirectory.GroupComponent
- Win32_SubDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 046de6ad1e09874351b37d58f7277126e39e990a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111200"
---
# <a name="win32_subdirectory-class"></a>Win32 \_ 子目錄類別

**Win32 \_ 子目錄** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將目錄 (資料夾) 與其子目錄中的其中一個 () 的子資料夾建立關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE469-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_SubDirectory : CIM_Component
{
  Win32_Directory REF GroupComponent;
  Win32_Directory REF PartComponent;
};
```

## <a name="members"></a>成員

**Win32 \_ 子目錄** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ 子目錄** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ 目錄**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "GroupComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ Directory" ) 
</dt> </dl>

代表此關聯中)  (資料夾的父目錄屬性之實例的參考。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ 目錄**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "PartComponent" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ Directory" ) 
</dt> </dl>

此實例的參考，代表關聯) 部分 (子資料夾的子目錄。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ 子目錄** 類別衍生自 [**CIM \_ 元件**](cim-component.md)。

若要傳回資料夾的子資料夾集合，請建立將 *ResultRole* 設定為 *PartComponent* 的關聯查詢。 這表示傳回集合中的所有專案都必須扮演資料夾物件的 PartComponent 或子資料夾的角色。 若要傳回資料夾的父資料夾，請將 *ResultRole* 設定為 *GroupComponent*。

**Win32 \_ 子目錄** 類別只適用于緊接在指定資料夾正上方或正下方的檔案系統層級。

## <a name="examples"></a>範例

下列 VBScript 範例會傳回資料夾 C：腳本中所有子資料夾的清單 \\ 。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSubfolders = objWMIService.ExecQuery _
 ("ASSOCIATORS OF {Win32_Directory.Name='c:\scripts'} " _
 & "WHERE AssocClass = Win32_Subdirectory " _
 & "ResultRole = PartComponent")
For Each objFolder in colSubfolders
 Wscript.Echo objFolder.Name
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

[**CIM \_ 元件**](cim-component.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> </dl>

 

 
