---
description: 32位系統上的系統虛擬位址 (VA) 空間，可能會因為片段而用盡。 您可以使用數個登錄機碼，在遇到此問題的32位系統上設定記憶體限制。
ms.assetid: ec2a8c6b-cd8e-4085-b337-02f78a210bb5
title: 記憶體管理登錄機碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48e8c53bd54f8caeb82aad58ceed61cc5644c112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852948"
---
# <a name="memory-management-registry-keys"></a><span data-ttu-id="6d571-104">記憶體管理登錄機碼</span><span class="sxs-lookup"><span data-stu-id="6d571-104">Memory Management Registry Keys</span></span>

<span data-ttu-id="6d571-105">32位系統上的系統虛擬位址 (VA) 空間，可能會因為片段而用盡。</span><span class="sxs-lookup"><span data-stu-id="6d571-105">System virtual address (VA) space on 32-bit systems can become exhausted due to fragmentation.</span></span> <span data-ttu-id="6d571-106">您可以使用數個登錄機碼，在遇到此問題的32位系統上設定記憶體限制。</span><span class="sxs-lookup"><span data-stu-id="6d571-106">Several registry keys can be used to configure memory limits on 32-bit systems that experience this issue.</span></span> <span data-ttu-id="6d571-107">64位系統上的系統 VA 空間不受片段的耗盡，因此，這些金鑰組64位系統沒有任何影響。</span><span class="sxs-lookup"><span data-stu-id="6d571-107">System VA space on 64-bit systems is not subject to exhaustion by fragmentation; therefore, these keys have no effect on 64-bit systems.</span></span>

<span data-ttu-id="6d571-108">若為32位系統，您必須在下列登錄機碼底下明確建立這些記憶體管理登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="6d571-108">For 32-bit systems, these memory management registry keys must be explicitly created under the following registry key:</span></span>

<span data-ttu-id="6d571-109">**HKEY \_本機 \_ 電腦** \\ **系統** \\ **目前的控制集** \\ **控制** \\ **會話管理員** \\ **記憶體管理**</span><span class="sxs-lookup"><span data-stu-id="6d571-109">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**Current Control Set**\\**Control**\\**Session Manager**\\**Memory Management**</span></span>

<span data-ttu-id="6d571-110">**Windows Server 2008 和 Windows Vista：** 從 Windows Server 2008 和 Windows Vista Service Pack 1 (SP1) 開始，這些登錄機碼可在32位系統上使用。</span><span class="sxs-lookup"><span data-stu-id="6d571-110">**Windows Server 2008 and Windows Vista:** These registry keys are available on 32-bit systems starting with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="6d571-111">若為32位和64位系統上的預設記憶體和位址空間限制，請參閱 [Windows 版本的記憶體限制](memory-limits-for-windows-releases.md)。</span><span class="sxs-lookup"><span data-stu-id="6d571-111">For default memory and address space limits on both 32-bit and 64-bit systems, see [Memory Limits for Windows Releases](memory-limits-for-windows-releases.md).</span></span>

<span data-ttu-id="6d571-112">下表描述可用來在32位系統上設定記憶體限制的記憶體管理登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="6d571-112">The following table describes the memory management registry keys that can be used to configure memory limits on 32-bit systems.</span></span> <span data-ttu-id="6d571-113">所有這些索引鍵都具有 REG \_ DWORD 類型，以及範圍從0到 2048 MB 的可能值。</span><span class="sxs-lookup"><span data-stu-id="6d571-113">All of these keys have a REG\_DWORD type and possible values that range from 0 through 2,048 MB.</span></span> <span data-ttu-id="6d571-114">預設值為0，表示不會強制執行任何限制。</span><span class="sxs-lookup"><span data-stu-id="6d571-114">The default is 0, which means no limit is enforced.</span></span> <span data-ttu-id="6d571-115">值會自動四捨五入至下一個系統 VA 配置界限，也就是32位系統上的 2 MB，其 [實體位址延伸](physical-address-extension.md) (pae) 啟用，而32位系統上的 4 mb 未啟用 pae。</span><span class="sxs-lookup"><span data-stu-id="6d571-115">Values are automatically rounded up to the next system VA allocation boundary, which is 2 MB on 32-bit systems that have [Physical Address Extension](physical-address-extension.md) (PAE) enabled and 4 MB on 32-bit systems that do not have PAE enabled.</span></span>



