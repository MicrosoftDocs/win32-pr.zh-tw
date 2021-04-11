---
description: 下列結構適用于記憶體管理：
ms.assetid: 02a2a874-9ced-4b7d-8aad-4a7768639a32
title: 記憶體管理結構
ms.topic: article
ms.date: 11/06/2018
ms.openlocfilehash: dc9f2837941c26f0ff9fed5b7d65a00f6bd254a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945418"
---
# <a name="memory-management-structures"></a><span data-ttu-id="cf206-103">記憶體管理結構</span><span class="sxs-lookup"><span data-stu-id="cf206-103">Memory Management Structures</span></span>

<span data-ttu-id="cf206-104">下列結構適用于記憶體管理。</span><span class="sxs-lookup"><span data-stu-id="cf206-104">The following structures are used with memory management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cf206-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="cf206-105">In this section</span></span>

| <span data-ttu-id="cf206-106">主題</span><span class="sxs-lookup"><span data-stu-id="cf206-106">Topic</span></span> | <span data-ttu-id="cf206-107">描述</span><span class="sxs-lookup"><span data-stu-id="cf206-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="cf206-108">**CFG \_ 呼叫 \_ 目標 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="cf206-108">**CFG\_CALL\_TARGET\_INFO**</span></span>](-cfg-call-target-info.md) | <span data-ttu-id="cf206-109">代表控制流程防護 (CFG) 的呼叫目標相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cf206-109">Represents information about call targets for Control Flow Guard (CFG).</span></span> |
| [<span data-ttu-id="cf206-110">**堆積 \_ 將 \_ 資源 \_ 資訊優化**</span><span class="sxs-lookup"><span data-stu-id="cf206-110">**HEAP\_OPTIMIZE\_RESOURCES\_INFORMATION**</span></span>](/windows/desktop/api/winnt/ns-winnt-heap_optimize_resources_information) | <span data-ttu-id="cf206-111">指定以 [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation)起始之 HeapOptimizeResources 作業的旗標。</span><span class="sxs-lookup"><span data-stu-id="cf206-111">Specifies flags for a HeapOptimizeResources operation initiated with [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation).</span></span> |
| [<span data-ttu-id="cf206-112">**記憶體 \_ 位址 \_ 需求**</span><span class="sxs-lookup"><span data-stu-id="cf206-112">**MEM\_ADDRESS\_REQUIREMENTS**</span></span>](/windows/desktop/api/winnt/ns-winnt-mem_address_requirements) | <span data-ttu-id="cf206-113">針對管理虛擬記憶體的函式，指定最低和最高的基底位址和對齊方式作為擴充參數的一部分。</span><span class="sxs-lookup"><span data-stu-id="cf206-113">Specifies a lowest and highest base address and alignment as part of an extended parameter to a function that manages virtual memory..</span></span> |
| [<span data-ttu-id="cf206-114">**記憶體 \_ 擴充 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="cf206-114">**MEM\_EXTENDED\_PARAMETER**</span></span>](/windows/desktop/api/winnt/ns-winnt-mem_extended_parameter) | <span data-ttu-id="cf206-115">表示管理虛擬記憶體之函式的擴充參數。</span><span class="sxs-lookup"><span data-stu-id="cf206-115">Represents an extended parameter for a function that manages virtual memory.</span></span> |
| [<span data-ttu-id="cf206-116">**記憶體 \_ 基本 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="cf206-116">**MEMORY\_BASIC\_INFORMATION**</span></span>](/windows/desktop/api/winnt/ns-winnt-memory_basic_information) | <span data-ttu-id="cf206-117">包含處理常式虛擬位址空間中某個頁面範圍的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cf206-117">Contains information about a range of pages in the virtual address space of a process.</span></span> |
| [<span data-ttu-id="cf206-118">**MEMORYSTATUS**</span><span class="sxs-lookup"><span data-stu-id="cf206-118">**MEMORYSTATUS**</span></span>](/windows/desktop/api/WinBase/ns-winbase-memorystatus) | <span data-ttu-id="cf206-119">包含實體和虛擬記憶體目前狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cf206-119">Contains information about the current state of both physical and virtual memory.</span></span> |
| [<span data-ttu-id="cf206-120">**MEMORYSTATUSEX**</span><span class="sxs-lookup"><span data-stu-id="cf206-120">**MEMORYSTATUSEX**</span></span>](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-memorystatusex) | <span data-ttu-id="cf206-121">包含實體和虛擬記憶體（包括延伸記憶體）目前狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cf206-121">Contains information about the current state of both physical and virtual memory, including extended memory.</span></span> |
| [<span data-ttu-id="cf206-122">**進程 \_ 堆積 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="cf206-122">**PROCESS\_HEAP\_ENTRY**</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-process_heap_entry) | <span data-ttu-id="cf206-123">包含堆積元素的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cf206-123">Contains information about a heap element.</span></span> |
| [<span data-ttu-id="cf206-124">**WIN32 \_ 記憶體 \_ 範圍 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="cf206-124">**WIN32\_MEMORY\_RANGE\_ENTRY**</span></span>](/windows/desktop/api/memoryapi/ns-memoryapi-win32_memory_range_entry) | <span data-ttu-id="cf206-125">指定記憶體的範圍。</span><span class="sxs-lookup"><span data-stu-id="cf206-125">Specifies a range of memory.</span></span> |
| [<span data-ttu-id="cf206-126">**WIN32 \_ 記憶體 \_ 區域 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="cf206-126">**WIN32\_MEMORY\_REGION\_INFORMATION**</span></span>](/windows/desktop/api/memoryapi/ns-memoryapi-win32_memory_region_information) | <span data-ttu-id="cf206-127">包含記憶體區域的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cf206-127">Contains information about a memory region.</span></span> |
| <span data-ttu-id="cf206-128">[**AtlThunkData \_ t**](/previous-versions/windows/desktop/legacy/mt805050(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cf206-128">[**AtlThunkData\_t**](/previous-versions/windows/desktop/legacy/mt805050(v=vs.85))</span></span> | <span data-ttu-id="cf206-129">表示 ATL Thunk 的不透明資料結構。</span><span class="sxs-lookup"><span data-stu-id="cf206-129">An opaque data structure that represents an ATL thunk.</span></span> |
