---
description: 本主題說明如何啟動和停止列印工作處理執行緒。
ms.assetid: CA3A81D6-332F-4867-881F-AC6859A076CF
title: 如何：啟動和停止列印執行緒
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393f1f95efbb52c7cdd81316db000de22d45ca9e5dda0eadebb82ebaa3942350
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117686710"
---
# <a name="how-to-start-and-stop-a-printing-thread"></a>如何：啟動和停止列印執行緒

本主題說明如何啟動和停止列印工作處理執行緒。

## <a name="overview"></a>概觀

若要防止列印活動封鎖使用者介面回應，請建立個別的執行緒來處理列印工作。 啟動程式時啟動的執行緒是處理使用者互動所產生之視窗訊息的執行緒，因此也就是 UI 執行緒。 程式必須在不延遲的情況下處理這些訊息，使用者介面才能及時回應使用者的滑鼠和鍵盤輸入。 為了讓程式能夠快速回應這些訊息，在任何一則訊息期間可以執行的處理量會受到限制。 當使用者要求需要大量處理時，不同的執行緒必須執行該處理，才能讓程式處理後續的使用者互動。

在不同的執行緒中處理資料時，程式必須協調使用者介面執行緒和處理執行緒的操作。 例如，當處理執行緒正在處理資料時，主執行緒不能改變該資料。 管理這項作業的其中一種方式是透過安全線程同步處理物件，例如信號、事件和 mutex。

同時，當處理執行緒正在執行時，必須避免某些使用者互動。 在範例程式中，應用程式資料會受到保護，而且使用者互動的限制是由 [強制回應的進度] 對話方塊來管理列印工作處理。 強制回應對話方塊會防止使用者與程式的主視窗互動，這可防止使用者在列印資料時改變應用程式資料。

當列印工作正在處理時，使用者可以執行的唯一動作是取消列印工作。 這項限制是由資料指標圖形向使用者發出信號。 當游標停留在 [ **取消** ] 按鈕上時，就會顯示箭號游標，指出使用者可以按一下此按鈕。 當游標停留在程式視窗區域的任何其他部分時，就會顯示等候游標，指出程式正在忙碌中，而且無法回應使用者輸入。

## <a name="creating-the-printing-thread-procedure"></a>建立列印執行緒程式

我們建議您在列印處理時包含這些功能。

-   **列印處理分為幾個步驟**

    如果使用者按一下 [ **取消** ] 按鈕，您可以將列印處理分割成不連續的處理步驟。 這項功能很有用，因為列印處理可能包括處理器密集的作業。 將此處理程式細分為步驟，可能會導致列印處理無法封鎖或延遲其他執行緒或進程。 將處理常式分解為邏輯步驟也可讓您在任何時間點完全終止列印處理，如此一來，完成列印工作之後，就不會離開任何孤立的資源。

    這是列印步驟的範例清單。

    ```C++
    HRESULT PrintStep_1_StartJob (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_2_DoOnePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_3_DoOneDoc (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_4_DoOnePage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_5_ClosePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_6_CloseJob (PPRINTTHREADINFO threadInfo);
    ```

    

-   **檢查步驟之間的取消事件**

    當使用者按一下 [ **取消** ] 按鈕時，使用者介面執行緒會發出取消事件的信號。 處理執行緒必須定期檢查取消事件，以知道使用者何時按一下 [ **取消** ] 按鈕。 [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)語句會執行這種檢查，而且也會提供其他程式執行的機會，讓列印工作處理不會封鎖或延遲其他執行緒或進程。

    下列程式碼範例將說明其中一個測試，以查看是否發生取消事件。

    ```C++
    waitStatus = WaitForSingleObject (
                    threadInfo->quitEvent, 
                    stepDelay);
    if (WAIT_OBJECT_0 == waitStatus)
    {
        hr = E_ABORT;
    }
    ```

    

-   **將狀態更新傳送至使用者介面執行緒**

    在每個列印處理步驟中，列印處理執行緒都會將更新訊息傳送至 [列印進度] 對話方塊，讓它可以更新進度列。 請注意，[列印進度] 對話方塊正在 UI 執行緒中執行。

    下列程式碼範例說明其中一個更新訊息呼叫。

    ```C++
    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    ```

    

## <a name="starting-the-printing-thread"></a>啟動列印執行緒

列印處理執行緒會執行，直到 PrintThreadProc 函式返回為止。 下列步驟會啟動列印執行緒。

