---
description: 控制外部裝置
ms.assetid: 5347cd55-a27e-40b9-857c-09e3665a1817
title: 控制外部裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84cb82de59877f2527c92da9123d8a9d5a59d41e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509842"
---
# <a name="controlling-an-external-device"></a><span data-ttu-id="62e63-103">控制外部裝置</span><span class="sxs-lookup"><span data-stu-id="62e63-103">Controlling an External Device</span></span>

<span data-ttu-id="62e63-104">若要控制視頻錄製器 (VTR) 裝置，請使用 [**IAMExtTransport：:p ui \_ 模式**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) 方法。</span><span class="sxs-lookup"><span data-stu-id="62e63-104">To control a video tape recorder (VTR) device, use the [**IAMExtTransport::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) method.</span></span> <span data-ttu-id="62e63-105">使用 [裝置傳輸狀態](device-transport-state.md)中列出的其中一個常數來指定新的狀態。</span><span class="sxs-lookup"><span data-stu-id="62e63-105">Specify the new state by using one of the constants listed in the [Device Transport State](device-transport-state.md).</span></span> <span data-ttu-id="62e63-106">例如，若要停止裝置，請使用下列程式：</span><span class="sxs-lookup"><span data-stu-id="62e63-106">For example, to stop the device, use the following:</span></span>


```C++
pTransport->put_Mode(ED_MODE_STOP); 
```



<span data-ttu-id="62e63-107">由於 VTR 是實體裝置，因此發出命令與命令完成之間通常會有延遲。</span><span class="sxs-lookup"><span data-stu-id="62e63-107">Because the VTR is a physical device, there is typically a lag between issuing the command and when the command completes.</span></span> <span data-ttu-id="62e63-108">您的應用程式應建立等候命令完成的第二個背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="62e63-108">Your application should create a second worker thread that waits for the command to finish.</span></span> <span data-ttu-id="62e63-109">當命令完成時，執行緒可以更新使用者介面。</span><span class="sxs-lookup"><span data-stu-id="62e63-109">When the command finishes, the thread can update the user interface.</span></span> <span data-ttu-id="62e63-110">使用重要區段來序列化狀態變更。</span><span class="sxs-lookup"><span data-stu-id="62e63-110">Use a critical section to serialize the state change.</span></span>

<span data-ttu-id="62e63-111">某些 VTRs 可以在裝置的傳輸狀態變更時通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="62e63-111">Some VTRs can notify the application when the device's transport state has changed.</span></span> <span data-ttu-id="62e63-112">如果裝置支援這項功能，背景工作執行緒可以等候通知。</span><span class="sxs-lookup"><span data-stu-id="62e63-112">If the device supports this feature, the worker thread can wait for the notification.</span></span> <span data-ttu-id="62e63-113">不過，根據1394貿易關聯的「AV/C 磁帶錄製器/玩家的次級」規格，傳輸狀態通知命令是選擇性的，這表示裝置不需要支援。</span><span class="sxs-lookup"><span data-stu-id="62e63-113">According to the 1394 Trade Association's "AV/C Tape Recorder/Player Subunit Specification", however, the transport-state notification command is optional, meaning devices are not required to support it.</span></span> <span data-ttu-id="62e63-114">如果裝置不支援通知，您應該以定期間隔輪詢裝置，以找出其目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="62e63-114">If a device does not support notification, you should poll the device at periodic intervals for its current state.</span></span>

<span data-ttu-id="62e63-115">本節先說明通知機制，然後描述裝置輪詢。</span><span class="sxs-lookup"><span data-stu-id="62e63-115">This section first describes the notification mechanism, and then describes device polling.</span></span>

<span data-ttu-id="62e63-116">使用傳輸狀態通知</span><span class="sxs-lookup"><span data-stu-id="62e63-116">Using Transport State Notification</span></span>

<span data-ttu-id="62e63-117">傳輸狀態通知的運作方式是讓驅動程式在傳輸切換至新狀態時發出事件信號。</span><span class="sxs-lookup"><span data-stu-id="62e63-117">Transport state notification works by having the driver signal an event when the transport switches to a new state.</span></span> <span data-ttu-id="62e63-118">在您的應用程式中，宣告重要區段、事件和執行緒控制碼。</span><span class="sxs-lookup"><span data-stu-id="62e63-118">In your application, declare a critical section, an event, and a thread handle.</span></span> <span data-ttu-id="62e63-119">重要區段可用來同步處理裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="62e63-119">The critical section is used to synchronize the device state.</span></span> <span data-ttu-id="62e63-120">當應用程式結束時，會使用此事件來停止背景工作執行緒：</span><span class="sxs-lookup"><span data-stu-id="62e63-120">The event is used to halt the worker thread when the application exits:</span></span>


```C++
HANDLE hThread = 0;
HANDLE hThreadEnd = CreateEvent(NULL, TRUE, FALSE, NULL); 
if (hThreadEnd == NULL)
{
    // Handle error.
}
CRITICAL_SECTION csIssueCmd;
InitializeCriticalSection(&cdIssueCmd);
```



