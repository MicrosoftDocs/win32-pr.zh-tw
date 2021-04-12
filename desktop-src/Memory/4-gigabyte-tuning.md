---
description: 4 gb 調整： BCDEdit 和 Boot.ini
ms.assetid: 991eb86f-9e6f-4084-8b6f-f979e42104b5
title: 4 gb 調整： BCDEdit 和 Boot.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f997ae09748370d5ec8ec246da80b6440d7aaf45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192658"
---
# <a name="4-gigabyte-tuning-bcdedit-and-bootini"></a><span data-ttu-id="c533b-103">4 gb 調整： BCDEdit 和 Boot.ini</span><span class="sxs-lookup"><span data-stu-id="c533b-103">4-Gigabyte Tuning: BCDEdit and Boot.ini</span></span>

<span data-ttu-id="c533b-104">在32位版本的 Windows 上，應用程式有 4 gb 的可用虛擬位址空間 (GB) 。</span><span class="sxs-lookup"><span data-stu-id="c533b-104">On 32-bit editions of Windows, applications have 4 gigabyte (GB) of virtual address space available.</span></span> <span data-ttu-id="c533b-105">虛擬位址空間已分割，因此應用程式可以使用 2 GB，而其他 2 GB 僅供系統使用。</span><span class="sxs-lookup"><span data-stu-id="c533b-105">The virtual address space is divided so that 2 GB is available to the application and the other 2 GB is available only to the system.</span></span> <span data-ttu-id="c533b-106">4 gb 調整 (4GT 或 4GT RAM 調整) 功能（使用 *BCDEdit/set increaseuserva* 命令啟用）會增加應用程式可用的虛擬位址空間（最多 3 GB），並將可供系統使用的空間減少為1到 2 gb。</span><span class="sxs-lookup"><span data-stu-id="c533b-106">The 4-gigabyte tuning (4GT or 4GT RAM Tuning) feature, enabled with the *BCDEdit /set increaseuserva* command, increases the virtual address space that is available to the application up to 3 GB, and reduces the amount available to the system to between 1 and 2 GB.</span></span>

<span data-ttu-id="c533b-107">對於需要海量儲存體的應用程式（例如 (DBMS) 的資料庫管理系統），使用較大的虛擬位址空間可提供可觀的效能和擴充性優勢。</span><span class="sxs-lookup"><span data-stu-id="c533b-107">For applications that are memory-intensive, such as database management systems (DBMS), the use of a larger virtual address space can provide considerable performance and scalability benefits.</span></span> <span data-ttu-id="c533b-108">不過，檔案快取、分頁集區和非分頁集區較小，可能會對具有大量網路或 i/o 的應用程式造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="c533b-108">However, the file cache, paged pool, and nonpaged pool are smaller, which can adversely affect applications with heavy networking or I/O.</span></span> <span data-ttu-id="c533b-109">因此，您可能會想要在負載下測試您的應用程式，並檢查效能計數器，以判斷您的應用程式是否受益于較大的位址空間。</span><span class="sxs-lookup"><span data-stu-id="c533b-109">Therefore, you might want to test your application under load, and examine the performance counters to determine whether your application benefits from the larger address space.</span></span>

<span data-ttu-id="c533b-110">若要啟用4GT，請使用 [BCDEdit/set](/windows-hardware/drivers/devtest/bcdedit--set) 命令將 **increaseuserva** 開機專案選項設定為介於 2048 (2 GB) 和 3072 (3 GB) 之間的值。</span><span class="sxs-lookup"><span data-stu-id="c533b-110">To enable 4GT, use the [BCDEdit /set](/windows-hardware/drivers/devtest/bcdedit--set) command to set the **increaseuserva** boot entry option to a value between 2048 (2 GB) and 3072 (3 GB).</span></span>

<span data-ttu-id="c533b-111">**Windows Server 2003 及更早版本：** 若要啟用4GT，請將 **/3gb** 參數新增至 Boot.ini 檔案。</span><span class="sxs-lookup"><span data-stu-id="c533b-111">**Windows Server 2003 and earlier:** To enable 4GT, add the **/3GB** switch to the Boot.ini file.</span></span> <span data-ttu-id="c533b-112">下列系統支援 **/3gb** 參數：</span><span class="sxs-lookup"><span data-stu-id="c533b-112">The **/3GB** switch is supported on the following systems:</span></span>

