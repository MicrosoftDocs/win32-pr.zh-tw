---
description: 在多處理器系統上執行時，應用程式可能會遇到問題，因為它們只會在單處理器系統上有效。
ms.assetid: b20a1d2c-b795-4ed8-ac33-539a347020c8
title: 同步處理和多處理器問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3896dc240e76f1506bac2a6a2e95f101b05beca7
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/21/2021
ms.locfileid: "107000499"
---
# <a name="synchronization-and-multiprocessor-issues"></a><span data-ttu-id="e11e5-103">同步處理和多處理器問題</span><span class="sxs-lookup"><span data-stu-id="e11e5-103">Synchronization and Multiprocessor Issues</span></span>

<span data-ttu-id="e11e5-104">在多處理器系統上執行時，應用程式可能會遇到問題，因為它們只會在單處理器系統上有效。</span><span class="sxs-lookup"><span data-stu-id="e11e5-104">Applications may encounter problems when run on multiprocessor systems due to assumptions they make which are valid only on single-processor systems.</span></span>

## <a name="thread-priorities"></a><span data-ttu-id="e11e5-105">執行緒優先順序</span><span class="sxs-lookup"><span data-stu-id="e11e5-105">Thread Priorities</span></span>

<span data-ttu-id="e11e5-106">請考慮具有兩個執行緒的程式，其優先順序高於另一個執行緒。</span><span class="sxs-lookup"><span data-stu-id="e11e5-106">Consider a program with two threads, one with a higher priority than the other.</span></span> <span data-ttu-id="e11e5-107">在單處理器系統上，較高優先順序的執行緒將不會放棄較低優先順序執行緒的控制權，因為排程器會提供優先權較高的執行緒。</span><span class="sxs-lookup"><span data-stu-id="e11e5-107">On a single-processor system, the higher priority thread will not relinquish control to the lower priority thread because the scheduler gives preference to higher priority threads.</span></span> <span data-ttu-id="e11e5-108">在多處理器系統上，這兩個執行緒可以同時執行，每個都在自己的處理器上執行。</span><span class="sxs-lookup"><span data-stu-id="e11e5-108">On a multiprocessor system, both threads can run simultaneously, each on its own processor.</span></span>

<span data-ttu-id="e11e5-109">應用程式應該同步處理資料結構的存取，以避免競爭情形。</span><span class="sxs-lookup"><span data-stu-id="e11e5-109">Applications should synchronize access to data structures to avoid race conditions.</span></span> <span data-ttu-id="e11e5-110">假設較高優先順序執行緒在不幹擾較低優先順序執行緒的情況下執行的程式碼，在多處理器系統上將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e11e5-110">Code that assumes that higher priority threads run without interference from lower priority threads will fail on multiprocessor systems.</span></span>

## <a name="memory-ordering"></a><span data-ttu-id="e11e5-111">記憶體順序</span><span class="sxs-lookup"><span data-stu-id="e11e5-111">Memory Ordering</span></span>

<span data-ttu-id="e11e5-112">當處理器寫入記憶體位置時，會快取此值以改善效能。</span><span class="sxs-lookup"><span data-stu-id="e11e5-112">When a processor writes to a memory location, the value is cached to improve performance.</span></span> <span data-ttu-id="e11e5-113">同樣地，處理器會嘗試滿足快取的讀取要求以改善效能。</span><span class="sxs-lookup"><span data-stu-id="e11e5-113">Similarly, the processor attempts to satisfy read requests from the cache to improve performance.</span></span> <span data-ttu-id="e11e5-114">此外，處理器在應用程式要求之前，會先從記憶體中提取值。</span><span class="sxs-lookup"><span data-stu-id="e11e5-114">Furthermore, processors begin to fetch values from memory before they are requested by the application.</span></span> <span data-ttu-id="e11e5-115">這種情況可能會發生在推理執行的過程中，或由於快取行的問題。</span><span class="sxs-lookup"><span data-stu-id="e11e5-115">This can happen as part of speculative execution or due to cache line issues.</span></span>

<span data-ttu-id="e11e5-116">CPU 快取可以分割成可以平行存取的銀行。</span><span class="sxs-lookup"><span data-stu-id="e11e5-116">CPU caches can be partitioned into banks that can be accessed in parallel.</span></span> <span data-ttu-id="e11e5-117">這表示記憶體作業可以依序完成。</span><span class="sxs-lookup"><span data-stu-id="e11e5-117">This means that memory operations can be completed out of order.</span></span> <span data-ttu-id="e11e5-118">為了確保記憶體作業已依序完成，大部分處理器都會提供記憶體屏障指令。</span><span class="sxs-lookup"><span data-stu-id="e11e5-118">To ensure that memory operations are completed in order, most processors provide memory-barrier instructions.</span></span> <span data-ttu-id="e11e5-119">*完整的記憶體屏障* 可確保記憶體屏障指令之前出現的記憶體讀取和寫入作業，會在記憶體關卡指令之後出現的任何記憶體讀取和寫入作業之前認可至記憶體。</span><span class="sxs-lookup"><span data-stu-id="e11e5-119">A *full memory barrier* ensures that memory read and write operations that appear before the memory barrier instruction are committed to memory before any memory read and write operations that appear after the memory barrier instruction.</span></span> <span data-ttu-id="e11e5-120">「 *讀取記憶體」屏障* 只會排序記憶體讀取作業，而 *寫入記憶體屏障* 只會對記憶體寫入作業進行排序。</span><span class="sxs-lookup"><span data-stu-id="e11e5-120">A *read memory barrier* orders only the memory read operations and a *write memory barrier* orders only the memory write operations.</span></span> <span data-ttu-id="e11e5-121">這些指示也可確保編譯器會停用任何可能在阻礙之間重新排列記憶體作業的優化。</span><span class="sxs-lookup"><span data-stu-id="e11e5-121">These instructions also ensure that the compiler disables any optimizations that could reorder memory operations across the barriers.</span></span>

