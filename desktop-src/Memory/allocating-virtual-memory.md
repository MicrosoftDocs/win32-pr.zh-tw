---
description: 虛擬記憶體函式會操作分頁的記憶體。 這些函數會使用目前電腦上的頁面大小，來將指定的大小和位址四捨五入。
ms.assetid: 509cd529-ff79-4b07-9e09-3c5ae65f6cba
title: 配置虛擬記憶體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f42b4f7eb9d5de3c8c5e9339c9e5931a89e371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319124"
---
# <a name="allocating-virtual-memory"></a><span data-ttu-id="d9243-104">配置虛擬記憶體</span><span class="sxs-lookup"><span data-stu-id="d9243-104">Allocating Virtual Memory</span></span>

<span data-ttu-id="d9243-105">虛擬記憶體函式會操作分頁的記憶體。</span><span class="sxs-lookup"><span data-stu-id="d9243-105">The virtual memory functions manipulate pages of memory.</span></span> <span data-ttu-id="d9243-106">這些函數會使用目前電腦上的頁面大小，來將指定的大小和位址四捨五入。</span><span class="sxs-lookup"><span data-stu-id="d9243-106">The functions use the size of a page on the current computer to round off specified sizes and addresses.</span></span>

<span data-ttu-id="d9243-107">[**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)函式會執行下列其中一項作業：</span><span class="sxs-lookup"><span data-stu-id="d9243-107">The [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function performs one of the following operations:</span></span>

-   <span data-ttu-id="d9243-108">保留一或多個可用的頁面。</span><span class="sxs-lookup"><span data-stu-id="d9243-108">Reserves one or more free pages.</span></span>
-   <span data-ttu-id="d9243-109">認可一或多個保留的頁面。</span><span class="sxs-lookup"><span data-stu-id="d9243-109">Commits one or more reserved pages.</span></span>
-   <span data-ttu-id="d9243-110">保留並認可一或多個可用的頁面。</span><span class="sxs-lookup"><span data-stu-id="d9243-110">Reserves and commits one or more free pages.</span></span>

<span data-ttu-id="d9243-111">您可以指定要保留或認可之頁面的起始位址，也可以讓系統判斷位址。</span><span class="sxs-lookup"><span data-stu-id="d9243-111">You can specify the starting address of the pages to be reserved or committed, or you can allow the system to determine the address.</span></span> <span data-ttu-id="d9243-112">函數會將指定的位址四捨五入至適當的頁面界限。</span><span class="sxs-lookup"><span data-stu-id="d9243-112">The function rounds the specified address to the appropriate page boundary.</span></span> <span data-ttu-id="d9243-113">保留的頁面無法存取，但是認可的頁面可以使用 **page \_ READWRITE**、 **page \_ READONLY** 或 **page \_ NOACCESS** access 來配置。</span><span class="sxs-lookup"><span data-stu-id="d9243-113">Reserved pages are not accessible, but committed pages can be allocated with **PAGE\_READWRITE**, **PAGE\_READONLY**, or **PAGE\_NOACCESS** access.</span></span> <span data-ttu-id="d9243-114">認可頁面時，會從 RAM 的整體大小和磁片上的分頁檔案配置記憶體費用，但每個頁面只會在第一次嘗試讀取或寫入該頁面時，初始化並載入實體記憶體中。</span><span class="sxs-lookup"><span data-stu-id="d9243-114">When pages are committed, memory charges are allocated from the overall size of RAM and paging files on disk, but each page is initialized and loaded into physical memory only at the first attempt to read from or write to that page.</span></span> <span data-ttu-id="d9243-115">您可以使用一般指標參考來存取 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) 函數所認可的記憶體。</span><span class="sxs-lookup"><span data-stu-id="d9243-115">You can use normal pointer references to access memory committed by the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function.</span></span>

 

 