-   <span data-ttu-id="c533b-113">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c533b-113">Windows Server 2003</span></span>
-   <span data-ttu-id="c533b-114">Windows XP Professional</span><span class="sxs-lookup"><span data-stu-id="c533b-114">Windows XP Professional</span></span>

<span data-ttu-id="c533b-115">**/3gb** 參數會為應用程式提供完整的 3 GB 虛擬位址空間，並將系統可用數量減少為 1 GB。</span><span class="sxs-lookup"><span data-stu-id="c533b-115">The **/3GB** switch makes a full 3 GB of virtual address space available to applications and reduces the amount available to the system to 1 GB.</span></span> <span data-ttu-id="c533b-116">在 Windows Server 2003 上，可以調整應用程式可用的位址空間量，方法是將 Boot.ini 中的 **/USERVA** 參數設定為介於2048和3072之間的值，這樣會增加系統可用的位址空間量。</span><span class="sxs-lookup"><span data-stu-id="c533b-116">On Windows Server 2003, the amount of address space available to applications can be adjusted by setting the **/USERVA** switch in Boot.ini to a value between 2048 and 3072, which increases the amount of address space available to the system.</span></span> <span data-ttu-id="c533b-117">當應用程式需要 2 GB 以上的位址空間時，這有助於維護整體系統效能。</span><span class="sxs-lookup"><span data-stu-id="c533b-117">This can help maintain overall system performance when the application requires more than 2 GB but less than 3 GB of address space.</span></span>

<span data-ttu-id="c533b-118">若要讓應用程式使用較大的位址空間，請在映射標頭中設定 [**影像檔案的 \_ \_ 大型 \_ 位址 \_ 感知**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) 旗標。</span><span class="sxs-lookup"><span data-stu-id="c533b-118">To enable an application to use the larger address space, set the [**IMAGE\_FILE\_LARGE\_ADDRESS\_AWARE**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) flag in the image header.</span></span> <span data-ttu-id="c533b-119">Microsoft Visual C++ 隨附的連結器支援 **/LARGEADDRESSAWARE** 參數，以設定此旗標。</span><span class="sxs-lookup"><span data-stu-id="c533b-119">The linker included with Microsoft Visual C++ supports the **/LARGEADDRESSAWARE** switch to set this flag.</span></span> <span data-ttu-id="c533b-120">設定此旗標，然後在沒有4GT 支援的系統上執行應用程式時，應該不會影響應用程式。</span><span class="sxs-lookup"><span data-stu-id="c533b-120">Setting this flag and then running the application on a system that does not have 4GT support should not affect the application.</span></span>

<span data-ttu-id="c533b-121">在64位版本的 Windows 中，以 [**圖像 \_ 檔案 \_ 大型 \_ 位址 \_ 感知**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) 旗標標記的32位應用程式有 4 GB 的可用位址空間。</span><span class="sxs-lookup"><span data-stu-id="c533b-121">On 64-bit editions of Windows, 32-bit applications marked with the [**IMAGE\_FILE\_LARGE\_ADDRESS\_AWARE**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) flag have 4 GB of address space available.</span></span>

<span data-ttu-id="c533b-122">**Itanium 版本的 Windows Server 2003：** 在 SP1 之前，32位進程只有 2 GB 的位址空間可用。</span><span class="sxs-lookup"><span data-stu-id="c533b-122">**Itanium editions of Windows Server 2003:** Prior to SP1, 32-bit processes have only 2 GB of address space available.</span></span>

<span data-ttu-id="c533b-123">使用下列指導方針來支援應用程式中的4GT：</span><span class="sxs-lookup"><span data-stu-id="c533b-123">Use the following guidelines to support 4GT in applications:</span></span>

