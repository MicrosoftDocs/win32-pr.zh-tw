---
description: 實體位址延伸 (PAE) 是一種處理器功能，可讓 x86 處理器存取超過 4 GB 的可用 Windows 版本實體記憶體。
ms.assetid: 1aec2414-cc93-4a86-955d-2433360c9125
title: 實體位址擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd313c1025eaaf4859436aebef90288c6d3fe49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027571"
---
# <a name="physical-address-extension"></a><span data-ttu-id="1ebfc-103">實體位址擴充功能</span><span class="sxs-lookup"><span data-stu-id="1ebfc-103">Physical Address Extension</span></span>

<span data-ttu-id="1ebfc-104">實體位址延伸 (PAE) 是一種處理器功能，可讓 x86 處理器存取超過 4 GB 的可用 Windows 版本實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-104">Physical Address Extension (PAE) is a processor feature that enables x86 processors to access more than 4 GB of physical memory on capable versions of Windows.</span></span> <span data-ttu-id="1ebfc-105">在 x86 系統上執行的某些32位版本的 Windows Server，可以使用 PAE 來存取高達 64 GB 或 128 GB 的實體記憶體，視處理器的實體位址大小而定。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-105">Certain 32-bit versions of Windows Server running on x86-based systems can use PAE to access up to 64 GB or 128 GB of physical memory, depending on the physical address size of the processor.</span></span> <span data-ttu-id="1ebfc-106">如需詳細資訊，請參閱 [Windows 版本的記憶體限制](memory-limits-for-windows-releases.md)。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-106">For details, see [Memory Limits for Windows Releases](memory-limits-for-windows-releases.md).</span></span>

<span data-ttu-id="1ebfc-107">Intel Itanium 和 x64 處理器架構可以原生存取超過 4 GB 的實體記憶體，因此不會提供對等的 PAE。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-107">The Intel Itanium and x64 processor architectures can access more than 4 GB of physical memory natively and therefore do not provide the equivalent of PAE.</span></span> <span data-ttu-id="1ebfc-108">只有在 x86 系統上執行的32位版本的 Windows 才會使用 PAE。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-108">PAE is used only by 32-bit versions of Windows running on x86-based systems.</span></span>

<span data-ttu-id="1ebfc-109">使用 PAE 時，作業系統會從兩個層級的線性位址轉譯移到三層的位址轉譯。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-109">With PAE, the operating system moves from two-level linear address translation to three-level address translation.</span></span> <span data-ttu-id="1ebfc-110">它不會將線性位址分割成三個不同的欄位來編制記憶體資料表的索引，而是將其分割成四個不同的欄位：2位位欄位、2 9 位位欄位和12位位位，其對應于 Intel 架構 (4 KB) 所執行的頁面大小。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-110">Instead of a linear address being split into three separate fields for indexing into memory tables, it is split into four separate fields: a 2-bit bitfield, two 9-bit bitfields, and a 12-bit bitfield that corresponds to the page size implemented by Intel architecture (4 KB).</span></span> <span data-ttu-id="1ebfc-111">在 PAE 模式下，頁面資料表專案的大小 (Pte) 和 (PDEs) 的頁面目錄專案會從32增加至64位。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-111">The size of page table entries (PTEs) and page directory entries (PDEs) in PAE mode is increased from 32 to 64 bits.</span></span> <span data-ttu-id="1ebfc-112">額外的位可讓作業系統 PTE 或 PDE 參考超過 4 GB 的實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-112">The additional bits allow an operating system PTE or PDE to reference physical memory above 4 GB.</span></span>

<span data-ttu-id="1ebfc-113">在以 x64 為基礎的系統上執行的32位 Windows 中，PAE 也啟用了數種先進的系統和處理器功能，包括支援硬體的 [資料執行防止](data-execution-prevention.md) (DEP) 、 [非統一記憶體存取 (NUMA) ](../procthread/numa-support.md)，以及在執行 (熱新增記憶體) 的情況下，將記憶體新增至系統的功能。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-113">In 32-bit Windows running on x64-based systems, PAE also enables several advanced system and processor features, including hardware-enabled [Data Execution Prevention](data-execution-prevention.md) (DEP), [non-uniform memory access (NUMA)](../procthread/numa-support.md), and the ability to add memory to a system while it is running (hot-add memory).</span></span>

<span data-ttu-id="1ebfc-114">PAE 不會變更進程可用的虛擬位址空間數量。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-114">PAE does not change the amount of virtual address space available to a process.</span></span> <span data-ttu-id="1ebfc-115">在32位視窗中執行的每個進程仍然受限於 4 GB 的虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-115">Each process running in 32-bit Windows is still limited to a 4 GB virtual address space.</span></span>

