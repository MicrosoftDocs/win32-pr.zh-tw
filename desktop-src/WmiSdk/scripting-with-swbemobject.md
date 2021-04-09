---
description: SWbemObject 腳本物件是一般的 WMI 物件，定義可使用的屬性和方法，不論 SWbemObject 物件系結的特定 WMI 物件為何。
ms.assetid: 33252b49-00d4-4c43-8abe-9368ed82f34b
ms.tgt_platform: multiple
title: 使用 SWbemObject 編寫腳本
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ce9a48779b13f1b1917ad189b2297b60329ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114892"
---
# <a name="scripting-with-swbemobject"></a>使用 SWbemObject 編寫腳本

[**SWbemObject**](swbemobject.md)腳本物件是一般的 wmi 物件，定義可使用的屬性和方法，不論 **SWbemObject** 物件系結的特定 WMI 物件為何。 所有 WMI 物件（例如 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 或任何其他 wmi 資料類別的實例）都會以 [**SWbemObject**](swbemobject.md) 表示，而且除了各自的特定屬性和方法之外，還可以使用 **SWbemObject** 的通用屬性和方法。

例如，您可以使用下列腳本，藉由呼叫 [**SWbemObject 實例 \_**](swbemobject-instances-.md)方法來取得 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)的所有實例。 ClsobjProcess 同時代表 **Win32 \_ 進程** 類別定義和 [**SWbemObject**](swbemobject.md)。


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set clsobjProcess = objWMIServices.Get("Win32_Process")
Set colProcesses = clsobjProcess.Instances_()
For Each Process in colProcesses
    WScript.Echo Process.Name
Next
```



下列範例會取得代表警報器服務的特定 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 實例，並將其儲存在 objAlerter 中。 然後，您可以呼叫 [**SWbemObject**](swbemobject.md) 方法，例如 Wscript.echo. echo ObjAlerter. Path \_ 或資料類別所定義的方法，例如 Wscript.echo. Echo objAlerter. State。 objAlerter，代表 Win32 服務的實例 \_ 和 **SWbemObject**。


```VB
strComputer = "." 
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set objAlerter = objWMIServices.Get("Win32_Service.Name='Alerter'")
WScript.Echo objAlerter.Path_
objAlerter.StopService()
WScript.Echo objAlerter.State
```




```VB
For each Prop in myObject.Properties_
    Wscript.Echo Prop.Name
Next
```



呼叫 [**SWbemObject \_**](swbemobject-instances-.md)時，會取得另一個泛型 WMI 腳本物件 [**swbemobjectset 搭配使用**](swbemobjectset.md)。 如所示， **swbemobjectset 搭配使用** 物件可視為 [集合](accessing-a-collection.md)。


```VB
Set clsobjProcess = objWMIServices.Get("Win32_Process")
```



您可以識別 [**SWbemObject**](swbemobject.md)方法，因為它們的結尾都是底線 (\_) ，例如 [**SWbemObject \_ 實例**](swbemobject-instances-.md)。

[**SWbemObjectEx**](swbemobjectex.md) 會擴充 [**SWbemObject**](swbemobject.md)的屬性。 例如，您現在可以藉由呼叫 [**\_ SWbemObjectEx**](swbemobjectex-refresh-.md)來更新任何 WMI 物件的資料，例如 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)的實例。

下列範例顯示每五秒可重新整理系統進程分頁錯誤資料的方式。


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'System'",,48) 
For Each Process in colProcesses
        i = 0
        Do Until i = 5
            i = i + 1
            Wscript.Echo "PageFaults = " & Process.PageFaults 
            Wscript.Sleep 10000
            Process.Refresh_
        Loop
Next
```



如需有關使用 [**SWbemRefresher**](swbemrefresher.md) 物件重新整理資料的詳細資訊，請參閱 [在腳本中重新整理 WMI 資料](refreshing-wmi-data-in-scripts.md)。

[**SWbemObject \_**](swbemobject-put-.md)和 [**PutAsync \_**](swbemobject-putasync-.md)可讓您將變更寫回任何 WMI 物件。 這些方法只會在建立物件的命名空間中，認可物件的變更。 您可以使用 [**SWbemServicesEx 將**](swbemservicesex-put.md) 物件寫入至不同的命名空間，或使用 [**SWbemServicesEx. PutAsync**](swbemservicesex-putasync.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[適用于 WMI 的腳本 API](scripting-api-for-wmi.md)
</dt> <dt>

[建立 WMI 腳本](creating-a-wmi-script.md)
</dt> <dt>

[更新整個實例](updating-an-entire-instance.md)
</dt> <dt>

[呼叫方法](calling-a-method.md)
</dt> </dl>

 

 