| <span data-ttu-id="6d571-116">Key</span><span class="sxs-lookup"><span data-stu-id="6d571-116">Key</span></span>                   | <span data-ttu-id="6d571-117">描述</span><span class="sxs-lookup"><span data-stu-id="6d571-117">Description</span></span>                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d571-118">**NonPagedPoolLimit**</span><span class="sxs-lookup"><span data-stu-id="6d571-118">**NonPagedPoolLimit**</span></span> | <span data-ttu-id="6d571-119">指定可供非分頁集區使用的系統 VA 空間數量上限。</span><span class="sxs-lookup"><span data-stu-id="6d571-119">Specifies the maximum amount of system VA space that can be used by the nonpaged pool.</span></span> <span data-ttu-id="6d571-120">在某些情況下，這項限制可能會超過一小部分。</span><span class="sxs-lookup"><span data-stu-id="6d571-120">Under certain conditions, this limit may be exceeded by a small amount.</span></span> |
| <span data-ttu-id="6d571-121">**PagedPoolLimit**</span><span class="sxs-lookup"><span data-stu-id="6d571-121">**PagedPoolLimit**</span></span>    | <span data-ttu-id="6d571-122">指定可供分頁集區使用的系統 VA 空間數量上限。</span><span class="sxs-lookup"><span data-stu-id="6d571-122">Specifies the maximum amount of system VA space that can be used by the paged pool.</span></span>                                                                            |
| <span data-ttu-id="6d571-123">**SessionSpaceLimit**</span><span class="sxs-lookup"><span data-stu-id="6d571-123">**SessionSpaceLimit**</span></span> | <span data-ttu-id="6d571-124">指定會話空間配置可以使用的系統 VA 空間數量上限。</span><span class="sxs-lookup"><span data-stu-id="6d571-124">Specifies the maximum amount of system VA space that can be used by session space allocations.</span></span>                                                                 |
| <span data-ttu-id="6d571-125">**SystemCacheLimit**</span><span class="sxs-lookup"><span data-stu-id="6d571-125">**SystemCacheLimit**</span></span>  | <span data-ttu-id="6d571-126">指定系統快取可使用的系統 VA 空間數量上限。</span><span class="sxs-lookup"><span data-stu-id="6d571-126">Specifies the maximum amount of system VA space that can be used by the system cache.</span></span> <span data-ttu-id="6d571-127">在某些情況下，這項限制可能會超過一小部分。</span><span class="sxs-lookup"><span data-stu-id="6d571-127">Under certain conditions, this limit may be exceeded by a small amount.</span></span>  |
| <span data-ttu-id="6d571-128">**SystemPtesLimit**</span><span class="sxs-lookup"><span data-stu-id="6d571-128">**SystemPtesLimit**</span></span>   | <span data-ttu-id="6d571-129">指定使用系統分頁表專案 (Pte) 的 i/o 對應和其他資源可以使用的最大系統 VA 空間量。</span><span class="sxs-lookup"><span data-stu-id="6d571-129">Specifies the maximum amount of system VA space that can be used by I/O mappings and other resources that consume system page table entries (PTEs).</span></span>            |



 

<span data-ttu-id="6d571-130">判斷系統 VA 空間是否已用盡，需要使用內核偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="6d571-130">Determining whether system VA space is being exhausted requires the use of a kernel debugger.</span></span> <span data-ttu-id="6d571-131">如需詳細資訊，請參閱＜ [Windows 偵錯工具](https://msdn.microsoft.com/library/cc267445.aspx)＞。</span><span class="sxs-lookup"><span data-stu-id="6d571-131">For more information, see [Debugging Tools for Windows](https://msdn.microsoft.com/library/cc267445.aspx).</span></span>

 

 



