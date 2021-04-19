---
description: SWbemLastError 物件的方法和屬性包含和操作錯誤物件。
ms.assetid: 11a652fa-29e8-437b-8e62-e28e56a8a38d
ms.tgt_platform: multiple
title: 'SWbemLastError 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError
- Associators_
- AssociatorsAsync_
- Delete_
- DeleteAsync_
- ExecMethod_
- ExecMethodAsync_
- Instances_
- InstancesAsync_
- Put_
- PutAsync_
- References_
- ReferencesAsync_
- SpawnDerivedClass_
- SpawnInstance_
- Subclasses_
- SubclassesAsync_
- Derivation_
- get_Derivation_
- Methods_
- get_Methods_
- Qualifiers_
- get_Qualifiers_
- Security_
- get_Security_
- ISWbemLastError
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a00d8e3421800acab7cc4958ddc1e6a75f101958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986839"
---
# <a name="swbemlasterror-object"></a>SWbemLastError 物件

**SWbemLastError** 物件的方法和屬性包含和操作錯誤物件。 這個物件的方法和屬性與 [**SWbemObject**](swbemobject.md) 物件的方法和屬性完全相同，但用來包含錯誤資訊，而不是 WMI 類別資訊。 這個物件可以由 VBScript **CreateObject** 呼叫建立。

您可以建立 **SWbemLastError** error 物件，以檢查與先前的方法呼叫相關聯的延伸錯誤資訊。 如果錯誤資訊無法使用，則嘗試建立錯誤物件將會失敗。 如果呼叫成功，並傳回錯誤物件，則會重設物件的狀態。 後續嘗試抓取錯誤物件將會失敗，直到發生新的錯誤為止。 如果您進行失敗的非同步呼叫， **SWbemLastError** 物件可能會由 *objWbemErrorObject* 參數中的 [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md)事件傳回給您。

## <a name="members"></a>成員

**SWbemLastError** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SWbemLastError** 物件有這些方法。



| 方法                                                   | 描述                                                                                  |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| **Associators of\_**                                        | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/> |
| **AssociatorsAsync\_**                                   | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/> |
| [**克隆\_**](swbemlasterror-clone-.md)                 | 建立目前物件的複本。<br/>                                               |
| [**CompareTo\_**](swbemlasterror-compareto-.md)         | 測試兩個物件是否相等。<br/>                                                   |
| **刪除\_**                                             | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/> |
| **DeleteAsync\_**                                        | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/> |
| **ExecMethod\_**                                         | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/> |
| **ExecMethodAsync\_**                                    | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/> |
| [**GetObjectText\_**](swbemlasterror-getobjecttext-.md) | 抓取以 MOF 語法撰寫之物件的文字標記法。<br/>       |
| **執行個體\_**                                          | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/> |
| **InstancesAsync\_**                                     | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/> |
| **把\_**                                                | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/> |
| **PutAsync\_**                                           | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/> |
| **參考資料\_**                                         | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/> |
| **ReferencesAsync\_**                                    | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/> |
| **SpawnDerivedClass\_**                                  | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/> |
| **SpawnInstance\_**                                      | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/> |
| **子\_**                                         | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/> |
| **SubclassesAsync\_**                                    | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/> |



 

### <a name="properties"></a>屬性

**SWbemLastError** 物件具有這些屬性。



| 屬性                                                      | 存取類型          | Description                                                                                                                                                   |
|:--------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **衍生\_**<br/>                                   | 唯讀<br/> | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/>                                                                  |
| **方法\_** <br/>                                     | 唯讀<br/> | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/>                                                                  |
| [**路徑\_**](swbemlasterror-path-.md)<br/>             | 唯讀<br/> | 包含 [**SWbemObjectPath**](swbemobjectpath.md) 物件，該物件表示目前類別或實例的物件路徑。<br/>                    |
| [**屬性\_**](swbemlasterror-properties-.md)<br/> | 唯讀<br/> | 表示 **SWbemLastError** 物件的屬性集合。 這個屬性是 [**內含**](swbempropertyset.md) 物件。<br/> |
| **限定詞\_**<br/>                                   | 唯讀<br/> | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/>                                                                  |
| **安全性\_**<br/>                                     | 唯讀<br/> | 未使用。 [**SWbemObject**](swbemobject.md)物件提供相同的方法。<br/>                                                                  |



 