<span data-ttu-id="e11e5-122">處理器可以使用取得、釋放和隔離語義來支援記憶體障礙的指示。</span><span class="sxs-lookup"><span data-stu-id="e11e5-122">Processors can support instructions for memory barriers with acquire, release, and fence semantics.</span></span> <span data-ttu-id="e11e5-123">這些語義會描述作業的結果可供使用的順序。</span><span class="sxs-lookup"><span data-stu-id="e11e5-123">These semantics describe the order in which results of an operation become available.</span></span> <span data-ttu-id="e11e5-124">使用取得語義時，作業的結果會在程式碼中出現的任何作業結果之前提供。</span><span class="sxs-lookup"><span data-stu-id="e11e5-124">With acquire semantics, the results of the operation are available before the results of any operation that appears after it in code.</span></span> <span data-ttu-id="e11e5-125">使用發行語義時，作業的結果會在程式碼中出現的任何作業結果之後使用。</span><span class="sxs-lookup"><span data-stu-id="e11e5-125">With release semantics, the results of the operation are available after the results of any operation that appears before it in code.</span></span> <span data-ttu-id="e11e5-126">範圍語義結合了取得和發行的語法。</span><span class="sxs-lookup"><span data-stu-id="e11e5-126">Fence semantics combine acquire and release semantics.</span></span> <span data-ttu-id="e11e5-127">具有範圍語義之作業的結果，可以在程式碼中出現的任何作業之前，以及在它之前出現的任何作業之後使用。</span><span class="sxs-lookup"><span data-stu-id="e11e5-127">The results of an operation with fence semantics are available before those of any operation that appears after it in code and after those of any operation that appears before it.</span></span>

<span data-ttu-id="e11e5-128">在支援 SSE2 的 x86 和 x64 處理器上，這些指示 **mfence** (記憶體隔離) 、 **lfence** (負載隔離) ，以及 **sfence** (存放區隔離) 。</span><span class="sxs-lookup"><span data-stu-id="e11e5-128">On x86 and x64 processors that support SSE2, the instructions are **mfence** (memory fence), **lfence** (load fence), and **sfence** (store fence).</span></span> <span data-ttu-id="e11e5-129">在 ARM 處理器上，instrutions 是 **.dmb** 和 **dsb**。</span><span class="sxs-lookup"><span data-stu-id="e11e5-129">On ARM processors, the instrutions are **dmb** and **dsb**.</span></span> <span data-ttu-id="e11e5-130">如需詳細資訊，請參閱處理器的檔。</span><span class="sxs-lookup"><span data-stu-id="e11e5-130">For more information, see the documentation for the processor.</span></span>

<span data-ttu-id="e11e5-131">下列同步處理函式會使用適當的阻礙來確保記憶體順序：</span><span class="sxs-lookup"><span data-stu-id="e11e5-131">The following synchronization functions use the appropriate barriers to ensure memory ordering:</span></span>

-   <span data-ttu-id="e11e5-132">輸入或離開重要區段的函式</span><span class="sxs-lookup"><span data-stu-id="e11e5-132">Functions that enter or leave critical sections</span></span>
-   <span data-ttu-id="e11e5-133">取得或釋放 SRW 鎖定的函式</span><span class="sxs-lookup"><span data-stu-id="e11e5-133">Functions that acquire or release SRW locks</span></span>
-   <span data-ttu-id="e11e5-134">一次性初始化開始和完成</span><span class="sxs-lookup"><span data-stu-id="e11e5-134">One-time initialization begin and completion</span></span>
-   <span data-ttu-id="e11e5-135">**EnterSynchronizationBarrier** 函式</span><span class="sxs-lookup"><span data-stu-id="e11e5-135">**EnterSynchronizationBarrier** function</span></span>
-   <span data-ttu-id="e11e5-136">信號同步處理物件的函數</span><span class="sxs-lookup"><span data-stu-id="e11e5-136">Functions that signal synchronization objects</span></span>
-   <span data-ttu-id="e11e5-137">Wait 函式</span><span class="sxs-lookup"><span data-stu-id="e11e5-137">Wait functions</span></span>
-   <span data-ttu-id="e11e5-138">連鎖函式 (除了具有 _NoFence_ 尾碼的函式之外，或具有 _\_ nf-e_ 尾碼的內建函式) </span><span class="sxs-lookup"><span data-stu-id="e11e5-138">Interlocked functions (except functions with _NoFence_ suffix, or intrinsics with _\_nf_ suffix)</span></span>

