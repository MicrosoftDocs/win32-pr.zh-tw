---
description: 將與指定索引相關聯的 SWbemObject 傳回集合中。
ms.assetid: 75830f78-0489-4fae-bf9c-2eee8526232e
ms.tgt_platform: multiple
title: 'Swbemobjectset 搭配使用. ItemIndex 方法 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
- ISWbemObjectSet.ItemIndex
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 606a09ebf54f0a31dbe14e10abd52a7e92d815d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992080"
---
# <a name="swbemobjectsetitemindex-method"></a>Swbemobjectset 搭配使用. ItemIndex 方法

**ItemIndex** 方法會將與指定索引相關聯的 [**SWbemObject**](swbemobject.md)傳回集合中。 索引會指出元素在集合中的位置。 集合編號從零開始。

## <a name="syntax"></a>語法


```VB
objWbemObject = .ItemIndex( _
  ByVal lIndex _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*lIndex* 
</dt> <dd>

集合中專案的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，要求的 [**SWbemObject**](swbemobject.md) 物件就會傳回。

## <a name="error-codes"></a>錯誤碼

當 [**專案**](swbemobjectset-item.md) 方法完成時， **Err** 物件可能會包含下列其中一個錯誤碼。

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001) 
</dt> <dd>

未指定的錯誤。

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008) 
</dt> <dd>

指定的參數無效。 如果提供了負索引編號，就會傳回此錯誤。

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006) 
</dt> <dd>

記憶體不足，無法完成操作。

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002) 
</dt> <dd>

找不到要求的專案。

</dd> </dl>

## <a name="remarks"></a>備註

**ItemIndex** 方法可讓以任何語言撰寫的 WMI 用戶端腳本和應用程式以一致的方式來操作集合（例如陣列）。 這個方法可以與 [**swbemobjectset 搭配使用**](swbemobjectset.md) 集合搭配使用。 查詢，例如 [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)、 [**SWbemServices. ReferencesTo**](swbemservices-referencesto.md)、 [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)或 [**SWbemServices.ExecQuery**](swbemservices-execquery.md) 會傳回 **swbemobjectset 搭配使用** 集合。 **ItemIndex** 方法無法用於不包含 [**SWbemObjects**](swbemobject.md)的集合，例如 [**SWbemMethodSet**](swbemmethodset.md)、 [**SWbemNamedValueSet**](swbemnamedvalueset.md)、 [**SWbemPrivilegeSet**](swbemprivilegeset.md)、[**內含**](swbempropertyset.md)和 [**SWbemQualifierSet**](swbemqualifierset.md)。

**ItemIndex** 也可用來取得單一類別的單一實例。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會查詢所有 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 實例的集合，然後顯示前三個處理常式的名稱。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colProcesses = _
    objWMIService.Execquery("Select * from Win32_Process")
Wscript.Echo  colProcesses.ItemIndex(0).Name
Wscript.Echo  colProcesses.ItemIndex(1).Name
Wscript.Echo  colProcesses.ItemIndex(2).Name
```



每個作業系統安裝都只會有一個 [**Win32 \_ 作業系統**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) 實例存在。 建立 [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) 路徑以取得單一實例很麻煩，因此腳本通常會列舉 **Win32 \_ 作業系統** ，即使只有一個實例可用也一樣。 下列 VBScript 程式碼範例示範如何使用 **ItemIndex** 方法來取得一個 **Win32 \_ 作業系統** ，而不使用 **for each** 迴圈。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery _
    ("Select * from Win32_OperatingSystem")

Wscript.Echo "Caption: " & colOperatingSystems.ItemIndex(0).Caption
```



下列 VBScript 程式碼範例會取得與 [**win32 \_ 作業系統**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)（例如 [**win32 \_ SystemOperatingSystem**](/windows/desktop/CIMWin32Prov/win32-systemoperatingsystem)）相關聯的實例。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")

set colOS = _
    objWMIService.Execquery("Select * from Win32_OperatingSystem")
    Wscript.Echo  colOS.ItemIndex(0).Name

set colAssociators = colOS.ItemIndex(0).Associators_
    For Each Associator in colAssociators 
        Wscript.Echo Associator.Path_.RelPath  
    Next
```



下列程式碼範例輸出顯示與 [**Win32 \_ 作業系統**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)相關聯的實例。

``` syntax
Windows Server 2008 
    |C:\Windows|\Device\Harddisk0\Partition1
Win32_ComputerSystem.Name="Test1"
Win32_AutochkSetting.SettingID="Windows Server 2008 
    |C:\\Windows|\\Device\\Harddisk0\\Partition1"
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ swbemobjectset 搭配使用<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Swbemobjectset 搭配使用**](swbemobjectset.md)
</dt> </dl>

 

