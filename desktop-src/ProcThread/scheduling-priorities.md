---
description: 執行緒已排程為根據其排程優先權執行。
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: 排程優先順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e80c8baf4ed066ec7034c97850248f81c298c65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976890"
---
# <a name="scheduling-priorities"></a><span data-ttu-id="42108-103">排程優先順序</span><span class="sxs-lookup"><span data-stu-id="42108-103">Scheduling Priorities</span></span>

<span data-ttu-id="42108-104">執行緒已排程為根據其 *排程優先權* 執行。</span><span class="sxs-lookup"><span data-stu-id="42108-104">Threads are scheduled to run based on their *scheduling priority*.</span></span> <span data-ttu-id="42108-105">每個執行緒都會指派排程優先權。</span><span class="sxs-lookup"><span data-stu-id="42108-105">Each thread is assigned a scheduling priority.</span></span> <span data-ttu-id="42108-106">優先權層級的範圍從零 (最低優先順序) 到 31 (最高優先順序) 。</span><span class="sxs-lookup"><span data-stu-id="42108-106">The priority levels range from zero (lowest priority) to 31 (highest priority).</span></span> <span data-ttu-id="42108-107">只有零頁執行緒的優先順序可以是零。</span><span class="sxs-lookup"><span data-stu-id="42108-107">Only the zero-page thread can have a priority of zero.</span></span> <span data-ttu-id="42108-108"> (零頁執行緒是系統執行緒，負責在沒有其他需要執行的執行緒時，將任何可用的頁面清空。 ) </span><span class="sxs-lookup"><span data-stu-id="42108-108">(The zero-page thread is a system thread responsible for zeroing any free pages when there are no other threads that need to run.)</span></span>

<span data-ttu-id="42108-109">系統會將具有相同優先權的所有線程視為相等。</span><span class="sxs-lookup"><span data-stu-id="42108-109">The system treats all threads with the same priority as equal.</span></span> <span data-ttu-id="42108-110">系統會以迴圈配置資源的方式，將時間配量指派給優先順序最高的所有線程。</span><span class="sxs-lookup"><span data-stu-id="42108-110">The system assigns time slices in a round-robin fashion to all threads with the highest priority.</span></span> <span data-ttu-id="42108-111">如果這些執行緒都未準備好執行，系統會以迴圈配置資源的方式，將時間配量指派給下一個最高優先順序的所有線程。</span><span class="sxs-lookup"><span data-stu-id="42108-111">If none of these threads are ready to run, the system assigns time slices in a round-robin fashion to all threads with the next highest priority.</span></span> <span data-ttu-id="42108-112">如果有較高優先順序的執行緒可供執行，系統就會停止執行較低優先順序的執行緒 (而不允許它使用時間配量) 完成，並將完整的時間配量指派給較高優先順序的執行緒。</span><span class="sxs-lookup"><span data-stu-id="42108-112">If a higher-priority thread becomes available to run, the system ceases to execute the lower-priority thread (without allowing it to finish using its time slice) and assigns a full time slice to the higher-priority thread.</span></span> <span data-ttu-id="42108-113">如需詳細資訊，請參閱 [內容切換](context-switches.md)。</span><span class="sxs-lookup"><span data-stu-id="42108-113">For more information, see [Context Switches](context-switches.md).</span></span>

<span data-ttu-id="42108-114">每個執行緒的優先順序取決於下列準則：</span><span class="sxs-lookup"><span data-stu-id="42108-114">The priority of each thread is determined by the following criteria:</span></span>

-   <span data-ttu-id="42108-115">其進程的 priority 類別</span><span class="sxs-lookup"><span data-stu-id="42108-115">The priority class of its process</span></span>
-   <span data-ttu-id="42108-116">執行緒在其進程的 priority 類別中的優先權層級</span><span class="sxs-lookup"><span data-stu-id="42108-116">The priority level of the thread within the priority class of its process</span></span>

