---
description: 本主題說明如何啟動和停止列印工作處理執行緒。
ms.assetid: CA3A81D6-332F-4867-881F-AC6859A076CF
title: 如何：啟動和停止列印執行緒
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9a47f81e384a135bb70e6deabefe15a3408a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194967"
---
# <a name="how-to-start-and-stop-a-printing-thread"></a><span data-ttu-id="bc2e0-103">如何：啟動和停止列印執行緒</span><span class="sxs-lookup"><span data-stu-id="bc2e0-103">How To: Start and Stop a Printing Thread</span></span>

<span data-ttu-id="bc2e0-104">本主題說明如何啟動和停止列印工作處理執行緒。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-104">This topic describes how to start and stop the print job processing thread.</span></span>

## <a name="overview"></a><span data-ttu-id="bc2e0-105">概觀</span><span class="sxs-lookup"><span data-stu-id="bc2e0-105">Overview</span></span>

<span data-ttu-id="bc2e0-106">若要防止列印活動封鎖使用者介面回應，請建立個別的執行緒來處理列印工作。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-106">To prevent printing activities from blocking the user interface response, create a separate thread to process the print job.</span></span> <span data-ttu-id="bc2e0-107">啟動程式時啟動的執行緒是處理使用者互動所產生之視窗訊息的執行緒，因此也就是 UI 執行緒。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-107">The thread that is started when the program is started, is the thread that handles the window messages that result from user interaction, and is therefore the UI thread.</span></span> <span data-ttu-id="bc2e0-108">程式必須在不延遲的情況下處理這些訊息，使用者介面才能及時回應使用者的滑鼠和鍵盤輸入。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-108">The program must process these messages without delay for the user interface to respond to the user's mouse and keyboard input in a timely manner.</span></span> <span data-ttu-id="bc2e0-109">為了讓程式能夠快速回應這些訊息，在任何一則訊息期間可以執行的處理量會受到限制。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-109">For the program to be able to respond to these messages quickly, the amount of processing that can be performed during any one message is limited.</span></span> <span data-ttu-id="bc2e0-110">當使用者要求需要大量處理時，不同的執行緒必須執行該處理，才能讓程式處理後續的使用者互動。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-110">When a user request requires extensive processing, a different thread must perform that processing to allow subsequent user interaction to be handled by the program.</span></span>

<span data-ttu-id="bc2e0-111">在不同的執行緒中處理資料時，程式必須協調使用者介面執行緒和處理執行緒的操作。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-111">Processing data in a separate thread requires the program to coordinate the operation of user interface thread and the processing thread.</span></span> <span data-ttu-id="bc2e0-112">例如，當處理執行緒正在處理資料時，主執行緒不能改變該資料。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-112">For example, while the processing thread is processing the data, the main thread must not alter that data.</span></span> <span data-ttu-id="bc2e0-113">管理這項作業的其中一種方式是透過安全線程同步處理物件，例如信號、事件和 mutex。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-113">One way to manage this is through thread-safe synchronization objects such as semaphores, events, and mutexes.</span></span>

<span data-ttu-id="bc2e0-114">同時，當處理執行緒正在執行時，必須避免某些使用者互動。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-114">At the same time, some user interaction must be prevented while the processing thread is running.</span></span> <span data-ttu-id="bc2e0-115">在範例程式中，應用程式資料會受到保護，而且使用者互動的限制是由 [強制回應的進度] 對話方塊來管理列印工作處理。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-115">In the sample program, the application data is protected and the user interaction is limited by having the print job processing be managed by the modal progress dialog box.</span></span> <span data-ttu-id="bc2e0-116">強制回應對話方塊會防止使用者與程式的主視窗互動，這可防止使用者在列印資料時改變應用程式資料。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-116">A modal dialog box prevents the user from interacting with the program's main window, which prevents the user from altering the application program data while the data is printed.</span></span>

