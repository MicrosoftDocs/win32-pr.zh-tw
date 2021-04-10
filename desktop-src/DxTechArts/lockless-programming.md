---
title: Xbox 360 和 Microsoft Windows 的 Lockless 程式設計考量
description: 本文概述在嘗試使用 lockless 的程式設計技術時，應考慮的一些問題。
ms.assetid: 44700352-a791-7ef7-0858-146214b0e3da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23bf8d66cada8aff00735fe6d6ac2d4f1369bc32
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "103933712"
---
# <a name="lockless-programming-considerations-for-xbox-360-and-microsoft-windows"></a><span data-ttu-id="ea66d-103">Xbox 360 和 Microsoft Windows 的 Lockless 程式設計考量</span><span class="sxs-lookup"><span data-stu-id="ea66d-103">Lockless Programming Considerations for Xbox 360 and Microsoft Windows</span></span>

<span data-ttu-id="ea66d-104">Lockless 程式設計是在多個執行緒之間安全共用變更資料的一種方式，而不需要取得和釋放鎖定的成本。</span><span class="sxs-lookup"><span data-stu-id="ea66d-104">Lockless programming is a way to safely share changing data between multiple threads without the cost of acquiring and releasing locks.</span></span> <span data-ttu-id="ea66d-105">這聽起來像是萬靈丹，但是 lockless 程式設計很複雜而且很微妙，有時也不會提供它所保證的優點。</span><span class="sxs-lookup"><span data-stu-id="ea66d-105">This sounds like a panacea, but lockless programming is complex and subtle, and sometimes doesn't give the benefits that it promises.</span></span> <span data-ttu-id="ea66d-106">Lockless 程式設計在 Xbox 360 上特別複雜。</span><span class="sxs-lookup"><span data-stu-id="ea66d-106">Lockless programming is particularly complex on Xbox 360.</span></span>

<span data-ttu-id="ea66d-107">Lockless 程式設計是一種適用于多執行緒程式設計的有效技術，但不應輕量使用。</span><span class="sxs-lookup"><span data-stu-id="ea66d-107">Lockless programming is a valid technique for multithreaded programming, but it should not be used lightly.</span></span> <span data-ttu-id="ea66d-108">在使用它之前，您必須先瞭解複雜性，而且應該謹慎地進行測量，以確定它確實提供您預期的提升。</span><span class="sxs-lookup"><span data-stu-id="ea66d-108">Before using it you must understand the complexities, and you should measure carefully to make sure that it is actually giving you the gains that you expect.</span></span> <span data-ttu-id="ea66d-109">在許多情況下，有更簡單且更快速的解決方案，例如較不頻繁地共用資料，應該改用。</span><span class="sxs-lookup"><span data-stu-id="ea66d-109">In many cases, there are simpler and faster solutions, such as sharing data less frequently, which should be used instead.</span></span>

<span data-ttu-id="ea66d-110">正確且安全地使用 lockless 程式設計需要對硬體和編譯器有很大的瞭解。</span><span class="sxs-lookup"><span data-stu-id="ea66d-110">Using lockless programming correctly and safely requires significant knowledge of both your hardware and your compiler.</span></span> <span data-ttu-id="ea66d-111">本文概述在嘗試使用 lockless 的程式設計技術時，應考慮的一些問題。</span><span class="sxs-lookup"><span data-stu-id="ea66d-111">This article gives an overview of some of the issues to consider when trying to use lockless programming techniques.</span></span>

## <a name="programming-with-locks"></a><span data-ttu-id="ea66d-112">使用鎖定進行程式設計</span><span class="sxs-lookup"><span data-stu-id="ea66d-112">Programming with Locks</span></span>

<span data-ttu-id="ea66d-113">撰寫多執行緒程式碼時，通常必須線上程之間共用資料。</span><span class="sxs-lookup"><span data-stu-id="ea66d-113">When writing multi-threaded code it is often necessary to share data between threads.</span></span> <span data-ttu-id="ea66d-114">如果有多個執行緒同時讀取和寫入共用資料結構，可能會發生記憶體損毀。</span><span class="sxs-lookup"><span data-stu-id="ea66d-114">If multiple threads are simultaneously reading and writing the shared data structures, memory corruption can occur.</span></span> <span data-ttu-id="ea66d-115">解決此問題最簡單的方法是使用鎖定。</span><span class="sxs-lookup"><span data-stu-id="ea66d-115">The simplest way of solving this problem is to use locks.</span></span> <span data-ttu-id="ea66d-116">比方說，如果 ManipulateSharedData 一次只能由一個執行緒執行，則 \_ 可以使用重要區段來保證這一點，如下列程式碼所示：</span><span class="sxs-lookup"><span data-stu-id="ea66d-116">For instance, if ManipulateSharedData should only be executed by one thread at a time, a CRITICAL\_SECTION can be used to guarantee this, as in the following code:</span></span>

``` syntax
// Initialize
CRITICAL_SECTION cs;
InitializeCriticalSection(&cs);

// Use
void ManipulateSharedData()
{
    EnterCriticalSection(&cs);
    // Manipulate stuff...
    LeaveCriticalSection(&cs);
}

// Destroy
DeleteCriticalSection(&cs);
```

<span data-ttu-id="ea66d-117">這段程式碼相當簡單簡單明瞭，很容易就能看出它是正確的。</span><span class="sxs-lookup"><span data-stu-id="ea66d-117">This code is fairly simple and straightforward, and it is easy to tell that it is correct.</span></span> <span data-ttu-id="ea66d-118">不過，使用鎖定進行程式設計有幾個可能的缺點。</span><span class="sxs-lookup"><span data-stu-id="ea66d-118">However, programming with locks comes with several potential disadvantages.</span></span> <span data-ttu-id="ea66d-119">例如，如果兩個執行緒嘗試取得相同的兩個鎖定，但以不同的順序取得它們，您可能會收到鎖死。</span><span class="sxs-lookup"><span data-stu-id="ea66d-119">For example, if two threads try to acquire the same two locks but acquire them in a different order, you may get a deadlock.</span></span> <span data-ttu-id="ea66d-120">如果程式的鎖定時間太長（因為設計不佳）或執行緒已由較高優先順序的執行緒交換，則可能會有很長的時間封鎖其他執行緒。</span><span class="sxs-lookup"><span data-stu-id="ea66d-120">If a program holds a lock for too long—because of poor design or because the thread has been swapped out by a higher priority thread—other threads may be blocked for a long time.</span></span> <span data-ttu-id="ea66d-121">這項風險特別適用于 Xbox 360，因為軟體執行緒是由開發人員指派硬體執行緒，而作業系統不會將它們移至另一個硬體執行緒，即使某個執行緒閒置也一樣。</span><span class="sxs-lookup"><span data-stu-id="ea66d-121">This risk is particularly great on Xbox 360 because the software threads are assigned a hardware thread by the developer, and the operating system won't move them to another hardware thread, even if one is idle.</span></span> <span data-ttu-id="ea66d-122">Xbox 360 也不會對優先順序反轉進行保護，其中高優先順序的執行緒會在等候低優先順序的執行緒釋放鎖定時，在迴圈中旋轉。</span><span class="sxs-lookup"><span data-stu-id="ea66d-122">The Xbox 360 also has no protection against priority inversion, where a high-priority thread spins in a loop while waiting for a low-priority thread to release a lock.</span></span> <span data-ttu-id="ea66d-123">最後，如果延遲程序呼叫或插斷服務常式嘗試取得鎖定，您可能會收到鎖死。</span><span class="sxs-lookup"><span data-stu-id="ea66d-123">Finally, if a deferred procedure call or interrupt service routine tries to acquire a lock, you may get a deadlock.</span></span>

<span data-ttu-id="ea66d-124">儘管有這些問題，同步處理原始物件（例如重要區段）通常是協調多個執行緒的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="ea66d-124">Despite these problems, synchronization primitives, such as critical sections, are generally the best way of coordinating multiple threads.</span></span> <span data-ttu-id="ea66d-125">如果同步處理原始物件的速度太慢，最好的解決方案通常較不常使用。</span><span class="sxs-lookup"><span data-stu-id="ea66d-125">If the synchronization primitives are too slow, the best solution is usually to use them less frequently.</span></span> <span data-ttu-id="ea66d-126">不過，對於可以承受額外複雜性的人，另一個選項是 lockless 程式設計。</span><span class="sxs-lookup"><span data-stu-id="ea66d-126">However, for those who can afford the extra complexity, another option is lockless programming.</span></span>

## <a name="lockless-programming"></a><span data-ttu-id="ea66d-127">Lockless 程式設計</span><span class="sxs-lookup"><span data-stu-id="ea66d-127">Lockless Programming</span></span>

<span data-ttu-id="ea66d-128">顧名思義，Lockless 程式設計是一系列的技術，可安全地操控共用資料，而不需要使用鎖定。</span><span class="sxs-lookup"><span data-stu-id="ea66d-128">Lockless programming, as the name suggests, is a family of techniques for safely manipulating shared data without using locks.</span></span> <span data-ttu-id="ea66d-129">有 lockless 演算法可用於傳遞訊息、共用清單和資料佇列，以及其他工作。</span><span class="sxs-lookup"><span data-stu-id="ea66d-129">There are lockless algorithms available for passing messages, sharing lists and queues of data, and other tasks.</span></span>

<span data-ttu-id="ea66d-130">進行 lockless 程式設計時，您必須處理兩個挑戰：非不可部分完成的作業和重新排列。</span><span class="sxs-lookup"><span data-stu-id="ea66d-130">When doing lockless programming, there are two challenges that you must deal with: non-atomic operations and reordering.</span></span>

## <a name="non-atomic-operations"></a><span data-ttu-id="ea66d-131">不可部分完成的作業</span><span class="sxs-lookup"><span data-stu-id="ea66d-131">Non-Atomic Operations</span></span>

<span data-ttu-id="ea66d-132">不可部分完成的作業是一種不可分割，也就是在執行一半時，其他執行緒保證永遠不會看到作業。</span><span class="sxs-lookup"><span data-stu-id="ea66d-132">An atomic operation is one that is indivisible—one where other threads are guaranteed to never see the operation when it is half done.</span></span> <span data-ttu-id="ea66d-133">不可部分完成的作業對 lockless 程式設計很重要，因為如果沒有這些作業，其他執行緒可能會看到半寫入值，或狀態不一致。</span><span class="sxs-lookup"><span data-stu-id="ea66d-133">Atomic operations are important for lockless programming, because without them, other threads might see half-written values, or otherwise inconsistent state.</span></span>

<span data-ttu-id="ea66d-134">在所有新式處理器上，您可以假設自然對齊原生類型的讀取和寫入是不可部分完成的。</span><span class="sxs-lookup"><span data-stu-id="ea66d-134">On all modern processors, you can assume that reads and writes of naturally aligned native types are atomic.</span></span> <span data-ttu-id="ea66d-135">只要記憶體匯流排的寬度至少與所讀取或寫入的類型相同，CPU 就會在單一總線交易中讀取並寫入這些類型，讓其他執行緒無法以半完成狀態來查看它們。</span><span class="sxs-lookup"><span data-stu-id="ea66d-135">As long as the memory bus is at least as wide as the type being read or written, the CPU reads and writes these types in a single bus transaction, making it impossible for other threads to see them in a half-completed state.</span></span> <span data-ttu-id="ea66d-136">在 x86 和 x64 上，無法保證大於8個位元組的讀取和寫入都是不可部分完成的。</span><span class="sxs-lookup"><span data-stu-id="ea66d-136">On x86 and x64 there, is no guarantee that reads and writes larger than eight bytes are atomic.</span></span> <span data-ttu-id="ea66d-137">這表示以16位元組的方式讀取和寫入串流 SIMD 延伸模組 (SSE) 暫存器和字串作業，可能不是不可部分完成的。</span><span class="sxs-lookup"><span data-stu-id="ea66d-137">This means that 16-byte reads and writes of streaming SIMD extension (SSE) registers, and string operations, might not be atomic.</span></span>

<span data-ttu-id="ea66d-138">未自然對齊的類型（例如，寫入跨四位元組界限的 Dword）的讀取和寫入不保證是不可部分完成的。</span><span class="sxs-lookup"><span data-stu-id="ea66d-138">Reads and writes of types that are not naturally aligned—for instance, writing DWORDs that cross four-byte boundaries—are not guaranteed to be atomic.</span></span> <span data-ttu-id="ea66d-139">CPU 可能必須以多個匯流排交易的形式來進行這些讀取和寫入作業，這可能會讓另一個執行緒在讀取或寫入的中間修改或查看資料。</span><span class="sxs-lookup"><span data-stu-id="ea66d-139">The CPU may have to do these reads and writes as multiple bus transactions, which could allow another thread to modify or see the data in the middle of the read or write.</span></span>

