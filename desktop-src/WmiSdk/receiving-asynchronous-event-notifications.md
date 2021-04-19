---
description: 非同步事件通知是一種技術，可讓應用程式在不需要獨佔系統資源的情況下，持續監視事件。
ms.assetid: 69ec8ead-9073-4689-bc66-5134728ab147
ms.tgt_platform: multiple
title: 接收非同步事件通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d883908475c796a6bcf31895f2928345541c940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000295"
---
# <a name="receiving-asynchronous-event-notifications"></a><span data-ttu-id="7d415-103">接收非同步事件通知</span><span class="sxs-lookup"><span data-stu-id="7d415-103">Receiving Asynchronous Event Notifications</span></span>

<span data-ttu-id="7d415-104">非同步事件通知是一種技術，可讓應用程式在不需要獨佔系統資源的情況下，持續監視事件。</span><span class="sxs-lookup"><span data-stu-id="7d415-104">Asynchronous event notification is a technique that allows an application to constantly monitor events without monopolizing system resources.</span></span> <span data-ttu-id="7d415-105">非同步事件通知具有與其他非同步呼叫相同的安全性限制。</span><span class="sxs-lookup"><span data-stu-id="7d415-105">Asynchronous event notifications have the same security limitations that other asynchronous calls have.</span></span> <span data-ttu-id="7d415-106">您可以改為進行半執行呼叫。</span><span class="sxs-lookup"><span data-stu-id="7d415-106">You can make semisynchronous calls instead.</span></span> <span data-ttu-id="7d415-107">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="7d415-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="7d415-108">路由至用戶端的非同步事件佇列可能會變得很大。</span><span class="sxs-lookup"><span data-stu-id="7d415-108">The queue of asynchronous events routed to a client has the potential to grow exceptionally large.</span></span> <span data-ttu-id="7d415-109">因此，WMI 會實行全系統的原則，以避免記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="7d415-109">Therefore, WMI implements a system-wide policy to avoid running out of memory.</span></span> <span data-ttu-id="7d415-110">WMI 會減緩事件，或當佇列成長超過特定大小時，從佇列開始卸載事件。</span><span class="sxs-lookup"><span data-stu-id="7d415-110">WMI either slows down events, or starts dropping events from the queue when the queue grows past a certain size.</span></span>

<span data-ttu-id="7d415-111">WMI 會使用 [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting)類別的 [**LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting)和 [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting)屬性，來設定記憶體外避免的限制。</span><span class="sxs-lookup"><span data-stu-id="7d415-111">WMI uses the [**LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) and [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) properties of the [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) class to set limits on out-of-memory avoidance.</span></span> <span data-ttu-id="7d415-112">最小值會指出 WMI 何時會開始減緩事件通知，而最大值則指出何時要開始卸載事件。</span><span class="sxs-lookup"><span data-stu-id="7d415-112">The minimum value indicates when WMI should start slowing event notification, and the maximum value indicates when to start dropping events.</span></span> <span data-ttu-id="7d415-113">低和高臨界值的預設值為 1000000 (10 MB) 和 2000000 (20 MB) 。</span><span class="sxs-lookup"><span data-stu-id="7d415-113">The default values for the low and high thresholds are 1000000 (10 MB) and 2000000 (20 MB).</span></span> <span data-ttu-id="7d415-114">此外，您可以設定 [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) 屬性來描述 WMI 在卸載事件之前應等待的時間量。</span><span class="sxs-lookup"><span data-stu-id="7d415-114">In addition, you can set the [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) property to describe the amount of time WMI should wait before dropping events.</span></span> <span data-ttu-id="7d415-115">**MaxWaitOnEvents** 的預設值為2000或2秒。</span><span class="sxs-lookup"><span data-stu-id="7d415-115">The default value for **MaxWaitOnEvents** is 2000, or 2 seconds.</span></span>

## <a name="receiving-asynchronous-event-notifications-in-vbscript"></a><span data-ttu-id="7d415-116">在 VBScript 中接收非同步事件通知</span><span class="sxs-lookup"><span data-stu-id="7d415-116">Receiving Asynchronous Event Notifications in VBScript</span></span>

