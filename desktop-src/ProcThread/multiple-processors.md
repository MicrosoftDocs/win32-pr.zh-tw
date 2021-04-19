---
description: 具有多個處理器的電腦通常是針對兩種架構的其中一種來設計： (NUMA) 或對稱式多重處理 (SMP) 的非統一記憶體存取。
ms.assetid: 3c9186c8-a54d-4536-8237-bfff78cc7d11
title: 多個處理器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0093404a0df653a153823915f1ac72b5e41d50c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987532"
---
# <a name="multiple-processors"></a><span data-ttu-id="63aa7-103">多個處理器</span><span class="sxs-lookup"><span data-stu-id="63aa7-103">Multiple Processors</span></span>

<span data-ttu-id="63aa7-104">具有多個處理器的電腦通常是針對兩種架構的其中一種來設計： (NUMA) 或對稱式多重處理 (SMP) 的非統一記憶體存取。</span><span class="sxs-lookup"><span data-stu-id="63aa7-104">Computers with multiple processors are typically designed for one of two architectures: non-uniform memory access (NUMA) or symmetric multiprocessing (SMP).</span></span>

<span data-ttu-id="63aa7-105">在 NUMA 電腦中，每個處理器都比其他處理器更接近某些部分的記憶體，使得記憶體的存取比其他部分更快。</span><span class="sxs-lookup"><span data-stu-id="63aa7-105">In a NUMA computer, each processor is closer to some parts of memory than others, making memory access faster for some parts of memory than other parts.</span></span> <span data-ttu-id="63aa7-106">在 NUMA 模型下，系統會嘗試在接近所用記憶體的處理器上排程執行緒。</span><span class="sxs-lookup"><span data-stu-id="63aa7-106">Under the NUMA model, the system attempts to schedule threads on processors that are close to the memory being used.</span></span> <span data-ttu-id="63aa7-107">如需 NUMA 的詳細資訊，請參閱 [Numa 支援](numa-support.md)。</span><span class="sxs-lookup"><span data-stu-id="63aa7-107">For more information about NUMA, see [NUMA Support](numa-support.md).</span></span>

<span data-ttu-id="63aa7-108">在 SMP 電腦中，兩個或多個相同的處理器或核心會連接到單一共用的主儲存體。</span><span class="sxs-lookup"><span data-stu-id="63aa7-108">In an SMP computer, two or more identical processors or cores connect to a single shared main memory.</span></span> <span data-ttu-id="63aa7-109">在 SMP 模型下，任何執行緒都可以指派給任何處理器。</span><span class="sxs-lookup"><span data-stu-id="63aa7-109">Under the SMP model, any thread can be assigned to any processor.</span></span> <span data-ttu-id="63aa7-110">因此，在 SMP 電腦上排程執行緒，類似于在具有單處理器的電腦上排定執行緒。</span><span class="sxs-lookup"><span data-stu-id="63aa7-110">Therefore, scheduling threads on an SMP computer is similar to scheduling threads on a computer with a single processor.</span></span> <span data-ttu-id="63aa7-111">不過，排程器具有處理器的集區，因此它可以排程要同時執行的執行緒。</span><span class="sxs-lookup"><span data-stu-id="63aa7-111">However, the scheduler has a pool of processors, so that it can schedule threads to run concurrently.</span></span> <span data-ttu-id="63aa7-112">排程仍取決於執行緒優先順序，但設定執行緒親和性和執行緒理想處理器可能會受到影響，如本主題中所述。</span><span class="sxs-lookup"><span data-stu-id="63aa7-112">Scheduling is still determined by thread priority, but it can be influenced by setting thread affinity and thread ideal processor, as discussed in this topic.</span></span>

## <a name="thread-affinity"></a><span data-ttu-id="63aa7-113">執行緒親和性</span><span class="sxs-lookup"><span data-stu-id="63aa7-113">Thread Affinity</span></span>

<span data-ttu-id="63aa7-114">*執行緒親和性* 會強制執行緒在特定的處理器子集上執行。</span><span class="sxs-lookup"><span data-stu-id="63aa7-114">*Thread affinity* forces a thread to run on a specific subset of processors.</span></span> <span data-ttu-id="63aa7-115">通常應該避免設定執行緒親和性，因為它可能會干擾排程器在跨處理器之間有效排程執行緒的能力。</span><span class="sxs-lookup"><span data-stu-id="63aa7-115">Setting thread affinity should generally be avoided, because it can interfere with the scheduler's ability to schedule threads effectively across processors.</span></span> <span data-ttu-id="63aa7-116">這可能會降低平行處理所產生的效能提升。</span><span class="sxs-lookup"><span data-stu-id="63aa7-116">This can decrease the performance gains produced by parallel processing.</span></span> <span data-ttu-id="63aa7-117">執行緒親和性的適當使用會測試每個處理器。</span><span class="sxs-lookup"><span data-stu-id="63aa7-117">An appropriate use of thread affinity is testing each processor.</span></span>

