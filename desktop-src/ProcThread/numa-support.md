---
description: 傳統的多處理器支援模型是 (SMP) 的對稱多處理器。 在此模型中，每個處理器都有相當於記憶體和 i/o 的存取權。 隨著新增更多處理器，處理器匯流排會成為系統效能的限制。
ms.assetid: a1263968-2b26-45cc-bdd7-6aa354821a5a
title: NUMA 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178f53c6b55b6ae291cd5cdcf99386515a441094
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549803"
---
# <a name="numa-support"></a><span data-ttu-id="7fed7-105">NUMA 支援</span><span class="sxs-lookup"><span data-stu-id="7fed7-105">NUMA Support</span></span>

<span data-ttu-id="7fed7-106">傳統的多處理器支援模型是 (SMP) 的對稱多處理器。</span><span class="sxs-lookup"><span data-stu-id="7fed7-106">The traditional model for multiprocessor support is symmetric multiprocessor (SMP).</span></span> <span data-ttu-id="7fed7-107">在此模型中，每個處理器都有相當於記憶體和 i/o 的存取權。</span><span class="sxs-lookup"><span data-stu-id="7fed7-107">In this model, each processor has equal access to memory and I/O.</span></span> <span data-ttu-id="7fed7-108">隨著新增更多處理器，處理器匯流排會成為系統效能的限制。</span><span class="sxs-lookup"><span data-stu-id="7fed7-108">As more processors are added, the processor bus becomes a limitation for system performance.</span></span>

<span data-ttu-id="7fed7-109">系統設計人員使用非統一記憶體存取 (NUMA) 來提高處理器速度，而不會增加處理器匯流排的負載。</span><span class="sxs-lookup"><span data-stu-id="7fed7-109">System designers use non-uniform memory access (NUMA) to increase processor speed without increasing the load on the processor bus.</span></span> <span data-ttu-id="7fed7-110">架構是非統一的，因為每個處理器都靠近記憶體的某些部分，而從記憶體的其他部分更遠。</span><span class="sxs-lookup"><span data-stu-id="7fed7-110">The architecture is non-uniform because each processor is close to some parts of memory and farther from other parts of memory.</span></span> <span data-ttu-id="7fed7-111">處理器可以快速存取接近的記憶體，但需要較長的時間才能存取離離的記憶體。</span><span class="sxs-lookup"><span data-stu-id="7fed7-111">The processor quickly gains access to the memory it is close to, while it can take longer to gain access to memory that is farther away.</span></span>

<span data-ttu-id="7fed7-112">在 NUMA 系統中，Cpu 會以較小的系統（稱為 *節點*）排列。</span><span class="sxs-lookup"><span data-stu-id="7fed7-112">In a NUMA system, CPUs are arranged in smaller systems called *nodes*.</span></span> <span data-ttu-id="7fed7-113">每個節點都有自己的處理器和記憶體，並透過快取一致的互連匯流排連接到較大的系統。</span><span class="sxs-lookup"><span data-stu-id="7fed7-113">Each node has its own processors and memory, and is connected to the larger system through a cache-coherent interconnect bus.</span></span>

<span data-ttu-id="7fed7-114">系統會嘗試在與所用記憶體相同的節點中，排程處理器上的執行緒，藉以改善效能。</span><span class="sxs-lookup"><span data-stu-id="7fed7-114">The system attempts to improve performance by scheduling threads on processors that are in the same node as the memory being used.</span></span> <span data-ttu-id="7fed7-115">它會嘗試滿足來自節點內的記憶體配置要求，但視需要從其他節點配置記憶體。</span><span class="sxs-lookup"><span data-stu-id="7fed7-115">It attempts to satisfy memory-allocation requests from within the node, but will allocate memory from other nodes if necessary.</span></span> <span data-ttu-id="7fed7-116">它也會提供 API，讓應用程式可以使用系統的拓撲。</span><span class="sxs-lookup"><span data-stu-id="7fed7-116">It also provides an API to make the topology of the system available to applications.</span></span> <span data-ttu-id="7fed7-117">您可以使用 NUMA 函數將排程和記憶體使用量優化，以改善應用程式的效能。</span><span class="sxs-lookup"><span data-stu-id="7fed7-117">You can improve the performance of your applications by using the NUMA functions to optimize scheduling and memory usage.</span></span>