<span data-ttu-id="62e63-121">建立 capture 篩選器的實例之後，請建立背景工作執行緒：</span><span class="sxs-lookup"><span data-stu-id="62e63-121">After you create an instance of the capture filter, create the worker thread:</span></span>


```C++
DWORD ThreadId;
hThread = CreateThread(NULL, 0, ThreadProc, 0, 0, &ThreadId);
```



<span data-ttu-id="62e63-122">在背景工作執行緒中，首先呼叫 [**IAMExtTransport：： GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) 方法，並使用值 ED 來 \_ 通知 \_ HEVENT \_ GET。</span><span class="sxs-lookup"><span data-stu-id="62e63-122">In the worker thread, start by calling the [**IAMExtTransport::GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) method with the value ED\_NOTIFY\_HEVENT\_GET.</span></span> <span data-ttu-id="62e63-123">此呼叫會傳回當作業完成時，將會收到信號的事件控制碼：</span><span class="sxs-lookup"><span data-stu-id="62e63-123">This call returns a handle to an event that will be signaled when an operation completes:</span></span>


```C++
// Get the handle to the notification event.
HANDLE hEvent = NULL;
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);
```



<span data-ttu-id="62e63-124">接下來，再次呼叫 **>getstate** 並傳遞值 ED \_ 模式 \_ 變更 \_ 通知：</span><span class="sxs-lookup"><span data-stu-id="62e63-124">Next, call **GetState** again and pass the value ED\_MODE\_CHANGE\_NOTIFY:</span></span>


```C++
LONG State;
hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
```



<span data-ttu-id="62e63-125">如果裝置支援通知，則此方法會傳回 E 值 E \_ 暫止。</span><span class="sxs-lookup"><span data-stu-id="62e63-125">If the device supports notification, the method returns the value E\_PENDING.</span></span> <span data-ttu-id="62e63-126"> (否則，您必須輪詢裝置，如下一節所述。 ) 假設裝置支援通知，則每當 VTR 傳輸的狀態變更時，就會發出事件。</span><span class="sxs-lookup"><span data-stu-id="62e63-126">(Otherwise, you must poll device, as described in the next section.) Assuming the device supports notification, the event will be signaled whenever the state of the VTR transport changes.</span></span> <span data-ttu-id="62e63-127">此時，您可以更新使用者介面，以反映新的狀態。</span><span class="sxs-lookup"><span data-stu-id="62e63-127">At this point, you can update the user interface to reflect the new state.</span></span> <span data-ttu-id="62e63-128">若要取得下一個通知，請重設事件句柄，並 \_ 再次使用 ED 模式變更通知來呼叫 GetStatus \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="62e63-128">To get the next notification, reset the event handle and call **GetStatus** with ED\_MODE\_CHANGE\_NOTIFY again.</span></span>

<span data-ttu-id="62e63-129">在背景工作執行緒結束之前，使用旗標 ED  \_ NOTIFY \_ HEVENT \_ 版本和控制碼的位址呼叫 GetStatus，以釋放事件控制碼：</span><span class="sxs-lookup"><span data-stu-id="62e63-129">Before the worker thread exits, release the event handle by calling **GetStatus** with the flag ED\_NOTIFY\_HEVENT\_RELEASE and the address of the handle:</span></span>


```C++
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify)
```



<span data-ttu-id="62e63-130">下列程式碼顯示完整的執行緒程式。</span><span class="sxs-lookup"><span data-stu-id="62e63-130">The following code shows the complete thread procedure.</span></span> <span data-ttu-id="62e63-131">函式 UpdateTransportState 會假設為會更新使用者介面的應用程式函數。</span><span class="sxs-lookup"><span data-stu-id="62e63-131">The function UpdateTransportState is assumed to be an application function that updates the user interface.</span></span> <span data-ttu-id="62e63-132">請注意，執行緒會等候兩個事件：通知事件 (*hNotify*) 和執行緒終止事件 (*hThreadEnd*) 。</span><span class="sxs-lookup"><span data-stu-id="62e63-132">Note that the thread waits for two events: the notification event (*hNotify*) and the thread-termination event (*hThreadEnd*).</span></span> <span data-ttu-id="62e63-133">另請注意，關鍵區段是用來保護裝置狀態變數。</span><span class="sxs-lookup"><span data-stu-id="62e63-133">Also note where the critical section is used to protect the device state variable.</span></span>