1.  **準備資料和使用者介面元素以進行列印。**

    開始列印處理執行緒之前，您必須先初始化描述列印工作和使用者介面元素的資料元素。 這些元素包括資料指標狀態，如此就會適當地顯示等候游標。 您也必須設定進度列，以反映列印工作的大小。 以下將詳細說明這些準備步驟 [：如何：收集使用者的列印工作資訊](preparing-to-print.md)。

    下列程式碼範例示範如何設定進度列，以反映使用者所要求的列印工作大小。

    ```C++
    // Compute the number of steps in this job.
    stepCount = (((
                // One copy of a document contains
                //  one step for each page +
                //  one step for the document
                ((threadInfo->documentContent)->pages + 1) * 
                // Each copy of the document includes
                //  two steps to open and close the document
                threadInfo->copies) + 2) * 
                // Each job includes one step to start the job
                threadInfo->packages) + 1;
    // Send the total number of steps to the progress bar control.
    SendMessage (
        dlgInfo->progressBarWindow, 
        PBM_SETRANGE32, 
        0L, 
        (stepCount));
    ```

    

2.  **啟動列印處理執行緒。**

    呼叫 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) 以啟動處理執行緒。

    下列程式碼範例會啟動處理執行緒。

    ```C++
    // Start the printing thread
    threadInfo->printThreadHandle = CreateThread (
                    NULL, 
                    0L, 
                    (LPTHREAD_START_ROUTINE)PrintThreadProc,
                    (LPVOID)threadInfo, 
                    0L, 
                    &threadInfo->printThreadId);
    ```

    

3.  **檢查啟動時列印處理是否失敗。**

    如果成功建立執行緒， [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)會傳回已建立之執行緒的控制碼。 在新執行緒中啟動的 PrintThreadProc 函式會先檢查某些條件，再開始進行實際的列印工作處理。 如果偵測到這些檢查中有任何錯誤，PrintThreadProc 可能會傳回，而不會處理任何列印工作資料。 UI 執行緒可以檢查處理執行緒是否已順利啟動，方法是等候執行緒控制碼的時間超過執行初始測試所花費的時間，但不再需要。 當執行緒結束時，執行緒的控制碼會變成發出信號。 程式碼會在啟動處理執行緒之後，檢查執行緒的狀態是否短一段時間。 當發生超時或執行緒控制碼收到信號時， [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) 函數會傳回。 如果 **WaitForSingleObject** 函式傳回 **等候 \_ 物件 \_ 0** 狀態，執行緒會提早結束，因此您應該關閉列印進度對話方塊，如下列程式碼範例所示。

    ```C++
    // Make sure the printing thread started OK
    //  by waiting to see if it is still running after
    //  a short period of time. This time delay should be
    //  long enough to know that it's running but shorter
    //  than the shortest possible print job.
    waitStatus = WaitForSingleObject (
        threadInfo->printThreadHandle, 
        THREAD_START_WAIT);

    // If the object is signaled, that means that the
    //  thread terminated before the timeout period elapsed.
    if (WAIT_OBJECT_0 == waitStatus)
    {
        // The thread exited, so post close messages.
        PostMessage (hDlg, USER_PRINT_CLOSING, 0L, (LPARAM)E_FAIL);
        PostMessage (hDlg, USER_PRINT_COMPLETE, 0L, (LPARAM)E_FAIL);
    }
    ```

    

## <a name="stopping-the-printing-thread"></a>停止列印執行緒

當使用者按一下 [列印進度] 對話方塊中的 [ **取消** ] 按鈕時，會通知列印執行緒，讓它能夠以有條理的方式停止處理列印工作。 雖然 [ **取消** ] 按鈕和 **quitEvent** 事件是這項處理的重要層面，但您必須設計整個處理順序才能成功中斷。 這表示，如果使用者在完成之前取消順序，則序列中的步驟不能保留任何未釋放的已配置資源。

下列程式碼範例會示範範例程式如何先檢查 **quitEvent** ，然後再處理所列印檔案中的每個頁面。 如果 **quitEvent** 已收到信號，或偵測到錯誤，列印處理就會停止。


```C++
// While no errors and the user hasn't clicked cancel...
while (((waitStatus = WaitForSingleObject (
                        threadInfo->quitEvent, 
                        stepDelay)) == WAIT_TIMEOUT) &&
        SUCCEEDED(hr))
{
    // ...print one page
    hr = PrintStep_4_DoOnePage (threadInfo);

    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    

    if (threadInfo->currentPage < (threadInfo->documentContent)->pages)
    {
        // More pages, so continue to the next one
        threadInfo->currentPage++;
    }
    else
    {
        // Last page printed so exit loop and close
        break;
    }
}
```



 

 
