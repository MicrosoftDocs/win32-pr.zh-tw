---
description: SWbemPrivilegeSet 物件是 SWbemSecurity 物件中 SWbemPrivilege 物件的集合，該物件會要求 Windows Management Instrumentation (WMI) 物件的特定許可權。
ms.assetid: 073cf2d4-f7ee-45a6-8fa6-ca77a4870346
ms.tgt_platform: multiple
title: 'SWbemPrivilegeSet 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet
- ISWbemPrivilegeSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b2946f8b1f745c0db123ed33dab312cbbe9d16c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318864"
---
# <a name="swbemprivilegeset-object"></a>SWbemPrivilegeSet 物件

**SWbemPrivilegeSet** 物件是 [**SWbemSecurity**](swbemsecurity.md)物件中 [**SWbemPrivilege**](swbemprivilege.md)物件的集合，該物件會要求 Windows Management Instrumentation (WMI) 物件的特定許可權。 請參閱 [**許可權常數**](privilege-constants.md)中的許可權清單。 使用 [**Add**](swbemprivilegeset-add.md) 和 [**AddAsString**](swbemprivilegeset-addasstring.md) 方法，將專案加入至集合。 專案是使用 [**Item**](swbemprivilegeset-item.md) 方法從集合中取出，並使用 [**Remove**](swbemprivilegeset-remove.md) 方法移除。 VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 方法呼叫無法建立這個物件。 如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。

**SWbemPrivilegeSet** 物件是特定物件的一組許可權覆寫要求。 使用這個物件進行 API 呼叫時，會嘗試許可權覆寫要求。 **SWbemPrivilegeSet** 物件不會定義目前使用者或進程可用的許可權。 換句話說，取得任何 WMI 物件的許可權，並不會識別連接至 WMI 時所進行的許可權設定，或是將物件傳遞到接收時的作用中許可權。

## <a name="members"></a>成員

**SWbemPrivilegeSet** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SWbemPrivilegeSet** 物件有這些方法。



| 方法                                               | 描述                                                                                                                                                             |
|:-----------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**添加**](swbemprivilegeset-add.md)                 | 使用 [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)常數，將 [**SWbemPrivilege**](swbemprivilege.md)物件加入至 **SWbemPrivilegeSet** 集合。<br/> |
| [**AddAsString**](swbemprivilegeset-addasstring.md) | 使用許可權字串，將 [**SWbemPrivilege**](swbemprivilege.md) 物件加入至 **SWbemPrivilegeSet** 集合。<br/>                                    |
| [**DeleteAll**](swbemprivilegeset-deleteall.md)     | 從集合中刪除擁有權限。<br/>                                                                                                              |
| [**項目**](swbemprivilegeset-item.md)               | 從集合中捕獲 [**SWbemPrivilege**](swbemprivilege.md) 物件。 這是這個物件的預設方法。<br/>                                 |
| [**移除**](swbemprivilegeset-remove.md)           | 從集合中移除 [**SWbemPrivilege**](swbemprivilege.md) 物件。<br/>                                                                              |



 

### <a name="properties"></a>屬性

**SWbemPrivilegeSet** 物件具有這些屬性。



| 屬性                                            | 存取類型          | Description                                       |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**計數**](swbemprivilegeset-count.md)<br/> | 唯讀<br/> | 集合中的項目數目<br/> |



 

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會取得 SWbemPrivileges 物件，並依許可權值將所有可用的許可權新增至集合，如 [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)中所定義。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\cimv2")
set colPrivileges = objWMIService.Security_.Privileges
For I = 1 To 27
colPrivileges.Add(I)
Next
' Display information about each privilege 
For Each objItem In colPrivileges
wscript.echo objItem.Identifier & vbtab & objItem.Name _
    & vbtab & objItem.Displayname _
    & vbtab & "Enabled = " & objItem.IsEnabled
Next
```



下列 VBScript 程式碼範例示範如何使用 **SWbemPrivilegeSet** 物件來加入許可權。


```VB
on error resume next

const wbemPrivilegeSecurity = 8
const wbemPrivilegeDebug = 20

set locator = CreateObject("WbemScripting.SWbemLocator")

' Add a single privilege using SWbemPrivilegeSet.Add

locator.Security_.Privileges.Add wbemPrivilegeSecurity 
Set Privilege = locator.Security_.Privileges(wbemPrivilegeSecurity)
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
locator.Security_.Privileges.Add 6535
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

locator.Security_.Privileges.Add wbemPrivilegeDebug 

locator.Security_.Privileges(wbemPrivilegeDebug).IsEnabled = false

' Add a single privilege using SWbemPrivilegeSet.AddAsString

Set Privilege = locator.Security_.Privileges.AddAsString ("SeChangeNotifyPrivilege")
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
locator.Security_.Privileges.AddAsString "SeChungeNotifyPrivilege"
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

WScript.Echo ""
for each Privilege in locator.Security_.Privileges
 WScript.Echo "[" & Privilege.DisplayName & "]", Privilege.Identifier, Privilege.Name, Privilege.IsEnabled
next

if err <> 0 then
 WScript.Echo Err.Number, Err.Description, Err.Source
end if 
```



下列 Perl 程式碼範例示範如何使用 **SWbemPrivilegeSet** 物件來加入許可權。


```
use strict;
use Win32::OLE;

close(STDERR);

my ($locator, $Privilege);
my $wbemPrivilegeSecurity = 8;
my $wbemPrivilegeDebug = 20;

eval { $locator = new Win32::OLE 'WbemScripting.SWbemLocator';};

if (!$@ && defined $locator)
{
 # Add a single privilege using SWbemPrivilegeSet.Add
 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeSecurity);
 $Privilege = $locator->{Security_}->Privileges($wbemPrivilegeSecurity);
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
 eval { $locator->{Security_}->{Privileges}->Add(6535); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);

 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeDebug); 
 $locator->{Security_}->Privileges($wbemPrivilegeDebug)->{IsEnabled} = 0;

 # Add a single privilege using SWbemPrivilegeSet.AddAsString
 $Privilege = $locator->{Security_}->{Privileges}->AddAsString ("SeChangeNotifyPrivilege");
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
 eval {$locator->{Security_}->{Privileges}->AddAsString ("SeChungeNotifyPrivilege"); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);
 print "\n";

 foreach $Privilege (in {$locator->{Security_}->{Privileges}})
 {
  printf "[%s] %d %s %d \n" , $Privilege->{DisplayName}, $Privilege->{Identifier}, $Privilege->{Name}, $Privilege->{IsEnabled};
 }
}
else
{
 print Win32::OLE->LastError, "\n";
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
| CLSID<br/>                    | CLSID \_ SWbemPrivilegeSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemPrivilegeSet<br/>                                                      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[執行具有特殊許可權的作業](executing-privileged-operations.md)
</dt> <dt>

[使用 VBScript 執行特殊許可權作業](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> <dt>

[**許可權常數**](privilege-constants.md)
</dt> </dl>

 