<span data-ttu-id="63aa7-118">系統會以位元遮罩（稱為處理器親和性遮罩）表示親和性。</span><span class="sxs-lookup"><span data-stu-id="63aa7-118">The system represents affinity with a bitmask called a processor affinity mask.</span></span> <span data-ttu-id="63aa7-119">親和性遮罩是系統中的處理器數目上限，並設定 bits 以識別處理器的子集。</span><span class="sxs-lookup"><span data-stu-id="63aa7-119">The affinity mask is the size of the maximum number of processors in the system, with bits set to identify a subset of processors.</span></span> <span data-ttu-id="63aa7-120">一開始，系統會決定遮罩中的處理器子集。</span><span class="sxs-lookup"><span data-stu-id="63aa7-120">Initially, the system determines the subset of processors in the mask.</span></span>

<span data-ttu-id="63aa7-121">您可以藉由呼叫 [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) 函式，為進程的所有線程取得目前的執行緒親和性。</span><span class="sxs-lookup"><span data-stu-id="63aa7-121">You can obtain the current thread affinity for all threads of the process by calling the [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) function.</span></span> <span data-ttu-id="63aa7-122">您可以使用 [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) 函數，為進程的所有線程指定執行緒親和性。</span><span class="sxs-lookup"><span data-stu-id="63aa7-122">Use the [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) function to specify thread affinity for all threads of the process.</span></span> <span data-ttu-id="63aa7-123">若要為單一線程設定執行緒親和性，請使用 [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) 函數。</span><span class="sxs-lookup"><span data-stu-id="63aa7-123">To set the thread affinity for a single thread, use the [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) function.</span></span> <span data-ttu-id="63aa7-124">執行緒親和性必須是進程親和性的子集。</span><span class="sxs-lookup"><span data-stu-id="63aa7-124">The thread affinity must be a subset of the process affinity.</span></span>

<span data-ttu-id="63aa7-125">在具有64以上處理器的系統上，親和性遮罩一開始代表單一處理器群組中的處理器。</span><span class="sxs-lookup"><span data-stu-id="63aa7-125">On systems with more than 64 processors, the affinity mask initially represents processors in a single processor group.</span></span> <span data-ttu-id="63aa7-126">但是，執行緒親和性可以設定為不同群組中的處理器，這會改變進程的親和性遮罩。</span><span class="sxs-lookup"><span data-stu-id="63aa7-126">However, thread affinity can be set to a processor in a different group, which alters the affinity mask for the process.</span></span> <span data-ttu-id="63aa7-127">如需詳細資訊，請參閱 [處理器群組](processor-groups.md)。</span><span class="sxs-lookup"><span data-stu-id="63aa7-127">For more information, see [Processor Groups](processor-groups.md).</span></span>

## <a name="thread-ideal-processor"></a><span data-ttu-id="63aa7-128">執行緒理想的處理器</span><span class="sxs-lookup"><span data-stu-id="63aa7-128">Thread Ideal Processor</span></span>

<span data-ttu-id="63aa7-129">當您指定 *執行緒理想的處理器* 時，排程器會盡可能在指定的處理器上執行執行緒。</span><span class="sxs-lookup"><span data-stu-id="63aa7-129">When you specify a *thread ideal processor*, the scheduler runs the thread on the specified processor when possible.</span></span> <span data-ttu-id="63aa7-130">您可以使用 [**SetThreadIdealProcessor**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor) 函數來指定執行緒的慣用處理器。</span><span class="sxs-lookup"><span data-stu-id="63aa7-130">Use the [**SetThreadIdealProcessor**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor) function to specify a preferred processor for a thread.</span></span> <span data-ttu-id="63aa7-131">這並不保證會選擇理想的處理器，但會對排程器提供實用的提示。</span><span class="sxs-lookup"><span data-stu-id="63aa7-131">This does not guarantee that the ideal processor will be chosen but provides a useful hint to the scheduler.</span></span> <span data-ttu-id="63aa7-132">在具有64以上處理器的系統上，您可以使用 [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex) 函式來指定特定處理器群組中的慣用處理器。</span><span class="sxs-lookup"><span data-stu-id="63aa7-132">On systems with more than 64 processors, you can use the [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex) function to specify a preferred processor in a specific processor group.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63aa7-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="63aa7-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63aa7-134">NUMA 支援</span><span class="sxs-lookup"><span data-stu-id="63aa7-134">NUMA Support</span></span>](numa-support.md)
</dt> <dt>

[<span data-ttu-id="63aa7-135">處理器群組</span><span class="sxs-lookup"><span data-stu-id="63aa7-135">Processor Groups</span></span>](processor-groups.md)
</dt> </dl>

 

 
