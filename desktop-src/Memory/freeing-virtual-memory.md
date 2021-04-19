---
description: VirtualFree 函式會根據下列規則來解除和釋放頁面。
ms.assetid: 8fbd7960-f3f0-4326-ad1d-12b636c0039e
title: 釋放虛擬記憶體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7628ed53f956d5cd13f0c7d2d1157443d529129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973827"
---
# <a name="freeing-virtual-memory"></a><span data-ttu-id="9d006-103">釋放虛擬記憶體</span><span class="sxs-lookup"><span data-stu-id="9d006-103">Freeing Virtual Memory</span></span>

<span data-ttu-id="9d006-104">[**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree)函式會根據下列規則來解除和釋放頁面：</span><span class="sxs-lookup"><span data-stu-id="9d006-104">The [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) function decommits and releases pages according to the following rules:</span></span>

-   <span data-ttu-id="9d006-105">解除一或多個認可的頁面，並將頁面的狀態變更為「已保留」。</span><span class="sxs-lookup"><span data-stu-id="9d006-105">Decommits one or more committed pages, changing the state of the pages to reserved.</span></span> <span data-ttu-id="9d006-106">Decommitting 頁面會釋放與頁面相關聯的實體儲存體，使其可供任何程式配置。</span><span class="sxs-lookup"><span data-stu-id="9d006-106">Decommitting pages releases the physical storage associated with the pages, making it available to be allocated by any process.</span></span> <span data-ttu-id="9d006-107">您可以已取消認可任何已認可頁面的區塊。</span><span class="sxs-lookup"><span data-stu-id="9d006-107">Any block of committed pages can be decommitted.</span></span>
-   <span data-ttu-id="9d006-108">釋放一或多個保留頁面的區塊，將頁面的狀態變更為「可用」。</span><span class="sxs-lookup"><span data-stu-id="9d006-108">Releases a block of one or more reserved pages, changing the state of the pages to free.</span></span> <span data-ttu-id="9d006-109">釋出頁面區塊，可讓處理常式配置保留位址的範圍。</span><span class="sxs-lookup"><span data-stu-id="9d006-109">Releasing a block of pages makes the range of reserved addresses available to be allocated by the process.</span></span> <span data-ttu-id="9d006-110">只有釋放 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)最初保留的整個區塊，才能釋放保留的頁面。</span><span class="sxs-lookup"><span data-stu-id="9d006-110">Reserved pages can be released only by freeing the entire block that was initially reserved by [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc).</span></span>
-   <span data-ttu-id="9d006-111">將一或多個認可頁面的區塊同時解除鎖定，並將頁面的狀態變更為「可用」。</span><span class="sxs-lookup"><span data-stu-id="9d006-111">Decommits and releases a block of one or more committed pages simultaneously, changing the state of the pages to free.</span></span> <span data-ttu-id="9d006-112">指定的區塊必須包含最初由 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)保留的整個區塊，而且所有的頁面都必須目前已認可。</span><span class="sxs-lookup"><span data-stu-id="9d006-112">The specified block must include the entire block initially reserved by [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), and all of the pages must be currently committed.</span></span>

<span data-ttu-id="9d006-113">當記憶體區塊釋出或已取消認可之後，您就不能再次參考它。</span><span class="sxs-lookup"><span data-stu-id="9d006-113">After a memory block is released or decommitted, you can never refer to it again.</span></span> <span data-ttu-id="9d006-114">在該記憶體中可能存在的任何資訊都將永遠消失。</span><span class="sxs-lookup"><span data-stu-id="9d006-114">Any information that may have been in that memory is gone forever.</span></span> <span data-ttu-id="9d006-115">嘗試讀取或寫入免費頁面會導致存取違規例外狀況。</span><span class="sxs-lookup"><span data-stu-id="9d006-115">Attempting to read from or write to a free page results in an access violation exception.</span></span> <span data-ttu-id="9d006-116">如果您需要資訊，請勿取消認可或釋放包含該資訊的記憶體。</span><span class="sxs-lookup"><span data-stu-id="9d006-116">If you require information, do not decommit or free memory containing that information.</span></span>

<span data-ttu-id="9d006-117">若要指定不再有興趣的記憶體範圍中的資料，請使用 VirtualAlloc **\_ 重設** 來呼叫 [](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) 。</span><span class="sxs-lookup"><span data-stu-id="9d006-117">To specify that the data in a memory range is no longer of interest, call [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) with **MEM\_RESET**.</span></span> <span data-ttu-id="9d006-118">頁面不會讀取或寫入分頁檔案。</span><span class="sxs-lookup"><span data-stu-id="9d006-118">The pages will not be read from or written to the paging file.</span></span> <span data-ttu-id="9d006-119">不過，您可以稍後再使用記憶體區塊。</span><span class="sxs-lookup"><span data-stu-id="9d006-119">However, the memory block can be used again later.</span></span>

 

 