<span data-ttu-id="bc2e0-117">當列印工作正在處理時，使用者可以執行的唯一動作是取消列印工作。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-117">The only action the user can perform while a print job is processing is to cancel the print job.</span></span> <span data-ttu-id="bc2e0-118">這項限制是由資料指標圖形向使用者發出信號。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-118">This restriction is signaled to the user by the cursor shape.</span></span> <span data-ttu-id="bc2e0-119">當游標停留在 [ **取消** ] 按鈕上時，就會顯示箭號游標，指出使用者可以按一下此按鈕。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-119">When the cursor is over the **Cancel** button, an arrow cursor is displayed, which indicates that the user can click this button.</span></span> <span data-ttu-id="bc2e0-120">當游標停留在程式視窗區域的任何其他部分時，就會顯示等候游標，指出程式正在忙碌中，而且無法回應使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-120">When the cursor is over any other part of the program's window area, a wait cursor is displayed, which indicates that the program is busy and cannot respond to user input.</span></span>

## <a name="creating-the-printing-thread-procedure"></a><span data-ttu-id="bc2e0-121">建立列印執行緒程式</span><span class="sxs-lookup"><span data-stu-id="bc2e0-121">Creating the Printing Thread Procedure</span></span>

<span data-ttu-id="bc2e0-122">我們建議您在列印處理時包含這些功能。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-122">We recommend including these features while print processing.</span></span>

-   <span data-ttu-id="bc2e0-123">**列印處理分為幾個步驟**</span><span class="sxs-lookup"><span data-stu-id="bc2e0-123">**Print processing is divided into steps**</span></span>

    <span data-ttu-id="bc2e0-124">如果使用者按一下 [ **取消** ] 按鈕，您可以將列印處理分割成不連續的處理步驟。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-124">You can divide the print processing into discrete processing steps that you can interrupt if the user clicks the **Cancel** button.</span></span> <span data-ttu-id="bc2e0-125">這項功能很有用，因為列印處理可能包括處理器密集的作業。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-125">This is useful because print processing can include processor-intensive operations.</span></span> <span data-ttu-id="bc2e0-126">將此處理程式細分為步驟，可能會導致列印處理無法封鎖或延遲其他執行緒或進程。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-126">Breaking this processing into steps can prevent the print processing from blocking or delaying other threads or processes.</span></span> <span data-ttu-id="bc2e0-127">將處理常式分解為邏輯步驟也可讓您在任何時間點完全終止列印處理，如此一來，完成列印工作之後，就不會離開任何孤立的資源。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-127">Breaking the processing into logical steps also makes it possible to cleanly terminate the print processing at any point, so that ending a print job before it has finished will not leave any orphaned resources.</span></span>

    <span data-ttu-id="bc2e0-128">這是列印步驟的範例清單。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-128">This is an example list of print steps.</span></span>

    ```C++
    HRESULT PrintStep_1_StartJob (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_2_DoOnePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_3_DoOneDoc (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_4_DoOnePage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_5_ClosePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_6_CloseJob (PPRINTTHREADINFO threadInfo);
    ```

    

-   <span data-ttu-id="bc2e0-129">**檢查步驟之間的取消事件**</span><span class="sxs-lookup"><span data-stu-id="bc2e0-129">**Check for a cancel event between steps**</span></span>

    <span data-ttu-id="bc2e0-130">當使用者按一下 [ **取消** ] 按鈕時，使用者介面執行緒會發出取消事件的信號。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-130">When the user clicks the **Cancel** button, the user interface thread signals the cancel event.</span></span> <span data-ttu-id="bc2e0-131">處理執行緒必須定期檢查取消事件，以知道使用者何時按一下 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-131">The processing thread must check the cancel event periodically to know when a user clicked the **Cancel** button.</span></span> <span data-ttu-id="bc2e0-132">[**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)語句會執行這種檢查，而且也會提供其他程式執行的機會，讓列印工作處理不會封鎖或延遲其他執行緒或進程。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-132">The [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) statements perform this check and they also give other programs a chance to run so that the print job processing doesn't block or delay other threads or processes.</span></span>

    <span data-ttu-id="bc2e0-133">下列程式碼範例將說明其中一個測試，以查看是否發生取消事件。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-133">The following code example illustrates one of the tests to see whether the cancel event has occurred.</span></span>

    ```C++
    waitStatus = WaitForSingleObject (
                    threadInfo->quitEvent, 
                    stepDelay);
    if (WAIT_OBJECT_0 == waitStatus)
    {
        hr = E_ABORT;
    }
    ```

    