<span data-ttu-id="7fed7-118">首先，您必須判斷系統中節點的版面配置。</span><span class="sxs-lookup"><span data-stu-id="7fed7-118">First of all, you will need to determine the layout of nodes in the system.</span></span> <span data-ttu-id="7fed7-119">若要取出系統中最高的編號節點，請使用 [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber) 函數。</span><span class="sxs-lookup"><span data-stu-id="7fed7-119">To retrieve the highest numbered node in the system, use the [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber) function.</span></span> <span data-ttu-id="7fed7-120">請注意，此數目不保證等於系統中的節點總數。</span><span class="sxs-lookup"><span data-stu-id="7fed7-120">Note that this number is not guaranteed to equal the total number of nodes in the system.</span></span> <span data-ttu-id="7fed7-121">此外，具有連續數位的節點不保證會同時關閉。</span><span class="sxs-lookup"><span data-stu-id="7fed7-121">Also, nodes with sequential numbers are not guaranteed to be close together.</span></span> <span data-ttu-id="7fed7-122">若要取出系統上的處理器清單，請使用 [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) 函數。</span><span class="sxs-lookup"><span data-stu-id="7fed7-122">To retrieve the list of processors on the system, use the [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) function.</span></span> <span data-ttu-id="7fed7-123">您可以使用 [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode) 函式來判斷清單中每個處理器的節點。</span><span class="sxs-lookup"><span data-stu-id="7fed7-123">You can determine the node for each processor in the list by using the [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode) function.</span></span> <span data-ttu-id="7fed7-124">或者，若要取得節點中所有處理器的清單，請使用 [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask) 函數。</span><span class="sxs-lookup"><span data-stu-id="7fed7-124">Alternatively, to retrieve a list of all processors in a node, use the [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask) function.</span></span>

<span data-ttu-id="7fed7-125">確定哪些處理器屬於哪些節點之後，您就可以將應用程式的效能優化。</span><span class="sxs-lookup"><span data-stu-id="7fed7-125">After you have determined which processors belong to which nodes, you can optimize your application's performance.</span></span> <span data-ttu-id="7fed7-126">若要確保進程的所有線程都在相同的節點上執行，請使用 [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) 函式搭配處理常式親和性遮罩，以指定相同節點中的處理器。</span><span class="sxs-lookup"><span data-stu-id="7fed7-126">To ensure that all threads for your process run on the same node, use the [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) function with a process affinity mask that specifies processors in the same node.</span></span> <span data-ttu-id="7fed7-127">這會增加執行緒需要存取相同記憶體的應用程式效率。</span><span class="sxs-lookup"><span data-stu-id="7fed7-127">This increases the efficiency of applications whose threads need to access the same memory.</span></span> <span data-ttu-id="7fed7-128">或者，若要限制每個節點上的執行緒數目，請使用 [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) 函數。</span><span class="sxs-lookup"><span data-stu-id="7fed7-128">Alternatively, to limit the number of threads on each node, use the [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) function.</span></span>

<span data-ttu-id="7fed7-129">需要海量儲存體的應用程式必須將記憶體使用量優化。</span><span class="sxs-lookup"><span data-stu-id="7fed7-129">Memory-intensive applications will need to optimize their memory usage.</span></span> <span data-ttu-id="7fed7-130">若要取出可供節點使用的可用記憶體數量，請使用 [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode) 函數。</span><span class="sxs-lookup"><span data-stu-id="7fed7-130">To retrieve the amount of free memory available to a node, use the [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode) function.</span></span> <span data-ttu-id="7fed7-131">[**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)函數可讓應用程式指定記憶體配置的慣用節點。</span><span class="sxs-lookup"><span data-stu-id="7fed7-131">The [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) function enables the application to specify a preferred node for the memory allocation.</span></span> <span data-ttu-id="7fed7-132">**VirtualAllocExNuma** 不會配置任何實體頁面，因此無論這些頁面是否可在該節點上或在系統中的其他位置上，都將會成功。</span><span class="sxs-lookup"><span data-stu-id="7fed7-132">**VirtualAllocExNuma** does not allocate any physical pages, so it will succeed whether or not the pages are available on that node or elsewhere in the system.</span></span> <span data-ttu-id="7fed7-133">實體頁面會依需求配置。</span><span class="sxs-lookup"><span data-stu-id="7fed7-133">The physical pages are allocated on demand.</span></span> <span data-ttu-id="7fed7-134">如果慣用的節點用盡頁面，記憶體管理員將會使用來自其他節點的頁面。</span><span class="sxs-lookup"><span data-stu-id="7fed7-134">If the preferred node runs out of pages, the memory manager will use pages from other nodes.</span></span> <span data-ttu-id="7fed7-135">如果記憶體已分頁，則會在重新進入時使用相同的進程。</span><span class="sxs-lookup"><span data-stu-id="7fed7-135">If the memory is paged out, the same process is used when it is brought back in.</span></span>

### <a name="numa-support-on-systems-with-more-than-64-logical-processors"></a><span data-ttu-id="7fed7-136">超過64個邏輯處理器的系統上的 NUMA 支援</span><span class="sxs-lookup"><span data-stu-id="7fed7-136">NUMA Support on Systems With More Than 64 Logical Processors</span></span>

<span data-ttu-id="7fed7-137">在具有超過64個邏輯處理器的系統上，會根據節點的容量將節點指派給 [處理器群組](processor-groups.md) 。</span><span class="sxs-lookup"><span data-stu-id="7fed7-137">On systems with more than 64 logical processors, nodes are assigned to [processor groups](processor-groups.md) according to the capacity of the nodes.</span></span> <span data-ttu-id="7fed7-138">節點的容量是指當系統啟動時，系統會與任何可在系統執行時新增的其他邏輯處理器一起出現的處理器數目。</span><span class="sxs-lookup"><span data-stu-id="7fed7-138">The capacity of a node is the number of processors that are present when the system starts together with any additional logical processors that can be added while the system is running.</span></span>

