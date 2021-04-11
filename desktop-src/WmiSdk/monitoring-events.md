---
description: 系統管理員可以使用 WMI 來監視網路上的事件。
ms.assetid: 871d4add-a7b1-4ec9-a202-3821fdf09e9f
ms.tgt_platform: multiple
title: 監視事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea5d9fc6f9a12f4aa1fb7bc0ff6f66fc4dd4a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114277"
---
# <a name="monitoring-events"></a><span data-ttu-id="3f93b-103">監視事件</span><span class="sxs-lookup"><span data-stu-id="3f93b-103">Monitoring Events</span></span>

<span data-ttu-id="3f93b-104">系統管理員可以使用 WMI 來監視網路上的事件。</span><span class="sxs-lookup"><span data-stu-id="3f93b-104">System administrators can use WMI to monitor events on a network.</span></span> <span data-ttu-id="3f93b-105">例如：</span><span class="sxs-lookup"><span data-stu-id="3f93b-105">For example:</span></span>

-   <span data-ttu-id="3f93b-106">服務意外停止。</span><span class="sxs-lookup"><span data-stu-id="3f93b-106">A service stops unexpectedly.</span></span>
-   <span data-ttu-id="3f93b-107">伺服器變得無法使用。</span><span class="sxs-lookup"><span data-stu-id="3f93b-107">A server becomes unavailable.</span></span>
-   <span data-ttu-id="3f93b-108">磁片磁碟機填滿80% 的容量。</span><span class="sxs-lookup"><span data-stu-id="3f93b-108">A disk drive fills to 80% capacity.</span></span>
-   <span data-ttu-id="3f93b-109">安全性事件會回報給 NT 事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="3f93b-109">Security events are reported to an NT Event Log.</span></span>

