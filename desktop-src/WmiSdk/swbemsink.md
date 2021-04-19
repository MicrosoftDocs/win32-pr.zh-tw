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
# <a name="swbemsink-object"></a><span data-ttu-id="90c8a-103">SWbemSink 物件</span><span class="sxs-lookup"><span data-stu-id="90c8a-103">SWbemSink object</span></span>

<span data-ttu-id="90c8a-104">**SWbemSink** 物件是由用戶端應用程式所執行，以接收非同步作業和事件通知的結果。</span><span class="sxs-lookup"><span data-stu-id="90c8a-104">The **SWbemSink** object is implemented by client applications to receive the results of asynchronous operations and event notifications.</span></span> <span data-ttu-id="90c8a-105">若要進行非同步呼叫，您必須建立 **SWbemSink** 物件的實例，並將它傳遞為 *ObjWbemSink* 參數。</span><span class="sxs-lookup"><span data-stu-id="90c8a-105">To make an asynchronous call, you must create an instance of an **SWbemSink** object and pass it as the *ObjWbemSink* parameter.</span></span> <span data-ttu-id="90c8a-106">當傳回狀態或結果時，或當呼叫完成時，會觸發 **SWbemSink** 的執行中的事件。</span><span class="sxs-lookup"><span data-stu-id="90c8a-106">The events in your implementation of **SWbemSink** are triggered when status or results are returned, or when the call is complete.</span></span> <span data-ttu-id="90c8a-107">VBScript **CreateObject** 呼叫會建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="90c8a-107">The VBScript **CreateObject** call creates this object.</span></span>

## <a name="members"></a><span data-ttu-id="90c8a-108">成員</span><span class="sxs-lookup"><span data-stu-id="90c8a-108">Members</span></span>

<span data-ttu-id="90c8a-109">**SWbemSink** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="90c8a-109">The **SWbemSink** object has these types of members:</span></span>

-   [<span data-ttu-id="90c8a-110">方法</span><span class="sxs-lookup"><span data-stu-id="90c8a-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="90c8a-111">方法</span><span class="sxs-lookup"><span data-stu-id="90c8a-111">Methods</span></span>

<span data-ttu-id="90c8a-112">**SWbemSink** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="90c8a-112">The **SWbemSink** object has these methods.</span></span>



| <span data-ttu-id="90c8a-113">方法</span><span class="sxs-lookup"><span data-stu-id="90c8a-113">Method</span></span>                             | <span data-ttu-id="90c8a-114">描述</span><span class="sxs-lookup"><span data-stu-id="90c8a-114">Description</span></span>                                                                        |
|:-----------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="90c8a-115">**取消**</span><span class="sxs-lookup"><span data-stu-id="90c8a-115">**Cancel**</span></span>](swbemsink-cancel.md) | <span data-ttu-id="90c8a-116">取消與此接收相關聯的所有非同步作業。</span><span class="sxs-lookup"><span data-stu-id="90c8a-116">Cancels all asynchronous operations that are associated with this sink.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="90c8a-117">備註</span><span class="sxs-lookup"><span data-stu-id="90c8a-117">Remarks</span></span>

<span data-ttu-id="90c8a-118">非同步回呼可讓未經驗證的使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="90c8a-118">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="90c8a-119">這會對您的腳本和應用程式帶來安全性風險。</span><span class="sxs-lookup"><span data-stu-id="90c8a-119">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="90c8a-120">若要消除風險，請使用兩個同步通訊或同步通訊。</span><span class="sxs-lookup"><span data-stu-id="90c8a-120">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="90c8a-121">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="90c8a-121">For more information, see [Calling a Method](calling-a-method.md).</span></span>

### <a name="events"></a><span data-ttu-id="90c8a-122">事件</span><span class="sxs-lookup"><span data-stu-id="90c8a-122">Events</span></span>

<span data-ttu-id="90c8a-123">您可以在觸發事件時，執行要呼叫的副程式。</span><span class="sxs-lookup"><span data-stu-id="90c8a-123">You can implement subroutines to be called when events are triggered.</span></span> <span data-ttu-id="90c8a-124">例如，如果您想要處理非同步查詢呼叫（例如 [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)）所傳回的每個物件，請使用非同步呼叫中指定的接收來建立副程式，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="90c8a-124">For example, if you want to process each object that is returned by an asynchronous query call such as [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), create a subroutine using the sink that is specified in the asynchronous call, as shown in the following example.</span></span>


```VB
Sub SinkName_OnObjectReady(objObject, objAsyncContext)
```



<span data-ttu-id="90c8a-125">使用下表做為參考，以識別事件和觸發程式描述。</span><span class="sxs-lookup"><span data-stu-id="90c8a-125">Use the following table as a reference to identify events and trigger descriptions.</span></span>