<span data-ttu-id="7fed7-139">**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 不支援處理器群組。</span><span class="sxs-lookup"><span data-stu-id="7fed7-139">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** Processor groups are not supported.</span></span>

<span data-ttu-id="7fed7-140">每個節點都必須完全包含在群組內。</span><span class="sxs-lookup"><span data-stu-id="7fed7-140">Each node must be fully contained within a group.</span></span> <span data-ttu-id="7fed7-141">如果節點的容量相對較小，系統會將多個節點指派給相同群組，選擇實體接近另一個節點的節點，以獲得更佳的效能。</span><span class="sxs-lookup"><span data-stu-id="7fed7-141">If the capacities of the nodes are relatively small, the system assigns more than one node to the same group, choosing nodes that are physically close to one another for better performance.</span></span> <span data-ttu-id="7fed7-142">如果節點的容量超過群組中的處理器數目上限，系統會將節點分割成多個較小的節點，每個節點的大小都足以容納在群組中。</span><span class="sxs-lookup"><span data-stu-id="7fed7-142">If a node's capacity exceeds the maximum number of processors in a group, the system splits the node into multiple smaller nodes, each small enough to fit in a group.</span></span>

<span data-ttu-id="7fed7-143">建立程式時，您可以使用處理 [**\_ 執行緒 \_ 屬性 \_ 慣用 \_ 節點**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) 擴充屬性來要求新進程的理想 NUMA 節點。</span><span class="sxs-lookup"><span data-stu-id="7fed7-143">An ideal NUMA node for a new process can be requested using the [**PROC\_THREAD\_ATTRIBUTE\_PREFERRED\_NODE**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) extended attribute when the process is created.</span></span> <span data-ttu-id="7fed7-144">就像執行緒理想的處理器一樣，理想的節點是排程器的提示，可在可能的情況下，將新的進程指派給包含要求之節點的群組。</span><span class="sxs-lookup"><span data-stu-id="7fed7-144">Like a thread ideal processor, the ideal node is a hint to the scheduler, which assigns the new process to the group that contains the requested node if possible.</span></span>

<span data-ttu-id="7fed7-145">擴充 NUMA 函式 [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)、 [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)、 [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)和 [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex) 與其 unextended 對應專案不同，因為節點編號是 **USHORT** 值而不是 **UCHAR**，以容納有超過64個邏輯處理器的系統上可能有更多節點數目。</span><span class="sxs-lookup"><span data-stu-id="7fed7-145">The extended NUMA functions [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex), [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex), [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex), and [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex) differ from their unextended counterparts in that the node number is a **USHORT** value rather than a **UCHAR**, to accommodate the potentially greater number of nodes on a system with more than 64 logical processors.</span></span> <span data-ttu-id="7fed7-146">此外，由擴充函式指定或抓取的處理器包含處理器群組;unextended 函式所指定或抓取的處理器是群組相關的。</span><span class="sxs-lookup"><span data-stu-id="7fed7-146">Also, the processor specified with or retrieved by the extended functions includes the processor group; the processor specified with or retrieved by the unextended functions is group-relative.</span></span> <span data-ttu-id="7fed7-147">如需詳細資訊，請參閱個別的函數參考主題。</span><span class="sxs-lookup"><span data-stu-id="7fed7-147">For details, see the individual function reference topics.</span></span>

<span data-ttu-id="7fed7-148">群組感知的應用程式可以使用對應的擴充 NUMA 函式，以類似于本主題稍早所述的方式，將其所有線程指派給特定的節點。</span><span class="sxs-lookup"><span data-stu-id="7fed7-148">A group-aware application can assign all of its threads to a particular node in a similar fashion to that described earlier in this topic, using the corresponding extended NUMA functions.</span></span> <span data-ttu-id="7fed7-149">應用程式會使用 [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) 取得系統上的所有處理器清單。</span><span class="sxs-lookup"><span data-stu-id="7fed7-149">The application uses [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) to get the list of all processors on the system.</span></span> <span data-ttu-id="7fed7-150">請注意，除非將進程指派給單一群組，且預期的節點位於該群組中，否則應用程式無法設定進程親和性遮罩。</span><span class="sxs-lookup"><span data-stu-id="7fed7-150">Note that the application cannot set the process affinity mask unless the process is assigned to a single group and the intended node is located in that group.</span></span> <span data-ttu-id="7fed7-151">應用程式通常必須呼叫 [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity) ，以將其執行緒限制為預定的節點。</span><span class="sxs-lookup"><span data-stu-id="7fed7-151">Usually the application must call [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity) to limit its threads to the intended node.</span></span>


