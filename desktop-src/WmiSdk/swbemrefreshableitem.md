---
description: 代表 SWbemRefresher 物件中的單一專案。
ms.assetid: 6a12c8eb-3ef9-4292-810c-6954294fc8c7
ms.tgt_platform: multiple
title: 'SWbemRefreshableItem 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem
- ISWbemRefreshableItem
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bc4f85145926aba2bd050052c33eb5669dfee8a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103696230"
---
# <a name="swbemrefreshableitem-object"></a>SWbemRefreshableItem 物件

**SWbemRefreshableItem** 物件代表 [**SWbemRefresher**](swbemrefresher.md)物件中的單一專案。 **SWbemRefreshableItem** 物件是透過 [**SWbemRefresher**](swbemrefresher.md)的 [**Add**](swbemrefresher-add.md)和 [**AddEnum**](swbemrefresher-addenum.md)方法來取得。 VBScript [CreateObject](creating-an-object-using-vbscript.md) 呼叫無法建立這個物件。

## <a name="members"></a>成員

**SWbemRefreshableItem** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SWbemRefreshableItem** 物件有這些方法。



| 方法                                        | 描述                                                                                                             |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**移除**](swbemrefreshableitem-remove.md) | 從父 [**SWbemRefresher**](swbemrefresher.md)物件移除 **SWbemRefreshableItem** 物件。<br/> |



 

### <a name="properties"></a>屬性

**SWbemRefreshableItem** 物件具有這些屬性。



| 屬性                                                       | 存取類型           | Description                                                                                                                          |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------|
| [**指數**](swbemrefreshableitem-index.md)<br/>         | 讀取/寫入<br/> | 專案在其父 [**SWbemRefresher**](swbemrefresher.md) 物件中的索引。<br/>                                          |
| [**IsSet**](swbemrefreshableitem-isset.md)<br/>         | 讀取/寫入<br/> | 指出 **SWbemRefreshableItem** 物件是否代表單一物件或物件集。<br/>                        |
| [**Object**](swbemrefreshableitem-object.md)<br/>       | 讀取/寫入<br/> | 表示重新整理的單一 [**SWbemObject**](swbemobject.md) 物件。<br/>                                          |
| [**ObjectSet**](swbemrefreshableitem-objectset.md)<br/> | 讀取/寫入<br/> | 表示要重新整理的物件集。<br/>                                                                                |
| [**複習**](swbemrefreshableitem-refresher.md)<br/> | 唯讀<br/>  | 表示包含 **SWbemRefreshableItem** 物件的父 [**SWbemRefresher**](swbemrefresher.md)物件。<br/> |



 

## <a name="remarks"></a>備註

VBScript 方法 [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) 無法直接用來建立 **SWbemRefreshableItem** 物件。

## <a name="examples"></a>範例

下列腳本說明如何建立 [**SWbemRefresher**](swbemrefresher.md) 物件，並將單一物件和列舉值 **SWbemRefreshableItem** 新增至其中。


```VB
' Get some namespace connections
set cimv2 = GetObject("winmgmts:root\cimv2")
set default = GetObject("winmgmts:root\default")    

' Create a refresher
set refresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object to the refresher.
' The @ is used because this is a singleton 
' system class so only one instance exists.
set item1 = refresher.Add (default, "__CIMOMIdentification=@").Object
MsgBox "WMI Version " item1
' Add an enumerator to the refresher.
' Note that the SWbemRefreshableItem.ObjectSet 
' property must be used to designate
' this as an object set rather than a single object.
set item2 = refresher.AddEnum (cimv2, "Win32_Process").ObjectSet

' Loop three times, refreshing the items

For I= 1 To 3
MsgBox "Refresh number " & I
refresher.Refresh

' Iterate through the collection of
' processes in item2 with name of wscript
    For each process in item2
        If process.name = "wscript.exe" then
        MsgBox "Process " & process.Name & _
           " Page Faults " & process.PageFaults
        End If
    Next 
Next

' Clear out the refresher
refresher.DeleteAll 

' The following should return 0
MsgBox "Number of items in Refresher after DeleteAll " _
    & refresher.Count
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefreshableItem<br/>                                                  |
| IID<br/>                      | IID \_ ISWbemRefreshableItem<br/>                                                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

 




