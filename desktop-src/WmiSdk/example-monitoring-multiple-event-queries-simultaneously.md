---
description: 下列腳本範例顯示非同步事件通知，利用 SWbemServices.Exe的 cNotificationQueryAsync 方法和 SWbemSink 物件。
ms.assetid: 8beb9804-088e-4dd1-adc8-a29ca450a220
ms.tgt_platform: multiple
title: 範例：同時監視多個事件查詢
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d70aff849cce81d6628b80f39e57a7f2430af056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975799"
---
# <a name="example-monitoring-multiple-event-queries-simultaneously"></a><span data-ttu-id="4dd9b-103">範例：同時監視多個事件查詢</span><span class="sxs-lookup"><span data-stu-id="4dd9b-103">Example: Monitoring Multiple Event Queries Simultaneously</span></span>

<span data-ttu-id="4dd9b-104">下列腳本範例顯示非同步事件通知，利用 [**SWbemServices.Exe的 cNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) 方法和 [**SWbemSink**](swbemsink.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="4dd9b-104">The following script example shows asynchronous event notification, making use of the [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) method and [**SWbemSink**](swbemsink.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="4dd9b-105">由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。</span><span class="sxs-lookup"><span data-stu-id="4dd9b-105">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="4dd9b-106">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="4dd9b-106">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 


```VB
Dim WithEvents sink As SWbemSink

Private Sub ExecNoteAsync_Click()

    Dim services As SWbemServices
    Dim strQuery As String
    Dim cntxt As SWbemNamedValueSet
    Set sink = New SWbemSink
    Set services = GetObject( _
        "winmgmts:{impersonationLevel=impersonate,(security)}")
    strQuery = "SELECT * FROM __InstanceCreationEvent "& _
                "WHERE TargetInstance ISA 'Win32_NTLogEvent'"
    Set cntxt = New SWbemNamedValueSet
    cntxt.Add "sinkname", "ExecNoteAsync"
    services.Security_.Privileges.Add (wbemPrivilegeSecurity)
    services.ExecNotificationQueryAsync sink, strQuery, , , , cntxt
    MsgBox "This program will asynchronously " _
        & "process Win32_NTLogEvent events."
        
End Sub

Private Sub sink_OnObjectReady( _
             ByVal objWbemObject As WbemScripting.ISWbemObject, 
             ByVal objWbemAsyncContext As _
                 WbemScripting.ISWbemNamedValueSet)
  On Error GoTo ErrorHandler
    Dim cntxt_item As WbemScripting.SWbemNamedValue

    Set cntxt_item = objWbemAsyncContext.Item("sinkname")
        
    If cntxt_item.Value = "ExecNoteAsync" Then
        MsgBox " Got event: " & objWbemObject.TargetInstance.Message
    End If

    Set objWbemObject = Nothing

    Exit Sub                                   ' Exit to avoid handler

ErrorHandler:
    MsgBox "Error number: " & Str(Err.Number) & vbNewLine & _
    "Description: " & Err.Description, vbCritical
End Sub
```



 

 