### <a name="behavior-starting-with-windows-10-build-20348"></a><span data-ttu-id="7fed7-152">從 Windows 10 組建20348開始的行為</span><span class="sxs-lookup"><span data-stu-id="7fed7-152">Behavior starting with Windows 10 Build 20348</span></span> 

> [!NOTE]
> <span data-ttu-id="7fed7-153">從 Windows 10 組建20348開始，此和其他 NUMA 函式的行為已經過修改，可提供更好的支援系統，其節點包含更多的64處理器。</span><span class="sxs-lookup"><span data-stu-id="7fed7-153">Starting with Windows 10 Build 20348, the behavior of this and other NUMA functions has been modified to better support systems with nodes containing more that 64 processors.</span></span>

<span data-ttu-id="7fed7-154">建立「假」節點以容納群組和節點之間的1:1 對應，會產生令人困惑的行為，其中報告了非預期的 NUMA 節點數目，因此從 Windows 10 組建20348開始，作業系統已變更為允許多個群組與節點相關聯，因此現在可以報告系統的真正 NUMA 拓撲。</span><span class="sxs-lookup"><span data-stu-id="7fed7-154">Creating "fake" nodes to accommodate a 1:1 mapping between groups and nodes has resulted in confusing behaviors where unexpected numbers of NUMA nodes are reported and so, starting with Windows 10 Build 20348, the OS has changed to allow multiple groups to be associated with a node, and so now the true NUMA topology of the system can be reported.</span></span>  

<span data-ttu-id="7fed7-155">在對 OS 進行這些變更的過程中，有一些 NUMA Api 已變更為支援報告多個群組，而現在可以與單一 NUMA 節點相關聯。</span><span class="sxs-lookup"><span data-stu-id="7fed7-155">As part of these changes to the OS, a number of NUMA APIs have changed to support reporting the multiple groups which can now be associated with a single NUMA node.</span></span> <span data-ttu-id="7fed7-156">更新和新的 Api 會標示在以下 **NUMA API** 區段的表格中。</span><span class="sxs-lookup"><span data-stu-id="7fed7-156">Updated and new APIs are labeled in the table in the **NUMA API** section below.</span></span>

<span data-ttu-id="7fed7-157">由於移除節點分割可能會影響現有的應用程式，因此可以使用登錄值來選擇回到舊版節點分割行為。</span><span class="sxs-lookup"><span data-stu-id="7fed7-157">Because the removal of node splitting can potentially impact existing applications, a registry value is available to allow opting back into the legacy node splitting behavior.</span></span> <span data-ttu-id="7fed7-158">您可以建立名為 "SplitLargeNodes" 的 **REG_DWORD** 值，並將值1放在 HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\NUMA 下方，以重新啟用節點分割。</span><span class="sxs-lookup"><span data-stu-id="7fed7-158">Node splitting can be re-enabled by creating a **REG_DWORD** value named "SplitLargeNodes" with value 1 underneath HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\NUMA.</span></span> <span data-ttu-id="7fed7-159">變更此設定需要重新開機才會生效。</span><span class="sxs-lookup"><span data-stu-id="7fed7-159">Changes to this setting require a reboot to take effect.</span></span>

```powershell
reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\NUMA" /v SplitLargeNumaNodes /t REG_DWORD /v 1
```

> [!NOTE]
> <span data-ttu-id="7fed7-160">如果應用程式已更新為使用新的 API 功能來回報真正的 NUMA 拓撲，在使用此登錄機碼重新啟用大型節點分割的系統上，將會繼續正常運作。</span><span class="sxs-lookup"><span data-stu-id="7fed7-160">Applications that are updated to use the new API functionality that reports the true NUMA topology will continue to work properly on systems where large node splitting has been reenabled with this registry key.</span></span>

<span data-ttu-id="7fed7-161">下列範例會先示範組建資料表使用舊版親和性 Api 將處理器對應到 NUMA 節點的潛在問題，而不再提供系統中所有處理器的完整涵蓋，這可能會導致不完整的資料表。</span><span class="sxs-lookup"><span data-stu-id="7fed7-161">The following example first demonstrates potential issues with builds tables mapping processors to NUMA nodes using the legacy affinity APIs, which no longer provide a full cover of all processors in the system this can result in an incomplete table.</span></span> <span data-ttu-id="7fed7-162">這類不完整性的含意取決於資料表的內容。</span><span class="sxs-lookup"><span data-stu-id="7fed7-162">The implications of such incompleteness depend on the contents of the table.</span></span> <span data-ttu-id="7fed7-163">如果資料表只是儲存對應的節點編號，則這可能只是因為未發現的處理器被保留在節點0中的效能問題。</span><span class="sxs-lookup"><span data-stu-id="7fed7-163">If the table simply stores the corresponding node number then this is likely only a performance issue with uncovered processors being left as part of node 0.</span></span> <span data-ttu-id="7fed7-164">但是，如果資料表包含每個節點內容結構的指標，則會在執行時間產生 Null 取值。</span><span class="sxs-lookup"><span data-stu-id="7fed7-164">However, if the table contains pointers to a per-node context structure this can result in NULL dereferences at runtime.</span></span>