| <span data-ttu-id="90c8a-126">事件</span><span class="sxs-lookup"><span data-stu-id="90c8a-126">Event</span></span>                                            | <span data-ttu-id="90c8a-127">描述</span><span class="sxs-lookup"><span data-stu-id="90c8a-127">Description</span></span>                                                             |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="90c8a-128">**OnCompleted**</span><span class="sxs-lookup"><span data-stu-id="90c8a-128">**OnCompleted**</span></span>](swbemsink-oncompleted.md)     | <span data-ttu-id="90c8a-129">在非同步作業完成時觸發。</span><span class="sxs-lookup"><span data-stu-id="90c8a-129">Triggered when an asynchronous operation is complete.</span></span>                   |
| [<span data-ttu-id="90c8a-130">**OnObjectPut**</span><span class="sxs-lookup"><span data-stu-id="90c8a-130">**OnObjectPut**</span></span>](swbemsink-onobjectput.md)     | <span data-ttu-id="90c8a-131">在非同步 Put 作業完成時觸發。</span><span class="sxs-lookup"><span data-stu-id="90c8a-131">Triggered when an asynchronous Put operation is complete.</span></span>               |
| [<span data-ttu-id="90c8a-132">**OnObjectReady**</span><span class="sxs-lookup"><span data-stu-id="90c8a-132">**OnObjectReady**</span></span>](swbemsink-onobjectready.md) | <span data-ttu-id="90c8a-133">當非同步呼叫提供的物件可用時觸發。</span><span class="sxs-lookup"><span data-stu-id="90c8a-133">Triggered when an object provided by an asynchronous call is available.</span></span> |
| [<span data-ttu-id="90c8a-134">**OnProgress**</span><span class="sxs-lookup"><span data-stu-id="90c8a-134">**OnProgress**</span></span>](swbemsink-onprogress.md)       | <span data-ttu-id="90c8a-135">觸發以提供非同步作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="90c8a-135">Triggered to provide the status of a asynchronous operation.</span></span>            |



 

<span data-ttu-id="90c8a-136">**非同步地取出事件記錄檔統計資料**</span><span class="sxs-lookup"><span data-stu-id="90c8a-136">**Asynchronously Retrieving Event Log Statistics**</span></span>

<span data-ttu-id="90c8a-137">WMI 支援非同步和半同步腳本。</span><span class="sxs-lookup"><span data-stu-id="90c8a-137">WMI supports both asynchronous and semi-synchronous scripts.</span></span> <span data-ttu-id="90c8a-138">從事件記錄檔取得事件時，非同步腳本通常會以更快的速度來取得此資料。</span><span class="sxs-lookup"><span data-stu-id="90c8a-138">When retrieving events from the event logs, asynchronous scripts often retrieve this data much faster.</span></span>

<span data-ttu-id="90c8a-139">在非同步腳本中，會發出查詢，並立即將控制權傳回給腳本。</span><span class="sxs-lookup"><span data-stu-id="90c8a-139">In an asynchronous script, a query is issued and control is immediately returned to the script.</span></span> <span data-ttu-id="90c8a-140">此查詢會繼續在不同的執行緒上進行處理，而腳本會開始立即對傳回的資訊採取動作。</span><span class="sxs-lookup"><span data-stu-id="90c8a-140">The query continues to process on a separate thread while the script begins to immediately act on the information that is returned.</span></span> <span data-ttu-id="90c8a-141">非同步腳本是事件驅動：每次抓取事件記錄時，就會引發 OnObjectReady 事件。</span><span class="sxs-lookup"><span data-stu-id="90c8a-141">Asynchronous scripts are event driven: each time an event record is retrieved, the OnObjectReady event is fired.</span></span> <span data-ttu-id="90c8a-142">當查詢完成時，將會引發 OnCompleted 事件，而腳本可以根據已傳回所有可用記錄的事實繼續進行。</span><span class="sxs-lookup"><span data-stu-id="90c8a-142">When the query has completed, the OnCompleted event will fire, and the script can continue based on the fact that all the available records have been returned.</span></span>

<span data-ttu-id="90c8a-143">相反地，在半同步腳本中，會發出查詢，然後腳本會將大量抓取的資訊排入佇列，然後再進行處理。</span><span class="sxs-lookup"><span data-stu-id="90c8a-143">In a semi-synchronous script, by contrast, a query is issued and the script then queues a large amount of retrieved information before acting upon it.</span></span> <span data-ttu-id="90c8a-144">對於許多物件而言，半同步處理已足夠;例如，在查詢磁片磁碟機的屬性時，在發出查詢的時間與傳回並處理資訊的時間之間可能只有一個分割秒。</span><span class="sxs-lookup"><span data-stu-id="90c8a-144">For many objects, semi-synchronous processing is adequate; for example, when querying a disk drive for its properties, there might be only a split second between the time the query is issued and the time the information is returned and acted upon.</span></span> <span data-ttu-id="90c8a-145">這是因為傳回的資訊數量相對較小，這是很大的部分。</span><span class="sxs-lookup"><span data-stu-id="90c8a-145">This is due in large part to the fact that the amount of information returned is relatively small.</span></span>

