---
title: WOW64 下的效能和記憶體耗用量
description: WOW64 下的效能和記憶體耗用量取決於下列因素。
ms.assetid: 77759840-7b1a-4956-a038-d6374b6ec354
keywords:
- WOW64 64 位 Windows 程式設計下的效能
- WOW64 64 位 Windows 程式設計下的記憶體耗用量
- WOW64 64 位 Windows 程式設計，效能
- WOW64 64 位 Windows 程式設計，記憶體耗用量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8928e7d50c8396aa2b5b34081af3e4ee2719e044
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382581"
---
# <a name="performance-and-memory-consumption-under-wow64"></a><span data-ttu-id="c22d2-107">WOW64 下的效能和記憶體耗用量</span><span class="sxs-lookup"><span data-stu-id="c22d2-107">Performance and Memory Consumption Under WOW64</span></span>

<span data-ttu-id="c22d2-108">WOW64 下的效能和記憶體耗用量取決於下列因素：</span><span class="sxs-lookup"><span data-stu-id="c22d2-108">Performance and memory consumption under WOW64 are determined by the following factors:</span></span>

-   <span data-ttu-id="c22d2-109">處理器硬體。</span><span class="sxs-lookup"><span data-stu-id="c22d2-109">Processor hardware.</span></span> <span data-ttu-id="c22d2-110">指令模擬會在晶片上執行。</span><span class="sxs-lookup"><span data-stu-id="c22d2-110">Instruction emulation is performed on the chip.</span></span> <span data-ttu-id="c22d2-111">在 x64 處理器上，x86 指令是由處理器以原生方式執行。</span><span class="sxs-lookup"><span data-stu-id="c22d2-111">On the x64 processor, x86 instructions are executed natively by the processor.</span></span> <span data-ttu-id="c22d2-112">因此，在 x64 上的 WOW64 下執行速度類似于32位 Windows 下的速度。</span><span class="sxs-lookup"><span data-stu-id="c22d2-112">Therefore, execution speed under WOW64 on x64 is similar to its speed under 32-bit Windows.</span></span> <span data-ttu-id="c22d2-113">在 Intel Itanium 處理器和任何 ARM64 處理器上，模擬有更多的軟體，因此效能也會受到影響。</span><span class="sxs-lookup"><span data-stu-id="c22d2-113">On the Intel Itanium processor and any ARM64 processors, more software is involved in the emulation, and performance suffers as a result.</span></span>
-   <span data-ttu-id="c22d2-114">API Thunk 的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="c22d2-114">API thunk overhead.</span></span> <span data-ttu-id="c22d2-115">相較于 NT 核心的系統呼叫，此額外負荷很小。</span><span class="sxs-lookup"><span data-stu-id="c22d2-115">This overhead is small compared to system calls to the NT kernel.</span></span> <span data-ttu-id="c22d2-116">NT 核心函式的設計不常被呼叫。</span><span class="sxs-lookup"><span data-stu-id="c22d2-116">NT kernel functions are intended to be called infrequently.</span></span>
-   <span data-ttu-id="c22d2-117">虛擬記憶體大小。</span><span class="sxs-lookup"><span data-stu-id="c22d2-117">Virtual memory size.</span></span> <span data-ttu-id="c22d2-118">在 Intel Itanium 處理器上，如果相同32位應用程式的兩個或多個實例同時執行，WOW64 會增加大量負荷。</span><span class="sxs-lookup"><span data-stu-id="c22d2-118">On the Intel Itanium processor, WOW64 adds significant overhead if two or more instances of the same 32-bit application are running concurrently.</span></span> <span data-ttu-id="c22d2-119">這是因為 Intel Itanium 上的原生 8 KB 頁面，它會使 x86 架構上原生 4 KB 頁面的模擬變得更複雜 (更多頁面標記為可寫入;所有可寫入的頁面都是進程) 的私用。</span><span class="sxs-lookup"><span data-stu-id="c22d2-119">This is due to the native 8 KB pages on the Intel Itanium, which complicates the emulation of the native 4 KB pages on the x86 architecture (more pages are marked as writable; all writable pages are private to the process).</span></span> <span data-ttu-id="c22d2-120">這可能會對特定處理器上的終端機服務的擴充性造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="c22d2-120">This can adversely affect the scalability of Terminal Services on certain processors.</span></span> <span data-ttu-id="c22d2-121">這不是 x64 處理器的情況。</span><span class="sxs-lookup"><span data-stu-id="c22d2-121">This is not the case for the x64 processor.</span></span>
-   <span data-ttu-id="c22d2-122">工作集。</span><span class="sxs-lookup"><span data-stu-id="c22d2-122">Working set.</span></span> <span data-ttu-id="c22d2-123">WOW64 會增加應用程式的工作集大小。</span><span class="sxs-lookup"><span data-stu-id="c22d2-123">WOW64 increases the size of the application's working set.</span></span>

<span data-ttu-id="c22d2-124">WOW64 可讓32位應用程式利用64位核心。</span><span class="sxs-lookup"><span data-stu-id="c22d2-124">WOW64 enables 32-bit applications to take advantage of the 64-bit kernel.</span></span> <span data-ttu-id="c22d2-125">因此，32位應用程式可以使用較大量的核心控制碼和視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="c22d2-125">Therefore, 32-bit applications can use a larger number of kernel handles and window handles.</span></span> <span data-ttu-id="c22d2-126">不過，32位應用程式可能無法在 WOW64 上建立多個執行緒，因為它們可以在 x86 系統上以原生方式執行，因為 WOW64 會配置額外的64位堆疊， (通常會為每個執行緒 512 KB) 。</span><span class="sxs-lookup"><span data-stu-id="c22d2-126">However, 32-bit applications may not be able to create as many threads under WOW64 as they can when running natively on x86-based systems because WOW64 allocates an additional 64-bit stack (usually 512 KB) for each thread.</span></span> <span data-ttu-id="c22d2-127">此外，某些位址空間會保留給 WOW64 本身，以及它所使用的資料結構。</span><span class="sxs-lookup"><span data-stu-id="c22d2-127">In addition, some amount of address space is reserved for WOW64 itself and the data structures it uses.</span></span> <span data-ttu-id="c22d2-128">保留的數量取決於處理器;優於 x64 或 ARM64 處理器上的 Intel Itanium 有更多保留。</span><span class="sxs-lookup"><span data-stu-id="c22d2-128">The amount reserved depends on the processor; more is reserved on the Intel Itanium than on the x64 or ARM64 processors.</span></span>

<span data-ttu-id="c22d2-129">如果應用程式在映射標頭中設定了 [**圖像 \_ 檔案 \_ 大型 \_ 位址 \_ 感知**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) 旗標，則每個32位應用程式會在 WOW64 環境中收到 4 GB 的虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="c22d2-129">If the application has the [**IMAGE\_FILE\_LARGE\_ADDRESS\_AWARE**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) flag set in the image header, each 32-bit application receives 4 GB of virtual address space in the WOW64 environment.</span></span> <span data-ttu-id="c22d2-130">如果未設定 **圖像 \_ 檔案 \_ 大型 \_ 位址 \_ 感知** 旗標，每個32位應用程式會在 WOW64 環境中收到 2 GB 的虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="c22d2-130">If the **IMAGE\_FILE\_LARGE\_ADDRESS\_AWARE** flag is not set, each 32-bit application receives 2 GB of virtual address space in the WOW64 environment.</span></span>

 

 