<span data-ttu-id="7fed7-165">接下來，此程式碼範例說明這兩個問題的因應措施。</span><span class="sxs-lookup"><span data-stu-id="7fed7-165">Next, the code example illustrates two workarounds for the issue.</span></span> <span data-ttu-id="7fed7-166">第一個是遷移至多重群組節點親和性 Api， (使用者模式和核心模式) 。</span><span class="sxs-lookup"><span data-stu-id="7fed7-166">The first is to migrate to the multi-group node affinity APIs (user-mode and kernel-mode).</span></span> <span data-ttu-id="7fed7-167">第二種方式是使用 **KeQueryLogicalProcessorRelationship** 來直接查詢與指定處理器編號相關聯的 NUMA 節點。</span><span class="sxs-lookup"><span data-stu-id="7fed7-167">The second is to use **KeQueryLogicalProcessorRelationship** to directly query the NUMA node associated with a given processor number.</span></span>

```cpp

//
// Problematic implementation using KeQueryNodeActiveAffinity.
//

USHORT CurrentNode;
USHORT HighestNodeNumber;
GROUP_AFFINITY NodeAffinity;
ULONG ProcessorIndex;
PROCESSOR_NUMBER ProcessorNumber;

HighestNodeNumber = KeQueryHighestNodeNumber();
for (CurrentNode = 0; CurrentNode <= HighestNodeNumber; CurrentNode += 1) {

    KeQueryNodeActiveAffinity(CurrentNode, &NodeAffinity, NULL);
    while (NodeAffinity.Mask != 0) {

        ProcessorNumber.Group = NodeAffinity.Group;
        BitScanForward(&ProcessorNumber.Number, NodeAffinity.Mask);

        ProcessorIndex = KeGetProcessorIndexFromNumber(&ProcessorNumber);

        ProcessorNodeContexts[ProcessorIndex] = NodeContexts[CurrentNode;]

        NodeAffinity.Mask &= ~((KAFFINITY)1 << ProcessorNumber.Number);
    }
}

//
// Resolution using KeQueryNodeActiveAffinity2.
//

USHORT CurrentIndex;
USHORT CurrentNode;
USHORT CurrentNodeAffinityCount;
USHORT HighestNodeNumber;
ULONG MaximumGroupCount;
PGROUP_AFFINITY NodeAffinityMasks;
ULONG ProcessorIndex;
PROCESSOR_NUMBER ProcessorNumber;
NTSTATUS Status;

MaximumGroupCount = KeQueryMaximumGroupCount();
NodeAffinityMasks = ExAllocatePool2(POOL_FLAG_PAGED,
                                    sizeof(GROUP_AFFINITY) * MaximumGroupCount,
                                    'tseT');

if (NodeAffinityMasks == NULL) {
    return STATUS_NO_MEMORY;
}

HighestNodeNumber = KeQueryHighestNodeNumber();
for (CurrentNode = 0; CurrentNode <= HighestNodeNumber; CurrentNode += 1) {

    Status = KeQueryNodeActiveAffinity2(CurrentNode,
                                        NodeAffinityMasks,
                                        MaximumGroupCount,
                                        &CurrentNodeAffinityCount);
    NT_ASSERT(NT_SUCCESS(Status));

    for (CurrentIndex = 0; CurrentIndex < CurrentNodeAffinityCount; CurrentIndex += 1) {

        CurrentAffinity = &NodeAffinityMasks[CurrentIndex];

        while (CurrentAffinity->Mask != 0) {

            ProcessorNumber.Group = CurrentAffinity.Group;
            BitScanForward(&ProcessorNumber.Number, CurrentAffinity->Mask);

            ProcessorIndex = KeGetProcessorIndexFromNumber(&ProcessorNumber);

            ProcessorNodeContexts[ProcessorIndex] = NodeContexts[CurrentNode];

            CurrentAffinity->Mask &= ~((KAFFINITY)1 << ProcessorNumber.Number);
        }
    }
}

//
// Resolution using KeQueryLogicalProcessorRelationship.
//

ULONG ProcessorCount;
ULONG ProcessorIndex;
SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX ProcessorInformation;
ULONG ProcessorInformationSize;
PROCESSOR_NUMBER ProcessorNumber;
NTSTATUS Status;

ProcessorCount = KeQueryActiveProcessorCountEx(ALL_PROCESSOR_GROUPS);

for (ProcessorIndex = 0; ProcessorIndex < ProcessorCount; ProcessorIndex += 1) {

    Status = KeGetProcessorNumberFromIndex(ProcessorIndex, &ProcessorNumber);
    NT_ASSERT(NT_SUCCESS(Status));

    ProcessorInformationSize = sizeof(ProcessorInformation);
    Status = KeQueryLogicalProcessorRelationship(&ProcessorNumber,
                                                    RelationNumaNode,
                                                    &ProcessorInformation,
                                                    &ProcesorInformationSize);
    NT_ASSERT(NT_SUCCESS(Status));

    NodeNumber = ProcessorInformation.NumaNode.NodeNumber;

    ProcessorNodeContexts[ProcessorIndex] = NodeContexts[NodeNumber];
}
```