<span data-ttu-id="42108-117">優先順序類別和優先權層級會合並以形成執行緒的 *基本優先權* 。</span><span class="sxs-lookup"><span data-stu-id="42108-117">The priority class and priority level are combined to form the *base priority* of a thread.</span></span> <span data-ttu-id="42108-118">如需執行緒動態優先權的詳細資訊，請參閱 [優先權提升](priority-boosts.md)。</span><span class="sxs-lookup"><span data-stu-id="42108-118">For information on the dynamic priority of a thread, see [Priority Boosts](priority-boosts.md).</span></span>

## <a name="priority-class"></a><span data-ttu-id="42108-119">Priority 類別</span><span class="sxs-lookup"><span data-stu-id="42108-119">Priority Class</span></span>

<span data-ttu-id="42108-120">每個進程都屬於下列其中一個優先順序類別：</span><span class="sxs-lookup"><span data-stu-id="42108-120">Each process belongs to one of the following priority classes:</span></span><dl> <span data-ttu-id="42108-121">閒置 \_ 優先權 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="42108-121">IDLE\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="42108-122">低於 \_ 一般 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="42108-122">BELOW\_NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="42108-123">一般 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="42108-123">NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="42108-124">高於 \_ 一般 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="42108-124">ABOVE\_NORMAL\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="42108-125">高 \_ 優先順序 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="42108-125">HIGH\_PRIORITY\_CLASS</span></span>  
<span data-ttu-id="42108-126">即時 \_ 優先權 \_ 類別</span><span class="sxs-lookup"><span data-stu-id="42108-126">REALTIME\_PRIORITY\_CLASS</span></span>  
</dl>

<span data-ttu-id="42108-127">依預設，進程的 priority 類別為一般 \_ 優先順序 \_ 類別。</span><span class="sxs-lookup"><span data-stu-id="42108-127">By default, the priority class of a process is NORMAL\_PRIORITY\_CLASS.</span></span> <span data-ttu-id="42108-128">當您建立子進程時，請使用 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數來指定子進程的優先權類別。</span><span class="sxs-lookup"><span data-stu-id="42108-128">Use the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function to specify the priority class of a child process when you create it.</span></span> <span data-ttu-id="42108-129">如果呼叫進程是閒置 \_ 優先權 \_ 類別或低於 \_ 一般 \_ 優先順序 \_ 類別，則新的進程會繼承這個類別。</span><span class="sxs-lookup"><span data-stu-id="42108-129">If the calling process is IDLE\_PRIORITY\_CLASS or BELOW\_NORMAL\_PRIORITY\_CLASS, the new process will inherit this class.</span></span> <span data-ttu-id="42108-130">您可以使用 [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) 函數來判斷進程的目前優先權類別，並使用 [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) 函數來變更進程的 priority 類別。</span><span class="sxs-lookup"><span data-stu-id="42108-130">Use the [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) function to determine the current priority class of a process and the [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) function to change the priority class of a process.</span></span>

<span data-ttu-id="42108-131">監視系統的進程（例如，會定期更新顯示器的螢幕保護裝置或應用程式）應該使用「閒置 \_ 優先順序」 \_ 類別。</span><span class="sxs-lookup"><span data-stu-id="42108-131">Processes that monitor the system, such as screen savers or applications that periodically update a display, should use IDLE\_PRIORITY\_CLASS.</span></span> <span data-ttu-id="42108-132">這可防止此進程的執行緒（沒有高優先順序）干擾較高優先順序的執行緒。</span><span class="sxs-lookup"><span data-stu-id="42108-132">This prevents the threads of this process, which do not have high priority, from interfering with higher priority threads.</span></span>