-   <span data-ttu-id="bc2e0-134">**將狀態更新傳送至使用者介面執行緒**</span><span class="sxs-lookup"><span data-stu-id="bc2e0-134">**Send status updates to user interface thread**</span></span>

    <span data-ttu-id="bc2e0-135">在每個列印處理步驟中，列印處理執行緒都會將更新訊息傳送至 [列印進度] 對話方塊，讓它可以更新進度列。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-135">As each print processing step, the print processing thread sends update messages to the print progress dialog box so that it can update the progress bar.</span></span> <span data-ttu-id="bc2e0-136">請注意，[列印進度] 對話方塊正在 UI 執行緒中執行。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-136">Note that the print progress dialog box is running in the UI thread.</span></span>

    <span data-ttu-id="bc2e0-137">下列程式碼範例說明其中一個更新訊息呼叫。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-137">The following code example illustrates one of the update message calls.</span></span>

    ```C++
    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    ```

    

## <a name="starting-the-printing-thread"></a><span data-ttu-id="bc2e0-138">啟動列印執行緒</span><span class="sxs-lookup"><span data-stu-id="bc2e0-138">Starting the Printing Thread</span></span>

<span data-ttu-id="bc2e0-139">列印處理執行緒會執行，直到 PrintThreadProc 函式返回為止。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-139">The print processing thread runs until the PrintThreadProc function returns.</span></span> <span data-ttu-id="bc2e0-140">下列步驟會啟動列印執行緒。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-140">The following steps start the printing thread.</span></span>

1.  <span data-ttu-id="bc2e0-141">**準備資料和使用者介面元素以進行列印。**</span><span class="sxs-lookup"><span data-stu-id="bc2e0-141">**Prepare the data and user interface elements for printing.**</span></span>

    <span data-ttu-id="bc2e0-142">開始列印處理執行緒之前，您必須先初始化描述列印工作和使用者介面元素的資料元素。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-142">Before starting the print processing thread, you must initialize the data elements that describe the print job and the user interface elements.</span></span> <span data-ttu-id="bc2e0-143">這些元素包括資料指標狀態，如此就會適當地顯示等候游標。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-143">These elements include the cursor state, so that the wait cursor will be displayed appropriately.</span></span> <span data-ttu-id="bc2e0-144">您也必須設定進度列，以反映列印工作的大小。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-144">You must also configure the progress bar to reflect the size of the print job.</span></span> <span data-ttu-id="bc2e0-145">以下將詳細說明這些準備步驟 [：如何：收集使用者的列印工作資訊](preparing-to-print.md)。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-145">These preparation steps are described in detail in [How To: Collect Print Job Information from the User](preparing-to-print.md).</span></span>

    <span data-ttu-id="bc2e0-146">下列程式碼範例示範如何設定進度列，以反映使用者所要求的列印工作大小。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-146">The following code example shows how to configure the progress bar to reflect the size of the print job that the user requested.</span></span>

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

    

2.  <span data-ttu-id="bc2e0-147">**啟動列印處理執行緒。**</span><span class="sxs-lookup"><span data-stu-id="bc2e0-147">**Start the print processing thread.**</span></span>

    <span data-ttu-id="bc2e0-148">呼叫 [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) 以啟動處理執行緒。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-148">Call [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) to start the processing thread.</span></span>

    <span data-ttu-id="bc2e0-149">下列程式碼範例會啟動處理執行緒。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-149">The following code example starts the processing thread.</span></span>

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

    

