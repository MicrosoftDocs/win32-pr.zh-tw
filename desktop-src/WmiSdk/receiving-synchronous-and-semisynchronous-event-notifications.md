---
description: 使用 SWbemServices.ExecQuery 來要求所有現有的事件。
ms.assetid: bc99719a-7e33-4e2d-8355-f8fc97c66f71
ms.tgt_platform: multiple
title: 接收同步和同步事件通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15327c66f7ba3e59824c94d54a206ec348c85952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987238"
---
# <a name="receiving-synchronous-and-semisynchronous-event-notifications"></a><span data-ttu-id="d8f49-103">接收同步和同步事件通知</span><span class="sxs-lookup"><span data-stu-id="d8f49-103">Receiving Synchronous and Semisynchronous Event Notifications</span></span>

<span data-ttu-id="d8f49-104">使用 [**SWbemServices.ExecQuery**](swbemservices-execquery.md) 來要求所有現有的事件。</span><span class="sxs-lookup"><span data-stu-id="d8f49-104">Use [**SWbemServices.ExecQuery**](swbemservices-execquery.md) to request all existing events.</span></span>

<span data-ttu-id="d8f49-105">下列程式碼範例示範如何查詢記錄檔中的事件。</span><span class="sxs-lookup"><span data-stu-id="d8f49-105">The following code example shows how to query for the events in a log.</span></span>

`Select * from Win32_NTLogEvent`

<span data-ttu-id="d8f49-106">如需詳細資訊，請參閱 [判斷要接收的事件種類](determining-the-type-of-event-to-receive.md)、 [接收事件通知](receiving-event-notifications.md)和 [WQL (適用于 WMI 的 SQL) ](wql-sql-for-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="d8f49-106">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md), [Receiving Event Notifications](receiving-event-notifications.md), and [WQL (SQL for WMI)](wql-sql-for-wmi.md).</span></span>

<span data-ttu-id="d8f49-107">[**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)的預設呼叫會使用半同步通訊。</span><span class="sxs-lookup"><span data-stu-id="d8f49-107">The default call to [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) uses semisynchronous communication.</span></span> <span data-ttu-id="d8f49-108">*Iflags* 參數預設會設定 **wbemFlagForwardOnly** 和 **wbemFlagReturnImmediately** 旗標。</span><span class="sxs-lookup"><span data-stu-id="d8f49-108">The *iflags* parameter has the **wbemFlagForwardOnly** and **wbemFlagReturnImmediately** flags set by default.</span></span> <span data-ttu-id="d8f49-109">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="d8f49-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="d8f49-110">下列程式描述如何使用 VBScript 接收半同步事件通知。</span><span class="sxs-lookup"><span data-stu-id="d8f49-110">The following procedure describes how to receive semisynchronous event notification using VBScript.</span></span>

<span data-ttu-id="d8f49-111">**在 VBScript 中接收半同步事件通知**</span><span class="sxs-lookup"><span data-stu-id="d8f49-111">**To receive semisynchronous event notification in VBScript**</span></span>

1.  <span data-ttu-id="d8f49-112">針對您想要接收的事件種類建立查詢。</span><span class="sxs-lookup"><span data-stu-id="d8f49-112">Create a query for the type of event that you want to receive.</span></span> <span data-ttu-id="d8f49-113">如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。</span><span class="sxs-lookup"><span data-stu-id="d8f49-113">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

2.  <span data-ttu-id="d8f49-114">如果您要求事件的實例類型（例如 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)），請在查詢中指出目標實例的類型，例如 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)。</span><span class="sxs-lookup"><span data-stu-id="d8f49-114">If you request an instance type of event such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md), indicate in the query a type of target instance, for example, [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>

3.  <span data-ttu-id="d8f49-115">如有必要，請在要求特定命名空間的未來 [**\_ \_ NamespaceModificationEvent**](--namespacemodificationevent.md)實例時，指定實例，例如命名空間的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8f49-115">If necessary, specify an instance, for example, the name of a namespace when requesting future [**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md) instances for a specific namespace.</span></span>

4.  <span data-ttu-id="d8f49-116">指定查詢中 Windows Management Instrumentation (WMI) 的輪詢間隔，例如「在10內」），以每隔10秒輪詢一次。</span><span class="sxs-lookup"><span data-stu-id="d8f49-116">Specify a polling interval for Windows Management Instrumentation (WMI) in a query, such as "WITHIN 10"—to poll every 10 seconds.</span></span> <span data-ttu-id="d8f49-117">如需詳細資訊，請參閱 [內部子句](within-clause.md)。</span><span class="sxs-lookup"><span data-stu-id="d8f49-117">For more information, see [WITHIN Clause](within-clause.md).</span></span>

5.  <span data-ttu-id="d8f49-118">使用查詢呼叫 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) 。</span><span class="sxs-lookup"><span data-stu-id="d8f49-118">Call [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) using the query.</span></span>

