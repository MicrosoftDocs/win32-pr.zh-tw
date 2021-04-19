---
description: 支援大型頁面可讓伺服器應用程式建立大型頁面的記憶體區域，這在64位的 Windows 上特別有用。
ms.assetid: 060115af-38d1-499c-b30c-47cd0cf42d20
title: Large-Page 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4578b5127e6613f2ff4b6e0b8a7cffcc53c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985608"
---
# <a name="large-page-support"></a><span data-ttu-id="6ed01-103">Large-Page 支援</span><span class="sxs-lookup"><span data-stu-id="6ed01-103">Large-Page Support</span></span>

<span data-ttu-id="6ed01-104">支援大型頁面可讓伺服器應用程式建立大型頁面的記憶體區域，這在64位的 Windows 上特別有用。</span><span class="sxs-lookup"><span data-stu-id="6ed01-104">Large-page support enables server applications to establish large-page memory regions, which is particularly useful on 64-bit Windows.</span></span> <span data-ttu-id="6ed01-105">每個大型頁面轉譯都會使用 CPU 內的單一轉譯緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6ed01-105">Each large-page translation uses a single translation buffer inside the CPU.</span></span> <span data-ttu-id="6ed01-106">這個緩衝區的大小通常會大於原生頁面大小的三個數量級順序;這會提高轉譯緩衝區的效率，進而提高經常存取之記憶體的效能。</span><span class="sxs-lookup"><span data-stu-id="6ed01-106">The size of this buffer is typically three orders of magnitude larger than the native page size; this increases the efficiency of the translation buffer, which can increase performance for frequently accessed memory.</span></span>

<span data-ttu-id="6ed01-107">下列程式說明如何使用大型頁面支援。</span><span class="sxs-lookup"><span data-stu-id="6ed01-107">The following procedure describes how to use large-page support.</span></span>

<span data-ttu-id="6ed01-108">**使用大型頁面支援**</span><span class="sxs-lookup"><span data-stu-id="6ed01-108">**To use large-page support**</span></span>

1.  <span data-ttu-id="6ed01-109">藉由呼叫 [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges)函數來取得 **SeLockMemoryPrivilege** 許可權。</span><span class="sxs-lookup"><span data-stu-id="6ed01-109">Obtain the **SeLockMemoryPrivilege** privilege by calling the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function.</span></span> <span data-ttu-id="6ed01-110">如需詳細資訊，請參閱將 [許可權指派給帳戶](../secbp/assigning-privileges-to-an-account.md) 和 [變更權杖中的許可權](../secbp/changing-privileges-in-a-token.md)。</span><span class="sxs-lookup"><span data-stu-id="6ed01-110">For more information, see [Assigning Privileges to an Account](../secbp/assigning-privileges-to-an-account.md) and [Changing Privileges in a Token](../secbp/changing-privileges-in-a-token.md).</span></span>
2.  <span data-ttu-id="6ed01-111">藉由呼叫 [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) 函式來取得最小的大型頁面大小。</span><span class="sxs-lookup"><span data-stu-id="6ed01-111">Retrieve the minimum large-page size by calling the [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) function.</span></span>
3.  <span data-ttu-id="6ed01-112">呼叫 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)函數時，請包含 **記憶體 \_ 大型 \_ 頁面** 的值。</span><span class="sxs-lookup"><span data-stu-id="6ed01-112">Include the **MEM\_LARGE\_PAGES** value when calling the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function.</span></span> <span data-ttu-id="6ed01-113">大小和對齊方式必須是最大頁面的倍數。</span><span class="sxs-lookup"><span data-stu-id="6ed01-113">The size and alignment must be a multiple of the large-page minimum.</span></span>

<span data-ttu-id="6ed01-114">撰寫使用大型頁面記憶體的應用程式時，請記住下列考慮：</span><span class="sxs-lookup"><span data-stu-id="6ed01-114">When writing applications that use large-page memory, keep the following considerations in mind:</span></span>

-   <span data-ttu-id="6ed01-115">因為每個大型頁面的實體空間必須是連續的，但記憶體可能已被分割，所以在系統長時間執行之後，可能很難取得大型頁面的記憶體區域。</span><span class="sxs-lookup"><span data-stu-id="6ed01-115">Large-page memory regions may be difficult to obtain after the system has been running for a long time because the physical space for each large page must be contiguous, but the memory may have become fragmented.</span></span> <span data-ttu-id="6ed01-116">在這些情況下配置大型頁面可能會大幅影響系統效能。</span><span class="sxs-lookup"><span data-stu-id="6ed01-116">Allocating large pages under these conditions can significantly affect system performance.</span></span> <span data-ttu-id="6ed01-117">因此，應用程式應該避免進行重複的大型頁面配置，並且在啟動時，一次配置所有的大型頁面。</span><span class="sxs-lookup"><span data-stu-id="6ed01-117">Therefore, applications should avoid making repeated large-page allocations and instead allocate all large pages one time, at startup.</span></span>
-   <span data-ttu-id="6ed01-118">記憶體一律是讀取/寫入，且 nonpageable (永遠常駐于實體記憶體) 。</span><span class="sxs-lookup"><span data-stu-id="6ed01-118">The memory is always read/write and nonpageable (always resident in physical memory).</span></span>
-   <span data-ttu-id="6ed01-119">記憶體是進程私用位元組的一部分，而不是工作集的一部分，因為工作集的定義只包含可分頁的記憶體。</span><span class="sxs-lookup"><span data-stu-id="6ed01-119">The memory is part of the process private bytes but not part of the working set, because the working set by definition contains only pageable memory.</span></span>
-   <span data-ttu-id="6ed01-120">大型分頁配置不受限於作業限制。</span><span class="sxs-lookup"><span data-stu-id="6ed01-120">Large-page allocations are not subject to job limits.</span></span>
-   <span data-ttu-id="6ed01-121">您必須將大型頁面的記憶體保留和認可為單一作業。</span><span class="sxs-lookup"><span data-stu-id="6ed01-121">Large-page memory must be reserved and committed as a single operation.</span></span> <span data-ttu-id="6ed01-122">換句話說，大型頁面無法用來認可先前保留的記憶體範圍。</span><span class="sxs-lookup"><span data-stu-id="6ed01-122">In other words, large pages cannot be used to commit a previously reserved range of memory.</span></span>
-   <span data-ttu-id="6ed01-123">在 Intel Itanium 型系統上的 WOW64 不支援使用此功能的32位應用程式。</span><span class="sxs-lookup"><span data-stu-id="6ed01-123">WOW64 on Intel Itanium-based systems does not support 32-bit applications that use this feature.</span></span> <span data-ttu-id="6ed01-124">應用程式應該重新編譯為原生64位應用程式。</span><span class="sxs-lookup"><span data-stu-id="6ed01-124">The applications should be recompiled as native 64-bit applications.</span></span>

 

 