```C++
DWORD WINAPI ThreadProc(void *pParam)
{
    HRESULT hr;
    HANDLE  EventHandles[2];
    HANDLE  hNotify = NULL;
    DWORD   WaitStatus;
    LONG    State;

    // Get the notification event handle. This event will be signaled when
    // the next state-change operation completes.   
    hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);

    while (hThread && hNotify && hThreadEnd) 
    {
        EnterCriticalSection(&csIssueCmd);
        // Ask the device to notify us when the state changes.
        hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
        LeaveCriticalSection(&csIssueCmd); 

        if(hr == E_PENDING)  // The device supports notification.
        {
            // Wait for the notification.
            EventHandles[0] = hNotify;
            EventHandles[1] = hThreadEnd;
            WaitStatus = WaitForMultipleObjects(2, EventHandles, FALSE, INFINITE);
            if(WAIT_OBJECT_0 == WaitStatus) 
            {
                // We got notified. Query for the new state.
                EnterCriticalSection(&csIssueCmd);  
                hr = m_pTransport->get_Mode(State);
                UpdateTransportState(State);  // Update the UI.
                LeaveCriticalSection(&m_csIssueCmd);
                ResetEvent(hNotify);
            } 
            else {
                break;  // End this thread.
            }
        } 
        else {          
            // The device does not support notification.
            PollDevice();        
        } 
    } // while

    // Cancel notification. 
    hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify);
    return 1; 
}
```



<span data-ttu-id="62e63-134">當您將命令發出至裝置時，也請使用重要區段，如下所示：</span><span class="sxs-lookup"><span data-stu-id="62e63-134">Also use the critical section when you issue commands to the device, as follows:</span></span>


```C++
// Issue the "stop" command.
EnterCriticalSection(&csIssueCmd); 
if (SUCCEEDED(hr = pTransport->put_Mode(ED_MODE_STOP)))
{
    UpdateTransportState(ED_MODE_STOP);
}
LeaveCriticalSection(&csIssueCmd); 
```



<span data-ttu-id="62e63-135">在應用程式結束之前，藉由設定執行緒端事件來停止次要執行緒：</span><span class="sxs-lookup"><span data-stu-id="62e63-135">Before the application exits, halt the secondary thread by setting the thread-end event:</span></span>


```C++
if (hThread) 
{
    // Signaling this event will cause the thread to end.    
    if (SetEvent(hThreadEnd))
    {
        // Wait for it to end.
        WaitForSingleObjectEx(hThread, INFINITE, FALSE);
    }
}
CloseHandle(hThreadEnd);
CloseHandle(hThread);
```



<span data-ttu-id="62e63-136">輪詢傳輸狀態</span><span class="sxs-lookup"><span data-stu-id="62e63-136">Polling the Transport State</span></span>

<span data-ttu-id="62e63-137">如果您使用 ED 模式變更通知旗標來呼叫 **IAMExtTransport：： GetStatus** ， \_ 且傳回 \_ \_ 值並非 E \_ 暫止，則表示裝置不支援通知。</span><span class="sxs-lookup"><span data-stu-id="62e63-137">If you call **IAMExtTransport::GetStatus** with the ED\_MODE\_CHANGE\_NOTIFY flag and the return value is not E\_PENDING, it means the device does not support notification.</span></span> <span data-ttu-id="62e63-138">在此情況下，您必須輪詢裝置以判斷其狀態。</span><span class="sxs-lookup"><span data-stu-id="62e63-138">In that case, you must poll the device to determine its state.</span></span> <span data-ttu-id="62e63-139">*輪詢* 只是表示定期呼叫 **get \_ 模式** 以檢查傳輸狀態。</span><span class="sxs-lookup"><span data-stu-id="62e63-139">*Polling* simply means calling **get\_Mode** at regular intervals to check the transport state.</span></span> <span data-ttu-id="62e63-140">您仍應使用次要執行緒和重要區段，如先前所述。</span><span class="sxs-lookup"><span data-stu-id="62e63-140">You should still use a secondary thread and a critical section, as described earlier.</span></span> <span data-ttu-id="62e63-141">執行緒會以固定的間隔查詢裝置的狀態。</span><span class="sxs-lookup"><span data-stu-id="62e63-141">The thread queries the device for its state at a regular interval.</span></span> <span data-ttu-id="62e63-142">下列範例示範執行執行緒的一種方式：</span><span class="sxs-lookup"><span data-stu-id="62e63-142">The following example shows one way to implement the thread:</span></span>


```C++
DWORD WINAPI ThreadProc(void *pParam)
{
    HRESULT hr;
    LONG State;
    DWORD WaitStatus;

    while (hThread && hThreadEnd) 
    {
        EnterCriticalSection(&csIssueCmd);  
        State = 0;
        hr = pTransport->get_Mode(&State);
        LeaveCriticalSection(&csIssueCmd); 
        UpdateTransportState(State);

        // Wait for a while, or until the thread ends. 
        WaitStatus = WaitForSingleObjectEx(hThreadEnd, 200, FALSE); 
        if (WaitStatus == WAIT_OBJECT_0)
        {
            break; // Exit thread now. 
        }
        // Otherwise, the wait timed out. Time to poll again.
    }
    return 1;
}
```



## <a name="related-topics"></a><span data-ttu-id="62e63-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="62e63-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62e63-144">控制 DV 攝像機</span><span class="sxs-lookup"><span data-stu-id="62e63-144">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