<span data-ttu-id="42108-133">請小心使用高 \_ 優先順序 \_ 類別。</span><span class="sxs-lookup"><span data-stu-id="42108-133">Use HIGH\_PRIORITY\_CLASS with care.</span></span> <span data-ttu-id="42108-134">如果執行緒在較高的優先權層級執行了較長的時間，則系統中的其他執行緒將不會取得處理器時間。</span><span class="sxs-lookup"><span data-stu-id="42108-134">If a thread runs at the highest priority level for extended periods, other threads in the system will not get processor time.</span></span> <span data-ttu-id="42108-135">如果有多個執行緒同時設定為高優先順序，執行緒就會失去其有效性。</span><span class="sxs-lookup"><span data-stu-id="42108-135">If several threads are set at high priority at the same time, the threads lose their effectiveness.</span></span> <span data-ttu-id="42108-136">高優先順序的類別應該保留給必須回應時間關鍵事件的執行緒。</span><span class="sxs-lookup"><span data-stu-id="42108-136">The high-priority class should be reserved for threads that must respond to time-critical events.</span></span> <span data-ttu-id="42108-137">如果您的應用程式執行一個需要高優先順序類別的工作，而其餘的工作都是一般優先順序，請使用 [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) 來暫時引發應用程式的 priority 類別;然後在時間關鍵工作完成後將它減少。</span><span class="sxs-lookup"><span data-stu-id="42108-137">If your application performs one task that requires the high-priority class while the rest of its tasks are normal priority, use [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) to raise the priority class of the application temporarily; then reduce it after the time-critical task has been completed.</span></span> <span data-ttu-id="42108-138">另一種策略是建立高優先順序的程式，讓它的所有線程都封鎖大部分的時間，只有在需要重要工作時才喚醒執行緒。</span><span class="sxs-lookup"><span data-stu-id="42108-138">Another strategy is to create a high-priority process that has all of its threads blocked most of the time, awakening threads only when critical tasks are needed.</span></span> <span data-ttu-id="42108-139">很重要的一點是，高優先順序的執行緒應該執行一小段時間，而且只有在具有要執行的時間緊迫工作時。</span><span class="sxs-lookup"><span data-stu-id="42108-139">The important point is that a high-priority thread should execute for a brief time, and only when it has time-critical work to perform.</span></span>

<span data-ttu-id="42108-140">您幾乎不應使用即時 \_ 優先權 \_ 類別，因為這會中斷管理滑鼠輸入、鍵盤輸入和背景磁片排清的系統執行緒。</span><span class="sxs-lookup"><span data-stu-id="42108-140">You should almost never use REALTIME\_PRIORITY\_CLASS, because this interrupts system threads that manage mouse input, keyboard input, and background disk flushing.</span></span> <span data-ttu-id="42108-141">此類別適用于與硬體直接進行「交談」的應用程式，或執行應該受限中斷的簡單工作。</span><span class="sxs-lookup"><span data-stu-id="42108-141">This class can be appropriate for applications that "talk" directly to hardware or that perform brief tasks that should have limited interruptions.</span></span>

## <a name="priority-level"></a><span data-ttu-id="42108-142">優先權層級</span><span class="sxs-lookup"><span data-stu-id="42108-142">Priority Level</span></span>

<span data-ttu-id="42108-143">以下是每個優先權類別內的優先權層級：</span><span class="sxs-lookup"><span data-stu-id="42108-143">The following are priority levels within each priority class:</span></span><dl> <span data-ttu-id="42108-144">執行緒 \_ 優先順序 \_ 閒置</span><span class="sxs-lookup"><span data-stu-id="42108-144">THREAD\_PRIORITY\_IDLE</span></span>  
<span data-ttu-id="42108-145">執行緒 \_ 優先順序 \_ 最低</span><span class="sxs-lookup"><span data-stu-id="42108-145">THREAD\_PRIORITY\_LOWEST</span></span>  
<span data-ttu-id="42108-146">一般的執行緒 \_ 優先順序 \_ \_</span><span class="sxs-lookup"><span data-stu-id="42108-146">THREAD\_PRIORITY\_BELOW\_NORMAL</span></span>  
<span data-ttu-id="42108-147">執行緒 \_ 優先順序 \_ 正常</span><span class="sxs-lookup"><span data-stu-id="42108-147">THREAD\_PRIORITY\_NORMAL</span></span>  
<span data-ttu-id="42108-148">\_ \_ 高於 \_ 一般的執行緒優先順序</span><span class="sxs-lookup"><span data-stu-id="42108-148">THREAD\_PRIORITY\_ABOVE\_NORMAL</span></span>  
<span data-ttu-id="42108-149">執行緒 \_ 優先順序 \_ 最高</span><span class="sxs-lookup"><span data-stu-id="42108-149">THREAD\_PRIORITY\_HIGHEST</span></span>  
<span data-ttu-id="42108-150">執行緒 \_ 優先順序 \_ 時間 \_ 嚴重不足</span><span class="sxs-lookup"><span data-stu-id="42108-150">THREAD\_PRIORITY\_TIME\_CRITICAL</span></span>  
</dl>