<span data-ttu-id="7d415-117">接收事件通知的腳本呼叫基本上與所有具有相同安全性問題的非同步呼叫相同。</span><span class="sxs-lookup"><span data-stu-id="7d415-117">The scripting calls to receive event notifications are essentially the same as all asynchronous calls with the same security issues.</span></span> <span data-ttu-id="7d415-118">如需詳細資訊，請參閱 [使用 VBScript 進行非同步呼叫](making-an-asynchronous-call-with-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="7d415-118">For more information, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="7d415-119">**若要在 VBScript 中接收非同步事件通知**</span><span class="sxs-lookup"><span data-stu-id="7d415-119">**To receive asynchronous event notifications in VBScript**</span></span>

1.  <span data-ttu-id="7d415-120">藉由呼叫 [Wscript.echo CreateObject](/previous-versions//xzysf6hc(v=vs.85)) ，並指定 "WbemScripting" 的 Progid 和 [**SWbemSink**](swbemsink.md)的物件類型，以建立接收物件。</span><span class="sxs-lookup"><span data-stu-id="7d415-120">Create a sink object by calling [WScript.CreateObject](/previous-versions//xzysf6hc(v=vs.85)) and specifying the progid of "WbemScripting" and the object type of [**SWbemSink**](swbemsink.md).</span></span> <span data-ttu-id="7d415-121">接收物件會收到通知。</span><span class="sxs-lookup"><span data-stu-id="7d415-121">The sink object receives the notifications.</span></span>
2.  <span data-ttu-id="7d415-122">針對您想要處理的每個事件撰寫副程式。</span><span class="sxs-lookup"><span data-stu-id="7d415-122">Write a subroutine for each event you want to handle.</span></span> <span data-ttu-id="7d415-123">下表列出 [**SWbemSink**](swbemsink.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="7d415-123">The following table lists the [**SWbemSink**](swbemsink.md) events.</span></span>

    

    | <span data-ttu-id="7d415-124">事件</span><span class="sxs-lookup"><span data-stu-id="7d415-124">Event</span></span>                                            | <span data-ttu-id="7d415-125">意義</span><span class="sxs-lookup"><span data-stu-id="7d415-125">Meaning</span></span>                                                                                                                         |
    |--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="7d415-126">**OnObjectReady**</span><span class="sxs-lookup"><span data-stu-id="7d415-126">**OnObjectReady**</span></span>](swbemsink-onobjectready.md) | <span data-ttu-id="7d415-127">回報將物件傳回至接收。</span><span class="sxs-lookup"><span data-stu-id="7d415-127">Reports the returns of an object to the sink.</span></span> <span data-ttu-id="7d415-128">使用這個呼叫會每次都傳回一個物件，直到作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="7d415-128">Using this call returns one object each time until the operation is complete.</span></span>     |
    | [<span data-ttu-id="7d415-129">**OnCompleted**</span><span class="sxs-lookup"><span data-stu-id="7d415-129">**OnCompleted**</span></span>](swbemsink-oncompleted.md)     | <span data-ttu-id="7d415-130">報告非同步呼叫完成的時間。</span><span class="sxs-lookup"><span data-stu-id="7d415-130">Reports when an asynchronous call is complete.</span></span> <span data-ttu-id="7d415-131">如果作業沒有限制，則永遠不會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="7d415-131">This event never occurs if the operation is indefinite.</span></span>                          |
    | [<span data-ttu-id="7d415-132">**OnObjectPut**</span><span class="sxs-lookup"><span data-stu-id="7d415-132">**OnObjectPut**</span></span>](swbemsink-onobjectput.md)     | <span data-ttu-id="7d415-133">報告非同步 put 作業的完成。</span><span class="sxs-lookup"><span data-stu-id="7d415-133">Reports the completion of an asynchronous put operation.</span></span> <span data-ttu-id="7d415-134">此事件會傳回實例或已儲存類別的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="7d415-134">This event returns the object path of the instance or the saved class.</span></span> |
    | [<span data-ttu-id="7d415-135">**OnProgress**</span><span class="sxs-lookup"><span data-stu-id="7d415-135">**OnProgress**</span></span>](swbemsink-onprogress.md)       | <span data-ttu-id="7d415-136">報告進行中之非同步呼叫的狀態。</span><span class="sxs-lookup"><span data-stu-id="7d415-136">Reports the status of an asynchronous call that is in progress.</span></span> <span data-ttu-id="7d415-137">並非所有提供者都支援過渡進度報表。</span><span class="sxs-lookup"><span data-stu-id="7d415-137">Not all providers support interim progress reports.</span></span>             |
    | [<span data-ttu-id="7d415-138">**取消**</span><span class="sxs-lookup"><span data-stu-id="7d415-138">**Cancel**</span></span>](swbemsink-cancel.md)               | <span data-ttu-id="7d415-139">取消與這個物件接收相關聯的所有未完成非同步作業。</span><span class="sxs-lookup"><span data-stu-id="7d415-139">Cancels all of the outstanding asynchronous operations associated with this object sink.</span></span>                                        |

    

     

<span data-ttu-id="7d415-140">下列 VBScript 程式碼範例會以10秒的輪詢間隔，通知刪除進程。</span><span class="sxs-lookup"><span data-stu-id="7d415-140">The following VBScript code example notifies the deletion of processes with a 10 second polling interval.</span></span> <span data-ttu-id="7d415-141">在此腳本中，副程式接收器 \_ OnObjectReady 會處理事件發生。</span><span class="sxs-lookup"><span data-stu-id="7d415-141">In this script, the subroutine SINK\_OnObjectReady handles the event occurrence.</span></span> <span data-ttu-id="7d415-142">在此範例中，接收物件會命名為 "Sink"，不過您可以依照您的選擇來命名此物件。</span><span class="sxs-lookup"><span data-stu-id="7d415-142">In the example, the sink object is named "Sink", however you can name this object as you choose.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, _
    "SELECT * FROM __InstanceDeletionEvent" _
    & " WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'"


WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "__InstanceDeletionEvent event has occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="receiving-asynchronous-event-notifications-in-c"></a><span data-ttu-id="7d415-143">在 c + + 中接收非同步事件通知</span><span class="sxs-lookup"><span data-stu-id="7d415-143">Receiving Asynchronous Event Notifications in C++</span></span>

<span data-ttu-id="7d415-144">若要執行非同步通知，您只需建立個別的執行緒來監視和接收來自 Windows Management Instrumentation (WMI) 的事件。</span><span class="sxs-lookup"><span data-stu-id="7d415-144">To perform asynchronous notification, you create a separate thread solely to monitor and receive events from Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="7d415-145">當該執行緒收到訊息時，執行緒會通知您的主應用程式。</span><span class="sxs-lookup"><span data-stu-id="7d415-145">When that thread receives a message, the thread notifies your main application.</span></span>

<span data-ttu-id="7d415-146">藉由專門建立個別的執行緒，您可以允許您的主要進程在等候事件抵達時執行其他活動。</span><span class="sxs-lookup"><span data-stu-id="7d415-146">By dedicating a separate thread, you permit your main process to perform other activities while waiting for an event to arrive.</span></span> <span data-ttu-id="7d415-147">非同步傳遞通知可改善效能，但可提供比您想要更低的安全性。</span><span class="sxs-lookup"><span data-stu-id="7d415-147">Asynchronous delivery of notifications improves performance but may provide less security than you want.</span></span> <span data-ttu-id="7d415-148">在 c + + 中，您可以選擇使用 [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) 介面，或對安全描述項執行存取檢查。</span><span class="sxs-lookup"><span data-stu-id="7d415-148">In C++, you have the option of using the [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) interface or performing access checks on security descriptors.</span></span> <span data-ttu-id="7d415-149">如需詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="7d415-149">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="7d415-150">**若要設定非同步事件通知**</span><span class="sxs-lookup"><span data-stu-id="7d415-150">**To set up asynchronous event notifications**</span></span>

1.  <span data-ttu-id="7d415-151">在初始化任何非同步通知之前，請確定已在 [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting)中正確設定您的記憶體不足的規避參數。</span><span class="sxs-lookup"><span data-stu-id="7d415-151">Before initializing any asynchronous notifications, ensure your out-of-memory avoidance parameters are set correctly in [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting).</span></span>

2.  <span data-ttu-id="7d415-152">決定您想要接收的事件種類。</span><span class="sxs-lookup"><span data-stu-id="7d415-152">Determine what kind of events you want to receive.</span></span>

    <span data-ttu-id="7d415-153">WMI 支援內部和外來事件。</span><span class="sxs-lookup"><span data-stu-id="7d415-153">WMI supports intrinsic and extrinsic events.</span></span> <span data-ttu-id="7d415-154">內建事件是 WMI 預先定義的事件，而外建事件則是由協力廠商提供者所定義的事件。</span><span class="sxs-lookup"><span data-stu-id="7d415-154">An intrinsic event is an event predefined by WMI, whereas an extrinsic event is an event defined by a third party provider.</span></span> <span data-ttu-id="7d415-155">如需詳細資訊，請參閱 [決定要接收的事件種類](determining-the-type-of-event-to-receive.md)。</span><span class="sxs-lookup"><span data-stu-id="7d415-155">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="7d415-156">下列程式描述如何在 c + + 中接收非同步事件通知。</span><span class="sxs-lookup"><span data-stu-id="7d415-156">The following procedure describes how to receive asynchronous event notifications in C++.</span></span>

<span data-ttu-id="7d415-157">**若要在 c + + 中接收非同步事件通知**</span><span class="sxs-lookup"><span data-stu-id="7d415-157">**To receive asynchronous event notifications in C++**</span></span>

1.  <span data-ttu-id="7d415-158">使用 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 和 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 函數的呼叫來設定應用程式。</span><span class="sxs-lookup"><span data-stu-id="7d415-158">Set up your application with calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions.</span></span>

    <span data-ttu-id="7d415-159">呼叫 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 會初始化 COM，而 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) 則會授與 WMI 呼叫取用者進程的許可權。</span><span class="sxs-lookup"><span data-stu-id="7d415-159">Calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) initializes COM, while [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) grants WMI the permission to call into the process of the consumer.</span></span> <span data-ttu-id="7d415-160">**CoInitializeEx** 函式也會授與您設計多執行緒應用程式的能力，這是非同步通知的必要專案。</span><span class="sxs-lookup"><span data-stu-id="7d415-160">The **CoInitializeEx** function also grants you the ability to program a multithreaded application, which is necessary for asynchronous notification.</span></span> <span data-ttu-id="7d415-161">如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。</span><span class="sxs-lookup"><span data-stu-id="7d415-161">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

    <span data-ttu-id="7d415-162">本主題中的程式碼需要下列參考，且必須 \# 要有語句才能正確編譯。</span><span class="sxs-lookup"><span data-stu-id="7d415-162">The code in this topic requires the following references and \#include statements to compile correctly.</span></span>

    ```C++
    #define _WIN32_DCOM
    #include <iostream>
    using namespace std;
    #include <wbemidl.h>
    ```

    

    <span data-ttu-id="7d415-163">下列程式碼範例說明如何使用 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 和 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)的呼叫來設定暫時性事件取用者。</span><span class="sxs-lookup"><span data-stu-id="7d415-163">The following code example describes how to set up the temporary event consumer with calls to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    ```C++
    void main(int argc, char **argv)
    {
        HRESULT hr = 0;
        hr = CoInitializeEx (0, COINIT_MULTITHREADED);
        hr = CoInitializeSecurity (NULL, 
           -1, 
           NULL, 
           NULL,   
           RPC_C_AUTHN_LEVEL_NONE, 
           RPC_C_IMP_LEVEL_IMPERSONATE, 
           NULL,
           EOAC_NONE,
           NULL); 

        if (FAILED(hr))
        {
           CoUninitialize();
           cout << "Failed to initialize security. Error code = 0x"
               << hex << hr << endl;
           return;
        }

    // ...
    }
    ```

    

