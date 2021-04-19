---
description: 堆積片段是可用記憶體分成小型、非連續區塊的狀態。
ms.assetid: d10abf82-423c-4942-b05e-55de3a5c4219
title: 低片段堆積
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad14a97fa6d95b663f63b21f0982332ba0de01e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987523"
---
# <a name="low-fragmentation-heap"></a><span data-ttu-id="2ca1e-103">低片段堆積</span><span class="sxs-lookup"><span data-stu-id="2ca1e-103">Low-fragmentation Heap</span></span>

<span data-ttu-id="2ca1e-104">\[本主題中的資訊適用于 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-104">\[The information in this topic applies to Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="2ca1e-105">從 Windows Vista 開始，系統會視需要使用低片段堆積 (LFH) 來服務記憶體配置要求。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-105">Starting with Windows Vista, the system uses the low-fragmentation heap (LFH) as needed to service memory allocation requests.</span></span> <span data-ttu-id="2ca1e-106">應用程式不需要為其堆積啟用 LFH。\]</span><span class="sxs-lookup"><span data-stu-id="2ca1e-106">Applications do not need to enable the LFH for their heaps.\]</span></span>

<span data-ttu-id="2ca1e-107">堆積片段是可用記憶體分成小型、非連續區塊的狀態。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-107">Heap fragmentation is a state in which available memory is broken into small, noncontiguous blocks.</span></span> <span data-ttu-id="2ca1e-108">當堆積已分割時，即使堆積中的總可用記憶體足以滿足要求，記憶體配置仍可能會失敗，因為沒有單一記憶體區塊夠大。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-108">When a heap is fragmented, memory allocation can fail even when the total available memory in the heap is enough to satisfy a request, because no single block of memory is large enough.</span></span> <span data-ttu-id="2ca1e-109">低片段堆積 (LFH) 有助於減少堆積片段。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-109">The low-fragmentation heap (LFH) helps to reduce heap fragmentation.</span></span>

<span data-ttu-id="2ca1e-110">LFH 不是個別的堆積。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-110">The LFH is not a separate heap.</span></span> <span data-ttu-id="2ca1e-111">相反地，它是應用程式可以為其堆積啟用的原則。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-111">Instead, it is a policy that applications can enable for their heaps.</span></span> <span data-ttu-id="2ca1e-112">當啟用 LFH 時，系統會以某些預先決定的大小來配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-112">When the LFH is enabled, the system allocates memory in certain predetermined sizes.</span></span> <span data-ttu-id="2ca1e-113">當應用程式從已啟用 LFH 的堆積要求記憶體配置時，系統會配置夠大的記憶體區塊，以容納所要求的大小。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-113">When an application requests a memory allocation from a heap that has the LFH enabled, the system allocates the smallest block of memory that is large enough to contain the requested size.</span></span> <span data-ttu-id="2ca1e-114">無論是否啟用 LFH，系統都不會將 LFH 用於大於 16 KB 的配置。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-114">The system does not use the LFH for allocations larger than 16 KB, whether or not the LFH is enabled.</span></span>

<span data-ttu-id="2ca1e-115">應用程式應該只針對呼叫進程的預設堆積或應用程式所建立的 [私](heap-functions.md) 用堆積，啟用 LFH。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-115">An application should enable the LFH only for the default heap of the calling process or for [private heaps](heap-functions.md) that the application has created.</span></span> <span data-ttu-id="2ca1e-116">若要啟用堆積的 LFH，請使用 [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) 函數來取得呼叫進程之預設堆積的控制碼，或使用 [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) 函數所建立之私用堆積的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-116">To enable the LFH for a heap, use the [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) function to obtain a handle to the default heap of the calling process, or use the handle to a private heap created by the [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) function.</span></span> <span data-ttu-id="2ca1e-117">然後使用控制碼呼叫 [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) 函式。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-117">Then call the [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) function with the handle.</span></span>

<span data-ttu-id="2ca1e-118">LFH 無法針對以 **堆積 \_ 無 \_ 序列化** 或使用固定大小建立的堆積來建立堆積。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-118">The LFH cannot be enabled for heaps created with **HEAP\_NO\_SERIALIZE** or for heaps created with a fixed size.</span></span> <span data-ttu-id="2ca1e-119">如果您在 Windows 或[Microsoft 應用程式驗證器](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&displaylang=en)的[偵錯工具](/windows-hardware/drivers/debugger/)中使用堆積偵錯工具，也無法啟用 LFH。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-119">The LFH also cannot be enabled if you are using the heap debugging tools in [Debugging Tools for Windows](/windows-hardware/drivers/debugger/) or [Microsoft Application Verifier](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&displaylang=en).</span></span>

<span data-ttu-id="2ca1e-120">針對堆積啟用 LFH 之後，就無法停用它。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-120">After the LFH has been enabled for a heap, it cannot be disabled.</span></span>

<span data-ttu-id="2ca1e-121">從 LFH 獲益最多的應用程式是多執行緒應用程式，會經常配置記憶體，並使用 16 KB 的各種配置大小。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-121">Applications that benefit most from the LFH are multithreaded applications that allocate memory frequently and use a variety of allocation sizes under 16 KB.</span></span> <span data-ttu-id="2ca1e-122">不過，並非所有應用程式都能受益于 LFH。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-122">However, not all applications benefit from the LFH.</span></span> <span data-ttu-id="2ca1e-123">若要評估在您的應用程式中啟用 LFH 的效果，請使用效能分析資料。</span><span class="sxs-lookup"><span data-stu-id="2ca1e-123">To assess the effects of enabling the LFH in your application, use performance profiling data.</span></span>

 

 