<span data-ttu-id="42108-151">所有線程都是使用執行緒 \_ 優先權 \_ NORMAL 來建立。</span><span class="sxs-lookup"><span data-stu-id="42108-151">All threads are created using THREAD\_PRIORITY\_NORMAL.</span></span> <span data-ttu-id="42108-152">這表示執行緒優先順序與進程優先權類別相同。</span><span class="sxs-lookup"><span data-stu-id="42108-152">This means that the thread priority is the same as the process priority class.</span></span> <span data-ttu-id="42108-153">在您建立執行緒之後，請使用 [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) 函數來調整其相對於進程中其他執行緒的優先權。</span><span class="sxs-lookup"><span data-stu-id="42108-153">After you create a thread, use the [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) function to adjust its priority relative to other threads in the process.</span></span>

<span data-ttu-id="42108-154">典型的策略是使用 \_ \_ \_ 處理常式輸入執行緒的一般一般或執行緒優先順序最高的執行緒優先順序 \_ \_ ，以確保應用程式能回應使用者。</span><span class="sxs-lookup"><span data-stu-id="42108-154">A typical strategy is to use THREAD\_PRIORITY\_ABOVE\_NORMAL or THREAD\_PRIORITY\_HIGHEST for the process's input thread, to ensure that the application is responsive to the user.</span></span> <span data-ttu-id="42108-155">背景執行緒（特別是處理器密集的執行緒）可以設定為 \_ \_ 低於 \_ 正常或執行緒優先順序的執行緒 \_ 優先順序 \_ ，以確保它們可以在必要時被佔用。</span><span class="sxs-lookup"><span data-stu-id="42108-155">Background threads, particularly those that are processor intensive, can be set to THREAD\_PRIORITY\_BELOW\_NORMAL or THREAD\_PRIORITY\_LOWEST, to ensure that they can be preempted when necessary.</span></span> <span data-ttu-id="42108-156">但是，如果您的執行緒等候另一個具有較低優先順序的執行緒完成一些工作，請務必封鎖等候高優先順序執行緒的執行。</span><span class="sxs-lookup"><span data-stu-id="42108-156">However, if you have a thread waiting for another thread with a lower priority to complete some task, be sure to block the execution of the waiting high-priority thread.</span></span> <span data-ttu-id="42108-157">若要這樣做，請使用 [wait](../sync/wait-functions.md)函式、 [重要區段](../sync/critical-section-objects.md)或 [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) 函數、 [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)或 [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) 函數。</span><span class="sxs-lookup"><span data-stu-id="42108-157">To do this, use a [wait function](../sync/wait-functions.md), [critical section](../sync/critical-section-objects.md), or the [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) function, [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex), or [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) function.</span></span> <span data-ttu-id="42108-158">最好是讓執行緒執行迴圈。</span><span class="sxs-lookup"><span data-stu-id="42108-158">This is preferable to having the thread execute a loop.</span></span> <span data-ttu-id="42108-159">否則，進程可能會變成鎖死，因為不會排定優先順序較低的執行緒。</span><span class="sxs-lookup"><span data-stu-id="42108-159">Otherwise, the process may become deadlocked, because the thread with lower priority is never scheduled.</span></span>

