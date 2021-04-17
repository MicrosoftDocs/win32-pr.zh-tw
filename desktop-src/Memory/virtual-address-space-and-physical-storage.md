---
description: Microsoft Windows 支援的實體記憶體最大數量，範圍從 2 GB 到 2 TB，視 Windows 版本而定。
ms.assetid: 5e8fca7a-b85f-4bbd-80c1-e580a815fdce
title: 虛擬位址空間和實體儲存體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d36445eb2639cbfc4db2a6e4abaf28b9af87cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513253"
---
# <a name="virtual-address-space-and-physical-storage"></a><span data-ttu-id="78d57-103">虛擬位址空間和實體儲存體</span><span class="sxs-lookup"><span data-stu-id="78d57-103">Virtual Address Space and Physical Storage</span></span>

<span data-ttu-id="78d57-104">Microsoft Windows 支援的實體記憶體最大數量，範圍從 2 GB 到 24 TB，視 Windows 版本而定。</span><span class="sxs-lookup"><span data-stu-id="78d57-104">The maximum amount of physical memory supported by Microsoft Windows ranges from 2 GB to 24 TB, depending on the version of Windows.</span></span> <span data-ttu-id="78d57-105">如需詳細資訊，請參閱 [Windows 版本的記憶體限制](memory-limits-for-windows-releases.md)。</span><span class="sxs-lookup"><span data-stu-id="78d57-105">For more information, see [Memory Limits for Windows Releases](memory-limits-for-windows-releases.md).</span></span> <span data-ttu-id="78d57-106">每個進程的虛擬位址空間可小於或大於電腦上可用的實體記憶體總數。</span><span class="sxs-lookup"><span data-stu-id="78d57-106">The virtual address space of each process can be smaller or larger than the total physical memory available on the computer.</span></span> <span data-ttu-id="78d57-107">位於實體記憶體之進程的虛擬位址空間子集，稱為 *工作集*。</span><span class="sxs-lookup"><span data-stu-id="78d57-107">The subset of the virtual address space of a process that resides in physical memory is known as the *working set*.</span></span> <span data-ttu-id="78d57-108">如果進程的執行緒嘗試使用的實體記憶體多於目前可用的實體記憶體，系統會將一些記憶體內容分頁至磁片。</span><span class="sxs-lookup"><span data-stu-id="78d57-108">If the threads of a process attempt to use more physical memory than is currently available, the system pages some of the memory contents to disk.</span></span> <span data-ttu-id="78d57-109">進程可用的虛擬位址空間總數量受限於可供分頁檔使用的實體記憶體和可用磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="78d57-109">The total amount of virtual address space available to a process is limited by physical memory and the free space on disk available for the paging file.</span></span>

<span data-ttu-id="78d57-110">實體儲存體和每個進程的虛擬位址空間會組織成 *頁面*（記憶體單位），其大小取決於主機電腦。</span><span class="sxs-lookup"><span data-stu-id="78d57-110">Physical storage and the virtual address space of each process are organized into *pages*, units of memory, whose size depends on the host computer.</span></span> <span data-ttu-id="78d57-111">例如，在 x86 電腦上，主機頁面大小為 4 kb。</span><span class="sxs-lookup"><span data-stu-id="78d57-111">For example, on x86 computers the host page size is 4 kilobytes.</span></span>

<span data-ttu-id="78d57-112">為了充分發揮其管理記憶體的彈性，系統可以將實體記憶體的頁面移入和移出磁片上的分頁檔。</span><span class="sxs-lookup"><span data-stu-id="78d57-112">To maximize its flexibility in managing memory, the system can move pages of physical memory to and from a paging file on disk.</span></span> <span data-ttu-id="78d57-113">當頁面在實體記憶體中移動時，系統會更新受影響之進程的頁面對應。</span><span class="sxs-lookup"><span data-stu-id="78d57-113">When a page is moved in physical memory, the system updates the page maps of the affected processes.</span></span> <span data-ttu-id="78d57-114">當系統需要實體記憶體中的空間時，會將最近使用的實體記憶體分頁移至分頁檔案。</span><span class="sxs-lookup"><span data-stu-id="78d57-114">When the system needs space in physical memory, it moves the least recently used pages of physical memory to the paging file.</span></span> <span data-ttu-id="78d57-115">系統對實體記憶體的操作對應用程式而言是完全透明的，只會在其虛擬位址空間中操作。</span><span class="sxs-lookup"><span data-stu-id="78d57-115">Manipulation of physical memory by the system is completely transparent to applications, which operate only in their virtual address spaces.</span></span>

 

 



