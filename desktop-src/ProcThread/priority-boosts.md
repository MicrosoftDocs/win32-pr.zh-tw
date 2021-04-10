---
description: 每個執行緒都有動態優先權。
ms.assetid: bcc6cec7-2d85-4810-98d0-7d99486f4924
title: 優先權提升
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f463f30b0abffb24daadb4241ad32c5b51f123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192758"
---
# <a name="priority-boosts"></a><span data-ttu-id="ac37c-103">優先權提升</span><span class="sxs-lookup"><span data-stu-id="ac37c-103">Priority Boosts</span></span>

<span data-ttu-id="ac37c-104">每個執行緒都有 *動態優先權*。</span><span class="sxs-lookup"><span data-stu-id="ac37c-104">Each thread has a *dynamic priority*.</span></span> <span data-ttu-id="ac37c-105">這是排程器用來判斷要執行哪個執行緒的優先權。</span><span class="sxs-lookup"><span data-stu-id="ac37c-105">This is the priority the scheduler uses to determine which thread to execute.</span></span> <span data-ttu-id="ac37c-106">一開始，執行緒的動態優先權與其基底優先權相同。</span><span class="sxs-lookup"><span data-stu-id="ac37c-106">Initially, a thread's dynamic priority is the same as its base priority.</span></span> <span data-ttu-id="ac37c-107">系統可以提升和降低動態優先順序，以確保它有回應，而且沒有任何執行緒會耗盡處理器時間。</span><span class="sxs-lookup"><span data-stu-id="ac37c-107">The system can boost and lower the dynamic priority, to ensure that it is responsive and that no threads are starved for processor time.</span></span> <span data-ttu-id="ac37c-108">系統不會提高基底優先權層級介於16到31之間的執行緒優先順序。</span><span class="sxs-lookup"><span data-stu-id="ac37c-108">The system does not boost the priority of threads with a base priority level between 16 and 31.</span></span> <span data-ttu-id="ac37c-109">只有基底優先順序介於0和15之間的執行緒才能獲得動態優先權。</span><span class="sxs-lookup"><span data-stu-id="ac37c-109">Only threads with a base priority between 0 and 15 receive dynamic priority boosts.</span></span>

<span data-ttu-id="ac37c-110">系統會提高執行緒的動態優先順序，以增強其回應性，如下所示。</span><span class="sxs-lookup"><span data-stu-id="ac37c-110">The system boosts the dynamic priority of a thread to enhance its responsiveness as follows.</span></span>

-   <span data-ttu-id="ac37c-111">當使用 NORMAL \_ PRIORITY 類別的進程 \_ 進入前景時，排程器會提高與前景視窗相關聯之進程的優先權類別，使其大於或等於任何背景進程的 priority 類別。</span><span class="sxs-lookup"><span data-stu-id="ac37c-111">When a process that uses NORMAL\_PRIORITY\_CLASS is brought to the foreground, the scheduler boosts the priority class of the process associated with the foreground window, so that it is greater than or equal to the priority class of any background processes.</span></span> <span data-ttu-id="ac37c-112">當進程不再存在於前景時，優先順序類別會回到其原始的設定。</span><span class="sxs-lookup"><span data-stu-id="ac37c-112">The priority class returns to its original setting when the process is no longer in the foreground.</span></span>
-   <span data-ttu-id="ac37c-113">當視窗接收到輸入（例如計時器訊息、滑鼠訊息或鍵盤輸入）時，排程器會提高擁有視窗之執行緒的優先順序。</span><span class="sxs-lookup"><span data-stu-id="ac37c-113">When a window receives input, such as timer messages, mouse messages, or keyboard input, the scheduler boosts the priority of the thread that owns the window.</span></span>
-   <span data-ttu-id="ac37c-114">當滿足已封鎖執行緒的等候條件時，排程器會提高執行緒的優先順序。</span><span class="sxs-lookup"><span data-stu-id="ac37c-114">When the wait conditions for a blocked thread are satisfied, the scheduler boosts the priority of the thread.</span></span> <span data-ttu-id="ac37c-115">例如，當與磁片或鍵盤 i/o 相關聯的等候操作完成時，執行緒會獲得優先權提升。</span><span class="sxs-lookup"><span data-stu-id="ac37c-115">For example, when a wait operation associated with disk or keyboard I/O finishes, the thread receives a priority boost.</span></span>

    <span data-ttu-id="ac37c-116">您可以藉由呼叫 [**SetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost) 或 [**SetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost) 函式來停用優先權提升功能。</span><span class="sxs-lookup"><span data-stu-id="ac37c-116">You can disable the priority-boosting feature by calling the [**SetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost) or [**SetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost) function.</span></span> <span data-ttu-id="ac37c-117">若要判斷是否已停用此功能，請呼叫 [**GetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost) 或 [**GetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost) 函式。</span><span class="sxs-lookup"><span data-stu-id="ac37c-117">To determine whether this feature has been disabled, call the [**GetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost) or [**GetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost) function.</span></span>

<span data-ttu-id="ac37c-118">在引發執行緒的動態優先順序之後，排程器會在每次執行緒完成時間配量時，將該優先權降到一層級，直到執行緒回復為其基底優先順序為止。</span><span class="sxs-lookup"><span data-stu-id="ac37c-118">After raising a thread's dynamic priority, the scheduler reduces that priority by one level each time the thread completes a time slice, until the thread drops back to its base priority.</span></span> <span data-ttu-id="ac37c-119">執行緒的動態優先權絕對不會小於其基底優先順序。</span><span class="sxs-lookup"><span data-stu-id="ac37c-119">A thread's dynamic priority is never less than its base priority.</span></span>

 

 