<span data-ttu-id="ea66d-140">複合作業（例如在遞增共用變數時所發生的讀寫寫入順序）不是不可部分完成的。</span><span class="sxs-lookup"><span data-stu-id="ea66d-140">Composite operations, such as the read-modify-write sequence that occurs when you increment a shared variable, are not atomic.</span></span> <span data-ttu-id="ea66d-141">在 Xbox 360 中，這些作業會實作為多個指示 (lwz、addi 和 stw) ，而執行緒可以透過序列交換中途。</span><span class="sxs-lookup"><span data-stu-id="ea66d-141">On Xbox 360, these operations are implemented as multiple instructions (lwz, addi, and stw), and the thread could be swapped out partway through the sequence.</span></span> <span data-ttu-id="ea66d-142">在 x86 和 x64 上，有單一的指令 (inc) 可用來遞增記憶體中的變數。</span><span class="sxs-lookup"><span data-stu-id="ea66d-142">On x86 and x64, there is a single instruction (inc) that can be used to increment a variable in memory.</span></span> <span data-ttu-id="ea66d-143">如果您使用此指令，則在單處理器系統上遞增變數是不可部分完成的，但在多處理器系統上仍然是不可部分完成的。</span><span class="sxs-lookup"><span data-stu-id="ea66d-143">If you use this instruction, incrementing a variable is atomic on single-processor systems, but it is still not atomic on multi-processor systems.</span></span> <span data-ttu-id="ea66d-144">在 x86 和 x64 型的多處理器系統上讓 inc. 不可部分完成，需要使用鎖定前置詞，以防止另一個處理器在 inc 指令的讀取和寫入之間進行讀取-修改-寫入順序。</span><span class="sxs-lookup"><span data-stu-id="ea66d-144">Making inc atomic on x86- and x64-based multi-processor systems requires using the lock prefix, which prevents another processor from doing its own read-modify-write sequence between the read and the write of the inc instruction.</span></span>

<span data-ttu-id="ea66d-145">下列程式碼提供了一些範例：</span><span class="sxs-lookup"><span data-stu-id="ea66d-145">The following code shows some examples:</span></span>

``` syntax
// This write is not atomic because it is not natively aligned.
DWORD* pData = (DWORD*)(pChar + 1);
*pData = 0;

// This is not atomic because it is three separate operations.
++g_globalCounter;

// This write is atomic.
g_alignedGlobal = 0;

// This read is atomic.
DWORD local = g_alignedGlobal;
```

## <a name="guaranteeing-atomicity"></a><span data-ttu-id="ea66d-146">保證不可部分完成性</span><span class="sxs-lookup"><span data-stu-id="ea66d-146">Guaranteeing Atomicity</span></span>

<span data-ttu-id="ea66d-147">您可以透過下列組合，確定您使用的是不可部分完成的作業：</span><span class="sxs-lookup"><span data-stu-id="ea66d-147">You can be sure you are using atomic operations by a combination of the following:</span></span>

-   <span data-ttu-id="ea66d-148">自然不可部分完成的作業</span><span class="sxs-lookup"><span data-stu-id="ea66d-148">Naturally atomic operations</span></span>
-   <span data-ttu-id="ea66d-149">用來包裝複合作業的鎖定</span><span class="sxs-lookup"><span data-stu-id="ea66d-149">Locks to wrap composite operations</span></span>
-   <span data-ttu-id="ea66d-150">執行常用複合作業之不可部分完成版本的作業系統函式</span><span class="sxs-lookup"><span data-stu-id="ea66d-150">Operating system functions that implement atomic versions of popular composite operations</span></span>

<span data-ttu-id="ea66d-151">遞增變數不是不可部分完成的作業，而且如果在多個執行緒上執行，則遞增可能會導致資料損毀。</span><span class="sxs-lookup"><span data-stu-id="ea66d-151">Incrementing a variable is not an atomic operation, and incrementing may lead to data corruption if executed on multiple threads.</span></span>

``` syntax
// This will be atomic.
g_globalCounter = 0;

// This is not atomic and gives undefined behavior
// if executed on multiple threads
++g_globalCounter;
```

<span data-ttu-id="ea66d-152">Win32 隨附一系列的函式，可為數個常見作業提供不可部分完成的讀寫版本。</span><span class="sxs-lookup"><span data-stu-id="ea66d-152">Win32 comes with a family of functions that offer atomic read-modify-write versions of several common operations.</span></span> <span data-ttu-id="ea66d-153">這些是 InterlockedXxx 系列的函式。</span><span class="sxs-lookup"><span data-stu-id="ea66d-153">These are the InterlockedXxx family of functions.</span></span> <span data-ttu-id="ea66d-154">如果共用變數的所有修改都使用這些函數，則修改將會是安全線程。</span><span class="sxs-lookup"><span data-stu-id="ea66d-154">If all modifications of the shared variable use these functions, the modifications will be thread safe.</span></span>

``` syntax
// Incrementing our variable in a safe lockless way.
InterlockedIncrement(&g_globalCounter);
```

## <a name="reordering"></a><span data-ttu-id="ea66d-155">重組</span><span class="sxs-lookup"><span data-stu-id="ea66d-155">Reordering</span></span>

<span data-ttu-id="ea66d-156">重新排列更微妙的問題。</span><span class="sxs-lookup"><span data-stu-id="ea66d-156">A more subtle problem is reordering.</span></span> <span data-ttu-id="ea66d-157">讀取和寫入不一定會按照您在程式碼中撰寫它們的順序來進行，而這可能會導致令人混淆的問題。</span><span class="sxs-lookup"><span data-stu-id="ea66d-157">Reads and writes do not always happen in the order that you have written them in your code, and this can lead to very confusing problems.</span></span> <span data-ttu-id="ea66d-158">在許多多執行緒演算法中，執行緒會寫入一些資料，然後寫入旗標，告知其他執行緒資料已就緒。</span><span class="sxs-lookup"><span data-stu-id="ea66d-158">In many multi-threaded algorithms, a thread writes some data and then writes to a flag that tells other threads that the data is ready.</span></span> <span data-ttu-id="ea66d-159">這就是所謂的寫入發行。</span><span class="sxs-lookup"><span data-stu-id="ea66d-159">This is known as a write-release.</span></span> <span data-ttu-id="ea66d-160">如果寫入已重新排序，其他執行緒可能會看到旗標已設定，然後才可以看到寫入的資料。</span><span class="sxs-lookup"><span data-stu-id="ea66d-160">If the writes are reordered, other threads may see that the flag is set before they can see the written data.</span></span>

<span data-ttu-id="ea66d-161">同樣地，在許多情況下，執行緒會從旗標讀取，然後在旗標指出執行緒已取得共用資料的存取權時，讀取一些共用資料。</span><span class="sxs-lookup"><span data-stu-id="ea66d-161">Similarly, in many cases, a thread reads from a flag and then reads some shared data if the flag says that the thread has acquired access to the shared data.</span></span> <span data-ttu-id="ea66d-162">這稱為「讀取取得」。</span><span class="sxs-lookup"><span data-stu-id="ea66d-162">This is known as a read-acquire.</span></span> <span data-ttu-id="ea66d-163">如果已重新排序讀取，則可能會在旗標之前從共用儲存區讀取資料，而且所見的值可能不是最新狀態。</span><span class="sxs-lookup"><span data-stu-id="ea66d-163">If reads are reordered, then the data may be read from shared storage before the flag, and the values seen might not be up to date.</span></span>

