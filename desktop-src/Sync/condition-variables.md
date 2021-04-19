---
description: 條件變數是同步處理原始物件，可讓執行緒等候，直到發生特定條件為止。 條件變數是無法跨進程共用的使用者模式物件。
ms.assetid: fef9bab0-cd69-4812-869a-b43a10772d86
title: 條件變數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711fad7d80c1c5e06fc6e496198cd298b190daba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980408"
---
# <a name="condition-variables"></a><span data-ttu-id="5267c-104">條件變數</span><span class="sxs-lookup"><span data-stu-id="5267c-104">Condition Variables</span></span>

<span data-ttu-id="5267c-105">條件變數是同步處理原始物件，可讓執行緒等候，直到發生特定條件為止。</span><span class="sxs-lookup"><span data-stu-id="5267c-105">Condition variables are synchronization primitives that enable threads to wait until a particular condition occurs.</span></span> <span data-ttu-id="5267c-106">條件變數是無法跨進程共用的使用者模式物件。</span><span class="sxs-lookup"><span data-stu-id="5267c-106">Condition variables are user-mode objects that cannot be shared across processes.</span></span>

<span data-ttu-id="5267c-107">條件變數可讓執行緒以不可部分完成的方式釋放鎖定，並進入睡眠狀態。</span><span class="sxs-lookup"><span data-stu-id="5267c-107">Condition variables enable threads to atomically release a lock and enter the sleeping state.</span></span> <span data-ttu-id="5267c-108">它們可與重要區段或超薄讀取器/寫入器搭配使用 (SRW) 鎖定。</span><span class="sxs-lookup"><span data-stu-id="5267c-108">They can be used with critical sections or slim reader/writer (SRW) locks.</span></span> <span data-ttu-id="5267c-109">條件變數支援「喚醒一個」或「喚醒所有」等候中線程的作業。</span><span class="sxs-lookup"><span data-stu-id="5267c-109">Condition variables support operations that "wake one" or "wake all" waiting threads.</span></span> <span data-ttu-id="5267c-110">喚醒執行緒之後，它會重新取得執行緒進入睡眠狀態時所釋放的鎖定。</span><span class="sxs-lookup"><span data-stu-id="5267c-110">After a thread is woken, it re-acquires the lock it released when the thread entered the sleeping state.</span></span>

