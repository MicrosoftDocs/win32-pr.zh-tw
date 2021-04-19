---
description: 虛擬記憶體函數可讓進程操作或判斷頁面在其虛擬位址空間中的狀態。
ms.assetid: 9488a854-1ef0-488f-b3d1-57c1acb82a88
title: 虛擬記憶體函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c76866fd10dac01315622e8a4faef7bea436a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970232"
---
# <a name="virtual-memory-functions"></a><span data-ttu-id="51ca3-103">虛擬記憶體函數</span><span class="sxs-lookup"><span data-stu-id="51ca3-103">Virtual Memory Functions</span></span>

<span data-ttu-id="51ca3-104">虛擬記憶體函數可讓進程操作或判斷頁面在其虛擬位址空間中的狀態。</span><span class="sxs-lookup"><span data-stu-id="51ca3-104">The virtual memory functions enable a process to manipulate or determine the status of pages in its virtual address space.</span></span> <span data-ttu-id="51ca3-105">他們可以執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="51ca3-105">They can perform the following operations:</span></span>

-   <span data-ttu-id="51ca3-106">保留進程的虛擬位址空間範圍。</span><span class="sxs-lookup"><span data-stu-id="51ca3-106">Reserve a range of a process's virtual address space.</span></span> <span data-ttu-id="51ca3-107">保留位址空間不會配置任何實體儲存體，但會防止其他配置作業使用指定的範圍。</span><span class="sxs-lookup"><span data-stu-id="51ca3-107">Reserving address space does not allocate any physical storage, but it prevents other allocation operations from using the specified range.</span></span> <span data-ttu-id="51ca3-108">它不會影響其他進程的虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="51ca3-108">It does not affect the virtual address spaces of other processes.</span></span> <span data-ttu-id="51ca3-109">保留頁面可避免不必要的實體儲存空間耗用量，同時讓進程能夠保留動態資料結構可以成長的範圍。</span><span class="sxs-lookup"><span data-stu-id="51ca3-109">Reserving pages prevents needless consumption of physical storage, while enabling a process to reserve a range of its address space into which a dynamic data structure can grow.</span></span> <span data-ttu-id="51ca3-110">此程式可以視需要配置此空間的實體儲存體。</span><span class="sxs-lookup"><span data-stu-id="51ca3-110">The process can allocate physical storage for this space, as needed.</span></span>
-   <span data-ttu-id="51ca3-111">在進程的虛擬位址空間中認可一系列的保留頁面，讓實體儲存體 (在 RAM 或磁片) 只能供配置的進程存取。</span><span class="sxs-lookup"><span data-stu-id="51ca3-111">Commit a range of reserved pages in a process's virtual address space so that physical storage (either in RAM or on disk) is accessible only to the allocating process.</span></span>
-   <span data-ttu-id="51ca3-112">針對某個範圍的認可頁面指定讀取/寫入、唯讀或無存取權。</span><span class="sxs-lookup"><span data-stu-id="51ca3-112">Specify read/write, read-only, or no access for a range of committed pages.</span></span> <span data-ttu-id="51ca3-113">這不同于一律以讀取/寫入存取權配置頁面的標準配置函數。</span><span class="sxs-lookup"><span data-stu-id="51ca3-113">This differs from the standard allocation functions that always allocate pages with read/write access.</span></span>
-   <span data-ttu-id="51ca3-114">釋放一系列的保留頁面，讓呼叫進程可使用虛擬位址的範圍來進行後續的配置作業。</span><span class="sxs-lookup"><span data-stu-id="51ca3-114">Free a range of reserved pages, making the range of virtual addresses available for subsequent allocation operations by the calling process.</span></span>
-   <span data-ttu-id="51ca3-115">取消認可一系列已認可的頁面，釋出其實體儲存體，並讓它可供任何程式進行後續的配置。</span><span class="sxs-lookup"><span data-stu-id="51ca3-115">Decommit a range of committed pages, releasing their physical storage and making it available for subsequent allocation by any process.</span></span>
-   <span data-ttu-id="51ca3-116">將一或多個認可的記憶體頁面鎖定 (RAM) 的實體記憶體，讓系統無法將頁面交換到分頁檔案。</span><span class="sxs-lookup"><span data-stu-id="51ca3-116">Lock one or more pages of committed memory into physical memory (RAM) so that the system cannot swap the pages out to the paging file.</span></span>
-   <span data-ttu-id="51ca3-117">取得呼叫進程之虛擬位址空間中的頁面範圍或指定進程的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="51ca3-117">Obtain information about a range of pages in the virtual address space of the calling process or a specified process.</span></span>
-   <span data-ttu-id="51ca3-118">在呼叫進程的虛擬位址空間或指定進程的虛擬位址空間中，為指定的認可頁面範圍變更存取保護。</span><span class="sxs-lookup"><span data-stu-id="51ca3-118">Change the access protection for a specified range of committed pages in the virtual address space of the calling process or a specified process.</span></span>

<span data-ttu-id="51ca3-119">如需詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="51ca3-119">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="51ca3-120">配置虛擬記憶體</span><span class="sxs-lookup"><span data-stu-id="51ca3-120">Allocating Virtual Memory</span></span>](allocating-virtual-memory.md)
-   [<span data-ttu-id="51ca3-121">比較記憶體配置方法</span><span class="sxs-lookup"><span data-stu-id="51ca3-121">Comparing Memory Allocation Methods</span></span>](comparing-memory-allocation-methods.md)
-   [<span data-ttu-id="51ca3-122">釋放虛擬記憶體</span><span class="sxs-lookup"><span data-stu-id="51ca3-122">Freeing Virtual Memory</span></span>](freeing-virtual-memory.md)
-   [<span data-ttu-id="51ca3-123">使用頁面</span><span class="sxs-lookup"><span data-stu-id="51ca3-123">Working With Pages</span></span>](working-with-pages.md)
-   [<span data-ttu-id="51ca3-124">記憶體管理函數</span><span class="sxs-lookup"><span data-stu-id="51ca3-124">Memory Management Functions</span></span>](memory-management-functions.md)

 

 



