---
description: SWbemNamedValueSet 物件是 SWbemNamedValue 物件的集合。
ms.assetid: 7d1c3a28-d0d3-4108-9628-74ad483e328e
ms.tgt_platform: multiple
title: 'SWbemNamedValueSet 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet
- ISWbemNamedValueSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b3048b8589666a07958251ed4c0d56100132fd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982340"
---
# <a name="swbemnamedvalueset-object"></a>SWbemNamedValueSet 物件

**SWbemNamedValueSet** 物件是 [**SWbemNamedValue**](swbemnamedvalue.md)物件的集合。 **SWbemNamedValueSet** 的方法和屬性主要是在送出 WMI 的某些呼叫時，將更多資訊傳送給提供者。 [**SWbemServices**](swbemservices.md)中的所有呼叫，以及 [**SWbemObject**](swbemobject.md)中的某些呼叫，會採用屬於此類型之物件的選擇性參數。 用戶端可以將資訊新增至 **SWbemNamedValueSet** 物件，並以呼叫的其中一個參數來傳送 **SWbemNamedValueSet** 物件。 這個物件可以由 VBScript **CreateObject** 呼叫建立。

如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。

> [!Note]  
> 重要-可能的話，請勿使用這項機制，因為它可以中斷以 WMI 為基礎的統一存取模型。 如果提供者使用此機制，請務必盡可能謹慎使用這項機制。 如果提供者需要大量的高度特定內容資訊來回應要求，則必須撰寫所有用戶端的程式碼，以提供這項資訊。 這種機制可讓您視需要存取這類提供者。

 

**SWbemNamedValueSet** 物件是 [**SWbemNamedValue**](swbemnamedvalue.md)元素的集合。 這些專案會使用 [**SWbemNamedValueSet**](swbemnamedvalueset-add.md) 加入至集合。 它們是使用 [**SWbemNamedValueSet**](swbemnamedvalueset-remove.md) 方法來移除，並使用 [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) 方法抓取。 您可以存取方法，以填入動態提供者所需的任何內容資訊。 呼叫其中一個 [**SWbemServices**](swbemservices.md) 方法之後，您可以重複使用 **SWbemNamedValueSet** 物件進行另一個呼叫。

基礎提供者會決定包含在 **SWbemNamedValueSet** 物件中的資訊。 WMI 不會使用該資訊，而只是將它轉寄給提供者。 提供者必須發佈服務要求所需的內容資訊。

## <a name="members"></a>成員

**SWbemNamedValueSet** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SWbemNamedValueSet** 物件有這些方法。



| 方法                                            | 描述                                                                                                                              |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**添加**](swbemnamedvalueset-add.md)             | 將 [**SWbemNamedValue**](swbemnamedvalue.md) 物件加入至集合。<br/>                                                  |
| [**克隆**](swbemnamedvalueset-clone.md)         | 製作這個 **SWbemNamedValueSet** 集合的複本。<br/>                                                                       |
| [**DeleteAll**](swbemnamedvalueset-deleteall.md) | 從集合中移除所有專案，使 **SWbemNamedValueSet** 物件空白。<br/>                                        |
| [**項目**](swbemnamedvalueset-item.md)           | 從集合中捕獲 [**SWbemNamedValue**](swbemnamedvalue.md) 物件。 這是物件的預設方法。<br/> |
| [**移除**](swbemnamedvalueset-remove.md)       | 從集合中移除 [**SWbemNamedValue**](swbemnamedvalue.md) 物件。<br/>                                             |



 

### <a name="properties"></a>屬性

**SWbemNamedValueSet** 物件具有這些屬性。



| 屬性                                             | 存取類型          | Description                                       |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**計數**](swbemnamedvalueset-count.md)<br/> | 唯讀<br/> | 集合中的項目數目<br/> |



 

## <a name="examples"></a>範例

下列 VBScript 範例示範如何操作命名值集，在此案例中，命名值為數組類型。


```VB
Set Context = CreateObject("WbemScripting.SWbemNamedValueSet")

On Error Resume Next

Context.Add "n1", Array (1, 2, 3)
str = "The initial value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

WScript.Echo ""

' report the value of an element of the context value
v = Context("n1")
WScript.Echo "By indirection the first element of n1 has value:",v(0)

' report the value directly
WScript.Echo "By direct access the first element of n1 has value:", Context("n1")(0)

' set the value of a single named value element
Context("n1")(1) = 11 
WScript.Echo "After direct assignment the first element of n1 has value:", Context("n1")(1)

' set the value of a single named value element
Set v = Context("n1")
v(1) = 345
WScript.Echo "After indirect assignment the first element of n1 has value:", Context("n1")(1)

' set the value of an entire context value
Context("n1") = Array (5, 34, 178871)
WScript.Echo "After direct array assignment the first element of n1 has value:", Context("n1")(1)

str = "After direct assignment the entire value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



下列 Perl 範例示範如何操作命名值集，在此案例中，命名值為數組類型。


```
use strict;
use Win32::OLE;

my ( $Context, $str, $x, @v);

eval {$Context = new Win32::OLE 'WbemScripting.SWbemNamedValueSet'; };
unless($@)
{
 $Context->Add("n1", [1, 2, 3]);
 $str = "The initial value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n\n";

 # report the value of an element of the context value
 @v = @{$Context->Item("n1")->{Value}};
 print "By indirection the first element of n1 has value:", $v[0], "\n";

 # report the value directly
 print "By direct access the first element of n1 has value:", @{$Context->Item("n1")->{Value}}[0], "\n";

 # set the value of a single named value element
 @{$Context->Item("n1")->{Value}}[1] = 11;
 print "After direct assignment the first element of n1 has value:", 
       @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of a single named value element
 @v = @{$Context->Item("n1")->{Value}};
 $v[1] = 345;
 print "After indirect assignment the first element of n1 has value:", 
    @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of an entire context value
 $Context->Item("n1")->{Value} = [5, 34, 178871];
 print "After direct array assignment the first element of n1 has value:", 
   @{$Context->Item("n1")->{Value}}[1], "\n";

 $str = "After direct assignment the entire value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n";
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
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
| CLSID<br/>                    | CLSID \_ SWbemNamedValueSet<br/>                                                    |
| IID<br/>                      | IID \_ ISWbemNamedValueSet<br/>                                                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

 




