---
description: Windows 包含下列新的程式設計專案以進行同步處理。
ms.assetid: 16cd98d2-adc5-4a14-ad39-a0c5b4cc00cc
title: 同步處理的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702ba10126d9c0eeeb85462195680b074918584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192931"
---
# <a name="whats-new-in-synchronization"></a><span data-ttu-id="1e565-103">同步處理的新功能</span><span class="sxs-lookup"><span data-stu-id="1e565-103">What's New in Synchronization</span></span>

<span data-ttu-id="1e565-104">Windows 包含下列新的程式設計專案以進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="1e565-104">Windows includes the following new programming elements for synchronization.</span></span>

## <a name="windows-8"></a><span data-ttu-id="1e565-105">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1e565-105">Windows 8</span></span>

### <a name="new-functions"></a><span data-ttu-id="1e565-106">新函式</span><span class="sxs-lookup"><span data-stu-id="1e565-106">New Functions</span></span>

<dl> <dt>

[<span data-ttu-id="1e565-107">**DeleteSynchronizationBarrier**</span><span class="sxs-lookup"><span data-stu-id="1e565-107">**DeleteSynchronizationBarrier**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="1e565-108">刪除同步處理屏障。</span><span class="sxs-lookup"><span data-stu-id="1e565-108">Deletes a synchronization barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="1e565-109">**EnterSynchronizationBarrier**</span><span class="sxs-lookup"><span data-stu-id="1e565-109">**EnterSynchronizationBarrier**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="1e565-110">讓呼叫執行緒在同步處理屏障等候，直到執行緒的最大數目進入關卡為止。</span><span class="sxs-lookup"><span data-stu-id="1e565-110">Causes the calling thread to wait at a synchronization barrier until the maximum number of threads have entered the barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="1e565-111">**GetOverlappedResultEx**</span><span class="sxs-lookup"><span data-stu-id="1e565-111">**GetOverlappedResultEx**</span></span>](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex)
</dt> <dd>

<span data-ttu-id="1e565-112">在指定的逾時間隔內，針對指定的檔案、具名管道或通訊裝置，抓取重迭作業的結果。</span><span class="sxs-lookup"><span data-stu-id="1e565-112">Retrieves the results of an overlapped operation on the specified file, named pipe, or communications device within the specified time-out interval.</span></span> <span data-ttu-id="1e565-113">呼叫執行緒可以執行可提供警示等候。</span><span class="sxs-lookup"><span data-stu-id="1e565-113">The calling thread can perform an alertable wait.</span></span>

</dd> <dt>

[<span data-ttu-id="1e565-114">**InitializeSynchronizationBarrier**</span><span class="sxs-lookup"><span data-stu-id="1e565-114">**InitializeSynchronizationBarrier**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="1e565-115">指定新同步處理屏障的執行緒數目上限和微調計數。</span><span class="sxs-lookup"><span data-stu-id="1e565-115">Specifies the maximum number of threads and spin count for a new synchronization barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="1e565-116">**WaitOnAddress**</span><span class="sxs-lookup"><span data-stu-id="1e565-116">**WaitOnAddress**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress)
</dt> <dd>

<span data-ttu-id="1e565-117">等候指定之位址的值變更。</span><span class="sxs-lookup"><span data-stu-id="1e565-117">Waits for the value at the specified address to change.</span></span>

</dd> <dt>

[<span data-ttu-id="1e565-118">**WakeByAddressAll**</span><span class="sxs-lookup"><span data-stu-id="1e565-118">**WakeByAddressAll**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall)
</dt> <dd>

<span data-ttu-id="1e565-119">喚醒等候位址值變更的所有線程。</span><span class="sxs-lookup"><span data-stu-id="1e565-119">Wakes all threads that are waiting for the value of an address to change.</span></span>

</dd> <dt>