## <a name="system-support-for-pae"></a><span data-ttu-id="1ebfc-116">適用于 PAE 的系統支援</span><span class="sxs-lookup"><span data-stu-id="1ebfc-116">System Support for PAE</span></span>

<span data-ttu-id="1ebfc-117">只有在下列以 x86 為基礎的系統上執行的 Windows 32 位版本上，才支援 PAE：</span><span class="sxs-lookup"><span data-stu-id="1ebfc-117">PAE is supported only on the following 32-bit versions of Windows running on x86-based systems:</span></span>

-   <span data-ttu-id="1ebfc-118">Windows 7 (僅限32位) </span><span class="sxs-lookup"><span data-stu-id="1ebfc-118">Windows 7 (32 bit only)</span></span>
-   <span data-ttu-id="1ebfc-119">Windows Server 2008 (僅限32位) </span><span class="sxs-lookup"><span data-stu-id="1ebfc-119">Windows Server 2008 (32-bit only)</span></span>
-   <span data-ttu-id="1ebfc-120">Windows Vista (僅限32位) </span><span class="sxs-lookup"><span data-stu-id="1ebfc-120">Windows Vista (32-bit only)</span></span>
-   <span data-ttu-id="1ebfc-121">Windows Server 2003 (僅限32位) </span><span class="sxs-lookup"><span data-stu-id="1ebfc-121">Windows Server 2003 (32-bit only)</span></span>
-   <span data-ttu-id="1ebfc-122">僅限 Windows XP (32 位) </span><span class="sxs-lookup"><span data-stu-id="1ebfc-122">Windows XP (32-bit only)</span></span>

## <a name="enabling-pae"></a><span data-ttu-id="1ebfc-123">啟用 PAE</span><span class="sxs-lookup"><span data-stu-id="1ebfc-123">Enabling PAE</span></span>

<span data-ttu-id="1ebfc-124">如果已在支援啟用硬體 DEP 的電腦上啟用 DEP，或電腦已設定為在超過 4 GB 的記憶體範圍內熱新增記憶體裝置，則 Windows 會自動啟用 PAE。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-124">Windows automatically enables PAE if DEP is enabled on a computer that supports hardware-enabled DEP, or if the computer is configured for hot-add memory devices in memory ranges beyond 4 GB.</span></span> <span data-ttu-id="1ebfc-125">如果電腦不支援已啟用硬體的 DEP，或未針對記憶體範圍中的熱新增記憶體裝置設定超過 4 GB，則必須明確地啟用 PAE。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-125">If the computer does not support hardware-enabled DEP or is not configured for hot-add memory devices in memory ranges beyond 4 GB, PAE must be explicitly enabled.</span></span>

<span data-ttu-id="1ebfc-126">若要明確啟用 PAE，請使用下列 [**BCDEdit/set**](/windows-hardware/drivers/devtest/bcdedit--set) 命令設定 **pae** 開機專案選項：</span><span class="sxs-lookup"><span data-stu-id="1ebfc-126">To explicitly enable PAE, use the following [**BCDEdit /set**](/windows-hardware/drivers/devtest/bcdedit--set) command to set the **pae** boot entry option:</span></span>

 <span data-ttu-id="1ebfc-127">**bcdedit/set \[ {ID} \] pae ForceEnable**</span><span class="sxs-lookup"><span data-stu-id="1ebfc-127">**bcdedit /set \[{ID}\] pae ForceEnable**</span></span>  


<span data-ttu-id="1ebfc-128">如果已啟用 DEP，則無法停用 PAE。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-128">IF DEP is enabled, PAE cannot be disabled.</span></span> <span data-ttu-id="1ebfc-129">使用下列 [**BCDEdit/set**](/windows-hardware/drivers/devtest/bcdedit--set) 命令來停用 DEP 和 PAE：</span><span class="sxs-lookup"><span data-stu-id="1ebfc-129">Use the following [**BCDEdit /set**](/windows-hardware/drivers/devtest/bcdedit--set) commands to disable both DEP and PAE:</span></span>

 <span data-ttu-id="1ebfc-130">**bcdedit/set \[ {ID} \] nx AlwaysOff**</span><span class="sxs-lookup"><span data-stu-id="1ebfc-130">**bcdedit /set \[{ID}\] nx AlwaysOff**</span></span>  
<span data-ttu-id="1ebfc-131">**bcdedit/set \[ {ID} \] pae ForceDisable**</span><span class="sxs-lookup"><span data-stu-id="1ebfc-131">**bcdedit /set \[{ID}\] pae ForceDisable**</span></span>  