<span data-ttu-id="42108-160">若要判斷線程的目前優先權層級，請使用 [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) 函數。</span><span class="sxs-lookup"><span data-stu-id="42108-160">To determine the current priority level of a thread, use the [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) function.</span></span>

## <a name="base-priority"></a><span data-ttu-id="42108-161">基本優先順序</span><span class="sxs-lookup"><span data-stu-id="42108-161">Base Priority</span></span>

<span data-ttu-id="42108-162">系統會合並進程優先權類別和執行緒優先順序層級，以構成每個執行緒的基本優先權。</span><span class="sxs-lookup"><span data-stu-id="42108-162">The process priority class and thread priority level are combined to form the base priority of each thread.</span></span>

<span data-ttu-id="42108-163">下表顯示處理優先權類別和執行緒優先順序值組合的基本優先權。</span><span class="sxs-lookup"><span data-stu-id="42108-163">The following table shows the base priority for combinations of process priority class and thread priority value.</span></span>


<table>
<tr>
<th colspan="2"><span data-ttu-id="42108-164">進程優先順序類別</span><span class="sxs-lookup"><span data-stu-id="42108-164">Process priority class</span></span></th>
<th><span data-ttu-id="42108-165">執行緒優先順序層級</span><span class="sxs-lookup"><span data-stu-id="42108-165">Thread priority level</span></span></th>
<th><span data-ttu-id="42108-166">基本優先順序</span><span class="sxs-lookup"><span data-stu-id="42108-166">Base priority</span></span></th>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="42108-167">IDLE_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="42108-167">IDLE_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="42108-168">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="42108-168">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="42108-169">1</span><span class="sxs-lookup"><span data-stu-id="42108-169">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-170">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="42108-170">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="42108-171">2</span><span class="sxs-lookup"><span data-stu-id="42108-171">2</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-172">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-172">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="42108-173">3</span><span class="sxs-lookup"><span data-stu-id="42108-173">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-174">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-174">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="42108-175">4</span><span class="sxs-lookup"><span data-stu-id="42108-175">4</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-176">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-176">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="42108-177">5</span><span class="sxs-lookup"><span data-stu-id="42108-177">5</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-178">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="42108-178">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="42108-179">6</span><span class="sxs-lookup"><span data-stu-id="42108-179">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-180">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="42108-180">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="42108-181">15</span><span class="sxs-lookup"><span data-stu-id="42108-181">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="42108-182">BELOW_NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="42108-182">BELOW_NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="42108-183">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="42108-183">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="42108-184">1</span><span class="sxs-lookup"><span data-stu-id="42108-184">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-185">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="42108-185">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="42108-186">4</span><span class="sxs-lookup"><span data-stu-id="42108-186">4</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-187">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-187">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="42108-188">5</span><span class="sxs-lookup"><span data-stu-id="42108-188">5</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-189">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-189">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="42108-190">6</span><span class="sxs-lookup"><span data-stu-id="42108-190">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-191">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-191">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="42108-192">7</span><span class="sxs-lookup"><span data-stu-id="42108-192">7</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-193">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="42108-193">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="42108-194">8</span><span class="sxs-lookup"><span data-stu-id="42108-194">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-195">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="42108-195">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="42108-196">15</span><span class="sxs-lookup"><span data-stu-id="42108-196">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="42108-197">NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="42108-197">NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="42108-198">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="42108-198">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="42108-199">1</span><span class="sxs-lookup"><span data-stu-id="42108-199">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-200">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="42108-200">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="42108-201">6</span><span class="sxs-lookup"><span data-stu-id="42108-201">6</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-202">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-202">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="42108-203">7</span><span class="sxs-lookup"><span data-stu-id="42108-203">7</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-204">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-204">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="42108-205">8</span><span class="sxs-lookup"><span data-stu-id="42108-205">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-206">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-206">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="42108-207">9</span><span class="sxs-lookup"><span data-stu-id="42108-207">9</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-208">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="42108-208">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="42108-209">10</span><span class="sxs-lookup"><span data-stu-id="42108-209">10</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-210">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="42108-210">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="42108-211">15</span><span class="sxs-lookup"><span data-stu-id="42108-211">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="42108-212">ABOVE_NORMAL_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="42108-212">ABOVE_NORMAL_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="42108-213">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="42108-213">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="42108-214">1</span><span class="sxs-lookup"><span data-stu-id="42108-214">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-215">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="42108-215">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="42108-216">8</span><span class="sxs-lookup"><span data-stu-id="42108-216">8</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-217">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-217">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="42108-218">9</span><span class="sxs-lookup"><span data-stu-id="42108-218">9</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-219">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-219">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="42108-220">10</span><span class="sxs-lookup"><span data-stu-id="42108-220">10</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-221">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-221">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="42108-222">11</span><span class="sxs-lookup"><span data-stu-id="42108-222">11</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-223">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="42108-223">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="42108-224">12</span><span class="sxs-lookup"><span data-stu-id="42108-224">12</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-225">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="42108-225">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="42108-226">15</span><span class="sxs-lookup"><span data-stu-id="42108-226">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="42108-227">HIGH_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="42108-227">HIGH_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="42108-228">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="42108-228">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="42108-229">1</span><span class="sxs-lookup"><span data-stu-id="42108-229">1</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-230">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="42108-230">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="42108-231">11</span><span class="sxs-lookup"><span data-stu-id="42108-231">11</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-232">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-232">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="42108-233">12</span><span class="sxs-lookup"><span data-stu-id="42108-233">12</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-234">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-234">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="42108-235">13</span><span class="sxs-lookup"><span data-stu-id="42108-235">13</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-236">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-236">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="42108-237">14</span><span class="sxs-lookup"><span data-stu-id="42108-237">14</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-238">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="42108-238">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="42108-239">15</span><span class="sxs-lookup"><span data-stu-id="42108-239">15</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-240">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="42108-240">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="42108-241">15</span><span class="sxs-lookup"><span data-stu-id="42108-241">15</span></span></td>
</tr>
<tr>
<td rowspan="7" colspan="2"><span data-ttu-id="42108-242">REALTIME_PRIORITY_CLASS</span><span class="sxs-lookup"><span data-stu-id="42108-242">REALTIME_PRIORITY_CLASS</span></span> </td>
<td><span data-ttu-id="42108-243">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="42108-243">THREAD_PRIORITY_IDLE</span></span></td>
<td><span data-ttu-id="42108-244">16</span><span class="sxs-lookup"><span data-stu-id="42108-244">16</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-245">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="42108-245">THREAD_PRIORITY_LOWEST</span></span></td>
<td><span data-ttu-id="42108-246">22</span><span class="sxs-lookup"><span data-stu-id="42108-246">22</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-247">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-247">THREAD_PRIORITY_BELOW_NORMAL</span></span></td>
<td><span data-ttu-id="42108-248">23</span><span class="sxs-lookup"><span data-stu-id="42108-248">23</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-249">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-249">THREAD_PRIORITY_NORMAL</span></span></td>
<td><span data-ttu-id="42108-250">24</span><span class="sxs-lookup"><span data-stu-id="42108-250">24</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-251">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="42108-251">THREAD_PRIORITY_ABOVE_NORMAL</span></span></td>
<td><span data-ttu-id="42108-252">25</span><span class="sxs-lookup"><span data-stu-id="42108-252">25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-253">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="42108-253">THREAD_PRIORITY_HIGHEST</span></span></td>
<td><span data-ttu-id="42108-254">26</span><span class="sxs-lookup"><span data-stu-id="42108-254">26</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="42108-255">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="42108-255">THREAD_PRIORITY_TIME_CRITICAL</span></span></td>
<td><span data-ttu-id="42108-256">31</span><span class="sxs-lookup"><span data-stu-id="42108-256">31</span></span></td>
</tr>
</table>

 

 

 
