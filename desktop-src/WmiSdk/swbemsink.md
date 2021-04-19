---
description: SWbemSink 物件是由用戶端應用程式所執行，以接收非同步作業和事件通知的結果。
ms.assetid: a90777ef-fa26-4bfb-b196-c083a0c92a29
ms.tgt_platform: multiple
title: 'SWbemSink 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink
- ISWbemSinkEvents
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b8007b7387a09e31f49dbc833f657bc959ee11e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977826"
---
# <a name="swbemsink-object"></a>SWbemSink 物件

**SWbemSink** 物件是由用戶端應用程式所執行，以接收非同步作業和事件通知的結果。 若要進行非同步呼叫，您必須建立 **SWbemSink** 物件的實例，並將它傳遞為 *ObjWbemSink* 參數。 當傳回狀態或結果時，或當呼叫完成時，會觸發 **SWbemSink** 的執行中的事件。 VBScript **CreateObject** 呼叫會建立這個物件。

## <a name="members"></a>成員

**SWbemSink** 物件具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**SWbemSink** 物件有這些方法。



| 方法                             | 描述                                                                        |
|:-----------------------------------|:-----------------------------------------------------------------------------------|
| [**取消**](swbemsink-cancel.md) | 取消與此接收相關聯的所有非同步作業。<br/> |



 

## <a name="remarks"></a>備註

非同步回呼可讓未經驗證的使用者提供資料給接收。 這會對您的腳本和應用程式帶來安全性風險。 若要消除風險，請使用兩個同步通訊或同步通訊。 如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。

### <a name="events"></a>事件

您可以在觸發事件時，執行要呼叫的副程式。 例如，如果您想要處理非同步查詢呼叫（例如 [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)）所傳回的每個物件，請使用非同步呼叫中指定的接收來建立副程式，如下列範例所示。


```VB
Sub SinkName_OnObjectReady(objObject, objAsyncContext)
```



使用下表做為參考，以識別事件和觸發程式描述。



| 事件                                            | 描述                                                             |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [**OnCompleted**](swbemsink-oncompleted.md)     | 在非同步作業完成時觸發。                   |
| [**OnObjectPut**](swbemsink-onobjectput.md)     | 在非同步 Put 作業完成時觸發。               |
| [**OnObjectReady**](swbemsink-onobjectready.md) | 當非同步呼叫提供的物件可用時觸發。 |
| [**OnProgress**](swbemsink-onprogress.md)       | 觸發以提供非同步作業的狀態。            |



 

**非同步地取出事件記錄檔統計資料**

WMI 支援非同步和半同步腳本。 從事件記錄檔取得事件時，非同步腳本通常會以更快的速度來取得此資料。

在非同步腳本中，會發出查詢，並立即將控制權傳回給腳本。 此查詢會繼續在不同的執行緒上進行處理，而腳本會開始立即對傳回的資訊採取動作。 非同步腳本是事件驅動：每次抓取事件記錄時，就會引發 OnObjectReady 事件。 當查詢完成時，將會引發 OnCompleted 事件，而腳本可以根據已傳回所有可用記錄的事實繼續進行。

相反地，在半同步腳本中，會發出查詢，然後腳本會將大量抓取的資訊排入佇列，然後再進行處理。 對於許多物件而言，半同步處理已足夠;例如，在查詢磁片磁碟機的屬性時，在發出查詢的時間與傳回並處理資訊的時間之間可能只有一個分割秒。 這是因為傳回的資訊數量相對較小，這是很大的部分。

不過，在查詢事件記錄檔時，查詢發出的時間間隔和半同步腳本可以完成傳回和處理資訊的時間可能需要數小時。 最重要的是，腳本可能會用盡記憶體，並在完成之前失敗。

對於具有大量記錄的事件記錄檔，處理時間的差異可能很可觀。 在事件記錄檔中具有2000記錄的 Windows 2000 型測試電腦上，在命令視窗中抓取所有事件並顯示這些事件的半同步查詢花費了10分鐘的45秒。 執行相同作業的非同步查詢花費了一分鐘54秒。

## <a name="examples"></a>範例

下列 VBScript 會以非同步方式查詢所有記錄的事件記錄檔。


```VB
Const POPUP_DURATION = 10
Const OK_BUTTON = 0
Set objWSHShell = Wscript.CreateObject("Wscript.Shell")
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
objWMIService.InstancesOfAsync objSink, "Win32_NTLogEvent"
errReturn = objWshShell.Popup("Retrieving events", POPUP_DURATION, _
"Event Retrieval", OK_BUTTON)
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
 WScript.Echo "Asynchronous operation is done."
End Sub
Sub SINK_OnObjectReady(objEvent, objAsyncContext)
 Wscript.Echo "Category: " & objEvent.Category
 Wscript.Echo "Computer Name: " & objEvent.ComputerName
 Wscript.Echo "Event Code: " & objEvent.EventCode
 Wscript.Echo "Message: " & objEvent.Message
 Wscript.Echo "Record Number: " & objEvent.RecordNumber
 Wscript.Echo "Source Name: " & objEvent.SourceName
 Wscript.Echo "Time Written: " & objEvent.TimeWritten
 Wscript.Echo "Event Type: " & objEvent.Type
 Wscript.Echo "User: " & objEvent.User
End Sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>>wbemdisp.tlb。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>wbemdisp.tlb .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSink<br/> CLSID \_ SWbemSinkEvents<br/>                           |
| IID<br/>                      | IID \_ ISWbemSink<br/> IID \_ ISWbemSinkEvents<br/>                             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[腳本 API 物件](scripting-api-objects.md)
</dt> </dl>

 

 




