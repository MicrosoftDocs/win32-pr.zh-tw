---
description: 控制外部裝置
ms.assetid: 5347cd55-a27e-40b9-857c-09e3665a1817
title: 控制外部裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f530bb48f35a6e35a0ab75d0559cc3c6770c4d0d1dfb2948f871982f70eb0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652128"
---
# <a name="controlling-an-external-device"></a>控制外部裝置

若要控制視頻錄製器 (VTR) 裝置，請使用 [**IAMExtTransport：:p ui \_ 模式**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) 方法。 使用 [裝置傳輸狀態](device-transport-state.md)中列出的其中一個常數來指定新的狀態。 例如，若要停止裝置，請使用下列程式：


```C++
pTransport->put_Mode(ED_MODE_STOP); 
```



由於 VTR 是實體裝置，因此發出命令與命令完成之間通常會有延遲。 您的應用程式應建立等候命令完成的第二個背景工作執行緒。 當命令完成時，執行緒可以更新使用者介面。 使用重要區段來序列化狀態變更。

某些 VTRs 可以在裝置的傳輸狀態變更時通知應用程式。 如果裝置支援這項功能，背景工作執行緒可以等候通知。 不過，根據1394貿易關聯的「AV/C 磁帶錄製器/玩家的次級」規格，傳輸狀態通知命令是選擇性的，這表示裝置不需要支援。 如果裝置不支援通知，您應該以定期間隔輪詢裝置，以找出其目前的狀態。

本節先說明通知機制，然後描述裝置輪詢。

使用傳輸狀態通知

傳輸狀態通知的運作方式是讓驅動程式在傳輸切換至新狀態時發出事件信號。 在您的應用程式中，宣告重要區段、事件和執行緒控制碼。 重要區段可用來同步處理裝置狀態。 當應用程式結束時，會使用此事件來停止背景工作執行緒：


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



建立 capture 篩選器的實例之後，請建立背景工作執行緒：


```C++
DWORD ThreadId;
hThread = CreateThread(NULL, 0, ThreadProc, 0, 0, &ThreadId);
```



在背景工作執行緒中，首先呼叫 [**IAMExtTransport：： GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) 方法，並使用值 ED 來 \_ 通知 \_ HEVENT \_ GET。 此呼叫會傳回當作業完成時，將會收到信號的事件控制碼：


```C++
// Get the handle to the notification event.
HANDLE hEvent = NULL;
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);
```



接下來，再次呼叫 **>getstate** 並傳遞值 ED \_ 模式 \_ 變更 \_ 通知：


```C++
LONG State;
hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
```



如果裝置支援通知，則此方法會傳回 E 值 E \_ 暫止。  (否則，您必須輪詢裝置，如下一節所述。 ) 假設裝置支援通知，則每當 VTR 傳輸的狀態變更時，就會發出事件。 此時，您可以更新使用者介面，以反映新的狀態。 若要取得下一個通知，請重設事件句柄，並 \_ 再次使用 ED 模式變更通知來呼叫 GetStatus \_ \_ 。

在背景工作執行緒結束之前，使用旗標 ED  \_ NOTIFY \_ HEVENT \_ 版本和控制碼的位址呼叫 GetStatus，以釋放事件控制碼：


```C++
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify)
```



下列程式碼顯示完整的執行緒程式。 函式 UpdateTransportState 會假設為會更新使用者介面的應用程式函數。 請注意，執行緒會等候兩個事件：通知事件 (*hNotify*) 和執行緒終止事件 (*hThreadEnd*) 。 另請注意，關鍵區段是用來保護裝置狀態變數。


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



當您將命令發出至裝置時，也請使用重要區段，如下所示：


```C++
// Issue the "stop" command.
EnterCriticalSection(&csIssueCmd); 
if (SUCCEEDED(hr = pTransport->put_Mode(ED_MODE_STOP)))
{
    UpdateTransportState(ED_MODE_STOP);
}
LeaveCriticalSection(&csIssueCmd); 
```



在應用程式結束之前，藉由設定執行緒端事件來停止次要執行緒：


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



輪詢傳輸狀態

如果您使用 ED 模式變更通知旗標來呼叫 **IAMExtTransport：： GetStatus** ， \_ 且傳回 \_ \_ 值並非 E \_ 暫止，則表示裝置不支援通知。 在此情況下，您必須輪詢裝置以判斷其狀態。 *輪詢* 只是表示定期呼叫 **get \_ 模式** 以檢查傳輸狀態。 您仍應使用次要執行緒和重要區段，如先前所述。 執行緒會以固定的間隔查詢裝置的狀態。 下列範例示範執行執行緒的一種方式：


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制 DV 攝像機](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