[<span data-ttu-id="1e565-120">**WakeByAddressSingle**</span><span class="sxs-lookup"><span data-stu-id="1e565-120">**WakeByAddressSingle**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle)
</dt> <dd>

<span data-ttu-id="1e565-121">喚醒一個等候位址值變更的執行緒。</span><span class="sxs-lookup"><span data-stu-id="1e565-121">Wakes one thread that is waiting for the value of an address to change.</span></span>

</dd> </dl>

### <a name="new-interlocked-functions"></a><span data-ttu-id="1e565-122">新的連鎖函數</span><span class="sxs-lookup"><span data-stu-id="1e565-122">New Interlocked Functions</span></span>

<dl> <dt>

<span data-ttu-id="1e565-123">[**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-123">[**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-124">在指定的 **LONG** 值上執行不可部分完成的加法運算。</span><span class="sxs-lookup"><span data-stu-id="1e565-124">Performs an atomic addition operation on the specified **LONG** values.</span></span> <span data-ttu-id="1e565-125">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-125">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-126">[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-126">[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-127">在指定的 **LONGLONG** 值上執行不可部分完成的加法運算。</span><span class="sxs-lookup"><span data-stu-id="1e565-127">Performs an atomic addition operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="1e565-128">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-128">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-129">[**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-129">[**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-130">在指定的 **LONG** 值上執行不可部分完成的運算。</span><span class="sxs-lookup"><span data-stu-id="1e565-130">Performs an atomic AND operation on the specified **LONG** values.</span></span> <span data-ttu-id="1e565-131">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-131">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-132">[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-132">[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-133">在指定的 **char** 值上執行不可部分完成的運算。</span><span class="sxs-lookup"><span data-stu-id="1e565-133">Performs an atomic AND operation on the specified **char** values.</span></span> <span data-ttu-id="1e565-134">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-134">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-135">[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-135">[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-136">對指定的 **短** 值執行不可部分完成的運算。</span><span class="sxs-lookup"><span data-stu-id="1e565-136">Performs an atomic AND operation on the specified **SHORT** values.</span></span> <span data-ttu-id="1e565-137">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-137">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-138">[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-138">[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-139">在指定的 **LONGLONG** 值上執行不可部分完成的運算。</span><span class="sxs-lookup"><span data-stu-id="1e565-139">Performs an atomic AND operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="1e565-140">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-140">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-141">[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-141">[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-142">測試指定之 **LONG64** 值的指定位，並加以補充。</span><span class="sxs-lookup"><span data-stu-id="1e565-142">Tests the specified bit of the specified **LONG64** value and complements it.</span></span> <span data-ttu-id="1e565-143">此作業是不可部分完成的。</span><span class="sxs-lookup"><span data-stu-id="1e565-143">The operation is atomic.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-144">[**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-144">[**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-145">測試指定之 **LONG** 值的指定位並將它設定為0。</span><span class="sxs-lookup"><span data-stu-id="1e565-145">Tests the specified bit of the specified **LONG** value and sets it to 0.</span></span> <span data-ttu-id="1e565-146">作業是不可部分完成的，而且會使用取得記憶體順序語義來執行。</span><span class="sxs-lookup"><span data-stu-id="1e565-146">The operation is atomic, and it is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-147">[**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-147">[**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-148">測試指定之 **LONG** 值的指定位並將它設定為0。</span><span class="sxs-lookup"><span data-stu-id="1e565-148">Tests the specified bit of the specified **LONG** value and sets it to 0.</span></span> <span data-ttu-id="1e565-149">作業是不可部分完成的，而且會使用記憶體釋放語義來執行。</span><span class="sxs-lookup"><span data-stu-id="1e565-149">The operation is atomic, and it is performed using memory release semantics.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-150">[**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-150">[**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-151">測試指定之 **LONG** 值的指定位並將它設定為1。</span><span class="sxs-lookup"><span data-stu-id="1e565-151">Tests the specified bit of the specified **LONG** value and sets it to 1.</span></span> <span data-ttu-id="1e565-152">作業是不可部分完成的，而且會使用取得記憶體順序語義來執行。</span><span class="sxs-lookup"><span data-stu-id="1e565-152">The operation is atomic, and it is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-153">[**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-153">[**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-154">測試指定之 **LONG** 值的指定位並將它設定為1。</span><span class="sxs-lookup"><span data-stu-id="1e565-154">Tests the specified bit of the specified **LONG** value and sets it to 1.</span></span> <span data-ttu-id="1e565-155">作業是不可部分完成的，而且會使用發行記憶體順序的語法來執行。</span><span class="sxs-lookup"><span data-stu-id="1e565-155">The operation is atomic, and it is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-156">[**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-156">[**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-157">在指定的值上執行不可部分完成的比較與交換作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-157">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="1e565-158">函數會比較兩個指定的32位值，並根據比較結果與另一個32位值交換。</span><span class="sxs-lookup"><span data-stu-id="1e565-158">The function compares two specified 32-bit values and exchanges with another 32-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="1e565-159">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-159">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="1e565-160">**InterlockedCompareExchange16**</span><span class="sxs-lookup"><span data-stu-id="1e565-160">**InterlockedCompareExchange16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange16)
</dt> <dd>

<span data-ttu-id="1e565-161">在指定的值上執行不可部分完成的比較與交換作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-161">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="1e565-162">函數會比較兩個指定的16位值，並根據比較結果與另一個16位值交換。</span><span class="sxs-lookup"><span data-stu-id="1e565-162">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-163">[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-163">[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-164">在指定的值上執行不可部分完成的比較與交換作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-164">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="1e565-165">函數會比較兩個指定的16位值，並根據比較結果與另一個16位值交換。</span><span class="sxs-lookup"><span data-stu-id="1e565-165">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="1e565-166">執行作業時，會使用取得記憶體順序的語法。</span><span class="sxs-lookup"><span data-stu-id="1e565-166">The operation is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-167">[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-167">[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-168">在指定的值上執行不可部分完成的比較與交換作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-168">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="1e565-169">函數會比較兩個指定的16位值，並根據比較結果與另一個16位值交換。</span><span class="sxs-lookup"><span data-stu-id="1e565-169">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="1e565-170">交換會以發行記憶體順序的語法來執行。</span><span class="sxs-lookup"><span data-stu-id="1e565-170">The exchange is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-171">[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-171">[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-172">在指定的值上執行不可部分完成的比較與交換作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-172">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="1e565-173">函數會比較兩個指定的16位值，並根據比較結果與另一個16位值交換。</span><span class="sxs-lookup"><span data-stu-id="1e565-173">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="1e565-174">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-174">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-175">[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-175">[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-176">在指定的值上執行不可部分完成的比較與交換作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-176">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="1e565-177">函數會比較兩個指定的64位值，並根據比較結果與另一個64位值交換。</span><span class="sxs-lookup"><span data-stu-id="1e565-177">The function compares two specified 64-bit values and exchanges with another 64-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="1e565-178">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-178">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="1e565-179">**InterlockedCompareExchange128**</span><span class="sxs-lookup"><span data-stu-id="1e565-179">**InterlockedCompareExchange128**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange128)
</dt> <dd>

<span data-ttu-id="1e565-180">在指定的值上執行不可部分完成的比較與交換作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-180">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="1e565-181">函數會比較兩個指定的128位值，並根據比較結果與另一個128位值交換。</span><span class="sxs-lookup"><span data-stu-id="1e565-181">The function compares two specified 128-bit values and exchanges with another 128-bit value based on the outcome of the comparison.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-182">[**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-182">[**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-183">在指定的值上執行不可部分完成的比較與交換作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-183">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="1e565-184">此函式會比較兩個指定的指標值，並根據比較結果與另一個指標值交換。</span><span class="sxs-lookup"><span data-stu-id="1e565-184">The function compares two specified pointer values and exchanges with another pointer value based on the outcome of the comparison.</span></span> <span data-ttu-id="1e565-185">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-185">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-186">[**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-186">[**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-187">遞減 (會以一) 指定的32位變數值做為不可部分完成的作業來減少。</span><span class="sxs-lookup"><span data-stu-id="1e565-187">Decrements (decreases by one) the value of the specified 32-bit variable as an atomic operation.</span></span> <span data-ttu-id="1e565-188">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-188">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="1e565-189">**InterlockedDecrement16**</span><span class="sxs-lookup"><span data-stu-id="1e565-189">**InterlockedDecrement16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockeddecrement16)
</dt> <dd>

<span data-ttu-id="1e565-190">遞減 (會將指定的16位變數值減少一) 為不可部分完成的作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-190">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-191">[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-191">[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-192">遞減 (會將指定的16位變數值減少一) 為不可部分完成的作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-192">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="1e565-193">執行作業時，會使用取得記憶體順序的語法。</span><span class="sxs-lookup"><span data-stu-id="1e565-193">The operation is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-194">[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-194">[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-195">遞減 (會將指定的16位變數值減少一) 為不可部分完成的作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-195">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="1e565-196">作業會使用發行記憶體順序的語法來執行。</span><span class="sxs-lookup"><span data-stu-id="1e565-196">The operation is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-197">[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-197">[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-198">遞減 (會將指定的16位變數值減少一) 為不可部分完成的作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-198">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="1e565-199">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-199">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-200">[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-200">[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-201">遞減 (會以一) 指定的64位變數值做為不可部分完成的作業來減少。</span><span class="sxs-lookup"><span data-stu-id="1e565-201">Decrements (decreases by one) the value of the specified 64-bit variable as an atomic operation.</span></span> <span data-ttu-id="1e565-202">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-202">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-203">[**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-203">[**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-204">將64位變數設定為指定的值，作為不可部分完成的作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-204">Sets a 64-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="1e565-205">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-205">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="1e565-206">**InterlockedExchange8**</span><span class="sxs-lookup"><span data-stu-id="1e565-206">**InterlockedExchange8**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedexchange8)
</dt> <dd>

<span data-ttu-id="1e565-207">將8位變數設定為指定的值，作為不可部分完成的作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-207">Sets an 8-bit variable to the specified value as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-208">[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-208">[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-209">將16位變數設定為指定的值，作為不可部分完成的作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-209">Sets a 16-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="1e565-210">作業是使用取得記憶體順序語義來執行。</span><span class="sxs-lookup"><span data-stu-id="1e565-210">The operation is performed using acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-211">[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-211">[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-212">將16位變數設定為指定的值，作為不可部分完成的作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-212">Sets a 16-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="1e565-213">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-213">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-214">[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-214">[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-215">將64位變數設定為指定的值，作為不可部分完成的作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-215">Sets a 64-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="1e565-216">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-216">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-217">[**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-217">[**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-218">以不可部分完成的方式交換一對位址。</span><span class="sxs-lookup"><span data-stu-id="1e565-218">Atomically exchanges a pair of addresses.</span></span> <span data-ttu-id="1e565-219">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-219">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-220">[**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-220">[**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-221">執行 2 32 位值的不可部分完成加法。</span><span class="sxs-lookup"><span data-stu-id="1e565-221">Performs an atomic addition of two 32-bit values.</span></span> <span data-ttu-id="1e565-222">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-222">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-223">[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-223">[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-224">執行 2 64 位值的不可部分完成加法。</span><span class="sxs-lookup"><span data-stu-id="1e565-224">Performs an atomic addition of two 64-bit values.</span></span> <span data-ttu-id="1e565-225">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-225">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-226">[**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-226">[**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-227">遞增 (會以一) 指定的32位變數值為不可部分完成的作業增加。</span><span class="sxs-lookup"><span data-stu-id="1e565-227">Increments (increases by one) the value of the specified 32-bit variable as an atomic operation.</span></span> <span data-ttu-id="1e565-228">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-228">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="1e565-229">**InterlockedIncrement16**</span><span class="sxs-lookup"><span data-stu-id="1e565-229">**InterlockedIncrement16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedincrement16)
</dt> <dd>

<span data-ttu-id="1e565-230">遞增 (增加一個) 指定的16位變數值為不可部分完成的作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-230">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-231">[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-231">[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-232">遞增 (增加一個) 指定的16位變數值為不可部分完成的作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-232">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="1e565-233">作業是使用取得記憶體順序語義來執行。</span><span class="sxs-lookup"><span data-stu-id="1e565-233">The operation is performed using acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-234">[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-234">[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-235">遞增 (增加一個) 指定的16位變數值為不可部分完成的作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-235">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="1e565-236">作業是使用發行記憶體順序的語法來執行。</span><span class="sxs-lookup"><span data-stu-id="1e565-236">The operation is performed using release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-237">[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-237">[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-238">遞增 (增加一個) 指定的16位變數值為不可部分完成的作業。</span><span class="sxs-lookup"><span data-stu-id="1e565-238">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="1e565-239">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-239">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-240">[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-240">[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-241">遞增 (會以一) 指定的64位變數值為不可部分完成的作業增加。</span><span class="sxs-lookup"><span data-stu-id="1e565-241">Increments (increases by one) the value of the specified 64-bit variable as an atomic operation.</span></span> <span data-ttu-id="1e565-242">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-242">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-243">[**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-243">[**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-244">在指定的 **LONG** 值上執行不可部分完成的或運算。</span><span class="sxs-lookup"><span data-stu-id="1e565-244">Performs an atomic OR operation on the specified **LONG** values.</span></span> <span data-ttu-id="1e565-245">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-245">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-246">[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-246">[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-247">在指定的 **char** 值上執行不可部分完成的或運算。</span><span class="sxs-lookup"><span data-stu-id="1e565-247">Performs an atomic OR operation on the specified **char** values.</span></span> <span data-ttu-id="1e565-248">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-248">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-249">[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-249">[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-250">對指定的 **短** 值執行不可部分完成的或運算。</span><span class="sxs-lookup"><span data-stu-id="1e565-250">Performs an atomic OR operation on the specified **SHORT** values.</span></span> <span data-ttu-id="1e565-251">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-251">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-252">[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-252">[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-253">在指定的 **LONGLONG** 值上執行不可部分完成的或運算。</span><span class="sxs-lookup"><span data-stu-id="1e565-253">Performs an atomic OR operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="1e565-254">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-254">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="1e565-255">**InterlockedPushListSListEx**</span><span class="sxs-lookup"><span data-stu-id="1e565-255">**InterlockedPushListSListEx**</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)
</dt> <dd>

<span data-ttu-id="1e565-256">在另一個單一連結清單的前方插入單一連結清單。</span><span class="sxs-lookup"><span data-stu-id="1e565-256">Inserts a singly-linked list at the front of another singly linked list.</span></span> <span data-ttu-id="1e565-257">系統會在多處理器系統上同步處理清單的存取。</span><span class="sxs-lookup"><span data-stu-id="1e565-257">Access to the lists is synchronized on a multiprocessor system.</span></span> <span data-ttu-id="1e565-258">此版本的方法不會使用[ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx)呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="1e565-258">This version of the method does not use the [\_\_fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx) calling convention.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-259">[**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-259">[**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-260">在指定的 **LONG** 值上執行不可部分完成 XOR 運算。</span><span class="sxs-lookup"><span data-stu-id="1e565-260">Performs an atomic XOR operation on the specified **LONG** values.</span></span> <span data-ttu-id="1e565-261">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-261">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-262">[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-262">[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-263">在指定的 **char** 值上執行不可部分完成 XOR 運算。</span><span class="sxs-lookup"><span data-stu-id="1e565-263">Performs an atomic XOR operation on the specified **char** values.</span></span> <span data-ttu-id="1e565-264">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-264">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-265">[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-265">[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-266">在指定的 **短** 值上執行不可部分完成的 XOR 運算。</span><span class="sxs-lookup"><span data-stu-id="1e565-266">Performs an atomic XOR operation on the specified **SHORT** values.</span></span> <span data-ttu-id="1e565-267">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-267">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="1e565-268">[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1e565-268">[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="1e565-269">在指定的 **LONGLONG** 值上執行不可部分完成的 XOR 運算。</span><span class="sxs-lookup"><span data-stu-id="1e565-269">Performs an atomic XOR operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="1e565-270">作業會以程式方式執行，但不會使用記憶體阻礙。</span><span class="sxs-lookup"><span data-stu-id="1e565-270">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> </dl>

## <a name="windows-7"></a><span data-ttu-id="1e565-271">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e565-271">Windows 7</span></span>

### <a name="new-functions"></a><span data-ttu-id="1e565-272">新函式</span><span class="sxs-lookup"><span data-stu-id="1e565-272">New Functions</span></span>

<dl> <dt>

[<span data-ttu-id="1e565-273">**SetWaitableTimerEx**</span><span class="sxs-lookup"><span data-stu-id="1e565-273">**SetWaitableTimerEx**</span></span>](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)
</dt> <dd>

<span data-ttu-id="1e565-274">啟用指定的可等候計時器，並提供計時器的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="1e565-274">Activates the specified waitable timer and provides context information for the timer.</span></span>

</dd> <dt>

[<span data-ttu-id="1e565-275">**TryAcquireSRWLockExclusive**</span><span class="sxs-lookup"><span data-stu-id="1e565-275">**TryAcquireSRWLockExclusive**</span></span>](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)
</dt> <dd>

<span data-ttu-id="1e565-276">嘗試取得超薄的讀取器/寫入器 (在獨佔模式中 SRW) 鎖定。</span><span class="sxs-lookup"><span data-stu-id="1e565-276">Attempts to acquire a slim reader/writer (SRW) lock in exclusive mode.</span></span> <span data-ttu-id="1e565-277">如果呼叫成功，呼叫的執行緒就會取得鎖定的擁有權。</span><span class="sxs-lookup"><span data-stu-id="1e565-277">If the call is successful, the calling thread takes ownership of the lock.</span></span>

</dd> <dt>

[<span data-ttu-id="1e565-278">**TryAcquireSRWLockShared**</span><span class="sxs-lookup"><span data-stu-id="1e565-278">**TryAcquireSRWLockShared**</span></span>](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)
</dt> <dd>

<span data-ttu-id="1e565-279">嘗試取得輕巧的讀取器/寫入器 (在共用模式中 SRW) 鎖定。</span><span class="sxs-lookup"><span data-stu-id="1e565-279">Attempts to acquire a slim reader/writer (SRW) lock in shared mode.</span></span> <span data-ttu-id="1e565-280">如果呼叫成功，呼叫的執行緒就會取得鎖定的擁有權。</span><span class="sxs-lookup"><span data-stu-id="1e565-280">If the call is successful, the calling thread takes ownership of the lock.</span></span>

</dd> </dl>

### <a name="new-structures"></a><span data-ttu-id="1e565-281">新結構</span><span class="sxs-lookup"><span data-stu-id="1e565-281">New Structures</span></span>

<dl> <dt>

[<span data-ttu-id="1e565-282">**原因 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="1e565-282">**REASON\_CONTEXT**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-reason_context)
</dt> <dd>

<span data-ttu-id="1e565-283">包含使用 [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)啟動之計時器的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="1e565-283">Contains context information for a timer activated with [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex).</span></span>

</dd> </dl>

 

 
