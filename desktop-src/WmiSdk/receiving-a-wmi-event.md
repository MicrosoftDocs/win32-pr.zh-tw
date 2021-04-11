---
description: WMI 包含的事件基礎結構會產生有關 WMI 資料和服務中變更的通知。 WMI 事件類別會在特定事件發生時提供通知。
ms.assetid: 347808a7-0f7b-4687-93f4-bea55c96795a
ms.tgt_platform: multiple
title: 接收 WMI 事件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 255f54f78bb64659d1cd07eddb72eae55b0263c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114900"
---
# <a name="receiving-a-wmi-event"></a><span data-ttu-id="1d455-104">接收 WMI 事件</span><span class="sxs-lookup"><span data-stu-id="1d455-104">Receiving a WMI Event</span></span>

<span data-ttu-id="1d455-105">WMI 包含的事件基礎結構會產生有關 WMI 資料和服務中變更的通知。</span><span class="sxs-lookup"><span data-stu-id="1d455-105">WMI contains an event infrastructure that produces notifications about changes in WMI data and services.</span></span> <span data-ttu-id="1d455-106">WMI [*事件類別*](gloss-e.md) 會在特定事件發生時提供通知。</span><span class="sxs-lookup"><span data-stu-id="1d455-106">WMI [*event classes*](gloss-e.md) provide notification when specific events occur.</span></span>