## <a name="fixing-a-race-condition"></a><span data-ttu-id="e11e5-139">修正競爭條件</span><span class="sxs-lookup"><span data-stu-id="e11e5-139">Fixing a Race Condition</span></span>

<span data-ttu-id="e11e5-140">下列程式碼在多處理器系統上有競爭條件，因為 `CacheComputedValue` 第一次執行的處理器可能會在 `fValueHasBeenComputed` 寫入主儲存體之前寫入主儲存體 `iValue` 。</span><span class="sxs-lookup"><span data-stu-id="e11e5-140">The following code has a race condition on a multiprocessor systems because the processor that executes `CacheComputedValue` the first time may write `fValueHasBeenComputed` to main memory before writing `iValue` to main memory.</span></span> <span data-ttu-id="e11e5-141">因此，在同一時間執行的第二個處理器 `FetchComputedValue` `fValueHasBeenComputed` 會讀取為 **TRUE**，但的新值 `iValue` 仍在第一個處理器的快取中，而且尚未寫入記憶體。</span><span class="sxs-lookup"><span data-stu-id="e11e5-141">Consequently, a second processor executing `FetchComputedValue` at the same time reads `fValueHasBeenComputed` as **TRUE**, but the new value of `iValue` is still in the first processor's cache and has not been written to memory.</span></span>

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

<span data-ttu-id="e11e5-142">您可以使用 **volatile** 關鍵字或 [**InterlockedExchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) 函數來修復上述的這個競爭條件，以確保的值在 `iValue` `fValueHasBeenComputed` 設定為 **TRUE** 之前，所有處理器的值都已更新。</span><span class="sxs-lookup"><span data-stu-id="e11e5-142">This race condition above can be repaired by using the **volatile** keyword or the [**InterlockedExchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) function to ensure that the value of `iValue` is updated for all processors before the value of `fValueHasBeenComputed` is set to **TRUE**.</span></span>

<span data-ttu-id="e11e5-143">從 Visual Studio 2005 開始，如果在 **/volatile： ms** 模式中進行編譯，則編譯器會針對 **volatile** 變數使用取得語義，並針對 **volatile** 變數進行寫入作業的發行語義，在 CPU) 支援時 (。</span><span class="sxs-lookup"><span data-stu-id="e11e5-143">Starting Visual Studio 2005, if compiled in **/volatile:ms** mode, the compiler uses acquire semantics for read operations on **volatile** variables and release semantics for write operations on **volatile** variables (when supported by the CPU).</span></span> <span data-ttu-id="e11e5-144">因此，您可以更正此範例，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e11e5-144">Therefore, you can correct the example as follows:</span></span>

``` syntax
volatile int iValue;
volatile BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

<span data-ttu-id="e11e5-145">使用 Visual Studio 2003 時， **volatile** 至 **volatile** 參考會被排序;編譯器不會重新排序 **volatile** 變數存取。</span><span class="sxs-lookup"><span data-stu-id="e11e5-145">With Visual Studio 2003, **volatile** to **volatile** references are ordered; the compiler will not re-order **volatile** variable access.</span></span> <span data-ttu-id="e11e5-146">不過，這些作業可能會由處理器重新排序。</span><span class="sxs-lookup"><span data-stu-id="e11e5-146">However, these operations could be re-ordered by the processor.</span></span> <span data-ttu-id="e11e5-147">因此，您可以更正此範例，如下所示：</span><span class="sxs-lookup"><span data-stu-id="e11e5-147">Therefore, you can correct the example as follows:</span></span>

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          FALSE, FALSE)==FALSE) 
  {
    InterlockedExchange ((LONG*)&iValue, (LONG)ComputeValue());
    InterlockedExchange ((LONG*)&fValueHasBeenComputed, TRUE);
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          TRUE, TRUE)==TRUE) 
  {
    InterlockedExchange((LONG*)piResult, (LONG)iValue);
    return TRUE;
  } 

  else return FALSE;
}
```

## <a name="related-topics"></a><span data-ttu-id="e11e5-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="e11e5-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e11e5-149">重要區段物件</span><span class="sxs-lookup"><span data-stu-id="e11e5-149">Critical Section Objects</span></span>](critical-section-objects.md)
</dt> <dt>

[<span data-ttu-id="e11e5-150">連鎖變數存取</span><span class="sxs-lookup"><span data-stu-id="e11e5-150">Interlocked Variable Access</span></span>](interlocked-variable-access.md)
</dt> <dt>

[<span data-ttu-id="e11e5-151">Wait 函式</span><span class="sxs-lookup"><span data-stu-id="e11e5-151">Wait Functions</span></span>](wait-functions.md)
</dt> </dl>

 

 