6.  <span data-ttu-id="d8f49-119">對您收到的集合執行迴圈。</span><span class="sxs-lookup"><span data-stu-id="d8f49-119">Loop through the collection you receive.</span></span>

<span data-ttu-id="d8f49-120">下列範例顯示如何從本機電腦上的磁片磁碟機，監視磁片的插入和移除。</span><span class="sxs-lookup"><span data-stu-id="d8f49-120">The following example shows how to monitor insertion and removal of disks from a floppy disk drive on a local machine.</span></span> <span data-ttu-id="d8f49-121">腳本會要求 \_ 磁片磁碟機 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)實例的 [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md)實例，並每隔10秒輪詢新的實例。</span><span class="sxs-lookup"><span data-stu-id="d8f49-121">The script requests \_[**\_\_InstanceModificationEvent**](--instancemodificationevent.md) instances for the floppy drive [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instance and polls every 10 seconds for new instances.</span></span> <span data-ttu-id="d8f49-122">此腳本是暫時性事件取用者的範例，並會繼續執行，直到工作管理員中停止或系統重新開機為止。</span><span class="sxs-lookup"><span data-stu-id="d8f49-122">This script is an example of a temporary event consumer, and continues running until it is stopped in Task Manager or the system is rebooted.</span></span> <span data-ttu-id="d8f49-123">如需詳細資訊，請參閱 [在您的應用程式期間接收事件](receiving-events-for-the-duration-of-your-application.md)。</span><span class="sxs-lookup"><span data-stu-id="d8f49-123">For more information, see [Receiving Events for the Duration of your Application](receiving-events-for-the-duration-of-your-application.md).</span></span>


```VB
Const FLOPPY_DISK = 2
Set colMonitoredDisks = GetObject("Winmgmts:").ExecNotificationQuery _
    ("Select * from __InstanceModificationEvent within 10 WHERE " _
        & "TargetInstance ISA 'Win32_LogicalDisk'")
i = 0
Do While i = 0
    Set strDiskChange = colMonitoredDisks.NextEvent
    If strDiskChange.TargetInstance.DriveType = FLOPPY_DISK Then
        If strDiskChange.TargetInstance.Size > 0 Then
            Wscript.Echo "A disk has been inserted" & _
                " into the floppy drive."
    Else
            Wscript.Echo "A disk has been removed" & _
                " from the floppy drive."
        End If
    End If
Loop
```



<span data-ttu-id="d8f49-124">下列程式說明如何使用 c + + 接收半同步事件通知。</span><span class="sxs-lookup"><span data-stu-id="d8f49-124">The following procedure describes how to receive semisynchronous event notification using C++.</span></span>

<span data-ttu-id="d8f49-125">**若要在 c + + 中接收半同步事件通知**</span><span class="sxs-lookup"><span data-stu-id="d8f49-125">**To receive semisynchronous event notification in C++**</span></span>

1.  <span data-ttu-id="d8f49-126">使用 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 和 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 函數的呼叫來設定應用程式。</span><span class="sxs-lookup"><span data-stu-id="d8f49-126">Set up the application with calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions.</span></span>

    <span data-ttu-id="d8f49-127">由於 WMI 是以 COM 為基礎，因此呼叫 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 和 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 是 wmi 應用程式的必要步驟。</span><span class="sxs-lookup"><span data-stu-id="d8f49-127">Because WMI is COM based, calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is a required step for a WMI application.</span></span> <span data-ttu-id="d8f49-128">如需詳細資訊，請參閱 [建立 WMI 應用程式或腳本](creating-a-wmi-application-or-script.md)。</span><span class="sxs-lookup"><span data-stu-id="d8f49-128">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

2.  <span data-ttu-id="d8f49-129">判斷您想要接收的事件種類。</span><span class="sxs-lookup"><span data-stu-id="d8f49-129">Determine the kind of events that you want to receive.</span></span>

    <span data-ttu-id="d8f49-130">WMI 支援內部和外來事件。</span><span class="sxs-lookup"><span data-stu-id="d8f49-130">WMI supports intrinsic and extrinsic events.</span></span> <span data-ttu-id="d8f49-131">內建事件是 WMI 預先定義的事件。</span><span class="sxs-lookup"><span data-stu-id="d8f49-131">An intrinsic event is an event predefined by WMI.</span></span> <span data-ttu-id="d8f49-132">外建事件是由協力廠商提供者所定義的事件。</span><span class="sxs-lookup"><span data-stu-id="d8f49-132">An extrinsic event is an event defined by a third party provider.</span></span> <span data-ttu-id="d8f49-133">如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。</span><span class="sxs-lookup"><span data-stu-id="d8f49-133">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

3.  <span data-ttu-id="d8f49-134">註冊，以透過呼叫 [**IWbemServices：： ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) 方法來接收特定類別的事件。</span><span class="sxs-lookup"><span data-stu-id="d8f49-134">Register to receive a specific class of events with a call to the [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) method.</span></span>

    <span data-ttu-id="d8f49-135">讓每個查詢都非常明確。</span><span class="sxs-lookup"><span data-stu-id="d8f49-135">Make each query very specific.</span></span> <span data-ttu-id="d8f49-136">註冊的目標是要只接收所需的通知。</span><span class="sxs-lookup"><span data-stu-id="d8f49-136">The goal of registration is to register to receive only the required notifications.</span></span> <span data-ttu-id="d8f49-137">不需要浪費處理和傳遞時間的通知。</span><span class="sxs-lookup"><span data-stu-id="d8f49-137">Notifications that are not required waste processing and delivery time.</span></span>

    <span data-ttu-id="d8f49-138">您可以設計事件取用者來接收多個事件。</span><span class="sxs-lookup"><span data-stu-id="d8f49-138">You can design an event consumer to receive multiple events.</span></span> <span data-ttu-id="d8f49-139">例如，取用者可能需要針對特定類別的裝置和安全性違規事件的實例修改事件通知。</span><span class="sxs-lookup"><span data-stu-id="d8f49-139">For example, a consumer might require notification of instance modification events for a specific class of device and security violation events.</span></span> <span data-ttu-id="d8f49-140">在此情況下，取用者在接收實例修改事件時所執行的工作，對兩個事件都是不同的。</span><span class="sxs-lookup"><span data-stu-id="d8f49-140">In this case, the tasks a consumer performs when receiving an instance modification event are different for the two events.</span></span> <span data-ttu-id="d8f49-141">因此，取用者應該呼叫 [**IWbemServices：： ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) 來註冊實例修改事件，以及對 **ExecNotificationQuery** 進行另一次呼叫，以註冊安全性違規事件。</span><span class="sxs-lookup"><span data-stu-id="d8f49-141">Thus, the consumer should make one call to [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) to register for instance modification events, and another call to **ExecNotificationQuery** to register for security violation events.</span></span>

    <span data-ttu-id="d8f49-142">在 [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)的呼叫中，將 *lFlags* 參數設定為 **WBEM \_ 旗 \_ \_** 標會立即傳回，而 **WBEM 旗標 \_ \_ \_ 只** 會順向。</span><span class="sxs-lookup"><span data-stu-id="d8f49-142">In the call to [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery), set the *lFlags* parameter to **WBEM\_FLAG\_RETURN\_IMMEDIATELY** and **WBEM\_FLAG\_FORWARD\_ONLY**.</span></span> <span data-ttu-id="d8f49-143">**Wbem 旗標會 \_ \_ \_ 立即** 傳回旗標要求的最半處理，而 **wbem 旗標 \_ \_ \_ 僅向前** 旗標會要求順向列舉值。</span><span class="sxs-lookup"><span data-stu-id="d8f49-143">The **WBEM\_FLAG\_RETURN\_IMMEDIATELY** flag requests semisynchronous processing, and the **WBEM\_FLAG\_FORWARD\_ONLY** flag requests a forward-only enumerator.</span></span> <span data-ttu-id="d8f49-144">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="d8f49-144">For more information, see [Calling a Method](calling-a-method.md).</span></span> <span data-ttu-id="d8f49-145">**ExecNotificationQuery** 函式會傳回 [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d8f49-145">The **ExecNotificationQuery** function returns a pointer to an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface.</span></span>

4.  <span data-ttu-id="d8f49-146">對 [**IEnumWbemClassObject：： Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) 方法進行重複呼叫，以輪詢已註冊的事件通知。</span><span class="sxs-lookup"><span data-stu-id="d8f49-146">Poll for registered event notifications by making repeated calls to the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) method.</span></span>
5.  <span data-ttu-id="d8f49-147">完成時，請釋放指向 [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) 物件的列舉值。</span><span class="sxs-lookup"><span data-stu-id="d8f49-147">When finished, release the enumerator that points to the [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) object.</span></span>

    <span data-ttu-id="d8f49-148">您可以釋放與註冊相關聯的 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) 指標。</span><span class="sxs-lookup"><span data-stu-id="d8f49-148">You can release the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer associated with the registration.</span></span> <span data-ttu-id="d8f49-149">釋放 **IWbemServices** 指標會導致 WMI 停止將事件傳遞給所有相關聯的暫時取用者。</span><span class="sxs-lookup"><span data-stu-id="d8f49-149">Releasing the **IWbemServices** pointer causes WMI to stop delivering events to all associated temporary consumers.</span></span>

 

 
