---
description: 記憶體管理員會建立下列記憶體集區，供系統用來配置記憶體：非分頁集區和分頁集區。
ms.assetid: 68ee9c72-f3a3-4f1f-a827-ed4210a665e4
title: 記憶體集區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60987b43347e55d8ee2d01672dbb8173ffc8dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992187"
---
# <a name="memory-pools"></a><span data-ttu-id="a1aa2-103">記憶體集區</span><span class="sxs-lookup"><span data-stu-id="a1aa2-103">Memory Pools</span></span>

<span data-ttu-id="a1aa2-104">記憶體管理員會建立下列記憶體集區，供系統用來配置記憶體：非分頁集區和分頁集區。</span><span class="sxs-lookup"><span data-stu-id="a1aa2-104">The memory manager creates the following memory pools that the system uses to allocate memory: nonpaged pool and paged pool.</span></span> <span data-ttu-id="a1aa2-105">這兩個記憶體集區都位於為系統保留的位址空間區域中，並對應至每個進程的虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="a1aa2-105">Both memory pools are located in the region of the address space that is reserved for the system and mapped into the virtual address space of each process.</span></span> <span data-ttu-id="a1aa2-106">非分頁集區包含保證存在於實體記憶體中的虛擬記憶體位址（只要配置了對應的核心物件）。</span><span class="sxs-lookup"><span data-stu-id="a1aa2-106">The nonpaged pool consists of virtual memory addresses that are guaranteed to reside in physical memory as long as the corresponding kernel objects are allocated.</span></span> <span data-ttu-id="a1aa2-107">分頁集區是由可在系統中傳入和傳出的虛擬記憶體所組成。</span><span class="sxs-lookup"><span data-stu-id="a1aa2-107">The paged pool consists of virtual memory that can be paged in and out of the system.</span></span> <span data-ttu-id="a1aa2-108">為了改善效能，具有單處理器的系統有三個分頁集區，而多處理器系統有五個分頁集區。</span><span class="sxs-lookup"><span data-stu-id="a1aa2-108">To improve performance, systems with a single processor have three paged pools, and multiprocessor systems have five paged pools.</span></span>

<span data-ttu-id="a1aa2-109">[核心物件](../sysinfo/kernel-objects.md)的控制碼會儲存在分頁集區中，因此您可以建立的控制碼數目是以可用的記憶體為基礎。</span><span class="sxs-lookup"><span data-stu-id="a1aa2-109">The handles for [kernel objects](../sysinfo/kernel-objects.md) are stored in the paged pool, so the number of handles you can create is based on available memory.</span></span>

<span data-ttu-id="a1aa2-110">系統會記錄其非分頁集區、分頁集區和分頁檔案使用方式的限制和目前值。</span><span class="sxs-lookup"><span data-stu-id="a1aa2-110">The system records the limits and current values for its nonpaged pool, paged pool, and page file usage.</span></span> <span data-ttu-id="a1aa2-111">如需詳細資訊，請參閱 [記憶體效能資訊](memory-performance-information.md)。</span><span class="sxs-lookup"><span data-stu-id="a1aa2-111">For more information, see [Memory Performance Information](memory-performance-information.md).</span></span>

 

 