## <a name="examples"></a>範例

下列 VBScript 範例示範如何檢查錯誤和錯誤物件資訊。


```VB
On Error Resume Next

'Ask for non-existent class to force error

Set t_Service = GetObject("winmgmts://./root/default")
Set t_Object = t_Service.Get("Nosuchclass000")

if Err = 0 Then
 WScript.Echo "Got a class"
Else
 WScript.Echo ""
 WScript.Echo "Err Information:"
 WScript.Echo ""
 WScript.Echo "  Source:", Err.Source
 WScript.Echo "  Description:", Err.Description
 WScript.Echo "  Number", "0x" & Hex(Err.Number)

 'Create the last error object
 set t_Object = CreateObject("WbemScripting.SWbemLastError")
 WScript.Echo ""
 WScript.Echo "WMI Last Error Information:"
 WScript.Echo ""
 WScript.Echo " Operation:", t_Object.Operation
 WScript.Echo " Provider:", t_Object.ProviderName

 strDescr = t_Object.Description
 strPInfo = t_Object.ParameterInfo
 strCode = t_Object.StatusCode

 if (strDescr <> nothing) Then
  WScript.Echo " Description:", strDescr  
 end if

 if (strPInfo <> nothing) Then
  WScript.Echo " Parameter Info:", strPInfo  
 end if

 if (strCode <> nothing) Then
  WScript.Echo " Status:", strCode  
 end if

 WScript.Echo ""
 Err.Clear
 set t_Object2 = CreateObject("WbemScripting.SWbemLastError")
 if Err = 0 Then
    WScript.Echo "Got the error object again - this shouldn't have happened!" 
 Else
    Err.Clear
    WScript.Echo "Couldn't get last error again - as expected"
 End if
End If

```



下列 Perl 範例示範如何檢查錯誤和錯誤物件資訊。


```
use strict;
use Win32::OLE;

my ( $t_Service, $t_Object, $t_Object2, $strDescr, $strPInfo, $strCode );

# Close STDERR file handle to eliminate redundant error message
close(STDERR);

# Ask for non-existent class to force error 
$t_Service = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default"); 
$t_Object = $t_Service->Get("Nosuchclass000");

if (defined $t_Object)
{
 print "Got a class\n"; 
}
else
{
 print "\nErr Information:\n\n";
 print Win32::OLE->LastError, "\n";

 # Create the last error object
 $t_Object = new Win32::OLE 'WbemScripting.SWbemLastError';
 print "\nWMI Last Error Information:\n\n";
 print " Operation: ", $t_Object->{Operation}, "\n";
 print " Provider: ", $t_Object->{ProviderName}, "\n";
 
 $strDescr = $t_Object->{Description};
 $strPInfo = $t_Object->{ParameterInfo};
 $strCode = $t_Object->{StatusCode};

 if (defined $strDescr)
 {
  print " Description: ", $strDescr, "\n";  
 }

 if (defined $strPInfo)
 {
  print " Parameter Info: ", $strPInfo, "\n";  
 }

 if (defined $strCode)
 {
  print " Status: ", $strCode, "\n";  
 }

 print "\n";

 $t_Object2 = new Win32::OLE 'WbemScripting.SWbemLastError';
 if (defined $t_Object2)
 {
  print "Got the error object again - this shouldn't have happened!\n";
 }
 else
 {
  print "Couldn't get last error again - as expected\n";
 }
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

 




