---
description: 進程的虛擬位址空間是一組可用的虛擬記憶體位址。 每個進程的位址空間都是私用的，除非共用，否則無法由其他進程存取。
ms.assetid: 747f9f53-a595-4f4b-8b81-3123d59edb2f
title: '虛擬位址空間 (記憶體管理) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6584d0404799e6b0e5ab343c7d8b39d7f8d741a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943579"
---
# <a name="virtual-address-space-memory-management"></a><span data-ttu-id="59fdd-104">虛擬位址空間 (記憶體管理) </span><span class="sxs-lookup"><span data-stu-id="59fdd-104">Virtual Address Space (Memory Management)</span></span>

<span data-ttu-id="59fdd-105">進程的虛擬位址空間是一組可用的虛擬記憶體位址。</span><span class="sxs-lookup"><span data-stu-id="59fdd-105">The virtual address space for a process is the set of virtual memory addresses that it can use.</span></span> <span data-ttu-id="59fdd-106">每個進程的位址空間都是私用的，除非共用，否則無法由其他進程存取。</span><span class="sxs-lookup"><span data-stu-id="59fdd-106">The address space for each process is private and cannot be accessed by other processes unless it is shared.</span></span>

<span data-ttu-id="59fdd-107">虛擬位址不代表物件在記憶體中的實際實體位置;相反地，系統會維護每個進程的 *頁面表格* ，這是用來將虛擬位址轉譯成其對應實體位址的內部資料結構。</span><span class="sxs-lookup"><span data-stu-id="59fdd-107">A virtual address does not represent the actual physical location of an object in memory; instead, the system maintains a *page table* for each process, which is an internal data structure used to translate virtual addresses into their corresponding physical addresses.</span></span> <span data-ttu-id="59fdd-108">每次執行緒參考位址時，系統會將虛擬位址轉譯為實體位址。</span><span class="sxs-lookup"><span data-stu-id="59fdd-108">Each time a thread references an address, the system translates the virtual address to a physical address.</span></span>

<span data-ttu-id="59fdd-109">32位 Windows 的虛擬位址空間的大小為 4 gb (GB) 並分為兩個磁碟分割：一個供進程使用，另一個則保留供系統使用。</span><span class="sxs-lookup"><span data-stu-id="59fdd-109">The virtual address space for 32-bit Windows is 4 gigabytes (GB) in size and divided into two partitions: one for use by the process and the other reserved for use by the system.</span></span> <span data-ttu-id="59fdd-110">如需64位 Windows 中虛擬位址空間的詳細資訊，請參閱 [64 位 windows 中的虛擬位址空間](../winprog64/virtual-address-space.md)。</span><span class="sxs-lookup"><span data-stu-id="59fdd-110">For more information about the virtual address space in 64-bit Windows, see [Virtual Address Space in 64-bit Windows](../winprog64/virtual-address-space.md).</span></span>

<span data-ttu-id="59fdd-111">如需虛擬記憶體的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="59fdd-111">For more information about virtual memory, see the following topics:</span></span>

-   [<span data-ttu-id="59fdd-112">虛擬位址空間和實體儲存體</span><span class="sxs-lookup"><span data-stu-id="59fdd-112">Virtual Address Space and Physical Storage</span></span>](virtual-address-space-and-physical-storage.md)
-   [<span data-ttu-id="59fdd-113">工作集</span><span class="sxs-lookup"><span data-stu-id="59fdd-113">Working Set</span></span>](working-set.md)
-   [<span data-ttu-id="59fdd-114">頁面狀態</span><span class="sxs-lookup"><span data-stu-id="59fdd-114">Page State</span></span>](page-state.md)
-   [<span data-ttu-id="59fdd-115">配置的記憶體範圍</span><span class="sxs-lookup"><span data-stu-id="59fdd-115">Scope of Allocated Memory</span></span>](scope-of-allocated-memory.md)
-   [<span data-ttu-id="59fdd-116">資料執行防止</span><span class="sxs-lookup"><span data-stu-id="59fdd-116">Data Execution Prevention</span></span>](data-execution-prevention.md)
-   [<span data-ttu-id="59fdd-117">記憶體保護</span><span class="sxs-lookup"><span data-stu-id="59fdd-117">Memory Protection</span></span>](memory-protection.md)
-   [<span data-ttu-id="59fdd-118">Windows 版本的記憶體限制</span><span class="sxs-lookup"><span data-stu-id="59fdd-118">Memory Limits for Windows Releases</span></span>](memory-limits-for-windows-releases.md)

## <a name="default-virtual-address-space-for-32-bit-windows"></a><span data-ttu-id="59fdd-119">32位 Windows 的預設虛擬位址空間</span><span class="sxs-lookup"><span data-stu-id="59fdd-119">Default Virtual Address Space for 32-bit Windows</span></span>

<span data-ttu-id="59fdd-120">下表顯示每個資料分割的預設記憶體範圍。</span><span class="sxs-lookup"><span data-stu-id="59fdd-120">The following table shows the default memory range for each partition.</span></span>