<span data-ttu-id="3f93b-110">WMI 支援事件偵測並傳遞給事件取用者，因為某些 WMI 提供者是事件提供者。</span><span class="sxs-lookup"><span data-stu-id="3f93b-110">WMI supports event detection and delivery to event consumers because some WMI providers are event providers.</span></span> <span data-ttu-id="3f93b-111">如需詳細資訊，請參閱 [接收 WMI 事件](receiving-a-wmi-event.md)。</span><span class="sxs-lookup"><span data-stu-id="3f93b-111">For more information, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="3f93b-112">[*事件取用者*](gloss-e.md) 是要求事件通知的應用程式或腳本，然後在發生特定事件時執行工作。</span><span class="sxs-lookup"><span data-stu-id="3f93b-112">[*Event consumers*](gloss-e.md) are applications or scripts that request notification of events, and then perform tasks when specific events occur.</span></span> <span data-ttu-id="3f93b-113">您可以建立事件監視腳本，或在事件發生時暫時監視的應用程式。</span><span class="sxs-lookup"><span data-stu-id="3f93b-113">You can create event monitoring scripts or applications that temporarily monitor when events occur.</span></span> <span data-ttu-id="3f93b-114">WMI 也提供一組預先安裝的永久事件提供者和永久的取用者類別，可讓您永久監視事件。</span><span class="sxs-lookup"><span data-stu-id="3f93b-114">WMI also supplies a set of preinstalled permanent event providers and the permanent consumer classes that enable you to permanently monitor events.</span></span> <span data-ttu-id="3f93b-115">如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="3f93b-115">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="3f93b-116">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="3f93b-116">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="3f93b-117">使用暫存事件取用者</span><span class="sxs-lookup"><span data-stu-id="3f93b-117">Using Temporary Event Consumers</span></span>](#using-temporary-event-consumers)
-   [<span data-ttu-id="3f93b-118">使用永久事件取用者</span><span class="sxs-lookup"><span data-stu-id="3f93b-118">Using Permanent Event Consumers</span></span>](#using-permanent-event-consumers)

## <a name="using-temporary-event-consumers"></a><span data-ttu-id="3f93b-119">使用暫存事件取用者</span><span class="sxs-lookup"><span data-stu-id="3f93b-119">Using Temporary Event Consumers</span></span>

<span data-ttu-id="3f93b-120">暫存事件取用者是傳回符合事件查詢或篩選準則之事件的腳本或應用程式。</span><span class="sxs-lookup"><span data-stu-id="3f93b-120">Temporary event consumers are scripts or applications that return the events that match an event query or filter.</span></span> <span data-ttu-id="3f93b-121">暫存事件查詢通常會使用 c + + 應用程式中的 [**IWbemServices：： ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) 或腳本和 Visual Basic 中的 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) 。</span><span class="sxs-lookup"><span data-stu-id="3f93b-121">Temporary event queries usually use either [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ applications or [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) in scripts and Visual Basic.</span></span>

<span data-ttu-id="3f93b-122">事件查詢會要求事件類別的實例，以指定特定類型的事件，例如 [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) 或 [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)。</span><span class="sxs-lookup"><span data-stu-id="3f93b-122">An event query requests instances of an event class that specifies a certain type of event, such as [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) or [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span>

<span data-ttu-id="3f93b-123">下列 VBScript 程式碼範例會在建立 [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) 的實例時要求通知。</span><span class="sxs-lookup"><span data-stu-id="3f93b-123">The following VBScript code example requests notification when an instance of [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) is created.</span></span> <span data-ttu-id="3f93b-124">當處理常式啟動或停止時，就會產生這個類別的實例。</span><span class="sxs-lookup"><span data-stu-id="3f93b-124">An instance of this class is generated when a process is started or stopped.</span></span>

<span data-ttu-id="3f93b-125">若要執行腳本，請將它複製到名為 event.vbs 的檔案，並使用下列命令列： **cscript event.vbs**。</span><span class="sxs-lookup"><span data-stu-id="3f93b-125">To execute the script, copy it to a file named event.vbs and use the following command line: **cscript event.vbs**.</span></span> <span data-ttu-id="3f93b-126">您可以啟動 Notepad.exe 或任何其他進程，查看腳本的輸出。</span><span class="sxs-lookup"><span data-stu-id="3f93b-126">You can see output from the script by starting Notepad.exe or any other process.</span></span> <span data-ttu-id="3f93b-127">腳本會在五個進程啟動或停止之後停止。</span><span class="sxs-lookup"><span data-stu-id="3f93b-127">The script stops after five processes have started or stopped.</span></span>

<span data-ttu-id="3f93b-128">此腳本會呼叫 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)，這是方法的最 [*半同步*](gloss-s.md) 版本。</span><span class="sxs-lookup"><span data-stu-id="3f93b-128">This script calls [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md), which is the [*semisynchronous*](gloss-s.md) version of the method.</span></span> <span data-ttu-id="3f93b-129">請參閱下一個腳本，以取得透過呼叫 [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)來設定非同步暫存事件訂閱的範例。</span><span class="sxs-lookup"><span data-stu-id="3f93b-129">See the next script for an example of setting up an asynchronous temporary event subscription by calling [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span></span> <span data-ttu-id="3f93b-130">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="3f93b-130">For more information, see [Calling a Method](calling-a-method.md).</span></span> <span data-ttu-id="3f93b-131">腳本會呼叫 [**SWbemEventSource**](swbemeventsource-nextevent.md) ，以在每個事件抵達時取得並處理它。</span><span class="sxs-lookup"><span data-stu-id="3f93b-131">The script calls [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) to obtain and process each event as it arrives.</span></span> <span data-ttu-id="3f93b-132">將腳本儲存在副檔名為 .vbs 的檔案中，並使用 CScript： **cscript file.vbs** 在命令列上執行腳本。</span><span class="sxs-lookup"><span data-stu-id="3f93b-132">Save the script in a file with a .vbs extension and run the script on a command line using CScript: **cscript file.vbs**.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM Win32_ProcessTrace")

Wscript.Echo "Waiting for events ..."
i = 0
Do Until i=5
    Set objReceivedEvent = objEvents.NextEvent
    'report an event
    Wscript.Echo "Win32_ProcessTrace event occurred" & VBNewLine _
        & "Process Name = " _
            & objReceivedEvent.ProcessName & VBNewLine _
        & "Process ID = " _
            & objReceivedEvent.Processid & VBNewLine _
        & "Session ID = " & objReceivedEvent.SessionID 
i = i+ 1
Loop
```



暫存事件取用者必須以手動方式啟動，而且不得跨 WMI 重新開機或作業系統重新開機來保存。 <span data-ttu-id="3f93b-134">暫存事件取用者只能在執行時處理事件。</span><span class="sxs-lookup"><span data-stu-id="3f93b-134">A temporary event consumer can process events only while it is running.</span></span>

<span data-ttu-id="3f93b-135">下列程式描述如何建立暫存事件取用者。</span><span class="sxs-lookup"><span data-stu-id="3f93b-135">The following procedure describes how to create a temporary event consumer.</span></span>

<span data-ttu-id="3f93b-136">**建立暫存事件取用者**</span><span class="sxs-lookup"><span data-stu-id="3f93b-136">**To create a temporary event consumer**</span></span>

1.  <span data-ttu-id="3f93b-137">決定要使用的程式設計語言。</span><span class="sxs-lookup"><span data-stu-id="3f93b-137">Decide which programming language to use.</span></span>

    <span data-ttu-id="3f93b-138">程式設計語言會決定要使用的 API。</span><span class="sxs-lookup"><span data-stu-id="3f93b-138">The programming language determines the API to use.</span></span>

    -   <span data-ttu-id="3f93b-139">針對 c + + 程式設計語言，請使用 [適用于 WMI 的 COM API](com-api-for-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="3f93b-139">For the C++ programming language, use the [COM API for WMI](com-api-for-wmi.md).</span></span>
    -   <span data-ttu-id="3f93b-140">針對 Visual Basic 或指令碼語言，請使用 [適用于 WMI 的腳本 API](scripting-api-for-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="3f93b-140">For Visual Basic or scripting languages, use the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

2.  <span data-ttu-id="3f93b-141">以您啟動 WMI 應用程式的相同方式開始撰寫暫存事件取用者應用程式的程式碼。</span><span class="sxs-lookup"><span data-stu-id="3f93b-141">Start coding a temporary event consumer application the same way that you start a WMI application.</span></span>

    <span data-ttu-id="3f93b-142">程式碼的第一個步驟取決於程式設計語言。</span><span class="sxs-lookup"><span data-stu-id="3f93b-142">The first steps of coding depend on the programming language.</span></span> <span data-ttu-id="3f93b-143">一般來說，您會登入 WMI 並設定安全性設定。</span><span class="sxs-lookup"><span data-stu-id="3f93b-143">Typically, you log onto WMI and set up the security settings.</span></span> <span data-ttu-id="3f93b-144">如需詳細資訊，請參閱 [建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)。</span><span class="sxs-lookup"><span data-stu-id="3f93b-144">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

3.  <span data-ttu-id="3f93b-145">定義您想要使用的事件查詢。</span><span class="sxs-lookup"><span data-stu-id="3f93b-145">Define the event query that you want to use.</span></span>

    <span data-ttu-id="3f93b-146">若要取得某些類型的效能資料，您可能需要使用高效能提供者所提供的類別。</span><span class="sxs-lookup"><span data-stu-id="3f93b-146">To obtain some types of performance data, you may need to use classes provided by high-performance providers.</span></span> <span data-ttu-id="3f93b-147">如需詳細資訊，請參閱 [監視效能資料](monitoring-performance-data.md)、 [判斷要接收的事件種類](determining-the-type-of-event-to-receive.md)，以及 [使用 WQL 查詢](querying-with-wql.md)。</span><span class="sxs-lookup"><span data-stu-id="3f93b-147">For more information, see [Monitoring Performance Data](monitoring-performance-data.md), [Determining the Type of Event To Receive](determining-the-type-of-event-to-receive.md), and [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="3f93b-148">決定要進行非同步呼叫或半執行呼叫，然後選擇 API 方法。</span><span class="sxs-lookup"><span data-stu-id="3f93b-148">Decide to make either an asynchronous call or an semisynchronous call, and choose the API method.</span></span>

    <span data-ttu-id="3f93b-149">非同步呼叫可讓您避免輪詢資料的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="3f93b-149">Asynchronous calls allow you to avoid the overhead of polling for data.</span></span> <span data-ttu-id="3f93b-150">不過，半同步呼叫可提供類似的效能，並提供更高的安全性。</span><span class="sxs-lookup"><span data-stu-id="3f93b-150">However, semisynchronous calls provide similar performance with greater security.</span></span> <span data-ttu-id="3f93b-151">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="3f93b-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

5.  <span data-ttu-id="3f93b-152">進行非同步或半同步方法呼叫，並將事件查詢包含為 *strQuery* 參數。</span><span class="sxs-lookup"><span data-stu-id="3f93b-152">Make the asynchronous or semisynchronous method call and include an event query as the *strQuery* parameter.</span></span>

    <span data-ttu-id="3f93b-153">若是 c + + 應用程式，請呼叫下列方法：</span><span class="sxs-lookup"><span data-stu-id="3f93b-153">For C++ applications, call the following methods:</span></span>

    -   [<span data-ttu-id="3f93b-154">**IWbemServices：： ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="3f93b-154">**IWbemServices::ExecNotificationQuery**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
    -   [<span data-ttu-id="3f93b-155">**IWbemServices：： ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="3f93b-155">**IWbemServices::ExecNotificationQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    <span data-ttu-id="3f93b-156">針對腳本，請呼叫下列方法：</span><span class="sxs-lookup"><span data-stu-id="3f93b-156">For scripts, call the following methods:</span></span>

    -   [<span data-ttu-id="3f93b-157">**SWbemServices.ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="3f93b-157">**SWbemServices.ExecNotificationQuery**</span></span>](swbemservices-execnotificationquery.md)
    -   [<span data-ttu-id="3f93b-158">**SWbemServices.ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="3f93b-158">**SWbemServices.ExecNotificationQueryAsync**</span></span>](swbemservices-execnotificationqueryasync.md)

6.  <span data-ttu-id="3f93b-159">撰寫程式碼來處理傳回的事件物件。</span><span class="sxs-lookup"><span data-stu-id="3f93b-159">Write the code to process the returned event object.</span></span>

    <span data-ttu-id="3f93b-160">若為非同步事件查詢，請將程式碼放在物件接收的各種方法或事件中。</span><span class="sxs-lookup"><span data-stu-id="3f93b-160">For asynchronous event queries, put the code in the various methods or events of the object sink.</span></span> <span data-ttu-id="3f93b-161">若為半活動查詢，每個物件會在 WMI 取得時傳回，因此程式碼應該在處理每個物件的迴圈中。</span><span class="sxs-lookup"><span data-stu-id="3f93b-161">For semisynchronous event queries, each object is returned as WMI obtains it, so the code should be in the loop that handles each object.</span></span>

<span data-ttu-id="3f93b-162">下列腳本程式碼範例是 [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) 腳本的非同步版本。</span><span class="sxs-lookup"><span data-stu-id="3f93b-162">The following script code example is an asynchronous version of the [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) script.</span></span> <span data-ttu-id="3f93b-163">由於非同步作業會立即傳回，因此當腳本正在等候事件時，對話方塊會保持作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="3f93b-163">Because asynchronous operations return immediately, a dialog box keeps the script active while it is waiting for events.</span></span>

<span data-ttu-id="3f93b-164">腳本會有 [**SWbemSink OnObjectReady**](swbemsink-onobjectready.md)事件的事件處理常式，而不是呼叫 [**SWbemEventSource NextEvent**](swbemeventsource-nextevent.md)來接收每個事件。</span><span class="sxs-lookup"><span data-stu-id="3f93b-164">Rather than call [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) to receive each event, the script has an event handler for the [**SWbemSink OnObjectReady**](swbemsink-onobjectready.md) event.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\CIMV2") 
Set EventSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync EventSink, _
    "SELECT * FROM Win32_ProcessTrace WITHIN 10"
WScript.Echo "Waiting for events..."

i = 0
While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "Win32_ProcessTrace event has occurred."
    i = i+1
    If i = 3 Then WScript.Quit 0 
End Sub

```



> [!Note]
>
> <span data-ttu-id="3f93b-165">非同步回呼，例如副程式所處理的回呼 `SINK_OnObjectReady` ，可讓 nonauthenticated 使用者提供資料給接收。</span><span class="sxs-lookup"><span data-stu-id="3f93b-165">An asynchronous callback such as a callback handled by the `SINK_OnObjectReady` subroutine, allows a nonauthenticated user to provide data to the sink.</span></span> <span data-ttu-id="3f93b-166">為了獲得更好的安全性，請使用兩個同步通訊或同步通訊。</span><span class="sxs-lookup"><span data-stu-id="3f93b-166">For better security, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="3f93b-167">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="3f93b-167">For more information, see the following topics:</span></span>
>
> -   [<span data-ttu-id="3f93b-168">使用 c + + 進行半同步呼叫</span><span class="sxs-lookup"><span data-stu-id="3f93b-168">Making a Semisynchronous Call with C++</span></span>](making-a-semisynchronous-call-with-c--.md)
> -   [<span data-ttu-id="3f93b-169">使用 VBScript 進行半同步呼叫</span><span class="sxs-lookup"><span data-stu-id="3f93b-169">Making a Semisynchronous Call with VBScript</span></span>](making-a-semisynchronous-call-with-vbscript.md)
> -   [<span data-ttu-id="3f93b-170">使用 c + + 進行非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="3f93b-170">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
> -   [<span data-ttu-id="3f93b-171">使用 VBScript 進行非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="3f93b-171">Making an Asynchronous Call with VBScript</span></span>](making-an-asynchronous-call-with-vbscript.md)
> -   [<span data-ttu-id="3f93b-172">在非同步呼叫上設定安全性</span><span class="sxs-lookup"><span data-stu-id="3f93b-172">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
> -   [<span data-ttu-id="3f93b-173">保護腳本用戶端</span><span class="sxs-lookup"><span data-stu-id="3f93b-173">Securing Scripting Clients</span></span>](securing-scripting-clients.md)

 

## <a name="using-permanent-event-consumers"></a><span data-ttu-id="3f93b-174">使用永久事件取用者</span><span class="sxs-lookup"><span data-stu-id="3f93b-174">Using Permanent Event Consumers</span></span>

<span data-ttu-id="3f93b-175">永久事件取用者會執行，直到明確取消其註冊，然後在 WMI 或系統重新開機時啟動。</span><span class="sxs-lookup"><span data-stu-id="3f93b-175">A permanent event consumer runs until its registration is explicitly canceled, and then starts up when WMI or the system restarts.</span></span>

<span data-ttu-id="3f93b-176">永久事件取用者是系統上 WMI 類別、篩選和 COM 物件的組合。</span><span class="sxs-lookup"><span data-stu-id="3f93b-176">A permanent event consumer is a combination of WMI classes, filters, and COM objects on a system.</span></span>

<span data-ttu-id="3f93b-177">下列清單會識別建立永久性事件取用者所需的元件：</span><span class="sxs-lookup"><span data-stu-id="3f93b-177">The following list identifies the parts required to create a permanent event consumer:</span></span>

-   <span data-ttu-id="3f93b-178">COM 物件，其中包含可執行永久取用者的程式碼。</span><span class="sxs-lookup"><span data-stu-id="3f93b-178">A COM object containing the code that implements the permanent consumer.</span></span>
-   <span data-ttu-id="3f93b-179">新的永久取用者類別。</span><span class="sxs-lookup"><span data-stu-id="3f93b-179">A new permanent consumer class.</span></span>
-   <span data-ttu-id="3f93b-180">永久取用者類別的實例。</span><span class="sxs-lookup"><span data-stu-id="3f93b-180">An instance of the permanent consumer class.</span></span>
-   <span data-ttu-id="3f93b-181">包含事件查詢的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="3f93b-181">A filter that contains the query for events.</span></span>
-   <span data-ttu-id="3f93b-182">取用者與篩選之間的連結。</span><span class="sxs-lookup"><span data-stu-id="3f93b-182">A link between the consumer and the filter.</span></span>

<span data-ttu-id="3f93b-183">如需詳細資訊，請參閱 [所有時間的接收事件](--filtertoconsumerbinding.md)。</span><span class="sxs-lookup"><span data-stu-id="3f93b-183">For more information, see [Receiving Events At All Times](--filtertoconsumerbinding.md).</span></span>

<span data-ttu-id="3f93b-184">WMI 提供數個永久取用者。</span><span class="sxs-lookup"><span data-stu-id="3f93b-184">WMI supplies several permanent consumers.</span></span> <span data-ttu-id="3f93b-185">已預先安裝包含程式碼的取用者類別和 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="3f93b-185">The consumer classes and COM object containing the code are preinstalled.</span></span> <span data-ttu-id="3f93b-186">例如，您可以建立並設定 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 類別的實例，以便在發生事件時執行腳本。</span><span class="sxs-lookup"><span data-stu-id="3f93b-186">For example, you can create and configure an instance of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class to run a script when an event occurs.</span></span> <span data-ttu-id="3f93b-187">如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="3f93b-187">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="3f93b-188">如需使用 **ActiveScriptEventConsumer** 的範例，請參閱 [根據事件執行腳本](running-a-script-based-on-an-event.md)。</span><span class="sxs-lookup"><span data-stu-id="3f93b-188">For an example of using **ActiveScriptEventConsumer**, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md).</span></span>

<span data-ttu-id="3f93b-189">下列程式描述如何建立永久事件取用者。</span><span class="sxs-lookup"><span data-stu-id="3f93b-189">The following procedure describes how to create a permanent event consumer.</span></span>

<span data-ttu-id="3f93b-190">**建立永久事件取用者**</span><span class="sxs-lookup"><span data-stu-id="3f93b-190">**To create a permanent event consumer**</span></span>

1.  <span data-ttu-id="3f93b-191">向您使用的命名空間[註冊事件提供者](registering-a-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="3f93b-191">[Register the event provider](registering-a-provider.md) with the namespace that you are using.</span></span>

    <span data-ttu-id="3f93b-192">某些事件提供者只能使用特定的命名空間。</span><span class="sxs-lookup"><span data-stu-id="3f93b-192">Some event providers can only use a specific namespace.</span></span> <span data-ttu-id="3f93b-193">例如， [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)是 [Win32 提供者](/windows/desktop/CIMWin32Prov/win32-provider)所支援的內建事件，並且預設會與 \\ 根 \\ cimv2 命名空間一起註冊。</span><span class="sxs-lookup"><span data-stu-id="3f93b-193">For example, [**\_\_InstanceCreationEvent**](--instancecreationevent.md) is an intrinsic event that is supported by the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider) and is registered by default with the \\root\\cimv2 namespace.</span></span>

    > [!Note]  
    > <span data-ttu-id="3f93b-194">您可以使用註冊中所使用之 [**\_ \_ >eventfilter**](--eventfilter.md)的 **EventNamespace** 屬性來建立跨命名空間的訂用帳戶。</span><span class="sxs-lookup"><span data-stu-id="3f93b-194">You can use the **EventNamespace** property of the [**\_\_EventFilter**](--eventfilter.md) used in the registration to create a cross-namespace subscription.</span></span> <span data-ttu-id="3f93b-195">如需詳細資訊，請參閱 [實施跨命名空間永久事件訂閱](implementing-cross-namespace-permanent-event-subscriptions.md)。</span><span class="sxs-lookup"><span data-stu-id="3f93b-195">For more information, see [Implementing Cross-Namespace Permanent Event Subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).</span></span>

     

2.  <span data-ttu-id="3f93b-196">向事件類別所在的命名空間[註冊事件取用者提供](registering-an-event-consumer-provider.md)者。</span><span class="sxs-lookup"><span data-stu-id="3f93b-196">[Register the event consumer provider](registering-an-event-consumer-provider.md) with the namespace where event classes are located.</span></span>

    <span data-ttu-id="3f93b-197">WMI 使用事件取用者提供者來尋找永久的事件取用者。</span><span class="sxs-lookup"><span data-stu-id="3f93b-197">WMI uses an event consumer provider to find an event consumer that is permanent.</span></span> <span data-ttu-id="3f93b-198">永久事件取用者是 WMI 在收到事件時所啟動的應用程式。</span><span class="sxs-lookup"><span data-stu-id="3f93b-198">The permanent event consumer is the application that WMI starts when an event is received.</span></span> <span data-ttu-id="3f93b-199">為了註冊事件取用者，提供者會建立 [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)的實例。</span><span class="sxs-lookup"><span data-stu-id="3f93b-199">To register event consumer, providers create instances of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span></span>

3.  <span data-ttu-id="3f93b-200">建立類別的實例，代表您要使用的永久事件取用者。</span><span class="sxs-lookup"><span data-stu-id="3f93b-200">Create an instance of the class that represents the permanent event consumer you want to use.</span></span>

    <span data-ttu-id="3f93b-201">事件取用者類別衍生自類別 [**\_ \_ EventConsumer**](--eventconsumer.md)。</span><span class="sxs-lookup"><span data-stu-id="3f93b-201">Event consumer classes are derived from the class [**\_\_EventConsumer**](--eventconsumer.md).</span></span> <span data-ttu-id="3f93b-202">設定事件取用者實例所需的屬性。</span><span class="sxs-lookup"><span data-stu-id="3f93b-202">Set the properties that the event consumer instance requires.</span></span>

4.  <span data-ttu-id="3f93b-203">使用 **regsvr32** 公用程式向 COM 註冊取用者。</span><span class="sxs-lookup"><span data-stu-id="3f93b-203">Register the consumer with COM by using the **regsvr32** utility.</span></span>
5.  <span data-ttu-id="3f93b-204">建立事件篩選類別 [**\_ \_ >eventfilter**](--eventfilter.md)的實例。</span><span class="sxs-lookup"><span data-stu-id="3f93b-204">Create an instance of the event filter class [**\_\_EventFilter**](--eventfilter.md).</span></span>

    <span data-ttu-id="3f93b-205">設定事件篩選準則實例的必要欄位。</span><span class="sxs-lookup"><span data-stu-id="3f93b-205">Set the required fields for the event filter instance.</span></span> <span data-ttu-id="3f93b-206">[**\_ \_ >eventfilter**](--eventfilter.md)的必要欄位為 **Name**、 **QueryLanguage** 和 **Query**。</span><span class="sxs-lookup"><span data-stu-id="3f93b-206">The required fields for [**\_\_EventFilter**](--eventfilter.md) are **Name**, **QueryLanguage**, and **Query**.</span></span> <span data-ttu-id="3f93b-207">**Name** 屬性可以是這個類別之實例的任何唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="3f93b-207">The **Name** property can be any unique name for an instance of this class.</span></span> <span data-ttu-id="3f93b-208">**QueryLanguage** 屬性一律設為 "WQL"。</span><span class="sxs-lookup"><span data-stu-id="3f93b-208">The **QueryLanguage** property is always set to "WQL".</span></span> <span data-ttu-id="3f93b-209">**查詢** 屬性是包含事件查詢的字串。</span><span class="sxs-lookup"><span data-stu-id="3f93b-209">The **Query** property is a string that contains an event query.</span></span> <span data-ttu-id="3f93b-210">當永久事件取用者的查詢失敗時，就會產生事件。</span><span class="sxs-lookup"><span data-stu-id="3f93b-210">An event is generated when a permanent event consumer's query fails.</span></span> <span data-ttu-id="3f93b-211">事件的來源為 WinMgmt，事件識別碼為10，而事件種類為「錯誤」。</span><span class="sxs-lookup"><span data-stu-id="3f93b-211">The event's source is WinMgmt, the event ID is 10, and the event type is Error.</span></span>

6.  <span data-ttu-id="3f93b-212">建立 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)類別的實例，以將邏輯事件取用者與事件篩選器產生關聯。</span><span class="sxs-lookup"><span data-stu-id="3f93b-212">Create an instance of the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) class to associate a logical event consumer with an event filter.</span></span>

    <span data-ttu-id="3f93b-213">WMI 會使用關聯來尋找與事件相關聯的事件取用者，該事件符合事件篩選準則中指定的準則。</span><span class="sxs-lookup"><span data-stu-id="3f93b-213">WMI uses an association to find the event consumer associated with the event that matches the criteria specified in the event filter.</span></span> <span data-ttu-id="3f93b-214">WMI 使用事件取用者提供者來尋找要啟動的永久事件取用者應用程式。</span><span class="sxs-lookup"><span data-stu-id="3f93b-214">WMI uses the event consumer provider to find the permanent event consumer application to start.</span></span>

 

 
