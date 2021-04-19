---
description: 使用 SWbemObjectPath 物件的方法和屬性來建立和驗證物件路徑。 這個物件可以由 VBScript CreateObject 呼叫建立。
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.tgt_platform: multiple
title: 'SWbemObjectPath 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath
- ISWbemObjectPath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1e6836cd58970f3667d8f629a678d55bec5185a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993052"
---
# <a name="swbemobjectpath-object"></a>SWbemObjectPath 物件

使用 **SWbemObjectPath** 物件的方法和屬性來建立和驗證物件路徑。 這個物件可以由 VBScript **CreateObject** 呼叫建立。

## <a name="members"></a>成員

**SWbemObjectPath** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SWbemObjectPath** 物件有這些方法。



| 方法                                                   | 描述                                                     |
|:---------------------------------------------------------|:----------------------------------------------------------------|
| [**SetAsClass**](swbemobjectpath-setasclass.md)         | 強制路徑為 WMI 類別定址。<br/>              |
| [**SetAsSingleton**](swbemobjectpath-setassingleton.md) | 強制路徑處理單一 WMI 實例。<br/> |



 

### <a name="properties"></a>屬性

**SWbemObjectPath** 物件具有這些屬性。



| 屬性                                                              | 存取類型           | Description                                                                                                                                                                          |
|:----------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**授權單位**](swbemobjectpath-authority.md)<br/>             | 讀取/寫入<br/> | 定義物件路徑之授權單位元件的字串。<br/>                                                                                                           |
| [**類別**](swbemobjectpath-class.md)<br/>                     | 讀取/寫入<br/> | 屬於物件路徑的類別名稱。<br/>                                                                                                                        |
| [**DisplayName**](swbemobjectpath-displayname.md)<br/>         | 讀取/寫入<br/> | 字串，其中包含格式的路徑，該路徑可當做標記顯示名稱使用。 請參閱 [建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)。<br/> |
| [**IsClass**](swbemobjectpath-isclass.md)<br/>                 | 唯讀<br/>  | 指出此路徑是否代表類別的布林值。 這類似于 COM API 中的[ \_ \_ 拼出動植物](wmi-system-properties.md)屬性。<br/>                    |
| [**IsSingleton**](swbemobjectpath-issingleton.md)<br/>         | 唯讀<br/>  | 指出此路徑是否代表單一實例的布林值。<br/>                                                                                                |
| [**索引鍵**](swbemobjectpath-keys.md)<br/>                       | 唯讀<br/>  | [**SWbemNamedValueSet**](swbemnamedvalueset.md)物件，其中包含索引鍵值系結。<br/>                                                                          |
| [**Locale**](swbemobjectpath-locale.md)<br/>                   | 讀取/寫入<br/> | 包含此物件路徑之地區設定的字串。<br/>                                                                                                                     |
| [**命名空間**](swbemobjectpath-namespace.md)<br/>             | 讀取/寫入<br/> | 屬於物件路徑一部分的命名空間名稱。 這與 COM API 中的[ \_ \_ Namespace](wmi-system-properties.md)屬性相同。<br/>                        |
| [**ParentNamespace**](swbemobjectpath-parentnamespace.md)<br/> | 唯讀<br/>  | 屬於物件路徑一部分之命名空間的父系名稱。<br/>                                                                                                      |
| [**路徑**](swbemobjectpath-path.md)<br/>                       | 讀取/寫入<br/> | 包含絕對路徑。 這與 COM API 中的[ \_ \_ Path](wmi-system-properties.md) system 屬性相同。 這是此物件的預設屬性。<br/>    |
| [**Relpath**](swbemobjectpath-relpath.md)<br/>                 | 讀取/寫入<br/> | 包含相對路徑。 這與 COM API 中的[ \_ \_ Relpath](wmi-system-properties.md)系統屬性相同。<br/>                                              |
| [**安全性\_**](swbemobjectpath-security-.md)<br/>            | 唯讀<br/>  | 用來讀取或變更安全性設定。<br/>                                                                                                                             |
| [**伺服器**](swbemobjectpath-server.md)<br/>                   | 讀取/寫入<br/> | 伺服器的名稱。 這與 COM API 中的[ \_ \_ 伺服器](wmi-system-properties.md)系統屬性相同。<br/>                                                       |



 

## <a name="examples"></a>範例

下列 VBScript 程式碼範例示範如何建立物件路徑。


```VB
on error resume next 
Set ObjectPath = CreateObject("WbemScripting.SWbemObjectPath")
ObjectPath.Server = "dingle"
ObjectPath.Namespace = "root/default/something"
ObjectPath.Class = "ho"
ObjectPath.Keys.Add "fred1", 10
ObjectPath.Keys.Add "fred2", -34
ObjectPath.Keys.Add "fred3", 65234654
ObjectPath.Keys.Add "fred4", "Wahaay"
ObjectPath.Keys.Add "fred5", -786186777

if err <> 0 then 
 WScript.Echo err.number
end if 

WScript.Echo "Pass 1:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.ImpersonationLevel = 3

WScript.Echo "Pass 2:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.AuthenticationLevel = 5

WScript.Echo "Pass 3:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

Set Privileges = ObjectPath.Security_.Privileges
if err <> 0 then
 WScript.Echo Hex(Err.Number), Err.Description
end if
Privileges.Add 8
Privileges.Add 20, false

WScript.Echo "Pass 4:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.DisplayName = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah"

WScript.Echo "Pass 5:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""
```



下列 Perl 程式碼範例示範如何建立物件路徑。


```
use strict;
use Win32::OLE;
use constant FALSE=>"false";

my ( $ObjectPath, $Privileges );

eval { $ObjectPath = new Win32::OLE 'WbemScripting.SWbemObjectPath'; };
unless($@)
{
 eval
 {
  $ObjectPath->{Server} = "dingle";
  $ObjectPath->{Namespace} = "root/default/something";
  $ObjectPath->{Class} = "ho";
  $ObjectPath->{Keys}->Add("fred1", 10);
  $ObjectPath->{Keys}->Add("fred2", -34);
  $ObjectPath->{Keys}->Add("fred3", 65234654);
  $ObjectPath->{Keys}->Add("fred4", "Wahaay");
  $ObjectPath->{Keys}->Add("fred5", -786186777);
 };
 unless($@)
 {
  print "\n";
  print "Pass 1:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{ImpersonationLevel} = 3 ;

  print "Pass 2:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{AuthenticationLevel} = 5 ;

  print "Pass 3:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  eval { $Privileges = $ObjectPath->{Security_}->{Privileges}; };
  unless($@)
  {
   $Privileges->Add(8);
   $Privileges->Add(20,FALSE);

   print "Pass 4:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n\n";

   $ObjectPath->{DisplayName} = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah";

   print "Pass 5:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n";
  }
  else
  {
   print STDERR Win32::OLE->LastError, "\n";
  }
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
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
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

 




