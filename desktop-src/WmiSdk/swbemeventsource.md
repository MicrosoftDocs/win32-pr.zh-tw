---
description: SWbemEventSource 物件會將事件查詢中的事件與 SWbemServices.ExecNotificationQuery 一起抓取。
ms.assetid: 7efd5e6a-4311-4d20-8b05-e9208eec098a
ms.tgt_platform: multiple
title: 'SWbemEventSource 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 09/25/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource
- ISWbemEventSource
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8da55a7b6722c263fe9a3fb0af7a8db07d672e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983551"
---
# <a name="swbemeventsource-object"></a>SWbemEventSource 物件

**SWbemEventSource** 物件會將事件查詢中的事件與 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)一起抓取。 如果您對 **SWbemServices.ExecNotificationQuery** 進行呼叫，以進行事件查詢，則會取得 **SWbemEventSource** 物件。 然後，您可以使用 [**NextEvent**](swbemeventsource-nextevent.md) 方法在到達時取出事件。 VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 呼叫無法建立這個物件。

## <a name="members"></a>成員

**SWbemEventSource** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SWbemEventSource** 物件有這些方法。



| 方法                                          | 描述                                                                                                                                  |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**NextEvent**](swbemeventsource-nextevent.md) | 用來將事件與 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)一起取得。<br/> |



 

### <a name="properties"></a>屬性

**SWbemEventSource** 物件具有這些屬性。



| 屬性                                                    | 存取類型          | Description                                              |
|:------------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**安全性\_**](swbemeventsource-security-.md)<br/> | 唯讀<br/> | 用來讀取或變更安全性設定。<br/> |



 

## <a name="examples"></a>範例

此腳本會使用 **SWbemEventSource** 類別和 [**SWbemServices**](swbemservices.md) 類別的方法搭配應用程式事件的 WQL 查詢。 如需 WMI 事件通知和查詢的詳細資訊，請參閱 [監視事件](monitoring-events.md)、 [根據事件執行腳本](running-a-script-based-on-an-event.md)，以及 [接收非同步事件通知](receiving-asynchronous-event-notifications.md)。


```VB
' Connect to WMI, obtaining an SWbemServices object
set svc = _
CreateObject("Wbemscripting.SWbemLocator")._
   ConnectServer(,"root\cimv2")

' Obtain an SWbemEventSource object from the 
' SWbemServices.ExecNotificationQuery method to specify the 
' event source as "Application" events in a Win32_NTLogEvent
set evtsrc = svc.ExecNotificationQuery("SELECT * " _
   & "FROM __InstanceCreationEvent " _
   & "WHERE TargetInstance ISA 'Win32_NTLogEvent'" _
   & "AND TargetInstance.Logfile ='Application'")

' Wait for an event by executing the NextEvent method on the 
' SWbemEventSource object.
while (num < 5)
    set inst = evtsrc.NextEvent(-1)
    Wscript.echo inst.TargetInstance.Logfile
    num = num + 1
wend
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>>wbemdisp.tlb .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemEventSource<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemEventSource<br/>                                                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

