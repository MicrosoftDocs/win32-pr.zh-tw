---
description: SWbemObjectPath 物件的 Relpath 屬性包含來自完整路徑的相對路徑。
ms.assetid: 9a4363ae-b6b3-4e8c-a7ca-a9e48c28e19b
ms.tgt_platform: multiple
title: 'SWbemObjectPath. Relpath 屬性 (>wbemdisp.tlb .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Relpath
- ISWbemObjectPath.Relpath
- ISWbemObjectPath.get_Relpath
- ISWbemObjectPath.put_Relpath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8330d1cdc65e818acd4fda63b223303b779b5472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975255"
---
# <a name="swbemobjectpathrelpath-property"></a>SWbemObjectPath. Relpath 屬性

[**SWbemObjectPath**](swbemobjectpath.md)物件的 **Relpath** 屬性包含來自完整路徑的相對路徑。

如需此語法的說明，請參閱 [腳本 API 的檔慣例](document-conventions-for-the-scripting-api.md)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
SWbemObjectPath.Relpath As String
```



## <a name="property-value"></a>屬性值

## <a name="examples"></a>範例

下列 VBScript 程式碼範例顯示從 [**SWbemObject \_**](swbemobject-path-.md)取得的資料與 **SWbemObjectPath. Relpath** 之間的差異。


```VB
set objWMIService = GetObject ("winmgmts:root/cimv2")

set Processes = objWMIService.ExecQuery( _
    "Select * from win32_process")

For Each Process in Processes
 WScript.Echo Process.Path_ 
 WScript.Echo Process.Path_.Relpath
Next
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



 

 