<span data-ttu-id="90c8a-146">不過，在查詢事件記錄檔時，查詢發出的時間間隔和半同步腳本可以完成傳回和處理資訊的時間可能需要數小時。</span><span class="sxs-lookup"><span data-stu-id="90c8a-146">When querying an event log, however, the interval between the time the query is issued and the time that a semi-synchronous script can finish returning and acting on the information can take hours.</span></span> <span data-ttu-id="90c8a-147">最重要的是，腳本可能會用盡記憶體，並在完成之前失敗。</span><span class="sxs-lookup"><span data-stu-id="90c8a-147">On top of that, the script might run out of memory and fail on its own before completing.</span></span>

<span data-ttu-id="90c8a-148">對於具有大量記錄的事件記錄檔，處理時間的差異可能很可觀。</span><span class="sxs-lookup"><span data-stu-id="90c8a-148">For event logs with a large number of records, the difference in processing time can be considerable.</span></span> <span data-ttu-id="90c8a-149">在事件記錄檔中具有2000記錄的 Windows 2000 型測試電腦上，在命令視窗中抓取所有事件並顯示這些事件的半同步查詢花費了10分鐘的45秒。</span><span class="sxs-lookup"><span data-stu-id="90c8a-149">On a Windows 2000-based test computer with 2,000 records in the event log, a semi-synchronous query that retrieved all the events and displayed them in a command window took 10 minutes 45 seconds.</span></span> <span data-ttu-id="90c8a-150">執行相同作業的非同步查詢花費了一分鐘54秒。</span><span class="sxs-lookup"><span data-stu-id="90c8a-150">An asynchronous query that performed the same operation took one minute 54 seconds.</span></span>

## <a name="examples"></a><span data-ttu-id="90c8a-151">範例</span><span class="sxs-lookup"><span data-stu-id="90c8a-151">Examples</span></span>

<span data-ttu-id="90c8a-152">下列 VBScript 會以非同步方式查詢所有記錄的事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="90c8a-152">The following VBScript asynchronously queries the event logs for all records.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="90c8a-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="90c8a-153">Requirements</span></span>



| <span data-ttu-id="90c8a-154">需求</span><span class="sxs-lookup"><span data-stu-id="90c8a-154">Requirement</span></span> | <span data-ttu-id="90c8a-155">值</span><span class="sxs-lookup"><span data-stu-id="90c8a-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90c8a-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90c8a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="90c8a-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90c8a-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="90c8a-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90c8a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="90c8a-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90c8a-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="90c8a-160">標頭</span><span class="sxs-lookup"><span data-stu-id="90c8a-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="90c8a-161"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="90c8a-161"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="90c8a-162">Idl</span><span class="sxs-lookup"><span data-stu-id="90c8a-162">IDL</span></span><br/>                      | <dl> <span data-ttu-id="90c8a-163"><dt>>wbemdisp.tlb .idl</dt></span><span class="sxs-lookup"><span data-stu-id="90c8a-163"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="90c8a-164">DLL</span><span class="sxs-lookup"><span data-stu-id="90c8a-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90c8a-165"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90c8a-165"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="90c8a-166">CLSID</span><span class="sxs-lookup"><span data-stu-id="90c8a-166">CLSID</span></span><br/>                    | <span data-ttu-id="90c8a-167">CLSID \_ SWbemSink</span><span class="sxs-lookup"><span data-stu-id="90c8a-167">CLSID\_SWbemSink</span></span><br/> <span data-ttu-id="90c8a-168">CLSID \_ SWbemSinkEvents</span><span class="sxs-lookup"><span data-stu-id="90c8a-168">CLSID\_SWbemSinkEvents</span></span><br/>                           |
| <span data-ttu-id="90c8a-169">IID</span><span class="sxs-lookup"><span data-stu-id="90c8a-169">IID</span></span><br/>                      | <span data-ttu-id="90c8a-170">IID \_ ISWbemSink</span><span class="sxs-lookup"><span data-stu-id="90c8a-170">IID\_ISWbemSink</span></span><br/> <span data-ttu-id="90c8a-171">IID \_ ISWbemSinkEvents</span><span class="sxs-lookup"><span data-stu-id="90c8a-171">IID\_ISWbemSinkEvents</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="90c8a-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90c8a-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90c8a-173">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="90c8a-173">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




