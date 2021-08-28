---
description: Swbemobjectset 搭配使用物件是 SWbemObject 物件的集合。 如需詳細資訊，請參閱存取集合。 VBScript CreateObject 呼叫無法建立這個物件。
ms.assetid: 00f5317e-eb8e-42f9-bada-963e11aadda4
ms.tgt_platform: multiple
title: 'Swbemobjectset 搭配使用物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet
- ISWbemObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 33cefd39dc0e860906bc99b1f591a87dae845d6a9317410ce4850fb1a54ea708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857098"
---
# <a name="swbemobjectset-object"></a>Swbemobjectset 搭配使用物件

**Swbemobjectset 搭配使用** 物件是 [**SWbemObject**](swbemobject.md)物件的集合。 如需詳細資訊，請參閱 [存取集合](accessing-a-collection.md)。 VBScript **CreateObject** 呼叫無法建立這個物件。

您可以藉由呼叫下列任何一種方法或其非同步對應來取得 **swbemobjectset 搭配使用** 物件：

-   [**SWbemObject. Associators of\_**](swbemobject-associators-.md)
-   [**SWbemObject 實例\_**](swbemobject-instances-.md)
-   [**SWbemObject 參考\_**](swbemobject-references-.md)
-   [**SWbemObject 子類別\_**](swbemobject-subclasses-.md)
-   [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)
-   [**SWbemServices.ExecQuery**](swbemservices-execquery.md)
-   [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)
-   [**SWbemServices. ReferencesTo**](swbemservices-referencesto.md)
-   [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)

> [!Note]  
> **Swbemobjectset 搭配使用** 物件不支援選擇性的 **加入** 和 **移除** 收集方法。

 

> [!Note]  
> 由於回呼的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

 

## <a name="members"></a>成員

**Swbemobjectset 搭配使用** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Swbemobjectset 搭配使用** 物件有這些方法。



| 方法                              | 描述                                                                                                                      |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [**Item**](swbemobjectset-item.md) | 從集合中捕獲 [**SWbemObject**](swbemobject.md) 物件。 這是物件的預設方法。<br/> |



 

### <a name="properties"></a>屬性

**Swbemobjectset 搭配使用** 物件具有這些屬性。



| 屬性                                                  | 存取類型          | 描述                                              |
|:----------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**計數**](swbemobjectset-count.md)<br/>          | 唯讀<br/> | 集合中的項目數目<br/>        |
| [**安全性\_**](swbemobjectset-security-.md)<br/> | 唯讀<br/> | 用來讀取或變更安全性設定。<br/> |



 

## <a name="remarks"></a>備註

**Swbemobjectset 搭配使用** 是零或多個 [**SWbemObject**](swbemobject.md)物件的集合。 **Swbemobjectset 搭配使用** 中的每個 **SWbemObject** 都可以代表兩個專案的其中一個：

-   受 WMI 管理之資源的實例。
-   類別定義的實例。

此類別在 WMI 中最常見的用法是作為 [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) 或 [**InstancesOf**](swbemservices-instancesof.md) 呼叫的傳回值，如下列程式碼範例所述：


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colServices = objSWbemServices.ExecQuery("SELECT State FROM Win32_Service")
For Each objService In colServices
    Wscript.Echo objService.Name, objService.State
Next
```



在大部分的情況下，您只會對 **swbemobjectset 搭配使用** 列舉集合本身所包含的所有物件。 不過， **swbemobjectset 搭配使用** 確實包含可在系統管理腳本中使用的屬性計數。 顧名思義，Count 會告訴您集合中的專案數。 例如，此腳本會取得電腦上安裝的所有服務的集合，然後回顯找到的服務總數：

如需如何使用這個類別的詳細資訊，請參閱 [列舉 WMI](enumerating-wmi.md)。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例說明如何操作 **swbemobjectset 搭配使用** 集合。


```VB
On Error Resume Next

Set Disks = GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")

WScript.Echo "There are", Disks.Count, " Disks"

Set Disk = Disks("Win32_LogicalDisk.DeviceID=""C:""")
WScript.Echo Disk.Path_.Path

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



下列 Perl 程式碼範例說明如何操作 **swbemobjectset 搭配使用** 集合。


```
use strict;
use Win32::OLE;

my ($disks,$disk);

eval { $disks = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf("CIM_LogicalDisk"); };
unless($@)
{
 print "\nThere are ", $disks->{Count}, " Disks \n";

 eval { $disk = $disks->Item("Win32_LogicalDisk.DeviceID=\"C:\""); };
 unless($@)
 {
  print $disk->{Path_}->{Path}, "\n";
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
| 標頭<br/>                   | <dl> <dt>>Wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>Wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ swbemobjectset 搭配使用<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

 