-   <span data-ttu-id="c533b-124">接近 2 GB 界限的位址通常會由各種系統 Dll 使用。</span><span class="sxs-lookup"><span data-stu-id="c533b-124">Addresses near the 2-GB boundary are typically used by various system DLLs.</span></span> <span data-ttu-id="c533b-125">因此，即使有整個 4 GB 的位址空間可供使用，32位程式也無法配置超過 2 GB 的連續記憶體。</span><span class="sxs-lookup"><span data-stu-id="c533b-125">Therefore, a 32-bit process cannot allocate more than 2 GB of contiguous memory, even if the entire 4-GB address space is available.</span></span>
-   <span data-ttu-id="c533b-126">若要取得總使用者虛擬空間的數量，請使用 [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) 函數。</span><span class="sxs-lookup"><span data-stu-id="c533b-126">To retrieve the amount of total user virtual space, use the [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) function.</span></span> <span data-ttu-id="c533b-127">若要取得可能的最高使用者位址，請使用 [**GetSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="c533b-127">To retrieve the highest possible user address, use the [**GetSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) function.</span></span> <span data-ttu-id="c533b-128">一律在執行時間偵測實際值，並避免使用硬式有線常數定義，例如： `#define HIGHEST_USER_ADDRESS 0xC0000000` 。</span><span class="sxs-lookup"><span data-stu-id="c533b-128">Always detect the real value at runtime, and avoid using hard-wired constant definitions such as: `#define HIGHEST_USER_ADDRESS 0xC0000000`.</span></span>
-   <span data-ttu-id="c533b-129">避免與指標進行簽署的比較，因為它們可能會導致應用程式在啟用4GT 的系統上損毀。</span><span class="sxs-lookup"><span data-stu-id="c533b-129">Avoid signed comparisons with pointers, because they might cause applications to crash on a 4GT-enabled system.</span></span> <span data-ttu-id="c533b-130">在 2 GB 以上的指標，如下所示的條件為 false： `if (pointer > 40000000)` 。</span><span class="sxs-lookup"><span data-stu-id="c533b-130">A condition such as the following is false for a pointer that is above 2 GB: `if (pointer > 40000000)`.</span></span>
-   <span data-ttu-id="c533b-131">當4GT 啟用時，針對應用程式定義目的使用指標最高位的程式碼將會失敗。</span><span class="sxs-lookup"><span data-stu-id="c533b-131">Code that uses the highest bit of a pointer for an application-defined purpose will fail when 4GT is enabled.</span></span> <span data-ttu-id="c533b-132">例如，如果32位字低於0x80000000，可能會被視為使用者模式位址，如果有的話，則會被視為錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c533b-132">For example, a 32-bit word might be considered a user-mode address if it is below 0x80000000, and an error code if above.</span></span> <span data-ttu-id="c533b-133">這對4GT 的情況並不成立。</span><span class="sxs-lookup"><span data-stu-id="c533b-133">This is not true with 4GT.</span></span>

<span data-ttu-id="c533b-134">[**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) 通常會傳回較高位址之前的低位址。</span><span class="sxs-lookup"><span data-stu-id="c533b-134">[**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) usually returns low addresses before high addresses.</span></span> <span data-ttu-id="c533b-135">因此，除非配置海量儲存體或有分散的虛擬位址空間，否則您的進程可能不會使用非常高的位址。</span><span class="sxs-lookup"><span data-stu-id="c533b-135">Therefore, your process may not use very high addresses unless it allocates a lot of memory or has a fragmented virtual address space.</span></span> <span data-ttu-id="c533b-136">若要強制配置在較低位址之前從較高的位址配置以供測試之用，請在呼叫 **VirtualAlloc** 或將下列登錄值設定為0x100000 時，指定 [**記憶體 \_ 上限 \_** ]：</span><span class="sxs-lookup"><span data-stu-id="c533b-136">To force allocations to allocate from higher addresses before lower addresses for testing purposes, specify **MEM\_TOP\_DOWN** when calling **VirtualAlloc** or set the following registry value to 0x100000:</span></span>

<span data-ttu-id="c533b-137">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制** \\ **會話管理員** \\ **記憶體管理** \\ **AllocationPreference**</span><span class="sxs-lookup"><span data-stu-id="c533b-137">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Session Manager**\\**Memory Management**\\**AllocationPreference**</span></span>

## <a name="related-topics"></a><span data-ttu-id="c533b-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="c533b-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c533b-139">Windows 版本的記憶體限制</span><span class="sxs-lookup"><span data-stu-id="c533b-139">Memory Limits for Windows Releases</span></span>](memory-limits-for-windows-releases.md)
</dt> <dt>

[<span data-ttu-id="c533b-140">實體位址擴充功能</span><span class="sxs-lookup"><span data-stu-id="c533b-140">Physical Address Extension</span></span>](physical-address-extension.md)
</dt> <dt>

<span data-ttu-id="c533b-141">[4 GT 技術參考](/previous-versions/windows/it-pro/windows-server-2003/cc778496(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="c533b-141">[4GT Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc778496(v=ws.10))</span></span>
</dt> </dl>

 

 