| <span data-ttu-id="59fdd-121">記憶體範圍</span><span class="sxs-lookup"><span data-stu-id="59fdd-121">Memory range</span></span>                             | <span data-ttu-id="59fdd-122">使用方式</span><span class="sxs-lookup"><span data-stu-id="59fdd-122">Usage</span></span>                |
|------------------------------------------|----------------------|
| <span data-ttu-id="59fdd-123">低 2GB (0x00000000 至 0x7FFFFFFF) </span><span class="sxs-lookup"><span data-stu-id="59fdd-123">Low 2GB (0x00000000 through 0x7FFFFFFF)</span></span>  | <span data-ttu-id="59fdd-124">由進程使用。</span><span class="sxs-lookup"><span data-stu-id="59fdd-124">Used by the process.</span></span> |
| <span data-ttu-id="59fdd-125">高 2GB (0x80000000 到 0xFFFFFFFF) </span><span class="sxs-lookup"><span data-stu-id="59fdd-125">High 2GB (0x80000000 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="59fdd-126">供系統使用。</span><span class="sxs-lookup"><span data-stu-id="59fdd-126">Used by the system.</span></span>  |



 

## <a name="virtual-address-space-for-32-bit-windows-with-4gt"></a><span data-ttu-id="59fdd-127">32位 Windows 與4GT 的虛擬位址空間</span><span class="sxs-lookup"><span data-stu-id="59fdd-127">Virtual Address Space for 32-bit Windows with 4GT</span></span>

<span data-ttu-id="59fdd-128">如果已啟用 [4 gb 調整](4-gigabyte-tuning.md) (4gt) ，則每個分割區的記憶體範圍如下所示。</span><span class="sxs-lookup"><span data-stu-id="59fdd-128">If [4-gigabyte tuning](4-gigabyte-tuning.md) (4GT) is enabled, the memory range for each partition is as follows.</span></span>



| <span data-ttu-id="59fdd-129">記憶體範圍</span><span class="sxs-lookup"><span data-stu-id="59fdd-129">Memory range</span></span>                             | <span data-ttu-id="59fdd-130">使用方式</span><span class="sxs-lookup"><span data-stu-id="59fdd-130">Usage</span></span>                |
|------------------------------------------|----------------------|
| <span data-ttu-id="59fdd-131">低 3GB (0x00000000 至 0xBFFFFFFF) </span><span class="sxs-lookup"><span data-stu-id="59fdd-131">Low 3GB (0x00000000 through 0xBFFFFFFF)</span></span>  | <span data-ttu-id="59fdd-132">由進程使用。</span><span class="sxs-lookup"><span data-stu-id="59fdd-132">Used by the process.</span></span> |
| <span data-ttu-id="59fdd-133">高 1GB (透過 0xFFFFFFFF) 0xC0000000</span><span class="sxs-lookup"><span data-stu-id="59fdd-133">High 1GB (0xC0000000 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="59fdd-134">供系統使用。</span><span class="sxs-lookup"><span data-stu-id="59fdd-134">Used by the system.</span></span>  |



 

<span data-ttu-id="59fdd-135">啟用4GT 之後，在其映射標頭中設定 [**圖像 \_ 檔案 \_ 大型 \_ 位址 \_ 感知**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) 旗標的進程，將可存取超過 2 gb 以上的額外 1 GB 記憶體。</span><span class="sxs-lookup"><span data-stu-id="59fdd-135">After 4GT is enabled, a process that has the [**IMAGE\_FILE\_LARGE\_ADDRESS\_AWARE**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) flag set in its image header will have access to the additional 1 GB of memory above the low 2 GB.</span></span>

## <a name="adjusting-the-virtual-address-space-for-32-bit-windows"></a><span data-ttu-id="59fdd-136">調整32位 Windows 的虛擬位址空間</span><span class="sxs-lookup"><span data-stu-id="59fdd-136">Adjusting the Virtual Address Space for 32-bit Windows</span></span>

<span data-ttu-id="59fdd-137">您可以使用下列命令來設定開機專案選項，將可供進程使用的磁碟分割大小設定為介於 2048 (2 GB) 和 3072 (3 GB) 之間的值：</span><span class="sxs-lookup"><span data-stu-id="59fdd-137">You can use the following command to set a boot entry option that configures the size of the partition that is available for use by the process to a value between 2048 (2 GB) and 3072 (3 GB):</span></span>

<span data-ttu-id="59fdd-138">[BCDEdit/set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *mb*</span><span class="sxs-lookup"><span data-stu-id="59fdd-138">[BCDEdit /set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *Megabytes*</span></span>

<span data-ttu-id="59fdd-139">在設定開機專案選項之後，每個分割區的記憶體範圍如下所示。</span><span class="sxs-lookup"><span data-stu-id="59fdd-139">After the boot entry option is set, the memory range for each partition is as follows.</span></span>



| <span data-ttu-id="59fdd-140">記憶體範圍</span><span class="sxs-lookup"><span data-stu-id="59fdd-140">Memory range</span></span>                            | <span data-ttu-id="59fdd-141">使用方式</span><span class="sxs-lookup"><span data-stu-id="59fdd-141">Usage</span></span>                |
|-----------------------------------------|----------------------|
| <span data-ttu-id="59fdd-142">低 (0x00000000 至 *mb*) </span><span class="sxs-lookup"><span data-stu-id="59fdd-142">Low (0x00000000 through *Megabytes*)</span></span>    | <span data-ttu-id="59fdd-143">由進程使用。</span><span class="sxs-lookup"><span data-stu-id="59fdd-143">Used by the process.</span></span> |
| <span data-ttu-id="59fdd-144">高 (*mb*+ 1 到 0xffffffff) </span><span class="sxs-lookup"><span data-stu-id="59fdd-144">High (*Megabytes*+1 through 0xFFFFFFFF)</span></span> | <span data-ttu-id="59fdd-145">供系統使用。</span><span class="sxs-lookup"><span data-stu-id="59fdd-145">Used by the system.</span></span>  |



 

<span data-ttu-id="59fdd-146">**Windows Server 2003：** 將 boot.ini 中的 **/USERVA** 參數設定為介於2048到3072之間的值。</span><span class="sxs-lookup"><span data-stu-id="59fdd-146">**Windows Server 2003:** Set the **/USERVA** switch in boot.ini to a value between 2048 and 3072.</span></span>

 

 