3.  <span data-ttu-id="bc2e0-150">**檢查啟動時列印處理是否失敗。**</span><span class="sxs-lookup"><span data-stu-id="bc2e0-150">**Check whether print processing failed on start.**</span></span>

    <span data-ttu-id="bc2e0-151">如果成功建立執行緒， [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)會傳回已建立之執行緒的控制碼。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-151">[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) returns a handle to the created thread if the thread was created successfully.</span></span> <span data-ttu-id="bc2e0-152">在新執行緒中啟動的 PrintThreadProc 函式會先檢查某些條件，再開始進行實際的列印工作處理。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-152">The PrintThreadProc function that was started in the new thread checks some conditions before it starts the actual print job processing.</span></span> <span data-ttu-id="bc2e0-153">如果偵測到這些檢查中有任何錯誤，PrintThreadProc 可能會傳回，而不會處理任何列印工作資料。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-153">If it detects any errors in these checks, PrintThreadProc could return without processing any print job data.</span></span> <span data-ttu-id="bc2e0-154">UI 執行緒可以檢查處理執行緒是否已順利啟動，方法是等候執行緒控制碼的時間超過執行初始測試所花費的時間，但不再需要。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-154">The UI thread can check whether the processing thread started successfully by waiting on the thread handle for a period of time that is longer than it takes to perform the initial tests but no longer than necessary.</span></span> <span data-ttu-id="bc2e0-155">當執行緒結束時，執行緒的控制碼會變成發出信號。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-155">When the thread exits, the handle to the thread becomes signaled.</span></span> <span data-ttu-id="bc2e0-156">程式碼會在啟動處理執行緒之後，檢查執行緒的狀態是否短一段時間。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-156">The code checks the thread's state for a short period of time after it starts the processing thread.</span></span> <span data-ttu-id="bc2e0-157">當發生超時或執行緒控制碼收到信號時， [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) 函數會傳回。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-157">The [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function returns when either the timeout occurs or the thread handle is signaled.</span></span> <span data-ttu-id="bc2e0-158">如果 **WaitForSingleObject** 函式傳回 **等候 \_ 物件 \_ 0** 狀態，執行緒會提早結束，因此您應該關閉列印進度對話方塊，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-158">If the **WaitForSingleObject** function returns a **WAIT\_OBJECT\_0** status, the thread exited early and so you should close the print progress dialog, as the following code example shows.</span></span>

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

    

## <a name="stopping-the-printing-thread"></a><span data-ttu-id="bc2e0-159">停止列印執行緒</span><span class="sxs-lookup"><span data-stu-id="bc2e0-159">Stopping the Printing Thread</span></span>

<span data-ttu-id="bc2e0-160">當使用者按一下 [列印進度] 對話方塊中的 [ **取消** ] 按鈕時，會通知列印執行緒，讓它能夠以有條理的方式停止處理列印工作。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-160">When the user clicks the **Cancel** button in the print progress dialog box, the printing thread is notified so that it can stop processing the print job in an orderly manner.</span></span> <span data-ttu-id="bc2e0-161">雖然 [ **取消** ] 按鈕和 **quitEvent** 事件是這項處理的重要層面，但您必須設計整個處理順序才能成功中斷。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-161">While the **Cancel** button and the **quitEvent** event are important aspects of this processing, you must design the entire processing sequence to be interrupted successfully.</span></span> <span data-ttu-id="bc2e0-162">這表示，如果使用者在完成之前取消順序，則序列中的步驟不能保留任何未釋放的已配置資源。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-162">This means that the steps in the sequence must not leave any allocated resources that are not freed if a user cancels the sequence before it had completed.</span></span>

<span data-ttu-id="bc2e0-163">下列程式碼範例會示範範例程式如何先檢查 **quitEvent** ，然後再處理所列印檔案中的每個頁面。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-163">The following code example shows how the sample program checks the **quitEvent** before it processes each page in the document being printed.</span></span> <span data-ttu-id="bc2e0-164">如果 **quitEvent** 已收到信號，或偵測到錯誤，列印處理就會停止。</span><span class="sxs-lookup"><span data-stu-id="bc2e0-164">If the **quitEvent** is signaled or an error was detected, print processing stops.</span></span>


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



 

 