## <a name="numa-api"></a><span data-ttu-id="7fed7-168">NUMA API</span><span class="sxs-lookup"><span data-stu-id="7fed7-168">NUMA API</span></span>

<span data-ttu-id="7fed7-169">下表描述 NUMA API。</span><span class="sxs-lookup"><span data-stu-id="7fed7-169">The following table describes the NUMA API.</span></span>



| <span data-ttu-id="7fed7-170">函式</span><span class="sxs-lookup"><span data-stu-id="7fed7-170">Function</span></span>                                                                     | <span data-ttu-id="7fed7-171">描述</span><span class="sxs-lookup"><span data-stu-id="7fed7-171">Description</span></span>                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fed7-172">**AllocateUserPhysicalPagesNuma**</span><span class="sxs-lookup"><span data-stu-id="7fed7-172">**AllocateUserPhysicalPagesNuma**</span></span>](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)      | <span data-ttu-id="7fed7-173">配置要在指定進程 (AWE) 區域內的任何 [位址視窗擴充](../memory/address-windowing-extensions.md) 內對應和取消對應的實體記憶體頁面，並為實體記憶體指定 NUMA 節點。</span><span class="sxs-lookup"><span data-stu-id="7fed7-173">Allocates physical memory pages to be mapped and unmapped within any [Address Windowing Extensions](../memory/address-windowing-extensions.md) (AWE) region of a specified process and specifies the NUMA node for the physical memory.</span></span> |
| [<span data-ttu-id="7fed7-174">**CreateFileMappingNuma**</span><span class="sxs-lookup"><span data-stu-id="7fed7-174">**CreateFileMappingNuma**</span></span>](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingnumaw)                      | <span data-ttu-id="7fed7-175">針對指定的檔案建立或開啟已命名或未命名的檔案對應物件，並為實體記憶體指定 NUMA 節點。</span><span class="sxs-lookup"><span data-stu-id="7fed7-175">Creates or opens a named or unnamed file mapping object for a specified file, and specifies the NUMA node for the physical memory.</span></span>                                                                                              |
| [<span data-ttu-id="7fed7-176">**GetLogicalProcessorInformation**</span><span class="sxs-lookup"><span data-stu-id="7fed7-176">**GetLogicalProcessorInformation**</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | <span data-ttu-id="7fed7-177">已在 Windows 10 組建20348中更新。</span><span class="sxs-lookup"><span data-stu-id="7fed7-177">Updated in Windows 10 Build 20348.</span></span> <span data-ttu-id="7fed7-178">抓取邏輯處理器和相關硬體的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7fed7-178">Retrieves information about logical processors and related hardware.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="7fed7-179">**GetLogicalProcessorInformationEx**</span><span class="sxs-lookup"><span data-stu-id="7fed7-179">**GetLogicalProcessorInformationEx**</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | <span data-ttu-id="7fed7-180">已在 Windows 10 組建20348中更新。</span><span class="sxs-lookup"><span data-stu-id="7fed7-180">Updated in Windows 10 Build 20348.</span></span> <span data-ttu-id="7fed7-181">抓取邏輯處理器和相關硬體關聯性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7fed7-181">Retrieves information about the relationships of logical processors and related hardware.</span></span>                                                                                                                                       |
| [<span data-ttu-id="7fed7-182">**GetNumaAvailableMemoryNode**</span><span class="sxs-lookup"><span data-stu-id="7fed7-182">**GetNumaAvailableMemoryNode**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)             | <span data-ttu-id="7fed7-183">抓取指定節點中的可用記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="7fed7-183">Retrieves the amount of memory available in the specified node.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="7fed7-184">**GetNumaAvailableMemoryNodeEx**</span><span class="sxs-lookup"><span data-stu-id="7fed7-184">**GetNumaAvailableMemoryNodeEx**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)         | <span data-ttu-id="7fed7-185">抓取指定為 **USHORT** 值之節點中的可用記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="7fed7-185">Retrieves the amount of memory available in a node specified as a **USHORT** value.</span></span>                                                                                                                                             |
| [<span data-ttu-id="7fed7-186">**GetNumaHighestNodeNumber**</span><span class="sxs-lookup"><span data-stu-id="7fed7-186">**GetNumaHighestNodeNumber**</span></span>](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)                 | <span data-ttu-id="7fed7-187">抓取目前具有最大數目的節點。</span><span class="sxs-lookup"><span data-stu-id="7fed7-187">Retrieves the node that currently has the highest number.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="7fed7-188">**GetNumaNodeProcessorMask**</span><span class="sxs-lookup"><span data-stu-id="7fed7-188">**GetNumaNodeProcessorMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)                 | <span data-ttu-id="7fed7-189">已在 Windows 10 組建20348中更新。</span><span class="sxs-lookup"><span data-stu-id="7fed7-189">Updated in Windows 10 Build 20348.</span></span> <span data-ttu-id="7fed7-190">抓取指定節點的處理器遮罩。</span><span class="sxs-lookup"><span data-stu-id="7fed7-190">Retrieves the processor mask for the specified node.</span></span>                                                                                                                                                                            |
| [<span data-ttu-id="7fed7-191">**GetNumaNodeProcessorMask2**</span><span class="sxs-lookup"><span data-stu-id="7fed7-191">**GetNumaNodeProcessorMask2**</span></span>](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormask2)                         | <span data-ttu-id="7fed7-192">Windows 10 組建20348中的新功能。</span><span class="sxs-lookup"><span data-stu-id="7fed7-192">New in Windows 10 Build 20348.</span></span> <span data-ttu-id="7fed7-193">抓取指定之節點的多群組處理器遮罩。</span><span class="sxs-lookup"><span data-stu-id="7fed7-193">Retrieves the multi-group processor mask of the specified node.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="7fed7-194">**GetNumaNodeProcessorMaskEx**</span><span class="sxs-lookup"><span data-stu-id="7fed7-194">**GetNumaNodeProcessorMaskEx**</span></span>](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)             | <span data-ttu-id="7fed7-195">已在 Windows 10 組建20348中更新。</span><span class="sxs-lookup"><span data-stu-id="7fed7-195">Updated in Windows 10 Build 20348.</span></span> <span data-ttu-id="7fed7-196">抓取指定為 **USHORT** 值之節點的處理器遮罩。</span><span class="sxs-lookup"><span data-stu-id="7fed7-196">Retrieves the processor mask for a node specified as a **USHORT** value.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="7fed7-197">**GetNumaProcessorNode**</span><span class="sxs-lookup"><span data-stu-id="7fed7-197">**GetNumaProcessorNode**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                         | <span data-ttu-id="7fed7-198">抓取指定處理器的節點編號。</span><span class="sxs-lookup"><span data-stu-id="7fed7-198">Retrieves the node number for the specified processor.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="7fed7-199">**GetNumaProcessorNodeEx**</span><span class="sxs-lookup"><span data-stu-id="7fed7-199">**GetNumaProcessorNodeEx**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                     | <span data-ttu-id="7fed7-200">以指定處理器的 **USHORT** 值形式抓取節點編號。</span><span class="sxs-lookup"><span data-stu-id="7fed7-200">Retrieves the node number as a **USHORT** value for the specified processor.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="7fed7-201">**GetNumaProximityNode**</span><span class="sxs-lookup"><span data-stu-id="7fed7-201">**GetNumaProximityNode**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                         | <span data-ttu-id="7fed7-202">抓取指定的相近識別碼的節點編號。</span><span class="sxs-lookup"><span data-stu-id="7fed7-202">Retrieves the node number for the specified proximity identifier.</span></span>                                                                                                                                                               |
| [<span data-ttu-id="7fed7-203">**GetNumaProximityNodeEx**</span><span class="sxs-lookup"><span data-stu-id="7fed7-203">**GetNumaProximityNodeEx**</span></span>](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                     | <span data-ttu-id="7fed7-204">將節點編號抓取為指定之相近識別碼的 **USHORT** 值。</span><span class="sxs-lookup"><span data-stu-id="7fed7-204">Retrieves the node number as a **USHORT** value for the specified proximity identifier.</span></span>                                                                                                                                         |
| [<span data-ttu-id="7fed7-205">**GetProcessDefaultCpuSetMasks**</span><span class="sxs-lookup"><span data-stu-id="7fed7-205">**GetProcessDefaultCpuSetMasks**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessdefaultcpusetmasks)                     | <span data-ttu-id="7fed7-206">Windows 10 組建20348中的新功能。</span><span class="sxs-lookup"><span data-stu-id="7fed7-206">New in Windows 10 Build 20348.</span></span> <span data-ttu-id="7fed7-207">抓取 SetProcessDefaultCpuSetMasks 或 SetProcessDefaultCpuSets 所設定之進程預設集中的 CPU 集合清單。</span><span class="sxs-lookup"><span data-stu-id="7fed7-207">Retrieves the list of CPU Sets in the process default set that was set by SetProcessDefaultCpuSetMasks or SetProcessDefaultCpuSets.</span></span>                                                                                                                                         |
| [<span data-ttu-id="7fed7-208">**GetThreadSelectedCpuSetMasks**</span><span class="sxs-lookup"><span data-stu-id="7fed7-208">**GetThreadSelectedCpuSetMasks**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadselectedcpusetmasks)                     | <span data-ttu-id="7fed7-209">Windows 10 組建20348中的新功能。</span><span class="sxs-lookup"><span data-stu-id="7fed7-209">New in Windows 10 Build 20348.</span></span> <span data-ttu-id="7fed7-210">為指定的執行緒設定選取的 CPU 集合指派。</span><span class="sxs-lookup"><span data-stu-id="7fed7-210">Sets the selected CPU Sets assignment for the specified thread.</span></span> <span data-ttu-id="7fed7-211">此指派會覆寫進程預設指派（如果有設定）。</span><span class="sxs-lookup"><span data-stu-id="7fed7-211">This assignment overrides the process default assignment, if one is set.</span></span>                                                                                                                                          |
| [<span data-ttu-id="7fed7-212">**MapViewOfFileExNuma**</span><span class="sxs-lookup"><span data-stu-id="7fed7-212">**MapViewOfFileExNuma**</span></span>](/windows/win32/api/winbase/nf-winbase-mapviewoffileexnuma)                          | <span data-ttu-id="7fed7-213">將檔案對應的視圖對應至呼叫進程的位址空間，並為實體記憶體指定 NUMA 節點。</span><span class="sxs-lookup"><span data-stu-id="7fed7-213">Maps a view of a file mapping into the address space of a calling process, and specifies the NUMA node for the physical memory.</span></span>                                                                                                 |
| [<span data-ttu-id="7fed7-214">**SetProcessDefaultCpuSetMasks**</span><span class="sxs-lookup"><span data-stu-id="7fed7-214">**SetProcessDefaultCpuSetMasks**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessdefaultcpusetmasks)                     | <span data-ttu-id="7fed7-215">Windows 10 組建20348中的新功能。</span><span class="sxs-lookup"><span data-stu-id="7fed7-215">New in Windows 10 Build 20348.</span></span> <span data-ttu-id="7fed7-216">針對指定進程中的執行緒，設定預設的 CPU 集合指派。</span><span class="sxs-lookup"><span data-stu-id="7fed7-216">Sets the default CPU Sets assignment for threads in the specified process.</span></span>                                                                                                                                          |
| [<span data-ttu-id="7fed7-217">**SetThreadSelectedCpuSetMasks**</span><span class="sxs-lookup"><span data-stu-id="7fed7-217">**SetThreadSelectedCpuSetMasks**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadselectedcpusetmasks)                     | <span data-ttu-id="7fed7-218">Windows 10 組建20348中的新功能。</span><span class="sxs-lookup"><span data-stu-id="7fed7-218">New in Windows 10 Build 20348.</span></span> <span data-ttu-id="7fed7-219">為指定的執行緒設定選取的 CPU 集合指派。</span><span class="sxs-lookup"><span data-stu-id="7fed7-219">Sets the selected CPU Sets assignment for the specified thread.</span></span> <span data-ttu-id="7fed7-220">此指派會覆寫進程預設指派（如果有設定）。</span><span class="sxs-lookup"><span data-stu-id="7fed7-220">This assignment overrides the process default assignment, if one is set.</span></span>                                                                                                                                          |
| [<span data-ttu-id="7fed7-221">**VirtualAllocExNuma**</span><span class="sxs-lookup"><span data-stu-id="7fed7-221">**VirtualAllocExNuma**</span></span>](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                            | <span data-ttu-id="7fed7-222">保留或認可指定進程的虛擬位址空間內的記憶體區域，並指定實體記憶體的 NUMA 節點。</span><span class="sxs-lookup"><span data-stu-id="7fed7-222">Reserves or commits a region of memory within the virtual address space of the specified process, and specifies the NUMA node for the physical memory.</span></span>                                                                          |



 

<span data-ttu-id="7fed7-223">[**QueryWorkingSetEx**](/windows/win32/api/psapi/nf-psapi-queryworkingsetex)函式可用來取出配置頁面的 NUMA 節點。</span><span class="sxs-lookup"><span data-stu-id="7fed7-223">The [**QueryWorkingSetEx**](/windows/win32/api/psapi/nf-psapi-queryworkingsetex) function can be used to retrieve the NUMA node on which a page is allocated.</span></span> <span data-ttu-id="7fed7-224">如需範例，請參閱 [從 NUMA 節點配置記憶體](../memory/allocating-memory-from-a-numa-node.md)。</span><span class="sxs-lookup"><span data-stu-id="7fed7-224">For an example, see [Allocating Memory from a NUMA Node](../memory/allocating-memory-from-a-numa-node.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fed7-225">相關主題</span><span class="sxs-lookup"><span data-stu-id="7fed7-225">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fed7-226">從 NUMA 節點配置記憶體</span><span class="sxs-lookup"><span data-stu-id="7fed7-226">Allocating Memory from a NUMA Node</span></span>](../memory/allocating-memory-from-a-numa-node.md)
</dt> <dt>

[<span data-ttu-id="7fed7-227">多個處理器</span><span class="sxs-lookup"><span data-stu-id="7fed7-227">Multiple Processors</span></span>](multiple-processors.md)
</dt> <dt>

[<span data-ttu-id="7fed7-228">處理器群組</span><span class="sxs-lookup"><span data-stu-id="7fed7-228">Processor Groups</span></span>](processor-groups.md)
</dt> </dl>

 

 