2.  <span data-ttu-id="7d415-164">透過 [**IWbemObjectSink**](iwbemobjectsink.md) 介面建立接收器物件。</span><span class="sxs-lookup"><span data-stu-id="7d415-164">Create a sink object through the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="7d415-165">WMI 使用 [**IWbemObjectSink**](iwbemobjectsink.md) 來傳送事件通知，以及報告非同步作業或事件通知的狀態。</span><span class="sxs-lookup"><span data-stu-id="7d415-165">WMI uses [**IWbemObjectSink**](iwbemobjectsink.md) to send event notifications and to report status on an asynchronous operation or event notification.</span></span>

3.  <span data-ttu-id="7d415-166">透過呼叫 [**IWbemServices：： ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) 方法來註冊您的事件取用者。</span><span class="sxs-lookup"><span data-stu-id="7d415-166">Register your event consumer with a call to the [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) method.</span></span>

    <span data-ttu-id="7d415-167">請確定 *pResponseHandler* 參數指向在上一個步驟中建立的接收器物件。</span><span class="sxs-lookup"><span data-stu-id="7d415-167">Make sure that the *pResponseHandler* parameter points to the sink object created in the preceding step.</span></span>

    <span data-ttu-id="7d415-168">註冊的目的是只接收必要的通知。</span><span class="sxs-lookup"><span data-stu-id="7d415-168">The purpose of registration is to receive only the required notifications.</span></span> <span data-ttu-id="7d415-169">接收多餘的通知會浪費處理和傳遞時間;而且不會使用 WMI 的篩選能力來發揮最大潛力。</span><span class="sxs-lookup"><span data-stu-id="7d415-169">Receiving superfluous notifications wastes processing and delivery time; and does not use the filtering ability of WMI to the fullest potential.</span></span>

    <span data-ttu-id="7d415-170">不過，暫時取用者可以接收一個以上的事件種類。</span><span class="sxs-lookup"><span data-stu-id="7d415-170">However, a temporary consumer can receive more than one type of event.</span></span> <span data-ttu-id="7d415-171">在此情況下，暫存取用者必須針對每個事件種類進行個別的 [**IWbemServices：： ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="7d415-171">In this case, a temporary consumer must make separate calls to [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) for each event type.</span></span> <span data-ttu-id="7d415-172">例如，取用者可能會在建立新的進程 (實例建立事件或 [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) ，以及 (登錄事件（例如 [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)) ）的變更時，要求通知。</span><span class="sxs-lookup"><span data-stu-id="7d415-172">For example, a consumer might require notification when new processes are created (an instance creation event or [**\_\_InstanceCreationEvent**](--instancecreationevent.md)) and for changes to certain registry keys (a registry event such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)).</span></span> <span data-ttu-id="7d415-173">因此，取用者會對 [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) 進行一次呼叫，以註冊實例建立事件和另一個對 **ExecNotificationQueryAsync** 的呼叫，以註冊註冊事件。</span><span class="sxs-lookup"><span data-stu-id="7d415-173">Therefore, the consumer makes one call to [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) to register for instance creation events and another call to **ExecNotificationQueryAsync** to register for registry events.</span></span>

    <span data-ttu-id="7d415-174">如果您選擇建立事件取用者來註冊多個事件，您應該避免使用相同的接收來註冊多個類別。</span><span class="sxs-lookup"><span data-stu-id="7d415-174">If you choose to create an event consumer that registers for multiple events, you should avoid registering multiple classes with the same sink.</span></span> <span data-ttu-id="7d415-175">相反地，請針對每個已註冊事件的類別使用個別的接收。</span><span class="sxs-lookup"><span data-stu-id="7d415-175">Instead, use a separate sink for each class of registered event.</span></span> <span data-ttu-id="7d415-176">具有專用接收可簡化處理和輔助維護，讓您可以取消一個註冊，而不會影響其他註冊。</span><span class="sxs-lookup"><span data-stu-id="7d415-176">Having a dedicated sink simplifies processing and aids in maintenance, allowing you to cancel one registration without affecting the others.</span></span>

4.  <span data-ttu-id="7d415-177">在事件取用者中執行任何必要的活動。</span><span class="sxs-lookup"><span data-stu-id="7d415-177">Perform any necessary activities in your event consumer.</span></span>

    <span data-ttu-id="7d415-178">此步驟應該包含大部分的程式碼，並包含將事件顯示為使用者介面的這類活動。</span><span class="sxs-lookup"><span data-stu-id="7d415-178">This step should contain most of your code and include such activities as displaying events to a user interface.</span></span>

5.  <span data-ttu-id="7d415-179">完成時，透過呼叫 [**IWbemServices：： CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) 事件來取消註冊暫存事件取用者。</span><span class="sxs-lookup"><span data-stu-id="7d415-179">When finished, unregister the temporary event consumer with a call to the [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) event.</span></span>

    <span data-ttu-id="7d415-180">不論 [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) 的呼叫成功或失敗，除非物件參考計數到達零，否則請勿刪除接收器物件。</span><span class="sxs-lookup"><span data-stu-id="7d415-180">Regardless of whether the call to [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) succeeds or fails, do not delete the sink object until the object reference count reaches zero.</span></span> <span data-ttu-id="7d415-181">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="7d415-181">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 