<span data-ttu-id="5267c-111">請注意，呼叫端必須配置 **條件 \_ 變數** 結構，並將它初始化，方法是呼叫 [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (，以動態方式初始化結構) 或將常數 **條件 \_ 變數 \_ INIT** 指派給結構變數 (以靜態方式) 初始化結構。</span><span class="sxs-lookup"><span data-stu-id="5267c-111">Note that the caller must allocate a **CONDITION\_VARIABLE** structure and initialize it by either calling [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (to initialize the structure dynamically) or assign the constant **CONDITION\_VARIABLE\_INIT** to the structure variable (to initialize the structure statically).</span></span>

<span data-ttu-id="5267c-112">**Windows Server 2003 和 WINDOWS XP：** 不支援條件變數。</span><span class="sxs-lookup"><span data-stu-id="5267c-112">**Windows Server 2003 and Windows XP:** Condition variables are not supported.</span></span>

<span data-ttu-id="5267c-113">以下是條件變數函數。</span><span class="sxs-lookup"><span data-stu-id="5267c-113">The following are the condition variable functions.</span></span>



| <span data-ttu-id="5267c-114">Condition 變數函式</span><span class="sxs-lookup"><span data-stu-id="5267c-114">Condition variable function</span></span>                                        | <span data-ttu-id="5267c-115">Description</span><span class="sxs-lookup"><span data-stu-id="5267c-115">Description</span></span>                                                                                                    |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5267c-116">**InitializeConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="5267c-116">**InitializeConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | <span data-ttu-id="5267c-117">初始化條件變數。</span><span class="sxs-lookup"><span data-stu-id="5267c-117">Initializes a condition variable.</span></span>                                                                              |
| [<span data-ttu-id="5267c-118">**SleepConditionVariableCS**</span><span class="sxs-lookup"><span data-stu-id="5267c-118">**SleepConditionVariableCS**</span></span>](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | <span data-ttu-id="5267c-119">在指定的條件變數上進入睡眠狀態，並以不可部分完成的作業形式釋放指定的重要區段。</span><span class="sxs-lookup"><span data-stu-id="5267c-119">Sleeps on the specified condition variable and releases the specified critical section as an atomic operation.</span></span> |
| [<span data-ttu-id="5267c-120">**SleepConditionVariableSRW**</span><span class="sxs-lookup"><span data-stu-id="5267c-120">**SleepConditionVariableSRW**</span></span>](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | <span data-ttu-id="5267c-121">在指定的條件變數上進入睡眠狀態，並以不可部分完成的作業形式釋放指定的 SRW 鎖定。</span><span class="sxs-lookup"><span data-stu-id="5267c-121">Sleeps on the specified condition variable and releases the specified SRW lock as an atomic operation.</span></span>         |
| [<span data-ttu-id="5267c-122">**WakeAllConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="5267c-122">**WakeAllConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | <span data-ttu-id="5267c-123">喚醒所有等候指定條件變數的執行緒。</span><span class="sxs-lookup"><span data-stu-id="5267c-123">Wakes all threads waiting on the specified condition variable.</span></span>                                                 |
| [<span data-ttu-id="5267c-124">**WakeConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="5267c-124">**WakeConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | <span data-ttu-id="5267c-125">喚醒等候指定條件變數的單一執行緒。</span><span class="sxs-lookup"><span data-stu-id="5267c-125">Wakes a single thread waiting on the specified condition variable.</span></span>                                             |



 

<span data-ttu-id="5267c-126">下列虛擬程式碼示範條件變數的一般使用模式。</span><span class="sxs-lookup"><span data-stu-id="5267c-126">The following pseudocode demonstrates the typical usage pattern of condition variables.</span></span>

``` syntax
CRITICAL_SECTION CritSection;
CONDITION_VARIABLE ConditionVar;

void PerformOperationOnSharedData()
{ 
   EnterCriticalSection(&CritSection);

   // Wait until the predicate is TRUE

   while( TestPredicate() == FALSE )
   {
      SleepConditionVariableCS(&ConditionVar, &CritSection, INFINITE);
   }

   // The data can be changed safely because we own the critical 
   // section and the predicate is TRUE

   ChangeSharedData();

   LeaveCriticalSection(&CritSection);

   // If necessary, signal the condition variable by calling
   // WakeConditionVariable or WakeAllConditionVariable so other
   // threads can wake
}
```

<span data-ttu-id="5267c-127">例如，在讀取器/寫入器鎖定的執行中，此函式 `TestPredicate` 會驗證目前的鎖定要求與現有的擁有者是否相容。</span><span class="sxs-lookup"><span data-stu-id="5267c-127">For example, in an implementation of a reader/writer lock, the `TestPredicate` function would verify that the current lock request is compatible with the existing owners.</span></span> <span data-ttu-id="5267c-128">如果是，則取得鎖定;否則，睡眠。</span><span class="sxs-lookup"><span data-stu-id="5267c-128">If it is, acquire the lock; otherwise, sleep.</span></span> <span data-ttu-id="5267c-129">如需更詳細的範例，請參閱 [使用條件變數](using-condition-variables.md)。</span><span class="sxs-lookup"><span data-stu-id="5267c-129">For a more detailed example, see [Using Condition Variables](using-condition-variables.md).</span></span>

<span data-ttu-id="5267c-130">條件變數會受限於未與明確喚醒) 和遭竊的假喚醒 (， (另一個執行緒會在喚醒執行緒) 之前執行管理。</span><span class="sxs-lookup"><span data-stu-id="5267c-130">Condition variables are subject to spurious wakeups (those not associated with an explicit wake) and stolen wakeups (another thread manages to run before the woken thread).</span></span> <span data-ttu-id="5267c-131">因此，您應該在睡眠作業傳回之後，重新檢查述詞 (通常會在 **while** 迴圈中) 。</span><span class="sxs-lookup"><span data-stu-id="5267c-131">Therefore, you should recheck a predicate (typically in a **while** loop) after a sleep operation returns.</span></span>

<span data-ttu-id="5267c-132">您可以使用 [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) 或 [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) 來喚醒其他執行緒，其方式是在與條件變數相關聯的鎖定內部或外部。</span><span class="sxs-lookup"><span data-stu-id="5267c-132">You can wake other threads using [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) or [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) either inside or outside the lock associated with the condition variable.</span></span> <span data-ttu-id="5267c-133">通常最好先釋放鎖定再喚醒其他執行緒，以減少內容切換的數目。</span><span class="sxs-lookup"><span data-stu-id="5267c-133">It is usually better to release the lock before waking other threads to reduce the number of context switches.</span></span>

<span data-ttu-id="5267c-134">使用多個具有相同鎖定的條件變數通常很方便。</span><span class="sxs-lookup"><span data-stu-id="5267c-134">It is often convenient to use more than one condition variable with the same lock.</span></span> <span data-ttu-id="5267c-135">例如，讀取器/寫入器鎖定的執行可能會使用單一重要區段，但會針對讀取器和寫入器分隔線件變數。</span><span class="sxs-lookup"><span data-stu-id="5267c-135">For example, an implementation of a reader/writer lock might use a single critical section but separate condition variables for readers and writers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5267c-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="5267c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5267c-137">使用條件變數</span><span class="sxs-lookup"><span data-stu-id="5267c-137">Using Condition Variables</span></span>](using-condition-variables.md)
</dt> </dl>

 

 