<span data-ttu-id="1ebfc-132">**Windows Server 2003 和 WINDOWS XP：** 若要啟用 PAE，請使用 [boot.ini](/windows-hardware/drivers/devtest/overview-of-the-boot-ini-file)檔案中的 **/pae** 參數。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-132">**Windows Server 2003 and Windows XP:** To enable PAE, use the **/PAE** switch in the [boot.ini](/windows-hardware/drivers/devtest/overview-of-the-boot-ini-file) file.</span></span> <span data-ttu-id="1ebfc-133">若要停用 PAE，請使用 **/NOPAE** 參數。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-133">To disable PAE, use the **/NOPAE** switch.</span></span> <span data-ttu-id="1ebfc-134">若要停用 DEP，請使用 **/EXECUTE** 參數。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-134">To disable DEP, use the **/EXECUTE** switch.</span></span>

## <a name="comparing-pae-and-other-large-memory-support"></a><span data-ttu-id="1ebfc-135">比較 PAE 和其他海量儲存體支援</span><span class="sxs-lookup"><span data-stu-id="1ebfc-135">Comparing PAE and other Large Memory Support</span></span>

<span data-ttu-id="1ebfc-136">PAE、 [4 gb 調整](4-gigabyte-tuning.md) (4gt) ，以及 [定址視窗擴充](address-windowing-extensions.md) (AWE) 提供不同的用途，並可獨立使用：</span><span class="sxs-lookup"><span data-stu-id="1ebfc-136">PAE, [4-gigabyte tuning](4-gigabyte-tuning.md) (4GT), and [Address Windowing Extensions](address-windowing-extensions.md) (AWE) serve different purposes and can be used independently of each other:</span></span>

-   <span data-ttu-id="1ebfc-137">PAE 可讓作業系統存取及使用超過 4 GB 的實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-137">PAE allows the operating system to access and use more than 4 GB of physical memory.</span></span>
-   <span data-ttu-id="1ebfc-138">4GT 可將進程可用的虛擬位址空間部分從 2 GB 增加至最多 3 GB。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-138">4GT increases the portion of the virtual address space that is available to a process from 2 GB to up to 3 GB.</span></span>
-   <span data-ttu-id="1ebfc-139">AWE 是一組 Api，可讓處理常式配置未分頁的實體記憶體，然後將此記憶體的部分動態對應到進程的虛擬位址空間中。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-139">AWE is a set of APIs that allows a process to allocate nonpaged physical memory and then dynamically map portions of this memory into the virtual address space of the process.</span></span>

<span data-ttu-id="1ebfc-140">如果沒有使用4GT 或 AWE，單一32位進程可使用的實體記憶體數量受限於 (2 GB) 的位址空間大小。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-140">When neither 4GT nor AWE are being used, the amount of physical memory that a single 32-bit process can use is limited by the size of its address space (2 GB).</span></span> <span data-ttu-id="1ebfc-141">在此情況下，啟用 PAE 的系統仍可使用超過 4 GB 的 RAM，同時執行多個進程或將檔案資料快取到記憶體中。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-141">In this case, a PAE-enabled system can still make use of more than 4 GB of RAM to run multiple processes at the same time or to cache file data in memory.</span></span>

<span data-ttu-id="1ebfc-142">您可以搭配或不使用 PAE 來使用4GT。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-142">4GT can be used with or without PAE.</span></span> <span data-ttu-id="1ebfc-143">不過，某些版本的 Windows 會限制使用4GT 時可支援的實體記憶體數量上限。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-143">However, some versions of Windows limit the maximum amount of physical memory that can be supported when 4GT is used.</span></span> <span data-ttu-id="1ebfc-144">在這類系統上，以4GT 啟用開機會導致作業系統略過超過限制的記憶體。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-144">On such systems, booting with 4GT enabled causes the operating system to ignore any memory in excess of the limit.</span></span>

<span data-ttu-id="1ebfc-145">AWE 不需要 PAE 或4GT，但通常會與 PAE 一起使用，從單一32位進程配置超過 4 GB 的實體記憶體。</span><span class="sxs-lookup"><span data-stu-id="1ebfc-145">AWE does not require PAE or 4GT but is often used together with PAE to allocate more than 4 GB of physical memory from a single 32-bit process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ebfc-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="1ebfc-146">Related topics</span></span>



[<span data-ttu-id="1ebfc-147">**IsProcessorFeaturePresent**</span><span class="sxs-lookup"><span data-stu-id="1ebfc-147">**IsProcessorFeaturePresent**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent)
</dt> <dt>

<span data-ttu-id="1ebfc-148">[PAE X86 技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc728455(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="1ebfc-148">[PAE X86 Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc728455(v=ws.10))</span></span>
</dt> </dl>

 

 