<span data-ttu-id="ea66d-164">編譯器和處理器都可以完成讀取和寫入的重新排列。</span><span class="sxs-lookup"><span data-stu-id="ea66d-164">Reordering of reads and writes can be done both by the compiler and by the processor.</span></span> <span data-ttu-id="ea66d-165">編譯器和處理器已完成這幾年的重新排列，但在單處理器電腦上，這不是問題。</span><span class="sxs-lookup"><span data-stu-id="ea66d-165">Compilers and processors have done this reordering for years, but on single-processor machines it was less of an issue.</span></span> <span data-ttu-id="ea66d-166">這是因為單處理器電腦上的讀取和寫入的 CPU 重新排列，在不屬於設備磁碟機) 一部分的非設備磁碟機程式碼 (中不可見，而且讀取和寫入的編譯器重新排列不太可能會在單處理器電腦上造成問題。</span><span class="sxs-lookup"><span data-stu-id="ea66d-166">This is because CPU rearrangement of reads and writes is invisible on single-processor machines (for non-device driver code that is not part of a device driver), and compiler rearrangement of reads and writes is less likely to cause problems on single-processor machines.</span></span>

<span data-ttu-id="ea66d-167">如果編譯器或 CPU 重新排列下列程式碼中所示的寫入，另一個執行緒可能會看到已設定作用旗標，但仍看到 x 或 y 的舊值。</span><span class="sxs-lookup"><span data-stu-id="ea66d-167">If the compiler or the CPU rearranges the writes shown in the following code, another thread may see that the alive flag is set while still seeing the old values for x or y.</span></span> <span data-ttu-id="ea66d-168">讀取時可能會發生類似的重新排列。</span><span class="sxs-lookup"><span data-stu-id="ea66d-168">Similar rearrangement can happen when reading.</span></span>

<span data-ttu-id="ea66d-169">在此程式碼中，一個執行緒會將新的專案新增至 sprite 陣列：</span><span class="sxs-lookup"><span data-stu-id="ea66d-169">In this code, one thread adds a new entry to the sprite array:</span></span>

``` syntax
// Create a new sprite by writing its position into an empty
// entry and then setting the ‘alive' flag. If ‘alive' is
// written before x or y then errors may occur.
g_sprites[nextSprite].x = x;
g_sprites[nextSprite].y = y;
g_sprites[nextSprite].alive = true;
```

<span data-ttu-id="ea66d-170">在下一個程式碼區塊中，另一個執行緒會從 sprite 陣列讀取：</span><span class="sxs-lookup"><span data-stu-id="ea66d-170">In this next code block, another thread reads from the sprite array:</span></span>

``` syntax
// Draw all sprites. If the reads of x and y are moved ahead of
// the read of ‘alive' then errors may occur.
for( int i = 0; i < numSprites; ++i )
{
    if( g_sprites[nextSprite].alive )
    {
        DrawSprite( g_sprites[nextSprite].x,
                g_sprites[nextSprite].y );
    }
}
```

<span data-ttu-id="ea66d-171">為了讓這個 sprite 系統的安全，我們需要防止編譯器和 CPU 重新排序讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="ea66d-171">To make this sprite system safe, we need to prevent both compiler and CPU reordering of reads and writes.</span></span>

### <a name="understanding-cpu-rearrangement-of-writes"></a><span data-ttu-id="ea66d-172">瞭解寫入的 CPU 重新排列</span><span class="sxs-lookup"><span data-stu-id="ea66d-172">Understanding CPU Rearrangement of Writes</span></span>

<span data-ttu-id="ea66d-173">某些 Cpu 會重新排列寫入，讓其他處理器或裝置以非程式順序對它們進行外部顯示。</span><span class="sxs-lookup"><span data-stu-id="ea66d-173">Some CPUs rearrange writes so that they are externally visible to other processors or devices in non-program order.</span></span> <span data-ttu-id="ea66d-174">單一執行緒的非驅動程式程式碼看不到這項重新排列功能，但是在多執行緒程式碼中可能會造成問題。</span><span class="sxs-lookup"><span data-stu-id="ea66d-174">This rearranging is never visible to single-threaded non-driver code, but it can cause problems in multi-threaded code.</span></span>

### <a name="xbox-360"></a><span data-ttu-id="ea66d-175">Xbox 360</span><span class="sxs-lookup"><span data-stu-id="ea66d-175">Xbox 360</span></span>

<span data-ttu-id="ea66d-176">雖然 Xbox 360 的 CPU 不會重新排序指令，但它會重新排列寫入作業，這會在指示本身之後完成。</span><span class="sxs-lookup"><span data-stu-id="ea66d-176">While the Xbox 360 CPU does not reorder instructions, it does rearrange write operations, which complete after the instructions themselves.</span></span> <span data-ttu-id="ea66d-177">這項寫入重新排列是由 PowerPC 記憶體模型明確允許。</span><span class="sxs-lookup"><span data-stu-id="ea66d-177">This rearranging of writes is specifically allowed by the PowerPC memory model.</span></span>

<span data-ttu-id="ea66d-178">Xbox 360 上的寫入不會直接移至 L2 快取。</span><span class="sxs-lookup"><span data-stu-id="ea66d-178">Writes on Xbox 360 do not go directly to the L2 cache.</span></span> <span data-ttu-id="ea66d-179">相反地，若要改善 L2 快取寫入頻寬，則會經歷存放區佇列，然後再流覽至存放區集合的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ea66d-179">Instead, in order to improve L2 cache write bandwidth, they go through store queues and then to store-gather buffers.</span></span> <span data-ttu-id="ea66d-180">存放區收集緩衝區可在一項作業中，將64位元組區塊寫入 L2 快取中。</span><span class="sxs-lookup"><span data-stu-id="ea66d-180">The store-gather buffers allow 64-byte blocks to be written to the L2 cache in one operation.</span></span> <span data-ttu-id="ea66d-181">有八個存放區收集的緩衝區，可有效率地寫入數個不同的記憶體區域。</span><span class="sxs-lookup"><span data-stu-id="ea66d-181">There are eight store-gather buffers, which allow efficient writing to several different areas of memory.</span></span>

<span data-ttu-id="ea66d-182">存放區收集緩衝區通常會以先進先出的 (FIFO) 順序寫入 L2 快取中。</span><span class="sxs-lookup"><span data-stu-id="ea66d-182">The store-gather buffers are normally written to the L2 cache in first-in-first-out (FIFO) order.</span></span> <span data-ttu-id="ea66d-183">但是，如果寫入的目標快取行不在 L2 快取中，則在從記憶體提取快取行時，可能會延遲寫入。</span><span class="sxs-lookup"><span data-stu-id="ea66d-183">However, if the target cache-line of a write is not in the L2 cache, that write may be delayed while the cache-line is fetched from memory.</span></span>

<span data-ttu-id="ea66d-184">即使以嚴格的 FIFO 順序將商店收集的緩衝區寫入 L2 快取，但這並不保證會依序將個別寫入寫入 L2 快取中。</span><span class="sxs-lookup"><span data-stu-id="ea66d-184">Even when the store-gather buffers are written to the L2 cache in strict FIFO order, this does not guarantee that individual writes are written to the L2 cache in order.</span></span> <span data-ttu-id="ea66d-185">比方說，假設 CPU 寫入至位置0x1000，然後到位置0x2000，再到位置0x1004。</span><span class="sxs-lookup"><span data-stu-id="ea66d-185">For instance, imagine that the CPU writes to location 0x1000, then to location 0x2000, and then to location 0x1004.</span></span> <span data-ttu-id="ea66d-186">第一個寫入會配置存放區收集緩衝區，並將其放在佇列的前方。</span><span class="sxs-lookup"><span data-stu-id="ea66d-186">The first write allocates a store-gather buffer and puts it at the front of the queue.</span></span> <span data-ttu-id="ea66d-187">第二個寫入會配置另一個存放區收集緩衝區，並將它放在佇列中的下一個。</span><span class="sxs-lookup"><span data-stu-id="ea66d-187">The second write allocates another store-gather buffer and puts it next in the queue.</span></span> <span data-ttu-id="ea66d-188">第三個寫入會將其資料新增至第一個存放區收集的緩衝區，這會保留在佇列的前端。</span><span class="sxs-lookup"><span data-stu-id="ea66d-188">The third write adds its data to the first store-gather buffer, which remains at the front of the queue.</span></span> <span data-ttu-id="ea66d-189">因此，第三個寫入最後會在第二次寫入之前進入 L2 快取。</span><span class="sxs-lookup"><span data-stu-id="ea66d-189">Thus, the third write ends up going to the L2 cache before the second write.</span></span>

<span data-ttu-id="ea66d-190">存放區收集緩衝區所造成的重新排列原因基本上是無法預期的，特別是因為核心上的兩個執行緒共用存放區收集的緩衝區，讓存放區集合的配置和清空變得非常不定。</span><span class="sxs-lookup"><span data-stu-id="ea66d-190">Reordering caused by store-gather buffers is fundamentally unpredictable, especially because both threads on a core share the store-gather buffers, making the allocation and emptying of the store-gather buffers highly variable.</span></span>

<span data-ttu-id="ea66d-191">這是如何重新排序寫入的其中一個範例。</span><span class="sxs-lookup"><span data-stu-id="ea66d-191">This is one example of how writes can be reordered.</span></span> <span data-ttu-id="ea66d-192">可能還有其他可能性。</span><span class="sxs-lookup"><span data-stu-id="ea66d-192">There may be other possibilities.</span></span>

### <a name="x86-and-x64"></a><span data-ttu-id="ea66d-193">x86 和 x64</span><span class="sxs-lookup"><span data-stu-id="ea66d-193">x86 and x64</span></span>

<span data-ttu-id="ea66d-194">即使 x86 和 x64 Cpu 會重新排序指令，但它們通常不會重新排列寫入作業相對於其他寫入的順序。</span><span class="sxs-lookup"><span data-stu-id="ea66d-194">Even though x86 and x64 CPUs do reorder instructions, they generally do not reorder write operations relative to other writes.</span></span> <span data-ttu-id="ea66d-195">寫入合併記憶體有一些例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ea66d-195">There are some exceptions for write-combined memory.</span></span> <span data-ttu-id="ea66d-196">此外，字串作業 (MOVS 和 STOS) 和16位元組的 SSE 寫入可在內部重新排列，但是不會重新排序寫入。</span><span class="sxs-lookup"><span data-stu-id="ea66d-196">Additionally, string operations (MOVS and STOS) and 16-byte SSE writes can be internally reordered, but otherwise, writes are not reordered relative to each other.</span></span>

### <a name="understanding-cpu-rearrangement-of-reads"></a><span data-ttu-id="ea66d-197">瞭解讀取的 CPU 重新排列</span><span class="sxs-lookup"><span data-stu-id="ea66d-197">Understanding CPU Rearrangement of Reads</span></span>

<span data-ttu-id="ea66d-198">某些 Cpu 會重新排列讀取，如此它們就能以非程式順序從共用儲存區來進行。</span><span class="sxs-lookup"><span data-stu-id="ea66d-198">Some CPUs rearrange reads so that they effectively come from shared storage in non-program order.</span></span> <span data-ttu-id="ea66d-199">單一執行緒的非驅動程式程式碼看不到這項重新排列，但可能會在多執行緒程式碼中造成問題。</span><span class="sxs-lookup"><span data-stu-id="ea66d-199">This rearranging is never visible to single-threaded non-driver code, but can cause problems in multi-threaded code.</span></span>

### <a name="xbox-360"></a><span data-ttu-id="ea66d-200">Xbox 360</span><span class="sxs-lookup"><span data-stu-id="ea66d-200">Xbox 360</span></span>

<span data-ttu-id="ea66d-201">快取遺漏可能會導致某些讀取延遲，這會有效地導致讀取不按照順序來自共用的記憶體，而這些快取遺漏的時間根本是無法預期的。</span><span class="sxs-lookup"><span data-stu-id="ea66d-201">Cache misses can cause some reads to be delayed, which effectively causes reads to come from shared memory out of order, and the timing of these cache misses is fundamentally unpredictable.</span></span> <span data-ttu-id="ea66d-202">預先提取和分支預測也可能會導致資料從共用記憶體中不按照順序。</span><span class="sxs-lookup"><span data-stu-id="ea66d-202">Prefetching and branch prediction can also cause data to come from shared memory out of order.</span></span> <span data-ttu-id="ea66d-203">這些只是幾個範例，說明如何將讀取重新排序。</span><span class="sxs-lookup"><span data-stu-id="ea66d-203">These are just a few examples of how reads can be reordered.</span></span> <span data-ttu-id="ea66d-204">可能還有其他可能性。</span><span class="sxs-lookup"><span data-stu-id="ea66d-204">There may be other possibilities.</span></span> <span data-ttu-id="ea66d-205">PowerPC 記憶體模型特別允許這項讀取重新排列。</span><span class="sxs-lookup"><span data-stu-id="ea66d-205">This rearranging of reads is specifically allowed by the PowerPC memory model.</span></span>

### <a name="x86-and-x64"></a><span data-ttu-id="ea66d-206">x86 和 x64</span><span class="sxs-lookup"><span data-stu-id="ea66d-206">x86 and x64</span></span>

<span data-ttu-id="ea66d-207">即使 x86 和 x64 Cpu 會重新排序指令，但它們通常不會將讀取作業重新排序為與其他讀取相關。</span><span class="sxs-lookup"><span data-stu-id="ea66d-207">Even though x86 and x64 CPUs do reorder instructions, they generally do not reorder read operations relative to other reads.</span></span> <span data-ttu-id="ea66d-208">字串作業 (MOVS 和 STOS) 和16位元組的 SSE 讀取可以在內部重新排序，但是讀取不會重新排序。</span><span class="sxs-lookup"><span data-stu-id="ea66d-208">String operations (MOVS and STOS) and 16-byte SSE reads can be internally reordered, but otherwise, reads are not reordered relative to each other.</span></span>

### <a name="other-reordering"></a><span data-ttu-id="ea66d-209">其他重新排列</span><span class="sxs-lookup"><span data-stu-id="ea66d-209">Other Reordering</span></span>

<span data-ttu-id="ea66d-210">即使 x86 和 x64 Cpu 不會重新排列寫入相對於其他寫入的順序，或重新排列讀取相對於其他讀取的順序，它們也可以重新排列相對於寫入的讀取順序。</span><span class="sxs-lookup"><span data-stu-id="ea66d-210">Even though x86 and x64 CPUs do not reorder writes relative to other writes, or reorder reads relative to other reads, they can reorder reads relative to writes.</span></span> <span data-ttu-id="ea66d-211">具體來說，如果程式寫入至某個位置，然後從不同的位置讀取，則讀取資料可能會在寫入的資料變成該處之前來自共用記憶體。</span><span class="sxs-lookup"><span data-stu-id="ea66d-211">Specifically, if a program writes to one location followed by reading from a different location, the read data may come from shared memory before the written data makes it there.</span></span> <span data-ttu-id="ea66d-212">重新排列可能會中斷某些演算法，例如 Dekker 的相互排除演算法。</span><span class="sxs-lookup"><span data-stu-id="ea66d-212">This reordering can break some algorithms, such as Dekker’s mutual exclusion algorithms.</span></span> <span data-ttu-id="ea66d-213">在 Dekker 的演算法中，每個執行緒都會設定一個旗標，表示它想要輸入重要區域，然後檢查另一個執行緒的旗標，以查看其他執行緒是否位於關鍵區域或嘗試輸入它。</span><span class="sxs-lookup"><span data-stu-id="ea66d-213">In Dekker's algorithm, each thread sets a flag to indicate that it wants to enter the critical region, and then checks the other thread’s flag to see if the other thread is in the critical region or trying to enter it.</span></span> <span data-ttu-id="ea66d-214">初始程式碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="ea66d-214">The initial code follows.</span></span>

``` syntax
volatile bool f0 = false;
volatile bool f1 = false;

void P0Acquire()
{
    // Indicate intention to enter critical region
    f0 = true;
    // Check for other thread in or entering critical region
    while (f1)
    {
        // Handle contention.
    }
    // critical region
    ...
}


void P1Acquire()
{
    // Indicate intention to enter critical region
    f1 = true;
    // Check for other thread in or entering critical region
    while (f0)
    {
        // Handle contention.
    }
    // critical region
    ...
}
```

<span data-ttu-id="ea66d-215">問題在於，P0Acquire 中的 f1 讀取可以在寫入 f0 使其成為共用儲存體之前讀取共用存放裝置。</span><span class="sxs-lookup"><span data-stu-id="ea66d-215">The problem is that the read of f1 in P0Acquire can read from shared storage before the write to f0 makes it to shared storage.</span></span> <span data-ttu-id="ea66d-216">同時，P1Acquire 中的 f0 讀取可以先從共用存放裝置讀取，然後再寫入至 f1，使其成為共用存放裝置。</span><span class="sxs-lookup"><span data-stu-id="ea66d-216">Meanwhile, the read of f0 in P1Acquire can read from shared storage before the write to f1 makes it to shared storage.</span></span> <span data-ttu-id="ea66d-217">最後的結果就是兩個執行緒都會將其旗標設定為 TRUE，而這兩個執行緒都會將另一個執行緒的旗標視為 FALSE，因此兩者都輸入重要區域。</span><span class="sxs-lookup"><span data-stu-id="ea66d-217">The net effect is that both threads set their flags to TRUE, and both threads see the other thread's flag as being FALSE, so they both enter the critical region.</span></span> <span data-ttu-id="ea66d-218">因此，雖然在 x86 和 x64 型系統上重新排序的問題，在 Xbox 360 上並不常見，但仍有可能發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="ea66d-218">Therefore, while problems with reordering on x86- and x64-based systems are less common than on Xbox 360, they definitely can still happen.</span></span> <span data-ttu-id="ea66d-219">在這些平臺上，Dekker 的演算法將無法運作，而不會有硬體記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="ea66d-219">Dekker’s algorithm will not work without hardware memory barriers on any of these platforms.</span></span>

<span data-ttu-id="ea66d-220">x86 和 x64 Cpu 將不會重新排序先前讀取之前的寫入。</span><span class="sxs-lookup"><span data-stu-id="ea66d-220">x86 and x64 CPUs will not reorder a write ahead of a previous read.</span></span> <span data-ttu-id="ea66d-221">x86 和 x64 Cpu 只會在以不同的位置為目標時，重新排序先前寫入之前的讀取。</span><span class="sxs-lookup"><span data-stu-id="ea66d-221">x86 and x64 CPUs only reorder reads ahead of previous writes if they target different locations.</span></span>

<span data-ttu-id="ea66d-222">PowerPC Cpu 可以在寫入之前重新排列讀取的順序，並可在讀取前重新排序寫入，只要它們是不同的位址即可。</span><span class="sxs-lookup"><span data-stu-id="ea66d-222">PowerPC CPUs can reorder reads ahead of writes, and can reorder writes ahead of reads, as long as they are to different addresses.</span></span>

### <a name="reordering-summary"></a><span data-ttu-id="ea66d-223">重新排列摘要</span><span class="sxs-lookup"><span data-stu-id="ea66d-223">Reordering Summary</span></span>

<span data-ttu-id="ea66d-224">Xbox 360 的 CPU 比起 x86 和 x64 Cpu 更積極地重新排序記憶體作業，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="ea66d-224">The Xbox 360 CPU reorders memory operations much more aggressively than do x86 and x64 CPUs, as shown in the following table.</span></span> <span data-ttu-id="ea66d-225">如需詳細資訊，請參閱處理器檔。</span><span class="sxs-lookup"><span data-stu-id="ea66d-225">For more details, consult the processor documentation.</span></span>



| <span data-ttu-id="ea66d-226">重新排列活動</span><span class="sxs-lookup"><span data-stu-id="ea66d-226">Reordering Activity</span></span>           | <span data-ttu-id="ea66d-227">x86 和 x64</span><span class="sxs-lookup"><span data-stu-id="ea66d-227">x86 and x64</span></span> | <span data-ttu-id="ea66d-228">Xbox 360</span><span class="sxs-lookup"><span data-stu-id="ea66d-228">Xbox 360</span></span> |
|-------------------------------|-------------|----------|
| <span data-ttu-id="ea66d-229">讀取在讀取前移動</span><span class="sxs-lookup"><span data-stu-id="ea66d-229">Reads moving ahead of reads</span></span>   | <span data-ttu-id="ea66d-230">否</span><span class="sxs-lookup"><span data-stu-id="ea66d-230">No</span></span>          | <span data-ttu-id="ea66d-231">是</span><span class="sxs-lookup"><span data-stu-id="ea66d-231">Yes</span></span>      |
| <span data-ttu-id="ea66d-232">寫入在寫入之前移動</span><span class="sxs-lookup"><span data-stu-id="ea66d-232">Writes moving ahead of writes</span></span> | <span data-ttu-id="ea66d-233">否</span><span class="sxs-lookup"><span data-stu-id="ea66d-233">No</span></span>          | <span data-ttu-id="ea66d-234">是</span><span class="sxs-lookup"><span data-stu-id="ea66d-234">Yes</span></span>      |
| <span data-ttu-id="ea66d-235">寫入在讀取前移動</span><span class="sxs-lookup"><span data-stu-id="ea66d-235">Writes moving ahead of reads</span></span>  | <span data-ttu-id="ea66d-236">否</span><span class="sxs-lookup"><span data-stu-id="ea66d-236">No</span></span>          | <span data-ttu-id="ea66d-237">是</span><span class="sxs-lookup"><span data-stu-id="ea66d-237">Yes</span></span>      |
| <span data-ttu-id="ea66d-238">讀取在寫入之前移動</span><span class="sxs-lookup"><span data-stu-id="ea66d-238">Reads moving ahead of writes</span></span>  | <span data-ttu-id="ea66d-239">是</span><span class="sxs-lookup"><span data-stu-id="ea66d-239">Yes</span></span>         | <span data-ttu-id="ea66d-240">是</span><span class="sxs-lookup"><span data-stu-id="ea66d-240">Yes</span></span>      |



 

## <a name="read-acquire-and-write-release-barriers"></a><span data-ttu-id="ea66d-241">Read-Acquire 和 Write-Release 阻礙</span><span class="sxs-lookup"><span data-stu-id="ea66d-241">Read-Acquire and Write-Release Barriers</span></span>

<span data-ttu-id="ea66d-242">用來防止讀取和寫入重新排序的主要結構稱為讀取取得和寫入釋放屏障。</span><span class="sxs-lookup"><span data-stu-id="ea66d-242">The main constructs used to prevent reordering of reads and writes are called read-acquire and write-release barriers.</span></span> <span data-ttu-id="ea66d-243">「讀取取得」是讀取旗標或其他變數以取得資源的擁有權，並結合了屏障以進行重新排序。</span><span class="sxs-lookup"><span data-stu-id="ea66d-243">A read-acquire is a read of a flag or other variable to gain ownership of a resource, coupled with a barrier against reordering.</span></span> <span data-ttu-id="ea66d-244">同樣地，寫入版本是一個旗標或其他變數的寫入，以提供資源的擁有權，並與阻礙重新排序。</span><span class="sxs-lookup"><span data-stu-id="ea66d-244">Similarly, a write-release is a write of a flag or other variable to give away ownership of a resource, coupled with a barrier against reordering.</span></span>

<span data-ttu-id="ea66d-245">Herb Sutter 的正式定義如下：</span><span class="sxs-lookup"><span data-stu-id="ea66d-245">The formal definitions, courtesy of Herb Sutter, are:</span></span>

-   <span data-ttu-id="ea66d-246">讀取器會在依照程式順序追蹤的相同執行緒上執行之前的所有讀取和寫入之前執行。</span><span class="sxs-lookup"><span data-stu-id="ea66d-246">A read-acquire executes before all reads and writes by the same thread that follow it in program order.</span></span>
-   <span data-ttu-id="ea66d-247">寫入發行會在程式順序中的相同執行緒之前的所有讀取和寫入之後執行。</span><span class="sxs-lookup"><span data-stu-id="ea66d-247">A write-release executes after all reads and writes by the same thread that precede it in program order.</span></span>

<span data-ttu-id="ea66d-248">當您的程式碼取得某些記憶體的擁有權時，可能是藉由取得鎖定，或從共用連結清單中提取專案， (沒有鎖定) 的情況下，一律會有相關的讀取-測試旗標或指標，以查看是否已取得記憶體的擁有權。</span><span class="sxs-lookup"><span data-stu-id="ea66d-248">When your code acquires ownership of some memory, either by acquiring a lock or by pulling an item off of a shared linked list (without a lock), there is always a read involved—testing a flag or pointer to see if ownership of the memory has been acquired.</span></span> <span data-ttu-id="ea66d-249">這項讀取可能是 **InterlockedXxx** 作業的一部分，在這種情況下，它牽涉到讀取和寫入，但它是指出是否已取得擁有權的讀取。</span><span class="sxs-lookup"><span data-stu-id="ea66d-249">This read may be part of an **InterlockedXxx** operation, in which case it involves both a read and a write, but it is the read that indicates whether ownership has been gained.</span></span> <span data-ttu-id="ea66d-250">取得記憶體的擁有權之後，通常會從記憶體讀取或寫入值，而且在取得擁有權之後，這些讀取和寫入都必須執行。</span><span class="sxs-lookup"><span data-stu-id="ea66d-250">After ownership of the memory is acquired, values are typically read from or written to that memory, and it is very important that these reads and writes execute after acquiring ownership.</span></span> <span data-ttu-id="ea66d-251">讀取取得關卡可保證這一點。</span><span class="sxs-lookup"><span data-stu-id="ea66d-251">A read-acquire barrier guarantees this.</span></span>

<span data-ttu-id="ea66d-252">當部分記憶體的擁有權釋出（藉由釋放鎖定或將專案推送至共用連結清單）時，一律會產生寫入，以通知其他執行緒現在可使用記憶體。</span><span class="sxs-lookup"><span data-stu-id="ea66d-252">When ownership of some memory is released, either by releasing a lock or by pushing an item on to a shared linked list, there is always a write involved which notifies other threads that the memory is now available to them.</span></span> <span data-ttu-id="ea66d-253">雖然您的程式碼具有記憶體的擁有權，但它可能會對其進行讀取或寫入，因此在釋放擁有權之前，這些讀取和寫入都必須先執行。</span><span class="sxs-lookup"><span data-stu-id="ea66d-253">While your code had ownership of the memory, it probably read from or wrote to it, and it is very important that these reads and writes execute before releasing ownership.</span></span> <span data-ttu-id="ea66d-254">寫入發行關卡可保證這一點。</span><span class="sxs-lookup"><span data-stu-id="ea66d-254">A write-release barrier guarantees this.</span></span>

<span data-ttu-id="ea66d-255">最簡單的方式是將讀取取得和寫入發行的屏障視為單一作業。</span><span class="sxs-lookup"><span data-stu-id="ea66d-255">It is simplest to think of read-acquire and write-release barriers as single operations.</span></span> <span data-ttu-id="ea66d-256">不過，有時必須從兩個部分進行建立：讀取或寫入，以及不允許讀取或寫入在其上移動的屏障。</span><span class="sxs-lookup"><span data-stu-id="ea66d-256">However, they sometimes have to be constructed from two parts: a read or write and a barrier that does not allow reads or writes to move across it.</span></span> <span data-ttu-id="ea66d-257">在此情況下，屏障的位置非常重要。</span><span class="sxs-lookup"><span data-stu-id="ea66d-257">In this case, the placement of the barrier is critical.</span></span> <span data-ttu-id="ea66d-258">針對讀取取得關卡，旗標的讀取會先出現，然後是屏障，然後讀取和寫入共用資料。</span><span class="sxs-lookup"><span data-stu-id="ea66d-258">For a read-acquire barrier, the read of the flag comes first, then the barrier, and then the reads and writes of the shared data.</span></span> <span data-ttu-id="ea66d-259">針對寫入發行關卡，共用資料的讀取和寫入會先出現，然後是屏障，然後寫入旗標。</span><span class="sxs-lookup"><span data-stu-id="ea66d-259">For a write-release barrier the reads and writes of the shared data come first, then the barrier, and then the write of the flag.</span></span>

``` syntax
// Read that acquires the data.
if( g_flag )
{
    // Guarantee that the read of the flag executes before
    // all reads and writes that follow in program order.
    BarrierOfSomeSort();

    // Now we can read and write the shared data.
    int localVariable = sharedData.y;
    sharedData.x = 0;

    // Guarantee that the write to the flag executes after all
    // reads and writes that precede it in program order.
    BarrierOfSomeSort();
    
    // Write that releases the data.
    g_flag = false;
}
```

<span data-ttu-id="ea66d-260">讀取取得和寫入發行之間的唯一差異在於記憶體屏障的位置。</span><span class="sxs-lookup"><span data-stu-id="ea66d-260">The only difference between a read-acquire and a write-release is the location of the memory barrier.</span></span> <span data-ttu-id="ea66d-261">讀取取得會在鎖定作業之後具有關卡，而寫入版本則具有關卡。</span><span class="sxs-lookup"><span data-stu-id="ea66d-261">A read-acquire has the barrier after the lock operation, and a write-release has the barrier before.</span></span> <span data-ttu-id="ea66d-262">在這兩種情況下，屏障都介於鎖定記憶體的參考與鎖定的參考之間。</span><span class="sxs-lookup"><span data-stu-id="ea66d-262">In both cases the barrier is in-between the references to the locked memory and the references to the lock.</span></span>

<span data-ttu-id="ea66d-263">若要瞭解在取得和釋出資料時，為什麼需要阻礙，最好是最好的 (以及最準確的) 將這些阻礙視為可保證與共享記憶體的同步處理，而不是其他處理器。</span><span class="sxs-lookup"><span data-stu-id="ea66d-263">To understand why barriers are needed both when acquiring and when releasing data, it is best (and most accurate) to think of these barriers as guaranteeing synchronization with shared memory, not with other processors.</span></span> <span data-ttu-id="ea66d-264">如果有一個處理器使用寫入發行將資料結構釋出至共用記憶體，而另一個處理器使用讀取取得來從共用記憶體存取該資料結構，則程式碼會正常運作。</span><span class="sxs-lookup"><span data-stu-id="ea66d-264">If one processor uses a write-release to release a data structure to shared memory, and another processor uses a read-acquire to gain access to that data structure from shared memory, the code will then work properly.</span></span> <span data-ttu-id="ea66d-265">如果其中一種處理器未使用適當的關卡，資料共用可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="ea66d-265">If either processor doesn't use the appropriate barrier, the data sharing may fail.</span></span>

<span data-ttu-id="ea66d-266">使用適當的關卡來防止編譯器和您的平臺重新調整 CPU 的關鍵。</span><span class="sxs-lookup"><span data-stu-id="ea66d-266">Using the right barrier to prevent compiler and CPU reordering for your platform is critical.</span></span>

<span data-ttu-id="ea66d-267">使用作業系統所提供的同步處理原始物件的優點之一，就是它們都包含適當的記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="ea66d-267">One of the advantages of using the synchronization primitives provided by the operating system is that all of them include the appropriate memory barriers.</span></span>

## <a name="preventing-compiler-reordering"></a><span data-ttu-id="ea66d-268">防止編譯器重新排列</span><span class="sxs-lookup"><span data-stu-id="ea66d-268">Preventing Compiler Reordering</span></span>

<span data-ttu-id="ea66d-269">編譯器的工作是將您的程式碼積極地優化，以便改善效能。</span><span class="sxs-lookup"><span data-stu-id="ea66d-269">A compiler's job is to aggressively optimize your code in order to improve performance.</span></span> <span data-ttu-id="ea66d-270">這包括重新排列指示的位置，以及不會變更行為的位置。</span><span class="sxs-lookup"><span data-stu-id="ea66d-270">This includes rearranging instructions wherever it is helpful and wherever it will not change behavior.</span></span> <span data-ttu-id="ea66d-271">因為 c + + 標準絕對不會提及多執行緒，而且因為編譯器不知道哪些程式碼必須是安全線程，所以編譯器會假設您的程式碼在決定可安全重排所以的情況下，會有單一執行緒。</span><span class="sxs-lookup"><span data-stu-id="ea66d-271">Because the C++ Standard never mentions multithreading, and because the compiler doesn't know what code needs to be thread-safe, the compiler assumes that your code is single-threaded when deciding what rearrangements it can safely do.</span></span> <span data-ttu-id="ea66d-272">因此，當不允許編譯器重新排序讀取和寫入時，您需要告訴編譯器。</span><span class="sxs-lookup"><span data-stu-id="ea66d-272">Therefore, you need to tell the compiler when it is not allowed to reorder reads and writes.</span></span>

<span data-ttu-id="ea66d-273">使用 Visual C++ 您可以使用編譯器內建 [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx)，以防止編譯器重新排列。</span><span class="sxs-lookup"><span data-stu-id="ea66d-273">With Visual C++ you can prevent compiler reordering by using the compiler intrinsic [**\_ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx).</span></span> <span data-ttu-id="ea66d-274">當您在程式碼中插入 **\_ ReadWriteBarrier** 時，編譯器不會在其上移動讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="ea66d-274">Where you insert **\_ReadWriteBarrier** into your code, the compiler will not move reads and writes across it.</span></span>

``` syntax
#if _MSC_VER < 1400
    // With VC++ 2003 you need to declare _ReadWriteBarrier
    extern "C" void _ReadWriteBarrier();
#else
    // With VC++ 2005 you can get the declaration from intrin.h
#include <intrin.h>
#endif
// Tell the compiler that this is an intrinsic, not a function.
#pragma intrinsic(_ReadWriteBarrier)

// Create a new sprite by filling in a previously empty entry.
g_sprites[nextSprite].x = x;
g_sprites[nextSprite].y = y;
// Write-release, barrier followed by write.
// Guarantee that the compiler leaves the write to the flag
// after all reads and writes that precede it in program order.
_ReadWriteBarrier();
g_sprites[nextSprite].alive = true;
```

<span data-ttu-id="ea66d-275">在下列程式碼中，另一個執行緒會從 sprite 陣列讀取：</span><span class="sxs-lookup"><span data-stu-id="ea66d-275">In the following code, another thread reads from the sprite array:</span></span>

``` syntax
// Draw all sprites.
for( int i = 0; i < numSprites; ++i )
{

    // Read-acquire, read followed by barrier.
    if( g_sprites[nextSprite].alive )
    {
    
        // Guarantee that the compiler leaves the read of the flag
        // before all reads and writes that follow in program order.
        _ReadWriteBarrier();
        DrawSprite( g_sprites[nextSprite].x,
                g_sprites[nextSprite].y );
    }
}
```

<span data-ttu-id="ea66d-276">請務必瞭解， [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx)不會插入任何額外的指示，也不會防止 CPU 重新排列讀取和寫入，它只會防止編譯器重新排列讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="ea66d-276">It is important to understand that [**\_ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx) does not insert any additional instructions, and it does not prevent the CPU from rearranging reads and writes—it only prevents the compiler from rearranging them.</span></span> <span data-ttu-id="ea66d-277">因此，當您在 x86 和 x64 (上實行寫入發行屏障時， **\_ ReadWriteBarrier** 便已足夠，因為 x86 和 x64 不會重新排列寫入的順序，而一般寫入足以釋出鎖定) ，但在大部分的情況下，也必須防止 CPU 重新排序讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="ea66d-277">Thus, **\_ReadWriteBarrier** is sufficient when you implement a write-release barrier on x86 and x64 (because x86 and x64 do not reorder writes, and a normal write is sufficient for releasing a lock), but in most other cases, it is also necessary to prevent the CPU from reordering reads and writes.</span></span>

<span data-ttu-id="ea66d-278">當您寫入至無法快取的寫入組合記憶體時，也可以使用 [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx) ，以防止寫入重新排序。</span><span class="sxs-lookup"><span data-stu-id="ea66d-278">You can also use [**\_ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx) when you write to non-cacheable write-combined memory to prevent reordering of writes.</span></span> <span data-ttu-id="ea66d-279">在此情況下， **\_ ReadWriteBarrier** 藉由保證寫入會以處理器的慣用線性順序進行，有助於改善效能。</span><span class="sxs-lookup"><span data-stu-id="ea66d-279">In this case **\_ReadWriteBarrier** helps to improve performance, by guaranteeing that the writes happen in the processor's preferred linear order.</span></span>

<span data-ttu-id="ea66d-280">您也可以使用 [**\_ ReadBarrier**](https://msdn.microsoft.com/library/z055s48f(v=VS.80).aspx)和 [**\_ WriteBarrier**](https://msdn.microsoft.com/library/65tt87y8(v=VS.80).aspx)內建函式來更精確地控制編譯器重新排列。</span><span class="sxs-lookup"><span data-stu-id="ea66d-280">It is also possible to use the [**\_ReadBarrier**](https://msdn.microsoft.com/library/z055s48f(v=VS.80).aspx) and [**\_WriteBarrier**](https://msdn.microsoft.com/library/65tt87y8(v=VS.80).aspx) intrinsics for more precise control of compiler reordering.</span></span> <span data-ttu-id="ea66d-281">編譯器不會跨 **\_ ReadBarrier** 移動讀取，且不會在 **\_ WriteBarrier** 之間移動寫入。</span><span class="sxs-lookup"><span data-stu-id="ea66d-281">The compiler will not move reads across a **\_ReadBarrier**, and it will not move writes across a **\_WriteBarrier**.</span></span>

## <a name="preventing-cpu-reordering"></a><span data-ttu-id="ea66d-282">防止 CPU 重新排序</span><span class="sxs-lookup"><span data-stu-id="ea66d-282">Preventing CPU Reordering</span></span>

<span data-ttu-id="ea66d-283">重新調整 CPU 比編譯器重新排列更為微妙。</span><span class="sxs-lookup"><span data-stu-id="ea66d-283">CPU reordering is more subtle than compiler reordering.</span></span> <span data-ttu-id="ea66d-284">您看不到直接發生的情況，只是看到 inexplicable 的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ea66d-284">You can't ever see it happen directly, you just see inexplicable bugs.</span></span> <span data-ttu-id="ea66d-285">為了防止 CPU 重新排序讀取和寫入，您必須在某些處理器上使用記憶體屏障指令。</span><span class="sxs-lookup"><span data-stu-id="ea66d-285">In order to prevent CPU reordering of reads and writes you need to use memory barrier instructions, on some processors.</span></span> <span data-ttu-id="ea66d-286">Xbox 360 和 Windows 上的記憶體屏障指令的所有用途名稱都是 [**system.threading.thread.memorybarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier)。</span><span class="sxs-lookup"><span data-stu-id="ea66d-286">The all-purpose name for a memory barrier instruction, on Xbox 360 and on Windows, is [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier).</span></span> <span data-ttu-id="ea66d-287">此宏會針對每個平臺適當地執行。</span><span class="sxs-lookup"><span data-stu-id="ea66d-287">This macro is implemented appropriately for each platform.</span></span>

<span data-ttu-id="ea66d-288">在 Xbox 360 上， [**system.threading.thread.memorybarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier)定義為 **lwsync** (輕量同步) ，也可透過 **\_ \_ lwsync** 內建（定義于 ppcintrinsics 中）來使用。</span><span class="sxs-lookup"><span data-stu-id="ea66d-288">On Xbox 360, [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) is defined as **lwsync** (lightweight sync), also available through the **\_\_lwsync** intrinsic, which is defined in ppcintrinsics.h.</span></span> <span data-ttu-id="ea66d-289">**\_ \_ lwsync** 也可作為編譯器記憶體屏障，以防止編譯器重新排列讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="ea66d-289">**\_\_lwsync** also serves as a compiler memory barrier, preventing rearranging of reads and writes by the compiler.</span></span>

<span data-ttu-id="ea66d-290">**Lwsync** 指令是 Xbox 360 上的記憶體屏障，可同步處理一個處理器核心與 L2 快取。</span><span class="sxs-lookup"><span data-stu-id="ea66d-290">The **lwsync** instruction is a memory barrier on Xbox 360 that synchronizes one processor core with the L2 cache.</span></span> <span data-ttu-id="ea66d-291">它可確保在 **lwsync** 之前的所有寫入都先將其寫入至 L2 快取，然後再執行任何寫入。</span><span class="sxs-lookup"><span data-stu-id="ea66d-291">It guarantees that all writes before **lwsync** make it to the L2 cache before any writes that follow.</span></span> <span data-ttu-id="ea66d-292">它也可保證遵循 **lwsync** 的任何讀取，都不會從 L2 取得比先前讀取更舊的資料。</span><span class="sxs-lookup"><span data-stu-id="ea66d-292">It also guarantees that any reads that follow **lwsync** don't get older data from L2 than previous reads.</span></span> <span data-ttu-id="ea66d-293">它不會防止的一種重新排列類型，就是在寫入至不同位址之前讀取的移動。</span><span class="sxs-lookup"><span data-stu-id="ea66d-293">The one type of reordering that it does not prevent is a read moving ahead of a write to a different address.</span></span> <span data-ttu-id="ea66d-294">因此， **lwsync** 會強制執行符合 x86 和 x64 處理器上預設記憶體順序的記憶體順序。</span><span class="sxs-lookup"><span data-stu-id="ea66d-294">Thus, **lwsync** enforces memory ordering that matches the default memory ordering on x86 and x64 processors.</span></span> <span data-ttu-id="ea66d-295">若要取得完整的記憶體順序，需要較昂貴的同步指令 (也稱為重量級同步) ，但在大部分情況下，則不需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="ea66d-295">To get full memory ordering requires the more expensive sync instruction (also known as heavyweight sync), but in most cases, this is not required.</span></span> <span data-ttu-id="ea66d-296">下表顯示 Xbox 360 上的記憶體重新排列選項。</span><span class="sxs-lookup"><span data-stu-id="ea66d-296">The memory reordering options on Xbox 360 are shown in the following table.</span></span>



| <span data-ttu-id="ea66d-297">重新排列 Xbox 360</span><span class="sxs-lookup"><span data-stu-id="ea66d-297">Xbox 360 Reordering</span></span>           | <span data-ttu-id="ea66d-298">無同步處理</span><span class="sxs-lookup"><span data-stu-id="ea66d-298">No sync</span></span> | <span data-ttu-id="ea66d-299">lwsync</span><span class="sxs-lookup"><span data-stu-id="ea66d-299">lwsync</span></span> | <span data-ttu-id="ea66d-300">sync</span><span class="sxs-lookup"><span data-stu-id="ea66d-300">sync</span></span> |
|-------------------------------|---------|--------|------|
| <span data-ttu-id="ea66d-301">讀取在讀取前移動</span><span class="sxs-lookup"><span data-stu-id="ea66d-301">Reads moving ahead of reads</span></span>   | <span data-ttu-id="ea66d-302">是</span><span class="sxs-lookup"><span data-stu-id="ea66d-302">Yes</span></span>     | <span data-ttu-id="ea66d-303">否</span><span class="sxs-lookup"><span data-stu-id="ea66d-303">No</span></span>     | <span data-ttu-id="ea66d-304">否</span><span class="sxs-lookup"><span data-stu-id="ea66d-304">No</span></span>   |
| <span data-ttu-id="ea66d-305">寫入在寫入之前移動</span><span class="sxs-lookup"><span data-stu-id="ea66d-305">Writes moving ahead of writes</span></span> | <span data-ttu-id="ea66d-306">是</span><span class="sxs-lookup"><span data-stu-id="ea66d-306">Yes</span></span>     | <span data-ttu-id="ea66d-307">否</span><span class="sxs-lookup"><span data-stu-id="ea66d-307">No</span></span>     | <span data-ttu-id="ea66d-308">否</span><span class="sxs-lookup"><span data-stu-id="ea66d-308">No</span></span>   |
| <span data-ttu-id="ea66d-309">寫入在讀取前移動</span><span class="sxs-lookup"><span data-stu-id="ea66d-309">Writes moving ahead of reads</span></span>  | <span data-ttu-id="ea66d-310">是</span><span class="sxs-lookup"><span data-stu-id="ea66d-310">Yes</span></span>     | <span data-ttu-id="ea66d-311">否</span><span class="sxs-lookup"><span data-stu-id="ea66d-311">No</span></span>     | <span data-ttu-id="ea66d-312">否</span><span class="sxs-lookup"><span data-stu-id="ea66d-312">No</span></span>   |
| <span data-ttu-id="ea66d-313">讀取在寫入之前移動</span><span class="sxs-lookup"><span data-stu-id="ea66d-313">Reads moving ahead of writes</span></span>  | <span data-ttu-id="ea66d-314">是</span><span class="sxs-lookup"><span data-stu-id="ea66d-314">Yes</span></span>     | <span data-ttu-id="ea66d-315">是</span><span class="sxs-lookup"><span data-stu-id="ea66d-315">Yes</span></span>    | <span data-ttu-id="ea66d-316">否</span><span class="sxs-lookup"><span data-stu-id="ea66d-316">No</span></span>   |



 

<span data-ttu-id="ea66d-317">PowerPC 也有同步處理指示 **isync** 和 **eieio** (，可用來控制重新排列至快取-抑制記憶體) 。</span><span class="sxs-lookup"><span data-stu-id="ea66d-317">PowerPC also has the synchronization instructions **isync** and **eieio** (which is used to control reordering to caching-inhibited memory).</span></span> <span data-ttu-id="ea66d-318">一般同步處理用途不需要這些同步處理指示。</span><span class="sxs-lookup"><span data-stu-id="ea66d-318">These synchronization instructions should not be needed for normal synchronization purposes.</span></span>

<span data-ttu-id="ea66d-319">在 Windows 上， [**system.threading.thread.memorybarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) 是在 Winnt 中定義，並根據您要針對 x86 或 x64 編譯而提供不同的記憶體屏障指令。</span><span class="sxs-lookup"><span data-stu-id="ea66d-319">On Windows, [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) is defined in Winnt.h and gives you a different memory barrier instruction depending on whether you are compiling for x86 or x64.</span></span> <span data-ttu-id="ea66d-320">記憶體關卡指令可做為完整的關卡，防止所有屏障的讀取和寫入重新排列。</span><span class="sxs-lookup"><span data-stu-id="ea66d-320">The memory barrier instruction serves as a full barrier, preventing all reordering of reads and writes across the barrier.</span></span> <span data-ttu-id="ea66d-321">因此，Windows 上的 **system.threading.thread.memorybarrier** 提供比 Xbox 360 更強的重新排序保證。</span><span class="sxs-lookup"><span data-stu-id="ea66d-321">Thus, **MemoryBarrier** on Windows gives a stronger reordering guarantee than it does on Xbox 360.</span></span>

<span data-ttu-id="ea66d-322">在 Xbox 360 以及許多其他 Cpu 上，都有一種額外的方式可以防止 CPU 進行讀取重新排列。</span><span class="sxs-lookup"><span data-stu-id="ea66d-322">On Xbox 360, and on many other CPUs, there is one additional way that read-reordering by the CPU can be prevented.</span></span> <span data-ttu-id="ea66d-323">如果您讀取指標，然後使用該指標載入其他資料，CPU 可保證讀取指標的次數不會比讀取指標還舊。</span><span class="sxs-lookup"><span data-stu-id="ea66d-323">If you read a pointer and then use that pointer to load other data, the CPU guarantees that the reads off of the pointer are not older than the read of the pointer.</span></span> <span data-ttu-id="ea66d-324">如果您的鎖定旗標是指標，且共用資料的所有讀取都不是指標，則可以省略 [**system.threading.thread.memorybarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) ，以節省適度的效能。</span><span class="sxs-lookup"><span data-stu-id="ea66d-324">If your lock flag is a pointer and if all reads of shared data are off of the pointer, the [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) can be omitted, for a modest performance savings.</span></span>

``` syntax
Data* localPointer = g_sharedPointer;
if( localPointer )
{
    // No import barrier is needed--all reads off of localPointer
    // are guaranteed to not be reordered past the read of
    // localPointer.
    int localVariable = localPointer->y;
    // A memory barrier is needed to stop the read of g_global
    // from being speculatively moved ahead of the read of
    // g_sharedPointer.
    int localVariable2 = g_global;
}
```

<span data-ttu-id="ea66d-325">[**System.threading.thread.memorybarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier)指令只會防止將讀取和寫入重新排序為可快取的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ea66d-325">The [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) instruction only prevents reordering of reads and writes to cacheable memory.</span></span> <span data-ttu-id="ea66d-326">如果您將記憶體配置為頁面 \_ NOCACHE 或頁面 \_ WRITECOMBINE，則裝置驅動程式作者和遊戲開發人員在 Xbox 360 上的常見技術， **system.threading.thread.memorybarrier** 不會影響此記憶體的存取。</span><span class="sxs-lookup"><span data-stu-id="ea66d-326">If you allocate memory as PAGE\_NOCACHE or PAGE\_WRITECOMBINE, a common technique for device driver authors and for game developers on Xbox 360, **MemoryBarrier** has no effect on accesses to this memory.</span></span> <span data-ttu-id="ea66d-327">大部分的開發人員都不需要同步處理無法快取的記憶體。</span><span class="sxs-lookup"><span data-stu-id="ea66d-327">Most developers don't need synchronization of non-cacheable memory.</span></span> <span data-ttu-id="ea66d-328">這已超出本文的範圍。</span><span class="sxs-lookup"><span data-stu-id="ea66d-328">That is beyond the scope of this article.</span></span>

## <a name="interlocked-functions-and-cpu-reordering"></a><span data-ttu-id="ea66d-329">連鎖函數和 CPU 重新排列</span><span class="sxs-lookup"><span data-stu-id="ea66d-329">Interlocked Functions and CPU Reordering</span></span>

<span data-ttu-id="ea66d-330">有時會使用其中一個 **InterlockedXxx** 函數來取得或釋放資源的讀取或寫入。</span><span class="sxs-lookup"><span data-stu-id="ea66d-330">Sometimes the read or write that acquires or releases a resource is done using one of the **InterlockedXxx** functions.</span></span> <span data-ttu-id="ea66d-331">在 Windows 中，這可簡化專案;因為在 Windows 上， **InterlockedXxx** 函式都是完全記憶體的阻礙。</span><span class="sxs-lookup"><span data-stu-id="ea66d-331">On Windows, this simplifies things; because on Windows, the **InterlockedXxx** functions are all full-memory barriers.</span></span> <span data-ttu-id="ea66d-332">它們在前後都有一個 CPU 記憶體屏障，這表示它們本身是完整的讀取或寫入發行關卡。</span><span class="sxs-lookup"><span data-stu-id="ea66d-332">They effectively have a CPU memory barrier both before and after them, which means that they are a full read-acquire or write-release barrier all by themselves.</span></span>

<span data-ttu-id="ea66d-333">在 Xbox 360 上， **InterlockedXxx** 函數不會包含 CPU 記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="ea66d-333">On Xbox 360, the **InterlockedXxx** functions do not contain CPU memory barriers.</span></span> <span data-ttu-id="ea66d-334">它們可防止編譯器重新排序讀取和寫入，而不會重新排列 CPU。</span><span class="sxs-lookup"><span data-stu-id="ea66d-334">They prevent compiler reordering of reads and writes but not CPU reordering.</span></span> <span data-ttu-id="ea66d-335">因此，在大部分情況下，在 Xbox 360 上使用 **InterlockedXxx** 函式時，您應該在其前面或後面加上 **\_ \_ lwsync**，使其成為讀取或寫入發行關卡。</span><span class="sxs-lookup"><span data-stu-id="ea66d-335">Therefore, in most cases when using **InterlockedXxx** functions on Xbox 360, you should precede or follow them with an **\_\_lwsync**, to make them a read-acquire or write-release barrier.</span></span> <span data-ttu-id="ea66d-336">為了方便起見，而且更容易閱讀，有許多 **InterlockedXxx** 函式的 **取得** 和 **發行** 版。</span><span class="sxs-lookup"><span data-stu-id="ea66d-336">For convenience and for easier readability, there are **Acquire** and **Release** versions of many of the **InterlockedXxx** functions.</span></span> <span data-ttu-id="ea66d-337">這些都有內建的記憶體屏障。</span><span class="sxs-lookup"><span data-stu-id="ea66d-337">These come with a built-in memory barrier.</span></span> <span data-ttu-id="ea66d-338">例如， [**InterlockedIncrementAcquire**](/previous-versions/windows/desktop/legacy/ms683618(v=vs.85))會執行連鎖的遞增，後面接著 **\_ \_ lwsync** 的記憶體屏障，以提供完整的讀取取得功能。</span><span class="sxs-lookup"><span data-stu-id="ea66d-338">For instance, [**InterlockedIncrementAcquire**](/previous-versions/windows/desktop/legacy/ms683618(v=vs.85)) does an interlocked increment followed by an **\_\_lwsync** memory barrier to give the full read-acquire functionality.</span></span>

<span data-ttu-id="ea66d-339">建議您使用 **InterlockedXxx** 函式的 **取得** 和 **發行** 版 (大多數都可在 Windows 上使用，但不會對效能造成負面影響) 讓您的意圖更加明顯，並讓您更輕鬆地在正確的位置取得記憶體關卡指令。</span><span class="sxs-lookup"><span data-stu-id="ea66d-339">It is recommended that you use the **Acquire** and **Release** versions of the **InterlockedXxx** functions (most of which are available on Windows as well, with no performance penalty) to make your intent more obvious and to make it easier to get the memory barrier instructions in the correct place.</span></span> <span data-ttu-id="ea66d-340">在 Xbox 360 上使用 **InterlockedXxx** 時，若沒有記憶體屏障，則應謹慎檢查，因為這通常是錯誤。</span><span class="sxs-lookup"><span data-stu-id="ea66d-340">Any use of **InterlockedXxx** on Xbox 360 without a memory barrier should be examined very carefully, because it is often a bug.</span></span>

<span data-ttu-id="ea66d-341">這個範例會示範一個執行緒如何使用 **InterlockedXxxSList** 函式的 **取得** 和 **發行** 版，將工作或其他資料傳遞到另一個執行緒。</span><span class="sxs-lookup"><span data-stu-id="ea66d-341">This sample demonstrates how one thread can pass tasks or other data to another thread using the **Acquire** and **Release** versions of the **InterlockedXxxSList** functions.</span></span> <span data-ttu-id="ea66d-342">**InterlockedXxxSList** 函式是一系列的函式，用來維護共用的單向連結清單，而不需要鎖定。</span><span class="sxs-lookup"><span data-stu-id="ea66d-342">The **InterlockedXxxSList** functions are a family of functions for maintaining a shared singly linked list without a lock.</span></span> <span data-ttu-id="ea66d-343">請注意，這些函式的 **取得** 和 **版本** 變體在 windows 上無法使用，但這些函式的一般版本是 windows 上的完整記憶體屏障。</span><span class="sxs-lookup"><span data-stu-id="ea66d-343">Note that **Acquire** and **Release** variants of these functions are not available on Windows, but the regular versions of these functions are a full memory barrier on Windows.</span></span>

``` syntax
// Declarations for the Task class go here.

// Add a new task to the list using lockless programming.
void AddTask( DWORD ID, DWORD data )
{
    Task* newItem = new Task( ID, data );
    InterlockedPushEntrySListRelease( g_taskList, newItem );
}

// Remove a task from the list, using lockless programming.
// This will return NULL if there are no items in the list.
Task* GetTask()
{
    Task* result = (Task*)
        InterlockedPopEntrySListAcquire( g_taskList );
    return result;
}
```

## <a name="volatile-variables-and-reordering"></a><span data-ttu-id="ea66d-344">Volatile 變數和重新排列</span><span class="sxs-lookup"><span data-stu-id="ea66d-344">Volatile Variables and Reordering</span></span>

<span data-ttu-id="ea66d-345">C + + 標準指出無法快取 volatile 變數的讀取、volatile 寫入無法延遲，而且無法將變動性讀取和寫入移到彼此的之後。</span><span class="sxs-lookup"><span data-stu-id="ea66d-345">The C++ Standard says that reads of volatile variables cannot be cached, volatile writes cannot be delayed, and volatile reads and writes cannot be moved past each other.</span></span> <span data-ttu-id="ea66d-346">這就足以與硬體裝置進行通訊，這是 c + + 標準中 volatile 關鍵字的用途。</span><span class="sxs-lookup"><span data-stu-id="ea66d-346">This is sufficient for communicating with hardware devices, which is the purpose of the volatile keyword in the C++ Standard.</span></span>

<span data-ttu-id="ea66d-347">但是，標準的保證並不足以針對多執行緒使用 volatile。</span><span class="sxs-lookup"><span data-stu-id="ea66d-347">However, the guarantees of the standard are not sufficient for using volatile for multi-threading.</span></span> <span data-ttu-id="ea66d-348">C + + 標準不會阻止編譯器重新排列相對於 volatile 讀取和寫入的非暫時性讀取和寫入，且不會顯示任何關於防止重新調整 CPU 的資訊。</span><span class="sxs-lookup"><span data-stu-id="ea66d-348">The C++ Standard does not stop the compiler from reordering non-volatile reads and writes relative to volatile reads and writes, and it says nothing about preventing CPU reordering.</span></span>

<span data-ttu-id="ea66d-349">Visual C++ 2005 超越標準 c + +，以針對 volatile 變數存取定義多執行緒易懂的語法。</span><span class="sxs-lookup"><span data-stu-id="ea66d-349">Visual C++ 2005 goes beyond standard C++ to define multi-threading-friendly semantics for volatile variable access.</span></span> <span data-ttu-id="ea66d-350">從 Visual C++ 2005 開始，會將 volatile 變數的讀取定義為具有讀取取得的語法，而 volatile 變數的寫入則定義為具有寫入發行語義。</span><span class="sxs-lookup"><span data-stu-id="ea66d-350">Starting with Visual C++ 2005, reads from volatile variables are defined to have read-acquire semantics, and writes to volatile variables are defined to have write-release semantics.</span></span> <span data-ttu-id="ea66d-351">這表示編譯器將不會重新排列任何超出它們的讀取和寫入，而在 Windows 上，則會確保 CPU 不會執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="ea66d-351">This means that the compiler will not rearrange any reads and writes past them, and on Windows it will ensure that the CPU does not do so either.</span></span>

<span data-ttu-id="ea66d-352">請務必瞭解這些新的保證只適用于 Visual C++ 2005 和未來版本的 Visual C++。</span><span class="sxs-lookup"><span data-stu-id="ea66d-352">It is important to understand that these new guarantees only apply to Visual C++ 2005 and future versions of Visual C++.</span></span> <span data-ttu-id="ea66d-353">其他廠商的編譯器通常會執行不同的語法，而不會有 Visual C++ 2005 的額外保證。</span><span class="sxs-lookup"><span data-stu-id="ea66d-353">Compilers from other vendors will generally implement different semantics, without the extra guarantees of Visual C++ 2005.</span></span> <span data-ttu-id="ea66d-354">此外，在 Xbox 360 上，編譯器不會插入任何指示，以防止 CPU 重新排序讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="ea66d-354">Also, on Xbox 360, the compiler does not insert any instructions to prevent the CPU from reordering reads and writes.</span></span>

## <a name="example-of-a-lock-free-data-pipe"></a><span data-ttu-id="ea66d-355">Lock-Free 資料管道的範例</span><span class="sxs-lookup"><span data-stu-id="ea66d-355">Example of a Lock-Free Data Pipe</span></span>

<span data-ttu-id="ea66d-356">管道是一種結構，可讓一個或多個執行緒寫入資料，然後由其他執行緒讀取。</span><span class="sxs-lookup"><span data-stu-id="ea66d-356">A pipe is a construct that lets one or more threads write data that is then read by other threads.</span></span> <span data-ttu-id="ea66d-357">管道的 lockless 版本可以是一種簡潔且有效率的方式，將工作從執行緒傳遞給執行緒。</span><span class="sxs-lookup"><span data-stu-id="ea66d-357">A lockless version of a pipe can be an elegant and efficient way to pass work from thread to thread.</span></span> <span data-ttu-id="ea66d-358">DirectX SDK 提供 **LockFreePipe**，這是可在 DXUTLockFreePipe 中使用的單一讀取器、單一寫入器 lockless 管道。</span><span class="sxs-lookup"><span data-stu-id="ea66d-358">The DirectX SDK supplies **LockFreePipe**, a single-reader, single-writer lockless pipe that is available in DXUTLockFreePipe.h.</span></span> <span data-ttu-id="ea66d-359">相同的 **LockFreePipe** 可在 AtgLockFreePipe 的 Xbox 360 SDK 中使用。</span><span class="sxs-lookup"><span data-stu-id="ea66d-359">The same **LockFreePipe** is available in the Xbox 360 SDK in AtgLockFreePipe.h.</span></span>

<span data-ttu-id="ea66d-360">當兩個執行緒有生產者/取用者關聯性時，可以使用 **LockFreePipe** 。</span><span class="sxs-lookup"><span data-stu-id="ea66d-360">**LockFreePipe** can be used when two threads have a producer/consumer relationship.</span></span> <span data-ttu-id="ea66d-361">生產者執行緒可以將資料寫入管道，讓取用者執行緒在日後進行處理，而不會遭到封鎖。</span><span class="sxs-lookup"><span data-stu-id="ea66d-361">The producer thread can write data to the pipe for the consumer thread to process at a later date, without ever blocking.</span></span> <span data-ttu-id="ea66d-362">如果管道填滿，寫入會失敗，而生產者執行緒必須稍後再試一次，但只有在產生生產者執行緒時，才會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="ea66d-362">If the pipe fills up, writes fail, and the producer thread will have to try again later, but this would only happen if the producer thread is ahead.</span></span> <span data-ttu-id="ea66d-363">如果管道清空，讀取會失敗，而取用者執行緒將必須稍後再試一次，但只有在沒有工作可供取用者執行緒執行時，才會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="ea66d-363">If the pipe empties, reads fail, and the consumer thread will have to try again later, but this would only happen if there is no work for the consumer thread to do.</span></span> <span data-ttu-id="ea66d-364">如果兩個執行緒都是妥善平衡的，且管道夠大，管道可讓它們順暢地傳遞資料，而不會有延遲或區塊。</span><span class="sxs-lookup"><span data-stu-id="ea66d-364">If the two threads are well-balanced, and the pipe is big enough, the pipe lets them smoothly pass data along with no delays or blocks.</span></span>

## <a name="xbox-360-performance"></a><span data-ttu-id="ea66d-365">Xbox 360 效能</span><span class="sxs-lookup"><span data-stu-id="ea66d-365">Xbox 360 Performance</span></span>

<span data-ttu-id="ea66d-366">Xbox 360 上的同步處理指示和函式的效能，會隨著其他程式碼的執行而有所不同。</span><span class="sxs-lookup"><span data-stu-id="ea66d-366">The performance of synchronization instructions and functions on Xbox 360 will vary depending on what other code is running.</span></span> <span data-ttu-id="ea66d-367">如果另一個執行緒目前擁有鎖定，取得鎖定將需要更長的時間。</span><span class="sxs-lookup"><span data-stu-id="ea66d-367">Acquiring locks will take much longer if another thread currently owns the lock.</span></span> <span data-ttu-id="ea66d-368">如果有其他執行緒寫入相同的快取行， [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement)和重要區段作業將需要更長的時間。</span><span class="sxs-lookup"><span data-stu-id="ea66d-368">[**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) and critical section operations will take much longer if other threads are writing to the same cache line.</span></span> <span data-ttu-id="ea66d-369">存放區佇列的內容也會影響效能。</span><span class="sxs-lookup"><span data-stu-id="ea66d-369">The contents of the store queues can also affect performance.</span></span> <span data-ttu-id="ea66d-370">因此，所有這些數位只是近似值，從非常簡單的測試產生：</span><span class="sxs-lookup"><span data-stu-id="ea66d-370">Therefore, all of these numbers are just approximations, generated from very simple tests:</span></span>

-   <span data-ttu-id="ea66d-371">**lwsync** 已測量為採用33-48 週期。</span><span class="sxs-lookup"><span data-stu-id="ea66d-371">**lwsync** was measured as taking 33-48 cycles.</span></span>
-   <span data-ttu-id="ea66d-372">[**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) 已測量為採用225-260 週期。</span><span class="sxs-lookup"><span data-stu-id="ea66d-372">[**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) was measured as taking 225-260 cycles.</span></span>
-   <span data-ttu-id="ea66d-373">取得或釋出重要區段的測量是大約大約345週期。</span><span class="sxs-lookup"><span data-stu-id="ea66d-373">Acquiring or releasing a critical section was measured as taking about 345 cycles.</span></span>
-   <span data-ttu-id="ea66d-374">取得或釋放 mutex 的測量是大約大約2350迴圈。</span><span class="sxs-lookup"><span data-stu-id="ea66d-374">Acquiring or releasing a mutex was measured as taking about 2350 cycles.</span></span>

## <a name="windows-performance"></a><span data-ttu-id="ea66d-375">Windows 效能</span><span class="sxs-lookup"><span data-stu-id="ea66d-375">Windows Performance</span></span>

<span data-ttu-id="ea66d-376">Windows 上的同步處理指示和函式的效能，會隨著處理器類型和設定，以及其他哪些程式碼正在執行而有很大的差異。</span><span class="sxs-lookup"><span data-stu-id="ea66d-376">The performance of synchronization instructions and functions on Windows vary widely depending on the processor type and configuration, and on what other code is running.</span></span> <span data-ttu-id="ea66d-377">多核心和多通訊端系統通常需要較長的時間來執行同步處理指示，而如果另一個執行緒目前擁有鎖定，取得鎖定的時間會更長。</span><span class="sxs-lookup"><span data-stu-id="ea66d-377">Multi-core and multi-socket systems often take longer to execute synchronizing instructions, and acquiring locks take much longer if another thread currently owns the lock.</span></span>

<span data-ttu-id="ea66d-378">但是，即使是從非常簡單的測試產生的一些測量也很有説明：</span><span class="sxs-lookup"><span data-stu-id="ea66d-378">However, even some measurements generated from very simple tests are helpful:</span></span>

-   <span data-ttu-id="ea66d-379">[**System.threading.thread.memorybarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) 已測量為採用20-90 週期。</span><span class="sxs-lookup"><span data-stu-id="ea66d-379">[**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) was measured as taking 20-90 cycles.</span></span>
-   <span data-ttu-id="ea66d-380">[**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) 已測量為採用36-90 週期。</span><span class="sxs-lookup"><span data-stu-id="ea66d-380">[**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) was measured as taking 36-90 cycles.</span></span>
-   <span data-ttu-id="ea66d-381">取得或釋放重要區段的測量是採用40-100 週期。</span><span class="sxs-lookup"><span data-stu-id="ea66d-381">Acquiring or releasing a critical section was measured as taking 40-100 cycles.</span></span>
-   <span data-ttu-id="ea66d-382">取得或釋放 mutex 的測量是大約大約750-2500 迴圈。</span><span class="sxs-lookup"><span data-stu-id="ea66d-382">Acquiring or releasing a mutex was measured as taking about 750-2500 cycles.</span></span>

<span data-ttu-id="ea66d-383">這些測試是在 Windows XP 上的各種不同處理器上完成。</span><span class="sxs-lookup"><span data-stu-id="ea66d-383">These tests were done on Windows XP on a range of different processors.</span></span> <span data-ttu-id="ea66d-384">在單處理器電腦上會有較短的時間，而在多處理器電腦上則是較長的時間。</span><span class="sxs-lookup"><span data-stu-id="ea66d-384">The short times were on a single-processor machine, and the longer times were on a multi-processor machine.</span></span>

<span data-ttu-id="ea66d-385">雖然取得和釋放鎖定的成本比使用 lockless 程式設計更高，但更能更頻繁地共用資料，進而避免成本。</span><span class="sxs-lookup"><span data-stu-id="ea66d-385">While acquiring and releasing locks is more expensive than using lockless programming, it is even better to share data less frequently, thus avoiding the cost altogether.</span></span>

## <a name="performance-thoughts"></a><span data-ttu-id="ea66d-386">效能想法</span><span class="sxs-lookup"><span data-stu-id="ea66d-386">Performance Thoughts</span></span>

<span data-ttu-id="ea66d-387">取得或釋出重要區段包含記憶體屏障、 **InterlockedXxx** 作業，以及一些額外檢查來處理遞迴，以及切換回 mutex （如有必要）。</span><span class="sxs-lookup"><span data-stu-id="ea66d-387">Acquiring or releasing a critical section consists of a memory barrier, an **InterlockedXxx** operation, and some extra checking to handle recursion and to fall back to a mutex, if necessary.</span></span> <span data-ttu-id="ea66d-388">您應該要謹慎地實行您自己的重要區段，因為在等候鎖定的迴圈中旋轉（等候鎖定是免費的），而不會回到 mutex，所以會浪費大量的效能。</span><span class="sxs-lookup"><span data-stu-id="ea66d-388">You should be wary of implementing your own critical section, because spinning in a loop waiting for a lock to be free, without falling back to a mutex, can waste considerable performance.</span></span> <span data-ttu-id="ea66d-389">對於嚴重爭用但未長期保留的重要區段，您應該考慮使用 [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) ，如此一來，當您嘗試取得重要區段時，作業系統會在等候重要區段的時候旋轉一段時間，而不是立即延遲至 mutex。</span><span class="sxs-lookup"><span data-stu-id="ea66d-389">For critical sections that are heavily contended but not held for long, you should consider using [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) so that the operating system will spin for a while waiting for the critical section to be available rather than immediately deferring to a mutex if the critical section is owned when you try to acquire it.</span></span> <span data-ttu-id="ea66d-390">為了識別可受益于微調計數的重要區段，您必須測量一般等候特定鎖定的長度。</span><span class="sxs-lookup"><span data-stu-id="ea66d-390">In order to identify critical sections that can benefit from a spin count, it is necessary to measure the length of the typical wait for a particular lock.</span></span>

<span data-ttu-id="ea66d-391">如果共用堆積用於記憶體配置（預設行為），則每個記憶體配置和免費都需要取得鎖定。</span><span class="sxs-lookup"><span data-stu-id="ea66d-391">If a shared heap is used for memory allocations—the default behavior—every memory allocation and free involves acquiring a lock.</span></span> <span data-ttu-id="ea66d-392">當執行緒的數目和配置數量增加時，效能層級會關閉，且最終會開始減少。</span><span class="sxs-lookup"><span data-stu-id="ea66d-392">As the number of threads and the number of allocations increases, performance levels off, and eventually starts to decrease.</span></span> <span data-ttu-id="ea66d-393">使用每個執行緒堆積或減少配置數目，可避免此鎖定瓶頸。</span><span class="sxs-lookup"><span data-stu-id="ea66d-393">Using per-thread heaps, or reducing the number of allocations, can avoid this locking bottleneck.</span></span>

<span data-ttu-id="ea66d-394">如果有一個執行緒正在產生資料，而另一個執行緒正在使用資料，它們可能會經常共用資料。</span><span class="sxs-lookup"><span data-stu-id="ea66d-394">If one thread is generating data and another thread is consuming data, they may end up sharing data frequently.</span></span> <span data-ttu-id="ea66d-395">如果有一個執行緒正在載入資源，而另一個執行緒正在轉譯場景，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="ea66d-395">This can happen if one thread is loading resources and another thread is rendering the scene.</span></span> <span data-ttu-id="ea66d-396">如果轉譯執行緒參考每個繪製呼叫上的共用資料，則鎖定的額外負荷會很高。</span><span class="sxs-lookup"><span data-stu-id="ea66d-396">If the rendering thread references the shared data on every draw call, the locking overhead will be high.</span></span> <span data-ttu-id="ea66d-397">如果每個執行緒都有私用資料結構，然後在每個框架或更短的時間內進行同步處理，則可以實現更好的效能</span><span class="sxs-lookup"><span data-stu-id="ea66d-397">Much better performance can be realized if each thread has private data structures which are then synchronized once per frame or less.</span></span>

<span data-ttu-id="ea66d-398">Lockless 演算法不保證會比使用鎖定的演算法更快。</span><span class="sxs-lookup"><span data-stu-id="ea66d-398">Lockless algorithms are not guaranteed to be faster than algorithms that use locks.</span></span> <span data-ttu-id="ea66d-399">您應該先查看鎖定是否真的會造成問題，然後再嘗試避免它們，而且您應該測量以查看您的 lockless 程式碼是否真的能改善效能。</span><span class="sxs-lookup"><span data-stu-id="ea66d-399">You should check to see if locks are actually causing you problems before trying to avoid them, and you should measure to see if your lockless code actually improves performance.</span></span>

## <a name="platform-differences-summary"></a><span data-ttu-id="ea66d-400">平臺差異摘要</span><span class="sxs-lookup"><span data-stu-id="ea66d-400">Platform Differences Summary</span></span>

-   <span data-ttu-id="ea66d-401">**InterlockedXxx** 函式會防止在 Windows 上重新排列 CPU 的讀取/寫入，而不是 Xbox 360。</span><span class="sxs-lookup"><span data-stu-id="ea66d-401">**InterlockedXxx** functions prevent CPU read/write reordering on Windows, but not on Xbox 360.</span></span>
-   <span data-ttu-id="ea66d-402">使用 Visual Studio c + + 2005 讀取和寫入 volatile 變數，可避免在 Windows 上重新排列 CPU 的讀取/寫入，但是在 Xbox 360 上，它只會防止編譯器的讀取/寫入重新排列。</span><span class="sxs-lookup"><span data-stu-id="ea66d-402">Reading and writing of volatile variables using Visual Studio C++ 2005 prevents CPU read/write reordering on Windows, but on Xbox 360, it only prevents compiler read/write reordering.</span></span>
-   <span data-ttu-id="ea66d-403">寫入會在 Xbox 360 上重新排序，但不會在 x86 或 x64 上重新排序。</span><span class="sxs-lookup"><span data-stu-id="ea66d-403">Writes are reordered on Xbox 360, but not on x86 or x64.</span></span>
-   <span data-ttu-id="ea66d-404">讀取會在 Xbox 360 上重新排序，但是在 x86 或 x64 上，它們只會重新排列相對於寫入的順序，而且只有在讀取和寫入目標不同位置時才會重新排序。</span><span class="sxs-lookup"><span data-stu-id="ea66d-404">Reads are reordered on Xbox 360, but on x86 or x64 they are only reordered relative to writes, and only if the reads and writes target different locations.</span></span>

## <a name="recommendations"></a><span data-ttu-id="ea66d-405">建議</span><span class="sxs-lookup"><span data-stu-id="ea66d-405">Recommendations</span></span>

-   <span data-ttu-id="ea66d-406">盡可能使用鎖定，因為它們比較容易使用。</span><span class="sxs-lookup"><span data-stu-id="ea66d-406">Use locks when possible because they are easier to use correctly.</span></span>
-   <span data-ttu-id="ea66d-407">避免鎖定太頻繁，因此鎖定成本不會變得很明顯。</span><span class="sxs-lookup"><span data-stu-id="ea66d-407">Avoid locking too frequently, so that locking costs do not become significant.</span></span>
-   <span data-ttu-id="ea66d-408">避免將鎖定保留太久，以避免長時間停止。</span><span class="sxs-lookup"><span data-stu-id="ea66d-408">Avoid holding locks for too long, in order to avoid long stalls.</span></span>
-   <span data-ttu-id="ea66d-409">適當時，請使用 lockless 程式設計，但請確定這些增益會證明複雜度。</span><span class="sxs-lookup"><span data-stu-id="ea66d-409">Use lockless programming when appropriate, but be sure that the gains justify the complexity.</span></span>
-   <span data-ttu-id="ea66d-410">在禁止其他鎖定的情況下使用 lockless 程式設計或旋轉鎖定，例如在延遲程序呼叫和一般程式碼之間共用資料時。</span><span class="sxs-lookup"><span data-stu-id="ea66d-410">Use lockless programming or spin locks in situations where other locks are prohibited, such as when sharing data between deferred procedure calls and normal code.</span></span>
-   <span data-ttu-id="ea66d-411">只使用已證明正確的標準 lockless 程式設計演算法。</span><span class="sxs-lookup"><span data-stu-id="ea66d-411">Only use standard lockless programming algorithms that have been proven to be correct.</span></span>
-   <span data-ttu-id="ea66d-412">進行 lockless 程式設計時，請務必視需要使用 volatile 旗標變數和記憶體關卡指令。</span><span class="sxs-lookup"><span data-stu-id="ea66d-412">When doing lockless programming, be sure to use volatile flag variables and memory barrier instructions as needed.</span></span>
-   <span data-ttu-id="ea66d-413">在 Xbox 360 上使用 **InterlockedXxx** 時，請使用 **取得** 和 **釋放** 變異。</span><span class="sxs-lookup"><span data-stu-id="ea66d-413">When using **InterlockedXxx** on Xbox 360, use the **Acquire** and **Release** variants.</span></span>

## <a name="references"></a><span data-ttu-id="ea66d-414">參考資料</span><span class="sxs-lookup"><span data-stu-id="ea66d-414">References</span></span>

-   <span data-ttu-id="ea66d-415">MSDN Library。</span><span class="sxs-lookup"><span data-stu-id="ea66d-415">MSDN Library.</span></span> <span data-ttu-id="ea66d-416">「[**volatile (c + +)**](https://msdn.microsoft.com/library/12a04hfd(v=VS.71).aspx)」。</span><span class="sxs-lookup"><span data-stu-id="ea66d-416">"[**volatile (C++)**](https://msdn.microsoft.com/library/12a04hfd(v=VS.71).aspx)."</span></span> <span data-ttu-id="ea66d-417">C + + 語言參考。</span><span class="sxs-lookup"><span data-stu-id="ea66d-417">C++ Language Reference.</span></span>
-   <span data-ttu-id="ea66d-418">Vance Morrison。</span><span class="sxs-lookup"><span data-stu-id="ea66d-418">Vance Morrison.</span></span> <span data-ttu-id="ea66d-419">「[瞭解多執行緒應用程式中 Low-Lock 技術的影響](/archive/msdn-magazine/2005/october/understanding-low-lock-techniques-in-multithreaded-apps)」。</span><span class="sxs-lookup"><span data-stu-id="ea66d-419">"[Understand the Impact of Low-Lock Techniques in Multithreaded Apps](/archive/msdn-magazine/2005/october/understanding-low-lock-techniques-in-multithreaded-apps)."</span></span> <span data-ttu-id="ea66d-420">2005年10月的 MSDN 雜誌。</span><span class="sxs-lookup"><span data-stu-id="ea66d-420">MSDN Magazine, October 2005.</span></span>
-   <span data-ttu-id="ea66d-421">Lyons，Michael。</span><span class="sxs-lookup"><span data-stu-id="ea66d-421">Lyons, Michael.</span></span> <span data-ttu-id="ea66d-422">「[PowerPC 儲存體模型與 AIX 程式設計](https://www-128.ibm.com/developerworks/eserver/articles/powerpc.mdl)」。</span><span class="sxs-lookup"><span data-stu-id="ea66d-422">"[PowerPC Storage Model and AIX Programming](https://www-128.ibm.com/developerworks/eserver/articles/powerpc.mdl)."</span></span> <span data-ttu-id="ea66d-423">IBM developerWorks，16 11 月2005日。</span><span class="sxs-lookup"><span data-stu-id="ea66d-423">IBM developerWorks, 16 Nov 2005.</span></span>
-   <span data-ttu-id="ea66d-424">McKenney，Paul E. "[新式微處理器中的記憶體順序，第二部分](https://www.linuxjournal.com/article/8212)。"</span><span class="sxs-lookup"><span data-stu-id="ea66d-424">McKenney, Paul E. "[Memory Ordering in Modern Microprocessors, Part II](https://www.linuxjournal.com/article/8212)."</span></span> <span data-ttu-id="ea66d-425">Linux 日誌，2005年9月。</span><span class="sxs-lookup"><span data-stu-id="ea66d-425">Linux Journal, September 2005.</span></span> <span data-ttu-id="ea66d-426">\[本文有一些 x86 詳細資料。\]</span><span class="sxs-lookup"><span data-stu-id="ea66d-426">\[This article has some x86 details.\]</span></span>
-   <span data-ttu-id="ea66d-427">Intel Corporation。</span><span class="sxs-lookup"><span data-stu-id="ea66d-427">Intel Corporation.</span></span> <span data-ttu-id="ea66d-428">「[Intel®64架構記憶體順序](https://www.cs.cmu.edu/~410-f10/doc/Intel_Reordering_318147.pdf)」。</span><span class="sxs-lookup"><span data-stu-id="ea66d-428">"[Intel® 64 Architecture Memory Ordering](https://www.cs.cmu.edu/~410-f10/doc/Intel_Reordering_318147.pdf)."</span></span> <span data-ttu-id="ea66d-429">2007年8月。</span><span class="sxs-lookup"><span data-stu-id="ea66d-429">August 2007.</span></span> <span data-ttu-id="ea66d-430">\[適用于 IA-32 和 Intel 64 處理器。\]</span><span class="sxs-lookup"><span data-stu-id="ea66d-430">\[Applies to both IA-32 and Intel 64 processors.\]</span></span>
-   <span data-ttu-id="ea66d-431">Niebler、Eric。</span><span class="sxs-lookup"><span data-stu-id="ea66d-431">Niebler, Eric.</span></span> <span data-ttu-id="ea66d-432">「[旅程報表： c + + 中線程](https://www.artima.com/cppsource/threads_meeting.html)的臨機操作會議」。</span><span class="sxs-lookup"><span data-stu-id="ea66d-432">"[Trip Report: Ad-Hoc Meeting on Threads in C++](https://www.artima.com/cppsource/threads_meeting.html)."</span></span> <span data-ttu-id="ea66d-433">C + + 來源，2006 10 月17日。</span><span class="sxs-lookup"><span data-stu-id="ea66d-433">The C++ Source, 17 Oct 2006.</span></span>
-   <span data-ttu-id="ea66d-434">Hart，Thomas E. 2006。</span><span class="sxs-lookup"><span data-stu-id="ea66d-434">Hart, Thomas E. 2006.</span></span> <span data-ttu-id="ea66d-435">「[快速進行 Lockless 同步處理：記憶體回收的效能影響](https://www.cs.toronto.edu/~tomhart/papers/hart_ipdps06.pdf)」。</span><span class="sxs-lookup"><span data-stu-id="ea66d-435">"[Making Lockless Synchronization Fast: Performance Implications of Memory Reclamation](https://www.cs.toronto.edu/~tomhart/papers/hart_ipdps06.pdf)."</span></span> <span data-ttu-id="ea66d-436">2006國際平行和分散式處理 Symposium (IPDPS 2006) 、Rhodes 島、希臘、4月2006。</span><span class="sxs-lookup"><span data-stu-id="ea66d-436">Proceedings of the 2006 International Parallel and Distributed Processing Symposium (IPDPS 2006), Rhodes Island, Greece, April 2006.</span></span>

 

 