<span data-ttu-id="1d455-107">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="1d455-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="1d455-108">事件查詢</span><span class="sxs-lookup"><span data-stu-id="1d455-108">Event Queries</span></span>](#event-queries)
-   [<span data-ttu-id="1d455-109">範例</span><span class="sxs-lookup"><span data-stu-id="1d455-109">Example</span></span>](#example)
-   [<span data-ttu-id="1d455-110">事件取用者</span><span class="sxs-lookup"><span data-stu-id="1d455-110">Event Consumers</span></span>](#event-consumers)
-   [<span data-ttu-id="1d455-111">提供事件</span><span class="sxs-lookup"><span data-stu-id="1d455-111">Providing Events</span></span>](#providing-events)
-   [<span data-ttu-id="1d455-112">訂用帳戶配額</span><span class="sxs-lookup"><span data-stu-id="1d455-112">Subscription Quotas</span></span>](#subscription-quotas)
-   [<span data-ttu-id="1d455-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d455-113">Related topics</span></span>](#related-topics)

## <a name="event-queries"></a><span data-ttu-id="1d455-114">事件查詢</span><span class="sxs-lookup"><span data-stu-id="1d455-114">Event Queries</span></span>

<span data-ttu-id="1d455-115">您可以建立 [半同步](receiving-synchronous-and-semisynchronous-event-notifications.md) 或 [**非同步**](receiving-asynchronous-event-notifications.md) 查詢來監視事件記錄檔、進程建立、服務狀態、電腦可用性或磁片磁碟機可用空間，以及其他實體或事件的變更。</span><span class="sxs-lookup"><span data-stu-id="1d455-115">You can create a [semisynchronous](receiving-synchronous-and-semisynchronous-event-notifications.md) or [**asynchronous**](receiving-asynchronous-event-notifications.md) query to monitor changes to event logs, process creation, service status, computer availability or disk drive free space, and other entities or events.</span></span> <span data-ttu-id="1d455-116">在腳本中，會使用 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) 方法來訂閱事件。</span><span class="sxs-lookup"><span data-stu-id="1d455-116">In scripting, the [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) method is used to subscribe to events.</span></span> <span data-ttu-id="1d455-117">在 c + + 中，會使用 [**IWbemServices：： ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) 。</span><span class="sxs-lookup"><span data-stu-id="1d455-117">In C++, [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) is used.</span></span> <span data-ttu-id="1d455-118">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="1d455-118">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="1d455-119">標準 WMI 資料模型中的變更通知稱為內建 [*事件*](gloss-i.md)。</span><span class="sxs-lookup"><span data-stu-id="1d455-119">Notification of a change in the standard WMI data model is called an [*intrinsic event*](gloss-i.md).</span></span> <span data-ttu-id="1d455-120">[**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)或 [**\_ \_ NamespaceDeletionEvent**](--namespacedeletionevent.md)是內部事件的範例。</span><span class="sxs-lookup"><span data-stu-id="1d455-120">[**\_\_InstanceCreationEvent**](--instancecreationevent.md) or [**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md) are examples of intrinsic events.</span></span> <span data-ttu-id="1d455-121">提供者用來定義提供者事件之變更的通知，稱為 [*外來事件*](gloss-e.md)。</span><span class="sxs-lookup"><span data-stu-id="1d455-121">Notification of a change that a provider makes to define a provider event is called an [*extrinsic event*](gloss-e.md).</span></span> <span data-ttu-id="1d455-122">例如， [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider)、 [電源管理事件提供者](/windows/desktop/CIMWin32Prov/power-management-event-provider)和 [Win32 提供者](/windows/desktop/CIMWin32Prov/win32-provider) 會定義自己的事件。</span><span class="sxs-lookup"><span data-stu-id="1d455-122">For example, the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider), [Power Management Event Provider](/windows/desktop/CIMWin32Prov/power-management-event-provider), and [Win32 Provider](/windows/desktop/CIMWin32Prov/win32-provider) define their own events.</span></span> <span data-ttu-id="1d455-123">如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。</span><span class="sxs-lookup"><span data-stu-id="1d455-123">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

## <a name="example"></a><span data-ttu-id="1d455-124">範例</span><span class="sxs-lookup"><span data-stu-id="1d455-124">Example</span></span>

<span data-ttu-id="1d455-125">下列腳本程式碼範例是事件類別 [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)內建 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)的查詢。</span><span class="sxs-lookup"><span data-stu-id="1d455-125">The following script code example is a query for the intrinsic [**\_\_InstanceCreationEvent**](--instancecreationevent.md) of the event class [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span> <span data-ttu-id="1d455-126">您可以在背景中執行此程式，當發生事件時，就會出現一則訊息。</span><span class="sxs-lookup"><span data-stu-id="1d455-126">You can run this program in the background and when there is an event, a message appears.</span></span> <span data-ttu-id="1d455-127">如果您關閉 [ **正在等候事件** ] 對話方塊，程式就會停止等候事件。</span><span class="sxs-lookup"><span data-stu-id="1d455-127">If you close the **Waiting for events** dialog box, the program stops waiting for events.</span></span> <span data-ttu-id="1d455-128">請注意，必須啟用 **SeSecurityPrivilege** 。</span><span class="sxs-lookup"><span data-stu-id="1d455-128">Be aware that the **SeSecurityPrivilege** must be enabled.</span></span>


```VB
Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo (objObject.TargetInstance.Message)
End Sub

Set objWMIServices = GetObject( _
    "WinMgmts:{impersonationLevel=impersonate, (security)}") 

' Create the event sink object that receives the events
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
 
' Set up the event selection. SINK_OnObjectReady is called when
' a Win32_NTLogEvent event occurs
objWMIServices.ExecNotificationQueryAsync sink,"SELECT * FROM __InstanceCreationEvent " & "WHERE TargetInstance ISA 'Win32_NTLogEvent' "

WScript.Echo "Waiting for events"
```


```PowerShell

# Define event Query
$query = "SELECT * FROM __InstanceCreationEvent 
          WHERE TargetInstance ISA 'Win32_NTLogEvent' "

<# Register for event - also specify an action that
displays the log event when the event fires.#>

Register-WmiEvent -Source Demo1 -Query $query -Action {
                Write-Host "Log Event occured"
                $global:myevent = $event
                Write-Host "EVENT MESSAGE"
                Write-Host $event.SourceEventArgs.NewEvent.TargetInstance.Message}
<# So wait #>
"Waiting for events"
```





<span data-ttu-id="1d455-129">下列 VBScript 程式碼範例顯示登錄提供者所定義的外建事件[ \_ \_ registryvaluechangeeven](registering-for-system-registry-events.md) 。</span><span class="sxs-lookup"><span data-stu-id="1d455-129">The following VBScript code example shows the extrinsic event [\_\_RegistryValueChangeEvent](registering-for-system-registry-events.md) that the registry provider defines.</span></span> <span data-ttu-id="1d455-130">腳本會使用 [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)的呼叫來建立暫時的取用者，而且只會在腳本執行時接收事件。</span><span class="sxs-lookup"><span data-stu-id="1d455-130">The script creates a temporary consumer by using the call to [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md), and only receives events when the script is running.</span></span> <span data-ttu-id="1d455-131">下列腳本會無限期地執行，直到電腦重新開機、WMI 已停止或腳本停止。</span><span class="sxs-lookup"><span data-stu-id="1d455-131">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="1d455-132">若要手動停止腳本，請使用工作管理員停止進程。</span><span class="sxs-lookup"><span data-stu-id="1d455-132">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="1d455-133">若要以程式設計方式停止它，請在 Win32 Process 類別中使用 [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) 方法 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1d455-133">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span> <span data-ttu-id="1d455-134">如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="1d455-134">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>


```VB
strComputer = "."

Set objWMIServices=GetObject( _
    "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default")

set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")


objWMIServices.ExecNotificationQueryAsync objSink, _
    "Select * from RegistryValueChangeEvent Where Hive = 'HKEY_LOCAL_MACHINE' and KeyPath = 'SYSTEM\\ControlSet001\\Control' and ValueName = 'CurrentUser'"

WScript.Echo "Waiting for events..."

While (True) 
     WScript.Sleep (1000)
Wend

 
WScript.Echo "Listening for Registry Change Events..." & vbCrLf 

While(True) 
    WScript.Sleep 1000 
Wend 

Sub SINK_OnObjectReady(wmiObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Value Change Event" & vbCrLf & wmiObject.GetObjectText_() 
End Sub
```



## <a name="event-consumers"></a><span data-ttu-id="1d455-135">事件取用者</span><span class="sxs-lookup"><span data-stu-id="1d455-135">Event Consumers</span></span>

<span data-ttu-id="1d455-136">當腳本或應用程式正在執行時，您可以使用下列取用者來監視或取用事件：</span><span class="sxs-lookup"><span data-stu-id="1d455-136">You can monitor or consume events using the following consumers while a script or application is running:</span></span>

-   <span data-ttu-id="1d455-137">暫存事件取用者</span><span class="sxs-lookup"><span data-stu-id="1d455-137">Temporary event consumers</span></span>

    <span data-ttu-id="1d455-138">[*暫時性取用者*](gloss-t.md)是接收 wmi 事件的 wmi 用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="1d455-138">A [*temporary consumer*](gloss-t.md) is a WMI client application that receives a WMI event.</span></span> <span data-ttu-id="1d455-139">WMI 包含一個唯一的介面，用來指定要傳送至用戶端應用程式的 WMI 事件。</span><span class="sxs-lookup"><span data-stu-id="1d455-139">WMI includes a unique interface that use to specify the events for WMI to send to a client application.</span></span> <span data-ttu-id="1d455-140">暫時的事件取用者被視為暫時性，因為它只有在使用者特別載入時才能運作。</span><span class="sxs-lookup"><span data-stu-id="1d455-140">A temporary event consumer is considered temporary because it only works when specifically loaded by a user.</span></span> <span data-ttu-id="1d455-141">如需詳細資訊，請參閱 [在您的應用程式期間接收事件](receiving-events-for-the-duration-of-your-application.md)。</span><span class="sxs-lookup"><span data-stu-id="1d455-141">For more information, see [Receiving Events for the Duration of Your Application](receiving-events-for-the-duration-of-your-application.md).</span></span>

-   <span data-ttu-id="1d455-142">永久事件取用者</span><span class="sxs-lookup"><span data-stu-id="1d455-142">Permanent event consumers</span></span>

    <span data-ttu-id="1d455-143">[*永久取用者*](gloss-p.md)是一種可隨時接收 WMI 事件的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="1d455-143">A [*permanent consumer*](gloss-p.md) is a COM object that can receive a WMI event at all times.</span></span> <span data-ttu-id="1d455-144">永久事件取用者會使用一組持續性物件和篩選來捕捉 WMI 事件。</span><span class="sxs-lookup"><span data-stu-id="1d455-144">A permanent event consumer uses a set of persistent objects and filters to capture a WMI event.</span></span> <span data-ttu-id="1d455-145">如同暫時性的事件取用者，您可以設定一系列的 WMI 物件和篩選器來捕捉 WMI 事件。</span><span class="sxs-lookup"><span data-stu-id="1d455-145">Like a temporary event consumer, you set up a series of WMI objects and filters that capture a WMI event.</span></span> <span data-ttu-id="1d455-146">當符合篩選準則的事件發生時，WMI 會載入永久事件取用者，並通知事件。</span><span class="sxs-lookup"><span data-stu-id="1d455-146">When an event occurs that matches a filter, WMI loads the permanent event consumer and notifies it about the event.</span></span> <span data-ttu-id="1d455-147">因為永久性取用者是在 WMI 存放庫中執行，而且是在 WMI 中註冊的可執行檔，所以永久事件取用者會在建立事件之後，以及在作業系統重新開機之後（只要 WMI 正在執行），就會操作和接收事件。</span><span class="sxs-lookup"><span data-stu-id="1d455-147">Because a permanent consumer is implemented in the WMI repository and is an executable file that is registered in WMI, the permanent event consumer operates and receives events after it is created and even after a reboot of the operating system as long as WMI is running.</span></span> <span data-ttu-id="1d455-148">如需詳細資訊，請參閱 [所有時間的接收事件](receiving-events-at-all-times.md)。</span><span class="sxs-lookup"><span data-stu-id="1d455-148">For more information, see [Receiving Events at All Times](receiving-events-at-all-times.md).</span></span>

<span data-ttu-id="1d455-149">接收事件的腳本或應用程式有特殊的安全性考慮。</span><span class="sxs-lookup"><span data-stu-id="1d455-149">Scripts or applications that receive events have special security considerations.</span></span> <span data-ttu-id="1d455-150">如需詳細資訊，請參閱 [保護 WMI 事件](securing-wmi-events.md)。</span><span class="sxs-lookup"><span data-stu-id="1d455-150">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

<span data-ttu-id="1d455-151">應用程式或腳本可以使用內建的 WMI 事件提供者，以提供 [標準取用者類別](standard-consumer-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="1d455-151">An application or script can use a built-in WMI event provider that supplies [standard consumer classes](standard-consumer-classes.md).</span></span> <span data-ttu-id="1d455-152">每個標準取用者類別都會傳送電子郵件訊息或執行腳本，以不同的動作來回應事件。</span><span class="sxs-lookup"><span data-stu-id="1d455-152">Each standard consumer class responds to an event with a different action by sending an email message or executing a script.</span></span> <span data-ttu-id="1d455-153">您不需要撰寫提供者程式碼，就能使用標準取用者類別來建立永久事件取用者。</span><span class="sxs-lookup"><span data-stu-id="1d455-153">You do not have to write provider code to use a standard consumer class to create a permanent event consumer.</span></span> <span data-ttu-id="1d455-154">如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="1d455-154">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="providing-events"></a><span data-ttu-id="1d455-155">提供事件</span><span class="sxs-lookup"><span data-stu-id="1d455-155">Providing Events</span></span>

<span data-ttu-id="1d455-156">事件提供者是將事件傳送至 WMI 的 COM 元件。</span><span class="sxs-lookup"><span data-stu-id="1d455-156">An event provider is a COM component that sends an event to WMI.</span></span> <span data-ttu-id="1d455-157">您可以建立事件提供者，以在 c + + 或 c # 應用程式中傳送事件。</span><span class="sxs-lookup"><span data-stu-id="1d455-157">You can create an event provider to send an event in a C++ or C# application.</span></span> <span data-ttu-id="1d455-158">大部分的事件提供者會管理 WMI 的物件，例如應用程式或硬體專案。</span><span class="sxs-lookup"><span data-stu-id="1d455-158">Most event providers manage an object for WMI, for example, an application or hardware item.</span></span> <span data-ttu-id="1d455-159">如需詳細資訊，請參閱 [撰寫事件提供者](writing-an-event-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="1d455-159">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

<span data-ttu-id="1d455-160">計時或重複事件是在預先定義的時間發生的事件。</span><span class="sxs-lookup"><span data-stu-id="1d455-160">A timed or repeating event is an event that occurs at a predetermined time.</span></span>

<span data-ttu-id="1d455-161">WMI 提供下列方法來為您的應用程式建立計時或重複事件：</span><span class="sxs-lookup"><span data-stu-id="1d455-161">WMI provides the following ways to create timed or repeating events for your applications:</span></span>

-   <span data-ttu-id="1d455-162">標準的 Microsoft 事件基礎結構。</span><span class="sxs-lookup"><span data-stu-id="1d455-162">The standard Microsoft event infrastructure.</span></span>
-   <span data-ttu-id="1d455-163">特製化計時器類別。</span><span class="sxs-lookup"><span data-stu-id="1d455-163">A specialized timer class.</span></span>

<span data-ttu-id="1d455-164">如需詳細資訊，請參閱 [接收計時或重複事件](receiving-a-timed-or-repeating-event.md)。</span><span class="sxs-lookup"><span data-stu-id="1d455-164">For more information, see [Receiving a Timed or Repeating Event](receiving-a-timed-or-repeating-event.md).</span></span> <span data-ttu-id="1d455-165">當您撰寫事件提供者時，請考慮安全 [地提供事件](providing-events-securely.md)中所識別的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="1d455-165">When you write an event provider, consider the security information identified in [Providing Events Securely](providing-events-securely.md).</span></span>

<span data-ttu-id="1d455-166">建議將永久性事件訂閱編譯成根訂用帳戶 \\ \\ 命名空間。</span><span class="sxs-lookup"><span data-stu-id="1d455-166">It is recommended that permanent event subscriptions be compiled into the \\root\\subscription namespace.</span></span> <span data-ttu-id="1d455-167">如需詳細資訊，請參閱 [實施跨命名空間永久事件訂閱](implementing-cross-namespace-permanent-event-subscriptions.md)。</span><span class="sxs-lookup"><span data-stu-id="1d455-167">For more information, see [Implementing Cross-Namespace Permanent Event Subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).</span></span>

## <a name="subscription-quotas"></a><span data-ttu-id="1d455-168">訂用帳戶配額</span><span class="sxs-lookup"><span data-stu-id="1d455-168">Subscription Quotas</span></span>

<span data-ttu-id="1d455-169">針對大型資料集支援查詢的提供者，輪詢事件可能會降低效能。</span><span class="sxs-lookup"><span data-stu-id="1d455-169">Polling for events can degrade performance for providers that support queries over huge data sets.</span></span> <span data-ttu-id="1d455-170">此外，對於具有動態提供者之命名空間的讀取權限的任何使用者，都可以執行拒絕服務 (DoS) 攻擊。</span><span class="sxs-lookup"><span data-stu-id="1d455-170">Additionally, any user that has read access to a namespace with dynamic providers can perform a denial of service (DoS) attack.</span></span> <span data-ttu-id="1d455-171">WMI 會針對位在根命名空間中 [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md)單一實例的每個事件取用者，維護所有使用者的配額 \\ 。</span><span class="sxs-lookup"><span data-stu-id="1d455-171">WMI maintains quotas for all of the users combined and for each event consumer in the single instance of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md) located in the \\root namespace.</span></span> <span data-ttu-id="1d455-172">這些配額是全域的，而不是每個命名空間。</span><span class="sxs-lookup"><span data-stu-id="1d455-172">These quotas are global rather than for each namespace.</span></span> <span data-ttu-id="1d455-173">您無法變更配額。</span><span class="sxs-lookup"><span data-stu-id="1d455-173">You cannot change the quotas.</span></span>

<span data-ttu-id="1d455-174">WMI 目前使用 [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md)的屬性來強制執行配額。</span><span class="sxs-lookup"><span data-stu-id="1d455-174">WMI currently enforces quotas using the properties of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md).</span></span> <span data-ttu-id="1d455-175">每個配額都有每個使用者和包含所有使用者組合的總版本，而不是每個命名空間。</span><span class="sxs-lookup"><span data-stu-id="1d455-175">Each quota has a per user and a total version that includes all users combined, not per namespace.</span></span> <span data-ttu-id="1d455-176">下表列出適用于 **\_ \_ ArbitratorConfiguration** 屬性的配額。</span><span class="sxs-lookup"><span data-stu-id="1d455-176">The following table lists the quotas that apply to the **\_\_ArbitratorConfiguration** properties.</span></span>



| <span data-ttu-id="1d455-177">Total/PerUser</span><span class="sxs-lookup"><span data-stu-id="1d455-177">Total/PerUser</span></span>                                                                   | <span data-ttu-id="1d455-178">Quota</span><span class="sxs-lookup"><span data-stu-id="1d455-178">Quota</span></span>                                                                       |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="1d455-179">TemporarySubscriptionsTotal</span><span class="sxs-lookup"><span data-stu-id="1d455-179">TemporarySubscriptionsTotal</span></span><br/> <span data-ttu-id="1d455-180">TemporarySubscriptionsPerUser</span><span class="sxs-lookup"><span data-stu-id="1d455-180">TemporarySubscriptionsPerUser</span></span><br/> | <span data-ttu-id="1d455-181">10,000</span><span class="sxs-lookup"><span data-stu-id="1d455-181">10,000</span></span><br/> <span data-ttu-id="1d455-182">1,000</span><span class="sxs-lookup"><span data-stu-id="1d455-182">1,000</span></span><br/>                                          |
| <span data-ttu-id="1d455-183">PermanentSubscriptionsTotal</span><span class="sxs-lookup"><span data-stu-id="1d455-183">PermanentSubscriptionsTotal</span></span><br/> <span data-ttu-id="1d455-184">PermanentSubscriptionsPerUser</span><span class="sxs-lookup"><span data-stu-id="1d455-184">PermanentSubscriptionsPerUser</span></span><br/> | <span data-ttu-id="1d455-185">10,000</span><span class="sxs-lookup"><span data-stu-id="1d455-185">10,000</span></span><br/> <span data-ttu-id="1d455-186">1,000</span><span class="sxs-lookup"><span data-stu-id="1d455-186">1,000</span></span><br/>                                          |
| <span data-ttu-id="1d455-187">PollingInstructionsTotal</span><span class="sxs-lookup"><span data-stu-id="1d455-187">PollingInstructionsTotal</span></span><br/> <span data-ttu-id="1d455-188">PollingInstructionsPerUser</span><span class="sxs-lookup"><span data-stu-id="1d455-188">PollingInstructionsPerUser</span></span><br/>       | <span data-ttu-id="1d455-189">10,000</span><span class="sxs-lookup"><span data-stu-id="1d455-189">10,000</span></span><br/> <span data-ttu-id="1d455-190">1,000</span><span class="sxs-lookup"><span data-stu-id="1d455-190">1,000</span></span><br/>                                          |
| <span data-ttu-id="1d455-191">PollingMemoryTotal</span><span class="sxs-lookup"><span data-stu-id="1d455-191">PollingMemoryTotal</span></span><br/> <span data-ttu-id="1d455-192">PollingMemoryPerUser</span><span class="sxs-lookup"><span data-stu-id="1d455-192">PollingMemoryPerUser</span></span><br/>                   | <span data-ttu-id="1d455-193">10000000 (0x989680) 位元組</span><span class="sxs-lookup"><span data-stu-id="1d455-193">10,000,000 (0x989680) bytes</span></span><br/> <span data-ttu-id="1d455-194">5000000 (0x4CB40) 位元組</span><span class="sxs-lookup"><span data-stu-id="1d455-194">5,000,000 (0x4CB40) bytes</span></span><br/> |



 

<span data-ttu-id="1d455-195">具有命名空間 **完整 \_ 寫入** 許可權的系統管理員或使用者可以修改 [**\_ \_ ArbitratorConfiguration**](--arbitratorconfiguration.md)的單一實例。</span><span class="sxs-lookup"><span data-stu-id="1d455-195">An administrator or a user with **FULL\_WRITE** permission in the namespace can modify the singleton instance of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md).</span></span> <span data-ttu-id="1d455-196">WMI 會追蹤每位使用者的配額。</span><span class="sxs-lookup"><span data-stu-id="1d455-196">WMI tracks the per-user quota.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d455-197">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d455-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d455-198">使用 WMI</span><span class="sxs-lookup"><span data-stu-id="1d455-198">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

